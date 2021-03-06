Title: Observing technical details
Save_as: observing-technical.html

[TOC]

The TESS mission provides the community with an opportunity to make ground-breaking discoveries in the field of exoplanets, astrophysics and planetary science. A summary of observing technical details that proposers should be aware of can be found here.


A description of the overall mission can be found in
[Ricker et al. 2015](http://adsabs.harvard.edu/abs/2015JATIS...1a4003R). Brief descriptions of the mission operations, including the TESS orbit, field-of-view, time-sampling, and observing strategy, can be found in the [Operations](operations.html) page. Details on all aspects of the mission, developed for GI proposers, are in the [TESS Observatory Guide](docs/TESS_observatory_guide_v1.1.pdf).

This website as well as the [TESS Instrument Handbook and Data Release Notes](documentation.html) should be consulted for the latest information regarding observing with TESS. 


<!-- ## Overview
The TESS spacecraft hosts four 10-cm aperture cameras in an
eccentric high-earth orbit in a 2-to-1 resonance with the Moon. This insures a thermally stable environment, provides the ability to remain on a single pointing for the
duration of each Sector, and allows for high data rates during perigee. 
Pointing is maintained by a combination of two reaction wheels and thrusters, 
reacting to motion data provided by fine guidance sensors 
(fine-point observing) or star trackers (coarse-point observing). 

With only two remaining reaction wheels, 
these operations are only possible while pointing within 
the orbital plane of the spacecraft, which approximates to the ecliptic. 
Only this specific family of pointings yields operational configurations 
where solar pressure is largely mitigated by spacecraft geometry, 
thereby making viable precision pointing and photometry 
approaching the quality achieved for the Kepler mission. -->



<!-- ### Capabilities
Science observations are taken at one of two timing settings: long (30-min) or short (1-min) cadence. When in fine-point observing, [K2 is capable of achieving a benchmark photometric precision](k2-observing.html#fine-point-photometric-precision) on an m<sub>V</sub> = 12 G2V star of better than 170 parts-per-million (ppm) in 30 minutes of integration, i.e., one long cadence exposure. 
This corresponds to ~30 ppm over a 6.5-hour transit 
of an Earth-sized body around that star.

While stars brighter than m<sub>V</sub> = 11.5 will saturate some pixels, 
K2 performs well on stars as bright as m<sub>V</sub> = 4, 
provided the scientific benefit justifies the large number of pixels 
needed to capture saturated flux bleeding along CCD columns. 
Kepler also has many faint-target scientific applications 
where m<sub>V</sub> = 20 objects yield a photometric precision 
of 10% over 30 minutes.

The broad photometric bandpass has a half-maximum transmission range 
of 430 to 840 nm. 
The instrument has neither changeable filters, 
dispersing elements, nor a shutter. 
The detector has a pixel scale of 3.98 arcseconds. 
Image quality varies with position in the focal plane, 
with the 95% encircled energy diameter ranging from 3.1 to 7.5 pixels with a median value of 4.2 pixels. 
The percentage of point-source flux concentrated in the center pixel 
is between 20% and 62% with a median value of 45%. -->


## Photometric performance


### Typical noise levels

The figure below shows the 1-hour Combined Differential Photometric Precision (CDPP) from TESS Sector 1. The red points are the RMS CDPP measurements for the 15,889 light curves from Sector 1 plotted as a function of TESS magnitude. The blue x's are the uncertainties, scaled to a 1-hour timescale. The purple curve is a moving 10th percentile of the RMS CDPP measurements, and the gold curve is a moving median of the 1-hour uncertainties. The photometric uncertainties are dominated by pointing jitter, but the best light curves are well below the mission requirements of (1) a systematic error floor at 60 ppm and (2) an achieved CDPP at 10th magnitude of 230 ppm, which is sufficient to detect super-Earths around bright stars. For fainter stars around Tmag = 16, the photometric precision drops to about 1%, which is still sufficient for many astrophysical studies such as supernovae and stellar variability.

The typical noise achieved in each individual TESS sector is described in the [Data Release Notes](https://archive.stsci.edu/tess/tess_drn.html) for each sector.


<br/>
<img class="img-responsive" style="max-width:67%;" src="images/giprogram/cdpp_sector1.png">
<br/>



<!-- A noise model for TESS photometry (figure below) shows the expected standard deviation of measurements of relative flux, as a function of apparent magnitude, based on 1 hr of data (Sullivan et al. 2015). For the brightest stars, the precision is limited by the systematic noise floor of 60 ppm. For the faintest stars, the precision is limited by noise from the zodiacal light (shown here for an ecliptic latitude of 30 deg). Over the range of apparent magnitudes 8-13, the photon-counting noise from the star is the dominant source of uncertainty.

<br/>
<img class="img-responsive" style="max-width:67%;" src="images/giprogram/tess_photometric_performance.png">
<br/>


The photometric precision for a 10th magnitude star is estimated to be about 200 ppm, so TESS will be sensitive to super-Earths around bright stars.

<br/>
<img class="img-responsive" style="max-width:67%;" src="images/giprogram/tess_noise_200ppm.png">
<br/>
*Image Credit: Zach Berta-Thompson with data from Sullivan at al. (2015)*

For fainter stars, such as a 16th magnitude star, the photometric precision drops to about 1%, which is sufficient for many astrophysical studies such as supernovae and stellar variability.

<br/>
<img class="img-responsive" style="max-width:67%;" src="images/giprogram/tess_noise_1percent.png">
<br/>
*Image Credit: Zach Berta-Thompson with data from Sullivan at al. (2015)* -->

### Saturation
The [TESS Instrument Handbook and Data Release Notes](documentation.html) should be consulted for the latest information regarding observing saturated stars with TESS. 

The amount of charge deposited by a star of magnitude m into the peak pixel depends on
the fraction of the total charge in the peak pixel: this value generally ranges from 0.2 to
0.4 in the TESS images. The TESS cameras create 15,000 e−/s for a star of m = 10: thus,
a star of m = 5 will create 3 × 106
electrons in a two-second exposure. For a flux fraction
of 0.3, the charge in the peak pixel is 9 × 105
e−, leading to a bloom length of 5 rows;
similarly, a star of m = 2.5 will create a bloom of 50 rows.
A key feature of the CCID-80 CCDs used on TESS is their ability to conserve charge even
from very saturated stars. Pre-launch ground tests showed that charge will be conserved
for stars at least as bright as 4th magnitude. Measurements of charge conservation using
flight data are in progress.

<! -- Saturation is anticipated in the central pixel at I_C = 7.5. This, however, does not represent the bright limit for precise photometry. Excess charge from saturated pixels is conserved and spread across adjacent pixels in a CCD column until the excess reaches a CCD boundary. This leads to "bleed trails" extending above and below a saturated pixel, similar to what is seen for bright stars in Kepler/K2 photometry. Precision photometry can still be achieved by creating a photometric aperture that is large enough to encompass all excess charge. The TESS bright limit is anticipated to be I_C=4. -->

<!-- ### Solar pressure-induced drift




### Fine-point pointing precision


### Point-spread function
 -->


### Crowding
Because the TESS pixels are large (21 arcsec), the TESS photometry for many targets will be contaminated by nearby objects. One of the goals of the TIC is to provide the information needed to estimate the contamination in the TESS band. This cannot be determined accurately ahead of time because it will depend on the pixels selected for the aperture photometry of each target and the exact position of the target in the aperture. However, it is possible for the TIC to provide some guidance concerning the level of expected contamination, for example by providing the number of known objects and their total brightness in the TESS band for some suitable standard aperture and photometer Pixel Response Function (PRF). 


## Sky coverage

The fraction of sky coverage for different time baselines that TESS will have over the 2-year prime mission is listed below. Note this does not yet take into account the shift in pointing in Sectors 14, 15, and 16 that are described below. 

<br/>
<img class="img-responsive" style="max-width:67%;" src="images/giprogram/tess_sky_coverage.png">
<br/>

### Pointing shifts

TESS is observing the northern ecliptic hemisphere during the second year of its primary mission. The cameras are oriented along a line of ecliptic longitude (as they were in Year 1), with that longitude determined by the anti-solar longitude at the mid-point of the sector. For most of Year 2, the camera array is oriented such that Camera 4 is centered on the northern ecliptic pole: in this orientation, the southernmost edge of Camera 1 is ~6° from the ecliptic.

However, for Sectors 14 and 15, scattered light from the Earth and Moon is a significant problem in Cameras 1 and 2, reducing the available observing time for exoplanet transits by as much as 75% in those cameras. To reduce the impact of scattered light, the field-of-view of the camera array was shifted north by 31° with respect to its nominal pointing in Sectors 14 and 15.

When the cameras are shifted north, the northern ecliptic pole is located 7° from the center of camera 3, and the southernmost edge of Camera 1 is at an ecliptic latitude of ~37°.  In addition, with this shift, the fields-of-view of Cameras 3 and 4 observe “on the other side of the pole”, thereby providing additional observations of parts of the sky that would otherwise only be observed in Sectors 20-22.

Scattered light from the Earth and Moon is also expected to be a problem in Sectors 25 and 26 and, to a lesser extent, in Sectors 16 and 24.  The scattered light performance in Sectors 14 and 15 has been reviewed, and it was decided that Sector 16 would also have its pointing shifted north. In addition, it was decided that Sectors 24, 25, and 26 would benefit from having their pointings shifted north as well.

[Additional details on TESS observations can be found at the MIT TESS website](https://tess.mit.edu/observations/). The [Web TESS Viewing Tool (WTV)](https://heasarc.gsfc.nasa.gov/cgi-bin/tess/webtess/wtv.py) has been updated to reflect the change in pointing for Sectors 14, 15, and 16 as well as Sectors 24, 25, and 26.

The sky coverage maps for Sectors 1-21 are given below in the ecliptic and celestial coordinate systems and show the shifted fields for Sectors 14, 15, and 16. 

*Sectors 14, 15, and 16 shifted north:*
<img class="img-responsive" style="max-width:80%;" src="images/PM_ecl_S1-21_16up.png">
<img class="img-responsive" style="max-width:80%;" src="images/PM_cel_S1-21_16up.png">



<!-- MOVED TO PROPOSING INVESTIGATIONS
## Target selection
The TESS Input Catalog (TIC) is a catalog of approximately half a billion objects generated to assist in planning and executing observations and data reduction. The TIC includes detailed information about the characteristics of more than 2 million stars that have been identified as potential targets for the TESS Planet Search. The TIC also includes basic information for optically luminous persistent astronomical objects that may influence the photometry of TESS targets. More information on the TIC can be found [here](proposing-investigations.html#target-selection)

The Candidate Target List (CTL) is a subset of TIC objects isolated to select the >200,000 targets for 2 min cadence observations in service of the mission's primary science requirements. More information on the CTL can be found [here](proposing-investigations.html#candidate-target-list-ctl) -->

<!-- 
### Data yield


## Learn more

<ul>
  <li>
    <a href="k2-fields.html">Campaign fields &raquo;</a>
  </li>
    <li>
    <a href="proposing.html">Proposing targets &raquo;</a>
  </li>
  <li>
    <a href="k2-approved-programs.html">Approved observing programs &raquo;</a>
  </li>
</ul> -->


<!-- MOVED TO PROPOSING INVESTIGATIONS (GI PROGRAM PAGE)
## Proposal tips

Due to the observing strategy of the TESS mission, the TSSC notes that GI proposers should be aware of several details when composing a science cases and target lists.

* The exact location of the first observing sector (and therefore all subsequent observing sectors) is a sensitive function of the TESS launch date. For GI program Cycle 1, the impact of the uncertainty in the exact sky locations of the TESS FOVs is that there is no guarantee that any given proposed target will not fall into a gap between sectors, camera CCDs, or camera FOVs. The mitigate this uncertainty, Cycle 1 proposers are encouraged to consider target lists that include a number of similar sources distributed across the sky.

* Adjacent TESS observing sectors have overlapping regions near the ecliptic poles, providing longer-term continuous coverage for stars falling in these regions which in turn provides sensitivity to smaller and longer-period planets. Objects within 12 deg of the ecliptic poles may be observed for ~1 year.

* Camera 4 is always centered on the ecliptic pole and targets in this camera will be observed continuously for an entire Cycle. This leads to a limitation in the number of 2 min cadence targets that can be selected in the portion of sky covered by camera 4. 

* Camera 1 is always closest to the ecliptic plane and will be contaminated by stray light from the Earth and Moon during some observing sectors. The level of contamination and which sectors will be most affected is dependent on the launch date and the final inclination of the TESS orbit. These parameters will not be known until after commissioning and calibration.

* Some cameras during some observing sectors cover portions of the Galactic plane and suffer from increased background contamination.

* A primary science target will nominally be observed nearly continuously for 27.4 days in a given TESS observing sector. However, mission requirements only require a minimum of 20 days of observations out of the 27.4 possible per sector.  This requirement accounts for all sources of observing inefficiency, including repointing for data downlink and interruptions due to the Earth and/or Moon in a camera FOV. -->


