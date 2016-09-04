---
layout: post
title: "Summer 2016 Sensor Standards Committee Meeting"
modified:
categories: blog
excerpt: "Hyperspectral calibration"
tags: [reference data, field scanner, standards]
image:
  feature:
date: 2016-09-02T20:43:38-05:00
---


* Table of Contents                                                                                 
{:toc}

## Participants (add your name below)

* David LeBauer, UIUC
* Solmaz Hajmohammadi, LemnaTec
* Nadia Shakoor, DDPSC
* Jeff White, USDA
* Max Burnette, UIUC
* Larry Biehl, Purdue
* Craig Willis, UIUC
* Alex Thomasson, TAMU
* Javi Ribera, Purdue student
* Charlie Zender, UCI
* Justin McGrath, UIUC
* Andries van der Meer
* Dave Guarrera, ARPA-e
* Andy French, USDA
* Yuhao Chen, Purdue
* Justin Manzo, ARPA-e
* Ben Niehaus, LemnaTec
* Paul Bartlett, Near Earth Autonomy



## Summary:

1. Reviewed Lemnatec protocol for calibrating Hyperspectral sensors
2. Discussed how to handle shade
2. C. Zender will add corrections for sun angle
  3. Near noon, plants will be shaded by sensor box.
  4. Sensor box is reflective. We could paint underside flat black 
3. Sensor box has lights,
  * physically, using lights at night is easiest to calibrate
  * biologically could affect plants (especially photoperiod sensitive); need to do illumination study
1. Cross-team comparisons
  * could have a common calibration object
  * could bring sensors to a common site 

### Action Items

* C Zender to add solar zenith angle
* Alex Thomasson is going to provide NEON protocols, information on test objects
* Stuart / UA / TERRA team
  * will use illumination at end of current season
  * will design / implement illumination expt to study impact of illumination on a few plants at the end of next season
* Justin Manzo / ARPA-E will work to coordinate cross site calibration 

## ˚

