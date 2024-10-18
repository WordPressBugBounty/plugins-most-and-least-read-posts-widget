=== Most And Least Read Posts Widget ===
Contributors: whiletrue
Donate link: https://www.whiletrue.it/
Tags: popular posts, post, posts, most read, least read, more read, top posts, less read, sidebar, widget, links 
Requires at least: 2.9+
Requires PHP: 7.0
Tested up to: 6.6
Stable tag: 2.5.20

Provide two widgets, showing lists of the most and reast read posts.

== Description ==
"Most And Least Read Posts Widget" is a free plugin for Wordpress. developed by Giuliano Polverari (WhileTrue.it) to generate lists of the most and least read posts.

The following options are customizable:

* number of posts to show
* exclude posts whose title contains certain words
* show post hits after the title (style customizable via CSS class)
* exclude posts older than XX days

The plugin starts counting hits once activated, storing them in the "custom_total_hits" custom field without the need of external accounts.

The most popular web crawlers (e.g. Googlebot) are recognized and their hits discarded; also Admin hits are discarded.

Archived post hits are shown in a column inside the backend post list.

The plugin is compatible with multi-language WPML plugin, showing most/least read posts for current language.

Optionally, the number of hits can be shown inside the post content, with:

* a custom phrase, e.g. "This post has already been read XX times!"
* a custom position (above the post, below the post, both)
* a custom CSS style

If you want to show the post hits anywhere inside the template loop, you can the PHP function provided, e.g.: 

`echo most_and_least_read_posts_get_hits(get_the_ID());`

= Shortcode =

Also, [most_read_posts] a shortcode is available. Use it like this:

`[most_read_posts type="most" posts_number="5" show_thumbs="false" date_from="2016-01-01" date_to="2016-04-30"]`

Shortcode attributes:

* type: "most" or "least"
* posts_number
* words_excluded
* title_max_chars
* excerpt_max_chars
* show_thumbs: "true" or "false"
* add_line_break_before_thumbs: "true" or "false"
*	show_hits: "true" or "false"
*	show_hits_text (default: "views")
* days_ago
* date_from and date_to: if set, overwrite the "days_ago" attribute (format: YYYY-MM-DD)

= Reference =

For more informations: [www.whiletrue.it](https://www.whiletrue.it/most-and-least-read-posts-widget-for-wordpress/ "www.whiletrue.it")

Do you like this plugin? Give a chance to our other works:

* [Good old Share](https://www.whiletrue.it/really-simple-share-wordpress-plugin/ "Good old Share")
* [Good old Twitter Feed Widget](https://www.whiletrue.it/really-simple-twitter-feed-widget-for-wordpress/ "Good old Twitter Feed Widget")
* [Tilted Tag Cloud Widget](https://www.whiletrue.it/tilted-tag-cloud-widget-per-wordpress/ "Tilted Tag Cloud Widget")
* [Reading Time](https://www.whiletrue.it/reading-time-for-wordpress/ "Reading Time")


== Installation ==
Best is to install directly from WordPress. If manual installation is required, please make sure to put all of the plugin files in a folder named `most_and_least_read_posts_widget` (not two nested folders) in the plugin directory, then activate the plugin through the `Plugins` menu in WordPress.

== Screenshots ==
1. Sample Widget on site, plain wiew 
2. Sample Widget on site, with post hits and thumbs 
3. Options available in the Admin Widget box
4. Options available in the Admin Settings menu 


== Frequently Asked Questions ==

= I get an error message that says "no results available" =
The plugin starts collecting hits once installed, so there are "no results available" for a short time, until the first data is stored. 
It's better to show the widget some hours (or days) after having installed it.

= The same post shows up multiple times =
This uncommon issue can be caused by duplicated custom fields in some posts. 
To solve it, inspect the post custom fields and delete unnecessary duplicates of the "custom_total_hits" field. 

= Can I customize the thumbs? =
Yes, you can do it editing the "mlrp_ul" class in your template style.css file.
E.g. 50x50 pixels images, floating on the right:
.mlrp_ul img { width: 50px; height: 50px; float: right; }

== Changelog ==

= 2.5.20 =
* Plugin tested up WordPress 6.6
* Fixed: SQL injection
* Fixed: CSS injection
* Fixed: PHP warnings

= 2.5.5 =
* Added: New "Add line break before thumb", "Limit post titles to X chars" and "Show post excerpts" options
* Added: internationalization
* Added: [most_read_posts] shortcode
* Added: Use the comma "," for thousands digits
* Added: Append a custom text (e.g. the word "views") next to total hits
* Added: WhileTrue RSS Feed
* Changed: web spiders update
* Changed: Avangate ads removal
* Changed: Skip updating hits if user is admin

= 1.9 =
* Added: option to show hits inside the post content or after the post title
* Added: style customization of hits on widget, through the "most_and_least_read_posts_hits" CSS class
* Added: option to exclude posts older than XX days (default: 365 days)
* Added: Frequently Asked Questions
* Added: archived post hits are now shown in a column inside the backend post list
* Added: php function to retrieve and show hits inside the template loop
* Added: show post thumbs option
* Added: "mlrp_ul" ul class for easy CSS styling
* Added: support for WPML plugin, showing most/least read posts for current language
* Changed: hits on widget put out of the link

= 1.0.0 =
Initial release


== Upgrade Notice ==

= 1.0.0 =
Initial release
