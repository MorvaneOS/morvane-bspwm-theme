# morvane-bspwm-theme

The MorvaneOS look for bspwm: bspwm's example `bspwmrc` with a Pastel Pink border
on the focused window and the Twilight wallpaper, and its example `sxhkdrc` with
dmenu in MorvaneOS colours.

bspwm and sxhkd read only `~/.config/bspwm/bspwmrc` and `~/.config/sxhkd/sxhkdrc`,
so there's nothing system-wide to set. This package installs the themed configs in
`/usr/share/morvane-bspwm-theme/`, and the MorvaneOS installer copies them to new
users' `~/.config`. They're then yours to edit; package updates don't change your
copies.

Terminal colours (urxvt) come from
[morvane-wm-theme](https://github.com/MorvaneOS/morvane-wm-theme), apps from
[morvane-gtk-theme](https://github.com/MorvaneOS/morvane-gtk-theme).

## Changing it

Edit `tools/build.py`, then run it on bspwm's examples
(`/usr/share/doc/bspwm/examples`):

```
python tools/build.py [path/to/bspwm/examples]
```

Needs only Python. Commit the output, bump `pkgver`, build and publish.

## License

BSD-2-Clause, like bspwm, since the configs are its examples with the MorvaneOS look
added.
