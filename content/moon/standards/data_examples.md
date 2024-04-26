---
title: Examples
weight: 70
---

**DRAFT**

This section contains more technical content, with example metadata as well as links to sample data, metadata, and data creation tutorials to support the creation of Lunar SDI-compliant ARD. This is a living, non-exhaustive list of examples. We would appreciate any feedback, requests for additional examples, or contributions to help the community of data producers and data providers.

### Map Projections
Map projections can be specified using Well Known Text (WKT) projection strings,[`proj:json`](https://proj.org/en/6.2/usage/projjson.html) strings, and/or [PROJ](https://proj.org/en/9.4/) defined projection shortcodes such as `IAU:2015:30130` or `IAU_2015:30130`. The options for communicating the data projection are provided in order of preference, with WKT projection strings offering the highest interoperability across tools and projection shortcodes offering good, but not universal interoperability[^1]. To find WKT projection strings that reflect IAU WGCCRE recommendations see [here](http://voparis-vespa-crs.obspm.fr:8080/web/moon.html). An example of one such string follows:

```
PROJCRS["Moon (2015) - Sphere / Ocentric/ North Polar",
    BASEGEOGCRS["Moon (2015) - Sphere / Ocentric",
        DATUM["Moon (2015) - Sphere",
    	ELLIPSOID["Moon (2015) - Sphere", 1737400, 0,
		LENGTHUNIT["metre", 1, ID["EPSG", 9001]]]],
    	PRIMEM["Reference Meridian", 0,
            ANGLEUNIT["degree", 0.0174532925199433, ID["EPSG", 9122]]],
        ID["IAU", 30100, 2015]],
    CONVERSION["North Polar",
        METHOD["Polar Stereographic (variant A)",
            ID["EPSG", 9810]],
        PARAMETER["Latitude of natural origin", 90,
            ANGLEUNIT["degree",0.0174532925199433,ID["EPSG", 9122]],
            ID["EPSG", 8801]],
		PARAMETER["Longitude of natural origin", 0,
            ANGLEUNIT["degree",0.0174532925199433,ID["EPSG", 9122]],
            ID["EPSG", 8802]],
		PARAMETER["Scale factor at natural origin", 1,
            SCALEUNIT["unity",1,ID["EPSG", 9201]],
            ID["EPSG", 8805]],
		PARAMETER["False easting", 0,
            LENGTHUNIT["metre",1,ID["EPSG", 9001]],
            ID["EPSG", 8806]],
		PARAMETER["False northing", 0,
            LENGTHUNIT["metre",1,ID["EPSG", 9001]],
            ID["EPSG", 8807]]],
    CS[Cartesian, 2],
        AXIS["Easting (E)", east,
            ORDER[1],
            LENGTHUNIT["metre", 1]],
        AXIS["Northing (N)", north,
            ORDER[2],
            LENGTHUNIT["metre", 1]],
    ID["IAU", 30130, 2015]]
```

This WKT string is complex and encodes a lot of information. The horizontal datum being used, radii, map projection and map projection parameters, and units (x,y and degrees) are all specified. When questions arise, data producers are encouraged to work with data providers, who have expertise with these projection strings.

Data providers can choose to provide data with a WKT string outside those available [here](http://voparis-vespa-crs.obspm.fr:8080/web/moon.html). Why might one do this? With high-resolution data, for example, at a landing site, it is often preferable to use locally centered projections (with different center latitude, and center longitude parameters which are not defaults provided at the aforementioned link). When providing data this way data providers are cautioned to be careful to specify a valid WKT string. One can run [`projinfo`](https://proj.org/en/9.3/apps/projinfo.html) as a tool for starting to validate a custom WKT projection definition.

For providers wishing to use `proj:json`, the same [`projinfo`](https://proj.org/en/9.3/apps/projinfo.html) command can be used to perform a conversion.

#### Conversion from proj:json to WKT (and back).
[PROJJSON](https://proj.org/en/9.3/specifications/projjson.html) is simply a JSON wrapper around a WKT2 projection string. A PROJJSON string and a WKT2 string contain the same information encoded differently. Therefore conversion from one format to another can be accomplished using existing tools.

The [`projinfo`](https://proj.org/en/9.3/apps/projinfo.html) command, that ships with the PROJ library (a dependency of GDAL, among many other spatial libraries) can perform format conversion. for example, the WKT example above can be converted to PROJJSON using: `projinfo IAU_2015:30130 -o projjson`. 

#### Why not use just PROJ shortcodes or simple PROJ strings?
PROJ short codes (e.g., `IAU_2015:30100`) are not interoperable when a client does not have access to a PROJ database with that shortcode. For example, the use of a short code will fail for most, if not all, web clients because they do not have the PROJ database (PROJSON is preferred). Likewise, older ArcGIS or QGIS installations are not guaranteed to have up-to-date PROJ databases.

Simple PROJ strings (e.g., `+proj=latlong +R=1737400`) are concise and usable in many applications. While portable and relatively easy to remember, these strings are lossy. They do not encode the same information (such as horizontal or vertical datum) as a WKT or PROJJSON string. Therefore, the use of these strings to describe Lunar SDI-endorsed data is discouraged.

### Human Readable Metadata
Examples of human-readable, lunar-focused metadata are available [here](https://stac.astrogeology.usgs.gov/docs/data/moon/kaguyatc/). The data documentation has been written targeting new data users with some background in planetary science, but no previous knowledge of this particular data set. All processing applied is described in plain language (see below for provenance or reproducibility examples), quantitative issues with the data are described, and when possible screen captures or GIFs are provided illustrating what these issues look like, and qualitative issues are discussed under the general usability heading. This format is one example of how a data provider can document their data and illustrates the style of documentation the Lunar SDI is promoting.

### Machine Readable Metadata
Examples of [STAC](https://stacspec.org) metadata, with support for planetary spatial data, are available via the [USGS STAC API](https://stac.astrogeology.usgs.gov/api/). One such example is [here](https://stac.astrogeology.usgs.gov/api/collections/kaguya_terrain_camera_stereoscopic_uncontrolled_observations/items/TC1W2B0_01_07109N362E3402). More tutorials on creating STAC metadata will be forthcoming.

- [STAC Validation Tool](https://staclint.com)
- [STAC Specification](https://github.com/radiantearth/stac-spec)
- [STAC Solar System Extension](https://github.com/stac-extensions/ssys)
- [Additional STAC Extensions](https://stac-extensions.github.io): See View Geometry, Electro-Optical, Projection, Point Cloud, Raster, and Scientific Citation for extensions known to be actively used by planetary STAC collections.

### Creating GeoPackage Vector Data Sets   
GeoPackage data sets can be created natively in QGIS and ArcGIS. Alternatively, command line tools can be used to convert legacy shapefiles to the more modern GeoPackage format.

- [In ArcGIS / ArcPro](https://learn.openwaterfoundation.org/owf-learn-geopackage/using-geopackage/arcgis/)
- [In QGIS 2 / 3](https://learn.openwaterfoundation.org/owf-learn-geopackage/using-geopackage/qgis/)
- [Using ogr2ogr](https://gdal.org/programs/ogr2ogr.html)

### Provenance  
Provenance files will vary by data product. Here are a few examples that are attempting to be closer to plain text scripts that users can simply run, to reproduce the processing that has been applied. 

- [Kaguya Terrain Camera Raw to ARD](https://astrogeo-ard.s3-us-west-2.amazonaws.com/moon/kaguya/terrain_camera/stereoscopic/uncontrolled/TC1W2B0_01_07109N362E3402/provenance.txt)
- [Controlled Galileo SSI](https://astrogeo-ard.s3-us-west-2.amazonaws.com/jupiter/europa/galileo_voyager/usgs_controlled_observations/s0639063413/provenance.txt): Note that this provenance starts from the photogrammetrically controlled product. This is because the [documentation](https://stac.astrogeology.usgs.gov/docs/data/jupiter/europa/galileo_individual_images/) describes the control that was applied (and that control is not easily reproduced). We hope that the source ISIS cube files will be archived somewhere, and these ARD, like all ARD, are derived from those archived data.


### Discussion

{{< comments >}}

[^1: IAU shortcodes require the PROJ shipped database which is available for local installs (e.g., with GDAL, ArcGIS, QGIS, etc). The PROJ database is not available for most javascript clients. Therefore, WKT strings offer higher interoperability than shortcodes.