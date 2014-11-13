# diversify

Script for quickly creating varying sizes of app icons for iOS project asset catalogs. 

## Example

Say you have a large `512px` or `1024px` version of your app icon called `Icon.png`. For a standard asset catalog, you need these sizes: 

![](./example.png)

Boy, that's a pain. 

```bash
$ diversify Icon.png

Creating 1x icons...
./Icon-29.png PNG 29x29 29x29+0+0 8-bit sRGB 91c 781B 0.000u 0:00.000
./Icon-40.png PNG 40x40 40x40+0+0 8-bit sRGB 110c 951B 0.000u 0:00.000
./Icon-50.png PNG 50x50 50x50+0+0 8-bit sRGB 124c 1.08KB 0.000u 0:00.000
./Icon-57.png PNG 57x57 57x57+0+0 8-bit sRGB 117c 1.06KB 0.000u 0:00.000
./Icon-72.png PNG 72x72 72x72+0+0 8-bit sRGB 124c 1.18KB 0.000u 0:00.000
./Icon-76.png PNG 76x76 76x76+0+0 8-bit sRGB 122c 1.2KB 0.000u 0:00.000
./Icon-120.png PNG 120x120 120x120+0+0 8-bit sRGB 137c 1.49KB 0.000u 0:00.000

Creating 2x icons...
./Icon-29@2x.png PNG 58x58 58x58+0+0 8-bit sRGB 117c 1.1KB 0.000u 0:00.000
./Icon-40@2x.png PNG 80x80 80x80+0+0 8-bit sRGB 130c 1.28KB 0.000u 0:00.000
./Icon-50@2x.png PNG 100x100 100x100+0+0 8-bit sRGB 135c 1.36KB 0.000u 0:00.000
./Icon-57@2x.png PNG 114x114 114x114+0+0 8-bit sRGB 133c 1.4KB 0.000u 0:00.000
./Icon-60@2x.png PNG 120x120 120x120+0+0 8-bit sRGB 137c 1.49KB 0.000u 0:00.000
./Icon-72@2x.png PNG 144x144 144x144+0+0 8-bit sRGB 139c 1.61KB 0.000u 0:00.000
./Icon-76@2x.png PNG 152x152 152x152+0+0 8-bit sRGB 140c 1.66KB 0.000u 0:00.000

Creating 3x icons...
./Icon-29@3x.png PNG 87x87 87x87+0+0 8-bit sRGB 118c 1.23KB 0.000u 0:00.000
./Icon-40@3x.png PNG 120x120 120x120+0+0 8-bit sRGB 137c 1.49KB 0.000u 0:00.000
./Icon-60@3x.png PNG 180x180 180x180+0+0 8-bit sRGB 142c 1.79KB 0.000u 0:00.000
```

Just edit the top of the script if you need to modify the sizes created. 

```bash
sizes1x="29 40 50 57 72 76 120"
sizes2x="29 40 50 57 60 72 76"
sizes3x="29 40 60"
```

And yes, a shipping app should probably take more care than this and hand-create each size of icon. This is mostly for dev apps and distribution. 
