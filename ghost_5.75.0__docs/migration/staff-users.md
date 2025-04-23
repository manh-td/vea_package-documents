Importing staff users to Ghost
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

Your import file must include both any users that you want to import and any users that you need to reference in the import file in relation to other resources.

Users with an email address that matches the email address of a existing user will not be duplicated or updated. Users with an unmatched email address will be imported, but their account will be locked so that they must reset their password to login.

#### Linking objects to users

To link your resources to a user, you would specify a user id relative to the user’s id in the import file. So, if you have a user with `id: 2` in your file, and a post with `published_by: 2` that post will be set to be published by that user.

All users with unmatched email addresses are imported first. Once this is complete, the importer uses the relative ID from the import file to look up which user to link, and then uses the email address to find the correct user in the database. Therefore if you want to link objects to a user that is already in the database you can specify the bare minimum information for that user so that it can be mapped correctly:

```
"users": [{
   id: 35,
   name: "A User",
   email: "user@example.com"
}]

```

If the importer is unable to find a reference for the user inside the import file, it will default to the Owner.

#### User Roles

All users are given the role of `author` by default. If you want to specify different roles, you can do so by providing a `roles_users` object, much like the `posts_tags` object. Please note that Ghost doesn’t yet support importing roles, so in this case the `role_id` is always relative to the `id` in the database, rather than in the file.

##### On this page

Launch your site
----------------

Last week, 5,069 brand new  
publications got started with Ghost.

Today, it's your turn.

[Start a free trial now →](https://account.ghost.org/signup/)Product

* [Creator platform](/)
* [Theme marketplace](/marketplace/)
* [Integrations](/integrations/)
* [Experts](/experts/)
* [Ghost for news](/news/)
Developers

* [How to install Ghost](/docs/install/)
* [Core concepts](/docs/)
* [Ghost hosting](/pricing/)
* [API documentation](/docs/content-api/)
* [Security overview](/docs/security/)
* [Source code](https://github.com/TryGhost/Ghost)
Resources

* [Ghost tutorials](/tutorials/)
* [Resources](/resources/)
* [Node.js CMS guide](https://nodecms.guide)
* [Open Subscription Platforms](https://opensubscriptionplatforms.com)
Comparisons

* [Ghost vs Substack](/vs/substack/)
* [Ghost vs WordPress](/vs/wordpress/)
* [Ghost vs Medium](/vs/medium/)
* [Ghost vs Memberful](/vs/memberful/)
* [Ghost vs Patreon](/vs/patreon/)
* [Ghost alternatives →](/alternatives/)
Support

* [Help center](/help/)
* [Community forum](https://forum.ghost.org/)
* [Status  
  Triangle
  
  
  
   99.9%](https://status.ghost.org/)
[![Non-Profit Foundation](/images/logos/indie.svg)](/about/)
[![Open Source](/images/logos/opensource.svg)](https://github.com/tryghost)
[![Carbon Neutral](/images/logos/carbonneutral.svg)](https://climate.stripe.com/6MNofu)

