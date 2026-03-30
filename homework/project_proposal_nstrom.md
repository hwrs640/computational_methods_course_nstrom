# HWRS640 - Final Project: Proposal Pitch

## Hillslope Soil Moisture Evaluation and Reconstruction Using EOF Analysis

### 1. Motivation and scientific question
The Landscape Evolution Observatory contains three artificial hillslopes instrumented with a 3D network of soil-moisture sensors used to monitor hydrologic and geomorphic evolution through time. Because the hillslopes are designed to remain undisturbed, instrumentation cannot be replaced once installed. Sensor failure has gradually reduced the available observations overtime. 

Since the initial establishment of the bare basaltic soil medium, biocrust and moss have developed and irrigation events have occurred, which have potentially altered the hillslope’s hydraulic structure. This raises the question of whether the spatial relationships governing soil-moisture (SM) dynamics remain stable through time, and whether data from the early period—when most sensors were functioning, can be used to reconstruct soil moisture at later times when sensors have failed.

This study therefore addresses two questions:

1) Do the dominant spatial patterns underlying hillslope soil-moisture dynamics remain consistent through time (2014–present)?

2) If these spatial relationships are constant, can the larger sensor network available during the early experimental period be used to reconstruct soil-moisture observations at later times where sensors have failed?


### 2. Dataset

Soil moisture data from the LEO Hillslopes is available from 2014 - present. Each hillslope has a sensor network of 496 water content sensors sptially distributed over the surface and across 5 - 50 cm depths. The temporal resolution is 15 minutes. 

I am a member of the research team of LEO, and therefore this data is accessible to me through their online data portal.

Some challenges that may arise with this data is time gaps (brief periods where data collection failed), progressive sensor failure (loss of spatial coverage), and possible uncorrected drift in sensors. The possible bias/drift of sensors is therefore unknown, and if this occurs significantly, it will influence the data and results of this study. 

### 3. Proposed method

To extract the underlying spatial patterns of hillslope soil-moisture variability, the Empirical Orthogonal Function (EOF) method will be applied to the full-year timeseries of the 2014 soil-moisture dataset, when the majority of soil-moisture sensors were operational and data coverage was highest.

To test Question #1, the EOF basis derived from 2014 will be projected onto soil-moisture observations from selected time windows in later years (2018, 2022, 2026). Using the resulting EOF coefficients, the soil-moisture field will be reconstructed and the RMSE between the reconstructed and observed fields will be computed across all sensors. This provides a metric to assess whether the spatial structure extracted from the 2014 data remains representative of hillslope soil-moisture dynamics in later years.

If the results of Question #1 suggest that the spatial structure of soil-moisture variability remains consistent through time, Question #2 will evaluate whether these early EOF patterns can be used to reconstruct missing sensor observations. For the same years and time windows described above, a subset of functioning sensors will be treated as “dead,” while the remaining sensors will be used to estimate the EOF coefficients. These coefficients will then be used to reconstruct the soil-moisture values at the "dead" sensors, and the RMSE between predicted and observed values will be evaluated.

If the results of Question #1 suggest that the spatial structure of soil-moisture variability has changed through time, EOF analysis will instead be computed separately for each year using the available sensor observations. In this case, subsets of sensors will again be treated as “dead,” and reconstruction of the withheld sensors will be evaluated using EOF patterns derived from the contemporaneous dataset.

### 4. Expected outcomes and evaluation

I expect that the EOF from the early 2014 years will remain representative of hillslope SM through the later years. The hillslope has experience minimal human disturbance since its establishment ~14 years ago. The primary changes have been the natural developement of moss and biocrust on the soil surface. If the dominant spatial relationships controlling SM remain stable, reconstruction using the 2014 EOF basis should produce consistently low RMSE values when compared to observed SM fields in later years. 

If RMSE increases progressively through time, this may indicate a few changes; evolution of the geomorphic properties, sensor drift, or inadequate information due to sensor failure. 

In addition to RMSE-based evaluation of the EOF reconstruction approach, the method will be compared against simpler spatial interpolation techniques, such as inverse-distance weighted interpolation or kriging. These approaches rely only on information available at the current timestep and therefore provide a useful benchmark for assessing whether the EOF-based method offers improved reconstruction performance.
