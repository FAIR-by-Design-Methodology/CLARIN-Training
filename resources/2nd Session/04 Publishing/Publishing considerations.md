---
title: "Publishing consideration"
author: "Skills4EOSC"
tags: 
    - Publishing
---

# Slides (new)

[Download the slides regarding the FAIR-by-Design Methodology here](https://github.com/FAIR-by-Design-Methodology/IDCC24workshop/raw/main/resources/02%20Skills4EOSC/Skills4EOSC-IDCCworkshop_FAIR-by-Design_Methodology.pptx){:download}



## Learning objectives

Upon completing this module the learner should be able to:

- define the publishing steps 
- use the proper versioning for the learning material the instructors kit


# Introduction


## Files Description

The [FAIR-by-Design templates repository](https://github.com/FAIR-by-Design-Methodology/templates) contains the accompanying files which we will need to alter:

- CITATION.cff
- README.md
- CODE_OF_CONDUCT.md
- RELEASE_NOTES.md

These files can be altered in any order desired, as long as making sure that they have all been covered. 

Starting from `CITATION.cff`, the purpose of this file is to provide information on how the Git repository can be cited. Its content, among other things, also controls the text shown when the `Cite this repository` button is clicked on the right hand side of a GitHub repository's homepage. It is written in a YAML format and has controlled vocabularies for most of the supported fields. Luckily, validators are also widely available, and we will discuss some options in this space in the Activity, below.

`README.md` is a Markdown file which should briefly describe the repository, so that first time visitors can get an initial idea what it is about. The README.md file's content is shown immediately below the directory browser on the repository's homepage.

The `CODE_OF_CONDUCT.md`, as its name suggests, describes the contributors' code of conduct which needs to be adhered to. It defines standards for how to engage in a community. It can also contain steps for resoling issues between members of the community. GitHub also shows a direct link to a repository's code of conduct (if available) above the citation information.

`RELEASE_NOTES.md` is a special Markdown file that keeps provides description of all the changes made to the material since its first release. The content of this file is embedded as is on the Git book homepage (the syllabus) in a collapsible block.

In the activity that follows we will go over all of the required changes that need to be made to these files, along with tips, and any potential pit-falls when it comes to controlled vocabulary fields.

## Activity: Publishing Preparation in Practice - Customizing Accompanying Files

### Setting up the Environment

1. Make sure that the latest changes have been pulled from the remote using the GitHub Desktop application
2. Open the Obsidian workspace
3. Ensure that all three files are already available (as a result of forking the templates repository previously) in the root of the repository: `CITATION.cff`, `README.md`, `CODE_OF_CONDUCT.md`.

### Filling out CITATION.cff

1. Click on `CITATION.cff` in Obsidian's file tree pane. In some environments Obsidian might not be able to automatically open the file since it has an unsupported extension - `.cff`. If so, select a preferred text editor which is already installed on your system (e.g., Notepad on Microsoft Windows).
2. Fill out the appropriate information in the following fields:
    - `authors` - a list of authors who participated in the creation of the learning materials
    - `title` - title of the training
    - `abstract` - a short abstract describing the learning materials
    - `license` (if a license other than the default CC-BY should be used)
    - `license-url` (if a license other than the default CC-BY should be used)
    - `keywords` - list of keywords which describe the learning materials
    - `repository` - the URL to the GitHub repository where the materials are hosted

    While filling out the file and adding new lines, make sure that they match the indentation of the examples. The picture below provides a visual example of how to correctly add a new author.

    ![CITATION.cff file example](./attachments/01-citation-cff.png)

    The newly added author (an imaginary John Doe) should have the same indentation (number of spaces at the beginning of the line) as the first author which is given as an example in the template. Inconsistent number of spaces will make the CITATION.cff file invalid. Additionally, we denote that we are adding information about a new author by prefixing the first property (in this case `family-names`) with a `-` character.

- Note that any other fields also present in the `CITATION.cff` file such as: `version`, `doi`, `date-released` **should not be manually edited**. They will be updated automatically when publishing the repository to Zenodo.

3. After having done the necessary updates to the fields, you can validate the structure of the `CITATION.cff` file using the free online utility which is available on [citation-file-format.github.io](https://citation-file-format.github.io/cff-initializer-javascript/#/update).
    - Paste the content into the text field
    - Press the `PARSE` button
    - Ignore any warnings about "extra" fields. It is important that a message stating `Parsed CFF successfully` appears.

        ![Validating the edits made to CITATION.cff](./attachments/02-citation-cff-validation.png)

        In case there is a validation error, a descriptive error message will be shown, pointing to the line that is incorrectly formatted. Assuming that the correct indentation policy is not followed when specifying the first name of an author, the error message will be:

        ![Example Validation Error](./attachments/03-validation-error.png)        

4. Save the changes made to the `CITATION.cff` file and close the text editor.

### Filling out README.md

1. Go back to Obsidian and open the `README.md` file by clicking on its name from the left-hand directory tree.
2. The content of the README.md file is free text, so you are welcome to provide any introduction that you would like. Just make sure to keep the official Skills4EOSC header image, and a reference to the templates repository.

### Filling out CODE_OF_CONDUCT.md

1. The `CODE_OF_CONDUCT.md` file, as present in the templates repository is a generic text that can be applied to any future trainings. 
2. Go over the text and make any desired changes.
3. Make sure to alter the contact information for the person responsible for the enforcement of the code of conduct rules, specified in the `Enforcement` section.


### Customizing the Signposting Information

The [automated workflows](../17-Zenodo%20Publishing/17-Zenodo%20Publishing.md#description-of-the-automated-publishing-workflow) provide an easy way of implementing [Signposting](https://signposting.org/FAIR/) for the developed content.

Minimal changes are needed to the `mkdocs.yml` to configure the automated workflow for Signposting. The `mkdocs.yml` file acquired from the `templates` repository has 3 dedicated parameters related to the implementation of Signposting:

- `signposting_linkset` - should never be changed manually; its content is handled by the workflow itself.
- `signposting_default_profile` - in case the source markdown files for the learning content follow a standardized and registered format, they can be further described by providing a link to the upstream profile. This is an optional field that can be left blank, in which case no profile information will be provided. More information is available on the [Signposting docs page](https://signposting.org/FAIR/#examples2:~:text=Level%201.-,item,-1%20or%20more).
- `signposting_gitbook_url` - an optional parameter that is commented by default. It should be uncommented only in cases when a custom domain is configured for hosting the Git book, instead of the default provided by GitHub. Uncommenting can be performed by removing the leading `#` character.
- `signposting_exclusions` - a list of file names that should **not** be referenced in the generated Signposting linkset description. Accompanying material such as activities, lesson plans, and feedback templates are already excluded by default. Pattern matching is supported. A single `*` matches any character in files at the current folder level, while `**` applies to all subfolders as well, irrespective of their position in the directory hierarchy.

In most cases, such as when [Signposting Level 1](https://signposting.org/FAIR/#level1) is sufficient, no manual changes need to be performed. If the content follows a well-defined template, then `signposting_default_profile` needs to be updated so that it points to the URL containing the template's description.

As a result of running the Signposting workflow a `linkset.json` file is placed in the root of the repository.

### Committing Changes

Once the three files have been updated, commit the changes and push them to GitHub using the GitHub Desktop application. Upon every change of the `CITATION.cff` file an automated action is executed which verifies its contents. In case of a validation error, you will receive an email message similar to the one shown below.

![CITATION.cff workflow error](./attachments/04-workflow-error.png)

The recommended action in such cases is to simply retry the validation of the `CITATION.cff` file manually using the [citation-file-format.github.io](https://citation-file-format.github.io/cff-initializer-javascript/#/update) tool. Make sure to address any errors, committing and pushing the results to GitHub once completed.




# Summary 



# Suggested Reading

- [Skills4EOSC FAIR-by-Design Methodology for Learning Materials Development](https://zenodo.org/records/8419242)



