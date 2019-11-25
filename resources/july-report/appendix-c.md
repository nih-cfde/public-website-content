Table of Contents:  
[Meeting Logistics](#user-content-meeting-logistics)  
[GTEx Overview](#user-content-gtex-overview)  
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
    [Major Use Cases](#user-content-major-use-cases)  
[Game Changers](#user-content-game-changers)  
[Agenda](#user-content-agenda)

### Meeting Logistics
We held a meeting with GTEx group at the Broad Institute on Monday June 3, 2019 for a day and a half. GTEx collaborated with us before the meeting to build the agenda at the end of this document, which we used as an informal guide for structuring the day. Representatives in attendance from the CFDE were: Anup Mahurkar (UMB), Amanda Charbonneau (UCD), Brian O'Connor (Bionimbus), Titus Brown (UCD), and Owen White (UMB). Primary representatives from GTEx were Kristin Ardlie (PI), Jared Nedzel (lead software developer) and Francois Aguet (lead computational biologist). Several sessions were held where we were able to meet with the entire GTEx staff of eight people.

Discussions were initiated with short introductions from the engagement team and attending DCC members. We reviewed that the goal for the engagement team was to collect information about GTEx, including technical specifications about the data they host, as well as information about training, organization, and the overall set of priorities for the GTEx group. The GTEx group was then asked to provide an overview of the GTEx operation, with topics including: mission, vision, goals, stakeholders, and challenges.

### GTEx Overview
GTEx is a data resource and tissue bank to study the relationship between genetic variation and gene expression in multiple human tissues.  It is a valuable tool for exploring the genetic basis of complex human diseases. GTEx is also examining sex-based, and cell-based differences in how genes are turned on and off and how they are regulated. Samples were collected from deceased adult donors, with multiple tissue samples collected per donor (e.g. lung, brain, pancreas, skin, etc.). The GTEx project differs from most other Common Fund DCCs in that instead of being dedicated to disease, they are striving to build a ‘reference normal’ database. While all of their tissue is necessarily from deceased donors, each sample is screened by pathologists, and tissues showing signs of specific diseases are excluded from their pipeline. As such, the GTEx data collection is our best current resource for representing the typical range of human gene expression. 

GTEx started in 2010 and was funded for seven years. During that time, over 650 papers were published using data from the GTEx data resource. The portal that provides access to GTEx resources was launched in 2013, and is still active. Although the project is officially over, the portal still has about 15,000 visitors a month, and is currently funded with a genomic resources grant. The current release of GTEx, V7 includes: ~1000 post mortem donors, 53 tissue sites, 11 distinct brain regions, and 2 cell lines. Due to their rigorous tissue screening process, the number of samples for each tissue varies greatly. For example, reproductive, bladder, and some brain tissues are under-represented in the dataset, which is unsurprising given the high mean age of their typical donor. Data types hosted by their group include: summaries of gene expression based on RNA-Seq data, quantitative trait loci data, and histology images. Their current dataset size is roughly 395 TeraBytes (TB), and will soon increase to a total of 600TB. GTEx also has a large number of datasets that have protected status and are stored at dbGaP. This information includes raw RNA-Seq files, whole genome shotgun sequence, genetic variants, and donor phenotypes.

### Harmonized data
GTEx has already harmonized with ENCODE and will be closely harmonized with MoTrPAC; their RNA-Seq pipeline is also implemented and used by TOPMed. These collaborations were primarily due to opportune circumstance: in addition to her work at GTEx, Kristin Ardlie sits on MoTrPAC advisory board, and collaborated with three MoTrPAC PIs who are experienced with the GTEx datasets (Mike Snyder and Steven Montgomery from Stanford, and Tuuli Lappalainen from the New York Genome Center). Both Kristin and Francois are also engaged in implementing best practices for RNA sequencing pipelines for TOPMed.

### Cross cutting metadata models
GTEx expressed concern that broad metadata harmonization may be practically unfeasible for more than a small number (likely fewer than 10) of core terms per data type, and that it may be of limited value. Instead, they favor creating a data definition language for metadata such that a user with sufficient knowledge of the ontology of two datasets can use the same API to navigate both and build correspondences as needed. The ontology could have a small number of core terms that are always applicable, as we as a more articulated set that cannot always or often be mapped between datasets. For instance, RNA-Seq datasets might always be required to have terms for metadata such as sample collection dates, tissue type, lane or other batch sequencing batch effects, and other data that would need to be incorporated into any model that was used to analyze RNA-Seq data taken from many experiments. In their view, an overall cross-cutting data model is not practical, or even particularly desirable: “The important thing is for the metadata to be clear and defined, so it can be clear if you’re comparing apples to apples or not.”

One potential solution to this is to introduce ‘metadata levels’, where a particular dataset with little or no metadata might be a ‘level zero’, one with the core metadata a ‘level one’, one with some level of harmonization is a ‘level three’, and so on. GTEx pointed out that a core problem with this approach is that once the ‘levels’ are linked to the amount of harmonization, the problem of assigning a level becomes extremely complex, because there is no single, defined ‘center’ of metadata to harmonize to. This means that a given dataset, A, might be 80% harmonized with a second dataset, B. However dataset A might not share any terms with a third dataset, C, even though 50% of the terms in datasets C and B are harmonized. The larger the number of datasets, the more impossible it will be to assign a single harmonization level to any given dataset. Instead, harmonization level would need to be described in terms of a given pair of datasets, and any given dataset would be very unlikely to be at the same level of harmonization with every other. This also has implications for FAIRness metrics, as assigning a dataset a degree of ‘Interoperability’ will have the same challenges. 

### Self-governed metadata standards
GTEx would be interested in contributing to defining a metadata standard, assuming that standard is based on something like the ontology described in the Harmonized Data section. That is, a method that encodes each ontology into a data definition language. In this way, two different ontologies can still be in the same common schema, and users that have knowledge of the ontology can use the same API to access that information. GTEx is not interested in participating in an attempt to broadly harmonize across every Data Commons dataset. This would take a substantial amount of resources, and they are skeptical that it can be achieved in any practical way. 

### FAIR assessments
#### Findability and Accessibility 
GTEx made a clear distinction between the different parts of FAIR and how, and whether, they are useful. Findability and Accessibility are important and actionable. As is further discussed in the Data Platform section, the raw data from GTEx is currently not readily accessible by users. As part of the DCPPC, GTEx moved all of their raw data into the cloud, however, when the program ended, the system for providing access to that data ended with it. Accessibility will continue to be a problem until there is both a system in place for data access, and also a long-term plan for funding the cloud model. The GTEx team are working on hosting of their upcoming V8 release with ANVIL.

Both GTEx and their users want their data to be easier to find, i.e. browse and combine with other datasets, and useable by more people, for more projects. Recently, GTEx surveyed their user base, and found that their users are extremely interested in locating data that can be used together. They asked:

> If we were able to integrate GTEx protected (dbGaP) data into the GTEx portal, would you find it useful to query and visualize sets of data grouped by phenotype (e.g. actual age, medical history, genotype, etc.) 
>
> Would you find it useful if we were able to integrate other protected datasets, such as TOPmed, with the visualizations on the GTEx Portal?” 

Of their 112 respondents, ~87.5% said yes to each of these questions. Although adding extra metadata into their portal is a straightforward task, GTEx has no immediate plans to incorporate these other protected metadatasets. This is because 1. dealing with the protected metadata aspect is currently intractable and, because, 2. they cannot financially support new staff to do the work. Onboarding the protected metadata would require integration with FireCloud/Terra, which is a FISMA Moderate platform. This means GTEx itself would have to become FISMA Moderate, and the portal currently does not have this level of access control. Bringing the portal up to FISMA Moderate standards would require a great deal of documentation and some re-programming of the portal. For example, currently the metadata used to draw the interactive plots in the portal is readable by any user that views the webpage source code and understands html. So, while the portal is fine for displaying publicly available metadata, it would unacceptably expose any restricted metadata that runs through it, and the codebase would require extensive re-writing to adequately protect private data. There are teams at the Broad who have the ability to do all of this work, however GTEx doesn’t have the resources or funding to support them. GTEx also noted that additional funding through the OT mechanism would not help, as they cannot make short contracts for engineering hires (<12 months). They would require a stable contract of at least one year to be able to hire people to improve this, or indeed any, aspect of their operation.

#### Interoperability and Reusability
GTEx is somewhat less concerned about the other aspects of FAIR: Interoperability and Reusability. The concern with these concepts is similar to the one they raised about metadata ‘levels’: whether a dataset or data center is ‘interoperable’ is based on what other dataset or data center you are comparing it to, and these pair-based comparisons are difficult or impossible to generalize. They will always be project-interaction-specific and context dependent. Similarly, whether a dataset is ‘reuseable’ is extremely difficult to judge, and contingent on people actually having done it, i.e. “data is not reusable unless it has been reused.” 

### Authentication/Authorization
Covered in [Brian O’Connor’s report](../july-report-appendix-j-single-sign-on-and-authorization-assessment).

### Data Dashboards
All of GTEx’s raw data is currently hosted on Google Cloud, so they have little use for this utility. If it could monitor access (which is currently a problem) or help with reporting usage statistics, they might find that useful. 

### CF Data Portal
GTEx has a refined and interactive portal that allows their users to explore their publicly available metadata and data. Any user can access the GTEx portal without logging in and use it to: 
* Search for data with specific metadata terms
* Find what genes are expressed, and at what level, in any tissue
* Compare gene expression between tissues
* Look up expression for a gene or genes across tissues
* Generate a PCA of expression subset by any public metadata
* Find and view eQTLs and make basic comparisons
* View histological images for over 25,000 samples
* Users with a Google login can submit requests for GTEx biosamples.

In the next few months, they will be rolling out additional features to allow their users to do more complex eQTL analysis. 

Their portal is extremely well used by their user community, and is popular because it requires little expertise to navigate and create useful figures. They see about fifteen thousand users per month on GTEx portal, with over a hundred and forty thousand page views. They are a globally used resource with roughly 50% of their users from the US or the UK, with the rest being spread throughout the world.  They serve a full spectrum of users on the portal, from bioinformaticians to clinicians and genetic counselors. Their portal is written in D3, and Python, with a Javascript front end, and REST back end. The database is MongoDB and Google Datastore, and uses the Google App Engine. 

Although GTEx is interested in a CFDE portal to connect users to new datasets, they suggested that the specificity of each DCC will make a single data analysis portal impractical. While some of their portal features are generic, most are specific to this project and their data organization. GTEx has a very specific picture of how their users want to interact with their data, and has tailored not only their portal, but their underlying analysis pipelines, to that vision. They expect all the other DCCs to do this as well.

All data coordinating centers are well-equipped to know the perils of their data, how users misinterpret data, and the most common ways that their data can be mis-used. GTEx reports that while they don’t know the experience level of their users, they have reason to believe that most of their users do not have the technical sophistication level to join GTEx data to other datasets in a statistically appropriate way. Many of the help requests at GTEx are low level bioinformatics questions that are not GTEx specific. Their users almost never ask about the type of statistical or technical issues that they would need to correctly combine their own data with GTEx results, which is a common use of GTEx data; and a recent paper found that most papers, 35 of the 50 sampled, did not use an appropriate method to compare the GTEx eQTLs with GWAS data (<https://www.nature.com/articles/s41588-019-0404-0>). This will only be made more problematic if users are able to link between GTEx datasets and other resources through the CFDE, without appropriate guidance and/or training. 

This example suggests that these type of data (GWAS, eQTLs) should be more readily available as harmonized resources. Although it would take a lot of time and resources to generate this kind of data, it would facilitate more sophisticated and statistically sound analyses for less expert users, who tend to look up individual SNPs. GTEx would not support a portal that allows an end user to naively combine processed datasets across DCCs unless they could be certain that all of the data a given user might choose had been run through the same pipeline and could be trusted to give scientifically valid answers. However, they would be in favor of a system that has expertly harmonized data for popular GTEx features (GWAS, eQTLs), and one that allows the individual interfaces of each DCC to pass data back and forth in a more facile way. They would also support a system that allowed users to find datasets across data centers, and think it would be of value to document issues concerning how to properly build and analyze new cohorts and to make those tutorials available to the wider community. 

### Data Platform
#### Data Hosting
GTEx has historically been the most frequently downloaded data from dbGaP, however that may no longer be true: due to their participation in the DCPPC, all of the GTEx raw data is now cloud based, and was set up to be accessed via the DCPPC access solutions. GTEx itself uploaded a copy of all the raw data to the Google Cloud, while a second copy of the GTEx data was made available on Amazon Web Services (AWS) by NHLBI. GTEx is still paying to host all of this data in the cloud, but it is inaccessible to end users. 

The DCPPC solution for the Google Cloud involved hosted pointers to data storage ‘buckets’. Unfortunately, when the DCPPC dissolved, the pointer hosting went with it, so although the data is in the Google Cloud, there is no way to access it. The AWS solution used signed URLs, and was set up with incorrect authentication. When the DCPPC ended, work on the signed URL system halted, and the authentication issue was never fixed. As such, users can see that the data exists on AWS, but cannot download it because the signed URLs don’t authenticate correctly, and users can’t get to the Google data bucket at all. The SRA database does not have the complete GTEx dataset, so at the time of our meeting, a large proportion of GTEx data was completely inaccessible to anyone outside GTEx. 

Even once access is fixed, GTEx has concerns about data storage in commercial clouds. First, GTEx currently only has funding to maintain their portal. They currently pay cloud hosting fees and all their other costs, using money leftover from the original grant. However, those funds will not last much longer, and it’s unclear who will pay for the cloud storage long term, or what will happen to the GTEx data when their funds run out. There are also issues with user costs. As difficult as dbGaP is to navigate, it is free for users, and that’s something users really like. Cloud buckets cost money for data storage, data processing, and data movement, i.e. downloads. Currently the GTEx buckets are set to be ‘requester pays’, that is, the user must pay download fees, which is expensive for the user. However the only current alternative would be for GTEx to incur the user download costs, which they don’t have funding for. A solution to the download problem would be to encourage users to work entirely in the cloud, and to simply access the data rather than downloading it. However, this has its own problems. Most GTEx users don’t know how to work in the cloud, or how to move their analysis pipeline there, and would need a great deal of basic bioinformatics training that GTEx doesn’t have the resources to provide, and wouldn’t fit their mission. It also simply moves the cost from ‘downloads’ to ‘compute time’, and there is no good way to mitigate those fees. Supplements to NIH grants, for example, do not work for non-NIH fundees, and as nearly half of GTEx users are international, they would likely not be covered by any US based supplement system. It will also be difficult to get users to move to a cloud-based model when many are at universities with on-premise High Performance Computing centers. HPCs are typically partially supported by overhead, and so are “free” for compute time and storage. These users have very little incentive to move to a cloud system that costs much more out of pocket and gives them only transient access to the data.

#### Data Analysis
GTEx are working with ANVIL to enable the next dbGaP release of the data to be available in ANVIL/Terra.

### Training
Helpdesk tickets at GTEx are handled by everyone on the team as they come in, via their internal request tracker. This is an important feature because users can ask questions and get answers from the person who best knows a given topic. Many of the questions are “one off”, and range from simple to sophisticated, however they are skewed towards the basics. Many of the questions are not particularly GTEx specific, and instead are about how to conduct general bioinformatics analyses, for e.g. how to do RNA-Seq. This is something that training could easily address, however GTEx does not have the time or resources to create or deliver such training. It’s also not clear that it is something they should put resources into, when there are so many GTEx specific data analyses they could be teaching. 

GTEx also has several other ways they reach users. Their portal has documentation and a small FAQ, they have held a small number of in person workshops, and they host three videos on YouTube with a combined total of about four thousand views: 

* GTEx: Genotype-Tissue Expression 1062 views
* GTEx Portal: Introduction to the Gene eQTL Visualizer 2731 views
* GTEx Portal: Viewing Gene Expression Data on the GTEx Portal 469 views

GTEx has had mixed results from these training efforts. On the one hand, they know their users crave training and outreach. Their workshops are always over-subscribed, and their help desk system is always filled with new questions, however their user base does not seem to be getting more sophisticated. As previously discussed, much of their help desk traffic is users who need basic bioinformatics training, and another large segment is users asking questions whose answers could already be found in the portal. For these latter questions, it's not clear whether the problem is more about the site, i.e. the answers are difficult to find, or about the user, i.e. it’s easier/faster to email the helpdesk than to look for the answer. In either case, it is clear that a great deal of GTEx resources are going into supporting naive users who might be better served by a more general bioinformatics training resource. 

This is an issue as GTEx’s main goal with providing training is to increase the usage, and depth of usage, of their data. They want to enable their users to deeply understand the data, to increase their ability to use it on their own, and to increase the sophistication of the questions they answer with it. To that end, GTEx is very interested in running a hands-on API workshop. This would require some kind of library implementation, but would result in users with much more flexibility in how they query the data. As GTEx already has the expertise to build this workshop, this could be a potential burst funding investment compatible with the OT mechanism.

Their other workshops would likely benefit from some restructuring. GTEx is concerned that perhaps one reason they don’t see an increase in user abilities after workshops is that they try to cover too much, too fast, and that learners leave having learned many things, but at too low a depth to be useful. Rather than try to cover all topics, they would like to try having more workshops, but with each one covering a narrower set of topics. This is a workable goal, but GTEx doesn’t currently have the time or resources to spend on restructuring their lessons.

### Outcomes
GTEx hosts a widely used dataset for a community with a broad spectrum of both biological and computational abilities. They are interested in expanding their user base, but even more keen to expand their user’s level of bioinformatic sophistication. They are constantly striving to offer tools that allow a deeper and more nuanced view of their data without demanding additional computational expertise on the part of their users, and everyone at GTEx contributes to giving personalized user support.

#### CFDE Targets
* Mailing List: GTEx has a mostly defunct mailing list set up through Mailchimp. The CFDE could help revive and increase the reach of this mailing list to help with training and reaching out to users.
* Workshop Development: GTEx needs more targeted training modules, and some new materials. The Brown lab from CFDE can provide resources to rapidly develop the training materials, as well as some personnel for running workshops. 
* Reliable funding: GTEx cannot hire for 6 month projects. Steady, longer-term funding through the CFDE would give GTEx the ability to fix many of their blockers. 

#### Major Use Cases:
* Query by gene, query by variant, by tissue
    * A user can query and visualize sets of data
    * Ideally, this would include data grouped by protected variables (e.g. actual age (instead of age in 10yr intervals)
* Data download
    * A user can use the results of a visual query to download the raw data, or link it to an analysis platform
* GTEx API (usage is untracked currently) - REST API
    * A user can run the GTEx visualization tools on any dataset with the appropriate data types, independent of the GTEx platform
    * Ideally, this would be used not only by end users, but other DCCs and would foster interoperability between data centers

### Game Changers
During our discussions with GTEx we collectively came to realize that there are several ways the CFDE might significantly advance the state of NIH biomedical data management across all of the Common Fund DCCs by accomplishing a targeted set of goals that were not originally included in our proposal. If these goals are shared by most DCCs, we could positively impact their internal operations and make important new advances in data access and analysis for the NIH research community. These targets are labeled as "game-changers" because by accomplishing these innovations, the CFDE has the potential to dramatically improve the access and usability of an organized set of resources hosted at the Common Fund DCCs. 

1. __Reduced barriers to search across all data at dbGaP.__  GTEx has been very successful in working with their users to understand the challenges that users experience, and a continuous theme throughout our discussions was the frustration experienced by users accessing data at dbGaP. For example, in a recent survey they conducted users were asked:

> If we were able to integrate GTEx protected (dbGaP) data into the GTEx portal, would you find it useful to query and vizualize sets of data grouped by phenotype (e.g. actual age, medical history, genotype, etc.)? 

Of the 112 users who replied to their survey, 87.5% answered yes to this question. Users face many challenges in using dbGaP: 
* Applications for data are cumbersome, and users must submit a separate application for access for data at each Common Fund DCC 
* dbGaP data associated with individual dataset is very poorly documented
* Data file names from DCCs are idiosyncratically changed on upload such that neither users nor DCCs can tell whether they’re using the same file
* User interfaces for viewing that data are quite superficial
* There is no uniformity in the way that data is described from one project to another 

The GTEx staff were adamant that a critical need for their users would be reduce the administrative barriers associated with users to be able to access dbGaP data, to improve the user interfaces that enable researchers to query on those data, and to reduce or eliminate the barriers for users to compare dgGaP data across Common Fund projects. One relatively simple, but impactful, step towards this goal would be simply making public what fields of private data exist for each dataset.

2. __CFDE compliance, component 1: establish the minimal metadata for a resource object.__ GTEx staff recommended that an important development would be to create a standard that describes a minimal set of metadata for an individual file, such as an RNA-Seq file associated with their project. Implementation for this standard would not be complicated, and would simply involve an agreed upon electronic format and fewer than 8 metadata terms that are relevant to each file. The minimal metadata terms would likely include: originating institution (e.g., "Broad Institute"), file type, tissue source and species name for the sample, a unique identifier, and a checksum for the file. While many implementations for electronically encoded metadata for biomedical resources have been proposed in the literature, no standard has been adopted by the broader user community. The GTEx group suggested that given the position of the CFDE project among several DCCs, and the funding incentives that could be offered by the Common Fund, the CFDE has a high likelihood of achieving adoption across several groups. 

3. __CFDE compliance, component 2: resource object collection.__ The ability to bundle a list of CFDE resource objects into an machine-readable file was also highlighted in our discussions. These lists are similar in function to users collecting a shopping list on a commercial web site. In this case it would be useful for objects (such as RNA-Seq files) to be identified by user queries at the CFDE portal, and for the object list to be passed to other resources such as the GTEx web site (to retrieve the data), or to a computing analysis resource such as Terra. We refer to these lists as manifests, and similar to the minimal metadata description described above, implementation of the manifests will not be complicated. Potential implementations have been proposed in the literature, and the Kesselman and Foster teams also proposed utilizing the bdBag system for manifests during Phase 1 of the DCPPC. While a standard for manifests has not been adopted by the broader community, the CFDE project represents an excellent opportunity to create a standard for all of the Common Fund DCCs.  CFDE Cost Incentives: All senior GTEx members in attendance at the meeting concluded that an extremely important incentive to get their group, as well as other DCCs, to participate in the two compliance components described here would be for the NIH to offer CFDE cost incentives - e.g., reductions in storage costs on the cloud for DCCs where were compliant with those technologies. 

4. __A proof of concept: enabling other DCCs to use GTEx visualization tools.__ One potential use for adopting a CFDE manifest is that a collection of files could be transferred to other resources such as RNA-Seq analysis tools. The GTEx staff have previously developed several visual analysis systems that are available as downloadable tools for their users. These tools were originally created for users who wanted to combine their own data with GTEx and be able to perform analyses that were similar to information presented at the GTEx website. Users are able to install the tools, link them to their own data, and create high quality figures that can then be used in publications. One suggestion that emerged from our discussion was to link these tools to RNA-Seq files from another Common Fund DCC, using the CFDE manifest as mechanism. 

5. __A CFDE search plug in.__ Another benefit of all Common Fund DCCs adopting a single set of minimal metadata for a research object, and a common manifest for describing lists of CFDE data is that it would then be relatively simple to create a web based plug-in that could be provided to all of DCCs, to assist with accessing data between sites. The advantage to creating a common plug in for all of the sites is that it would reduce costs associated with multiple DCCs creating interfaces that perform the same function, and would simplify the user's experience by creating a single search tool. By having a single development team create the plug-in, it would also mean we could rapidly respond to changes to the underlying implementation of the minimal metadata standards and CFDE manifest system. 

6. __User Helpbot: a first point of contact help desk for all CFDE users.__ The GTEx group has been systematically tracking helpdesk requests over the past few years using an RT tracking system. The GTEx staff have also generated documentation, lists of Frequently Asked Questions (FAQs), and other materials. GTEx staff report that somewhere between 25-50% of the help desk questions reflect requests from users that are more related to basic bioinformatics questions, than they are associated with the GTEx dataset. The GTEx staff also noted that many of the submitted questions would be answered if users simply read the FAQs. This observation led to the realization that creation of the CFDE is likely to increase the help desk burden of all DCCs. In addition to creating new, potentially confusing, ways for users to combine data, the CFDE will draw additional users to all sites, many of whom may lack significant bioinformatics training. During our discussion the group realized that it would be of significant positive impact to create a common front-end “helpbot” service that would be available at all DCC web sites created for the CFDE. This service could potentially use AI approaches to first filter user questions, to see if questions could be answered from FAQ content, and to handle basic bioinformatic questions that were not related to any particular DCC. This "user helpbot" could significantly lower the support burden for each DCC, and unify the bioinformatic educational information supplied to CFDE users. 

7. __Reducing costs for FISMA compliance.__ The Federal Information Security Management Act (FISMA) defines a set of controls to protect computer information and operations from security breaches. Requirements include maintaining an inventory of IT systems, categorizing data systems by risk level, maintaining a security plan, utilizing security controls, conducting risk assessments, obtaining certification, and conducting continuous monitoring. These activities often incur more than $100,000 in costs to institutions obtaining FISMA compliance. However, the benefits to obtaining FISMA compliance is that each DCC would increase it's likelihood to host human protected data, obtain trusted partner status for managing data (even just metadata) that are currently hosted at dbGaP, and to share data with other FISMA-compliant DCCs. GTEx staff encouraged us to examine mechanisms that might be supplied from a centralized service that would help reduce the cost burden of obtaining FISMA compliance for these reasons. 

### Agenda
**MONDAY June 3, 2019 - Broad Institute – 415 Main Street Cambridge MA 02142**  
 *Room Location: 75A-11-Teton (11081)*  
**9:00am(ish)-9:30am - Introductions**  
**DCC Attendees:** Kristin, Jared & Francois  
Short introductions from engagement team members and attending DCC members.  
 
**9:30am-10:00am – GTEx DCC overview**  
**DCC Attendees:** Kristin, Jared  
Short overview of GTEx: Results from GTEx user surveys; User statistics; Data statistics; Current metadata harmonization; Current training and outreach
 
**10:00am-12:00pm - Goals Assessment**  
**DCC Attendees:** Kristin, Francois, Jared, Katherine Huang, Duyen Nguyen, Shankara Anand, Aaron Graubert  
GTEx to rank these goals by importance and potential timeline, followed by discussion around why they rank goals the way they do,
 
**Goals List:**

* Self-governed metadata standards
* Harmonized data
* Cross cutting metadata models
* FAIR assessment
* Authentication/Authorization
* Data Dashboards
* CF Data Portal
* Data Platform
* Training

**12:00pm-1:00pm – Lunch**
 
**1:00pm – 4:00pm Open discussion (with breaks)**  
**DCC Attendees:** Kristin, Jared & Francois  
Using the results of the mornings exercise and a collaborative format, iteratively discuss goals, blockers, etc., such that the DCC agrees that the engagement team can accurately describe their answers, motivations and goals.
 
**Topics:**  
Infrastructure (KA, JN, FA):  
* What has been your experience with uploading to the cloud?
* What challenges have you faced?
* How have you dealt with those challenges?
* How well does dbGaP work for GTEx?
 
Review of metadata (KA, FA):  
* What's metadata is important for your org? For your users?
* Do all of your datasets have approximately the same metadata? Or do you have many levels of completeness? 
* Do you have any data already linked to outside resources?
* What kinds of datasets would you like to link into your collection? 
* What implementation and schemas do you already have (or want)?
* What standards do you have (or want)?
* How do your users obtain metadata and raw data?
 
Use cases (KA, FN, JN):  
* What if any, use cases do you have documented? Undocumented?
* What things are users currently able to do with your data? 
* What things would people love to do with your data, but currently can’t (or can’t easily)?
* What are the challenges associated with those desired uses? 
 
Training (KA, FA, JN):  
* What training resources do you already have? 
* What training resources would you like to offer? On what timescale? 
* What challenges keep you from offering the training you’d like? 
 
User Interactions/HelpDesk (KA, FA, JN):  
* How do you interact with your users? Who on your team does these interactions?
* What kinds of issues to you most frequently handle?
* What lessons do you wish you could impart on users, but currently can’t?
* Does your org have any dream initiatives that could be realized with extra resources? What resources would you need?
 
Policies (KA, JN, FA optional if need the time):  
* How do users currently obtain access to your data? 
* What are your concerns about human data protection? 
* What potential challenges do you see in bringing in new datasets?
 
FAIR (JN, KA):  
* Are there any aspects of FAIR that are particularly important for your org? 
* Are there any aspects of FAIR that your org is not interested in?
* What potential challenges do you see in making your data more FAIR?
 
**TUESDAY June 4, 2019**  
 *Room Location: 75A-5-Biscayne (5021)*  
**9:00am-12:00am Review of goals and CFDE involvement**  
**DCC Attendees:** Kristin, Jared & Francois  
Review of what topics are priorities for GTEx, and discussion of where and how they would utilize extra personnel/money/other resources
