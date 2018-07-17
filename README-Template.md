# Adaptive Optics


## Direct Wavefront Sensing

Using a direct wavefront sensor (e.g. Shack-Hoffman sensor or lens-array + CCD camera) to detect the wavefront, whose gradients in each segments are indicated as the spot shift on the image. Using a spatial light modulator (e.g. deformable mirror) to compensate the wavefront distortion.

### Two-photon point-scanning system

For 2p raster-scanning imaging, we 

× detect the fluorescence abberation on the SH-imaging path;

× correct the 2p laser illumination by setting a negative value on the deformable mirror;

× collect intensity pixel-by-pixel using PMT.

```
Note1: We DO NOT need to compensate the aberation between samplet to the PMT, because the PMT records spatially unresolved total intensity. 
```
```
Note2: Descaned scheme avoids the spot shift on the SH sensor when the illumination is scanning.
```

### Wide-field imaging system

For SIM, 

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo


## Indirect Wavefront Sensing

Estimate the wavefront distortion based on some metrics (e.g. intensity, spot shift) and correct using spatial light modulator. Do not need guide-star as in direct wavefront sensing. 




