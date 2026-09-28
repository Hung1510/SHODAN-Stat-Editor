![SHODAN Stat Editor](images/header.png)

# SHODAN Stat Editor

An in-game panel for **Helldivers 2** that changes weapon and stratagem stats while you play.
Press **F8**, pick a weapon or stratagem, and change its numbers. Changes apply at once, are
saved, and are applied again automatically every time the game starts.

**[Download the latest release](../../releases/latest)** · Requires **Bingus Shared Loader** (v15 or newer)

![The panel](images/feature.png)

## What you can change

**Weapons**: every primary, secondary and support weapon

| Section | Stats |
|---|---|
| Damage | Damage, durable damage, armor penetration (direct, slight, large and extreme angle), demolition force, stagger force, push force |
| Projectile | Projectiles per shot, velocity, drag factor, penetration slowdown |
| Fire | Fire rate (every fire mode the weapon has) |
| Ammo | Magazine size, starting magazines, magazines from supply, max spare magazines (or rounds, for weapons loaded by the round) |
| Handling | Recoil (horizontal, vertical), spread (horizontal, vertical), sway, ergonomics |

Beam weapons (Scythe, Dagger, Trident, Laser Cannon, Meltagun) get their damage from their beam
and are fully supported.

**Stratagems**

| Stratagem | Stats |
|---|---|
| All | Cooldown, and uses where limited |
| Eagles | Uses per rearm, Eagle rearm time |
| Orbital and Eagle strikes | For every projectile and blast they use: velocity, inner / outer / shockwave radius, and the full damage set above |
| Orbital Laser | Duration, tracking speed, search radius, damage tick |
| Sentries and emplacements | Their gun, stat for stat like a weapon |

## Install

1. Install **Bingus Shared Loader** (v15 or newer).
2. Download `SHODAN-Stat-Editor-v1.1.0.zip` from the [releases page](../../releases/latest).
3. Install the zip with your Helldivers 2 mod manager, like any other mod package.

## Use

Press **F8** in game to open or close the panel. The mouse works wherever the game shows a
cursor; the keyboard works everywhere:

| Key | Action |
|---|---|
| Up / Down | Choose a stat |
| Left / Right | Change it (hold Shift for bigger steps) |
| PgUp / PgDn | Previous / next weapon |
| Del | Reset the stat to the game's value |

Every change is saved to

```
%LOCALAPPDATA%\CowboyBingus\Helldivers2\StatEditor\config.txt
```

and applied again on every start, a few seconds after launch (on the title screen). The hotkey
can be changed in that file (for example `hotkey F7`). Delete a line, or the whole file, to go
back to the game's values.

## Good to know

- **Shared values.** Some weapons fire the same projectile or share its damage values (for
  example the Liberator, Liberator Carbine, StA-52 and Stalwart). The panel names the weapons
  that change along with the one you edit.
- **Variants.** Some weapons exist more than once in the game's data (a mounted copy, a sentry
  version, an underbarrel attachment). The list labels each one, and the panel says which copy
  you are editing.
- **Arc, flame and melee weapons** have no damage rows yet; their handling and ammo can be
  changed.
- **Barrages** can use different shells for different rounds; the section names say which rounds
  a value belongs to. Long lists scroll: Up/Down follow the chosen stat, or use the buttons under
  the list.
- **Magazine attachments** (for example on the MP-98 Knight or SG-225 Breaker) set magazine
  counts themselves when one is fitted.
- The **armory** still shows the game's own numbers; the changes apply in play.
- **In multiplayer** your changes exist only in your game.
- **Other mods** that change the same stats will fight over them; use one or the other.
- **Nothing on disk is modified.** The mod changes the game's settings in memory while it runs.

## Reporting problems

Open an [issue](../../issues) and attach the log:

```
%LOCALAPPDATA%\CowboyBingus\Helldivers2\Logs\SHODANStatEditor.log
```

The log lists the tables the mod found, every stratagem it listed, and anything it could not
match, which is usually enough to find the cause.

## Credits

- **Bingus Shared Loader** by CowboyBingus, which runs the mod.
- **HD2Runtime** by Skyeshade, whose weapon and stratagem catalogs name the weapons and map
  every strike to its projectiles, blasts and damage.
- **[Filediver](https://github.com/xypwn/filediver)** and the **[helldivers.io](https://helldivers.io/)**
  data dump by shalzuth, for the game's data layouts.
- **DiverKit** and **HD2 HUD Plus**, which showed where the game's UI font lives.

## License

Public domain ([The Unlicense](LICENSE)). Use, change, share or sell it however you like; no
credit needed.

SHODAN Stat Editor is not affiliated with or endorsed by Arrowhead Game Studios or Sony
Interactive Entertainment.
