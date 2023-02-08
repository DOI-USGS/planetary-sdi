---
title: Metadata Standards
weight: 70
---

**DRAFT**

### Licensing
- Data should be licensed using the open [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/) license. When allowable by the funding agency, data may also be licensed using [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/), thereby requiring attribution, or [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) thereby requiring attribution and including a share-alike clause requiring derived products to adopt the same license.
### Metadata Content
- Data will have qualitative process and usability information available in text format that describes (1) a description of the data set, (2) the process used to create the data, (3) the available assets or files within a data set, (4) the accuracy, errors, and identification of known issues with the data set, (5) the qualitative usability of the data set (as mediated by the data provider or steward), (6) textual description of the proposed update cadence for this data set, and (7) optionally textual links to other data sets of potential interest to users of this data set.

### Accuracy Descriptions
- Accuracy should be described using the [ISO 19157:2013 standard](https://wiki.icaci.org/index.php?title=ISO_19157:2013_Geographic_information_-_Data_quality). 

### File Formats
- Data will have an [ISO compliant XML metadata file](https://wiki.icaci.org/index.php?title=ISO_19157:2013_Geographic_information_-_Data_quality). This file is to be as compliant as possible and should use the planetary domain extension.
- Data will have a Spatio-Temporal Asset Catalog ([STAC](https://www.google.com/search?client=safari&rls=en&q=spatio-temporal+asset+catalog&ie=UTF-8&oe=UTF-8)) metadata JSON file.
- Data should have a provenance file that minimally describes the creation of the data. When possible, the provenance file will support complete reproduction of a derived data product by replicating commands provided to processing tools.

### Data Linkages and Unique Identifiers
- Data derived from lower level data, stored in a long term archive, linkages back to the source data should be provided[^1].
- Data not easily derived from lower level data should include a unique identifier (e.g., a DOI).

[^1]: Combined with the provenance files, this allows users to recreate products from source files, reproducing or modifying the processing pipeline as desired.