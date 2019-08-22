# Using the Shortcode

<style>
    .notice {
        background-color: #FEC;
        padding: 0.5rem 1rem;
        border-radius: .25rem;
        color: #654a15;
    }
</style>

<div style="padding-top: 56.25%; position: relative;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/Ax-MSgWP5ww" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<p class="notice">**This tutorial was made for Video Background Pro, but will also work for Video Background.**</p>

The shortcode is the backbone of the entire Video Background plugin. Whether or not you realize it, every other way to create a video background (metabox, WPBakery, SiteOrigin) all end up using the shortcode to initialize the plugin and add it to your website.

## Parameters

The shortcode has parameters that you can specify to tailor your video background experience.

**It's important to note that due to the way that shortcodes are implemented, every value is interpreted as a string.**

| Parameter | Description | Accepts | Default Value
| -|-| -| -| -|
| container | The container value. This is where your video background will go. This parameter is required. | Any DOM Element | ""
| mp4 | The .mp4 file link. | Any URL with an `.mp4` file extension. | "#"
| webm | The .webm file link. | Any URL with a `.webm` file extension. | "#"
| poster | The poster image will be shown while the video is loading and for devices/browsers that do not support video backgrounds. | Any URL to an image. .png and .jpg are recommended. | "#"
| muted | This option has been depreciated due to browser restrictions. As of Video Background 2.7.0 this option will no longer do anything. | `true` or `false` | "true"
| loop | This option will dictate whether or not the video background will loop. | `true` or `false` | "true"
| overlay | To enable the overlay or not. | `true` or `false` | "false"
| overlay_color | Specify the color of the overlay as a hex color. The `overlay` parameter must be set to `true` for this to take effect. | Any Hex color. | "#000"
| overlay_alpha | Specify the amount of transparency your overlay will have. This can be useful for text legibility. | A value between `0.00` and `1.00` where `0.00` is completely transparent and `1.00` begin opaque. | "0.3"

## Constructing the Shortcode

When you are constructing the shortcode, you only need to add the parameters that matter to you. If we wanted a simple video background with an mp4 video and fallback image, our shortcode would look something like this:

```
[vidbg container=".my-section-5" mp4="http://example.com/link-to-video.mp4" poster="http://example.com/link-to-fallback.png"]
```