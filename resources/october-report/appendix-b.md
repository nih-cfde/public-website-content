**Location:** 1218 Chestnut Street, 8th Floor, Philadelphia, PA 19107   
**Date:** Thursday September 5, 2019    
**Attendees:** Representatives in attendance from the CFDE were: Amanda Charbonneau (UCD), Steve Edwards (RTI), Titus Brown (UCD), and Owen White (UMB) and Anup Mahurkar (UMB). The representatives from SPARC were Chris Baglieri, Blackfynn’s SVP of Product, Leonardo Guercio Blackfynn’s Scientific Engagement Manager, and Joost Wagenaar, co-founder and VP, Scientific Applications of Blackfynn.

Table of Contents:  
[Meeting Logistics](#user-content-meeting-logistics)  
[SPARC Overview](#user-content-sparc-overview)  
[Program Lifestage](#user-content-program-lifestage)  
[Data Platform](#user-content-data-platform)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Infrastructure](#user-content-infrastructure)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Analysis](#user-content-analysis)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Access](#user-content-access)  
[Harmonization and Metadata](#user-content-harmonization-and-metadata)  
[Sustainability](#user-content-sustainability)  
[Training](#user-content-training)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Internal](#user-content-internal)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[External](#user-content-external)  
[FAIR](#user-content-fair)  
[DCC Cross-pollination](#user-content-dcc-cross-pollination)  
[SSO](#user-content-sso)  
[Outcomes](#user-content-outcomes)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Infrastructure Reuse](#user-content-infrastructure-reuse)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Challenges](#user-content-challenges)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Potential Solutions](#user-content-potential-solutions)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Potential Projects](#user-content-potential-projects)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Game Changers](#user-content-game-changers)  
[Agenda](#user-content-agenda)

### Meeting Logistics
We held a meeting with Blackfynn at their office in Philadelphia on Thursday, September 5, 2019 for a day and a half to discuss their work for the NIH Common Fund’s SPARC program. During the meeting, we used the agenda at the end of this document as an informal guide for structuring the day. 

The engagement team began by reviewing their goals for the meeting. These goals include learning about the structure and goals of SPARC, including specifics about the data they host, as well as information about training, organization, and the overall set of priorities for their group. In turn, Blackfynn provided us with a wide-ranging overview of their work on the SPARC program, demos of their data management system, and an insightful view into the intersection of government and industry in human research.

### SPARC Overview
Stimulating Peripheral Activity to Relieve Conditions (SPARC) is a Common Fund program focused on accelerating the development of therapeutic devices that modulate electrical activity in nerves to improve organ function. SPARC is different from many Common Fund programs in that its Data and Resource Center is shared among three academic and corporate entities. 
* Blackfynn, which serves as the Data Core, is a private company, and SPARC is its largest NIH grant. 
* Simulation Core is headed by Niels Küster of the IT'IS Foundation in Switzerland.
* Map Core is run by Peter Hunter at the University of Auckland. 

On this visit, we met with the Data Core. Currently, there are six full-time developers working on the SPARC project, plus a fluctuating number of people who contribute on an ad hoc basis. The platform is populated by data from sixty different labs. Blackfynn’s mission, both for the SPARC initiative and their company, is to provide technology that enables basic research, optimizes clinical trials, and transforms the treatment of neurological diseases. Their largest engagement outside the NIH is with the Michael J. Fox Foundation, supporting their Parkinson’s Progression Markers Initiative (PPMI: <https://www.ppmi-info.org/>). 

They told us that the general challenge is that data is not accessible in practice, and they want to ensure that clinicians and scientists have access to data, and at the right level of detail, to answer both clinical and scientific questions. They were excited to discuss the role for companies in meeting this challenge and were interested in the opinions within NIH.

### Program Lifestage
The SPARC Data and Resource Center (DRC) components were all funded beginning in September 2017 and had just begun their third year at the time of our visit. However, like several other Common Fund Programs, data collection by researchers had been funded for several years before the DRC was formed. This means that the DRC already has a great deal of data, more than 8TB, and is primarily focused on creating technology that can be easily worked into the pre-existing workflows of their researchers rather than defining and imposing standards. 

### Data Platform
Blackfynn develops two interconnected platforms that are leveraged by the SPARC program:
* The Blackfynn Data Management platform (<https://app.blackfynn.io/>)
* Blackfynn Discover (<https://discover.blackfynn.com/>)

The former is a platform for uploading, curating, and managing datasets. From this platform, users can publish snapshots of a dataset to Blackfynn Discover, which is a public, open data repository focused on the Neurosciences. 

The SPARC Portal is an independent open-source web portal (<https://github.com/nih-sparc/data-portal>) developed by the SPARC consortium to provide an integrated portal into the data, simulation, and mapping tools developed by the SPARC consortium. A large component of the SPARC Portal is powered by the Blackfynn Discover platform. That is, the SPARC Portal leverages the Blackfynn Discover APIs to show public datasets, support search, and allow browsing the contents of the dataset. The goal of the SPARC Portal is to share data, anatomical maps, and computational models generated by the SPARC-funded researchers. 

In order for the data (and subsequently the maps and models) to be visible on the SPARC Portal, the investigators must first publish their datasets within the Blackfynn platform to the Blackfynn Discover repository. The Blackfynn platform allows researchers to “publish” their dataset, and includes a number of traditional publishing features and rules: datasets have authors and co-authors (who can associate their ORCID IDs); the dataset is published with a markdown abstract to describe it, which is editable by submitter. 

Datasets can have multiple versions with multiple DOIs that are managed by DataCite.org. Once the data is in the SPARC Portal, there are several specialized analysis tools for running computational models (developed by the Simulation Core), as well as a collection of interactive anatomical maps for various species (developed by the Map Core). 

#### Infrastructure 
The Blackfynn platforms are entirely hosted on the Amazon cloud (AWS). The SPARC Portal is hosted through Heroku (<https://heroku.com>), which in turn is leveraging AWS. They chose to use a 100% cloud-based model for a number of reasons, mostly having to do with the flexibility of the cloud. Disk drives inevitably fail, and the amount of extra processing power, download or upload speed, and disk space that the project needs fluctuates depending on what users are doing. Determining up front how to account for those needs is difficult and error prone, however, when using cloud services, malfunctioning disk drives automatically fail over to working ones, and processes can scale almost infinitely. They also don’t have to worry that their internet connection is stable or has enough bandwidth — a large proportion of Amazon’s servers around the world would have to be impacted before it would affect the SPARC Portal. 

The SPARC Portal launched in July 2019, and, at the time of our visit, it contained approximately 10TB of data, about 3TB of which is out of embargo and publicly available. In the first eight months of 2019, 35 datasets have been published and each dataset has one or more versions.

SPARC expects their overall data collection to increase to at least 100TB over the next year. The Data Core hosts a wide variety of data types including imaging data (mostly microscopy), metadata (as CSV files), Word documents, PDFs, PowerPoints, -omics data, modeling and simulation data, and EEG traces. Currently, all data is submitted by SPARC-funded investigators; however, SPARC hopes to support community contributions in the future. The Blackfynn platform is HIPAA-compliant, and soon to be General Data Protection Regulation (GDPR) compliant, so the web user interface could support protected information. However, the SPARC Portal does not currently contain personally identifiable data.

Unpublished data on the Blackfynn Data Management Platform is stored differently than published data. Data and metadata that are still under embargo are located within the Blackfynn platform. Once the data and metadata have been reviewed and approved by the SPARC Data Curation Team (a subgroup of the Map Core), the dataset is published to Blackfynn Discover and the SPARC Portal. While submitted/embargoed metadata is initially uploaded as CSV files, once the dataset is approved for publication, it is stored in a Neo4j graph database on the Blackfynn platform, and the metadata is indexed using AWS ElasticSearch once published. Published metadata is exported as a mix of CSV and JSON files to allow users to utilize the platform of their choice when working with the data.

When a dataset is first published, it’s “snapshotted” and given a DOI. Any user with manager access to the dataset can make changes, however only the dataset owners can publish new versions of the dataset with a new DOI. This system works well for most of the data types that SPARC supports, that is, anything that is uploaded as a physical file.

A challenge with linking to external repositories in the context of dataset publishing is that you lose control over the underlying assets and rely on the external resource to handle this. For example, if you create a snapshot of a dataset and assign a DOI, we can guarantee that the data will never change. However, if part of the data is a URL to an external resource, we cannot guarantee that the contents at that URL have not changed. For example, SPARC leverages Protocols.io to store protocols associated with a dataset. They rely on protocols.io and users to not update/change a protocol after the SPARC dataset is published.

Blackfynn told us that their two main goals are to ensure the scalability of the platform and to ensure a quality user experience. Most of their resources are being invested in scalable platform development. Creating the infrastructure needed to support the work of a diverse range of researchers at the scale of petabytes of data, while adhering to security and global compliance requirements, is a gargantuan task. They are also putting significant effort into ensuring that their platform is friendly to both novices and technologically savvy users. This includes developing both a point-and-click user interface and enabling programmatic data access using a Python or MATLAB API or by using a Command Line Interface (CLI).

#### Analysis
SPARC does not have a dedicated workspace for users to do custom analysis, however it does host several specialized analysis tools for working with specific datasets, and a number of simulation models. Researchers publishing data to SPARC also can (and do) publish their pipelines or links to pipelines in their publication, and the Data Core is considering adding features such as embedded Jupyter notebooks to allow users to run custom, cloud-based analysis pipelines within the portal in the future. 

One of the biggest challenges is how to fit a platform like this into researchers’ existing workflows. Most of their users have established, custom workflows and have no idea how to even begin changing their workflow to take advantage of Blackfynn. Given the very large datasets that are made available through the SPARC effort, there is a need to educate investigators to run analyses in the cloud and avoid egress charges on the data.

Blackfynn has made instructions available to spin up AWS compute instances close to the data, but these are not intended for a general audience at this point. However, a significant effort is underway to leverage the public, standardized nature of the Blackfynn Discover platform to run analysis over public data using the users’ own AWS account. By training users how to leverage their own AWS accounts to freely interact with published data, Blackfynn 1) reduces the likelihood of runaway analysis costs on the platform side, and 2) removes any security concerns that arise from running arbitrary code on behalf of a user in the platform.

#### Access
At the time of this writing, 23 datasets are openly available on the SPARC Portal, with about forty more embargoed until January of 2020. About 60 different data generating sites are currently active, and there are between 300 and 400 portal users. Most of those users are data uploaders, but the platform is slowly moving towards supporting workflows for combining data and modeling.

The SPARC platform supports several modes of data access. For datasets less than 5GB, users can directly download a zipped archive of the data and any provided metadata files for free. For larger datasets, users can transfer data from the SPARC AWS bucket to their own or access data using any of the AWS tooling. This is generally free within AWS regions. Users can also use an AWS account to download the data, or to move it to another location using AWS tools or clients. The SPARC Data Core made the important point that “open data is not free data” at large scales. Their bucket billing system is currently set as ‘requester pays’, so users who download data, move it to another AWS region, or transfer it to another host will be required to pay data egress charges. SPARC public data is indexed through Google datasets.

### Harmonization and Metadata
Blackfynn’s goal is not to build a platform to share data, but to build a platform for data management that makes it easy to share and publish scientific data. Their philosophy is that scientific data is more than just files, and that meaningful data sharing should include rich, descriptive metadata. For this reason, the Blackfynn platform doesn’t restrict users to a specific data model. Users are required to supply only five metadata values for the dataset to receive a DOI and be published: Title, Summary, Description, Contributors, and Tags. Users can supply as much additional metadata as they want to describe their datasets, using any standard or user-defined metadata model. Users are not required to fit their data to a schema, but they are given the option to map their data to one or more schemas, as they see fit. Users can upload data files in any format and can include any number of supplementary files (such as PowerPoint presentations) or link to outside resources to enhance the reusability of their data. The SPARC program, however, does require that users follow a pre-fixed data structure, ontology/data standard, and specific file formats based on the BIDS (Brain Imaging Data Structure) specification (<https://docs.sparc.science/submit_data.html#1-creating-a-draft-dataset>).

Blackfynn’s strategy for harmonization has typically not been to define a strict metadata schema up-front and require users to fit their data into a specific schema. Rather, they work with users to define a schema that best fits their needs. Harmonization can happen retrospectively by smart mapping between the schemas. Rather than try to make data interoperable by mapping it onto the same metadata model, the Data Core envisions a future where data models are organically and progressively linked to ontologies. They have done some work on building classification algorithms that can do this. Currently, their software can take two datasets that use different metadata, but that were built from the same samples, and identify which metadata terms should be joined, with minimal user input. 

### Sustainability
Blackfynn told us that they were chosen as the Data Core for the SPARC program because of their company’s focus on data sustainability, security, and scalability. The company’s philosophy on data management is also important. They view data sharing as more than just making files available and are thinking strategically about how to interpret and contextualize these datasets and how to enable people to interact with them. 

Their platform is a great example of this philosophy in action. It is designed as a data management system that happens to make it easy for users to share their data, rather than as a data sharing platform. This distinction is important, because their platform is primarily about making their users daily data workflow easier, by giving them simple tools to organize their datasets, from the moment the data is collected. The platform also allows users to store related files like PowerPoints, or any other associated data, so it’s all in one place. This means that when it is time to share a dataset, the data, and all the other files the researcher has been using, are already uploaded and can be published together. This helps to ensure that data published on the SPARC Portal is complete, and easily reusable by other researchers.

By creating the platform as a data management tool, Blackfynn also hopes they can encourage people to adopt shared standards and other best practices. For instance, providing the appropriate text suggestions when implementing autocomplete capability for metadata fields, similar to predictive text options in a Google search, can help make metadata more consistent across datasets and improve interoperability. The predictive text shows the researcher similar terms that already exist on Blackfynn in other datasets and lets them easily use those same terms. The user can still choose to finish typing their own custom terminology, but by offering easy selections, the system encourages users to all adopt the same set of metadata terms. Blackfynn also hopes to create incentives for their users to foster the use of data repositories and to make data sharing a common practice within the Neuroscience community.

### Training
#### Internal
The SPARC Data Core did not express any dissatisfaction or problems related to their internal communication methods. Given that the DRC is distributed around the world, it will be interesting to talk to the Map Core and Simulation Core to see how well it is working across the consortium. 

#### External
About 80% of SPARC users are academics in the Neurosciences and the other 20% are clinicians. The SPARC award does not have a training mandate, however, Blackfynn provides user documentation for their web application (<https://help.blackfynn.com>) and developer documentation (<https://developer.blackfynn.com>) for programmatic access to the platform, and they are planning to add short tutorial videos in the next year. Furthermore, Blackfynn manages the SPARC Program documentation page (<https://docs.sparc.science>) detailing the overall workflow of the collective DRC. They also hold a ~monthly webinar, and occasional outreach, however they would be interested in improving and increasing the frequency of these events. The team was also very excited about collaborating with the CFDE to host hackathons. 

The SPARC Data Core told us that their support burden, and that of the Map Core, for these users is primarily about big data. Most users want to download data, and don’t understand that downloading terabytes of raw data is not efficient or sustainable. These users also usually don’t know how to use the cloud or realize that it is a better choice. Blackfynn also told us about problems with data upload: “We have had users drag 50,000 files into a browser window expecting that data would automatically upload instantly, and we have had users upload single files that were larger than 130GB.”

The team also told us that they anticipate that providing the right tools to enable cloud-based analysis of data will be the next big challenge for their platform, and that they would like to offer the ability to run custom cloud-based analysis pipelines. The challenge is figuring out what the researchers actually want to do and creating both the tools and training. The goal would be to bring biomedical data scientists with varying levels of technical expertise closer to the ability to use Blackfynn effectively.

### FAIR
The Data Core told us that they are 100% committed to making a FAIR resource. They are members of DataCite, ORCID, and the Research Data Alliance and actively work with those groups to further this mission. They currently mint DataCite URLs for data published in their platform and follow previous guidance from the Data Commons program regarding identifiers for their data. In our meeting, the Data Core took a very pragmatic stance on FAIR, and talked about it mostly in terms of data ownership and the practicalities of data movement. 

When talking about Findability and Accessibility, the SPARC Data Core differentiated between how these words are used in theory, and what they should mean in practice. Blackfynn pointed out that just putting data in a repository doesn’t necessarily make it findable or accessible in a practical sense. “Accessible to us means the user should be able to get many Terabytes of data available to them in an easy and scalable way.”

Data may be very difficult or impossible to find inside a given repository for any number of reasons. For instance, sensitive data, like that at dbGAP, has many metadata terms that could be of interest to a user, but that are hidden until the user has been granted access, which makes discovery of datasets impractical. Or, some data may not be well suited to the faceted search at its home repository, which keeps it from being found by most users. Even when a user finds data, it is only accessible if the user can actually use the data. A very large dataset at a repository that only supports data download may be functionally inaccessible to users, as they are restricted by both their local infrastructure and internet bandwidth. 

There are also monetary concerns around accessibility. Data hosting and egress charges have traditionally been covered by the institution that is funded to share the data. However, repositories increasingly don’t have the funding to do this at scale. The Sequence Read Archive (SRA), for instance, stopped accepting large sequencing project data years ago, mostly due to budgetary constraints. For data in the cloud, the largest cost is typically data download: “To mitigate these costs, many repositories either limit the size of datasets or limit the throughput on downloads. However, this goes squarely against the FAIR principles and results in repositories that have the notion of data-sharing while in fact the data in not truly available.” The Data Core suggested that the ultimate fix for this problem needs to be user education and training. Researchers need to be aware of the time and money required for downloading data, and that working in the cloud is a much faster and cheaper option. However, to work in the cloud, users need training that isn’t readily available right now. 

Even with a better educated user base, SPARC told us that there needs to be a long-term sustainability plan for data storage and use costs, and cautioned against adopting a system where the NIH pays data egress fees directly, without oversight:

> “If you do provide a platform that enable scalable, high-throughput data access to very large amounts of public data, one needs to take in consideration the cost that could be incurred by users. For example, what if a graduate student writes a script to download the entire public repository each night. What if this is a student in a different country, what if this is mal intended? Given the high availability of the resource, it would be very easy to have hundreds of thousands of dollars in unexpected costs within a couple of days.”

Finally, there are additional concerns with thinking not only about FAIR but also about making data publicly available. In a discussion about data ownership, the SPARC Data Core told us that one difficulty with making data public, is that often several entities claim rights to the same dataset, and have different views on where and how it should be stored and accessed: =

> “We strongly believe that data on our platform is owned by the users of our platform and not Blackfynn. However, our experience with academic institutions is that they also claim rights to the data, even though the NIH mandates data sharing. It would be great to have a discussion on mechanisms to break through this impasse.”

The SPARC Data Core also told us that although they believe they have made their stance on data ownership clear, they still frequently encounter resistance from academics who are wary of hosting their data on a portal ostensibly owned by a corporation.

### DCC Cross-pollination
The SPARC Data Core told us that they would be very interested in participating in a Common Fund Program community at many levels. While they have not identified any potential partners, they would be interested in participating in paired initiatives for demonstrating data reuse or building integrated datasets. As the Data Core has a deep interest in data ownership and sustainability, they also expressed excitement about the possibility of participating in CFDE governance and helping to establish best practices and standards. 

They also expressed interest in less focused community engagement such as participating in discussions and workshops at meetings for Common Fund Project PIs. In particular, they suggested that a “bring your analysis to the data” workshop with one or more Programs, would be an interesting way to test scaling analyses out into the cloud. Additionally, they suggested that NIH attendance at these events would be a useful way for the Programs to engage the NIH on complex, cross-program issues.

### SSO
Blackfynn provides its own user management and is planning to roll out single sign on (SSO) for their web applications in the near future. They expressed concern about the use of other single sign on systems for several practical reasons. As the SPARC Portal is hosted and managed by Blackfynn, and is part of their corporate constellation of systems, it falls under their service level agreements, that is, they guarantee a certain, small, maximum level of downtime, and have a number of processes dedicated to ensuring their system is always available. If they were to use an SSO service provided by another entity, such as the eRA Commons, they would lose that control over the system. Anytime the eRA Commons was down, either for maintenance, or due to technical issues, the SPARC Portal would be inaccessible. Worse, SPARC (and any other Common Fund Program using that SSO) would have no ability to fix or mitigate the problem. 

### Outcomes
#### Infrastructure Reuse
The SPARC data management model of building a portal (see the [Sustainability](#user-content-sustainability) section) is a good candidate for technology/philosophy that could be integrated into the larger Common Fund Program community. Many other Common Fund Programs have told us that their data creators are willing to submit data back to the coordinating center, but that getting those creators to submit the needed metadata in a useable format is much harder. The SPARC Portal encourages users to put all the data and files (including things like PowerPoint presentations) related to a project in a single place as they are created, which lowers the burden on the user at the time the data is shared. It also minimizes the metadata requirements while allowing users flexibility to include additional metadata as desired.

Although it is still in the planning stages, Blackfynn also told us about an open source ETL (extract, transfer, load) pipeline that they would like to build, which would be useful across the Neurosciences, and potentially the entire Common Fund. This pipeline would essentially be a cloud-based file format converter that could be used to make data more broadly reusable. Since many laboratories have their own data management systems and file formats, this would provide them with an easy way to get data into data sharing platforms or get data from these platforms into their workflow. It would also allow the community to make new file format converters that leverage the power of the cloud instead of relying locally run scripts. 

#### Challenges 
The Blackfynn team described a number of challenges with two main foci: user training and sustainability. 
* Users on the SPARC Portal frequently do not understand how to work with data at a large scale. Blackfynn related many stories of users attempting to upload or download extremely large datasets that overwhelmed the users’ web browser, as well as problems with users attempting to upload or download hundreds of smaller files simultaneously, with similar results. However, there is no clear articulation of what SPARC-specific training should be — “There is a lot of urgency as long as you’re in a conference call.”
* The SPARC Data Core told us that the biggest threat to sustainability is the misconception that “Open Data is Free Data.” There will always be costs associated with data download, storage, transfer and analysis, and while it is possible to make data available for free to users, that increases the cost of hosting the data, which is of particular concern after the Common Fund Program that generated the data has ended. Sustainability is defined by finding the best way to distribute these costs.
* Data ownership ambiguity is also a sustainability threat. The NIH funds the projects, and so ultimately owns the data; the data creators, and their institutions also often claim ownership rights. This ambiguity impedes data sharing and FAIRness. 
* Blackfynn also noted some practical concerns regarding the implementation and meaning of FAIR principles. For example, if FAIR means that each file needs a DOI, there are significant complications for the service that mints these DOIs (e.g., DataCite.org). If all Common Fund Programs started minting each file, the DOI services would all come to a standstill. For SPARC, each dataset will get a single DOI per version, and each file within a dataset is assigned a unique ID but does not need a global DOI. 

#### Potential Solutions
* Training and Support
    * Run hackathons for SPARC tools and interface enhancements. This would both help with refining the SPARC tools and with discovering new use cases that are important to their users. There is value in getting technical folks and users in the same room to better understand how the tools are being used and what is needed on the infrastructure side.
* ustainability
    * Increased interaction between Common Fund Programs, and Common Fund Programs and the NIH. Blackfynn was very interested in bringing the NIH into workgroups and brainstorming sessions to help address the many challenges to sustainability that they see both within their program and across the Common Fund.
    * From our discussions with the programs, we suggested that SPARC and LINCS might mutually benefit from discussing their approaches to data and potentially doing some analytic collaborations.

#### Potential Projects
A theme for training could be, “bringing your analysis into the cloud/close to the data.” This would help to address both training (“open data is not free data”) and sustainability (transfer costs). Potentially, these could be a CFDE-wide pilot workshop with KF/Cavatica, GTEx/Terra.

#### Game Changer
***Open Source ETL (extract, transfer, load) Pipeline***  
If Blackfynn were funded to create the ETL they envision, it would be a game-changing development towards interoperability. They want to design and build a cloud-based file format converter that could be used to make data more broadly reusable, as it would allow a user to translate a file into a wide range of other file types and formats. They estimate that creating this pipeline would require around 500K of funding per year for 2-3 years, as well as a consortium of stakeholders who would like to participate. They already have good connections with Neurodata Without Borders, the INCF, and other academic partners that would be willing to participate.


### Agenda
**Day 1**  
**9-9:30am Introductions**  
Short introductions from engagement team members and attending DCC members. The overarching goal for the engagement team is to collect value and process data about the DCC. Values data will include things like: mission, vision, goals, stakeholders, and challenges. Process data includes: datatypes and formats maintained, tools and resources owned by the DCC that they would like to have broader use, points of contact for follow up on technical resources, etc. 

**9:30-10am DCC overview**  
Short overview of DCC. Can be formal or informal, choose 1-5 topics to cover. Suggested topics: What is your vision for your organization? What big problems are you trying to solve? What are your big goals for the next year? Who do you see as your most important users/stakeholders? What project(s) is currently taking up the bulk of your effort/time? What areas of your organization are you putting the most resources into? What is the rough composition of your user base in terms of discipline? Do you have any challenges that are blocking implementation of your current goals? What skill set would you like to add to your project? How do you engage with your users? What kind of sustainability issues are you confronting? Can you currently do combined analyses with external datasets?

**10am-Noon Goals Assessment**  
An exercise to get an idea of what types of things are important, what types of things are challenges, what do you dedicate your time/resources towards, and what types of things are not current priorities. Given a list of common goals provided by the engagement team, plus any additional goals the DCC would like to add, DCC members will prioritize goals into both timescale: “Solved/Finished”, “Current-Input wanted”, “Current-Handled”, “Future-planned”, “Future-unplanned”, “NA to our org” and for desirability: “Critical”, “Nice to have”, “Neutral”, “Unnecessary”, and “NA to our org”. The engagement team will work to understand the reasons for prioritization, but will not actively participate in making or guiding decisions. 

**Goal List**  
* Increase end user engagement X% over Y years
* Move data to cloud
* Metadata harmonized within DCC
* Metadata harmonized with _________ 
* Metadata harmonized across Common Fund
* Implement new service/pipeline ____________
* Increase number of visitors to your site
* Common Fund Data Portal
* Single Sign On
* Pre-filtered/harmonized data conglomerations
* A dashboard for monitoring data in cloud
* User-led training for end users (i.e., written tutorials)
* Webinars, MOOCs, or similar outreach/trainings for end users
* In-person, instructor led trainings for end users
* A NIH cloud playbook
* Full Stacks access
* Developing a data management plan
* Increased FAIRness
* Governance role in CFDE

**Lunch**

**1 - 3:30pm Open discussion (with breaks)**  
Using the results of the morning exercise and a collaborative format, iteratively discuss goals, blockers, etc., such that the DCC agrees that the engagement team can accurately describe their answers, motivations and goals. Topics don’t need to be covered it order, we’d just like to touch on these types of questions.  
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
* What pipelines are best suited to your datatypes?
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
* Has your org done any self-assessments or outside assessments for FAIRness?
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

**10-noon Open Discussion**  
DCC reflection on suggestions, open discussion to find shared solutions.

**Lunch**

**1-2pm Thoroughness checking**  
Touch on any questions not covered previously, ensure we have:
* Action Items for us, and rough timelines for getting back to DCC on them
* Tools/resources the DCC thinks might be useful for the overall project 
* Points of contact “Who is the best point of contact for your metadata schemas, your use cases, the survey of all your datatypes?”
* Who would like to be added to our governance mailing list?
    * Or contact info/instructions on how to get that information offline.