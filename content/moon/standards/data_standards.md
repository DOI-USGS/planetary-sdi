---
title: Data Interoperability Standards
weight: 31.1
---

**DRAFT**

### Body Parameters
The Report of the IAU Working Group on Cartographic Coordinates and Rotational Elements: 2015 (2018) and the Final Report of the Lunar Critical Data Products Specific Action Team (LCDP-SAT) body parameters will be used. This includes a sphere radius of 1737.4km, the 2008 JPL DE 421 ephemeris rotated to the mean Earth/polar axis (ME) system and rotation parameters as defined in Table 2 (Archinal, et al., 2018).

### Horizontal and Vertical Datum
Reference sphere defined as 1737.4km as defined by the IAU (IAU;2018). Proxy products usable to tie to the vertical reference frame (and have topography or shape) include:
- Gridded Lunar Orbiter Laser Altimeter (LOLA) 
- SLDEM 2015
- Lunar Polar Gridded Data Record

The horizontal datum to be used is the 2008 JPL DE 421, which, as per the LCDP-SAT, is only slightly different than the 2021 JPL DE 440 ephemerides. The proxy products that data creators can use to tie new data products to the horizontal reference frames include:
- Gridded Lunar Orbiter Laser Altimeter (LOLA) 
- SLDEM 2015
- Lunar Polar Gridded Data Record
At this time, no global visible observations are usable to rigorously align to the horizontal reference frame.

### Map Projections
- Data are provided in a simple cylindrical (equirectangular) map projection.
- Data are orthorectified to a sphere using the IAU radius => 1737.4km (sphere)
- Data are made available in a -180 – 180 (CLON 0; web maps hate this)  OR 0 – 360 (lots of data in this system; historical argument) Positive East coordinate system with a center longitude of 180 degrees and use planetocentric latitude. 
- For observational data, pixel scale or resolution should be maintained at native scale, (i.e., do not up sample or down sample data.) 
- For derived data (e.g., DTMs), data should be made available at a reasonable resolution that avoids extrapolation of information.
- Data for large spatial scale (e.g., 1:24000), small spatial extent maps, (e.g. landing sites) can be provided in a local stereographic (candidate to also have a grab bag to also include gnomonic and orthographic) centered on image.
- Data at mid-latitudes (35˚ - 65˚ N/S) data providers are encouraged to also provide data in a Lambert Conformal Conic Projection with a longitude origin of 0 and standard parallels of 33˚ and 45˚ N/S (as appropriate). (discuss; this is a classic North America LCC)
- Data for polar areas (latitudes > ??˚ North or South) should use a polar stereographic projection centered at the pole.

### Ephemeris Information
- All sun, spacecraft, sensor, and target body ephemeris information is to be provided either by [Navigation and Ancillary Information Facility (NAIF)](https://naif.jpl.nasa.gov/naif/) as SPICE kernels or in NAIF SPICE compliant format by another provider (e.g., a mission team). This includes sensor and target positions, velocities, and orientations as well as sensor parameters such as distortion models.