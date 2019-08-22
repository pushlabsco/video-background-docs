---
title: Change "Tap to unmute" Text
description: A filter to change the "Tap to unmute" text
---

# Change "Tap to unmute" Text

In Video Background, there is a "Tap to unmute" button to play the audio. If you would like to change the text of this button, you can do so with a filter. Please paste the following function at the bottom of your `functions.php` file. Be sure to replace the text with whatever you want.

```php
/**
 * Change Video Background "Tap to unmute" text
 *
 * @since 2.7.0
 * @author Push Labs
 * @param String $text The button text
 * @return String $text
 */
function themeprefix_vidbg_tap_to_unmute_text( $text ) {
  $text = 'Tap to unmute';
  return $text;
}
add_filter( 'vidbg_tap_to_unmute_text', 'themeprefix_vidbg_tap_to_unmute_text' );
```