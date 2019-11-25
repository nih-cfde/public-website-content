**AIM 1 - An assessment of potential linkage of DCC-to-DCC assets.**  
One premise of the CFDE is that it will enable linking between data assets hosted by two different DCCs, and that jointly analyzing those data will result in meaningful results that ideally are of publication quality. This Aim will test this premise, and determine the extent of work that is required to enable linking between two large-scale data generation projects. 

GTEx and Kids First have similar types of data (genotypes and vcf files, RNA-Seq expression data, variant calls, sample types, etc). Both DCCs have utilized separate, and possibly incompatible, best practices approaches for grooming these data, so compatibility of the assets at each site must be evaluated before any analysis is done. To determine if it is feasible to co-analyze assets hosted at each DCC, we will perform the following activities:

* determine if the identifiers used by each site to reference genes in the human genome are the same, compatible, or mutually incompatible;
* determine if identifiers that describe gene variants are the same, compatible, or mutually incompatible;
* identify tissues and cell types that are shared between the two DCCs;
* review the formats of VCF files, and establish whether the pipelines that were used for generation of those files are compatible;
* review whether the quality control and gene count pipelines for RNA-Seq data are the same (which is quite unlikely), and if not, whether they are compatible; 
* for each of the above assessments, determine what steps, if any, will need to be taken in order to make the data compatible

Note, this Aim refers to the data assets host at each DCC. It does not refer to their metadata. 

**AIM 2 - Compare pediatric ‘normal’ to GTEx adult normal gene expression data.**   
To gain insights into changes in gene expression by age (child vs adult), which will be useful to better understand drug targeting in patients, we will evaluate gene expression data of normal tissue from adult at GTEx versus pediatric samples at Kids First. We assume human protection issues would not allow Kids First data to be displayed at GTEx. However, we will also generate mock ups of how these results could be displayed using visualization tools at GTEx, in a scenario where sharing of human protected data was possible. 

As described in Aim 1 above, Aim 2 is dependent on the premise that genes can referenced at each DCC can be mapped, and that the expression levels described at both DCCs are appropriate for comparison, or can be made so.

**AIM 3 - Integrate structural, and other, variants with gene expression data.**  
We will evaluate structural variants derived from studies at Kids First, and review the consequences of these variants in the context of expression. Using variant data we will define the genes that are knocked out, and use GTEx data to ask which of those genes are associated with tissue specific expression. We will evaluate if that tissue expression corresponds with disease phenotypes for any of the genes, if there eQTLs for those genes, and if effect size or direction inform our understanding of what occurs in a heterozygote.

Results will be evaluated, and we will also generate mock ups of examples for how results could be displayed using GTEx visualization tools. For example, we expect that at GTEx, we can query a gene, display all the known disease mutations from Kids First for that gene on the genome browser, and determine whether those genes can be mapped to eQTLs, splice-QTLs, chromatin marks or methylation sites. We will also test for tissue specificity of the effects, and if they match phenotype specificity. 

As described in Aim 1 above, Aim 3 is dependent on the premise that genes can referenced at each DCC can be mapped, and that the expression levels described at both DCCs are appropriate for comparison. 

**COST ESTIMATION**  
This project will require 1 Bioinformatics Analyst for data analysis and quality control, and 2 Software/Bioinformatics Engineers, 40% effort from a senior level supervisor and 6 months of computational support. Based on using the high range for salary estimates:

Administrative / senior supervisor: $170,000  
Software or Bioinformatics Engineer: $130,000  
Bioinformatics Analyst: $110,000  
Computing costs: $1800/month

Total costs are approximately $448,000 for each site, totaling: $897,600
