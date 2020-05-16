# In process since 2020-05-16

Colemak-Qwerty hotkeys XKB configuration files for Linux(Ubuntu 20.04)

Inspired by https://github.com/ZeptByteS/dvorak-qwerty

# Installation

#### 1. Copy the "colemak_qwerty" file

```
git clone https://github.com/the-devil-you-know/colemak-qwerty-x11-xkb.git
cd colemak-qwerty-x11-xkb
sudo cp colemak_qwerty /usr/share/X11/xkb/types/colemak_qwerty
```

#### 2. Update the xkb "complete" file

Add `include "colemak_qwerty"` to the "complete" file

```
sudo gedit /usr/share/X11/xkb/types/complete
```

It should look like this:
```
default xkb_types "complete" {
    include "basic"
    include "mousekeys"
    include "pc"
    include "iso9995"
    include "level5"
    include "extra"
    include "numpad"
    include "colemak_qwerty"
};
```

#### 3. Update the "us" file

Copy the text from the "us-colemak" file and past it at the and of the xkb "us" file
```
sudo gedit /usr/share/X11/xkb/symbols/us
```
