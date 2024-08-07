---
title: Lunar Metadata Standards
weight: 60
---

Human and machine-readable metadata are the cornerstone of data usability. These metadata must provide enough information so that users can make informed decisions about the suitability of a product for their use case. These metadata must also support machine discoverability, access, and traversability to other, related data sets. The framework to assess and maximize the usability of data is detailed by the [FAIR principles](https://www.go-fair.org/fair-principles/), where data and metadata are assessed on criteria related to Findability, Accessibility, Interoperability, and Reuse. 

We assume that data being made available to users are available digitally via the internet. Therefore, these metadata standards make use of current, spatial metadata standards that support cloud-native storage and data processing.

The standards described here are general because the ability to create metadata is varied based on the data set. In brief, data promoted under the lunar SDI should:

- make use of the Spatio-Temporal Asset Catalog (STAC) specification that supports discoverability. By definition all promoted data have a spatial, and likely a temporal, dimension. 
- have an accessible data documentation page, and possibly one or more peer-reviewed publications, that contain best-effort quantitative accuracies and a qualitative, fitness-of-use report.
- include provenance information describing how the data were created in a manner that supports transparency and reproducibility from archived data. This could be a listing of the exact processing commands and software version information used to create the data from archived from or a detailed, plain text description of all processing steps.
- ultimately metadata should be indexed in a federal data catalog as directed by NASA SMD information policy [SPD-41a](https://smd-cms.nasa.gov/wp-content/uploads/2023/08/smd-information-policy-spd-41a.pdf) so that resources are discoverable via [data.gov](https://data.gov/).


### Metadata Content
Data will have qualitative process and usability information available in text format that describes (1) a description of the data set, (2) the process used to create the data, (3) the available assets or files within a data set, (4) the precision, accuracy, errors, and identification of error sources and known issues with the data set, (5) the qualitative usability of the data set (as mediated by the data provider), (6) textual description of the proposed update cadence for this data set, and (7) optionally textual links to other data sets of potential interest to users of this data set.

### Accuracy Descriptions
Accuracy statements should consider using a standard reporting mechanism such as the [ISO 19157:2013 standard](https://wiki.icaci.org/index.php?title=ISO_19157:2013_Geographic_information_-_Data_quality). 

### Qualitative Fitness of Use 
We are not aware of existing qualitative, fitness-for-use standards. Therefore, these statements can be varied in form. Please consider describing the types of qualitative issues that may be present in the given dataset, the motivation for the original data collection and initial intended use, the use cases that are most likely for the data product, and the use cases where caution is required. Please also describe the original purpose for which the data were created.


### Provenance and Traceability
The goal of provenance is to allow a user to reproduce the creation of an analysis-ready data product from the archived form. Why is this desirable? As an example, for some applications, the traceability of individual pixel values can be of extreme importance. Are their values anomalous because of processing that occurred, or are they observations warranting additional study? To allow users to answer those questions, they must be able to re-create a data product, stopping at any step along the creation process to perform their own analysis.

To support this, a data provider should provide some reasonable mechanism for recreation. Some potential options include a text file or script with the commands and information on the software and software version used to create the file or a step-by-step plain language description of the processing steps including citations for the tools used. When possible, links to source data in the PDS or elsewhere should be provided.

### Artificial Intelligence / Machine Learning Derived Data
Data derived in whole or in part using AI/ML techniques must be clearly labeled as such. When possible, the input data sets and model(s) used should be described. As with all data, qualitative and quantitative metadata are essential. When feasible, models and training data should be made available and linked in the data documentation.

### Data Interpolation
For derived data (e.g., DTMs, image mosaics, etc.), decisions made by the data producer to interpolate the data should document the method selected and the rationale. This supports user interpretation of the data and helps with traceability of data values within the product. 

### File Formats
- Data will have a Spatio-Temporal Asset Catalog ([STAC](https://www.google.com/search?client=safari&rls=en&q=spatio-temporal+asset+catalog&ie=UTF-8&oe=UTF-8)) metadata JSON file.
- Data can have an [ISO-compliant XML metadata](https://wiki.icaci.org/index.php?title=ISO_19157:2013_Geographic_information_-_Data_quality) file](https://wiki.icaci.org/index.php?title=ISO_19157:2013_Geographic_information_-_Data_quality). This file is to be as compliant as possible and should use the planetary domain extension.

### Data Linkages and Unique Identifiers
- For data derived from archived sources (e.g., the PDS, JAXA DARTS, ESA PSA), linkages back to the source data should be provided. When combined with the provenance files, this allows users to recreate products from source files, reproducing or modifying the processing pipeline as desired.
- Data not easily derived from lower-level data should include a unique identifier (e.g., a DOI).
- Linkages to a primary, peer-reviewed, science publication should be provided when possible.
- Linkags to superseded datasets should be provided when the releasing data would supersede a previously released data set. Ideally, this linkage is by-directional. 

### Discussion

{{< comments >}}

[^1] If a DOI is not available, consider asking the archive to mint a DOI for you to best track data provenance.
