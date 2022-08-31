![MGnify](images/mgnify_logo_vf2.svg)
# Practical 2: MGnify services

For this session we will look at some data and analyses that are available from MGnify. We will navigate the resource, try out different ways to search for interesting samples/studies, and then investigate the analysis results that are available.

### Browsing MGnify

From the MGnify front page (https://www.ebi.ac.uk/metagenomics/) you can see various options to browse the data. There are quick links to the various data-types (e.g. amplicon, assembly, metagenomes, etc) we support, as well as a subset of the biomes that the data covers.

1. Click on the "Digestive system" biome icon.
There are several options for searching data in MGnify, including this browse data view.

![Question](images/question.png) How many studies are related to the human digestive system?

#### We will search for studies related to the human digestive system biome with the search term 'dietary'.
2. Enter 'dietary' in the search terms.

![Question](images/question.png) How many of those previous studies have the phrase 'dietary' in their study title or description?

3. Select study MGYS00005742 

![Question](images/question.png)  Where do these samples originate from?

4. Under publications select the Europe PMC annotations

![Question](images/question.png)  What, if any treatments are mentioned as included/excluded in the related publication?


### View amplicon analysis outputs
5. Scroll to analyses and select the first analysis accession 'MGYA00583656'
6. Click on the sample accession

![Question](images/question.png)  
What is the ENA sample accession?

What is the BioSamples accession?

From BioSamples ENA or MGnify find the latitude and longitude of the sample.

7. Navigate back to analysis 'MGYA00583656' and browse the other available tabs

![Question](images/question.png)  
How many reads remain after quality control?

What is the maximum sequence length (bp)?

Which bacterial phylum is most prevalent in this sample?

How many matches are there to the 'Bacteroidetes' phylum?


### View samples programatically 
Another way to view sample metadata is using the API and MGnifyR

8. Navigate back to study MGYS00005742
9. Under programmatic access, select 'Open study in R'

This will open an R notebook to access a study, and it's metadata.
10. Scroll to section 'Fetch a list of the Analyses for the Study'
11. To the code block add the line ```analyses_accessions <- head(analyses_accessions)```
12. Start at the beginning now. Following the instructions: To run this code, click into each cell and press the ▶ button in the top toolbar, or press shift+enter.

You should have a metadata table for the first 6 samples and some diversity graphs.

![Question](images/question.png)  
What is the largest number of predicted SSU sequences in these 6 samples?

What sequencing platform and model was used?

Which sample has the highest observed taxa (Richness)?


### View assembly analysis outputs
13. Now, search for the analysis MGYA00595418. You can use the text search to find this accession. Have a look at the functional analysis tab.

![Question](images/question.png)  
How many predicted coding sequences (pCDS) are in the assembly?

How many pCDS have InterProScan hits?

14. Scroll down the page to the InterPro match summary section.

![Question](images/question.png)  
How many InterPro entries are matched by the pCDS?

Why is this figure different to the number of pCDS that have InterProScan hits?

15. Click on the GO Terms sub-tab. This shows a summary of the most common GO terms annotated to the pCDS as both bar charts, and pie charts.

![Question](images/question.png)  
What is the top biological process predicted for the pCDS from this assembly?

16. Click on the Pathways/Systems tab. Have a look at the data reported in the 3 sub-tabs: KEGG Module, Genome Properties, and antiSMASH.

![Question](images/question.png)  
How many KEGG modules are reported as 100% complete for this assembly?

How many Genome Properties of the category DNA handling, are found within this assembly?

What is the most common class of biosynthetic gene cluster detected by antiSMASH found in this assembly?

17. Click on the Contig Viewer tab. Load the data for the 4th contig in the list by clicking on the contig name (ERZ5381791.4-NODE-4-length-260716-cov-21.822620:1-260,716). This contig will now be loaded into the viewer.
18. Select the coding sequence starting at 68385.

![Question](images/question.png)  
How long is the contig? 

How long is the selected protein?

What does the protein code for?

There are lots of different visualisation options available within the contig viewer. Take some time now to investigate the various options, and play about with it by looking at a few different contigs and the anotations they contain.

### Requesting analysis of data

#### Note: This step will show you how to request analysis in the future. You don't need to make any changes or request anything today as data needs to be submitted to ENA before it can be analysed.

To analyse data in MGnify we first need consent to access your data in ENA. To allow this:

- Login to your webin account here https://www.ebi.ac.uk/ena/submit/webin/login

- Click 'Manage account'.

Scroll down to metagenomics consent. For any analysis requests in the future you will need to first agree to consent access if you are happy to do so.

- Navigate to the MGnify homepage and select Login. Login with your Webin credentials.

- Navigate back to the homepage.

- Click 'Submit and/or Request' and select 'Yes' to the data submission question.

When requesting analysis in the future: here you can specify the study accessions you wish to have analysed and the analyses type.












