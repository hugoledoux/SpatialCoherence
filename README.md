# SpatialCoherence
Calculates the spatial coherence of an input LAS file.
Outputs a GeoTIFF with values representing time between first and last point entry in cell.
Based on [AHN3](https://downloads.pdok.nl/ahn3-downloadpage/) logic.


 ![image](https://user-images.githubusercontent.com/4410453/129718884-4ecaf6cb-315c-4eee-a86d-36badcc3faba.png)
 
 # Compilation
 
 1. Download and unzip somewhere the [LAStools](https://lastools.github.io/) ([direct link to .zip](https://lastools.github.io/download/LAStools.zip))
 2. modify `CMakeLists.txt` line6 and line8 to link to the LAStools you have
 3. install the [GDAL library](https://gdal.org/)
 4. `cmake . && make`
 5. voilà

# To run

```
./SpatialCoherence my.files out.tiff 100
```

- `my.files` is just a text file with a list (one per line) of input LAS/LAZ files
- `out.tiff` is the output GeoTIFF
- 100 is the number of pixels in x or y
