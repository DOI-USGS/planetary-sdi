---
title: Data Interoperability Standards
weight: 31.1
---

**DRAFT**

### Body Parameters
The [Report of the IAU Working Group on Cartographic Coordinates and Rotational Elements: 2015 (Archinal, et al. 2018)](https://doi.org/10.1007/s10569-017-9805-5) and the [Final Report of the Lunar Critical Data Products Specific Action Team](https://www.lpi.usra.edu/mapsit/standup-committees/LCDP-SAT-REPORT-20211110.pdf) (LCDP-SAT) body parameters will be used. This includes a sphere radius of 1737.4km, the 2008 JPL DE 421 ephemeris (but soon expected to change to the DE 440 ephemeris) rotated to the mean Earth/polar axis (ME) system and rotation parameters as defined in Table 2 (Archinal, et al., 2018).

### Horizontal and Vertical Datum
Reference sphere defined as 1737.4km as defined by the IAU ([Archinal, et al. 2018](https://doi.org/10.1007/s10569-017-9805-5)). Proxy products usable to tie to the vertical reference frame (and have topography or shape) include:
- [Gridded Lunar Orbiter Laser Altimeter (LOLA)](https://doi.org/10.17189/1520642)
- SLDEM 2015
- Lunar Polar Gridded Data Record

The standard horizontal datum to be used is the 2008 JPL DE 421, which is expected to shift to the 2021 JPL DE 440 ephemeris (and new projects should begin using the DE 440). The proxy products that data creators can use to tie new data products to the horizontal reference frames include:
- Gridded Lunar Orbiter Laser Altimeter (LOLA) 
- SLDEM 2015
- Lunar Polar Gridded Data Record

At this time, no global visible observations are usable to rigorously align to the horizontal reference frame.

### Map Projections
- See [cartographic standards]({{< ref "cartographic_standards" >}}).

### Ephemeris Information
- All sun, spacecraft, sensor, and target body ephemeris information is to be provided either by [Navigation and Ancillary Information Facility (NAIF)](https://naif.jpl.nasa.gov/naif/) as SPICE kernels or in NAIF SPICE compliant format by another provider (e.g., a mission team). This includes sensor and target positions, velocities, and orientations as well as sensor parameters such as distortion models.
