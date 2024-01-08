---
title: Lunar Data Interoperability Standards
weight: 40
---

**DRAFT**

Data promoted by the lunar SDI must adhere to the standards idenfied here-in. These standards are intended to cover data at rest (data which are not being actively analyzed and manipulated by a tool or frontend visualization client, these are examples of data at use). These standards have been identified so that data providers, tool developers, frontend developers, and off-the-shelf tools can all interoperate using a shared understanding.

We understand that the projections, datums, and symbologies for data at rest will differ from the optimal representation in a tool. As stated above, the goal of these standards is to set common expectations for interoperability between provders and users.

### Body Parameters
The [Report of the IAU Working Group on Cartographic Coordinates and Rotational Elements: 2015 (Archinal, et al. 2018)](https://doi.org/10.1007/s10569-017-9805-5) and the [Final Report of the Lunar Critical Data Products Specific Action Team](https://www.lpi.usra.edu/mapsit/standup-committees/LCDP-SAT-REPORT-20211110.pdf) (LCDP-SAT) body parameters will be used. This includes a sphere radius of 1737.4km, the 2008 JPL DE 421 ephemeris (but soon expected to change to the DE 440 ephemeris) rotated to the mean Earth/polar axis (ME) system and rotation parameters as defined in Table 2 (Archinal, et al., 2018).

### Horizontal and Vertical Datum
Reference sphere defined as 1737.4km as defined by the IAU ([Archinal, et al. 2018](https://doi.org/10.1007/s10569-017-9805-5)). Proxy products usable to tie to the vertical reference frame (and have topography or shape) include, but are not limited to:
- [Gridded Lunar Orbiter Laser Altimeter (LOLA)](https://doi.org/10.17189/1520642)
- SLDEM 2015 (also part of the [LOLA](https://doi.org/10.17189/1520642) archive)
- Lunar Polar Gridded Data Record

The standard horizontal datum to be used is the 2008 JPL DE 421, which is expected to shift to the 2021 JPL DE 440 ephemeris (and new projects should begin using the DE 440). The proxy products that data creators can use to tie new data products to the horizontal reference frames include:
- Gridded Lunar Orbiter Laser Altimeter (LOLA) 
- SLDEM 2015
- Lunar Polar Gridded Data Record

At this time, no global visible observations are usable to rigorously align to the horizontal reference frame.

### Map Projections
- Data are provided map projected, with a valid, well known text (such as those documented [here](http://voparis-vespa-crs.obspm.fr:8080/web/moon.html)) or [`proj:json`](https://proj.org/specifications/projjson.html) projection string.
  - Rationale: A goal of the lunar SDI is to improve data accessability and access. One way to do that is to provide to users, data processed and ready for analysis. By providing map projected products with properly defined projection strings, users can immediately work with data products from multiple providers in off-the-shelf tools.
- Data are orthorectified to a sphere using the IAU radius => 1737.4km ([Archinal, et al. 2018](https://doi.org/10.1007/s10569-017-9805-5)), or higher fidelity shape model using the IAU endorsed radii. Data report the proper vertical datum via their WKT or `proj:json` projection string.
  - Rationale: Variations in the underlying vertical datum can have dramatic, and hard to debug effects as the scale of analysis increases. The IAU is the standards body from which datum definitions emerge, and it is essential that data are properly reporting their datums.
- Data are made available in -180 to 180 positive East coordinate system with a center longitude of 0 degrees using [planetocentric or planetographic latitude](https://proj.org/en/9.3/operations/conversions/geoc.html). We note that either latitude definition is acceptable because the IAU sphere is used.
  - Rationale: Off-the-shelf tools, with an earth focus operate almost exclusively in the -180 to 180 domain. The same can be said for the specifications (promoted by organizations like the OGC) tht facilitate data interoperability. We understand that many data user prefer to work in the 0 to 360 longitude domain and actively promote tools and user-interfaces that makes this possible. 

### Vector Symbology
- The OGC maintained [Styled Layer Descriptor](https://www.ogc.org/standards/sld) standard will be used for vector symbology for all data in the GeoPackage format.

### Ephemeris Information
- All sun, spacecraft, sensor, and target body ephemeris information is to be provided either by [Navigation and Ancillary Information Facility (NAIF)](https://naif.jpl.nasa.gov/naif/) as SPICE kernels or in NAIF SPICE compliant format by another provider (e.g., a mission team). This includes sensor and target positions, velocities, and orientations as well as sensor parameters such as distortion models.

Alternatively, ephemeris information can be provided using a common interchange format such as a Community Sensor Model [Images Support Data]() or [State]() file. These plain text files should repackage data sourced from the NAIF SPICE kernerls or be data derived from said kernels (for example, after photogrammetric control). See [Planetary Sensor Models Interoperability Using the Community Sensor Model Specification](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2019EA000713) for additional information.

### Discussion

{{< comments >}}