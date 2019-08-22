# Add Custom Post Types to Metabox

To add the Video Background metabox to a custom post type, add the function below to your `functions.php` file. In the `$post_types` `array`, add your desired custom post types.

```php
/**
 * Define Video Backgrounds post types
 *
 * @since 2.5.7
 * @author Push Labs
 * @param array $post_types
 * @return array Array of post types Video Background should use
 */
function themeprefix_vidbg_post_types( $post_types ) {
  /**
   * list the post types you would like Video Background
   * to use in the form of an array
   */
  $post_types = array( 'post', 'page' );
  return $post_types;
}
add_filter( 'vidbg_post_types', 'themeprefix_vidbg_post_types' );
```