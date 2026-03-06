# SourceMod Gap Plugin

A SourceMod plugin primarily for CS:S (might work for CS:GO, not tested, idk) that measures the distance between two world points and calculates the minimum velocity required to cross the gap.

Based on [gap by Nairdaa](https://github.com/Nairdaa/gap).

## Features

- Place two points (A and B) via aim/raytrace to measure distances
- Displays per-axis distances (X, Y, Z) and combined distances (XY, XZ, YZ, XYZ)
- Calculates minimum horizontal velocity needed to cross the gap
- Shows minimum velocity with a one-tick head start (+1t)
- Snap-to-grid support (off, 1, 2, 4, 8, 16, 32, 64 units)
- Visual crosshair cursor at your aim position
- Beam line drawn between point A and B with ring markers

## Usage

```
sm_gap
```

Opens the gap menu. From the menu:

1. **Select point A** - raytraces your crosshair to place the first point
2. **Select point B** - raytraces your crosshair to place the second point and calculate results
3. **Clear points** - resets both points
4. **Decrease/Increase grid** - cycles snap-to-grid value
5. **Show cursor: on/off** - toggles the 3D crosshair at your aim position

Once both points are placed, the menu displays:
- Coordinates of A and B
- X, Y, Z axis distances
- XY, XZ, YZ plane distances
- XYZ 3D distance
- **MinVel** - minimum speed needed at jump start to reach point B
- **+1t** - minimum speed needed if starting one tick before the jump
- **Impossible** if the vertical drop exceeds 65 units

## Credits

- **Nairdaa** - original plugin ([github.com/Nairdaa/gap](https://github.com/Nairdaa/gap))
- **ici** - base implementation
- **Saul** - velocity calculation formula
- **Charles_(hypnos)** - velocity calculation implementation
