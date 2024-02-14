---
layout: ../layouts/HelpLayout.astro
title: File List guide
---
## File List Guide
<style>
    figure {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        row-gap: 5px;
        border: 1px solid lightgray;
        border-radius: 5px;
        width: 400px;
    }

    figcaption {
        font-style: italic;
        padding: 0 1rem 0 1rem;
        text-align: center;
    }
</style>


### Summary

A File List is used to describe all the files that you wish to include in your submission, both image files and other supporting files e.g., analysis results. It contains file level metadata.

You must have one file list per [study component]({{ site.baseurl }}/rembi-help-examples/).

* File lists are tabular data, either in tsv or Excel (.xlsx) format. 
* The first column of the header has to contain the word "Files".
* It has to have one file per line.
* Do not leave blank lines.
* Filenames are case-sensitive.
* File path separator must be forward slash "/".

### Detailed Help

A File List is used to describe all the files that you wish to include in your submission, both image files and other supporting files e.g., analysis results. The file list also allows you to specify file level metadata, i.e. attributes associated with each file.

<figure class="float-right margin-left-large" >
<img src="/bioimage-archive/static/submit/filelist.png" alt="file list">
  <figcaption class="figure-caption">An example file list</figcaption>
</figure>

File lists are tabular data, and can be uploaded either in tsv or Excel (.xlsx) format. Unless it is generated programmatically, we recommend using a spreadsheet editing software to create the File List, exporting as tsv before submission.

The first line will be the File List's header. The first column of the header has to contain the word "Files". Values for other header columns are not predefined; we recommend using descriptive, self-explanatory names. Some examples of column names:

* For compound treatment experiments: Compound, Concentration, Time  ([Example File List](https://docs.google.com/spreadsheets/d/1Pj-JTXytPCw7p4-oBEg5MCdpbHZ6DbyVsHS6dx3zzcI/edit?usp=sharing){:target="_blank"})
* For genetic variation studies: Gene Identifier, Gene Symbol ([Example File List](https://docs.google.com/spreadsheets/d/1jMPOj9cZnU_0DUXwAU-wndcKOQxziqHD5WRdw3mVZCc/edit?usp=sharing){:target="_blank"})
* For antibody reagent studies: Antibody Name, Antibody ID, Target Protein Name, Target Protein ID ([Example File List](https://docs.google.com/spreadsheets/d/1wTQHCcXuzWZ_zk9E9dqEvLcveGelnMosUrHF38VXkVk/edit?usp=sharing){:target="_blank"})
* For other high content screening studies: Plate, Well, Field ([Example File List](https://docs.google.com/spreadsheets/d/1ID-3ZlWjgg7vfnU_UIC1wvwqRG1bF94VnOwbNmAkPz0/edit?usp=sharing){:target="_blank"})
* Other commonly used annotations: Channel, Description, QC info ([Example File List](https://docs.google.com/spreadsheets/d/1MzogH2NE9ODWyipx3u8h-KWe8zLieDdTSz259VOnWe4/edit?usp=sharing){:target="_blank"})

It is useful to include only attributes that have at least two distinct values for the set of image files you are describing in a particular file list; include values that are constant throughout the submission (e.g., "Organism" being "Homo Sapiens") in the annotation of the study entered via the web form.
You can use the [Ontology Lookup Service](https://www.ebi.ac.uk/ols/index){:target="_blank"} to search and access different biomedical ontologies.

Each submission file should be listed in the file list, one file per line. Use as many lines as there are files in your dataset, and enter the exact filenames in the first column. Please note that filenames are case-sensitive.

Fill in attribute values for each of the image files. Do not leave blank lines.

If you have organised files in your BioStudies home directory in a hierarchy, do not forget to reflect that in the file list. E.g., if you have in your home directory folders "Sample1" and "Sample2", refer to files inside those folders as "Sample1/imageFile1.tif" etc. Please note that the file path separator must be forward slash "/", anything else like "\\" or "\ \\" won't work.

<figure class="center margin-bottom-large margin-right-large" style="width: 600px">
  <img src="/bioimage-archive/static/submit/flat_and_hierarchical.png" alt="different file structures">
</figure>

You need to have at least one file list per submission. If you have different study components, like different experiments belonging to the same submission, you must have one file list per study component. In this case the file list of that study component would only list the names of files that belong to that study component. There are different ways to arrange your submission into study components if you wish to do so, e.g. by experiments in which you imaged different samples or used different imaging techniques, or by different screens in a high content screening study.

As an example, the file structure below contains both raw data as zarr images and analysis results as tsv files for two different experiments. The submission is divided into two study components: Experiment 1 and Experiment 2, each containing raw and analysis files belonging to that experiment. The submission has two file lists, one for each study component.

<figure class="center margin-bottom-large margin-right-large" style="width: 800px">
  <img src="/bioimage-archive/static/submit/two_experiment_filelist.png" alt="file lists per study component">
</figure>

<!-- The figures below show how that submission looks like on the BioImage Archive. Data files view can be expended (see figure below) and shows all the metadata included in the file lists.
 -->
Please [email us](mailto:bioimage-archive@ebi.ac.uk) if you have any further questions.

<!-- <figure class="center margin-bottom-large margin-right-large" style="width: 800px">
  <img src="/bioimage-archive/static/submit/BIA_submission_eg.png" alt="BIA submission example">
  <figcaption class="figure-caption">An example submission with two study components</figcaption>
</figure>

<figure class="center margin-bottom-large margin-right-large" style="width: 800px">
  <img src="/bioimage-archive/static/submit/BIA_filelist.png" alt="BIA submission data files">
    <figcaption class="figure-caption">Data files expended view of the submission with two study components</figcaption>
</figure> -->
