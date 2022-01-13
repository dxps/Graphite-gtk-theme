## My Notes on Changes

- Using font size 11 for compact as well (in `src/sass/gnome-shell/_variables.scss`).
  ```scss
  $font_size: if($compact == 'false', 11, 11);
  ```

- Updated `%theme_dialogs`'s `box-shadow` (in `src/sass/gnome-shell/common/_dialogs.scss`):
  ```scss
  box-shadow: 8px 8px 16px -13px rgba(black, 0.35);
  ```
  
- Updated `shadow-z`s (in `src/sass/_variables.scss`):
  ```scss
  $shadow-z1:
    // 0 2px 2px -2px rgba(black, 0.3),
    // 0 1px 2px -1px rgba(black, 0.24),
    // 0 1px 2px -.6px rgba(black, 0.17);
    0 6px 6px -8px rgba(black, 0.4),
    0 4px 6px -6px rgba(black, 0.34),
    0 4px 6px -.8px rgba(black, 0.27);
  $shadow-z2:
    0 3px 2px -10px rgba(black, 0.3),
    0 2px 2px -9px rgba(black, 0.24),
    0 1px (5px * .6) 0 rgba(black, 0.12);
  $shadow-z3:
    0 3px 2px -2px rgba(black, 0.2),
    0 3px (4px * .6) 0 rgba(black, 0.14),
    0 1px (8px * .6) 0 rgba(black, 0.12);
  $shadow-z4:
    0 2px (4px * .6) -1px rgba(black, 0.2),
    0 4px (5px * .6) 0 rgba(black, 0.14),
    0 1px (10px * .6) 0 rgba(black, 0.12);
  $shadow-z12:
    0 7px (8px * .6) -4px rgba(black, 0.2),
    0 12px (17px * .6) 2px rgba(black, 0.14),
    0 5px (22px * .6) 4px rgba(black, 0.12);
  $shadow-z16:
    //  0 8px (10px * .6) -5px rgba(black, 0.2),
    // 0 16px (24px * .6) 2px rgba(black, 0.14),
    // 0 6px (30px * .6) 5px rgba(black, 0.12);
    0 8px (10px * .6) -8px rgba(black, 0.4),
    0 16px (24px * .6) 4px rgba(black, 0.34),
    0 6px (30px * .6) 8px rgba(black, 0.32);
  ```

<br/>

### Changes & Apply

- After doing changes, make sure you run `./parse-sass.sh` before installing it.<br/>

- I started using the borderless flavor, installed using:<br/>
  `./install.sh -c dark -s compact --tweaks rimless`.

<br/>
