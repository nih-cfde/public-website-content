Table of Contents:  
[Metabolomics Site Visit](#user-content-metabolomics-site-visit)  
[Metabolomics Overview](#user-content-metabolomics-overview)  
[Program Lifestage](#user-content-program-lifestage)  
[Data Platform](#user-content-data-platform)  
[Harmonization and Metadata](#user-content-harmonization-and-metadata)  
[Sustainability](#user-content-sustainability)  
[Training](#user-content-training)  
[FAIR](#user-content-fair)  
[Cross-pollination](#user-content-cross-pollination)  
[SSO (Single Sign-on)](#user-content-sso-single-sign-on)  
[Outcomes](#user-content-outcomes)  
[Agenda](#user-content-agenda)  
  
### Metabolomics Site Visit
**Location:** University of San Diego, Bioengineering Building, 9500 Gilman Drive, La Jolla, CA  
  
**Date:** Wednesday-Thursday, November 13-14, 2019  
  
**Attendees:** Representatives in attendance from the CFDE were Amanda Charbonneau (UCD), Meisha Mandal (RTI), Titus Brown (UCD), and Owen White (UMB). The representatives from Metabolomics were Shankar Subramaniam (PI), Eoin Fahy (Senior Scientist), Kenan Azam (Scientific Programmer), and Andrew Caldwell (Research Scientist). Manish Sud (Lead Research Analyst) was not able to attend the meeting. Two representatives from the San Diego Supercomputer Center (SDSC): Christine Kirkpatrick (Executive Director) and Kevin Coakley (Senior Systems and Cloud Integration Engineer).  
  
#### Meeting Logistics
The CFDE engagement team met with representatives of the Common Fund’s Metabolomics program on Wednesday, November 13, 2019 and Thursday, November 14, 2019 in the lab of Dr. Shankar Subramaniam at the University of California, San Diego (UCSD) to discuss the Common Fund’s ongoing Metabolomics program headed by Dr. Subramaniam. The agenda at the end of this document was used as an informal guide for structuring the day.  
  
After brief introductions, the engagement team and Metabolomics representatives, each reviewed their goals for the meeting. For the engagement team, these goals include learning about the structure and goals of Metabolomics, including technical specifications about the data they host, as well as information about training, organization, and the overall set of priorities for their group. For Metabolomics, these goals included discussing data integration as well as metadata, ontologies, and harmonization. In turn, our hosts provided us with an overview of their Metabolomics Workbench site, including descriptions of the studies involved and types of data generated, online data submission process, data sharing/harmonization, data analysis, and a live demonstration of their portal.  
  
### Metabolomics Overview
The Common Fund’s Metabolomics program aims to stimulate metabolomics research and to expand the capacity of researchers to study small molecules and their relationship to human disease. While the field of metabolomics research is several decades old, it has lagged behind other biomedical fields in terms of popularity and ease of use. Processing metabolomic data requires the use of specialized equipment (NMR, mass spectrometry, liquid chromatography) and requires expert users for both the technical machine aspects and the first pass data analysis. The Metabolomics program represents a dedicated effort to bring metabolite screens into more widespread use by working to standardize methods, compound names, and analysis tools, thereby lowering the barrier to entry for researchers.  
  
The Metabolomics Program was funded in two unequal stages. They are currently halfway through their second phase and the consortium consists of six Regional Comprehensive Metabolomics Resource Cores (RCMRCs), sometimes also called the Compound Identification Cores (CIDCs), and seven Data and Tools Cores (DTCs) that are overseen by the Metabolomics Consortium Coordinating Center at the University of Florida. See below for a table summarizing the roles and member organizations for the Metabolomics centers.  
  
The creators of the National Metabolomics Data Repository (NMDR), who hosted our visit, are responsible for collating, analyzing, and distributing the data gathered by the RCMRCs and hosting the tools and methods created by the DTCs. For the first six years of Metabolomics funding, there were also three training centers, however dedicated training centers were dropped for the second phase of funding.  
  
Data, including associated metadata, for the Metabolomics program are hosted by the NMDR. The NMDR contains data from 11 major taxonomic categories that are generated through both targeted (focused on a set of defined metabolites) and non-targeted (covering the entire metabolome, including unknown metabolites) metabolomic assays. Currently, the NMDR contains ~1200 studies from ~200 different institutions worldwide. It is dominated by human data, but a considerable portion is from mice and other mammalian species.  
  
|Center|Member Organization(s)|Responsibilities|
|:-|:-|:-|
|Metabolomics Workbench/NMDR|1. UC San Diego|Collate, analyze, and distribute data generated by RCMRCs. Host tools and methods created by DTCs.|
|Metabolomics Consortium Coordinating Center (M3C)|1. U. of Florida|Coordinate activities across Metabolomics centers and promote the work of the Consortium.|
|Regional Comprehensive Metabolomics Resource Cores (RCMRCs)|1. U. of Georgia<br>2. U. of Michigan<br>3. UC Davis<br>4. Emory University<br>5. Pacific Northwest Nat. Lab.|Develop processes and resources to facilitate and improve the accuracy of metabolite identification.|
|Data and Tools Cores (DTCs)|1. MD Anderson Cancer C.<br>2. Vanderbilt University<br>3. U. of North Carolina Charlotte<br>4. Emory University<br>5. U. of Michigan<br>6. U. of Colorado, Denver<br>7. U. at St. Louis|Develop methods and computational tools to facilitate the collection, processing, and analysis of metabolomics data.|  
  
### Program Lifestage
The Metabolomics program was initially funded in 2012 and has been receiving data submissions since March 2013. The program wrapped up the first stage (six years) of funding in FY17 and is currently in the second stage, which spans FY18-FY21. As the program has matured, its database has come to include diverse data sources and the NMDR has become a hub of their community. Early in the program, starting in June 2015, the NMDR additionally began accepting data from a variety of sources outside of their consortium as well as aggregating data from their RCMRCs. Currently, of the ~1200 studies in their database, about 150 were deposited by NIH-funded programs or consortia. The rest were submitted by non-NIH-funded institutions—over 900 came from within the US, and a further 100 were international submissions. Similarly, their analytical chemistry-centric effort to standardize molecule names, RefMet, the “**Ref**erence list of **Met**abolite names” is an international effort, and its governing board has eight international experts. They also developed mwTab, a standardized format for sharing metabolite data and metadata in a single file. The mwTab format is now widely used, and is the backbone of the MetabolomeXchange, an index of metabolomics data used by five countries.  
  
### Data Platform
The Common Fund Metabolomics program developed and maintains the Metabolomics Workbench (MW), the Metabolomics Workbench Metabolite Database, the Human Metabolome Gene/Protein Database (MGP), and the Reference list of Metabolite names (RefMet).  
  
The Metabolomics Workbench (MW), <https://www.metabolomicsworkbench.org>, is an online interface to the NMDR developed at UCSD. It allows users to manage and upload studies as well as browse and search available studies. Using the MW interface, submitters upload data and results, including metadata, targeted data measurements, protocols/methods files, untargeted data measurements, and raw data (MS/NMR files, etc.). Other researchers can then use the MW website to browse, search, analyze, and download data as well as view summary figures of key study search parameters (e.g., bubble chart showing studies by sample source). For example, studies can be filtered by study metadata (disease, sample source, species, instrumentation) or metabolite information (metabolite classification, biochemical pathways, retention time, etc.) to identify data relevant to the user’s needs. Additionally, it provides analysis tools and access to metabolite standards, protocols, tutorials, training, and other resources to support metabolomic researchers.  
  
The MW analysis offerings include normalization/averaging, clustering/correlation, univariate analysis, multivariate analysis, feature analysis, classification, and comparative analysis across studies. Users can also programmatically query and access data (metabolite structures, metadata, experimental results) through the MW REST API \(<https://www.metabolomicsworkbench.org/tools/mw_rest.php>\) using HTTP requests in a browser, script or third-party application. The REST API was released last April and was developed in collaboration with the Scripps Research Institute.  
  
The Metabolomics Workbench Metabolite Database is a Postgres database containing over 65,000 structures and annotations of biologically relevant metabolites collected from public repositories (e.g., LIPID MAPS, ChEBI, HMDB, BMRB, PubChem, KEGG). Users can search for metabolites in the database by substructure, text, or mass (m/z ratio). Each entry contains key information about the metabolite, including structure, molecular weight, common and systematic names, PubChem compound ID, and classification. Entries also contain cross references to external databases and repositories (e.g., HMDB, ChEBI, LIPID MAPS, METLIN, ChemSpider, KEGG, etc.) as well as links to the MoNA MS spectra and human metabolic pathways containing the metabolite. Additionally, the open-source chemistry cartridge enables substructure searching, generation of chemistry-centric attributes (formula, exact mass), and interconversion of molecular formats.  
  
The Human Metabolome Gene/Protein Database (MGP) is a database of metabolome-related genes and proteins containing over 7,300 genes and over 15,500 proteins. Users can search by gene (name, symbol, entrez ID, etc.), HMDB Pathway, or Reactome Pathway. MGP displays genes/proteins and metabolites associated with a pathway of interest. Searching by gene displays information about the gene’s associated proteins and pathways, including a summary of the function and metabolites involved in the pathway.  
  
The **Ref**erence list of **Met**abolite names, RefMet, is effectively a large spreadsheet that provides a standard nomenclature for over 95,500 chemical species. Users can interact with RefMet in a number of ways. From the Metabolomics Workbench website, it can be browsed and searched directly or a user can input a list of metabolite names and have them automatically converted to RefMet nomenclature. A user can also directly download the data, either in whole or after filtering as one would with a simple Excel sheet. Or the entire dataset can be downloaded as part of a Shiny R app and queried locally.  
  
#### Infrastructure
The NIH Common Fund Metabolomics program runs entirely on cloud platforms, with some caveats. They have taken advantage of STRIDES and have worked to integrate that billing system into their project to pay for data storage; however, they are also part of a cloud computing collaboration with the San Diego Supercomputer Center. Their Workbench platform is hosted on an internal cloud system at UCSD. Their cloud-based workbench and cloud-hosted notebooks are on Google Cloud Platform (GCP). Analysis tools are in Docker containers running Jupyter notebooks and utilize both R and Python modules. The public can access the notebooks through binder, a free service that hosts Jupyter notebooks (mybinder.org). Jupyter files can be copied to a local installation for private access.  
  
#### Analysis
The MW offers a number of data analysis tools, including a study-specific analysis toolbox accessible from the main study page. The analysis workflows use common R statistics packages that have been integrated into embedded R Shiny modules. Users can run a wide range of statistical analyses on the workbench using data hosted in the NMDR. As the pipelines are built entirely of standard R packages, a user could technically re-implement the pipeline locally, however this would be difficult for a novice user. In creating the toolchains encoded by the Shiny modules the Metabolomics group has made a number of decisions about parameters and defaults that are not transparent to the user. This makes the Shiny apps extremely easy to use, but not straightforward to recreate. A user wishing to run the same pipeline locally would need to create the code that strings the various tools together, as well as set a number of parameter options. However, users can analyze their own data on the workbench site using the pre-standardized pipelines by uploading a tab or comma delimited file. Once uploaded, the user is presented with a Shiny interface where they can set several useful options such as defining sample groupings, choosing which experimental factors to include, and what normalization method should be used to ensure that the data is analyzed correctly. For most users, who have only one or two datasets to analyze at a time, uploading their data to the site and using the point and click interface is likely preferable to local reimplementation.  
  
Many of the individual analysis tools as well as the ability to search RefMet have also been ported to Python, and can be run in Jupyter notebooks using binder or could be downloaded and run in a local Jupyter notebook. These are all available at the Metabolomics Workbench GitHub page: <https://github.com/metabolomicsworkbench>. These tools are still actively being ported, and are not yet as user friendly as the Shiny R apps embedded in the MW. As of this writing, the Jupyter notebooks are designed as examples of the tool, and do not have instructions for how to edit the code to use other data. As such, an end user would need to be familiar with Python to use them.  
  
#### Access
Uploaded data are publicly accessible via the MW’s web portal or API. Unlike any other DCC we’ve visited, an end user at Metabolomics can access both raw and processed mass spectrometry (MS), nuclear magnetic resonance (NMR) and related files. There is also open access to all available metadata, protocols, and methods for both targeted and untargeted studies. Users also have free access to a variety of browsing, searching, and statistical analysis tools, can upload their own data for processing, and can download any of the files in a variety of formats. All of these data, features and tools can be accessed by any user, without a log-in.  
  
Data creators are similarly unrestricted. The NMDR welcomes data from any source as long as it is a metabolite analysis file, is submitted with the required metadata, and passes their review process. To facilitate the review process, data creators are required to create an account to obtain authorization. Authorization requests are reviewed by the MW staff and are typically approved within five business days. Once authorization is obtained, researchers need to register their study prior to uploading data. A step-by-step tutorial is available to assist researchers in the data submission process. Once the study is submitted, NMDR reviews the uploaded dataset, which typically takes less than 30 days. After the NMDR review process is completed the submitter is notified and may review their uploaded data. After the entire review process is completed, the study is made available on the public MW website. During the submission process, submitters can set an embargo if the study has not yet been published and can lift the embargo after publication to allow access to the data. At the time of our meeting, approximately 180 submitted studies were under embargo.  
  
### Harmonization and Metadata
The Metabolomics program has invested heavily in data/metadata harmonization efforts, most notably with the development and maintenance of a reference list of metabolite names and a new file format (mwTab). However, they warned that metabolomic data will always be difficult to combine across studies as results can vary widely due to differences in machine or operator. For instance, Dr. Subramaniam’s group ran a “ringtest” where they sent the same samples to multiple cores for analysis. In many cases the results from different cores had significant variation suggesting that even properly harmonized data might be difficult to re-combine with other studies. Still, resources such as mwTab and RefMet have greatly increased our ability to cross-reference study data, and have made data portable across platforms.  
  
The Metabolomics program developed the **Ref**erence list of **Met**abolite Names (RefMet) as a way to standardize metabolite names across studies and experiments. Depending on the instrument used to identify molecules (e.g. nuclear magnetic resonance (NMR), mass spectrometry), the method used to separate fragment and separate metabolites (e.g. mass spectrometry (MS), liquid chromatography (LC), time of flight (TOF), etc), and the electric charge of the substrate used to separate them, the same starting metabolite will be discovered as one of many different breakdown products across experiments. For this reason, metabolites can often be accurately referred to by multiple different names in the literature. This makes it exceedingly difficult to determine whether any two studies found the same metabolic compounds unless they used exactly the same methods. To create RefMet, the NMDR recorded ~220,000 variable metabolite names from across ~1200 MS and NMR studies. By mapping all the variations in metabolite names to standard RefMet designations, the NMDR was able to collapse most (about 200,000) of the variable names into 95,000 standardized metabolite species.

RefMet is a huge international effort. The database is entirely human curated, and the work is governed by a board consisting of eight international experts in metabolomics, including collaborators like PubChem. Users submitting data to the NMDR are strongly encouraged to use common metabolite names from RefMet in uploaded data. An online tool to map current metabolite identifications to corresponding RefMet species in metabolomic data is available to assist with this process via the MW.  

Another data harmonization effort undertaken by the Metabolomics program is the creation of the [mwTab file format](https://www.metabolomicsworkbench.org/data/mwTab_specification.pdf). It was designed to serve as a “common currency” for sharing all of the relevant metadata and data from an experiment in a single file, for any metabolomic assay, and is the basis of the NMDR data repository, as shown in their online data/metadata submission flowchart below. The format is both machine and human readable, and very flexible. It contains sections for high level metadata such as project information, PI contact and publication information, as well as more standard metadata (e.g. sample collection, treatment, sample preparation, analysis).The data section of the file is broken into a number of optional data blocks, so a single file can accommodate any combination of methods. Each data block has a number of standardized, optional, fields which correspond to every possible setting for various instruments. A third section allows for mostly freeform additional comments. Since the format is machine readable it can be read by all R based tools, and since it includes all relevant metadata, it can be automatically ingested into the NMDR as part of data submission.  
  
![online data metadata submission flowchart](https://github.com/nih-cfde/public-website-content/blob/master/images/metabolomics-data-flowchart.jpg)  
  
Since its creation, the mwTab format has become popular in the field, and is the file format used by the MetabolomeXchange, an international data aggregation and notification service for metabolomics. The MetabolomeXchange was originally funded by the European Commission-funded COSMOS project, and is used by five countries. The site indexes metabolomics data with mwTab and connects a number of metabolomics data repositories across Europe and the USA. The MetabolomeXchange also provides an [API](http://api.metabolomexchange.org/) which can translate mwTab into several other formats. In effect, all data in the MetabolomeXchange, as well as any data that is properly formatted into an mwTab file, is automatically harmonized with all of the data at Metabolomics and can instantly be used in any of their tools.  
  
In addition to developing mwTab format and RefMet, the Metabolomics group encourages and facilitates data harmonization in other ways such as through the use external standards whenever possible. The NMDR has developed a metadata model to support large scale human studies in the Metabolomics Workbench. The model, shown here, was made in consultation with TOPMED, MoTrPAC, CHEAR and the European Bioinformatics Institute:  
  
![metadata model chart](https://github.com/nih-cfde/public-website-content/blob/master/images/metabolomics-data-model.jpg)  
  
Note that although the Unique Identifier contains a number of clinical variables, all human data in the MW is completely de-identified.  
  
### Sustainability
As the Metabolomics program plays a central role in international efforts to standardize and popularize metabolomic research, they have begun to make plans to ensure their work survives the projected end of Common Fund funding. For RefMet, they are hoping to involve some other institute in sustaining the effort. The National Institute of Diabetes and Digestive and Kidney Diseases (NIDDK) has indicated interest, however there is currently no guarantee that funding will appear. The NMDR is actively in talks with NIDDK to explore ways to continue funding, but are also interested in other opportunities if they become available. Due to its integration with the MetabolomeXchange, it seems likely any required maintenance will be tied to that effort.  
  
The fate of the Metabolomics Workbench, the portal that allows end users to access and analyze NMDRs data, is less certain. All of the pipelines for the project are in Docker containers or other similar shareable systems. The idea is to provide everything in a way that lets sophisticated users do their analysis, and lets companies (the machine creators) engage with the software and tools they’ve built. However, the widespread popularity of the workbench, paradoxically, makes it more difficult to find an Institutional Center or other organization to fund it. Dr. Subramaniam has a long history of obtaining funding for projects in systems biology and metabolomics and is pursuing alternative sources of funding for the Metabolomics program after the FY18-FY21 funding period ends.  
  
### Training
#### Internal
Currently, all training and nearly all help requests that occur at the NMDR are related to data submission; primarily on how to create and properly format mwTab files. The team at UCSC has created a [detailed format specification](https://www.metabolomicsworkbench.org/data/mwTab_specification.pdf) and has developed some training materials which they occasionally offer as workshops, however the bulk of their interaction with these users is one-on-one: when a data creator is trying to format their mwTab file, they contact the NMDR for help and advice, or the NMDR reaches out to investigators who have submitted an ill-formatted document. They field approximately 100 queries per day, almost all of which are related to data submission, often from users submitting to the NMDR for the first time.  
  
#### External
The MW site has a high volume of traffic, mainly from users querying the metabolite and RefMet databases, or using the statistical analysis tools. Remarkably, they report having almost no support burden from end users despite having over 270,000 page views per year. The NMDR team told us that this is where they would most like to expand their training efforts. They are very interested in reaching out to end users, finding out what they’re doing with the data, and offering training or help to increase data use. Currently, the only training the NMDR offers end users is [written documentation](https://www.metabolomicsworkbench.org/data/tutorials/DRCCOnlineBrowsingAndToolsTutorial.pdf) on using the search and analysis features. The NMDR indicated that they are very interested in getting assistance from the CFDE with training, and engaging end users to incorporate NMDR data into larger studies. In stage 1 of the Metabolomics project, two groups in the consortium had funding allocated specifically for training. However, in stage 2, no groups are solely tasked with training, and there is no substantial funding allocated to training efforts. The Metabolomics Consortium Coordinating Center (M3C) at the University of Florida, which handles overall coordination for the Metabolomics program, does host end user trainings. However, these are typically broader training on metabolomics experimental techniques and data analysis. At the time of our visit, 15 training workshops, courses, and conferences were scheduled from January 2020 to November 2020 and ranged in length from two days to several weeks. The events have costs ranging from free (one event) to $5,000, typically have ~100 attendees and are live-tweeted. They are generally organized by the various centers of the Metabolomics program but also include links to training efforts outside the consortium such as at Birmingham Metabolomics Training Centre, and The Association for Mass Spectrometry.  
  
### FAIR
The NMDR team is committed to making their data FAIR, and has made great strides in improving the FAIRness of metabolomic data, both in their own database and across the field. RefMet, their database for standardizing metabolite names, increases the Findability of data, and allows researchers to Find and Reuse datasets that might be Interoperable. mwTab, their file format specification, makes all of the data at the NMDR at least technically Interoperable with any other data in that format. As mwTab is used by metabolomic data repositories in six countries, this represents a huge proportion of available data. The format is documented at <fairsharing.org>  
  
Data at the NMDR also has a number of basic FAIR features. For instance, metadata is formatted using Schema.org which allows it to be found and indexed by search engines, and DOIs assigned to each submitted dataset study. The Metabolomics Workbench website is completely open access. Raw and processed data can be searched, analyzed and downloaded in a variety of formats, without a login, making all of the data freely Findable and Accessible. Additionally, all metabolomic data and RefMet information can be programmatically accessed via an API. Users can also Reuse any of the NMDR tools on their own uploaded data either on the MW website, or using Dockerized versions.  
  
The NMDR staff did express some frustration with current efforts to measure FAIRness. They told us that rubrics developed to test FAIRness are generally not designed by people who implement FAIR principles. This means that the priorities of the data maintainers and the constraints they face when implementing FAIR are often not accounted for. This mismatch between the reality of data managers and the goals of FAIR rubric creators sometimes results in metrics that can’t be satisfied, and other times in metrics that are easy to meet, but don’t actually materially improve the FAIRness of the data.  
  
### Cross-pollination
The members of the Metabolomics NMDR are highly supportive of cross-pollination between Common Fund Programs and are already involved in a number of collaborations with major metabolomics data-producing entities. At the direction of NIH they have ongoing collaborations with MoTrPAC and TOPMed. However, there is no funding specifically allocated to support these efforts. In addition to their previously mentioned RefMet and mwTab work, the Metabolomics program also collaborates with the Children’s Health Exposure Analysis Resource \(<https://cheardatacenter.mssm.edu/>\) at the Icahn School of Medicine at Mount Sinai. They also have a strong collaboration with LIPID MAPS. Notably, ~65% of all the studies on the MW relate to lipids.  
  
### SSO (Single Sign-on)
The NMDR does not use an SSO service, and only requires a login for certain users. Data generators are required to create a log-in and register before they can submit data. New data submitters are manually screened before being authorized for access. Submitters are responsible for cleaning their data prior to uploading it in accordance with Federal Health Insurance Privacy and Portability Act (HIPAA) requirements. In particular, human data must be de-identified, with patient IDs and any other personally identifiable information removed. As no private data is in the portal, end users are not required to create an account or log in to the MW in order to download or access data, or to use tools.  
  
As data upload is only permitted by people with an account, and other users do not currently require a login, moving the workbench to a SSO system would require several large changes to their workflow while making access more difficult for end users.  
  
### Outcomes
#### Infrastructure and Resource Reuse
The MW tools are, by design, highly reusable, and will work on any data that is coerced into the mwTab format. Additionally, they have ported the R pipeline to Python based Docker containers that could be easily reused by other programs with similar data types. The mwTab format created by the Metabolomics group also contributes significantly to the MW platform’s reusability. Any data in mwTab format, independent of the data’s source, can be submitted to the MW and analyzed using the available tools.  
  
Dr. Subramaniam has a wide breadth of knowledge about other Common Fund programs. He is an advisor for TOPMed, LINCS, and MoTrPac. Over the course of two days, he related several potential Use Cases ‘Horizontal Integrations’ that could be completed with various collaborations, explained how to create a matrix view of Common Fund datasets that could be used to identify new potential collaborations, and presented a way to structure all Common Fund data into a nested ontology. Dr. Subramaniam and his lab were clearly thinking deeply about both the theoretical and practical aspects of building a Common Fund Data Ecosystem long before we arrived, and their help will be invaluable for community building within the CFDE.  
  
#### Challenges
During the meeting the Metabolomics NMDR team identified a number of challenges it is currently facing or anticipates facing in the future.   
  
*Unfunded Mandates.* One challenge is the lack of funding for collaboration efforts. For example, the collaborations between Metabolomics and MoTrPAC, and Metabolomics and TOPMed have been directed by NIH, however no specific funding has been allocated to collaboration efforts. Any time dedicated to collaboration, such as the time required to convert data into shareable formats or standardize names using RefMet, must be absorbed by the Programs. Similarly, projects are often required or expected to host training, but with little or no support. Although two groups were allocated funds specifically for training in the first stage of the project, there are no centers with funding solely for training in-specific funds for stage 2.  
  
*Researcher Focus.* Metabolomics researchers tend to be “islands” and stick to metabolomic or lipidomic studies as opposed to multi-omic or other cross-discipline studies. This is not unique to metabolomics researchers: researchers in other areas rarely think about using metabolomics.  
  
*Barriers to Training Access.* One reason that metabolomics data is underutilized is that the data can only be collected on specialized equipment that is often restricted to only expert users, and analyzing that data requires specialized knowledge that is difficult to acquire and has a steep learning curve. Researchers generally learn by being in a lab that already does metabolite work, but for an outsider, there are few ways to get even a cursory overview of what metabolomics is, or to learn why a researcher might want to start incorporating that kind of data into their experiments. Christine Kirkpatrick lamented that after an exhaustive search, she couldn’t find a single example of metabolomic non-fiction. The closest she could find to an intro on the topic for a novice was a book chapter written by Eoin Fahy. There are training workshops and other events about metabolomics, however they are costly, aimed at people who already do metabolite research, and not broad enough. For example, a ‘Best practice in operating mass spectrometers in Metabolomics’ workshop, offered by the West Coast Metabolomics Center is a beginner course, but teaches only how to run a single machine, with no data analysis or practical application. Registration is also $1500 and the course is a four day commitment, an amount of time and money that would likely deter a researcher who simply wants to see if it makes sense to add metabolomics to their skillset.  
    
*STRIDES.* The NMDR team shared that although they are happy with their STRIDES collaboration, they are concerned about how the program might be affected by the conflicting goals of the NIH and commercial interests. They noted that the cloud providers are often the ones writing the policies and that the administrators at the NIH who are brokering the deal may not appreciate their long-term consequences. For instance, part of the STRIDES discount is made by putting most of the user support burden on the CF Programs. This means that a DCC will be responsible for answering questions not just about their own data and pipelines, but about the cloud infrastructure and other things that would normally have been answered by the cloud provider. The savings from the discount, however, are unlikely to make up for the increased support burden at DCCs.  
    
#### Potential Solutions
We also discussed a number of ways in which the CFDE could offer support to help address some of the challenges faced by the Metabolomics program.  
  
*Funding More Cross-talk between Groups and Researchers.* In addition, the CFDE plan to fund new collaborations, funding could also go towards activities such as expanding existing collaborations. These efforts could include other data-generating organizations or outreach aimed at metabolomics researchers to encourage the use of standard formats/naming or other data harmonization efforts.  
  
Another potential direction would be funding projects specifically aimed at increasing cross-collaboration. This could be an initiative similar to the NSF Convergence Accelerator \(<https://www.nsf.gov/od/oia/convergence-accelerator/index.jsp>\) which specifically funds projects with a convergent approach to promote interdisciplinary collaborations.  
  
*Training and Community Building.* The CFDE could help with two main training efforts: training for existing users, and outreach to broaden the use of metabolite data. 
* Expanding Metabolomics Workbench-specific training for data submission and mwTab format would help reduce the user support burden. Currently, the NMDR gets about 100 requests per day for help with data submission.  
  
Outreach efforts aimed at researchers outside the metabolomics community to encourage the broader use of metabolite data. This requires outreach and education about the basics of metabolomics techniques and analysis, as well as examples of how this kind of data can enhance experiments. A number of ideas were discussed for specific training workshops that the CFDE could offer. Of note, Christine Kirkpatrick stated that she has a pool of people that might be able to organize and lead CFDE trainings.  
* Introducing metabolomics with a focus on topics of public interest to engage participants. One possibility is a ‘What are metabolomics and metabolite signatures good for’ workshop. Potential topics:  
  * Analysis of metabolites in blood/urine/saliva for non-invasive disease diagnosis. 
  * How do specific pharmaceutical drugs alter the metabolome? Look for deviations from homeostasis and effects in other metabolites beyond the expected direct targets of the drug. 
  * How does the environment alter our metabolism (exposome)? 
  * Interrogate tissue specific metabolism.
  * Interaction of metabolomics with gene expression and other biological processes.
* Novice friendly training workshop in metabolomics. This could be an ANGUS-affiliated workshop or hackathon covering:
  * Processing and analysis of metabolomic data
  * How to use mass spec data
  * Naming of metabolites
  * Connecting metabolites to functions and pathways
  * Common pitfalls in metabolomics research
* A “data storytelling” workshop to train current experts in metabolomics how to effectively communicate their findings and research to be interesting to a broader audience. 
  * This could be combined with a storytelling workshop and evening where NIH program managers are invited to hear researchers present their stories. This would allow NIH to hear about the impact of the CFDE through users instead of the CFDE.
* An ‘Opportunities and Challenges of Metabolomics” workshop or hackathon.
  * This could be done as a collaboration between MoTrPAC and Metabolomics. 
  * Ideas for workshop topics:
    * Materials development/brainstorming workshop around data integration with other data types.
    * Bring your own data and learn how to intersect it with metabolomics data. 
    * An exercise incorporating metabolomics into published research.  
  
*Infrastructure and Data Reuse.* In order to increase reusability, the CFDE could support an effort to standardize metabolomics data and have other DCCs routinely use RefMet and mwTab format. This would be facilitated by making an API that can directly translate mwTab into a C2M2 compatible format.  
    
#### Potential Projects
As previously noted, the NMDR is already engaged in a number of efforts across funding institutions and nations, and is actively working to create new collaborations with MoTrPAC and TOPMed.    
  
#### Game Changers
*Crowdsourcing Data Harmonization Use Cases.* Dr. Subramaniam and the Metabolomics team had many intriguing ideas for crowdsourcing use cases. Some of the ideas discussed were:
* Developing a platform where PIs can submit ideas for use cases. NIH funded postdoc positions would be dedicated to working closely with the relevant DCCs on implementing these use cases. One goal would be to make the analysis reusable for use in future projects.
* Presenting researchers with a matrix of Common Fund datasets and collecting ideas for use cases involving the data as well as developing a platform to match them with postdocs that could help implement their ideas.
  * One way to implement this would be to bring together a group of bioinformaticians and clinical researchers to discuss what types of data are available in the common fund. 
* Have a 30-minute presentation at an IC council meeting by the CFDE providing a matrix of the types of data available in the Common Fund to researchers in a variety of research areas (HLB, diabetes, etc.). Ask researchers to think of use case scenarios that would be useful in advancing their research.  
  
*Common Fund 10 Big Ideas.* Similar to the NSF 10 Big Ideas, create a collection of topics for CF DCCs to coalesce their collaborations around.  
  
*Informatics-specific Funding.* We live in a data world. Doing good science depends on having reliable, accessible, well managed data, but the NIH rarely dedicates money to data. NIH Institutes don’t have a specific line item for data science, data management or informatics, and so money often ends up being used for the science, at the expense of the data. The CFDE could advocate for the NIH to allocate funding specifically for data management, data science and informatics at a high level, i.e. having a certain portion of the NIH budget dedicated to it. This is being done elsewhere in other federal agencies., NASA, for example, has a percentage of their funding that goes specifically to data management.  
  
*Innovative ways to view Common Funds Data Portfolio.* Dr. Subramaniam suggested several ways to condense and contextualize the varied datasets at the Common Fund so that a Program Officer or PI at a program could easily determine how their project fits into the overall portfolio, and who might be good targets for collaboration. For instance, the CFDE could create a matrix view of datasets, where programs could be easily compared by the data types, biological systems, or other useful terms that describe their work. He further suggested that one could imagine the Common Fund portfolio in terms of nested hierarchies describing the assets. At a very high level, data could be grouped according to its structure:  
  
![structure grouping flow chart](https://github.com/nih-cfde/public-website-content/blob/master/images/metabolomics-data-hierarchies-1.jpg)  
  
Data might be conceptually categorized by aspects of the technology and protocol used to create it:  
  
![protocol grouping flow chart](https://github.com/nih-cfde/public-website-content/blob/master/images/metabolomics-data-hierarchies-2.jpg)  
  
Or by its scientifically interesting properties:  
  
![scientifically interesting grouping flow chart](https://github.com/nih-cfde/public-website-content/blob/master/images/metabolomics-data-hierarchies-3.jpg)  
  
The overall idea is that if we built these kinds of trees, and mapped Common Fund programs onto them, it would be easy to not only see what exists, but to find overlaps between them.  
  

*Scientifically Motivated Cross Cutting Questions.* Dr. Subramaniam shared several ‘Horizontal Integrations’; scientific questions that he thinks could be answered with current Common Fund data, by someone with sufficient time and expertise to combine datasets:  
  
> LINCS project has generated proteomic and transcription factor data following drug perturbation of cells (e.g. cancer cells). ENCODE has ChIP seq data on the same cells. GTEx provides tissue specific expression on the tissue that embeds the cancer cells.  
> Can we seek:  
> * What are the transcription regulatory pathways and genes that are affected in the tissue based on extrapolating the drug perturbation data from the primary cancer cells? 
> * What CRISPR experiments can be designed based on the function/pathway analysis to explore tissue specific role of specific genes?
> * From LINCS time series protein data, can we infer a “pseudo” time series that can be explored by specific kinase inhibitors?
> * Can the mechanisms inferred be explored in other tissues from tissue-specific expression data?  
  
### Agenda
**Day 1**  
**9-9:30am Introductions**  
Short introductions from engagement team members and attending DCC members. The overarching goal for the engagement team is to collect value and process data about the DCC. Values data will include things like: mission, vision, goals, stakeholders, and challenges. Process data includes: data-types and formats maintained, tools and resources owned by the DCC that they would like to have broader use, points of contact for follow up on technical resources, etc.  
  
**9:30-10am DCC Overview**  
Short overview of DCC. Can be formal or informal. Suggested topics to cover: What is your vision for your organization? What big problems are you trying to solve? What are your big goals for the next year? Who do you see as your most important users/stakeholders? What project(s) is currently taking up the bulk of your effort/time? What areas of your organization are you putting the most resources into? What is the rough composition of your user base in terms of discipline? Do you have any challenges that are blocking implementation of your current goals?  
  
**10am-Noon Goals Assessment**  
An exercise to get an idea of what types of things are important, what types of things are challenges, what do you dedicate your time/resources towards, and what types of things are not current priorities. Given a list of common goals provided by the engagement team, plus any additional goals the DCC would like to add, DCC members will prioritize goals into both timescale: “Solved/Finished”, “Current-Input wanted”, “Current-Handled”, “Future-planned”, “Future-unplanned”, “NA to our org” and for desirability: “Critical”, “Nice to have”, “Neutral”, “Unnecessary”, and “NA to our org”. The engagement team will work to understand the reasons for prioritization, but will not actively participate in making or guiding decisions.  
  
**Goal List**
* Increase end user engagement X% over Y years
* Move data to cloud
* Metadata harmonized within DCC
* Metadata harmonized with _________ 
* Metadata harmonized across Common Fund
* Implement new service/pipeline ____________
* Increase number of eyeballs at your site
* CF Data Portal
* Single Sign On
* Pre-filtered/harmonized data conglomerations
* A dashboard for monitoring data in cloud
* User-led training for end users (i.e. written tutorials)
* Webinars, MOOCs, or similar outreach/trainings for end users
* In-person, instructor led trainings for end users
* A NIH cloud playbook
* Full Stacks access
* Developing a data management plan
* Increased FAIRness
* Governance role in CFDE  
  
**Lunch: as a group, or separately, host’s choice**  
  
**1-2pm Open discussion (with breaks)**  
Using the results of the morning’s exercise and a collaborative format, iteratively discuss goals, blockers, etc., such that the DCC agrees that the engagement team can accurately describe their answers, motivations and goals.  
  
**Topics:**  
Infrastructure:  
* Do you intend to host data on a cloud service? 
* Have you already started using cloud hosting? If yes:
  * Approximately how much of your data have you uploaded? How long did that take? How are you tracking progress?
  * What challenges have you faced?
  * How have you dealt with those challenges?
* What potential future problems with cloud hosting are you watching for?
* Does your org use eRA Commons IDs? Do the IDs meet your sign on needs?
  * If yes, did you have/are you having challenges implementing them?
  * If no, what do you use? What advantages does your system provide your org?  
Use cases:
* What is the rough composition of your user base in terms of discipline?
* What if any, use cases do you have documented? Undocumented?
* What things do people currently love to do with your data?
* What things would people love to do with your data, but currently can’t (or can’t easily)?
* What pipelines are best suited to your data types?
* What are the challenges associated with those desired uses?
* What other kinds of users would you want to attract to your data?  
Review of metadata:
* What's metadata is important for your org? For your users?
* Do all of your datasets have approximately the same metadata? Or do you have many levels of completeness?
* Do you have any data already linked to outside resources?
  * Did you find the linking process easy? Challenging? Why?
* What kinds of datasets would you like to link into your collection?
* What implementation and schemas do you already have (or want)?
* What standards do you have (or want)?
* What automated systems do you currently have for obtaining metadata and raw data?  
Training:
* What training resources do you already have?
* What training resources would you like to offer? On what timescale?
* What challenges keep you from offering the training you’d like?  
Policies:
* How do users currently obtain access to your data?
* What are your concerns about human data protection?
* What potential challenges do you see in bringing in new datasets?  
NIH Cloud Guidebook:
* What would you like to see included?
* What would be better left to individual DCCs to decide?
* Would you be interested in contributing to it?  
FAIR:
* Has your org done any self assessments or outside assessments for FAIRness?
* Are there any aspects of FAIR that are particularly important for your org?
* Are there any aspects of FAIR that your org is not interested in?
* What potential challenges do you see in making your data more FAIR?  
Other: 
* What search terms would make your data stand out in a shared DC search engine?
* Does your org have any dream initiatives that could be realized with extra resources? What resources would you need?
* If you had free access to a Google Engineer for a month, what project would you give them?
* Any other topics/questions the DCC would like to cover  
  
**Day 2**  
**9-10am Review of goals and CFC involvement**  
A quick review of what topics are priorities for the DCC with suggestions from engagement team on how we can help.  
  
**10-noon Open Discussion, Thoroughness checking**  
DCC reflection on suggestions, open discussion to find shared solutions.
Touch on any questions not covered previously, ensure we have information on 
* datatypes they maintain
* formats etc of same
* tools / resources they think might be useful for the project 
* points of contact “Who is the best point of contact for your metadata schemas, your use cases, the survey of all your data types?”
* Who would like to be added to our governance mailing list?  
Or contact info/instructions on how to get that information offline.