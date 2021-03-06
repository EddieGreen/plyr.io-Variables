# plyr.io-Variables

Default playr.io CSS generated with variables, allowing users to modify player appearance and functionality using CSS variables.

## plyr.io

This is based on compiled SCSS code from https://github.com/sampotts/plyr.

The latest release in this repo adopts the version number of the code available in the playr.io repository.

### Revisions

**10/02/2021** - 3.6.4

## CDN Sources

The compiled CSS is available using the following CDN sources. These will always be the latest version published in this repo. See revisions above.

https://cdn.jsdelivr.net/gh/EddieGreen/plyr.io-Variables@master/plyr.min.css

https://cdn.jsdelivr.net/gh/EddieGreen/plyr.io-Variables@master/plyr.css

## Visual Studio 2019

The project can be opened and modified as a web site project - See solution file. Requires Web Essentials 2019 extension in VS2019 in order to compile scss/sass code - see https://github.com/madskristensen/WebEssentials2019

## Usage Example

Set for all players - CSS selector targets `:root`

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/EddieGreen/plyr.io-Variables@master/plyr.min.css" />
<style>
:root {
  --plyr-color-main: #d62a14;
  --plyr-font-size-captions-large: 21px;
  --plyr-control-radius: 50%; }
</style>
```

Set for a specific class of player
```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/EddieGreen/plyr.io-Variables@master/plyr.min.css" />
<style>
.sample_player {
  --plyr-color-main: #d62a14;
  --plyr-font-size-captions-large: 21px;
  --plyr-control-radius: 50%; }
</style>
```

Set to individual player
```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/EddieGreen/plyr.io-Variables@master/plyr.min.css" />
<video class="player" style="--plyr-color-main: #d62a14; --plyr-font-size-captions-large: 21px; --plyr-control-radius: 50%;">
    ...
