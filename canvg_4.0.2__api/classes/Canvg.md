



Class: Canvg | canvg



[Skip to main content](#)

SVG renderer on canvas.

Constructors[​](#constructors "Direct link to heading")
-------------------------------------------------------

### constructor[​](#constructor "Direct link to heading")

• **new Canvg**(`ctx`, `svg`, `options?`)

Main constructor.

#### Parameters[​](#parameters "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `ctx` | [`RenderingContext2D`](/api/#renderingcontext2d) | Rendering context. |
| `svg` | `Document` | SVG Document. |
| `options` | [`IOptions`](/api/interfaces/IOptions) | Rendering options. |

#### Defined in[​](#defined-in "Direct link to heading")

[src/Canvg.ts:82](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L82)

Properties[​](#properties "Direct link to heading")
---------------------------------------------------

### parser[​](#parser "Direct link to heading")

• `Readonly` **parser**: [`Parser`](/api/classes/Parser)

XML/HTML parser instance.

#### Defined in[​](#defined-in-1 "Direct link to heading")

[src/Canvg.ts:64](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L64)

---

### screen[​](#screen "Direct link to heading")

• `Readonly` **screen**: [`Screen`](/api/classes/Screen)

Screen instance.

#### Defined in[​](#defined-in-2 "Direct link to heading")

[src/Canvg.ts:68](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L68)

---

### document[​](#document "Direct link to heading")

• `Readonly` **document**: [`Document`](/api/classes/Document)

Canvg Document.

#### Defined in[​](#defined-in-3 "Direct link to heading")

[src/Canvg.ts:72](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L72)

---

### documentElement[​](#documentelement "Direct link to heading")

• `Private` `Readonly` **documentElement**: [`SVGElement`](/api/classes/SVGElement)

#### Defined in[​](#defined-in-4 "Direct link to heading")

[src/Canvg.ts:73](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L73)

---

### options[​](#options "Direct link to heading")

• `Private` `Readonly` **options**: [`IOptions`](/api/interfaces/IOptions)

#### Defined in[​](#defined-in-5 "Direct link to heading")

[src/Canvg.ts:74](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L74)

Methods[​](#methods "Direct link to heading")
---------------------------------------------

### from[​](#from "Direct link to heading")

▸ `Static` **from**(`ctx`, `svg`, `options?`): `Promise`<[`Canvg`](/api/classes/Canvg)>

Create Canvg instance from SVG source string or URL.

#### Parameters[​](#parameters-1 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `ctx` | [`RenderingContext2D`](/api/#renderingcontext2d) | Rendering context. |
| `svg` | `string` | SVG source string or URL. |
| `options` | [`IOptions`](/api/interfaces/IOptions) | Rendering options. |

#### Returns[​](#returns "Direct link to heading")

`Promise`<[`Canvg`](/api/classes/Canvg)>

Canvg instance.

#### Defined in[​](#defined-in-6 "Direct link to heading")

[src/Canvg.ts:32](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L32)

---

### fromString[​](#fromstring "Direct link to heading")

▸ `Static` **fromString**(`ctx`, `svg`, `options?`): [`Canvg`](/api/classes/Canvg)

Create Canvg instance from SVG source string.

#### Parameters[​](#parameters-2 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `ctx` | [`RenderingContext2D`](/api/#renderingcontext2d) | Rendering context. |
| `svg` | `string` | SVG source string. |
| `options` | [`IOptions`](/api/interfaces/IOptions) | Rendering options. |

#### Returns[​](#returns-1 "Direct link to heading")

[`Canvg`](/api/classes/Canvg)

Canvg instance.

#### Defined in[​](#defined-in-7 "Direct link to heading")

[src/Canvg.ts:50](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L50)

---

### fork[​](#fork "Direct link to heading")

▸ **fork**(`ctx`, `svg`, `options?`): `Promise`<[`Canvg`](/api/classes/Canvg)>

Create new Canvg instance with inherited options.

#### Parameters[​](#parameters-3 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `ctx` | [`RenderingContext2D`](/api/#renderingcontext2d) | Rendering context. |
| `svg` | `string` | SVG source string or URL. |
| `options` | [`IOptions`](/api/interfaces/IOptions) | Rendering options. |

#### Returns[​](#returns-2 "Direct link to heading")

`Promise`<[`Canvg`](/api/classes/Canvg)>

Canvg instance.

#### Defined in[​](#defined-in-8 "Direct link to heading")

[src/Canvg.ts:105](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L105)

---

### forkString[​](#forkstring "Direct link to heading")

▸ **forkString**(`ctx`, `svg`, `options?`): [`Canvg`](/api/classes/Canvg)

Create new Canvg instance with inherited options.

#### Parameters[​](#parameters-4 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `ctx` | [`RenderingContext2D`](/api/#renderingcontext2d) | Rendering context. |
| `svg` | `string` | SVG source string. |
| `options` | [`IOptions`](/api/interfaces/IOptions) | Rendering options. |

#### Returns[​](#returns-3 "Direct link to heading")

[`Canvg`](/api/classes/Canvg)

Canvg instance.

#### Defined in[​](#defined-in-9 "Direct link to heading")

[src/Canvg.ts:123](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L123)

---

### ready[​](#ready "Direct link to heading")

▸ **ready**(): `Promise`<`void`>

Document is ready promise.

#### Returns[​](#returns-4 "Direct link to heading")

`Promise`<`void`>

Ready promise.

#### Defined in[​](#defined-in-10 "Direct link to heading")

[src/Canvg.ts:138](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L138)

---

### isReady[​](#isready "Direct link to heading")

▸ **isReady**(): `boolean`

Document is ready value.

#### Returns[​](#returns-5 "Direct link to heading")

`boolean`

Is ready or not.

#### Defined in[​](#defined-in-11 "Direct link to heading")

[src/Canvg.ts:146](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L146)

---

### render[​](#render "Direct link to heading")

▸ **render**(`options?`): `Promise`<`void`>

Render only first frame, ignoring animations and mouse.

#### Parameters[​](#parameters-5 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `options` | [`IScreenStartOptions`](/api/interfaces/IScreenStartOptions) | Rendering options. |

#### Returns[​](#returns-6 "Direct link to heading")

`Promise`<`void`>

#### Defined in[​](#defined-in-12 "Direct link to heading")

[src/Canvg.ts:154](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L154)

---

### start[​](#start "Direct link to heading")

▸ **start**(`options?`): `void`

Start rendering.

#### Parameters[​](#parameters-6 "Direct link to heading")

| Name | Type | Description |
| --- | --- | --- |
| `options` | [`IScreenStartOptions`](/api/interfaces/IScreenStartOptions) | Render options. |

#### Returns[​](#returns-7 "Direct link to heading")

`void`

#### Defined in[​](#defined-in-13 "Direct link to heading")

[src/Canvg.ts:171](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L171)

---

### stop[​](#stop "Direct link to heading")

▸ **stop**(): `void`

Stop rendering.

#### Returns[​](#returns-8 "Direct link to heading")

`void`

#### Defined in[​](#defined-in-14 "Direct link to heading")

[src/Canvg.ts:188](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L188)

---

### resize[​](#resize "Direct link to heading")

▸ **resize**(`width`, `height?`, `preserveAspectRatio?`): `void`

Resize SVG to fit in given size.

#### Parameters[​](#parameters-7 "Direct link to heading")

| Name | Type | Default value |
| --- | --- | --- |
| `width` | `number` | `undefined` |
| `height` | `number` | `width` |
| `preserveAspectRatio` | `string` | `boolean` | `false` |

#### Returns[​](#returns-9 "Direct link to heading")

`void`

#### Defined in[​](#defined-in-15 "Direct link to heading")

[src/Canvg.ts:198](https://github.com/canvg/canvg/blob/15fc145/src/Canvg.ts#L198)

* [Constructors](#constructors)
  + [constructor](#constructor)
* [Properties](#properties)
  + [parser](#parser)
  + [screen](#screen)
  + [document](#document)
  + [documentElement](#documentelement)
  + [options](#options)
* [Methods](#methods)
  + [from](#from)
  + [fromString](#fromstring)
  + [fork](#fork)
  + [forkString](#forkstring)
  + [ready](#ready)
  + [isReady](#isready)
  + [render](#render)
  + [start](#start)
  + [stop](#stop)
  + [resize](#resize)




