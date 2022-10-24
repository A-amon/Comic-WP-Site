# Comic-WP-Site
**Please note that the media assets used in this project do not belong to me.** 😁  
```  
Hopefully you may find this project helpful in setting up your own comic reading/publishing site! 🥳  
```

## Screenshots
<table>
<tr>
<td><img src="https://github.com/A-amon/Comic-WP-Site/blob/main/demo/login.PNG"/></td>
<td><img src="https://github.com/A-amon/Comic-WP-Site/blob/main/demo/home.PNG"/></td>
</tr>
<tr>
<td><img src="https://github.com/A-amon/Comic-WP-Site/blob/main/demo/book.PNG"/></td>
<td><img src="https://github.com/A-amon/Comic-WP-Site/blob/main/demo/chapter.PNG"/></td>
</tr>
</table>

## Getting Started
The code and required settings have been included in this [SQL file](https://github.com/A-amon/Comic-WP-Site/blob/main/wp.sql).  
`❗ wp_usermeta, wp_users and wp_options are excluded from the SQL file ❗`
  
These include code for:
- REST API ➡ rate, follow titles
- Books menu ➡ for performing CRUD on Titles and Chapters
- Additional columns in Chapters and Titles admin tables
- Basic Pods Templates code ➡ for displaying books information
- Basic theme customisations
- Ready-to-use shortcodes

|Shortcode|Attribute(s)|Description|
|---------|------------|-----------|
|pods-override|override|Call Pods shortcode with overridden attributes <br/> E.g. <br/> If override="slug", set `slug` attribute on Pods shortcode to current page's slug|
|post-time|datetime|Show datetime passed since the provided `datetime` value (Find current post's datetime if `datetime` attribute is unset)
|post-control|taxonomy, home|Show Previous/ Next post links <br/> Set `taxonomy` attribute to relevant taxonomy name if require previous/next linking to posts with same taxonomy <br/> Set `home` attribute to "true" if require showing "Home" link on last post|
|follow-title|slug|Set "Follow" button's initial status using "Follow Button" reusable block|
|rate-title|slug|Set "Rating" input's initial status using "Rating Input" reusable block <br/> Rating defaults to 1 if no rating yet|

Add `define('PODS_SHORTCODE_ALLOW_SUB_SHORTCODES',true);` to `wp-config.php`  
  
Set your homepage to use `Home` at your Settings > Reading  

Include the [uploads](https://github.com/A-amon/Comic-WP-Site/tree/main/uploads/2022) folder in your project too because the examples/setups are using them.
  
**Plugins (❗)**
- [Content Control](https://wordpress.org/plugins/content-control/)
- [My Custom Functions](https://wordpress.org/plugins/my-custom-functions/)
- [Pods](https://wordpress.org/plugins/pods/)
- [Reusable Blocks Extended](https://wordpress.org/plugins/reusable-blocks-extended)
- [Theme My Login](https://wordpress.org/plugins/theme-my-login/)
- [WP Revisions Control](https://wordpress.org/plugins/wp-revisions-control/)
  
*Developed on*  
Wordpress 6.0.3  
**Theme:** Twenty Twenty-Two  
XAMPP Version: 7.3.4
## Notes

Security-wise, I used [Wordpress' Nonce](https://codex.wordpress.org/WordPress_Nonces) to authenticate/identify the user when  
performing actions restricted for logged in users (rate, follow)  
  
This project's meant to be my playground for Wordpress so, it can be considered work-in-progress. 😉
  
Don't hesitate to drop your suggestion/feedback in the [Issues](https://github.com/A-amon/Comic-WP-Site/issues) section.  
I'll get to them when I have time. 😂
