We use the `DATS.json` file format to store metadata describing CONP datasets.  `DATS.json` is a flexible machine-readable structure allowing for sophisticated representation of a wide range of different types of datasets, from neuroimaging to genomics. A `DATS.json` file must be prepared for each dataset.  The information will be used to create your resource landing page on the CONP portal and will help other users to find your dataset.  The table below summarises required, recommended and optional fields. 


| | |
|-|-|
|title|**REQUIRED**. The name of the dataset, usually one sentence or short description of the dataset. The title needs to be short and easily recognizable and searchable. If an acronym, please also provide the long name.|
|creators|**REQUIRED**. The person(s) or organization(s) which contributed to the creation of the dataset. This can be the principal investigator, hospital, university, centre, clinic, etc. If no other contact is provided this will be the main contact for this dataset.|
|description|**REQUIRED**. A short paragraph providing a rapid overview of the dataset and the context of data collection. Suggestion of items to include in the description (if applicable): main use of the dataset, population studied, study design, sample size, data collected, methods, techniques, apparatus used to generate the data.|
|types|**REQUIRED**. Terms to describe the nature of the data. Data type can be single or multiple. Add a term with the [interlex URI](https://neuinfo.org/interlex/dashboard) if possible.| 
|version|**REQUIRED**. Provide the version number, or the release point of your dataset.|
|licenses|**REQUIRED**. The use of license name abbreviations is suggested for specifying a license. Please visit [Creative Commons](https://creativecommons.org/share-your-work/) to choose the right licence for you.|
|keywords|**REQUIRED**. Tags associated with the dataset, which will help in its discovery. We suggest entering at least 5 keywords, different from the datatype.|
|distributions - format|**REQUIRED**. Primary data files format (*example*: csv, nifti, txt, fasta).|
|distributions - size|**REQUIRED**. Total size of the dataset.|
|distributions - unit|**REQUIRED**. Unit in which the size is measured.(*example*: GB)|
|distributions - access - landingPage|**REQUIRED**. Web address where the original dataset can be found.|
|distributions - access - authorizations|Contains an array with a single entry for "value". This must be one of "public", "registered" or "private". When this field is absent the value will be treated as "public".|
|extraProperties - files|**REQUIRED**. Total number of files in the dataset.|
|extraProperties - subjects|**REQUIRED**. Total number of subjects constituting the dataset.|
|extraProperties - CONP_status|**REQUIRED**. Must contain one of the values "CONP", "Canadian" (for non-CONP datasets generated in Canada) or "external" (for all other datasets).| 
|extraProperties - derivedFrom|**IF** the dataset is a derived dataset, the URL of the dataset it is derived from is **REQUIRED**.  The original dataset must also be included as a submodule in the derived dataset.|
|extraProperties - parent_dataset_id|**IF** the dataset is a derived dataset, the parent dataset id (as specified in _conp_dataset/.gitmodules_) is **REQUIRED**.|
|primaryPublications|**RECOMMENDED**. The primary publication(s) associated with the dataset, usually describing how the dataset was produced.|
|dimensions|**RECOMMENDED**. The different dimensions (granular components) making up a dataset. Providing dimensions give more details about the data types.|
|identifier|**RECOMMENDED**. Primary identifier for the dataset. Provide a *Document Object Identifier (DOI)* if you have one.|
|extraProperties - contact|**RECOMMENDED**. Provide contact information (name, email, telephone) of the person responsible for the dataset.|
|extraProperties - logo|**RECOMMENDED**. Link to or provide a logo to display on your resource landing page.|
|creators - name - roles - value("Principal Investigator")|**RECOMMENDED** Indicate which of the creators is PI for this dataset.  May not be applicable in cases where the value of "creators" is an organisation rather than a person or list of people.|
|dates|**OPTIONAL**.  Relevant dates for the dataset. If you provide a date, it must come with a description of the date.|<!--will later choose from a pulldown list--> 
|citations|**OPTIONAL**.  Publication(s) citing this dataset.|
|citationCount|**OPTIONAL**. The number of publications that cite this dataset (enumerated in the citations property).|
|producedBy|**OPTIONAL**. Process which generated a given dataset.|
|isAbout|**OPTIONAL**. Entities (biological entity, taxonomic information, disease, molecular entity, anatomical part, treatment) associated with this dataset.|
|hasPart|**OPTIONAL**. A dataset that is a subset of this dataset; datasets declaring the 'hasPart' relationship are considered a collection of datasets.  The aggregation criteria should be included in the 'description' field.|
|acknowledges|**OPTIONAL**. Grant(s) which funded and supported the work reported by the dataset.|
|refinement|**OPTIONAL**. Qualifier describing the level of data processing of the dataset and its distributions.|
|aggregation|**OPTIONAL**. Qualifier indicating whether the entity represents an 'instance of a dataset' or a 'collection of datasets'.|
|spatialCoverage|**OPTIONAL**. The geographical extension and span covered by the dataset and its measured dimensions/variables.|

The DATS dataset schema can be found [here](https://github.com/CONP-PCNO/schema/blob/master/dataset_schema.json), and the `DATS.json` file from the visual-working-memory dataset [here](https://github.com/conpdatasets/ds001634/blob/master/DATS.json) can be used as a template. A graphic interface allowing users to fill in fields online is under development [here](https://dats-creator.herokuapp.com/).





