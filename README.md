# In process since 2020-05-16

Colemak-Qwerty hotkeys XKB configuration files for Linux(Ubuntu 20.04)

Inspired by https://github.com/ZeptByteS/dvorak-qwerty

# Installation

It will take 2 minutes

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

#### 4. Update the "evdev.xml" file

Add
```
        <variant>
          <configItem>
            <name>colemak-qwerty</name>
            <description>English (Colemak-Qwerty)</description>
          </configItem>
        </variant>
```
to the "evdev.xml" file (for the "us" section)
```
sudo gedit /usr/share/X11/xkb/rules/evdev.xml
```

It should look like this:
```
...
            <description>English (Colemak)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>colemak-qwerty</name>
            <description>English (Colemak-Qwerty)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>dvorak</name>
...
```

#### 5. After reboot, you can choose the Colemak-Qwerty layout!
