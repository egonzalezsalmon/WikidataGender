# WikidataGender
Gender assignment algorithm based on Wikidata + Second WGND Dictionary

Here we will explain how to use the list of Wikidata names + [World Gender Name Dictionary](https://github.com/IES-platform/r4r_gender/blob/main/wgnd/README.md) (WGND) second dictionary to assign gender to names.
Note that we only look at the probability that a certain name is assigned to a certain gender in a specific
country. That is, we are not identifying the gender of names but looking at the probability of a gender-name
combination.

It is also important to take into account the binary view of gender and names that this gender assignation
approach has, since only Men/Women/Unknonwn options are possible. So far, algorithms have not been
able to solve this issue, that hinders and hides non-binary realities.

Given that, we have divided the procedure in six different steps (with a seven and eight optional step): 
1. Load packages, clean your data
2. Assign gender to Slavic names* using Wikidata names (WDNAMESslav)
3. Assign gender to non-Slavic names* using Wikidata names (WDNAMESrest)
4. Join Slavic and non-Slavic names, clean data
5. With those names that remained unknown, use a second list of Wikidata names (WDNAMES2)**
6. With those names that remain unknown, use the WGND second dictionary based on language-gender-name information.
7. Create graph to show results (Optional)
8. Create world map to show global distribution of results (Optional)
   
*The reason for this division lays in the fact that Slavic names may contain gender information on last
names, whereas non-Slavic names do not.

**Files needed for this step, [wgnd_2_0_code_langcode](https://dataverse.harvard.edu/file.xhtml?fileId=4750349&datasetVersionId=268165) and [wgnd_2_0_name_gender_langcode](https://dataverse.harvard.edu/file.xhtml?fileId=4750353&datasetVersionId=268165) can be found in the original World Gender Name Dictionary repository. 


Warning: Depending on your data (given the number of columns, etc.), you may need to do small modifications to the code. Some notions of the workings of R are recommended. 