</video>
```

## Customizing the CSS

If you want to change any design tokens used for the rendering of the player, you can do so using [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties).

Here's a list of the properties and what they are used for:

| Name                                           | Description                                                                                             | Default / Fallback                                                    |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `--plyr-color-main`                            | The primary UI color.                                                                                   | ![#f03c15](https://placehold.it/15/00b3ff/000000?text=+) `#00b3ff`    |
| `--plyr-video-background`                      | The background color of video and poster wrappers for using alpha channel videos and poster images.     | `rgba(0, 0, 0, 1)`    |
| `--plyr-tab-focus-color`                       | The color used for the dotted outline when an element is `:focus-visible` (equivalent) keyboard focus.  | `--plyr-color-main`                                                   |
| `--plyr-badge-background`                      | The background color for badges in the menu.                                                            | ![#4a5464](https://placehold.it/15/4a5464/000000?text=+) `#4a5464`    |
| `--plyr-badge-text-color`                      | The text color for badges.                                                                              | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-badge-border-radius`                   | The border radius used for badges.                                                                      | `2px`                                                                 |
| `--plyr-tab-focus-color`                       | The color used to highlight tab (keyboard) focus.                                                       | `--plyr-color-main`                                                   |
| `--plyr-captions-background`                   | The color for the background of captions.                                                               | `rgba(0, 0, 0, 0.8)`                                                  |
| `--plyr-captions-text-color`                   | The color used for the captions text.                                                                   | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-control-icon-size`                     | The size of the icons used in the controls.                                                             | `18px`                                                                |
| `--plyr-control-spacing`                       | The space between controls (sometimes used in a multiple - e.g. `10px / 2 = 5px`).                      | `10px`                                                                |
| `--plyr-control-padding`                       | The padding inside controls.                                                                            | `--plyr-control-spacing * 0.7` (`7px`)                                |
| `--plyr-control-radius`                        | The border radius used on controls.                                                                     | `3px`                                                                 |
| `--plyr-control-toggle-checked-background`     | The background color used for checked menu items.                                                       | `--plyr-color-main`                                                   |
| `--plyr-video-controls-background`             | The background for the video controls.                                                                  | `linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75))`              |
| `--plyr-video-control-color`                   | The text/icon color for video controls.                                                                 | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-video-control-color-hover`             | The text/icon color used when video controls are `:hover`, `:focus` and `:focus-visible` (equivalent).  | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-video-control-background-hover`        | The background color used when video controls are `:hover`, `:focus` and `:focus-visible` (equivalent). | `--plyr-color-main`                                                   |
| `--plyr-audio-controls-background`             | The background for the audio controls.                                                                  | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-audio-control-color`                   | The text/icon color for audio controls.                                                                 | ![#4a5464](https://placehold.it/15/4a5464/000000?text=+) `#4a5464`    |
| `--plyr-audio-control-color-hover`             | The text/icon color used when audio controls are `:hover`, `:focus` and `:focus-visible` (equivalent).  | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-audio-control-background-hover`        | The background color used when video controls are `:hover`, `:focus` and `:focus-visible` (equivalent). | `--plyr-color-main`                                                   |
| `--plyr-menu-background`                       | The background color for menus.                                                                         | `rgba(255, 255, 255, 0.9)`                                            |
| `--plyr-menu-color`                            | The text/icon color for menu items.                                                                     | ![#4a5464](https://placehold.it/15/4a5464/000000?text=+) `#4a5464`    |
| `--plyr-menu-shadow`                           | The shadow used on menus.                                                                               | `0 1px 2px rgba(0, 0, 0, 0.15)`                                       |
| `--plyr-menu-radius`                           | The border radius on the menu.                                                                          | `4px`                                                                 |
| `--plyr-menu-arrow-size`                       | The size of the arrow on the bottom of the menu.                                                        | `6px`                                                                 |
| `--plyr-menu-item-arrow-color`                 | The color of the arrows in the menu.                                                                    | ![#728197](https://placehold.it/15/728197/000000?text=+) `#728197`    |
| `--plyr-menu-item-arrow-size`                  | The size of the arrows in the menu.                                                                     | `4px`                                                                 |
| `--plyr-menu-border-color`                     | The border color for the bottom of the back button in the top of the sub menu pages.                    | ![#dcdfe5](https://placehold.it/15/dcdfe5/000000?text=+) `#dcdfe5`    |
| `--plyr-menu-border-shadow-color`              | The shadow below the border of the back button in the top of the sub menu pages.                        | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-progress-loading-size`                 | The size of the stripes in the loading state in the scrubber.                                           | `25px`                                                                |
| `--plyr-progress-loading-background`           | The background color on the loading state in the scrubber.                                              | `rgba(35, 40, 47, 0.6)`                                               |
| `--plyr-video-progress-buffered-background`    | The fill color for the buffer indication in the scrubber for video.                                     | `rgba(255, 255, 255, 0.25)`                                           |
| `--plyr-audio-progress-buffered-background`    | The fill color for the buffer indication in the scrubber for audio.                                     | `rgba(193, 200, 209, 0.6)`                                            |
| `--plyr-range-thumb-height`                    | The height of the scrubber handle/thumb.                                                                | `13px`                                                                |
| `--plyr-range-thumb-background`                | The background of the scrubber handle/thumb.                                                            | ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `#ffffff`    |
| `--plyr-range-thumb-shadow`                    | The shadow of the scrubber handle/thumb.                                                                | `0 1px 1px rgba(215, 26, 18, 0.15), 0 0 0 1px rgba(215, 26, 18, 0.2)` |
| `--plyr-range-thumb-active-shadow-width`       | The width of the shadow when the scrubber handle/thumb is `:active` (pressed).                          | `3px`                                                                 |
| `--plyr-range-track-height`                    | The height of the scrubber/progress track.                                                              | `5px`                                                                 |
| `--plyr-range-fill-background`                 | The fill color of the scrubber/progress.                                                                | `--plyr-color-main`                                                   |
| `--plyr-video-range-track-background`          | The background of the scrubber/progress.                                                                | `--plyr-video-progress-buffered-background`                           |
| `--plyr-video-range-thumb-active-shadow-color` | The color of the shadow when the video scrubber handle/thumb is `:active` (pressed).                    | `rgba(255, 255, 255, 0.5)`                                            |
| `--plyr-audio-range-track-background`          | The background of the scrubber/progress.                                                                | `--plyr-video-progress-buffered-background`                           |
| `--plyr-audio-range-thumb-active-shadow-color` | The color of the shadow when the audio scrubber handle/thumb is `:active` (pressed).                    | `rgba(215, 26, 18, 0.1)`                                              |
| `--plyr-tooltip-background`                    | The background color for tooltips.                                                                      | `rgba(255, 255, 255, 0.9)`                                            |
| `--plyr-tooltip-color`                         | The text color for tooltips.                                                                            | ![#4a5464](https://placehold.it/15/4a5464/000000?text=+) `#4a5464`    |
| `--plyr-tooltip-padding`                       | The padding for tooltips.                                                                               | `calc(var(--plyr-control-spacing) / 2))`                              |
| `--plyr-tooltip-arrow-size`                    | The size of the arrow under tooltips.                                                                   | `4px`                                                                 |
| `--plyr-tooltip-radius`                        | The border radius on tooltips.                                                                          | `3px`                                                                 |
| `--plyr-tooltip-shadow`                        | The shadow on tooltips.                                                                                 | `0 1px 2px rgba(0, 0, 0, 0.15)`                                       |
| `--plyr-font-family`                           | The font family used in the player.                                                                     |                                                                       |
| `--plyr-font-size-base`                        | The base font size. Mainly used for captions.                                                           | `15px`                                                                |
| `--plyr-font-size-small`                       | The smaller font size. Mainly used for captions.                                                        | `13px`                                                                |
| `--plyr-font-size-large`                       | The larger font size. Mainly used for captions.                                                         | `18px`                                                                |
| `--plyr-font-size-xlarge`                      | The even larger font size. Mainly used for captions.                                                    | `21px`                                                                |
| `--plyr-font-size-time`                        | The font size for the time.                                                                             | `--plyr-font-size-small`                                              |
| `--plyr-font-size-menu`                        | The font size used in the menu.                                                                         | `--plyr-font-size-small`                                              |
| `--plyr-font-size-badge`                       | The font size used for badges.                                                                          | `9px`                                                                 |
| `--plyr-font-weight-regular`                   | The regular font weight.                                                                                | `400`                                                                 |
| `--plyr-font-weight-bold`                      | The bold font weight.                                                                                   | `600`                                                                 |
| `--plyr-line-height`                           | The line height used within the player.                                                                 | `1.7`                                                                 |
| `--plyr-font-smoothing`                        | Whether to enable font antialiasing within the player.                                                  | `false`                                                               |
