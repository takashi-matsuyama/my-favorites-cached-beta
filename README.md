# My Favorites Cached Beta

This is the development repository for My Favorites Cached Beta, a WordPress plugin that saves user's favorite posts and lists them. Development of the WordPress plugin "my-favorites" to work with cached WordPress. If you want to test this code, please do so in a test environment. It may cause bugs and various problems.

Contributors: takashimatsuyama  
Donate link:  
Tags: favorites, likes, accessibility, favorite posts  
Requires at least: 4.8  
Tested up to: 5.9  
Requires PHP: 5.4.0  
Stable tag: 0.0.0  
License: GPLv2 or later  
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Save user's favorite posts and list them.

## Description

Save user's favorite posts and list them.
This plugin is simple. You can save the user's favorite posts just a install and display them anywhere you want with just a shortcode.
The logged-in user's data is saved in the user meta. Other user's data is saved to Web Storage (localStorage).

## Usage

- **Shortcode:** `[ccc_my_favorite_select_button post_id="" style=""]`
- **Shortcode:** `[ccc_my_favorite_list_menu slug="" text="" style=""]`
- **Shortcode:** `[ccc_my_favorite_list_results class="" style=""]`

For pages with a shortcode for list view ([ccc_my_favorite_list_results]).

"Load More" is displayed with "posts_per_page".
It will be displayed when the user has more favorite posts than "posts_per_page".

- **Shortcode:** `[ccc_my_favorite_list_results posts_per_page="10"]` default is 100 posts.

You can display the post's "excerpt".
This value is the char length.
If not needed, use "no excerpt" or "0".

- **Shortcode:** `[ccc_my_favorite_list_results excerpt="30"]`

If you want, you can change the code for list view yourself.

- **Shortcode:** `[ccc_my_favorite_list_custom_template style=""]`

For pages with a shortcode for custom list view ([ccc_my_favorite_list_custom_template]).
Add the function (`function ccc_my_favorite_list_custom_template( $my_favorite_post_id ) { }`) for your list view to `your-theme/functions.php`.
`$my_favorite_post_id` is array.
`style="none"` excludes the default CSS for the list.

Detailed usage is under preparation.

## Installation

It seems to be working with cached websites, probably in my environment. However, I have not verified it from various perspectives and it is just a test code to accomplish one task.  It is quite possible that this change may cause loss of traditional functionality or other bugs.
Therefore, I cannot yet merge the changes of this issue into the official WordPress.org directory, but we would like to test it for future use and verify it in this repository as I review the specification.
If you want to test this code, please do so in a test environment. It may cause bugs and various problems.

1. Upload `my-favorites-cached-beta` to the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. Use shortcodes to display the favorite posts list and an icon for save and a menu for link to list.

## Changelog

### 0.0.0

Update: Initial test.
