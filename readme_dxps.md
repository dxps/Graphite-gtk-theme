## My Notes on Changes

1. Fixed the `cp` issue (just using `-f` instead of `-rf`) on `parse-sass.sh` and `install.sh` scripts.
2. Using font size 11 (in `src/sass/gnome-shell/_variables.scss`).
3. Darker border color for Gnome Shell (see `// dxps` comments in `src/sass/gnome-shell/common/*.scss` files).
4. Darker border color for Windows and other modals (see `// dxps` comments in `src/sass/gtk/_common-3.0.scss`, `src/sass/gtk/_common-4.0.scss`, and `src/sass/gtk/apps/_gnome-3.0.scss` files).

It all started with [this issue](https://github.com/vinceliuice/Graphite-gtk-theme/issues/17#issuecomment-987761429).

### Changes & Apply

After doing changes, make sure you run `./parse-sass.sh` before `./install.sh`.<br/>
All installs ran fine, as long as I change the _settings_ in `src/sass/_tweaks.scss` instead of providing the install flags.
