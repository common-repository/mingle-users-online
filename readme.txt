=== Mingle - Users - Online ===
Contributors: Jay Schires

Based on the WP-UserOnline plugin.

Tags: mingle, useronline, usersonline, wp-useronline, online, users, user, ajax, widget
Requires at least: 3.0
Tested up to: 3.0
Stable tag: 0.1

Enable you to display how many users are online on your Wordpress blog with detailed statistics. Now has corrected url linking for Mingle User Profiles

== Description ==

**PHP 5 is required.**

Modified from the original: [WP-UserOnline](http://wordpress.org/extend/plugins/wp-useronline/)

This plugin enables you to display how many users are online on your Wordpress site, with detailed statistics of where they are and who they are (Members/Guests/Search Bots). Now has corrected url linking for Mingle User Profiles

Links: [Plugin News](http://icommow.com)

== Installation ==

You can either install it automatically from the WordPress admin, or do it manually:

1. Unzip the archive and put the `mingle-users-online` folder into your plugins folder (/wp-content/plugins/).
1. Activate the plugin from the Plugins menu.

= Usage =

**General Usage (With Widget)**

1. Go to `WP-Admin -> Appearance -> Widgets`
1. The widget name is <strong>Mingle Users Online</strong>.
1. Scroll down for instructions on how to create a *UserOnline Page*.


**General Usage (Without Widget)**

Open `wp-content/themes/<YOUR THEME NAME>/sidebar.php` and add Anywhere:

`
<?php if (function_exists('users_online')): ?>
	<p>Users online: <div id="useronline-count"><?php users_online(); ?></div></p>
<?php endif; ?>
`

**UserOnline Page**

1. Go to `WP-Admin -> Pages -> Add New`
1. Type any title you like in the post's title area
1. If you **ARE** using nice permalinks, after typing the title, WordPress will generate the permalink to the page. You will see an 'Edit' link just beside the permalink.
1. Click 'Edit' and type in `useronline` in the text field and click 'Save'.
1. Type `[page_useronline]` in the post's content area
1. Click 'Publish'

If you **ARE NOT** using nice permalinks, you need to go to `WP-Admin -> Settings -> Mingle User Online` and under 'UserOnline URL', you need to fill in the URL to the UserOnline Page you created above.

**UserOnline Stats (Outside WP Loop)**

To Display *Most Number Of Users Online* use:

`
<?php if (function_exists('get_most_users_online')): ?>
   <p>Most Users Ever Online Is <?php echo get_most_users_online(); ?> On <?php echo get_most_users_online_date(); ?></p>
<?php endif; ?>
`

To Display *Users Browsing Site* use:

`
<?php if (function_exists('get_users_browsing_site')): ?>
   <div id="useronline-browsing-site"><?php echo get_users_browsing_site(); ?></div>
<?php endif; ?>
`

To Display *Users Browsing A Page* use:

`
<?php if (function_exists('get_users_browsing_page')): ?>
   <div id="useronline-browsing-page"><?php echo get_users_browsing_page(); ?></div>
<?php endif; ?>
`

== Frequently Asked Questions ==

= Error on activation: "Parse error: syntax error, unexpected..." =

Make sure your host is running PHP 5. The only foolproof way to do this is to add this line to wp-config.php (after the opening `<?php` tag):

`var_dump(PHP_VERSION);`
<br>

== Changelog ==

= 0.1 =
* Corrected links for Mingle Installs


