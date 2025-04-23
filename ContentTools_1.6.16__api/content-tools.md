
ContentTools API documentation · ContentTools

































**ContentTools** aims to provide both a fully-functional content editor that can be used out of the box and a tool kit of classes and functions that can be used to build your own editor. The tool kit includes a lightweight set of user interface classes, a set of tools for performing common editing tasks, and a history stack for managing undo/redo. Whilst the components provided by the tool kit work well together, they can also be used or replaced as required.

The rest of this page is purely reference documentation for the **ContentTools** library, for usage guides and examples I recommend you read the [Getting Started](/getting-started) guide and other [Tutorials](/tutorials).

Reference
---------

The library consists of a collection of classes namespaced under **ContentTools**:

* **[Settings](#settings)**
* **[Functions](#functions)**
* **[ContentTools.EditorApp](#editor-app)**
* **[ContentTools.History](#history)**
* **[ContentTools.StylePalette](#style-palette)**
* **[ContentTools.Style](#style)**
* **[Tools](#tools)**
* **[ContentTools.ToolShelf](#tool-shelf)**
* **[ContentTools.Tool](#tool)**
* **[ContentTools.Event](#event)**
* **[ContentTools.ComponentUI](#component-ui)**
* **[ContentTools.WidgetUI](#widget-ui)**
* **[ContentTools.AnchoredComponentUI](#anchored-component-ui)**
* **[ContentTools.FlashUI](#flash-ui)**
* **[ContentTools.IgnitionUI](#ignition-ui)**
* **[ContentTools.InspectorUI](#inspector-ui)**
* **[ContentTools.TagUI](#tag-ui)**
* **[ContentTools.ModalUI](#modal-ui)**
* **[ContentTools.ToolboxUI](#toolbox-ui)**
* **[ContentTools.ToolUI](#tool-ui)**
* **[ContentTools.BaseDialogUI](#base-dialog-ui)**
* **[ContentTools.AnchoredDialogUI](#anchored-dialog-ui)**
* **[ContentTools.DialogUI](#dialog-ui)**
* **[ContentTools.ImageDialog](#image-dialog)**
* **[ContentTools.LinkDialog](#link-dialog)**
* **[ContentTools.PropertiesDialog](#properties-dialog)**
* **[ContentTools.TableDialog](#table-dialog)**
* **[ContentTools.VideoDialog](#video-dialog)**

### Settings

A number of settings are provided against the **ContentTools** namespace. These can be set directly.

DEFAULT\_TOOLS

The default tool configuration for the editor's toolbox. The format is an array of arrays, where each top level array is a grouping and each group array holds a list of tools specified by their registered name as a string.

```
// Defaults to
DEFAULT_TOOLS: [
    [
        'bold',
        'italic',
        'link',
        'align-left',
        'align-center',
        'align-right'
    ], [
        'heading',
        'subheading',
        'paragraph',
        'unordered-list',
        'ordered-list',
        'table',
        'indent',
        'unindent',
        'line-break'
    ], [
        'image',
        'video',
        'preformatted'
    ], [
        'undo',
        'redo',
        'remove'
    ]
]
```

DEFAULT\_VIDEO\_WIDTH, DEFAULT\_VIDEO\_HEIGHT

Default sizes for new videos when inserted.

*Defaults to **400** by **300***

HIGHLIGHT\_HOLD\_DURATION

If the user holds down the shift key for an extended period of time the editor will highlight the editable regions on the page. This setting determines how long the user must hold down the shift key to activate this feature.

*Defaults to **2000***

INSPECTOR\_IGNORED\_ELEMENTS

A list of element class names ignored by the inspector, typically because attributes cannot be safely set against them.

*Defaults to **[ListItemText, Region, TableCellText]***

IMAGE\_UPLOADER

A function that accepts an **ImageDialog**, the function then binds handlers to various events for the **ImageDialog** to implement support for uploading and manipulating images asynchronously *(see the [Handling image uploads](/tutorials/handling-image-uploads) tutorial)*.

*There is no default image uploader.*

MIN\_CROP

The minimum region that can be selected when cropping an image (in pixels).

*Defaults to **10***

RESTRICTED\_ATTRIBUTES

A map of restricted attributes; attributes which can't be viewed or modified in the properties dialog. The map is defined as an object with a list of restricted attributes against each tag name. Attribute and tag names must be specified in lower case.

Attribute and tag names must be specified in lower case.

```
// Defaults to
RESTRICTED_ATTRIBUTES: {
    '*': [],
    'img': ['height', 'src', 'width', 'data-ce-max-width', 'data-ce-min-width'],
    'iframe': ['height', 'width']
    }

```

'\*' is a special case tag name any attributes defined against it will be restricted for all tags.

### Functions

ContentTools.getEmbedVideoURL(url)

Validate/parse a video **url** and return a valid embed URL. Supports *YouTube* and *Vimeo* URLs.

ContentTools.getRestrictedAtributes(tagName)

Return a list of restricted attributes for the given **tagName**. This will include restricted attributes defined against all tags using **'\*'** as the tag name.

### EditorApp (inherits from [ComponentUI](#component-ui))

The **EditorApp** class is actually a wrapper class that provides singleton access to, by default, the out of the box content editor. Access is provided via the **get** class method like so:

```
var editor = EditorApp.get();
```

Whilst the reference below provides details of the methods for the default editor, if you're thinking of extending or rolling your own editor you will either want to use the **getCls** method to monkey patch or inherit from the default editor, and if you're inheriting or rolling your own you'll need to modify the EditorApp wrapper class so that it returns your new class, for example:

```
// Monkey patching default editor class
var editorClass = EditorApp.getCls();
editorClass.prototype.someMethod = function () { ...monkey, monkey... };

// Rolling your own
var MyEditor = function () {
    ... optionally extended using the `editorClass`...
};

// Patch the EditorApp wrapper class to support our new class
EditorApp.getCls = function () { return MyEditor; }
```

Writing your own editor from scratch requires you to have a good knowledge of the **ContentTools** code base. If it's a small change you want to make then monkey patching or extending and overwriting is the way to go.

| Event name | Description |
| --- | --- |
| revert | Triggered when the editor reverts the page to it's previous state. |
| save | Triggered when the editor saves the page. The event includes the **passive** key/value. |
| saved | Triggered after the editor has saved the page. The event includes the **passive** and **regions** key/value pairs. Regions is an object containing a map (name/content) of regions that have changed. |
| start | Triggered when the editor is started. |
| stop | Triggered when the editor is stopped. The event includes the **save** key/value. |
| tool-apply | Triggered when a tool is applied. The event includes the **tool** class, **element** and if applicable the content **selection**. |
| tool-applied | Triggered after a tool is applied. The event includes the **tool** class, **element** and if applicable the content **selection**. |

editor = ContentTools.EditorApp.get()

Returns the single instance of the **editor**.

cls = ContentTools.EditorApp.getCls()

Return the class used to generate an editor instance.

editor.init(  
    queryOrDOMElements,  
    namingProp='id',   
    fixtureTest=null,  
    withIgnition=true  
    )

Initialize the **editor**. The **queryOrDOMElements** parameter can either be a CSS query selecting that selects the editable regions on the page or a list of DOM elements, and the **namingProp** is used to determine which attribute against each of the region DOM elements will be used to uniquely identify each region. The **query** should be a string containing one or more CSS selectors, for example:

```
<!-- HMTL -->
<div data-editable data-name="article-body">...</div>

// JavaScript
var editor = ContentTools.EditorApp.get();
editor.init('[data-editable]', 'data-name');​​​​​​​​​​
```

Optionally a fixture test function can be provided which will receive a DOM element representing a region/fixture and should return true if it is a [Fixture](/api/content-edit#fixture), for example:

```
editor.init(
    '[data-editable], [data-fixture]', 
    'data-name',
    function (domElement) { 
        return domElement.hasAttribute('data-fixture');
    }
);​
```

If no fixture test is provided then the editor will provide a default test function identical to the one in the example given above.

The last argument, **withIgnition**, allows you to control if an ignition component will be created for the editor, this is useful when you want to use a different mechanism/UI to start/stop the editor.

editor.crtlDown()

Returns true if the Ctrl key (or Command key on Apple) is currently being held down.

editor.destroy()

Destroy/tear down the editor application.

editor.domRegions()

Return a list of all the DOM elements that are known to the editor as regions.

editor.getState()

Returns the current state of the editor. The possible editor states are:

|  |  |
| --- | --- |
| DORMANT | An instance of the `\_EditorApp` class exists but the `init` method has not yet been called (the primary distinction here is that the editor has not been mounted to the DOM). |
| READY | The editor has been mounted to the DOM and is ready (e.g the `start` method can be called to begin editing the document). |
| EDITING | The editor is in the editing state allowing changes to be made to the document. |
| Editor state | Description |
| --- | --- |

Editor states are held against the **ContentTools.EditorApp** class.

editor.history

The **editor** tracks changes to the page using the **[History](#history)** class. The **history** property holds an instance of the **History** class used to store the state of the current editing session.

editor.ignition()

Return the [ignition](#ignition-ui) UI component for the editor.

editor.inspector()

Return the [inspector](#inspector-ui) UI component for the editor.

editor.isDormant()

Return true if the editor is currently in the dormant state.

editor.isReady()

Return true if the editor is currently in the ready state.

editor.isEditing()

Return true if the editor is currently in the editing state.

editor.orderedRegions()

Return a list of regions in their navigation order. By default this is based on their position in the page, but it can be modified using the **setRegionOrder** method.

editor.regions()

Return a list of **[ContentEdit.Region](/api/content-edit#region)**s that the editor is managing.

editor.shiftDown()

Returns true if the Shift key is currently being held down.

editor.toolbox()

Return the [toolbox](#toolbox-ui) UI component for the editor.

editor.busy(busyState)

Get/set the busy state of the editor; if no **busyState** is provided then the current state is returned (as **true** or **false**). If a **busyState** is provided then the **editor** will either be set or taken out of the busy state.

editor.createPlaceholderElement(region)

Return a placeholder element for the region (used to populate an empty region).

If you want to customize the default placeholder element used to populate a region when it becomes empty then override this method. By default it will return an empty paragraph.

editor.highlightRegions(highlight)

**Highlight** (or stop **highlight**ing) editable regions within the page.

editor.paste(element, clipboardData)

Paste content from the **[clipboardData](https://developer.mozilla.org/en-US/docs/Web/API/ClipboardEvent/clipboardData)** into the given **element**. The **editor** monitors for paste events from the user and uses this method to handle them.

editor.revert()

Revert the page to its previous state (before we started editing it).

editor.revertToSnapshot(snapshot, restoreEditable=true)

Revert the page to a **snapshot**. See **[History](#history)**.

editor.save(passive)

Save the page in its current state. This triggers  **save** and **saved** events against the **editor**.

The **saved** event allows changes to the page to be saved somewhere, for example a database or file (*see [Saving changes](/getting-started#save-changes)*).

If the **passive** argument is given and **true** then the **saved** event will trigger, but the page will remain editable. This allows a save to be called by external code that doesn't want to change the state of the editor (e.g to support auto-saving).

editor.setRegionOrder(regionNames)

Similar to the tab index of fields in a form, this method allows the navigation order of regions to be set. The new order is defined by a list of **regionNames**.

editor.start()

Start editing the page. Calling this method makes the regions the **editor** was initialized with editable.

editor.stop(save)

Stop editing the page. The **save** argument if determines whether **stop** will call the editors **save** method (if true) or **revert** method (if false).

editor.syncRegions(regionQuery)

Sync the editor with the page. **SyncRegions** can be called in any editor state making it easy to add or remove editable regions while live editing. If a **regionQuery** is provided then the existing region query will be replaced.

**syncRegions** looks for new or removed editable regions since **syncRegions** was last called. (potentially indirectly from **init** and **start**). If you want to replace the content within the existing region then consider using the **[Region.setContent](/api/content-edit#region)** method.

### History

The **History** class provides a mechanism for storing, navigating and reverting the changes made to an editable document.

**Snaphots** are referenced throughout the following section. The term refers to an object which contains a map of region names and their HTML content as well as the selection state at the point the snapshot was taken.

```
// The structure of a snapshot
var snapshot = {
    regions: {
        'article-body': '...', // (a string of HTML)
        ...
        },
    selected: {
        element: element,      // a ContentEdit.Element instance
        selection: selection   // a ContentSelect.Range instance
        }
};
```

stack = new ContentTools.History(regions)

Create a new **History** stack monitoring the given **regions**. The **regions** should be specified as an object where region names map to their **[ContentEdit.Region](/api/content-edit#region)** instance.

stack.canRedo()

Returns **true** if there is one or more snapshots ahead of the current snapshot and therefore the **redo** method can be called.

stack.canUndo()

Returns **true** if there is one or more snapshots behind the current snapshot and therefore the **undo** method can be called.

stack.length()

Return the number of snaphots stored in the **stack**.

stack.snapshot()

Return the current snapshot.

stack.goTo(index)

Move the **stack**'s head to the given **index** and return the snapshot at that position.

stack.redo()

Move the **stack**'s head forward one position and return the snapshot at that position.

stack.replaceRegions(regions)

Replace the regions the **stack** is monitoring with a new set. The **regions** should be specified as an object where region names map to their **[ContentEdit.Region](/api/content-edit#region)** instance.

stack.restoreSelection(snapshot)

Restore the content selection and caret position for the given **snapshot**.

stack.stopWatching()

Stop watching the page for changes.

stack.undo()

Move the **stack**'s head backwards one position and return the snapshot at that position.

stack.watch()

Watch the document for changes. The watch process monitors the root *(see **[ContentEdit.Root](/api/content-edit#root)**)* for changes by comparing its modified date with the date a snapshot was last taken; if the two are not the same then it triggers the creation of snapshot.

To ensure we don't take snapshots whilst the user is still actively making changes we wait for a short period of inactivity before taking the snapshot.

### StylePalette

The **StylesPalette** class stores a list of styles available to users via the editor. A list of styles is usually defined and added to the palette as part of initializing the application *(see [Configure styles](/getting-started#configure-styles))*.

**StylePalette** is a static class and should not be initialized, all its methods are class methods.

ContentTools.StylePalette.add(styles)

Add a list of **Style**s to the **palette**.

ContentTools.StylePalette.styles(tagName)

Return a list of styles in the palette. If a **tagName** is specified then only styles applicable to that tag will be returned.

### Style

The **Style** class is used to define styles (CSS classes) for use in the editor. **Styles** must be registered with **StylePalette** before they can be accessed in the editor.

style = new ContentTools.Style(name, cssClass, applicableTo)

Create a new **Style.** The **name** is displayed to users in the editor, the **cssClass** is added to the **class** attribute of an element the style is applied to, and the **applicableTo** can be used to limit the **style** to a list of applicable tag names. If **applicableTo** is not given, the **style** will be applicable to all tags.

style.applicableTo()

Return the tag names this style is applicable to, no value (**null**) means the style is applicable to all tags.

style.cssClass()

Return the CSS class name for the style.

style.name()

Return the name of the style.

### Tools

**ContentTools** provides a set of tools for common editing tasks. Whilst these tools provide a good base for creating a content editor, it is possible to create new tools as required (*see the [Adding new tools](/tutorials/adding-new-tools) tutorial*).

The following tools are available in the standard code base.

| Tool name | Tool description |
| --- | --- |
| bold | Make the current selection of text bold (e.g `<b>foo</b>`). Applying the tool to bold text will remove the format. |
| italic | Make the current selection of text italic (e.g `<i>foo</i>`). Applying the tool to italic text will remove the format. |
| link | Insert a link. |
| heading | Convert the current text block to a heading (e.g `<h1>foo</h1>`). |
| subheading | Convert the current text block to a subheading (e.g `<h2>foo</h2>`). |
| paragraph | Convert the current text block to a paragraph (e.g `<p>foo</p>`). |
| preformatted | Convert the current text block to a preformatted block (e.g `<pre>foo</pre>`). |
| align-left | Apply a class to left-align the contents of the current text block. The class applied is **text-left**. |
| align-center | Apply a class to center-align the contents of the current text block. The class applied is **text-center**. |
| align-right | Apply a class to right-align the contents of the current text block. The class applied is **text-right**. |
| unordered-list | Set an element as an unordered list. |
| ordered-lists | Set an element as an ordered list. |
| table | Insert/update a Table. |
| indent | Indent a list item. |
| unindent | Un-indent a list item. |
| line-break | Insert a line break into the current element at the specified selection. |
| image | Insert an image. |
| video | Insert a video. |
| undo | Undo the last change. |
| redo | Redo the last undo. |
| remove | Remove the current element. |

### ToolShelf

The **ToolShelf** class allows tools to be stored and retrieved using a name. Tool names are used to define the tools that will populate the editor **ToolboxUI** widget *(see **DEFAULT\_TOOLS** in [settings](#settings))*.

**ToolShelf** is a static class and should not be initialized, all its methods are class methods.

ContentTools.ToolShelf.stow(cls, name)

Add a tool class to the shelf so we can retrieve it later by **name**.

ContentTools.ToolShelf.fetch(name)

Return a tool from the shelf associated with the given **name**.

### Tool

The **Tool** class defines a common API for editor tools, for this reason any tool class you write should inherit from the **Tool** class (*see the [Adding new tools](/tutorials/adding-new-tools) tutorial*).

Classed derived from the **Tool** class are static classes; every property and method is held against the class and the class should not be initialized.

ContentTools.Tool.label

The tools **label**, this will be displayed as a tool tip when the user hovers over the tools icon in the tool box.

ContentTools.Tool.icon

The tools **icon** class, this will be added as a modifier of the **ct-tool** CSS class, for example if the **icon** was defined as *bold* the modifier CSS class would be **ct-tool--bold**.

ContentTools.Tool.canApply(element, selection)

Return **true** if the tool can be applied to the given **element** and **selection**.

ContentTools.Tool.isApplied(element, selection)

Return **true** if the tool is currently applied to the the given **element** and **selection**.

ContentTools.Tool.apply(element, selection, callback)

Apply the tool to the given **element** and **selection**. Optionally a **callback** function can be provided which will be called once the tool has been applied.

### Event

The **Event** class provides information about events dispatched by [ComponentUI](#component-ui) instances.

The event model changed in release 1.2 and is no longer compatible with the [ContentEdit](/api/content-edit) event model. The change was necessary to allow UI events in ContentTools to modify the default behaviour and halt other registered callbacks.

event = ContentTools.Event(eventName, detail)

Create a new Event with the given name and detail. The **eventName** is used so that event listeners can be added which will trigger bound callbacks when an event of the same name is dispatched. The **detail** for an event can be any value but will always be either an **object** or **undefined** if dispatched by the core library (and we recommend that you follow this approach).

event.defaultPrevented()

Return **true** of the event has been cancelled.

event.detail()

Return the detail of the event.

event.name()

Return the name of the event.

event.propagationStopped()

Return **true** if the event has been halted.

event.timeStamp()

Return a time stamp of when the event was created.

event.preventDefault()

Cancel the event preventing the default event action.

event.stopImmediatePropagation()

Halt the event preventing any bound listener functions that have not yet been called for the event being called.

### ComponentUI

ContentTools provides a small set of user interface classes to support the included editor. The UI is not designed to be a complete UI library and is deliberately designed to be concise. If you're writing your own editor you may well choose to use a more complete UI library, however if you're just looking to extend the functionality of the existing editor the UI library is quite capable.

All UI component classes inherit from the **ComponentUI** class which provides base functionality and a common API.

component = ContentTools.ComponentUI()

Create a new **ComponentUI**.

component.children()

Return a list of children for the **component** (this list is a copy but the child components are not).

component.domElement()

Return the mounted DOM element for the **component**.

component.parent()

Return the parent component for the **component**.

component.isMounted()

Return **true** if the **component** is mounted to the DOM.

component.attach(child, index)

Attach a component as a **child** of this **component**.

component.addCSSClass(className)

Add a CSS class to the **component**'s DOM element. The CSS class is not retained if the **component** is remounted.

component.detach(component)

Detach a child from this **component**.

component.mount()

Mount the component to the DOM.

component.removeCSSClass(className)

Remove a CSS class to the **component**'s DOM element.

component.unmount()

Unmount the **component** from the DOM.

component.addEventListener(eventName, callback)

Add an event listener for the named event against **component**.

component.createEvent(eventName, detail)

Create an [event](#event). This provides a useful short-cut allowing you to call `@createEvent(...)` instead of `new ContentTools.Event(...)`.

component.dispatchEvent(ev)

Dispatch an event against the **compontent**.

component.removeEventListener(eventName, callback)

Remove a previously registered event listener for the **component**. If;

* no **eventName** is given all listeners are unbound from the **component**,
* an **eventName** is given but no **callback** is, then all listeners for the named event are unbound,
* an **eventName** and **callback** are given then the listener for the given **calback** is unbound for the named event.

component.\_addDOMEventListeners()

Added DOM event bindings for the **component**.

component.\_removeDOMEventListeners()

Remove DOM event bindings for the **component**.

I typically don't document private methods (indicated by the prefixed \_ character) but these two methods (**\_addDOMEventListeners**/**\_removeDOMEventListeners**) are worth documenting as when you're writing your own components you should override these and add any DOM event binding/unbinding code to them.

ContentTools.ComponentUI.createDiv(classNames, attributes, content)

All UI components are constructed entirely from one or more nested **<div>**s. This **createDiv** class method provides a short-cut for creating a **<div>** including the initial CSS class names, **attributes** and **content**. A DOM element is returned.

### WidgetUI (inherits from [ComponentUI](#component-ui))

The **WidgetUI** class is the base class for components that are mounted at the root of the application such as the toolbox, tag inspector, ignition and dialogs (e.g within the `<div class="ct-app">..</div>` element added by the editor).

widget = new ContentTools.WidgetUI()

Create a new **WidgetUI**.

widget.show()

Show the **widget**. By default widgets are not visible when they are mounted to the DOM.

widget.hide()

Hide the **widget**.

### AnchoredComponentUI

Anchored components are mounted against DOM elements at a specified point. Remounting an anchored component requires that the parent perform the re-mount.

The benefit of anchored components is they are lightweight and can be rendered into a specific DOM element by the parent, for example tools within the toolbox are anchored components.

component = new ContentTools.AnchoredComponentUI()

Create a new **AnchoredComponentUI**.

component.mount(domParent, before)

Mount the **component** in the DOM within the **domParent**, if a DOM element is given as **before** then the **component** will be mounted before that element, provided it is a child of **domParent**. If before is not given then the **component** will be mounted as the last child of the **domParent**.

### FlashUI (inherits from [AnchoredComponentUI](#anchored-component-ui))

A flash is a visual indicator displayed typically once a task has been completed, for example it might show that a save has been successful or that it failed.

Instances of the **FlashUI** class are short lived, they display as soon as mounted and are unmounted as soon as their animation has finished. As such, references to flash instances should not be stored, for example:

```
// Let the user know everything went OK
new ContentTools.FlashUI('ok');
```

flash = new ContentTools.FlashUI(modifier)

Create a new FlashUI with the given modifier (*see the **[mount](#flash-ui-mount)** method*).

flash.mount(modifier)

Mount the **flash** on the DOM, the **modifier** will be applied as a CSS modifier of the **ct-flash** class for example if the **modifier** is *ok* then the modifier class would be **ct-flash--ok**.

The modifiers currently included in the code base are:

* **ok** which displays a tick.
* **no** which displays a cross.

There is no need to call mount directly as it is called when the FlashUI instance is initialized.

### IgnitionUI (inherits from [WidgetUI](#widget-ui))

To control editing of content (e.g. start/stop/busy) an **IgnitionUI** class is provided. The ignition switch is typically created and used by the **[EditorApp](#editor-app)** class to control its state and would not usually be accessed outside of the **EditorApp** class.

| Event name | Description |
| --- | --- |
| busy | Triggered when the iginition is set to or reverted from the busy state. The event includes the **busy** key/value. |
| cancel | Triggered when the ignition's cancel action is selected. |
| confirm | Triggered when the ignition's confirm action is selected. |
| edit | Triggered when the ignition's edit action is selected. |
| statechange | Triggered when the ignition's state is changed. The event includes the **state** key/value. |

ignition = new ContentTools.IgnitionUI()

Create a new **IgnitionUI**.

ignition.busy(busy)

Set the **ignition** to busy (or revert if from a busy state to its previous state.

ignition.cancel()

Dispatch the cancel event against the **ignition** and set its state to ready.

ignition.confirm()

Dispatch the confirm event against the **ignition** set its state to ready.

ignition.edit()

Dispatch the edit event against the **ignition** and set its state to editing.

ignition.state(state)

Get/Set the state of the **ignition**. State must be one of the following values:

* busy
* editing
* ready

### InspectorUI (inherits from [WidgetUI](#widget-ui))

The **InspectorUI** class provides a breadcrumb style navigation tool for the selected editable element within the document and its chain of parent elements.

inspector = new ContentTools.InspectorUI()

Create a new **InspectorUI**.

inspector.updateTags()

Update the tags displayed in the **inspector**'s tag trail based on the editable element that currently has focus.

### TagUI (inherits from [AnchoredComponentUI](#anchored-component-ui))

The **TagUI** class is used to populate the **InspectorUI**'s tag trail. Each tag represents an editable element. Selecting a tag from the inspector bar allows the user to modify its properties.

tag = new ContentTools.TagUI(element)

Create a **TagUI** for the given **element** which must be a **[ContentEdit.Element](/api/content-edit#element)** instance.

### ModalUI (inherits from [WidgetUI](#widget-ui))

The ModalUI class provides a blocking layer which prevents the user from interacting with the page whilst allowing them to interact with UI components above the layer such as a dialog.

modal = new ContentTools.ModalUI(transparent, allowScrolling)

Create a new **ModalUI**. The **transparent** flag determines if the **modal**'s layer should in some way hide the page content (e.g to reduce distraction) or if the layer shouldn't be invisible to the user. The **allowScrolling** flag determines if the page can be scrolled while the **modal** is open - when a dialog is opened you typically don't want the page to scroll as that behaviour may interfere with the scrolling of content within the dialog.

The **transparent** flag determines if the **modal**'s layer should in some way hide the page content (e.g to reduce distraction) or if the layer shouldn't be invisible to the user.

The **allowScrolling** flag determines if the page can be scrolled while the **modal** is open. When a dialog is opened you typically don't want the page to scroll as that behaviour may interfere with the scrolling of content within the dialog.

| Event name | Description |
| --- | --- |
| click | Triggered when the user clicks on the modal. |

### ToolboxUI (inherits from [WidgetUI](#widget-ui))

The ToolboxUI class provides a floating window of content-editing tools. The toolbox is draggable so that the user can position it as required whilst editing. The position is stored in local storage so it persists between editing sessions.

toolbox = ContentTools.ToolboxUI(tools)

Create a new **ToolboxUI** containing the given **tools**. The **tools** should be provided as an array of tool groups where each tool group is an array of tool names (*see the DEFAULT\_TOOLS in [settings](#settings).*).

toolbox.isDragging()

Return true if the **toolbox** is currently being dragged.

toolbox.tools(tools)

Get/set the **tools** that populate the **toolbox**. If a new set of **tools** is given then the the tools populating the **toolbox** will be updated, otherwise those that currently populate it will be returned.

toolbox.updateTools()

Refresh all tools in the **toolbox**, this must be called whenever the currently selected element is changed so that the tools can be updated (e.g applied, can be applied states) to reflect those changes.

### ToolUI (inherits from [AnchoredComponentUI](#anchored-dialog-ui))

A tool that can be selected in the toolbox.

| Event name | Description |
| --- | --- |
| apply | Triggered when the tool is selected. The event includes **element** and **selection** key/values. |
| applied | Triggered after a tool has been applied. The event includes **element** and **selection** key/values. |

tool = new ContentTools.ToolUI(tool)

Create a new **ToolUI** that when selected will apply the specified **tool** ([Tool](#tool)).

tool.apply(element, selection)

Apply the tool ([Tool](#tool)) associated with the **tool** (ToolUI) to the given **element** and optionally **selection**.

tool.disabled(disabledState)

Get/Set the disabled state of the **tool**. If **disabledState** is given then the tool's state will be set otherwise the tool's current state will be returned.

tool.update(element, selection)

Update the tool's active state and applied appearance based on a given **element** and optionally **selection**.

### AnchoredDialogUI (inherits from [WidgetUI](#widget-ui))

The **AnchoredDialogUI** class is the base class for creating anchored dialogs. An anchored dialog appears above the page but is anchored to a set position within it, they are useful for in-page edits such as setting a link within the page.

dialog = new ContentTools.AnchoredDialogUI()

Create a new **AnchoredDialogUI**.

dialog.position(newPosition)

Get/set the position of the dialog. If a **newPosition** is given then the dialog will be anchored there, if not then the **dialog**'s current position will be returned.

The **newPosition** must be a 2 item array in the form **[x, y]** (in pixels).

### DialogUI (inherits from [WidgetUI](#widget-ui))

The **DialogUI** class is the base class for creating dialogs.

| Event name | Description |
| --- | --- |
| cancel | Triggered when the dialog is cancelled (closed without saving). |
| save | Triggered when the dialog is saved. Typical the save event will provide one or more key/value pairs containing details of the dialog's content when the user saved. |

dialog = new ContentTools.DialogUI(caption='')

Create a new **DialogUI** with the given **caption**.

dialog.busy(busyState)

Get/set the busy state of the **dialog**, if no **busyState** is provided then the current state is returned (as **true** or **false**). If a **busyState** is provided then the **dialog** will either be set or taken out of the busy state.

dialog.caption(newCaption)

Get/set the **dialog**'s caption. If no **newCaption** is provided then the current caption is returned. If a **newCaption** is provided then the **dialog**'s caption will be updated.

### ImageDialog

The **ImageDialog** class provides a dialog for uploading, rotating and cropping images.

The dialog doesn't handle the uploading of images. A function should be set against the **IMAGE\_UPLOADER** setting like so:

```
ContentTools.IMAGE_UPLOADER = myImageUploader;

```

This function receives the dialog when the dialog is initialized, at which point it can set up all the required event bindings to support image uploads (*see the [Handling image uploads](/tutorials/handling-image-uploads) tutorial*).

| Event name | Description |
| --- | --- |
| .cancelupload | Triggered when a user cancels the upload of an image file. |
| .clear | Triggered when a user clears the image from the dialog. |
| .fileready | Triggered when a user selects an image to upload. The event provides the **file** key/value. |
| .mount | Triggered when the image dialog is mounted. |
| .rotatecw | Triggered when the user rotates the image clockwise. |
| .rotateccw | Triggered when the user rotates the image counter-clockwise. |
| .save | Triggered when the user selects to save the image. |
| .unmount | Triggered when the image dialog is unmounted. |

The prefixed full-stop **.** against each event above means the event is namespaced under **imageuploader**, for example **.cancelupload** would be **imageuploader.cancelupload**.

dialog = new ContentTools.ImageDialog()

Create a new **ImageDialog**.

dialog.cropRegion()

Return the defined crop-region (*top, left, bottom, right*). The values are normalized to the range **0.0 - 1.0**. If no crop region is defined then the maximum region will be returned (e.g **[0, 0, 1, 1]**).

dialog.addCropMarks()

Add crop marks to the current image so the user can define a crop region.

dialog.clear()

Clear the image that currently populates the **dialog**.

dialog.populate(imageURL, imageSize)

Populate the **dialog** with an image. The **imageURL** should point to the image to display in the **dialog.** There's little point in this being larger than the **dialog**'s viewport (570x320 pixels) - the **imageSize** should be the actual image size as a 2 item of the form **[width, height]** in pixels.

The **populate** method is typically called when a new image is uploaded or after the current image has been rotated.

dialog.progress(uploadProgress)

When an image is being uploaded the dialog displays a progress bar. The **progress** method will get/set the **uploadProgress** percentage for the **dialog**. If **uploadProgress** is given (as a percentage, e.g 0-100) then the progress bar will be updated to reflect the new value, if not then the current progress value will be returned.

dialog.removeCropMarks()

Remove crop marks from the current image.

dialog.save(imageURL, imageSize, imageAttrs)

Save and insert the current image. This method triggers the **save** event against the **dialog.** The event is triggered with the following arguments:

* **imageURL** The URL of the image to insert.
* **imageSize** The size of the image (the size at which it will be inserted into the page) given as a 2 item of the form [width, height] in pixels.
* **imageAttrs** The attributes for the image given as an object. Common attributes to include are **alt** and **data-ce-max-width** (*see [ContentEdit.ResizeableElement](/api/content-edit#resizable-element)*).

dialog.state(newState)

Set/get the state of the **dialog**. The dialog can be set to any of the following states - **empty**, **uploading**, **populated**. If a **newState** is given then the dialog's state will be set, otherwise its current state will be returned.

### LinkDialog (inherits from [AnchoredDialogUI](#anchored-dialog-ui))

The **LinkDialog** class provides a dialog that floats above a selection of text or image and allows a link to be entered. The dialog is associated with the **[link](#tools)** tool.

dialog = new ContentTools.LinkDialog(initialValue='')

Create a **LinkDialog**. The **initialValue** is used to pre-populate the **dialog's** input field, for example with the current URL for the link.

dialog.save()

Save the link. This method triggers the save event against the **dialog.** The event is triggered with the value of the **dialog's** input field.

### PropertiesDialog (inherits from [DialogUI](#dialog-ui))

The **PropertiesDialog** class provides a dialog that allows an element's styles, attributes and inner HTML to be viewed and updated. The properties dialog is opened by selecting a tag in tag inspector.

dialog = new ContentTools.PropertiesDialog(element)

Create a new **PropertiesDialog** populated by the given **element**.

dialog.changedAttributes()

Return an object of attributes set in the **dialog** that have been changed by the user (e.g were added, modified or removed). Attributes that have been removed are assigned a **null** value, for example:

```
{
    'alt': 'My dragon Burt', // + This attribute was added or updated
    'id': null               // - This attribute was removed
}
```

dialog.changedStyles()

Return an object of styles that have been changed by the user (e.g applied or removed). The styles CSS class is mapped to **true** if the style has been applied and **false** if it's been removed, for example:

```
{
    'note': true,       // + This style was applied
    'definition': false // - This style was removed
}
```

dialog.getElementInnerHTML()

Return the inner HTML for the element, taking into account that the element might be a **[ListItem](/api/content-edit#list-item)** or **[TableCell](/api/content-edit#table-cell)** and in which case the content is stored in a child **[ListItemText](/api/content-edit#list-item-text)** or **[TableCellText](/api/content-edit#table-cell-text)** element respectively.

dialog.save()

Save any changes to the properties. This method triggers the **save** event against the **dialog**, the event is triggered with the following arguments:

* **attributes** the attributes that have been changed and their values. Attributes with **null** values have been removed (see the **changedAttributes** method).
* **styles** the styles that have changed (see the **changedStyles** method).
* **innerHTML** The inner HTML for the element. If the element doesn't support content the value will be **null**.

### TableDialog (inherits from [DialogUI](#dialog-ui))

The **TableDialog** class provides a dialog that allows a table to be inserted or modified. The dialog is associated with the **[table](#table)** tool.

dialog = new ContentTools.TableDialog(table)

Create a new **TableDialog**, if a **table** element is provided, the dialog allows the user to update the table, if not the dialog allows the user to insert a new table.

dialog.save()

Save the table. This method triggers the **save** event against the **dialog.** The event is triggered with the following arguments:

* **body** the number of columns in the body of the table.
* **foot** whether the table has a footer **<tfoot>**.
* **head** whether the table has a head **<thead>**.

### VideoDialog (inherits from [DialogUI](#dialog-ui))

The **VideoDialog** class provides a **dialog** that allows a *YouTube* or *Vimeo* video to be inserted, alternatively a user can enter any URL and an **<iframe>** will be inserted with the specified URL as its source. The **dialog** is associated with the **[video](#tools)** tool.

dialog = new ContentTools.VideoDialog()

Create a new **VideoDialog**.

dialog.clearPreview()

Clear the preview video from the **dialog**.

dialog.preview(url)

Show a preview video in the **dialog** for the given **url**.

dialog.save()

Save the video. This method triggers the **save** event against the **dialog.** The event is triggered with the URL for the video.

The URL may differ from that entered by the user if it is a *YouTube* or *Vimeo* URL, in which case it may be altered to match the required format to embed such videos *(see the the **[getEmbedVideoURL](#functions)** function)*.








