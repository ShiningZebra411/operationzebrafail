
Saves use a custom format and `.gsf` extension that is not compatible with other emulators. If no save path is specified,
the same path as the ROM is used, but with the `.gsf` extension instead of whatever the ROM image is using. If no save is
found matching either the given or default path, then a new save is created using that path. Saves are overwritten on exit,
unless the `--nosave` argument is used.

When using multiplayer, the same save file resolution algorithm is used. If there are conflicting paths, they are fixed by
appending an index. It's incremented for each previous player that has a conflicting save file.

The emulator can almost always auto-detect the save type, but it's not guaranteed to always work. If it doesn't work, then you will need to
use the following switches to configure the save memory manually.

The `--save-memory` switch is used to configure the main save memory. It takes any one of the following arguments (case senstive).

| Argument   | Description         |
|------------|---------------------|
| SRAM       | 64KB of static RAM  |
| FLASH_512K | 512Kb of Flash      |
| FLASH_1M   | 1Mb of Flash        |
| NONE       | No main save memory |
| AUTO       | Decide from the ROM |

The `--eeprom` and `--rtc` switches are used to configure the optional EEPROM and RTC respectively.
They take any one of the following arguments (case senstive).

| Argument | Description         |
|----------|---------------------|
| ON       | Enabled             |
| OFF      | Disabled            |
| AUTO     | Decide from the ROM |

These flags are only needed when creating a new save, after that the format is saved in the save file.

### GBA controls ###

These will be re-mapable in a future version.

| Gamepad | Keyboard | Controller       |
|---------|----------|------------------|
| A       | P        | A                |
| B       | L        | B                |
| Up      | W        | D-pad or L-stick |
| Down    | S        | D-pad or L-stick |
| Right   | D        | D-pad or L-stick |
| Left    | A        | D-pad or L-stick |
| R       | R-shift  | RB or RT         |
| L       | L-shift  | LB or LT         |
| Start   | Enter    | Start            |
| Select  | Tab      | Select           |

### Emulator controls ###

These will be re-mapable in a future version.

| Function      | Keyboard | Controller       |
|---------------|----------|------------------|
| Quick save    | Q        | X                |
| Switch player | 1 to 4   | N/A              |

Quick saves are not save states, they just write the contents of the save memory to the save file immediately.
Otherwise this is only done on exit. This is useful to ensure you do not loose game progress if the emulator crashes
or fails to close normally. Note that quick saves are disabled when using the `-N` switch.


