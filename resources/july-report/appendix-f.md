Table of Contents:  
[Meeting Logistics](#user-content-meeting-logistics)  
[LINCS Overview](#user-content-lincs-overview)  
[Harmonized Data](#user-content-harmonized-data)  
[Cross Cutting Metadata Models](#user-content-cross-cutting-metadata-models)  
[Self-Governed Metadata Standards](#user-content-self-governed-metadata-standards)  
[FAIR Assessments](#user-content-fair-assessments)  
    [Findability](#user-content-findability)  
    [Interoperability](#user-content-interoperability)  
    [Accessibility](#user-content-accessibility)  
    [Reusability](#user-content-reusability)  
[Authentication/Authorization](#user-content-authentication-authorization)  
[Data Dashboards](#user-content-data-dashboards)  
[CF Data Portal](#user-content-cf-data-portal)  
[Data Platform](#user-content-data-platform)  
    [Data Hosting](#user-content-data-hosting)  
    [Data Analysis](#user-content-data-analysis)  
[Training](#user-content-training)  
[Outcomes](#user-content-outcomes)  
    [CFDE Targets](#user-content-cfde-targets)   
[Game Changers](#user-content-game-changers)  
[Agenda](#user-content-agenda)

### Meeting Logistics
We held a meeting with LINCS via Zoom on Wednesday July 10, 2019 for about three hours. During the meeting, we used the agenda at the end of this document as an informal guide for structuring the meeting. Representatives in attendance from the CFDE were: Amanda Charbonneau (UCD), and Titus Brown (UCD). We spoke with three LINCS PIs: Mario Medvedovic from University of Cincinnati; Stephan Schürer from University of Miami; and Avi Ma'ayan from the Icahn School of Medicine at Mount Sinai (ISMMS). Also on the call were Jarek Meller from University of Cincinnati, who developed the LINCS proteomics portal; and three members from the ISMMS team: Alexandra Keenan is an MD/PhD student, who has been working with LINCS data throughout her PhD and presented on some of her work at our meeting, Daniel Clarke, a bioinformatician, and Sherry Jenkins, who is the project manager and the outreach lead of the center. 

The engagement team began by reviewing their goals for the meeting. These goals include learning about the structure and goals of LINCS, including technical specifications about the data they host, as well as information about training, organization, and the overall set of priorities for their group. In turn, LINCS provided us with an overview of their data generation pipelines, datasets, and breadth of analysis tools. They also gave us a great deal of insight on how DCCs navigate their final year of funding.

### LINCS Overview
The Library of Integrated Cellular Signals (LINCS) is a two stage CF program. In the LINCS Pilot Phase, LINCS Phase I, the program was comprised of two data generation centers, with no data coordination center. After four years of funding, the grants underwent a competitive renewal phase in 2014. Phase II of the project was to fund six data generation centers and one data coordination center for six years; this funding is due to complete on June 30th, 2020. 

Conceptually, LINCS is based on a Science paper from 2006: ‘The Connectivity Map: using gene-expression signatures to connect small molecules, genes, and disease’. The idea is that by collecting gene expression profiles, and other multivariate data, for small molecules before and after the treatment of human cell lines, it is possible to create a reference library that could be used by the community to form hypotheses to accelerate drug and target discovery. The patterns of changes in response to the drug perturbation defines a ‘signature’. The procedure is then repeated for various combinations of cell type, phenotypic assays, and perturbations to build a dense database of signatures that LINCS refers to as the LINCS cube. This database is useful for finding small molecules that have a specific effect on cell lines, and this can be used to enable predicting the effects of drugs on the human phenotype. By querying the LINCS database with signatures created by individual investigators, one can identify positive connections (i.e. drugs that mimic a disease signature) or negative connections (i.e. drugs that reverse disease signatures). Most of the LINCS data is from human cell lines, and includes a  small set of primary cells.

The structure of the LINCS consortium is complex, and has many different, loosely integrated, pieces. In Phase I, there were 10 production centers: two that did data production and analysis, four that worked on biological technology development, and four that built computational tools. There was no overall coordination effort. In Phase II, the Data Coordination and Integration Center (DCIC) was established. The DCIC has four components: DSR, which is focused on internal and external research projects; the IKE which maintains metadata and builds the portal, APIs, visualization, and integration tools; the CTO which manages training and outreach, and the CCA, which focuses on coordination and infrastructure. The DCIC is headed by three different PIs from three institutions, and they all contribute to each component.

Together, the DCIC works to coordinate the data coming from the six Data and Signature Generation Centers (DSGCs). Each of the DSGCs has a somewhat different focus for data collection and analysis. The Broad has two teams who are working independently, but sharing some conditions and cell lines. The first has generated the largest amount of data due to their L1000 assay for profiling human cells. The other Broad group focuses on high-throughput proteomics, however, their P100 and GCP assays are not as high-throughput as the L1000 team. The Oregon Health and Science University has a focus on RPPA proteomics and an assay. The DToxS DSGC also from ISMMS is examining how combination of drugs currently used in the clinic might be used to mitigate cardiotoxicity, using a variety of assays. The Harvard Medical School (HMS) DSGC LINCS center focuses on high throughput imaging, proteomics, and phenotypic assays (mostly in cancer) as well as cell signaling and modeling. NeuroLINCS, a multi-institute team, is focused on the systems biology of ALS. They create their own cell lines from patients with ALS and profile them using imaging, ATAC-Seq, proteomics, transcriptomics, and phenotypic assays to get a fuller picture of the molecular mechanisms of ALS. The MEP LINCS center as OHSU is using the microenvironment microarrays (MEMA) assay with microscopy to study how extracellular matrix proteins affect cell signaling in cancer cells. This breadth of studies resulted in the overall LINCS dataset hosting an unusually diverse set of data.

### Harmonized data
LINCS has a data ingest pipeline that requires some basic metadata: reagents, assay type, dataset type, experimental metadata, processing pipelines, and data files. However, since all of the DSGCs tend towards having such specialized analyses, most of the metadata terms are non-overlapping. The LINCS DCIC reported that although their data is not generally harmonizable in the sense of having easily combined metadata, there are still ways in which their datasets are interoperable. The signatures created by their experimental methods can be compared independently of the pipeline used to create them. However, the DCIC explained that pipelines using different aligners and/or different expression analysis systems give similar output, resulting in what they refer to as gene lists. “At the gene set level, these pipelines produce approximately similar up/down lists.” Since these gene lists comprise the signature, and are fairly stable, they argue that one RNA-Seq signature can be compared with other RNA-Seq signatures, regardless of the pipeline used to process the data. On balance, the LINCS team also stated that comparability only applied to certain types of experiments.

### Cross cutting metadata models
LINCS is committed to ensuring that their portal is compatible with the data model that will be used by the CFDE, referred to as the C2M2. Data in the portal is annotated with metadata, and there is already a version of JSON-LD that describe those datasets in our C2M2. 

### Self-governed metadata standards
The LINCS data is quite varied and their data is more like a loose confederation of related datasets. The common thread of LINCS datasets is that they can all be described by signatures; however, this does not mean that all of their metadata can be harmonized. The data LINCS hosts is very diverse in terms of data types, approaches, scientific questions, and scientific contexts; LINCS told us that they have no effective authority to enforce a unified processing pipeline, or to impose standards.

They noted that self-governed metadata standards are difficult to make and enforce, even within their own program. Most of the DSGCs have their own specialized pipelines and best practises, which they are not interested in changing. Similarly, although early on in the project everyone agreed to metadata standards for DCIC submissions, most of the DSGCs do not actually follow them. To ameliorate this, the DCIC built a comprehensive API that allows for easy data upload, and that allows the user to map any incongruent variables to the LINCS standard without having to edit their own copies. Still, the DCIC reported that most of the time, they need to go find the data and upload it manually, and this results in significant time following up with the DSGCs, and occasionally even a need to involve the program officers to convince the DSGCs to give them the data at all. Even then, most of the DSGSs do not use the API, opting to instead send files or links with little or no metadata. The DSGCs host their own data, or use data repositories like Synapse (<https://www.synapse.org/>), which mints DOIs and allows them be credited for data use, but also do not require metadata of any kind. So, while the DCIC staff were certain they could meet the minimal requirements suggested by the CFDE, they did not think it was practical to impose broader metadata standards on the data generators. 

### FAIR assessments
#### Findability
The LINCS program as a whole has numerous portals and tools, for example, each DSGC has their own web address. The various portals host mostly non-overlapping information and there is no one portal where a user can access all of the LINCS data. However, a user can search though most of the processed data from the main portal at: <http://lincsportal.ccs.miami.edu/dcic-portal/>. 

#### Interoperability
Members of the DCIC have taken the initiative to build end-to-end data analysis pipelines, data registration, and building these resources according to the standards agreed on by the consortium. The current version of their data portal has dataset packages, where the data comes from DSGCs, packaged with standardized metadata so the data is intercompatible. All the signature elements, the entities that a user would try to quantify, are also all normalized. At the high level of processing that most of their users are interested in, the LINCS data is interoperable. By using signatures, LINCS has also made progress towards integrating all of their data with external datasets, and building LINCS tools to work with more datasets. They can also support users bringing their own data and instantly comparing it with the LINCS database. Researchers who want to compare their own data to the LINCS database can use the LINCS signature search tools. Since LINCS signatures are such high level overviews of the underlying data, they are, in theory, interoperable with many other Common Fund dataset, provided all Common Fund datasets are processed into signatures. At a more basic level of processing, the diverseness of LINCS data and metadata will make interoperating with other Common Fund assets a challenge.

#### Accessibility
As a user, building a new dataset from raw data generated at more than one DSGC would be difficult. The user would have to get access to each DSGC portal separately, and learn each system, as each portal has a different implementation, and each DSGC uses differing metadata. However, LINCS also told us that this is not a significant issue for their users because the LINCS projects are so diverse that combining data from multiple sources is often not a common requirement. Most users are interested in the more processed data that is readily available through the main portal, or one type of data which can be accessed from the DSGCs portals.

#### Reusability
LINCS has created more than thirty specialized analysis apps, and reports that they can be easily applied to other projects or datasets, provided those data are processed and saved in the format expected by the app. The tools themselves are generic and have APIs, however, they would need some additional documentation before they would be easily reusable by the community. 

LINCS also told us that the signatures and the process to create them are very reusable. LINCS has done a lot of work on describing their processing pipelines and making them automated, so others should be able to re-use this work.

The data at LINCS, while reuseable in theory, is not uniformly reused. The LINCS datasets are very diverse, and some are much more specialized than others. LINCS told us that about 80% of the types of data they maintain, (about 10% of the overall data volume) are so highly specialized that it is unlikely to ever be re-used outside of the research project it was originally generated for. However, a great deal of LINCS data is reused frequently. They estimate that by volume, about 90% of their data is reused.

### Authentication/Authorization
Covered in [Brian O’Connor’s report](./appendix-j).

### Data Dashboards
The DCIC staff like the idea of a data dashboard, but are extremely leery of its implementation. They told us that early on in their program, they built a data dashboard very similar to the one the CFDE proposed. It monitored where data was physically stored, where it was in the process of being uploaded to the DCIC, how far along it was in the signature generation pipeline, and other similar metrics. However, the DCIC discontinued the use of the tool shortly after implementing it, because it was stressing their relationships with the DSGCs. As was discussed in the self-governed metadata standards section, the DSGCs maintain their own raw data, and it often takes significant effort on the part of DCIC staff to obtain a copy of their processed data. The data dashboard was widely disliked by the DSGCs, because it made the data handover process transparent in ways that disincentivized the DSGCs. For instance, the monitoring system made it simple to tell that a DSGC was holding data that had passed its embargo date, but not submitted to the DCIC. However, datasets that were delayed or withheld for transfer to ensure quality control or to fix other legitimate problems, could be construed by the NIH as simply being late. Keeping the data transfer process more opaque is less useful from a data tracking perspective, but protects the DSGCs from potential embarrassment over difficult to process and QC datasets. Discontinuing use of the data dashboard solved only the political issues: the DCIC is aware of several datasets that were generated by DSGCs more than two years before our interview, but that still have not been uploaded to the DCIC. 

### CF Data Portal
LINCS is interested in having their data be searchable through a centralized portal, but the CFDE will likely face the same challenges they did with finding overlapping metadata for search. The main data portal at LINCS is on its second version, and is an amalgamation of several portals. From the landing page, a user can choose to search by dataset, small molecule, cell or gene, each of which opens a more specialized portal implementation with varying search capabilities. As each section is highly adapted to the underlying dataset, the LINCS portal could not easily be reused by other DCCs. 

### Data Platform
#### Data Hosting
LINCS data as a whole is hosted on local storage clusters that are distributed across the country, and these different storage sites all host varying fractions of the overall data, at varying levels of processing. Here, it is useful to distinguish between the DCIC, which is the official coordinating center for the data, and the DSGCs, which generate the data, as all entities have some of the overall LINCS data, but no one has all of it.

__The DCIC__  
The DCIC portal does not have a complete copy of the overall data created as part of LINCS, for two main reasons. First, the DCIC typically only receives partially processed data from the DSGCs, with varying levels of metadata, so the DCIC has almost never has access to the raw data. LINCS told us that they (and most users) would not have much use for the raw data aside from storing it. A great deal of the LINCS data is generated on highly specialized machines, and so the raw data can only be viewed and processed using equally specialized software that most people do not have access to. Second, the DSGCs are not always timely with their data deposits. The DCIC is aware of several datasets that were generated by DSGCs more than two years before our interview, but that have not been uploaded to the DCIC. The LINCS DCIC also told us that some of the DSGCs are still generating data, and it is unclear whether all of the processed data will be incorporated into the main portal before LINCS funding ends.

The DCIC hosts the main portal (<http://lincsportal.ccs.miami.edu/dcic-portal/>) as well as a tool marketplace (<http://www.lincsproject.org/LINCS/tools>) that contains links to tens of specialized apps created by the LINCS DCIC and the DSGCs. These apps generally do not access all of the data available at the main DCIC portal. A given app website is tailored to a specific audience or question, and only has access to the specific data, at a specific data processing level, that it needs to run. All of the data in the main portal as well as that used by the apps is unprotected.

The infrastructure that supports most of the tools and the data portal are running on local servers but are cloud ready. This means that the apps, including the portal are dockerized and can be launched in a cloud environment without much needed engineering work. For now, Miami, Cincinnati, and Mount Sinai groups each have their own local cluster, each with its own tools, methods, deployment and management solutions. This is done mainly to keep costs low since there is no direct charge to host these servers locally. 

The LINCS DCIC suggested that moving to the cloud would not be extremely difficult, but that moving the data would be more difficult than moving the apps. They have tested transitioning their apps to a cloud based system, and currently have 'hybrid' apps that run both on the Amazon cloud, Google cloud, and local resources. However, several challenges remain. Their apps are containerized already for use on the cloud; but the apps are associated with many websites which would require careful coordination for their deployment. The apps are tied to subsets of the data which also require careful deployment on the cloud. Some apps are owned by the DSGCs, so those groups would have to be involved with transitioning to a cloud platform. The LINCS DCIC team stated that it would also be of value to review which datasets would or would not be useful to the research community, for example, they own a relatively large dataset of imaging of nearly 1 PB, which would be costly to host at Amazon and likely not that useful for the broad research community.

__The DSGCs__  
Most DSGCs store their own raw data and also have their own portals, however, they have varying levels of sophistication and useability. Generally, they do not distribute their raw data to the DCIC, however, some do additionally store their raw data in repositories such as dbGaP, NCBI GEO, Chorus/Skyline (for proteomics), and Synapse. In instances where there is protected data, it is also retained by the DSGCs and stored in dbGaP, but not distributed to the DCIC. LINCS has only a few datasets that require human subject protection.

#### Data Analysis
As with data storage, data analysis at LINCS is highly distributed. The portals associated with the DSGCs all have some data analysis tools, at varying levels of sophistication and access. The Broad’s clue.io platform, for instance, allows users to do analysis of their L1000 data, however, it requires a log-in and has strict rules for commercial use. Other DSGC portals have fewer or no restrictions, and most offer less analysis power.
 
The DCIC itself also has tens of analysis apps, and these also vary in their data, and access restrictions. The DCIC does not have a single analysis platform or tool. Rather, the apps are all self-contained websites, linked to from the main LINCS portal. A given app website is tailored to a specific audience or question, and only has access to the specific data, at a specific data processing level, that it needs to run. 

While none of the DCIC apps contain private data, some require a simple log-in before use. The DCIC staff suggested that the log-in requirement, or lack of one, in their own apps was largely due to the preference of the person who wrote the app rather than there being a particular need for some apps to track users. Internally, there has been some push for a universal log-in, however, it’s unlikely to happen in the final year of the program due to other priorities. A universal login system was attempted but it presented both technical, and cultural challenges, and was discontinued. DCIC apps generally do not have access to all of the data available at the main DCIC portal. 

The DCIC staff does not have access to usage statistics for the DSGC portals or analysis platforms, however, they know that their own apps are widely used. Their 31 tools, which between them have access to over a million signatures, have had over 700,000 unique users since 2014, and have been cited by more than 2,500 papers. In 2019, the ninth year of their program, they still consistently see more than two thousand users a day. 

LINCS told us that their large number of users results in many technological challenges. Most of their apps were not originally designed to run at this high volume, and maintaining or updating them takes time away from other projects. At the time of our visit, Enrichr, their most popular tool, was under a DDoS attack and had been down for several days, and fixing it was a difficult problem. For ongoing work, LINCS reports their software development practices are improving, and they now approach software in a more professional way. They credited their involvement with the DCPPC with making their coding practices more deliberate and starting to use systems that help ensure reusability like GitHub and Docker. These practices should help mitigate future issues with new tools, but they could use resources to modernize their current batch of products.

### Training
LINCS has a robust outreach and training program that uses a number of modalities: they host a summer research training program, deliver webinars, and offer a Massive Open Online Courses (MOOCs). They reach an astounding number of people at various levels of experience. The summer research program is a data-intensive fellowship that supports ~10-15 undergraduate students per year. This year the program had over 500 applicants. The LINCS webinar series is currently inactive, after running consistently for the first four years of the program. For the series, LINCS invited researchers who were active in the community, but not a part of the consortium, to give seminars, which the DCIC would record and post. These webinars typically have hundreds of viewers, and can be found on YouTube by searching for ‘dcic lincs’. LINCS has two MOOCs that have been available for five years through Coursera. One MOOC is about LINCS specifically, while the other teaches systems biology. Between them, the videos within these MOOCs have been viewed more than half a million times. About 100,000 people have officially signed up for the MOOCs, and more than 10,000 of those people completed a series. They also have a fellowship for mid-stage researchers, that falls somewhere between being a postdoc and an assistant professor. The fellows are physically located at a DSGCs and work with both the coordination center and the generation center to do a data intensive project. 

LINCS told us that they value their training program for a wide variety of reasons. Their training and outreach programs function as advertising for the LINCS project, and increase its use. They also directly increase the sophistication of their users and encourage proper data use. LINCS credited their fellowship programs especially with swaying talented scientists to do public biomedical research rather than moving on to higher paying corporate jobs. By giving people the freedom and resources to explore interesting projects, the LINCS DCIC members said they can compete with industry for the best candidates. The DCIC also told us that their training program drives research and innovation. When students come to learn about a tool or attend a workshop, their reaction to subject matter can help inform how to build future tools, databases, and interfaces to be more user friendly, and to accomplish tasks that the development team might not have thought of. Students and fellows that come for longer periods to work on a project for a few months to a year are an important force that keeps projects going. ‘Students drive the whole operation forward.’ LINCS told us that projects done by students, even high school students, benefit the overall mission of the center, and that their projects seed more and bigger research. The students benefit as well, they gain useful experience in a complex field. 

### Outcomes
Most of the new outcomes that LINCS would like to see from the CFDE involve building a robust community and assisting periods of transition at DCCs.

#### CFDE Targets
* Institutional memory:
    * CFDE could serve as a resource for “here are how other DCCs have done things”. This would be particularly useful to newly opening DCCs that might be struggling with ramping up operations
* NIH K grantee program
    * If there was a program for people coming out of DCCs, that would help recruit people into them in the first place. The challenge is recruiting good career-focused people to an end-dated project.
* Structure and Organization
    * “At LINCS there was a lot of building the airplane as it flew.” LINCS suggested that there is a middle ground between a set rulebook for DCCs and complete freedom. As a young DCC, they would have appreciated a framework to build from rather than starting from scratch. This is closely related to the idea of maintaining an institutional memory.

### Game Changers
During our discussions with LINCS we heard about the need for a framework for DCCs, the need for institutional memory, and the feeling of abruptness at both the beginning and end of a DCCs lifecycle.  This target is labeled a "game-changer" because it would positively impact the entire ecosystem. 

__Creating a lifecycle support program for DCCs__. LINCS told us about several different challenges they faced as both now and as a young DCC, however these issues all seemed to stem from inadequate support for specific stages. They also told us that their Program officers are very concerned about data continuity. This applies not only to the DCIC data, but for the original data producing centers. They want to sustain resources used to generate data and all of the portals. Conclusions from our discussion with LINCS was the CFDE could create a lifecycle support program to:
* Interview and engage with DCCs throughout their lifecycle to learn about how they are operating, and how they have addressed issues. The CFDE would maintain the institutional memory of lessons learned at various DCCs and pass that knowledge on through DCC engagement.
* Provide DCC best practices and other lightweight structure for young DCCs, to help reduce administrative burden. This could include institutional memory, “here are how other DCCs have done things”, as well as generic tools for common tasks like onboarding.
* Create long-term outlook guides for young DCCs to help them better plan for any asset transitions that are needed at the end of lifecycle.
* Work with DCCs in their last year or two to identify Common Fund assets that should be maintained after the DCC funding ends, and help to transition those assets to a longer term owner, or recommend those assets for longer term funding by the Common Fund.
* Potentially play a role in recruiting and retaining well trained specialists by relocating them to new DCCs. 

### Agenda
**10 minutes Introduction from CFDE**  
Short introductions from engagement team members and attending LINCS members. The overarching goal for the engagement team is to collect value and process data about LINCS. Values data will include things like: mission, vision, goals, stakeholders, and challenges. Process data includes: data-types and formats maintained, tools and resources owned by LINCS that they would like to have broader use, points of contact for follow up on technical resources, etc.     
 
**20-30 minutes LINCS Overview**  
Short overview of LINCS. Can be formal or informal, choose 1-5 topics to cover. Suggested topics: What is your vision for LINCS once the program ends next year? What big problems are you trying to solve? What are your big goals for the next year? Who do you see as your most important users/stakeholders? What project(s) is currently taking up the bulk of your effort/time? What areas of development the LINCS DCIC is putting the most resources into? What is the rough composition of your user base in terms of discipline? Do you have any challenges that are blocking implementation of your current goals? What skill set would you like to add to your project? How do you engage with your users? What kind of sustainability issues are you confronting? Can you currently do combined analyses with external datasets?
 
**30 minutes Review Goals Assessment**  
Please use the FunRetro board provided to sort this apriori set of goals that we expect DCCs might have **at least the day before** our meeting time. For each goal sticky in the ToSort column, drag it to the column that best describes the current state/thinking/goals of your organization. Then, leave a comment on each that specifics how desirable that goal is using these terms: “Critical”, “Nice to have”, “Neutral”, “Unnecessary”, and “NA to our org”. Please add as many other comments as you wish. If your organization has a goal that is not listed, please click the ‘+’ at the top of a column to add a new sticky.  

**1 - 1.5 hours Open Discussion**  
Using the results of the goals assessment and a collaborative format, iteratively discuss goals, blockers, etc., such that the engagement team can accurately describe LINCSs answers, motivations and goals. Topics don’t need to be covered in order, we’d just like to touch on these types of questions.

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

FAIR:
* Has your org done any self assessments or outside assessments for FAIRness?
* Are there any aspects of FAIR that are particularly important for your org?
* Are there any aspects of FAIR that your org is not interested in?
* What potential challenges do you see in making your data more FAIR?

Other: 
* What search terms would make your data stand out in a shared DC search engine?
* Does your org have any dream initiatives that could be realized with extra resources? What resources would you need?
* Any other topics/questions the HMP would like to cover

**30 minutes Review of Goals and CFDE Involvement**
A quick review of what topics are priorities for LINCS with suggestions from engagement team on how we can help.