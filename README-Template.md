# Adaptive Optics

One Paragraph of project description goes here

## Direct Wavefront Sensing

Using a direct wavefront sensor (e.g. Shack-Hoffman sensor or lens-array + CCD camera) to detect the wavefront, whose gradients in each segments are indicated as the spot shift on the image. Using a spatial light modulator (e.g. deformable mirror) to compensate the wavefront distortion.

### Two-photon point-scanning system

For 2p raster-scanning imaging, we 

1) detect the fluorescence abberation on the SH-imaging path;

2) correct the 2p laser illumination by setting a negative value on the deformable mirror;

3) collect intensity pixel-by-pixel using PMT.

Note: We DO NOT need to compensate the aberation between samplet to the PMT, because the PMT records spatially unresolved total intensity. 


```
Give examples
```

### Wide-field imaging system

For

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



### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

