# Adaptive Optics


## Direct Wavefront Sensing

Using a direct wavefront sensor (e.g. Shack-Hoffman sensor or lens-array + CCD camera) to detect the wavefront, whose gradients in each segments are indicated as the spot shift on the image. Using a spatial light modulator (e.g. deformable mirror) to compensate the wavefront distortion.


### Two-photon point-scanning system

For 2p raster-scanning imaging, we: 

1) detect the fluorescence abberation on the SH-imaging path;

2) correct the 2p laser illumination by setting a negative value on the deformable mirror;

3) collect intensity pixel-by-pixel using PMT.

```
Note1: We DO NOT need to compensate the aberation between samplet to the PMT, 
       because the PMT records spatially unresolved total intensity. 
```
```
Note2: Descanned scheme avoids spot shifting on the SH sensor when the illumination is scanning.
```

* Open-loop Design

Only the 2p illumination light passes through the DM. Can only do AO correction once.

* Close-loop Design

The DM controls both the illumination and the SH-imaging path. Can conduct iterative corrections.



### Wide-field imaging system

For SIM, the main difference from 2p scanning imaging is that the sample-induced abberation CAN NOT be neglected, however, the illumination aberration (mainly represented as the shift of fringes's phases and frequencies) can be compensated in the process of SIM reconstruction. Therefore, we: 

1) using the 2p laser illumination, detect the fluorescence abberation on the SH-imaging path;

2) correct the wide-field fluorecence aberration by setting a negative value on the deformable mirror.

 ```
 Note: the fluorecence aberration of SIM and SH-imaging are considered equal (assumption: they share as much light path as possible).
 ```



## Indirect Wavefront Sensing

Estimate the wavefront distortion based on some metrics (e.g. intensity, spot shift) and correct using spatial light modulator. Do not need guide-star as in direct wavefront sensing. 




