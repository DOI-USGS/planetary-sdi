---
title: Data Checklist
weight: 100
---

This section contains a checklist for data producers and data providers to use to assess the compliance of their data to the lunar SDI standards. The goal of the checklist is to help determine what level of effort would be required to bring the data set into compliance.

Data products that are compliant with the checklist will be certified by the Lunar SDI and promoted. Ultimately, we seek to answer four questions:

1. Do the data meet the LSDI spatial standards?
1. Do the data meet the LSDI format standards?
1. Do the metadata meet the LSDI standards?
1. Is the license compliant with the LSDI licensing requirements?

A key role played by the lunar SDI is to help data producers release data via data providers. We are here to help producers and providers. If the checklist is daunting or the steps needed to alter the data are unclear, please reach out.

## Compliance Importance
Compliance with the LSDI standards is not a binary, yes/no, assessment. Ultimately, the goal of meeting these standards is to maximize the discoverability, usability, and interoperability of data for all users. Therefore, the following high-level guidance can be used when assessing how compliant a data set is:

1. Are the data in formats that are usable in tools that users already use?
1. Are the data spatially compliant and well documented? Does a user have to intimately understand radii, datum, or map projection?
1. Does that data have machine-readable metadata that is discoverable with the LSDI ecosystem (e.g., STAC)?
1. Does the data have human-readable documentation, written in an accessible manner where a new user can safely use the product for science or engineering goals?

## A Note on PDS Archives
PDS archives seek to solve the problem of long-term data preservation and storage. Long-term data archiving goals are orthogonal (at best) to the goals of the LSDI standards. Under the current scope of effort, as defined by the PDS, their holdings are not compliant with the LSDI standards. Rather, PDS holdings are terrific input data sets to be postprocessed to meet the LSDI standards.

### Data Standards
These data standards apply whether the data are provided in raster or vector formats. Most of these standards can be checked using the `gdalinfo` and `ogrinfo` tools. See our examples for guidance using those tools.

#### Body Standards
- [ ] The data were created or adjusted to use a reference sphere with a radius of 1737.4km.
- [ ] The ephemeris information used to create the data used JPL DE 421 or JPL DE 440. One needs to validate this either via an included PDS label, ISIS label, CSM ISD, or other sidecar file that describes the ephemeris information used to map project the product.
- [ ] The reference sphere and ephemeris are declared in metadata and/or projection strings. 

#### Vertical and Horizontal Datum
- [ ] The horizontal and vertical datums the data uses are declared in metadata and/or projection string.
- [ ] The metadata provided with the data describes any efforts, and associated accuracies, to tie the product to the horizontal and/or vertical datum.
- [ ] If topographic data, data are released with the z-dimension in radius **or** the metadata declared the reference surface from which potential heights were computed.

#### Map Projection
- [ ] If provided in raster format, the data are map projected.
- [ ] If provided in vector format, the data are **not** map projected.
- [ ] The map projection uses a valid well-known text string. (Reference projections are available [here](http://voparis-vespa-crs.obspm.fr:8080/web/moon.html)).
- [ ] The data use the -180 to 180 longitude domain.

#### Vector Symbology
These apply if the data are provided in a vector format.

- [ ] If the data have a specific symbology (e.g., for a geologic map), a compliant Styled Layer Descriptor (SLD) file is also embedded or provided.

#### Ephemeris Information
These apply if the data include external ephemeris information. For example, through the release of updated ephemeris data.

- [ ] NAIF SPICE kernels **or** Community Sensor Model ISD or state files are provided.

### Data Formats

#### Formats for Offline Data Access

- [ ] If raster data, the data are provided as valid Cloud Optimized GeoTiffs.
- [ ]If vector data, the data are provided as an OGC GeoPackage with associated layer symbology. 

#### Formats for Online Data Access

- [ ] If raster data, the data are provided as valid Cloud Optimized GeoTiffs with accompanying Spatiotemporal Asset Catalog (STAC) metadata **or** the data are provided by an OGC-compliant server (e.g., a WMS).
- [ ] If vector data, the data are provided using an OGC-compliant server such as WMS or WMTS **or** a vector tile server.
- [ ] If lidar data, the data are provided using the COPC format.
- [ ] Online data sources are properly communicating the data projection.
- [ ] Data are discoverable via STAC metadata, provided via a STAC-API-compliant server.

### Metadata Standards

#### General

- [ ] The data are accompanied by STAC metadata. Reviewers should seek out [JSON](https://json.org/example.html) formatted metadata and attempt to validate it using the tools described [here](data_examples.md#machine-readable-metadata)
- [ ] Data have an ISO:19157:3013 style XML metadata file (optional).
- [ ] The data have a publicly available homepage.

#### Metadata Content
The metadata, preferably available in a single, human-readable webpage includes:
  - [ ] a description of the data set;
  - [ ] a description of the process used to create the data set;
  - [ ] the available assets or files provided in the data set;
  - [ ] a discussion of the quantitative aspects of the data (e.g., accuracy, precision, identified errors, etc.);
  - [ ] a discussion of the qualitative or fitness-for-use aspects of the data;
  - [ ] a description of the proposed update cadence for the data;
  - [ ] links to appropriate peer-reviewed data descriptions;
  - [ ] optionally, links to associated data sets.

#### Accuracy Descriptions

- [ ] Horizontal, vertical, and attribute accuracy statements use ISO 19157:2013 (optional).

#### Provenance and Traceability

- [ ] The data include a textual processing description.
- [ ] The data includes step-by-step processing commands **or** a runnable script to reproduce the data product.

#### AI/ML Derived Data

- [ ] Data are appropriately labeled if they were derived, in whole or in part, using AI/ML techniques.
- [ ] Data making use of statistical learning, generative, or other AI/ML methods are appropriately labelled as such.

#### Data Interpolation

- [ ] Interpolated data are labeled as such with a description of the interpolation methods used.

#### Linkages

- [ ] Data links back to the source archive or products used in their derivation.

### Licensing

- [ ] Data are appropriately licensed, with a permissive, open license. See our discussion on [licensing](licensing.md) for more information on this criteria.



### Discussion

{{< comments >}}

