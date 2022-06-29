# qb-apartments
Apartments System for QB-Core Framework :office:

# License

    QBCore Framework
    Copyright (C) 2021 Joshua Eger

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>


## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-clothing](https://github.com/qbcore-framework/qb-clothing) - To save outfits
- [qb-houses](https://github.com/qbcore-framework/qb-houses) - House logic
- [qb-interior](https://github.com/qbcore-framework/qb-interior) - Interior logic
- [qb-weathersync](https://github.com/qbcore-framework/qb-weathersync) - To desync weather while inside
- [qb-spawn](https://github.com/qbcore-framework/qb-spawn) - To spawn the player at apartment if last location was in apartment

## Screenshots
outdated

## Features
- Door Bell
- Stash
- Log Out Marker
- Saved Outfits

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-apartments.sql` in your database
- Add the following code to your server.cfg/resouces.cfg
```
ensure qb-core
ensure qb-interior
ensure qb-weathersync
ensure qb-clothing
ensure qb-houses
ensure qb-spawn
ensure qb-apartments
```

## Configuration
```
Apartments = {}
Apartments.Starting = true
Apartments.SpawnOffset = 30

-- **** IMPORTANT ****
-- UseTarget should only be set to true when using qb-target
Apartments.UseTarget = true



Apartments.Locations = { --can add multiple
    ["apartment1"] = {
        name = "apartment1",
        label = "Hotell",
        coords = {
            enter = vector4(-1222.27, -173.4, 39.33, 334.73),
        },
        polyzoneBoxData = {
            minZ = 38.5,
            maxZ = 42.0,
            debug = false,
            length = 3,
            width = 1,
            distance = 2.0,
            created = false
        }
    },
}

```
