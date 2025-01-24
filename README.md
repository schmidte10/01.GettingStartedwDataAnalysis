# 01.Getting Started with Data Analysis

Tips on how to set yourself up for easy data analysis

This repository is set up to help you design and manage your workflows and data files to ensure that your data analysis is easy to manage.

If you haven't already you should make sure that you have installed Git on your computer a set up project for your data analysis that is version controlled. I'm not going to go over how to install Git on your computer in this repository there are already several sources that do a good job of it. Keeping your data analysis on a GitHub repository will help ensure that your data is backed up, pubicly available (when you want it to be), and easy to access on additional computers.

**NOTE:** When setting up your project repository make sure to include a README file, as well as, a .gitignore file.

## .gitignore

The .gitignore should be used when you have files in your main directory that you do not want uploaded to GitHub. This could be because the data is restricted or sensitive and should not be placed on public repositories (althought note that on GitHub you can set your repository to be either *public* or *private*).

To make sure a certain file is not uploaded, you can enter the filetype into .gitignore. As an example you can see if this repository I have placed \_\*.txt\_ files within the .gitignore files, so that no txt files will be stored on the online repository.

**NOTE:** This step has to be done before any files are uploaded to the online repository. If you have already loaded \_\*.txt\_ files onto your repository and then enter the filetype into .gitignore it will not remove the already uploaded files.

## Directory

Within your project is is important to have a clean and managed directory. This means keeping files organised within folders.

One way to organise a directory is like this:

``` bash
-------------->01.GettingStartedwDataAnalysis 
               |
                ---->excel_files 
               |
                ---->import_files 
               |
                ---->data_analysis 
                     |
                      ---->01.DataMetric1 
                     |
                      ---->02.DataMetric2 
                     | 
                      ---->03.DataMetric3 
               | 
                ---->figures 
               |
                ---->tables 
               |
                ---->manuscripts 
```

This way it is easy for someone to navigate your repository in the future. I have included both **excel_files** as well as **import_files**. It is good practice when working with data to have a **Glossary** of terms in your excel files so that a reader unfamiliar with your data set knows what your columns and codes mean. However, because data that will actually be imported into R I save as text files.

## Glossasy

Excel files should always have a **glossary** sheet within the file to help future users understand your data and codes. Here is an example:

``` bash
EXP_FISH_ID         Combined FISH_ID with TEMPERATURE the fish was tested at 
FISH_ID            Unique alphamueric code provided to fish
POPULATION         Population/Reef the fish was collected from 
REGION             Region (i.e. core or leading) fish was collected from 
TEMPERATURE        Temperature fish was tested at 
MASS               Mass of the fish 
```

## Dataframes

Setting up dateframes properly will really help save you time during your data analysis. Below are a couple of tricks that will help you.

-   Don't have ***any*** space in your column names or data abbreviations if it can be avoided
-   Have your column labels either **ALL_CAPS** OR **all_lowercase**. If you have received your data from someone else this be corrected using the 'clean_names' function in the **janitor** package.\
-   Zero pad your values - this will make sure that your values can sorted easily
-   If you have codes for different data groups make sure they are all the same in length and order LOC001, LOC002......LOC100

# Workspace 

Make sure that your _save workspace to .RData on exit_ is set to **Never**. This 
will remove everything from your workspace Environment upon closing R. It will 
help make sure that your scripts are repeatable. 