1. Review Lemnatec [draft protocol for hyperspectral sensor calibration](https://docs.google.com/document/d/1w_zHHlrPVKsy1mnW9wrVzAU2edVqZH8i1IZa5BZxVpo/edit#). This will be a focus of discussion so please review this document in advance of the meeting. This document and supplementary information (sensor specs, factory calibration, calibration object) are in a [shared folder](https://drive.google.com/open?id=0By_PDCcY5g2JRWNnZ3E4akRHQTA) on Google Drive. 
2. Evaluate Sample (uncalibrated) hyperspectral data product [https://terraref.ncsa.illinois.edu/clowder/spaces/57aa3f60e4b0f7d0a1924a44](https://terraref.ncsa.illinois.edu/clowder/spaces/57aa3f60e4b0f7d0a1924a44)
3. Peruse References (below)


## Proposed Hyperspectral Calibration Protocol

Below it is outline how to measure the reflectance for the hyperspectral sensor. The system does not give back any radiance values, typically in watt / mÂ² or a similar value. However the Oceanopitcs (upward facing VNIR spectrometer) sensor does give radiance values.

In any case for the analysis the reflectance values will be more important. 

Repeat factory calibration using the calibration lamp provided by Headwall. This would need to repeated once a year, or every time the system is modified. 

### During daily operations:

1. Measurement of Hyperspectral Spectralon Reference Target. (**R**)

 * Height of the Target at Canopy level. 
 * Horizontally leveled

 * Distance set to normal height ( I believe it is around 1.8m, Stuart to confirm)
 * need to adjust to the factory calibration for spectralon panel âŠ 
2. Take Dark Current Image of the SWIR sensor.  (**D**)

 * Headwall SWIR sensors are able to compensate the dark current. Usually the LemnaTec software internally sends a command to the Headwall SWIR camera software to compensate for the dark current before the start of each recording. 

3. Image the sample that need to be analyzed. In this case it would be the plant. (**S**)
4. To be considered:
  * Between the image acquisition of the target and the sample the illumination should ideally not change at all.
  * This is of course highly difficult in outside environments. Thus it would be recommended to scan it every 15- 20 min
  * The dark current image need to be repeated every time the temperature of the sensor changes. Ideally before each scan per row. It takes about 30-60s 

### Discussion

* Larry: spectralon provides known reflectance; may not be brightest in view
* Ben: reflectance can be > target,e.g. If leaves are wet
  *  At night, active illumination can be more certain that plants will not reflect > 95%; active reflectance allows to use greater dynamic range of the calendar. See presentation [https://docs.google.com/presentation/d/10Yl915Af5ZpgQ3G9sUJ97-Zpo-ESJRQ8BP0TVN04plA/edit?usp=sharing](https://docs.google.com/presentation/d/10Yl915Af5ZpgQ3G9sUJ97-Zpo-ESJRQ8BP0TVN04plA/edit?usp=sharing)

### Correction Method:

![image alt text](image_0.png)

Where is the respective wavelength S the Sample data, D the dark current data (in this case Headwall software already corrects for the dark current data) R the Reference data and *RC*Î»,Îž the correction value of the spectralon target provided with the target. 

It might be worth to consider a normalization of the overall values. These normalization could take place either per plot, per field, per experiment etc. 

Eg. 

![image alt text](image_1.png)

Normalizing the reflectance data for each band of each pixel to the sum of all bands of the same pixel. 

Other Normalisation methods can be thought of as well. Eg. normalizing to the largest intensity in each image, which is a feature offered by Headwall as a built in routine. This however might not be appropriate and could change the results significantly.

#### Discussion

* Larry: Spectralon calibration should take into account zenith angle; varies with wavelength âŠ *RC*Î»,Îž illumination angle. Larry uses polynomial function of angle.
* Andy French: suggests grey panel
* Alex Thomasson (agrees) uses 6, 20, 40%, mostly don't see above 100%
* Melba: easy to correct angle
* Dave H (NSF NEON): error sources (in order) factory calibration, flying near noon, atmospheric correction (atm correction relevant at km scale of airborne platform)
* Jeff White: real issue is shading at solar noon âŠ 
* CZ: are we trying to estimate downward looking reflectance (at nadir)?
* DH: need to calibrate ground reflectance, to compare across sites, times, illumination.
* LB: report âthis measurement given illumination angle of x, view angle of y, (y always ~= perpendicular to ground) 
* JW: y changes scanning left to right, view angle 
* CZ: how to use downwelling radiometer / spectrometer
 1. Limited wavelengths (up to 900nm) so may only apply to VNIR; SWRI no overlap
 2. Partially shaded âŠ 
* BN: looking into second spectrometer to extend range to 2500nm like SWIR, currently on the wish list
* LB: what is field of view of Ocean optics spectrometer? 
 * BN: 15 degrees, looking straight up, fiber optic. 
 * LB: only looking at one spot in sky? Yes
   * Is it looking through frosted glass etc?
   * What is purpose?
* MC: keep downwelling radiances separate in the data products
 * Headwall does have a system (?votis?sp) through 1000nm integrated w/ cameras, may be better integrated

## Open points to be discussed: 

Given that the field of view is partially shaded, how do we compute reflectances. We have a few options: use either only shaded or unshaded area, use artificial illumination, 

* BN: artificial illumination at night is ideal from engineering (as opposed to plant) perspective. As long as plants are happy, this would be âgold standardâ. Line illumination is in development. 
* Justin M: light has impacts on many time scales (from s-h). Some traits wonât change (photosynthetic capacity, vcmax, etc) on this time scale; photosynthetic rate will change
* BN: how does it affect plants?
* JW: could limit measurements to end of season; 
* JM: should mainly impact phenology but could affect architecture or physiological processes.
* JW: sorghum is photoperiod sensitive. The bioenergy sorghums are short-day plants. In mid-summer with long days, short night interruptions thus should be less of a concern. More problems would be expected as daylengths shorten in September to October.

## 1. Shaded area vs. non shaded area: 

* Should only the shaded or unshaded area be used? 
* Should a pixel wise correction happen to correct for the differences in the shaded and non shaded area? 

* Scan the target before and after each scan and assume a linear regression between the two scans, adapt the correction method accordingly with a time function
* Have a scanning day where the reflectance target is constantly scanned throughout the day to develop an interpolation method between two scans. These days would need to be repeated throughout the year as the angle of the sun is changing. 
* How would we handle passing clouds?

#### Discussion

* CZ: R_lambda does this have a per-pixel component across scan line? Will we have a pixel-by-pixel calibration? Has bearing on how / if we can handle shade.
* BN: yes, will have per pixel. If illumination is constant, would use average. For sunlight, would scan entire target (1.5m) and average over length for per-pixel calibration.
* CZ: Will S and R have same dimensions?
  * BN: Yes.
  * CZ: so no pixel mapping required. Excellent!
* AT: there is spectral change with shade, there are known relationships that could be used. Is significant, measurable, prob. has been measured
* BN: depends on where shade is coming from, but will be object specific.
* LB: illumination in shade is very dependent on composition and distance of object. Has found shading object also increases illumination (sun â leaf â object â leaf), especially in infrared (not detectable by eye) âŠ he tries to paint everything ultra-flat black, especially anything shiny (aluminum, etc).
* CZ: is dark light going to be an average over all pixels, or pixel by pixel? 
* LB: measure it to prove it doesnât make a difference
* AF: and measure periodically to verify camera dark response hasnt changed

## 2. Using artificial illumination.

* Upside would be that the Illumination does not change over time thus once calibrated can be used for the whole scan. 
* Downside: disturbs the plant

LemnaTec is currently in development of a new light source suitable for Field applications which illuminates only one small area. This illumination is planned to have 50 mW/cm2 (500 W/m2)

Similar to the lab version in image to the left: 

This would reduce the impact on the plant as the would only receive the illumination for a short period of time. 

This could be part of the system extension. 

From a pure measurement point of view the new illumination would be the ideal situation. 

3. Empirical correlation between the *R*Î» and the Oceanoptics sensors. 

Still open shaded vs. non shaded Thus two correlation would need to be developed. 

Add additional oceanoptics sensors covering 1000-2500 nm to correct values for the SWIR as well if method is working well for VNIR in overlapping regions

#### Discussion:

Cross-site calibration. One option: share targets. Another option: send all sensors to one location.

* LB: share targets
* Alex: NEON started w/ concrete, uses rubber material. Ceramic tiles standard in cotton fiber industry. 
* JW: has tested a few different tiles, not as good as published. Buy large batch, store carefully, cross-check within batch. 
* AT: will send data w/ specifications
* Justin Manzo: same targets across sites vs. all sensor measure the same target at one site.

# Supplementary Information:

## GitHub Discussions:

* [Convert exposure to reflectance](https://github.com/terraref/computing-pipeline/issues/88)
* [Calibrating downwelling spectral radiances](https://github.com/terraref/reference-data/issues/30)
* [Georeferencing hyperspectral data](https://github.com/terraref/computing-pipeline/issues/144)
* [Access via THREDDS server?](https://github.com/terraref/computing-pipeline/issues/155)

## Software

* Hyperspectral Pipeline scripts: [scripts/hyperspectral/](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/)
* Description in [README.md](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/README.md)


### References:

## GitHub Discussions:

* [Convert exposure to reflectance](https://github.com/terraref/computing-pipeline/issues/88)
* [Calibrating downwelling spectral radiances](https://github.com/terraref/reference-data/issues/30)
* [Georeferencing hyperspectral data](https://github.com/terraref/computing-pipeline/issues/144)
* [Access via THREDDS server?](https://github.com/terraref/computing-pipeline/issues/155)

## Software 

* Hyperspectral Pipeline scripts: [scripts/hyperspectral/](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/)
* Description in [README.md](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/README.md)

## Publications

* Robinson, B. F., and L. L. Biehl. "Calibration procedures for measurement of reflectance factor in remote sensing field research." 23rd Annual Technical Symposium. International Society for Optics and Photonics, 1979. [(pdf)](https://drive.google.com/open?id=0By_PDCcY5g2JODNCNWhlaU1mNHc)
* Jackson, Ray D., Thomas R. Clarke, and M. Susan Moran. "Bidirectional calibration results for 11 Spectralon and 16 BaSO 4 reference reflectance panels." Remote Sensing of Environment 40.3 (1992): 231-239. ([pdf](https://drive.google.com/open?id=0By_PDCcY5g2Jb1doQ3RDTDJfUVU))
* Knighton, N., Bugbee, B., 2004. A mixture of barium sulfate and white paint is a low-cost substitute reflectance standard for Spectralon. ftp://128.138.70.84/pub/fromDominik/snow_probe/snow%20probe%202014-01-09/Barium_Sulfate_paint.pdf
* Sanches, I., Tuohy, M., Hedley, M., Bretherton, M., 2009. Large, durable and low-cost reflectance standard for field remote sensing applications. International Journal of Remote Sensing 30, 2309-2319.
* Singh, A., Serbin, S. P., McNeil, B. E., Kingdon, C. C. and Townsend, P. A. (2015), Imaging spectroscopy algorithms for mapping canopy foliar chemical and morphological traits and their uncertainties. Ecological Applications. doi:10.1890/14-2098.1 ([pdf](https://drive.google.com/open?id=0By_PDCcY5g2JNmctOEFqWVJONTg))


