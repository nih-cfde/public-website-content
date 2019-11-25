Table of Contents:  
[Meeting Logistics](#user-content-meeting-logistics)  
[HMP Overview](#user-content-hmp-overview)  
[Harmonized Data](#user-content-harmonized-data)  
[Cross Cutting Metadata Models](#user-content-cross-cutting-metadata-models)  
[Self-Governed Metadata Standards](#user-content-self-governed-metadata-standards)  
[FAIR Assessments](#user-content-fair-assessments)  
    [Findability and Accessibility](#user-content-findability-and-accessibility)  
    [Interoperability and Reusability](#user-content-interoperability-and-reusability)    
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
We held a meeting with the HMP via Zoom on Wednesday July 17, 2019 for about three hours. During the meeting, we used the agenda at the end of this document as an informal guide for structuring the meeting. Representatives in attendance from the CFDE were: Amanda Charbonneau (UCD), Ben Carr (BioTeam) and Titus Brown (UCD). We spoke with several members of the HPM team: Michelle Giglio, Heather Creasy, Victor Felix, Kemi Ifeonu, and Jonathan Crabtree. The PI, Owen White, joined us for the last half an hour or so. Anup Mahurkar was not available so he held a one on one conference with Amanda to ensure his input made it into the report.

The engagement team began by reviewing their goals for the meeting. These goals include learning about the structure and goals of the HMP, including technical specifications about the data they host, as well as information about training, organization, and the overall set of priorities for their group. In turn, the HMP gave us an overview of their organization, and talked to us about the varying goals and mandates of their two HMP grants. They also gave us a great deal of insight on how DCCs navigate the end of their lifecycle.

### HMP Overview
The Human Microbiome Project (HMP) had two phases. Phase 1 (HMP1), began in 2007 with the goal of building a shared community resource: a representation of the healthy human baseline normal microbiome. They recruited over 300 people to the project and sampled 15 body sites from men and 18 from women. Most of these were analyzed using 16s sequencing, and about 2200 of the samples were used for whole genome sequencing. The HMP Data Analysis and Coordinating Center (DACC) worked with four sequencing centers, the Broad Institute, the Baylor College of Medicine, Washington University School of Medicine, and the J. Craig Venter Institute, to create a single, integrated data resource. They also worked with some researchers to do ‘demonstration projects’, in which twelve groups were funded to examine correlations between changes in the microbiome communities and a disease. A subset of these projects received additional funding for follow up studies. Finally, the HMP was involved in an effort to find and sequence 3000 bacterial reference strains, which eventually became part of the NIAID BEI resource database. Funding for phase 1 of the HMP ended in 2012. 

Phase 2 of the HMP had a different focus, with some new sequencing centers, and a different overall organizational principle. Beginning in 2013, the DCC shifted to serving as only a Data Coordinating Center -- with no analysis support -- for the ‘Integrative HMP’, variously referred to as iHMP or HPM2. The Phase 2 goal was to characterize the microbiomes of three study groups: pre-term birth (both of the pregnant women and the child), Inflammatory Bowel Disease (IBD) patients, and Type II diabetes patients. These are all longitudinal studies that aim to study how the microbiome changes during progression of each condition. Data collection was split between sequencing centers by project. Virginia Commonwealth University collected the pregnancy and pre-term birth data; Stanford University and Jackson Laboratory collaborated to build the onset of Type 2 Diabetes dataset; and Harvard Medical School and The Broad Institute worked together on characterizing the onset of IBD. Taken together, these changes resulted in a dataset that has much deeper sequencing, but a narrower scope, and overall is a much less integrated dataset compared to phase 1.

### Harmonized data
Surprisingly, the harmonization effort at HMP is tightly linked to the terminology in their originating grants. Although the DCC was a ‘center’ for both HMP1 and HMP2 grants, the mandates of the RFAs, and by extension, the overall structure of the consortia, were very different. In HMP1, the team performed *data analysis*, that is, they were charged with ensuring that the data from the four sequencing centers was integrated and interoperable. The DACC captured all of the protocols and did a lot of cross-validation to ensure data quality. They created a single set of metadata terms that mapped to a single ontology. They also had the authority to impose those standards on the data generation centers. As such, all of the data from this phase acts as a single, harmonized dataset. It is comprised of many smaller datasets, but it can basically be treated as one enormous study: all the data was built with common analysis pipelines, using common outputs.

In HMP2, the coordinating team was designated a Data *Coordinating* Center, and that dramatically changed both their mandate and their ability to make a cohesive dataset. As a coordinating center, they were mostly charged with building a portal and making sure the data was accessible, but had no funding or power to make the data interoperable. HMP2 was essentially a loose federation of related sequencing efforts: every center used their favorite pipelines and their own ontologies. In order to upload their data to the DCC, they all did agree on a shared format for data, but that is where the similarities end. At the end of the project, it was effectively impossible to combine data across the various parts of HMP2, or to compare anything from HMP2 to HMP1. 

Although their funding has ended, the HMP DCC staff have been working to increase harmonization between the datasets, and to make all of the data from the two projects at least partially integratable on the portal. However, the center does not have access to the protected metadata associated with either phase, and so has no ability to harmonize it. As such, although the HMP studies should all be easily interoperable because they used many tissues in common, they are not.

### Cross cutting metadata models
The data structure used by the HMP, for both phases, should make them easily integratable with the C2M2. HMP data is organized within the Open Science Data Framework (OSDF) and uses a RESTful API for storing, retrieving and modifying JSON documents. Their JSON-Schema imposes structure on the data, and allows for validation of completeness or correctness of data by defining required properties, data types and formats using controlled ontologies. The HMP schemas are freely available at <https://github.com/ihmpdcc/osdf-schemas>. 

### Self-governed metadata standards
The HMP group noted that during the course of their project they were able to work closely with the data generators to develop a preliminary set of metadata, but data collected still required further curation. For example, during the first phase of the HMP only four centers were generating sequence information from a single study, and terms such as body site still varied based on the center performing the sequencing. During the first round of the HMP several demonstration projects were supported, and while subject variables were collected (e.g., race, weight, smoking status),none of the data generators used common controlled vocabularies to describe those variables. In the second half of the project, the iHMP data generators also gathered subject variables in a free form manner. 

### FAIR assessments
The KF DRC is very interested in FAIR principles, primarily due to their belief that making the data more accessible to more researchers, faster, is the key to improving outcomes for their patients. The KF staff are dedicated to every element of making data more accessible. As an independent entity, their DRC dedicates an enormous amount of time and energy to all elements of making their data assets findable, accessible, interoperable, and reusable -- what was evident from talking to them however was that there are no clear guidelines to operationalize FAIRness. Other than their own expertise, there is a vacuum of guidelines for them to operationalize FAIRness improvement.

#### Findability and Accessibility 
At the time of our meeting, processed data from both phases of the HMP was easily findable and accessible through the portal. Users can use faceted search to find a particular subset of data, and are provided with a manifest and instructions for downloading their selections. However, in the absence of funding, the portal will be shut down in mid 2020, and data from the HMP2 will be functionally impossible to find or access.

#### Interoperability and Reusability
Although FAIR terminology didn’t yet exist during HMP1, the consortium was working according to FAIR principles. They were very focused on metadata consistency and completeness, and have detailed SOPs for their workflows. However, they told us that the average user could not easily integrate their dataset with the HMP, or reuse the data:  “There’s no way in the world that this data could be integrated with a dataset that comes along from a new project.” 

This is largely due to the age of their data. For example, HMP1 did their gene calls using the version of blasttools that was cutting edge in the late 2000’s. Their process and pipeline is well documented, and includes relevant variables such as the version of blasttools they used. However, a user couldn’t replicate the HMP results unless they could also access the same blast database. Perhaps more importantly, it is not clear that you could recreate the results even if the HMP could provide a copy of the old database. The pipeline is outdated at this point, and has not been containerized. So while the pipeline is reproducible in principle, it would not possible to reproduce the results because databases that are used for assigning gene calls have changed. From their website page explaining the pipelines:

>Please be aware that HMP1 funding ended in 2012, and therefore some of these resources may have changed, moved or been discontinued. This list is no longer regularly maintained.

The HMP has already experienced problems with users trying to re-use their data. Since their funding has ended, members of their consortium have wanted to write publications and still required support from the DCC for data wrangling, as the data essentially needs to be entirely reprocessed for each user. One solution might be to fund the HMP to update the pipeline and reprocess all the data, so that the data is more directly comparable to modern analyses.

### Authentication/Authorization
Covered in [Brian O’Connor’s report](../july-report-appendix-j-single-sign-on-and-authorization-assessment).

### Data Dashboards
The HMP currently has no funding to move their data to the cloud, and so cannot use a data dashboard.

### CF Data Portal
The HMP  is interested in having their data be searchable through a centralized portal, however the CFDE will likely face the same challenges they did with harmonizing metadata and the inaccessibility of protected metadata terms. 

The current HMP portal offers a faceted query interface, and users can pull down a manifest file with standard fields. However, the HMP was skeptical that it could be re-used by other DCCs as it is a challenging piece of software, with many custom integrations. Porting the technology could probably be done, but the recipient would need assistance from the HMP. They also noted that many new technologies have been created since they built their portal framework, and newer technology might dramatically simplify shared data search. 

### Data Platform
#### Data Hosting
Ongoing data management is a problem at HMP. Processed data from the first phase of the HMP is stored locally, in the SRA, and in the cloud: several years ago, the HMP staff participated in a program where they received free, indefinite storage space from Amazon to host that data. However, phase 2 HMP processed data storage is only local, and currently on servers paid for by funds from initial HMP1 grant. The HMP does not store, or have access to the raw data or protected metadata from either phase of the project, which is stored at dbGaP.

The local servers that hold copies of both datasets were purchased on the original grant, so they are outdated and UMD is retiring them early next year. At the time of our meeting, the HMP had no funding to move the HMP2 data to the cloud, and did not believe the data could be added to their current, free, Amazon allocation. They also do not have funding to purchase new local machines, and data cannot be moved to the SRA at NCBI, because they are no longer accepting large datasets. Due to NIH data retention policies, the HMP must keep copies of the data, however there is no requirement for the data to be easily accessible. In the absence of further funding to move the HMP2 data to the cloud, their plan is to shut down the HMP portal in early 2020, and archive all of their local data on tape drives for the remainder of their required data storage time.

Altogether, this means that the HMP1 data will likely remain available to the public for some time: it was created sufficiently long ago that it was uploaded to the SRA before their prohibition on consortia datasets, and it also benefits from an old Amazon initiative to host scientific datasets for free. However, the processed HMP2 data, which was publicly released only in the last few months, will be unavailable starting in early 2020. 

If the HMP were to receive funding to migrate their data to the cloud, they indicated that they would need that funding very soon: the funding would need to be received by the end of December 2019, or January 2020 at the latest. This is because they need to move 10s of terabytes of data to the cloud or to tapes, and need to need to start that process before their servers are retired. The HMP estimated that they need to start data migration in January to finish in time, whether it be to the cloud or to tape archives. The HMP estimates it will take a month to transfer data to the cloud, but notes that depends on what we mean by ‘data’. The data that are actively in use by the portal (the final calls in the form of FASTA files) is around 42Tb, but this is only about 20-25% of the overall data stored by HMP. The other 75% is intermediate files, and it’s not obvious whether those need to be moved too. The current best practices for bioinformatics pipelines suggests that if a user has the raw files and a reproducible protocol, then the intermediate files are not necessary. However, given the age of the HMP project, those guidelines don’t necessarily apply, as many of their pipelines cannot be replicated. Given that, perhaps ‘data’ should mean *everything*, including intermediate files. If that is true, uploading the data to the cloud or archive will take closer to five months.

#### Data Analysis
HMP does not have an analysis platform, and has no current plans or funding to support one. However, they indicated that given additional funding, they would be interested in having full stack access for their users.

### Training
The HMP told us that there was little integrated outreach across HMP, however they offered several training opportunities. The finalized pipelines from HMP1, for instance, are available as walkthroughs - step by step tutorials - for users to help them perform the same analysis. In 2017, they hosted a one-off cloud workshop for fifty people, and they also host a standard metagenomics workshop, and a regular microbiome analysis workshop. The HMP has a helpdesk support burden that continues today. Their portal has 652 registered users, and approximately 8000 active users per month, who need regular support. 

### Outcomes
The CFDE discussed several challenges, and potential solutions that could be implemented by the Common Fund Data Ecosystem:

#### CFDE Targets
* Cloud funding:
    * Even if the HMP is funded move their data to the cloud, it’s not clear who will maintain it or pay continued storage and access costs. 
        * The HMP group suggested that the Common fund or CFDE will have to pay for ALL cloud costs: transfer, download, upkeep. 
            * The HMP could set up a bucket with user pay, but it would break the implicit system of taxpayer funded research: researchers expect NIH data to be free. It is technologically easy to make the users pay for data egress, but socially very difficult or impossible. 
            * The HMP noted that when universities set up a cloud hosting contract, one thing they frequently negotiate is no egress charges. They suggest that the NIH should set up STRIDES to not have egress charges, or be prepared to pay those charges
* Data continuity/upkeep/maintenance
    * Among the challenges that the HMP noted concerning end of life cycle are the costs involved in keeping an online presence. Even a static website needs periodic maintenance and security updates for the site; this is significant additional effort for the portal, databases and other features. 
    * They also noted that ‘data integration’ is an ongoing process, that has to be re-implemented every time a new DCC is added. 
* Training/outreach continuity/upkeep/maintenance
    * For datasets to be reused, new researchers need opportunities for outreach and training on those datasets. This points to a need for funding well past the 10 year DCC lifetime to keep datasets from falling into disuse.
* Funding clarification
    * The HMP is past their 10 year funding limit, and it is unclear whether and how new funds might be allocated to them for moving data to the cloud or for participating in other CFDE activities. No one is sure what the nuances of the law are, and an official ruling from the NIH would make it easier for end of life cycle DCCs to determine if it is worth their remaining time to work with the CFDE.

### Game Changers
During our discussions with the HMP group we heard about how meeting the requirements specified in the RFA for a DCC can sometimes have the unintended downstream consequence of making data less FAIR.

__Shifting the mandate of DCCs__ The biggest problem at HMP, and the one that they are still working on even after the grant is over, is lack of harmonization, and the HMP group told us that the problem stemmed from their shift from an analysis center to data repository. As a repository in HMP2, they could not ask for more people or computational resources, nor could they force the sequencing centers to align. The HMP DCC had no way to incentivize people to use the same pipelines or adopt the same standards. 

The HMP suggested that the single best investment that the NIH could make would be to routinely fund DCCs to also perform analysis roles. The analysis component is critical to keeping everyone on the same page, and would ensure data is collected and analyzed in a sustainable and interoperable way. Supplemental funding after a DCC is established is not as helpful as doing it right the first time, because enforcing changes on sequencing centers in the middle of a project is both technically and socially difficult. 

__Cross DCC Mentoring__ The HMP told us that they already are involved in some informal mentoring of other DCCs, and mentoring is an effective way for young programs to benefit from the experiences of older ones. This recommendation fits well with other suggestions for the CFDE to create a community of DCCs and increase opportunities for cross-pollination of ideas. 

### Agenda
**10 minutes Introduction from CFDE**  
Short introductions from engagement team members and attending HMP members. The overarching goal for the engagement team is to collect value and process data about HMP. Values data will include things like: mission, vision, goals, stakeholders, and challenges. Process data includes: data-types and formats maintained, tools and resources owned by HMP that they would like to have broader use, points of contact for follow up on technical resources, etc.    
 
**20-30 minutes HMP Overview**  
Please use the FunRetro board provided to sort this apriori set of goals that we expect DCCs might have **at least the day before** our meeting time. For each goal sticky in the ToSort column, drag it to the column that best describes the current state/thinking/goals of your organization. Then, leave a comment on each that specifics how desirable that goal is using these terms: “Critical”, “Nice to have”, “Neutral”, “Unnecessary”, and “NA to our org”. Please add as many other comments as you wish. If your organization has a goal that is not listed, please click the ‘+’ at the top of a column to add a new sticky.
 
**30 minutes Review Goals Assessment**  
An exercise to get an idea of what types of things are important, what types of things are challenges, what do you dedicate your time/resources towards, and what types of things are not current priorities. Given a list of common goals provided by the engagement team, plus any additional goals the DCC would like to add, DCC members will prioritize goals into both timescale: “Solved/Finished”, “Current-Input wanted”, “Current-Handled”, “Future-planned”, “Future-unplanned”, “NA to our org” and for desirability: “Critical”, “Nice to have”, “Neutral”, “Unnecessary”, and “NA to our org”. The engagement team will work to understand the reasons for prioritization, but will not actively participate in making or guiding decisions.   

**1 - 1.5 hours Open Discussion**  
Using the results of the goals assessment and a collaborative format, iteratively discuss goals, blockers, etc., such that the engagement team can accurately describe HMPs answers, motivations and goals. Topics don’t need to be covered it order, we’d just like to touch on these types of questions.

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
A quick review of what topics are priorities for the HMP with suggestions from engagement team on how we can help.