<!-- DO NOT EDIT THIS FILE; it is auto-generated from readme.txt -->
# Archived Post Status

![Banner](assets/banner-1544x500.png)
Allows posts and pages to be archived so you can unpublish content without having to trash it.

**Contributors:** [fjarrett](https://profiles.wordpress.org/fjarrett)  
**Tags:** [admin](https://wordpress.org/plugins/tags/admin), [posts](https://wordpress.org/plugins/tags/posts), [pages](https://wordpress.org/plugins/tags/pages), [status](https://wordpress.org/plugins/tags/status), [workflow](https://wordpress.org/plugins/tags/workflow)  
**Requires at least:** 3.0  
**Tested up to:** 4.1  
**Stable tag:** 0.3.0  
**License:** [GPLv2 or later](http://www.gnu.org/licenses/gpl-2.0.html)  

[![Build Status](https://travis-ci.org/fjarrett/archived-post-status.png?branch=master)](https://travis-ci.org/fjarrett/archived-post-status) 

## Description ##

**Did you find this plugin helpful? Please consider [writing a review](https://wordpress.org/support/view/plugin-reviews/archived-post-status).**

This plugin allows you to archive your WordPress content similar to the way you archive your e-mail.

* Makes a new post status available in the dropdown called Archived
* Unpublish your posts and pages without having to trash them
* Compatible with posts, pages and custom post types
* Ideal for sites where certain kinds of content is not meant to be evergreen

**Languages supported:**

* English
* Deutsch
* Español
* Français
* Português
* Русский

**Development of this plugin is done [on GitHub](https://github.com/fjarrett/archived-post-status). Pull requests welcome. Please see [issues reported](https://github.com/fjarrett/archived-post-status/issues) there before going to the plugin forum.**

## Frequently Asked Questions ##

### Isn't this the same as using the Draft or Private statuses? ###
Actually, no, they are not the same thing.

The Draft status is a "pre-published" status that is reserved for content that is still being worked on. You can still make changes to content marked as Draft, and you can preview your changes.

The Private status is a special kind of published status. It means the content is published, but only certain logged-in users can view it.

The Archived post status, on the other hand, is meant to be a "post-published" status. Once a post has been set to Archived it can no longer be edited or viewed.

Of course, you can always change the status back to Draft or Publish if you want to be able to edit its content again.

### Can't I just trash old content I don't want anymore? ###
Yes, there is nothing wong with trashing old content. And the behavior of the Archived status is very similar to that of trashing.

However, WordPress automatically purges trashed posts every 7 days (by default).

This is what makes the Archived post status handy. You can unpublish content without having to delete it forever.

### Can I exclude the Archived status from appearing on certain post types? ###
Yes, you can do this by using the `aps_excluded_post_types` filter:

```php
function my_aps_excluded_post_types( $post_types ) {
	$post_types[] = 'my_custom_post_type';

	return $post_types;
}
add_filter( 'aps_excluded_post_types', 'my_aps_excluded_post_types', 10, 1 );
```


## Screenshots ##

### Post list table screen

![Post list table screen](assets/screenshot-1.png)

### Quick Edit mode

![Quick Edit mode](assets/screenshot-2.png)

### Publish metabox controls

![Publish metabox controls](assets/screenshot-3.png)

## Changelog ##

### 0.3.0 - January 26, 2015 ###
* Added language support for German, Spanish, French, Portuguese and Russian
* Users with the `read_private_posts` capability can now view Archived content
* The `aps_excluded_post_types` filter now works as expected on Edit screens
* Automatically close comments and pings when content is archived
* Allow mulitple post states to exist alongside Archived in edit screen

Props [fjarrett](https://github.com/fjarrett)

### 0.2.0 - January 21, 2015 ###
* Make archived content read-only

Props [fjarrett](https://github.com/fjarrett), [pollyplummer](https://github.com/pollyplummer)

### 0.1.0 - January 4, 2015 ###
* Initial release

Props [fjarrett](https://github.com/fjarrett)


