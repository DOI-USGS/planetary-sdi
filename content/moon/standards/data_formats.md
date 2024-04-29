---
title: Lunar Data Format Standards
weight: 50
---

### Formats for Offline Data Access
- Data in raster format should be provided as cloud-optimized[ GeoTiffs](https://www.cogeo.org)(COG), complying with the [cartographic standards]({{< ref "data_standards/#map-projections" >}}). 
  - Rationale: a COG is "just" a GeoTIFF with additional header information that supports data streaming. COGs are preferable as data volumes increase and local analyses of large data volumes become less tractable. Legacy TIFFs can be converted to COGs with little overhead beyond the (re)processing costs.
- Data in vector format should be provided in [OGC GeoPackage format](https://www.geopackage.org) with information stored in decimal degrees (i.e., no map projection applied) or in a map projected form complying with the [cartographic standards]({{< ref "data_standards/#map-projections" >}})
  - Rationale: More widely used vector data standards such as [Shapefile](http://switchfromshapefile.org) are rapidly approaching their End-of-Life. Therefore, we suggest that data users (who often create vector data sets) consider shifting their workflows slightly. See the [data examples]({{< ref "data_examples" >}}) for suggestions on creating GeoPackage files natively **or** converting shapefiles into GeoPackage files. Vector data provided in formats other than GeoPackage should include files for proper representation of features without the need for propriety visualization software. This is especially important for data such as geologic maps where the symbology are essential to interpretation of the data.


### Formats for Online Data Access
- Data in raster format should be provided as cloud-optimized[ GeoTiffs](https://www.cogeo.org), complying with the above projection standards. These data will be accessed via their [STAC](https://stacspec.org/en) data files. Alternatively, data in raster format can be provided using an OGC-compliant [WMS](https://www.ogc.org/standards/wms) service. This service must encode a proper [IAU 2015/2018 projection code](https://ui.adsabs.harvard.edu/abs/2021LPICo2549.7012H).
  - Rationale: As data volumes increase, data formats that are both interoperable with existing tooling and performant are required. COGs and OCG WMS both provide remote, streaming data access, a means to communicate spatial metadata and work with the vast majority of spatial tools. For interoperability, standards-compliant projection information must be explicitly included in the data.
- Data in vector format should be served using an OCG-compliant [WFS](https://www.ogc.org/standards/wfs) or [WMTS](https://www.ogc.org/standards/wmts) service or a vector tile server. Most importantly, the server must encode a proper [IAU 2015/2018 projection code](https://ui.adsabs.harvard.edu/abs/2021LPICo2549.7012H).
  - Rationale: The complexity of vector data, in terms of vertex count and symbology, is ever-increasing. These OGC standards provide high interoperability and encode projections (something that standards like GeoJSON fail to include).
- The [STAC-API](https://github.com/radiantearth/stac-api-spec) specification (a remotely accessible search service) will be used to support metadata query and data discoverability. 
  - Rationale: The STAC-API is the preferred search API for lunar SDI-endorsed data. This API supports spatial, temporal, and attribute-level queries, is maintained by a large group of corporate, government, and non-governmental organizations, and has proven scalability beyond the raw count of planetary observations. Data providers meet the shared discovery expectations of tool developers and users via a STAC-API-compliant search endpoint.
- Lidar (point cloud) data will be provided using the [Cloud Optimised Point Cloud (COPC)](https://copc.io) or [Entwine Point Tile (EPT)](https://entwine.io/entwine-point-tile.html) format with proper WKT or `proj:json` projection information. Lidar data are encouraged to use an [STAC](https://stacspec.org/en) metadata file for improved discoverability. Further, when possible data should be provided in gridded and ungridded (e.g., point cloud for DTMs) forms.
  - Rationale: Terrestrial lidar projects of varying scales have coalesced around several highly interoperable formats such as [LAS and LAZ](https://learn.rockrobotic.com/understanding-las-and-laz-file-formats). These formats, released over 20 years ago, are developed and maintained by the American Society for Photogrammetry and Remote Sensing. The COPC and Entwine formats are small extensions to LAS/LAZ that improve cloud-based streaming and data expansion without sacrificing interoperability.

### Discussion

{{< comments >}}