# Gear Tray for Omarchy

Hides the icons on the right of the Omarchy bar behind a gear. Click the gear and they slide out to its left as it turns; click it again to hide them.

![Closed and open](screenshots/tray-closed.png)
![Open](screenshots/tray-open.png)

- **Only the gear opens and closes the drawer.** Clicking elsewhere doesn't close it and it doesn't grab the keyboard, so you can keep working with it open.
- Pressing the gear while one of the drawer's panels (e.g. Volume) is open closes both.
- Right-click the gear to manage system tray (status notifier) items.
- This is a clone of Omarchy's `omarchy.tray` with the same slide animation, rounded to whole pixels so the gear doesn't shake.

## Install

```bash
omarchy plugin add https://github.com/Albertus-de-Klerk/omarchy-gear-tray.git --enable
omarchy plugin disable omarchy.tray
omarchy restart shell
```

Put the gear alone in the bar's right section, then move the widgets you want hidden into the `tray` section:

```bash
omarchy bar move omarchy.audio --section tray
```

Command line: `omarchy-shell albertus.tray open|close|toggle|status`.

Tested on Omarchy 4.5.0.

## Remove

```bash
omarchy plugin remove albertus.tray
omarchy plugin enable omarchy.tray
omarchy restart shell
```
