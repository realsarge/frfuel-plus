# FRFuel+
:fuelpump: A long-awaited successor to [@thers](https://github.com/thers/FRFuel) FRFuel.

![FRFuel+](https://i.imgur.com/QUdmaW5.png)

## Features

+ Support for helicopters
+ Realistic fuel consumption for helicopters and quads
+ Customizable helicopter pads (refuel stations)
+ An ability to refuel any supported vehicle type with a fuel truck

## Roadmap

- [ ] Support for planes
- [ ] Support for boats
- [ ] Sound effects for planes & helicopters (low fuel alert etc.)
- [ ] Disallow refueling for helicopters at conventional fuel pumps and vice versa

## Installation
1. Download latest release of [FRFuel+](https://github.com/h0kkaido/frfuel-plus/releases/latest)
2. Drag & Drop contents of `frfuelplus.zip` to your resources folder
3. Add frfuelplus to your server.cfg: `start frfuelplus`

## Configuration
> config.ini
+ CreatePickups (true/false) - creates/hides a gas canister at your pumps;
+ CreateBlips (true/false) - creates/hides a gas station/pad blip on global map and minimap;
+ ShowHud (true/false) - shows/hides a fuel bar above minimap;
+ ShowHudWhenEngineOff (true/false) - shows/hides a fuel bar when engine is disabled;
+ EngineToggleKey ([controls](https://docs.fivem.net/game-references/controls/)) - configurable button to turn engine on/off;
+ FuelConsumptionRate (float) - rate of fuel consumption (applied to every vehicle except helicopters and quads);
+ RefuelRate (float) - rate of refuel at gas pump;
+ FuelBarNormalColor, FuelBarWarningColor (color hex) - colors of fuel bar (ShowHud).

> GasStations.json

Both gas stations/pads have three main variables:
1. Coordinates (float X,Y,Z) - coordinates at which your gas station/pad blip would be located;
2. Type (VEHICLE/HELIPAD) - responisble for placing a conventional/helipad station blip on your map;
3. Pumps (float X,Y,Z array) - coordinates of pumps, where refueling would be available.

## Feature: Fire Truck
To use a fuel truck, you must have a refuel vehicle named `fueltruck`.
>> Note: This can be changed in lines 391 & 396 at FRFuel.cs.*

Pull up to a vehicle/aircraft and player in control of it will see a notification, which states that refuel is available.
![Fuel Truck](https://i.imgur.com/2AnWgrO.png)
If you want to use Freightliner FL-60-70 displayed in image above, you can download it at [LSPDFR](https://www.lcpdfr.com/files/file/21804-freightliner-fl-60-70-fire-mini-pack-non-els-templated/) and RON livery for it in [Releases]().

---
*Coded with love by @h0kkaido.*
