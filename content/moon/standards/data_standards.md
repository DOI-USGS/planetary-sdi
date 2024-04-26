---
title: Lunar Data Interoperability Standards
weight: 40
---

**DRAFT**

Data promoted by the lunar SDI must adhere to the standards identified herein. These standards are intended to cover data-at-rest (data that are not being actively analyzed and manipulated by a tool or frontend visualization client, these are examples of data at use). These standards have been identified so that data providers, tool developers, frontend developers, and off-the-shelf tools can all interoperate using a shared understanding of the source data and source metadata formats, structure, and capabilities.

We understand that the projections, datums, and symbologies for data-at-rest will differ from the optimal representation in a tool for data-in-use. As stated above, the goal of these standards is to set common expectations for interoperability between providers and users.

### Body Standards
“A Standardized Lunar Coordinate System for the Lunar Reconnaissance Orbiter and Lunar Datasets” from the LRO mission and the Lunar Geodesy and Cartography Working Group“, the [Report of the IAU Working Group on Cartographic Coordinates and Rotational Elements: 2015 (Archinal, et al. 2018)](https://doi.org/10.1007/s10569-017-9805-5), and the [Final Report of the Lunar Critical Data Products Specific Action Team](https://www.lpi.usra.edu/mapsit/standup-committees/LCDP-SAT-REPORT-20211110.pdf) (LCDP-SAT) body parameters will be used. This includes a reference sphere radius of 1737.4 km, the 2008 JPL DE 421 ephemeris (but soon expected to change to the DE 440 ephemeris) rotated to the mean Earth/polar axis (ME) system and rotation parameters as defined in (Archinal, et al., 2018, Section 3).

### Vertical and Horizontal Datum
The vertical datum to be used is a reference sphere with a 1737.4 km radius as defined by the IAU Working Group on Cartographic Coordinates and Rotational Elements (WGCCRE) (Archinal, et al. 2018). Geometric height should be expressed as either a radius from the center of mass of the Moon, or the height above the reference sphere. Proxy products usable to tie to the vertical reference frame (and have topography or shape) include, but are not limited to:

- [Gridded Lunar Orbiter Laser Altimeter (LOLA)](https://doi.org/10.17189/1520642)
- SLDEM 2015 (also part of the [LOLA](https://doi.org/10.17189/1520642) archive)
- Lunar Polar Gridded Data Record

A best practice we promote is the specification of height based on the body radius. Heights in these data sets will be stored in a [Body-Centered, Body-Fixed](https://en.wikipedia.org/wiki/Earth-centered,_Earth-fixed_coordinate_system) coordinate system with heights taking the form of radius values and the origin being the IAU-defined body center (center of mass). When data sets with a vertical component store height in a different form, for example, height above some ellipsoid, data producers and data providers must ensure proper documentation **and** a properly declared vertical datum in the metadata.

Ideally, any computed potential heights should use the best available lunar geoid (and not a geometric surface, such as a shere or ellipsoid). The current best available lunar geoid is the [GRGM1200A geoid](https://pgda.gsfc.nasa.gov/products/50), though that product uses a radius of 1738km (and not the newer, IAU-endorsed radius of 1737.4km).

The standard horizontal datum to be used is the 2008 JPL DE 421 rotated to the ME frame, which is expected to shift to the 2021 JPL DE 440 ephemeris rotated to the DE 421 ME frame (and new projects should begin using the DE 440). The proxy products that data creators can use to tie new data products to the horizontal reference frames include: 
- Gridded Lunar Orbiter Laser Altimeter (LOLA):
- [SLDEM 2015](https://pgda.gsfc.nasa.gov/products/54): Values are relative to the 1737.4km sphere.
- Lunar Polar Gridded Data Record:

At this time, no globally photogrammetrically controlled visible or IR observations are usable as a proxy for the horizontal reference frame. The positional accuracy of some lunar observations are known well enough that they can be used for inter-observation alignment at a given error budget(e.g., LRO WAC observations are assessed to be accurate to ___________).

### Map Projections
- Data are provided map projected, with a valid well-known text (such as those documented [here](http://voparis-vespa-crs.obspm.fr:8080/web/moon.html)) or [`proj:json`](https://proj.org/specifications/projjson.html) projection string.
  - Rationale: A goal of the lunar SDI is to improve data accessibility and access. One way to do that is to provide to users, data processed and ready for analysis. By providing map-projected products with properly defined projection strings, users can immediately work with data products from multiple providers in off-the-shelf tools.
- Data are orthorectified to a sphere using the IAU WGCCRE radius => 1737.4km ([Archinal, et al. 2018](https://doi.org/10.1007/s10569-017-9805-5)), or a higher fidelity shape model referenced to the center of mass of the Moon or the IAU reference radius. Data report the proper vertical datum via their WKT or `proj:json` projection string.
  - Rationale: Variations in the underlying vertical datum can have dramatic, and hard-to-debug effects as the scale of analysis increases. The IAU WGCCRE is the Solar System (other than the Earth) standards body from which datum definitions emerge, and data must be properly reporting their datums.
- Data are stored at rest in a -180 to 180 positive East coordinate system with a center longitude of 0 degrees using [planetocentric](https://proj.org/en/9.3/operations/conversions/geoc.html). We note that planetocentric and planetographic latitude definitions are the same if a reference sphere is used; however, because of the possibility of confusion, we recommend using planetocentric.
  - Rationale: Off-the-shelf tools, with an earth focus, operate almost exclusively in the -180 to 180 degrees domain. The same can be said for the specifications (promoted by organizations like the OGC) that facilitate data interoperability. We understand that many data users prefer to work in the 0 to 360 longitude domain and actively promote tools and user interfaces that make this possible. We note that the LRO mission and representatives of several space agencies (including NASA, ESA, JAXA, ISRO, CNSA) have agreed to use a 0 to 360 longitude domain ([LGCWG White Paper, 2008](https://science.nasa.gov/wp-content/uploads/2024/01/luncoordwhitepaper-10-08.pdf)). Our recommendation is that data provided to maximize interoperability be stored, at rest, in the longitude domain ammenable to the storage standards and tooling. Clients, tools, and user interfaces can then ingest that data without ambiguity and convert to the desired longitude domain.

### Vector Symbology
The OGC-maintained [Styled Layer Descriptor](https://www.ogc.org/standards/sld) standard will be used for vector symbology for all data in the GeoPackage format.

### Ephemeris Information
- All Moon, Earth, Sun, spacecraft, and sensor ephemeris information is to be provided either by  [Navigation and Ancillary Information Facility (NAIF)](https://naif.jpl.nasa.gov/naif/) as SPICE kernels or in NAIF SPICE compliant format by another provider (e.g., a mission team). This includes sensor and target positions, velocities, and orientations as well as sensor parameters such as distortion models. The JPL DE 440 ephemeris should be used for the positions of Solar System bodies. 

Alternatively, ephemeris information can be provided using a common interchange format such as a Community Sensor Model [Images Support Data]() or [State]() file. These plain text files should repackage data sourced from the NAIF SPICE kernels or be data derived from said kernels (for example, after photogrammetric control). See [Planetary Sensor Models Interoperability Using the Community Sensor Model Specification](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2019EA000713) for additional information.

### Discussion

{{< comments >}}