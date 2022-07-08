## My Change Notes applied to Original Theme

- Using font size 11 for compact as well (in `src/sass/gnome-shell/_variables.scss`).
  ```scss
  $font_size: if($compact == 'false', 11, 11);
  ```

- Updated `%theme_dialogs`'s `box-shadow` (in `src/sass/gnome-shell/common/_dialogs.scss`):
  ```scss
  %theme_dialogs {
    ...
    box-shadow: 8px 8px 16px -13px rgba(black, 0.55);
  ```
  
- Updated `shadow-z`s (in `src/sass/_variables.scss`):
  ```scss
  $shadow-z1:
    0 6px 6px -8px rgba(black, 0.4),
    0 4px 6px -6px rgba(black, 0.34),
    0 4px 6px -.8px rgba(black, 0.27);
  $shadow-z2:
    0 3px 2px -10px rgba(black, 0.4),
    0 2px 2px -9px rgba(black, 0.34),
    0 1px (5px * .6) 0 rgba(black, 0.22);
  $shadow-z3:
    0 3px 2px -2px rgba(black, 0.4),
    0 3px (4px * .6) 0 rgba(black, 0.34),
    0 1px (8px * .6) 0 rgba(black, 0.32);
  $shadow-z4:
    0 2px (4px * .6) -1px rgba(black, 0.4),
    0 4px (5px * .6) 0 rgba(black, 0.34),
    0 1px (10px * .6) 0 rgba(black, 0.32);
  $shadow-z12:
    0 7px (8px * .6) -4px rgba(black, 0.4),
    0 12px (17px * .6) 2px rgba(black, 0.34),
    0 5px (22px * .6) 4px rgba(black, 0.32);
  $shadow-z16:
    0 8px (10px * .6) -8px rgba(black, 0.5),
    0 16px (24px * .6) 4px rgba(black, 0.44),
    0 6px (30px * .6) 8px rgba(black, 0.42);
  ```
- Updated Nord's dark bg colors (in `src/sass/_colors.scss`) to look awesome in both day (light) and night (dark) times:
  ```
  @function background($type) {
    @if ($color_type == 'nord') {
      ...
    @if ($darker == 'true') {
      @if ($type == 'e') { @return #1c1f26; }
      @if ($type == 'f') { @return #1e222a; }
      // [dxps] @if ($type == 'g') { @return #252a33; }
      // [dxps] @if ($type == 'g') { @return #313742; }
      @if ($type == 'g') { @return #3B4252; }
      // [dxps] @if ($type == 'h') { @return #333a47; }
      // [dxps] @if ($type == 'h') { @return #404959; }
      @if ($type == 'h') { @return #4C566A; }
    } @else {
      // @if ($type == 'e') { @return #292e38; }
      // @if ($type == 'f') { @return #2b303b; }
      // @if ($type == 'g') { @return #313744; }
      // @if ($type == 'h') { @return #404859; }
      // [dxps] Using Polar Night colors (see www.nordtheme).
      //        with 'f' as a version between e and g values.
      @if ($type == 'e') { @return #2e3440; }
      @if ($type == 'f') { @return #333A47; }
      @if ($type == 'g') { @return #3b4252; }
      @if ($type == 'h') { @return #434c5e; }
    }
  ```

<br/>

## Gruvbox Color Type

The default color type is set in `src/sass/_tweaks.css` file as `$color_type: 'gruvbox';`.
This is done since `--tweaks` flag does not support multiple values.

in `src/sass/_colors.scss` 

<br/>

## Changes & Apply

- After doing changes, make sure you run `./parse-sass.sh` before installing it.<br/>

- Install the borderless flavor using:<br/>
  `./install.sh -s compact --tweaks rimless`.

- Before applying it, use ALT + F2 to restart the X server.

Note: At least one time, when GNOME didn't detect the changes, installed it with a different name using:
`./install.sh -n GraphiteDXPS -s compact --tweaks rimless`

<br/>
