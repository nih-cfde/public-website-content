# The Common Fund Data Ecosystem’s Crosscut Metadata Model (CFDE C2M2)

## What is C2M2?
The [Crosscut Metadata Model (C2M2)](https://nih-cfde.org/product/c2m2-glossary/#user-content-c2m2) is a standard for describing biomedical experimental data. The C2M2 framework will enable the biomedical research community to perform powerful cross-dataset searches, custom aggregation of experimental data, and rigorous statistical analysis.

## Why do we need it?

There is an abundance of rich biological data in the world today that is almost impossible for researchers to find, share, and study.

Making data **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable (FAIR) is not an easy task. Data created through different studies and for different projects often do not share terms even when the underlying data types are identical.

> For example, when study A labels its tissue of origin data column as "tissue", study B labels the same column as "anatomy", and study C calls it "UBERON IDs", combining data from all three studies would require significant terminology expertise and cross-study collaboration.

Many datasets are also hidden away in isolated, niche data repositories making it extremely difficult to find and access unless you already know where to look.

The CFDE is working to make data FAIR by building a standardized way of linking related terms from different datasets to one another. The C2M2 model is that standard. Under this framework, terminologies will be consistent and clearly defined, and researchers will know how to find, access, combine and reuse all available datasets from across the Common Fund Programs.

## How does the model work?

The C2M2 model is akin to nested dolls with interconnected layers of increasing complexity built on top of one another.

**Level 0**

Level 0 is the smallest and least complex layer that comprises the most basic information of a dataset (e.g. file types and dataset sizes).
The basic information provided in Level 0 is openly searchable without requiring special access to protected data.

**Level 1**

Level 1 builds on the Level 0 layer by adding important biological information about each data point such as species, anatomical tissue, and experiment type. As with Level 0, Level 1 does not encompass protected data and can be accessed by everyone.


**Level 2**

At Level 2, additional complex biological data are added to the model including disease states, sex, and age of the individual the data is from.  


Ultimately our goal is to incorporate multiple Levels that capture all information necessary to comprehensively describe the data. However, this will require building controlled access capability into our infrastructure to protect the identities of patients. 


Using this C2M2 infrastructure, the Data Coordinating Centers ([DCCs](https://nih-cfde.org/product/c2m2-glossary/#user-content-dcc)) can share structured information ([metadata](https://nih-cfde.org/product/c2m2-glossary/#user-content-metadata)) about their experimental resources with the research community, dramatically widening access to usable observational data and accelerating discovery.



## How do data coordinators participate? 

The Data Coordinating Centers ([DCCs](https://nih-cfde.org/product/c2m2-glossary/#user-content-dcc)) from each Common Fund Program will collect metadata and format it by standardizing terms used to describe data. The format is specified to be easily readable by a computer, so that it can be loaded into a database. Researchers will then be able to search the database using a human readable web portal. 

> For the "tissue of origin" example, the formatting and standardization process might involve each study agreeing to adopt the term "anatomy" to describe tissue of origin, and consequently reformatting their individual data submission. 

Appropriately formatted datasets submitted to the CFDE will be integrated into C2M2. The CFDE software infrastructure will automatically validate submission format compliance and metadata integrity, and request changes from data submitter if necessary.


The general expectation is that the metadata submitted and managed by a DCC will transition, over time, through increasingly rich modeling levels as the life cycle of DCC/CFDE technical interaction progresses, which will enable increasingly powerful downstream applications.


## What can a researcher use the model levels for?

**Level 0 and Level 1:** Levels 0 and 1 consist entirely of unprotected metadata terms, and therefore likely to represent data from all Common Fund Programs. These two levels are sufficient to support two minimal [Use Cases](https://cfde-usecases.readthedocs-hosted.com/en/latest/use-cases/). 

**Level 1 and Level 2:** Using only the metadata from Levels 1 and 2, [a researcher can find datasets](https://cfde-usecases.readthedocs-hosted.com/en/latest/use-cases/uc0001-researcher-browse-and-filter/) from across the Common Fund that contain information about tissue of interest, assayed using a method of choice. Similarly, [staff at the NIH can compare the tissues, species and assay types available across DCCs](https://cfde-usecases.readthedocs-hosted.com/en/latest/use-cases/uc0003-monitor-data-releases-as-a-data-custodian/).

More complex Use Cases, such as the [ability for a researcher to find datasets for patients with a specific disease in a specific age range](https://cfde-usecases.readthedocs-hosted.com/en/latest/use-cases/uc0005-researcher-browse-and-filter-complex/) will require the Programs to submit protected metadata terms. However, this is a limitation of our current infrastructure which makes our access to protected data illegal, and will be solved in the near future. 
