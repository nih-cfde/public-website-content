**Location:** 300 S Craig St, Pittsburg, PA 19107  
**Date:** Tuesday September 3, 2019  
**Attendees:** Representatives from CFDE included Amanda Charbonneau (UCD), Brian O'Connor (Bionimbus), Steve Edwards (RTI), Titus Brown (UCD), and Owen White (UMB). Representatives from HuBMAP included Jonathan Silverstein (PI), Nick Nystrom (PI), and Robin Flaus Scibek (Project Manager). We were also intermittently joined over Zoom by the HuBMAP Project Officers and Project Lead from NIH: Tyler Best, Ajay Pillai and Richard Conroy.

Table of Contents:  
[Meeting Logistics](#user-content-meeting-logistics)  
[HuBMAP Overview](#user-content-hubmap-overview)  
[Program Lifestage](#user-content-program-lifestage)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Infrastructure](#user-content-infrastructure)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Analysis](#user-content-analysis)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Access](#user-content-access)  
[Harmonization and Metadata](#user-content-harmonization-and-metadata)  
[Sustainability](#user-content-sustainability)  
[Training](#user-content-training)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Internal](#user-content-internal)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[External](#user-content-external)  
[FAIR](#user-content-fair)  
[Common Fund Program Cross-pollination](#user-content-common-fund-program-cross-pollination)  
[SSO](#user-content-sso)  
[Outcomes](#user-content-outcomes)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Infrastructure Reuse](#user-content-infrastructure-reuse)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Challenges](#user-content-challenges)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Potential Solutions](#user-content-potential-solutions)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Potential Projects](#user-content-potential-projects)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Game Changers](#user-content-game-changers)  
[Agenda](#user-content-agenda)  

### Meeting Logistics
We held a meeting with the Infrastructure and Engagement Component (IEC) of the HuBMAP Integration, Visualization, and Engagement (HIVE) Collaboratory at the Pittsburgh Supercomputing Center on Tuesday September 3, 2019 for a day and a half. During the meeting, we used the agenda at the end of this document as an informal guide for structuring the day. 

The engagement team began by reviewing their goals for the meeting. These goals include learning more about: 
* Structure and goals of HuBMAP, including specifics about the data they host
* Information about training and organization
* Overall set of priorities for their group

Prior to our discussion regarding the HuBMAP program, the engagement team presented an overview of the proposed projects for the CFDE in 2020 as requested by our HuBMAP hosts. The HuBMAP team then provided a brief overview of the current structure of the HuBMAP program and how it has evolved since the launch last November. This was followed by a discussion of their proposed infrastructure for housing HuBMAP data. 

Day 1 concluded with a brainstorming session on what role CFDE could play in supporting the HuBMAP program. Day 2 focused these discussions with the goal of establishing a set of concrete actions whereby the CFDE could add value to the HuBMAP program.

### HuBMAP Overview
The goal of the Human BioMolecular Atlas Program (HuBMAP) is to develop an open and global platform to house a molecular atlas of the human body at cellular resolution beginning with foundational maps from 8 tissues: bladder, kidney/ureter, colon, lung, lymph nodes, spleen, thymus, and vasculature. HuBMAP complements an earlier effort to study gene expression across many tissues (GTEx) by generating single cell level data on a smaller number of subjects. The program is organized into three components:
1. Tissue Mapping Centers (TMCs)
2. HuBMAP Integration, Visualization and Engagement (HIVE) collaborative components
3. Innovative Technologies Groups (Transformative Technology and Development (TTD) and RTI)

The five TMCs (Caltech-UW, Stanford-WashU, UCSD, University of Florida, and Vanderbilt) are responsible for generating high-quality data at scale with standardized metadata annotations. This will include single cell ‘omics assays that compare chromatin-level changes with changes in expression of biomolecules at the cellular level. These studies will be combined with molecular-level analysis of tissue blocks using imaging methods such as fluorescent microscopy, sequential fluorescent in situ hybridization, imaging mass spectrometry, and imaging mass cytometry. In all, there are over thirty data modalities that will be employed by the TMCs. The tissues are derived from healthy human organ donors with the caveat that death of the donor will impact even healthy organs depending on the cause.

The data generated from the TMCs will be integrated and disseminated by the HuBMAP Integration, Visualization, and Engagement (HIVE) Collaboratory, which consists of five components of three types: 

| Component | Organization(s) Included | Responsibilities |
|:-|:-|:-|
| Infrastructure and Engagement Component (IEC) | Pittsburgh Supercomputing Center and University of Pittsburgh | Housing all data from the HuBMAP program, providing compute capacity for analysis of the data, and coordinating the efforts of the consortium. |
| Two Tools Components (TC) | Carnegie Mellon, Harvard Medical School | Providing tools that allow users to visualize and analyze the data generated by the HuBMAP program. |
| Two Mapping Components (MC) | Indiana University Bloomington, New York Genome Center | Developing the common coordinate framework to allow exploration and visualization of results from different individuals, technologies, and labs. |

The original arrangement of the HIVE had the Collaboration/Engagement activities separated from the Infrastructure Component. These activities were merged in summer 2019 with the Pittsburgh Supercomputing Center and University of Pittsburgh becoming the new Infrastructure and Engagement Component (IEC). Efforts for all HIVE components are coordinated by the IEC to ensure a unified user experience when interacting with HuBMAP data. In addition to collecting data from the members of the HuBMAP consortium, the HIVE has also been tasked with integrating data from related projects such as the Human Cell Atlas with the data generated by the HuBMAP program.

Whereas the emphasis of the TMCs is to generate large amounts of data using state of the art technologies, the Innovative Technologies Groups are focused on identifying new approaches that will complement and extend the existing technologies. The Transformative Technology and Development (TTD) investigators at the California Institute of Technology, Harvard, Purdue, and Stanford will establish proof of principle and validation of next generation tools to expand throughput, multiplexing, and discrimination of biomolecules in human tissues. The Rapid Technology Integration (RTI) organizations will be launching soon and are responsible for implementing new technologies in the HuBMAP consortium. 

### Program Lifestage
The HuBMAP program is completing its first year, and production phase for data generation is scheduled for 2022. However, the consortium is planning an initial data release in mid-2020. The first year of the HIVE has mostly been used to create teams and working groups to manage the many moving pieces that comprise HuBMAP. The HuBMAP HIVE also has a mandate to collaborate with other atlas projects and integrate data from those projects with the HuBMAP data. As a result, the HuBMAP HIVE will likely have a CFDE-like role for cellular level body atlas data. 

As part of their planning phase, members of the HIVE have visited all the TMCs to determine the datatypes expected from each and the estimated timeline for data availability. They have recently established data release teams for each datatype (e.g., RNA, Histology, proteomics) to coordinate the data ingestion, processing, and release and portal release teams to focus on developing the web site (UI), infrastructure, and APIs (Application Support Interfaces) that will allow automated data access. These teams each consist of 5-10 people and are currently establishing metadata standards and acceptable file formats. This effort is complementary with the activities within the MC regarding semantic and spatial descriptions of the anatomical locations including defined integration points between the efforts. The Portal Release Team has adopted a scrum-based software development approach with sprints beginning in September 2019.

The overall HuBMAP consortium is guided by a steering committee that meets once a month. Under that are five working groups focused on policy, communications, data science, technology, and tools with representation from each HuBMAP awardee on each group. Additional teams are set up that include ad hoc members from the TMC, TTD, and HIVE components to carry out the work. This results in 3-4 meetings of various types every week, across the formal consortium-wide calendar. High-level decisions are made at the working group level with oversight from the steering committee and implementation plans developed by the individual task teams. All workstreams flow into two structures: product owners who determine what should be developed and technical contacts who determine how it will be built. This structure has recently evolved toward the conclusion of the initial year of the project as the IEC took on coordination and engagement inside and outside the HuBMAP consortium.

#### Infrastructure
The HuBMAP IEC is using a hybrid of on-premises and cloud computing for the HIVE. The Pittsburgh Computing Center is a leading partner in XSEDE (Extreme Science and Engineering Discovery Environment), the National Science Foundation (NSF) cyberinfrastructure program. With funding from the NSF, they have developed the Bridges resource that brings together high-performance computing (HPC), AI and Big Data to support applications including genomics, machine learning, graph analytics, image processing and materials science. They are still working on FISMA certification, but they are certified on other projects and do not anticipate this being an issue.

This existing infrastructure allows them to provide some services at a small fraction of the cost of hosting on AWS. From the perspective of HuBMAP, a vast amount of compute capacity is freely available to academic and non-profit researchers through 2029 as part of the XSEDE program and the recent renewal of Bridges. Although this on-premises solution is local, it was built to be interchangeable with cloud computing systems, so HuBMAP can push jobs to AWS or other commercial cloud providers anytime additional compute capacity is needed. The IEC has had discussions with STRIDES regarding the fiscal management of the cloud component of their hybrid solution, but this is delayed due to factors outside of the control of HuBMAP.

The biggest savings for an on-premises solution is in storage. Given the scale of the existing resource, they can time purchases of new storage to match the anticipated receipt of data from HuBMAP researchers. This eliminates the typical advantage of on-demand storage from a cloud provider and makes hosting their own storage much more cost effective. The size of their operation also allows them to build in redundancy and mirroring backups that offset the risks associated with data loss from local storage vs. the cloud. They do not anticipate problems with the ever-growing storage demands, because the cost of storage tends to decrease in parallel with the increased storage requirements. 

The data ingestion portal is being built now. The infrastructure behind this is a microservices architecture heavily using APIs and a combination of technologies: a Neo4j graph database for provenance, NOSQL for metadata indexing, and Globus for data management and security of APIs. The HIVE will collect raw data for the more common methodologies, but they may only collect processed data for the less common datatypes. For example, raw mass spectrometry files from the Vanderbilt group require specialized software to open and are not broadly useful until after processing. In this case, the HIVE will receive the results from Vanderbilt’s initial pre-processing and analysis. For methods that are being implemented across multiple TMCs, however, there will be a common analysis pipeline within the HIVE to provide reproducible results across all the TMCs. The TMCs may still perform their own analyses for their publications, but the data provided by the HIVE will be consistent across TMCs. There is some tension between when/where to get their pipelines into production within the HIVE. The further away from data generation they get when running processing pipelines the more context gets lost. For this reason, the HIVE is paying close attention to tracking the provenance of all data both prior to and after deposition in the HIVE. 

#### Analysis
The analysis tools for the HIVE are being developed by separate components, but the IEC is responsible for providing the compute platform and data in a computable form. The production phase of HuBMAP doesn’t begin until 2022, so many of the issues surrounding this are still under discussion. Containers are likely to be a big part of the solution both for the initial processing of the data by the IEC and the downstream analysis and visualization tools built by the TC. However, there is still a great deal of discussion within their consortium about data formats and specifications as well as what specific technologies to implement.
The Portal Release Team has been tasked with defining a vision for handling both initial data analysis by the IEC and analysis tools developed by the TC. They will evaluate resources such as Kubernetes and Airflow, but the general challenge is how to hook back to the compute allocations and not go over budget. There is a small amount of funding for this allocated in year 2 of the program. 

One key specification for designing the workflows will be ensuring they work with the hybrid infrastructure. While some workflows can run entirely on the HIVE local infrastructure, that same workflow on a very large dataset may need to start locally and then move to the cloud for some steps of the analysis. HuBMAP workflows will need to account for the possibility of these ‘burst runs’ in the cloud and be able to push data into cloud temporarily and then vaporize. While the cost associated with moving data into the cloud is free, the time required for large datasets could be considerable. The workflows must optimize the stage in which data are transferred to the cloud to minimize the lag associated with large data transfers.

#### Access
All data received from TMCs will be processed and made immediately available back to the TMC, however the infrastructure will support embargos for other users based on the data sharing policies established by the HuBMAP Steering Committee, which are focused on public releases having proper quality assurance and moving data to public or appropriately restricted access based upon IRB/consent limitations as soon as possible. Data embargos will not be used to protect private research. Access to resources, including whether data can be downloaded or accessed, including open public information, is managed through Globus groups.

HuBMAP plans to offer their users some level of computing resources for free through the XSEDE program, but they do not have unlimited capacity. As free services will need to be limited, an open question is who should have access to these free services, at what level, and for how long. For example, HuBMAP plans to allow people to easily bring their existing data into the HIVE and do joint analysis, but users bringing in large datasets will require a lot of resources. The obvious solution would be to give each user some amount of credit and then charge for use, however this is complicated by HuBMAP’s relationship with XSEDE, as XSEDE is prohibited from charging users. One possible solution would be to allow users to use common workbenches such as CAVATICA and TERRA, which are linked to AWS billing, while another may be ensuring that users can export data with minimal friction to public cloud infrastructures for their own analysis. 

### Harmonization and Metadata
HuBMAP IEC is using the Unified Medical Language System and other open ontologies for canonical metadata. The IEC told us that Metadata standards within the HuBMAP program are a big enough challenge in the short term and trying to adhere to outside requirements (e.g. imposed by the CFDE) would be a distraction, so their main focus is how to accommodate the diversity of data and data formats coming from the TMCs. At the HuBMAP kickoff meeting, the NIH Director challenged the HuBMAP consortium with determining how to represent single cell data consistently across many different organs and tissues. There are ongoing discussions within the HuBMAP working groups to define the standards within the program, and they are trying to standardize the file formats to the greatest extent possible. In many cases, however, the file formats are determined by the equipment that generates the data. 

The IEC indicated that they would be willing to participate in discussions with the other Common Fund Programs to promote interoperability, but they believe that the fundamental notion of defined metadata by consensus upfront is wrong. For example, they have experience translating multiple Electronic Medical Records stored in multiple different systems into a common metadata model. However, they find that the systems give different results over the same events, even though the underlying data model is identical, because translation to the model involves substantive data loss. This reinforces their position that “conference room” metadata harmonization ultimately fails for many purposes. Rather, flexible information sharing approaches (via APIs and other data interchanges) are the focus required to support users of those data to transmute those data for their interoperational purposes. In short, combined analysis will always require deep knowledge of the original dataset. Of course, integrated data will be presented but it must not be the exclusive goal.

### Sustainability
The HuBMAP project is the newest of the Common Fund programs, so their perspective is quite different from many of the other Common Fund Programs that have been interviewed thus far. The HuBMAP program is currently funded through the OTA mechanism, and expects to be funded for eight years. It isn’t clear whether the 10-year limit on Common Fund grants will apply to this mechanism or whether there will be a future opportunity to continue support for the HIVE under a different mechanism. The IEC investigators are very happy with the OTA mechanism thus far. They noted that all changes in scope for the project have been coupled with supplemental funding to support the work. The largest of these was when the IC took over the engagement activities from the CC this summer. However, the OTA includes a much narrower description of what needs to be accomplished with the funds, so there is a little less flexibility in implementation compared with a grant. With the ongoing support for compute infrastructure from the NSF XSEDE program, they do not anticipate any issues with data access during the lifetime of the HuBMAP program. They plan to stand up a Data Access Committee to handle governance of the data dissemination once data starts coming in next year.

### Training
#### Internal
During the opening presentation at the HuBMAP kickoff meeting, Richard Conroy (program officer) acknowledged the complexity of HIVE and the corresponding challenge of coordinating the multi-site effort: “It’s complex but that complexity is expected.” The first year has been heavily focused on getting committees and working groups in place to coordinate the disparate efforts while simultaneously trying to get the individual efforts started. They anticipate that merging the Infrastructure and Engagement components will streamline operations, and now have most of the committees and working groups established. Robin is now leading the engagement portion of the IEC, which includes all the training activities. The first year of the HuBMAP program does highlight the increasing complexity associated with the large Common Fund programs. 

The HIVE is using the following technologies to coordinate activities and disseminate information:
* Zoom - Video conferencing
* GitHub - version control and issue tracking
* Slack - Team communications
* E-mail
* Protocols.io - Capturing experimental protocols and computational workflows
* Asana - track NIH milestones and project management

While the IEC has technologically solved the problem of communication across a distributed consortium, they are experiencing some common social communication issues, primarily in getting everyone to buy-in to the technology. For example, they noted that onboarding consortium members to services like Asana, and convincing them that the effort needed to learn that service is worthwhile, were ongoing pain points. The IEC also distributes a weekly newsletter to all members of the consortium, but struggles to get people to contribute content. This forces the IEC to devote extra time and resources to finding and compiling noteworthy news.

#### External
The HIVE goal is to provide sufficient compute options such that most users will use online tools rather than downloading the data. Since the instinct for users is to download data and work locally, this will likely be a significant challenge. The IEC told us that since the Tools Components are building the online tools, they expect that most of the training for those tools will be developed by the TCs. 

Instead, the IEC plans to focus on documentation. A key question when designing tools and training to support data access is who the user of the data will be and what support will they need. The IEC pointed out that while providing tools that would allow anyone to meaningfully interact with the data is a laudable goal, they must face the reality that at a certain point they would invest more resources designing tools to support naive users than society would gain from what they are able to do with the data. They argue that anyone who is serious about successfully utilizing the data from HuBMAP will invest the time and energy to understand the data and how to access it regardless of how the data are shared, and that a deep understanding of the data is necessary when performing a secondary analysis to avoid making assumptions about the data collection that are incorrect. As such, they plan to build and document flexible APIs enabling motivated users to use tools that are as simple as fit the tasks. 

Given the early stage of HuBMAP, they have not established a training plan yet, but they do have a lot of previous experience with training. They have previously developed training for onboarding to the system as part of the XSEDE program, but the login, set up, onboarding, etc. is sufficiently different that the HuBMAP training will be assembled from scratch. In terms of how to train, they have a great Wide Angle Classroom setup that allows them to have a single instructor to teach several virtual classrooms simultaneously. They plan to leverage their current XSEDE centers that already have TAs, rooms, etc. to pilot any future training initiatives. They are also considering Massive Open Online Courses (MOOCs) as another option. 

### FAIR
The HuBMAP HIVE is dedicated to the FAIR principles but have not yet documented clearly what that means in terms of implementation. For their part, all data in their portal will be accessible programmatically via well-documented APIs, and they are in the process of determining what minimum requirements for metadata would allow users to find and understand the data provided. They are also interested in ensuring that their workflows are reproducible and transparent. They noted that it would be useful to know how different Common Fund Programs are handling workflows and which ones are attempting to document and disseminate workflows for reproducibility purposes. They are considering Zenodo or Dockstore as potential repositories for sharing workflows. 

The HIVE was given a mandate to interoperate with other consortia, and as the TMCs have a heavy focus on lung and kidney, the LungMAP and GUDMAP consortia are logical choices. However, the Human Cell Atlas (HCA) program is the highest priority source of non-HuBMAP data in the short term, and there is a joint meeting planned for HuBMAP and HCA from March 31 through April 1, 2020. They have evaluated the HCA annotated metadata model and what it would take to incorporate HCA data into the HIVE, however it is not the highest priority because the effort expended on this can’t pull resources away from the core effort required to launch the portal to support ingestion of HuBMAP data beginning next year. While the NIH wants to see cross-program analytics, the HuBMAP budget for this effort is only $75K at the moment. 

In the short term, HuBMAP would rather focus on pairwise interactions with efforts such as HCA rather than trying to enable a cross-program multi-DCC portal. They emphasized the need to better explore how the data can be combined and used before trying to build tools that support the process. They expressed skepticism that users interested in superficially combining datasets across Common Fund Programs would gain much from a multi-DCC portal. In their view, successful data integration will require a talented and motivated user with a deeper understanding of the data, which would necessitate working with the original data sources.

### Common Fund Program Cross-pollination
The IEC told us that they have limited time for general collaboration and would likely not attend Common Fund cross-pollination events without specific foci and benefits to participants. They expressed concern that a large event would not provide the right conditions for fostering relationships, and the time they invest in attending would be wasted. However, they said they would be very interested in meeting with individual programs and building pairwise collaborations, especially if they were given some outside direction about what programs would be best to work with.

They have a year 2 mandate to bring public data into HuBMAP, but have invested little time to research potential collaborations with other DCCs. The HuBMAP program is focused on normal tissue, and they would be most interested in opportunities to build a federation with repositories that include diseased tissues. They noted that they would even be interested in collaborations with sunsetting programs and would be willing to integrate older data into HuBMAP. 

### SSO
HuBMAP uses Globus for all security, including Federated identity management, data movement, sign on for their portal, application, and even workflow, pipeline, and query API permissions (via passing authorization tokens). They have successfully used this for the XSEDE program in the past. Globus includes ORCID and ERA Commons as authentication sources, so they view this as meeting the NIH requirements for SSO. 

### Outcomes
#### Infrastructure Reuse
Although many Common Fund Programs are opting for cloud-based infrastructure, HuBMAP’s hybrid cloud model employed by the HIVE could be more broadly useful within the Common Fund. The hybrid model works well for HuBMAP because they already have a great deal of expertise, infrastructure, and connections. From their work with XSEDE and the Pittsburgh Supercomputing Center, the IEC staff have tens of years of experience in designing, maintaining and administering large complex computing systems at scale. 

They also have the space to store these machines, as well as dependable high-throughput fiber internet connections, electrical systems that can reliably support thousands of supercomputing processors, and staff that can maintain it all. Finally, they have vendor agreements and connections in the industry that they can leverage to purchase software and hardware at volume for a substantial discount. By leveraging their existing expertise and resources from XSEDE, HuBMAP was able to dramatically reduce their computing costs. 

Although HuBMAP’s hybrid infrastructure is working well for them, it may not work for all Common Fund programs. While getting contracts for inexpensive storage is relatively easy, the services required to keep them secure and running smoothly need to be maintained and refreshed periodically, and require specialized knowledge, as well as a lot of underlying site infrastructure. In general, for smaller systems at organizations without an existing infrastructure, cloud solutions provide a cost-effective way to implement a robust system without a large, upfront hardware and IT investment. 

As the size of the system increases, the cost considerations shift such that for larger programs, the initial investment in hardware and IT support is cheaper. In the case of HuBMAP, the size of the program makes it more cost-effective to host the system locally. In addition, both the infrastructure and expertise already existed at the Pittsburgh Supercomputing Center because of their ongoing work as part of the XSEDE program. It also is unclear how the hybrid infrastructure will impact data accessibility when HuBMAP funding ends, however their current system is built to seamlessly move data to the cloud for extra compute capacity, so it shouldn’t be difficult to transition the data to the cloud if Common Fund decides to go that direction.
 
The wide-angle classroom technology that HuBMAP is planning to use may also be useful to other Common Fund Programs. This technology is similar to a webinar in that a single person can present a lesson, and it will be broadcast to many locations. However, the system is much more interactive than a typical webinar. Each classroom receiving the broadcast is outfitted with cameras which display back to the presenter, such that the instructor can see all of the learners and react to questions individually, much like they would in a standard classroom. Each receiving classroom also is staffed by a small number of teaching assistants who can help troubleshoot and fix problems locally. 

By investing in creating compatible classrooms at several locations around the world, they have substantially reduced the number of teachers required to have a worldwide presence. The XSEDE program currently offers training on a regular basis in several countries, with just a single instructor.

#### Challenges 
The HuBMAP team highlighted a number of challenges faced by the increasingly complex centers that coordinate these large Common Fund Programs, and we had a productive discussion regarding how CFDE could potentially assist in overcoming those challenges.

* HuBMAP is a multi-component, multi-organization, collaboration similar to CFDE in scale, but huge complex projects take much longer to ramp up, and there are thousands of decisions that go into building their infrastructure. This highlights the need for assistance during the first year, as well as a Common Fund Playbook and list of best practices to guide those decisions. 
* While the FAIR principles are clear, there is concern that if the CFDE attempts to normalize the implementation across different programs, it will create an unneeded hardening of the requirements, which will reduce the flexibility for the individual programs to implement FAIRness.
* The HIVE IEC expressed concerns about the zeal to create tools for merging data across different programs. They worry that the further the analysts are from the origin of the data, the more likely they are to misuse the data. GTEx expressed similar concerns during their site visit.

#### Potential Solutions
* Training and Support
    * Create a playbook on challenges that result from the increasing complexity of the Common Fund Programs. Provide CFDE assistance to help new programs during their first year. Promote sharing of best practices among Common Fund Programs.
    * Contact the TCs to discuss training for their tools
    * Create a decision tree to assist new Common Fund Programs in selection of on-premises, cloud, or hybrid solutions based on the experiences from the existing Common Fund Programs. Provide CFDE support and connect new Common Fund Programs with existing Common Fund Programs as needed to provide additional details.
    * Establish practical guidance on the implementation of FAIR principles. Documentation for new Common Fund Programs and CFDE helpdesk support to field questions.
* Enable data aggregators
    * The HIVE has a mandate for incorporating single cell atlas data from outside as well as inside the HuBMAP consortium. CFDE could provide support for these applications and establish a community of Common Fund Programs to share best practices and identify partnership opportunities.
    * CFDE could establish a pilot project with the HIVE to establish a proof of concept for Common Fund data aggregators. The HIVE has a mandate to incorporate HCA data, but the funding for this is minimal. CFDE could support the development of this resource and document the process for the benefit of future Common Fund Programs should they be given a similar mandate.
* Promote pairwise interactions
    * The CFDE can identify people from different Common Fund Programs who could usefully interact about specific topics, and provide introductions as a way of beginning to build community connections without requiring a lot of time or effort on the part of the Common Fund Program PIs.
* Pilot Projects 
    * CFDE could promote pilot projects whereby two or more Common Fund Programs collaborate to demonstrate the value of integrating data from disparate sources. These should be science-driven and not too theoretical. The goal is to have pilot projects that are indicative of the types of questions researchers would ask rather than projects driven by a general desire to show utility. These pilot projects would result in the following benefits:
        * Demonstrate utility
        * Highlight the costs associated with specific analyses and help determine the best mechanisms for covering those costs.
        * Create detailed use cases to drive future CFDE tool development
        * Help to clarify policy questions about who gets access to a resource, what level of access to grant, who pays for it, etc.

#### Potential Projects
* CFDE could develop a set of case studies to illustrate science-driven data reuse/analysis. This could include small grants to the larger research community to support postdocs who want to analyze data from two or more separate sources. It would also include support for members of the chosen data sources to assist with the interpretation and use of the data.
    * HuBMAP is interested in connecting their data from normal humans with disease data. HCA has some disease data in addition to the normal core work.
    * Could also consider projects that bring in a small amount of data from an R01 or equivalent and then try to leverage data from these larger projects to provide additional context for those data.
    * Possibly model this after the NCI ICTR (https://itcr.cancer.gov/) program.
    * The Kids First/GTEx collaboration is a model for these case studies. Identify a dataset or two available in this time frame.

#### Game Changers
The OTA funding mechanism has allowed HuBMAP to adapt much more readily than other Common Fund Programs. This, coupled with the early stage of their program, meant that they are not in a good position to recommend game-changing opportunities for the CFDE at this time. Most ideas stemming from our brainstorming are likely to benefit future Common Fund Programs more than the HuBMAP program. However, there was one new area where CFDE activities could enable HuBMAP to more easily incorporate non-HuBMAP data. 

***Enabling data aggregators.*** As noted previously, the HIVE was given a mandate to incorporate other human atlas data that would complement those being generated by the HuBMAP program. While they’ve received a small amount of funding to support these activities, their primary responsibility must be on preparing the HIVE to accept HuBMAP data as is becomes available. If CFDE could facilitate the incorporation of the HCA metadata model into the HIVE provenance model and thereby facilitate the ingestion of HCA data, that would greatly increase the probability of success for that effort while providing valuable information about how this should be done in general. 

***Creating a lifecycle support program for Common Fund Programs.*** While they have worked through the process of coordinating a large, complex effort such as HuBMAP during their first year, they acknowledged the potential benefits of having access to lessons learned from prior Common Fund Programs at the beginning. They are also looking ahead to the training required as the HuBMAP data become available to users. They would welcome assistance in this area and were enthusiastic about the idea of a tiered help system that would shield the HuBMAP training team from general questions about bioinformatics or data access. While end of life for the HuBMAP program is not an imminent need, they acknowledged the need for the CFDE to provide solutions that avoid any data from a Common Fund Program being lost to the research community. They also offered their platform as an option for programs that are reaching end of life who have data that would be compatible with the HuBMAP data models.

***Building a Common Fund Program community.*** The HIVE IEC recognizes that even within the single cell body atlas space, it is highly unlikely that a single repository will ever house all the data. They are interested in collaborating with other related programs to build a data federation whereby the data from separate repositories can be assembled without unreasonable effort. They would be willing to participate in CFDE organized Common Fund Program communities with this goal in mind as well as to benefit from the collective knowledge of the community.


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
* CF Data Portal
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

