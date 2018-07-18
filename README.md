# Adaptive Optics


## Direct Wavefront Sensing

Using a direct wavefront sensor (e.g. Shack-Hoffman sensor or lens-array + CCD camera) to detect the wavefront, whose gradients in each segments are indicated as the spot shift on the image. Using a spatial light modulator (e.g. deformable mirror) to compensate the wavefront distortion.


### Two-photon point-scanning system

* For 2p raster-scanning imaging, AO aims to retrieve a tighted focused focal spot (diffraction-limited) to achieve both signal intensity and spatial resolution. We **do NOT** need to compensate the aberation between the sample and the PMT, because the PMT records spatially unresolved total intensity. In implementation, we: 

       1. detect the fluorescence abberation on the SH-imaging path;

       2. correct the 2p laser illumination by setting a negative value on the deformable mirror;

       3. collect intensity pixel-by-pixel using PMT.

  See figure e for a schematic demonstration.

     ![figure e](https://github.com/Jessie-ucb/Adaptive-Optics/blob/master/nmeth.4218-F3.jpg)


* Depending on whether or not the fluorescence goes back along the same galvos with the illumination light to the SH camera, we devide the optical system into **descanned** and **non-descanned** architectures. Descanned scheme avoids spot shifting on the SH sensor when the illumination is scanning (averaging effect, see Eric's paper).

* For 2p imaging, the deformable mirror is used to correct the aberration on the illumination path. As for the fluorescence detection path, we can either apply the same correction or not, leading to two different designs:

     - **Open-loop Design**: Only the 2p illumination light passes through the DM. Can only do AO correction once.

     - **Close-loop Design**: The DM controls both the illumination and the SH-imaging path. Can conduct iterative corrections.



### Wide-field imaging system

* For wide-field AO, we still use 2p illumination to generate fluorescence and detect the wavefront aberration using SH sensor. The difference from 2p scanning imaging is that the sample-induced abberation **CAN NOT** be neglected, however, the illumination aberration in SIM system (mainly represented as the shift of fringes's phases and frequencies) can be compensated in the process of SIM reconstruction. Therefore, we correct the aberration in the SIM fluorecence imaging path using a deformable mirror. To conclude, we: 

       1. using the 2p laser illumination, detect the fluorescence aberration on the SH-imaging path;

       2. correct the wide-field fluorecence aberration by setting a negative value on the DM.

   Note: the fluorecence aberration of SIM and SH-imaging are considered equal (assumption: they share as much light path as possible).

* Open-loop or close-loop and descan or non-descan are specified according to the 2p illumination and SH detection design.


## Indirect Wavefront Sensing

Estimate the wavefront distortion based on some metrics (e.g. intensity, spot shift) and correct using spatial light modulator. Do not need guide-star as in direct wavefront sensing. Applicable for more scattering sample or higher depth.


