





How to build custom sign-up forms in Ghost









































---


For publications with a strong brand identity or those looking to fully optimize their Ghost site, a custom sign-up form is more than just a tool — it's an extension of the brand itself.

Using *Of Record*, a publication focusing on vinyl collecting and music listening, as our example, we'll delve into:

* The reasons for going bespoke
* The anatomy of a custom sign-up form
* A peek into what makes an engaging sign-up form

Here's a preview of the sign-up form we'll build in this tutorial:


0:00
/0:13









Ready to elevate your sign-up form into a memorable experience? Let's dive in!

It may be simpler than you think
--------------------------------

For most publications, Ghost already offers a simple solution that works out of the box and without any custom code.

[Embeddable signup formsStart growing your audience from anywhere on the web, using the new embeddable signup forms. It’s now even easier attract new subscribers from any website, while keeping Ghost as the hub for your memberships. Branded Include your logo, publication name, and description in your signup form, and…![](https://ghost.org/changelog/content/images/size/w256h256/2023/06/ghost-orb-orange-squircle-04.png)ChangelogTeam Ghost![](https://ghost.org/changelog/content/images/2023/06/Signup-form-2.png)](https://ghost.org/changelog/embeddable-signup-forms/?ref=ghost.org)

Head to **Settings** → **Membership**, select a layout, and color, apply your labels, then simply copy the embed code for use anywhere on the web. Here's a live example:

  
  
However, for advanced users, Ghost provides tools for creating a completely custom sign-up form that allows you to:

* Fully align the form with your brand's visual identity.
* Provide a unique user experience.
* Optimize performance.

Let's see these tools at work by analyzing *Of Record's* sign-up form, shown below.

![Custom sign-up form from Of Record's webpage](https://ghost.org/tutorials/content/images/2023/08/sign-up-form-2.png)

Anatomy of a custom sign-up form
--------------------------------

The beauty of building a custom sign-up form is that it's exactly the same as building one with standard HTML elements. Integrating it with Ghost is as simple as adding a few custom data attributes. Here's the code for *Of Record's* sign-up form:

```
<form data-members-form= >
    <input data-members-label type="hidden" value="Turntable buying guide" />
    <label>
        Name
        <input data-members-name />
    </label>
    <label>
        Email
        <input data-members-email type="email" required />
    </label>
    <button>
        Sign up
    </button>
    <p class="loading">⏲️ Please hold while we check our collection.</p>
    <p class="error">❗Something's gone wrong. Please try again.</p>
    <p class="success">🎸 Success! Check your inbox for our email.</p>
</form>
```

Putting this form anywhere in your theme or on your site via an HTML card will instantly create a custom sign-up form ✨

Let's talk about the necessary attributes that make it work.

### Activate the form

To make Ghost aware of your custom form, add the `data-members-form` attribute to the form. Note that you can change the language of the email that a new member will receive by adding a value to the attribute:

* `data-members-form="signup"`: new members receive an email with "sign up" language
* `data-members-form="subscribe"` (default): new members receive an email with "subscribe" language

Functionally, both of these options are identical. Opting for one or the other will depend entirely on your publication's identity. [See additional options for the `data-members-form` attribute in the docs](https://ghost.org/docs/themes/members/?ref=ghost.org#extending-forms).

💡Use the match helper with the @member object to only show the sign-up form to nonmembers. [Learn more.](https://ghost.org/tutorials/index/#dynamic-cta)
### Get a name

```
<label>
    Name
    <input data-members-name />
</label>
```

In *Of Record's* form, we wrap the input with a `label` element. This approach is optional, but it's a convenient method to associate the label and input, which makes the form more accessible.

The `data-members-name` attribute tells Ghost to collect the member's name. However, because `required` is omitted from the input, this field is optional. A member will be able to sign up without giving their name. To require a name, use the `required` attribute as seen in the next section.

### Get an email

```
<label>
    Email
    <input data-members-email type="email" required />
</label>
```

On this input, we include the `type="email"` and `required` attributes. These help with validation (the browser checks if the email is valid) and `required` ensures a value is present before submitting.

The magic comes in with the addition of the `data-members-email` attribute, which Ghost uses to capture the submitted email.

### Add a label

In addition to capturing a name and email, it's also possible to add a label to members who sign up with your custom form. [These labels appear on the member's profile in Ghost Admin and are filterable via the **Members** menu](https://ghost.org/help/member-management/?ref=ghost.org#labels). Also, when sending an email, you can use these labels as recipient groups. This works great if your sign-up form is coupled with particular content, and you want to send an update related to that content. With labels, you already have a list of everyone interested in that content!

Here's what the member profile looks like in Ghost Admin. Note the "Turntable buying guide" label.

![](https://ghost.org/tutorials/content/images/2023/08/member.png)

And, here's the code to add to set a label.

```
<input data-members-label type="hidden" value="Turntable buying guide" />
```

It works by adding a `hidden` input type (meaning it won't appear to the user) along with the `data-members-label` attribute. Then, set the `value` to the label you want to add. That's it!

Now, whenever someone signs up with your custom form, this label will be applied automatically.

💡Bright Themes has an advanced tutorial on letting users choose which labels are associated with their signup. [Check out how it's done](https://brightthemes.com/blog/ghost-member-labels?ref=ghost.org).

Form states and CSS styling
---------------------------

```
<p class="loading">⏲️ Please hold while we check our collection.</p>
<p class="error">❗Something's gone wrong. Please try again.</p>
<p class="success">🎸 Success! Check your inbox for our email.</p>
```

Not only does adding Ghost's custom data attributes ensure your form gets your members signed up, but it also adds relevant classes as the user signs up. These classes, added to the `form` element, reflect its state: `loading`, `success`, and `error`.

![Loading state with text: Please hold while we check our collection](https://ghost.org/tutorials/content/images/2023/08/loading.png)
![Success state and message](https://ghost.org/tutorials/content/images/2023/08/success.png)
![Error state and message](https://ghost.org/tutorials/content/images/2023/08/error.png)

These classes enable you to convey the form's state to your user. How you want to do this is completely up to you, but we'll show you the basic logic to implement in CSS.

```

/* Form states */
:where(.loading, .success, .error)  {
    display: none;
}

.loading .loading, .success .success, .error .error {
    display: block;
}

```

We set the default style of the states (like `<p class="success">`) to `display: none`. Then, we override these states when Ghost adds the class to the `form` element. For example, here's what the form HTML looks like when the sign up is loading:

```
<form data-members-form class="loading">
  ...
</form>
```

The `loading` class on the form and the same class on the `p` element makes the selector `.loading .loading` match and updates the `display` property to show the state.

Because it's just CSS controlling whether elements are shown, you can simulate the different states by adding and removing the different classes from the form, rather than having to actually sign up over and over again.

Keeping the user apprised of where they are in the sign-up process is possible with just a few lines of CSS and opens up lots of creative possibilities when creating a custom form.

Designing content for your form
-------------------------------

Now that you know *how* to make a custom sign-up form, you may be faced with the tricky task of *what* actually to put in it 🤔

With a custom sign-up form, you can take any approach you want:

* Minimalist: Simple, clean typography focuses on essential values
* Visual storytelling: Imagery tells a story and connects with the audience
* All about the benefits: Bullet points or icons convey the value position instantly
* Interactive experience: Animations, transitions, and interactive elements engage the user and make signing up a blast

These are but a few of the approaches you can take, which makes things difficult. How can you create an effective sign-up form? Don't worry! We've got you covered over on [Ghost Resources](https://ghost.org/resources/?ref=ghost.org).

We share evidence-based best practices to support creators, businesses, and publishers. For example, check out this [formula for creating powerful copy](https://ghost.org/resources/refine-marketing-copy/?ref=ghost.org#a-simple-formula-for-powerful-copy) or these [strategies for building a sign-up form that converts](https://ghost.org/resources/conversion-strategy/?ref=ghost.org).

Summary
-------

Whether you're a publication with a strong brand identity like *Of Record* or someone looking to fully optimize your Ghost site, a custom sign-up form is a powerful tool to build your audience.

With knowledge of Ghost's custom data attributes and the styles to show and hide form states, you now have everything you need to create gorgeous, custom sign-up forms.

If you create one, don't hesitate to share it with the Ghost community. We like to hang out on the [official Forum](https://forum.ghost.org/?ref=ghost.org). It's also a great place to get ideas and learn more about building with Ghost.

Oh, and don't forget to sign up 💌

![email letter on fire](https://ghost.org/tutorials/content/images/size/w1000/2023/04/flames-of-knowledge.jpg)
**On this page**
[Introduction](#intro)




---




How was the tutorial?
---------------------


Keep on learning
----------------

[### Custom settings are the ultimate power-up for themes

6 min read](/tutorials/custom-settings/)

[### The art of the post template

12 min read](/tutorials/post-template/)

[### A complete guide to partials

10 min read](/tutorials/partials/)

[### A comprehensive guide to the index template

9 min read](/tutorials/index/)

[### A comprehensive guide to the default template

9 min read](/tutorials/default/)

[### Essential concepts to know when building a Ghost theme

7 min read](/tutorials/essential-concepts/)

[### How to install Ghost locally

3 min read](/tutorials/local-ghost/)

[### Install Node on macOS, Windows, and Linux

4 min read](/tutorials/node/)

[### How to create a read-next section

10 min read](/tutorials/read-next/)

[### How to build a custom homepage

11 min read](/tutorials/custom-homepage/)

[### Create a custom post template

4 min read](/tutorials/create-a-custom-post-template/)

[### Implementing redirects

5 min read](/tutorials/implementing-redirects/)

[### Show reading time & progress

3 min read](/tutorials/reading-time/)

[### How to build CSS files

2 min read](/tutorials/build-css-files/)

[### How to make a podcast RSS feed

4 min read](/tutorials/custom-rss-feed/)







Be the first to know.
---------------------

Join the Ghost developer community — sign up to get early access to the latest features, developer tools, and tutorials.



No spam. Once a month. Unsubscribe any time.
[![](https://ghost.org/tutorials/assets/img/most-helpful.jpg?v=235936095d)

Most helpful
------------

Essential tutorials to get you started](https://ghost.org/tutorials/most-helpful/)
[![](https://ghost.org/tutorials/assets/img/fundamentals.jpg?v=235936095d)

Funda­mentals
-------------

The basics of Ghost theme development](https://ghost.org/tutorials/fundamentals/)
[![](https://ghost.org/tutorials/assets/img/level-up.jpg?v=235936095d)

Level up
--------

Next-level development techniques](https://ghost.org/tutorials/level-up/)
[![](https://ghost.org/tutorials/assets/img/do-more.jpg?v=235936095d)

Do more
-------

Ideas & inspiration for whatever comes next](https://ghost.org/tutorials/do-more/)









