Colemak-Qwerty hotkeys XKB configuration files for Linux(Ubuntu 20.04)


# Installation

```
$ git clone https://github.com/the-devil-you-know/colemak-qwerty-x11-xkb.git
$ xkbcomp colemak-qwerty-x11-xkb/.xkb_keymap_us $DISPLAY
```
**Congratulations! Everything is ready!**

You may see a lot of warnings, don't worry about it.


# Personalization

This layout has remappings:

1. Return is mapped to the Alt_r
2. Mode_switch to the Caps
3. Ctrl_l to the Alt_l
4. Alt_l to the Ctrl_l

If you don't need it, remove from the **.xkb_keymap_us**:
```
key <RALT> { actions[Group1]=[ RedirectKey(keycode=<RTRN>) ] };
key <LALT> { [ Control_L, Control_L ] };
key <LCTL> { [ Alt_L ] };
key <CAPS> { [ Mode_switch ] };

modifier_map Control { <LALT> };
modifier_map Mod1 { <LCTL> };
```

# Additional features

![additional features](additional_features.jpg)

Hold down the **Mode_switch** (which is mapped to the **Caps**) and you will have a layout like in the picture above.
