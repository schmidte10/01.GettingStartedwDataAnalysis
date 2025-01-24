# 01.Getting Started with Data Analysis
Tips on how to set yourself up for easy data analysis

This repository is set up to help you design and manage your workflows and 
data files to ensure that your data analysis is easy to manage. 

If you haven't already you should make sure that you have installed Git on your 
computer a set up project for your data analysis that is version controlled. 
I'm not going to go over how to install Git on your computer in this repository 
there are already several sources that do a good job of it. Keeping your data 
analysis on a GitHub repository will help ensure that your data is backed up, 
pubicly available (when you want it to be), and easy to access on additional 
computers. 

**NOTE:** When setting up your project repository make sure to include a README 
file, as well as, a .gitignore file. 

## .gitignore 

The .gitignore should be used when you have files in your main directory that 
you do not want uploaded to GitHub. This could be because the data is restricted 
or sensitive and should not be placed on public repositories (althought note 
that on GitHub you can set your repository to be either _public_ or _private_). 

To make sure a certain file is not uploaded, you can enter the filetype into 
.gitignore. As an example you can see if this repository I have placed _*.txt_ 
files within the .gitignore files, so that no txt files will be stored on the 
online repository. 

**NOTE:** This step has to be done before any files are uploaded to the online 
repository. If you have already loaded _*.txt_ files onto your repository and 
then enter the filetype into .gitignore it will not remove the already uploaded 
files. 

## Directory 

Within your project is is important to have a clean and managed directory. This 
means keeping files organised within folders. 

One way to organise a directory is like this: 

```bash
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

This way it is easy for someone to navigate your repository in the future. I 
have included both **excel_files** as well as **import_files**. It is good 
practice when working with data to have a **Glossary** of terms in your excel 
files so that a reader unfamiliar with your data set knows what your columns 
and codes mean. However, because data that will actually be imported into R I 
save as text files. 

## Glossasy 

Excel files should always have a **glossary** sheet within the file to help 
future users understand your data and codes. Here is an example: 


```basg
EXP_FISH_ID         Combined FISH_ID with TEMPERATURE the fish was tested at 
FISH_ID            Unique alphamueric code provided to fish
POPULATION         Population/Reef the fish was collected from 
REGION             Region (i.e. core or leading) fish was collected from 
TEMPERATURE        Temperature fish was tested at 
MASS               Mass of the fish 
RESTING_DATE       Date the resting metabolic rate was recorded for each fish     
RESTING_CHAMBER    Respirometry chamber the fish was tested in for RMR
RESTING_SYSTEM     Respirometry system (i.e. dell or asus) fish was tests with 
RESTING_SUMP       Respirometry sump (i.e., 1 or 2) fish was tested in
RESTING_AM_PM      Time of day (i.e. morning or afternoon) fish was tested 
RESTING_START_TIME Time that the fish was placed inside the repirometry chamber 
RESTING            Resting metabolic rate (RMR)  
RESTING_MgO2.hr    Resting metabolic rate divded mass 
MAX_DATE           Date that maximum metabolic rate was recored 
MAX_CHAMBER        Respirometry chamber the fish was tested in for MMR
MAX_SYSTEM         Respirometry system fish was test with for MMR 
MAX_SUMP           Respirometry sump (i.e., 1 or 2) fish was tested in for MMR 
MAX_AM_PM          Time of day (i.e. morning or afternoon) fish was tested for MMR 
MAX_START_TIME     Time that the fish was placed inside the chamber for MMR 
MAX                Maximum metabolic rate (MMR) 
MAX_MgO2.hr        Maximum metabolic rate divided by mass 
FAS                Factorial metabolic rate (MMR/RMR) 
NAS                Net metabolic rate (MMR - RMR) 
MgO2.hr_Net        Net metaboic rate divided by mass 
Swim.performance   Fish swim performance in swim tunnel (i.e., good, okay, poor) 
Notes              Additional experimental notes
MASS_CENTERED      Mass of fish (centered)
```
