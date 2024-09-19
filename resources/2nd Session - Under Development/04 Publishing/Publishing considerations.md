---
title: "Publishing consideration"
author: "Skills4EOSC"
tags: 
    - Publishing
    - Machine readable metadata
    - FAIR Signposting
---

# Publishing considerations

## Slides

[Download the slides here TBD]https://github.com/FAIR-by-Design-Methodology/CLARIN-Training/raw/main/resources/2nd%20Session/03%20Recognition/recognition_OB_EDC.pptx){:download}


## Learning objectives

Upon completing this module the learner should be able to:

- examine the content of the accompanying files for publishing 
- define the publishing steps from the Skills4EOSC FAIR by Design Methodology
- use the FAIR signposting to include machine readable metadata in the resulting html pages


## Introduction

The Skills4EOSC FAIR-by-design Methodology defines a set of steps to make sure that the produced learning materials are published respecting the FAIR principles. To prepare for this, a set of files needs to be manually edited, making sure all the necessary information needed to accompany the materials is present. The methodology also uses the FAIR signposting, enabling metadata to be present in the resulting html files. 

!!!tip "Repository choice"
	The FAIR-by-Design Methodology opted for using Zenodo as a open access repository, but other communities and users can use different repositories, suitable for their purpose. 

## Files Description

The [FAIR-by-Design templates repository](https://github.com/FAIR-by-Design-Methodology/templates) contains the accompanying files which we will need to alter:


- README.md
- CODE_OF_CONDUCT.md
- Licence.txt
- Contributors

These files can be altered in any order desired, as long as making sure that they have all been covered. 

`README.md` is a Markdown file which should briefly describe the repository, so that first time visitors can get an initial idea what it is about. The README.md file's content is shown immediately below the directory browser on the repository's homepage.

The `CODE_OF_CONDUCT.md`, as its name suggests, describes the contributors' code of conduct which needs to be adhered to. It defines standards for how to engage in a community. It can also contain steps for resoling issues between members of the community. GitHub also shows a direct link to a repository's code of conduct (if available) above the citation information.

The `Licence.txt` file contains the description of the license under which the training material is released. If you have been creating your own repo from scratch or cloned the templates repo, most probably the current license you have in your repo at the moment is CC0. If you have decided that you will use another license (compatible with the reused material, derived using the adapter's license rules, etc.) then you need to replace the LICENSE file in your repository with the correct one. The contente of the license file can be downloaded from the [Plaintext versions of Creative Commons 4.0 licenses](https://creativecommons.org/2014/01/07/plaintext-versions-of-creative-commons-4-0-licenses/)

The FAIR-by-Design Methodology does not use any separate files and roles for the contributors, other than the ones in the RDA Metadata. However, even thou there is not a standardised taxonomy for the contributors and roles, [Contributor Role Taxonomy (CRediT)](https://credit.niso.org) can be helpful. The [All Contributors specification](https://allcontributors.org/docs/en/specification) defines that Open source projects should include the following mandatory items to support the All Contributors specification:

1. A "Contributors" section in a prominent site of the project repository documentation that includes a list of all project contributors
    - The goal should be to use the most prominent site of the project documentation when feasible. In many cases, this is the project README file
    - Consider [using a CONTRIBUTORS file](https://allcontributors.org/docs/en/bot/configuration#moving-the-all-contributors-table-into-a-different-file) in the top level of the repository when the number of project contributors exceeds a level at which it is unfeasible to use the README file to acknowledge contributions. In this case, a prominent link to the CONTRIBUTORS file should be included on the README page under the "Contributors" heading
2. The listings should be formatted as a table with the following information about the project contributors:
    - Name
    - URL link to a site where more information can be learned about the contributor. This URL may be determined by the contributor at the project's discretion.
    - An indication of the Contribution Category in text or icon image format using the defined Contribution Categories and/or Contribution Categories emoji images (see below).
    - A link to the Contribution Category in text or emoji format using the defined Contribution Categories and/or [Contribution Categories emoji](https://allcontributors.org/docs/en/emoji-key).
        - The list of contributors can be spread across multiple lines (each technically being its table) as needed.
        - The order of contributors is immaterial to the spec. Order them how you wish.


!!!tip "Contributors example"
	Example use of contributors and their roles can be seen in the [Galaxy Project Training Network - GTN](https://training.galaxyproject.org/training-material/topics/contributing/tutorials/create-new-tutorial-content/tutorial.html#listing-contributors). 


## FAIR Signposting 

[Signposting](http://signposting.org/), presents a lightweight, but powerful approach to increase the FAIRness of learning materials.   
Landing pages of learning materials support humans interaction with learning materials on the web, by providing descriptive metadata and links to content. Signposting helps machine agents by providing this information, and more, in a standards-based way. It contributes to FAIR's Findable, Accessible, and Reusable by uniformly conveying to machines what the persistent identifier of a scholarly object is, where its landing page is, where and what its content is, where metadata that describes it is, and what the persistent identifier of its author is. It conveys this by means of meaningful links that have web locations (HTTP URIs) as their target.

There are two levels of compliance to FAIR Signposting:

- Level 1 provide a minimal set of typed links with the landing page as the link origin. 
- Level 2 elevates the compliance by providing a comprehensive set of typed links for landing pages, content, and metadata resources.

!!!note "FAIR Signposting implementation"
	The publishing workflow of the Methodology described below provides an easy way of implementing Signposting for the developed content. Note that the signposting is not mandatory part of the Methodology, but a very useful addition to it. 

!!!info "FAIR Signposting output"
	As a result of running the Signposting workflow a `linkset.json` file is placed in the root of the repository. This file is accessible to crawlers as it is embedded in the meta information in the head of the landing HTML page.


## Automated publishing workflow


The [templates](https://github.com/FAIR-by-Design-Methodology/templates) repository of the FAIR-by-design Methodology includes a set of Git actions that implement the publishing workflow. The workflow is triggered with each new Github release. When triggered they automate the complete Zenodo publishing process. 

The steps performed by these actions include:

- validation of the information provided in the accompanying files, 
- implementation of the signposting, 
- draft entry creation in Zenodo, 
- updating the DOI in all files that reference it, including slides and syllabus, 
- rebuilding and 
- releasing a new version of the Git book. 


!!!note "Manual editing"
	In the accompanying files, some of the fields should be edited manually, while others are automatically updated by the publishing workflow and should not be manually changed. Examples of such field are `version`, `doi`, `date-released` from the `CITATION.cff`.


As as result of the successful completion of this workflow the following actions will be performed:

- new or updated entry in the Zenodo repository
- updated citation in the Gitpages
- updated `citation.cff` file
- updated FAIR signposting metadata
- updated citation in the PowerPoint slides (if used)

## Summary 

FAIR-by-Design Methodology pays special attention to the publishing of the learning materials, making sure that they conform to the FAIR principles. Several accompanying files are needed to ensure that the required elements are present. Using the Signposting technique, the published html version of the training materials are made understandable not only to humans, but also to the machines - crawlers that process web learning resources. The methodology provides a specific workflow that enables each new release to be clearly visible and added to the Zenodo repository as a new version of the learning materials.  

## Suggested Reading

- [Skills4EOSC FAIR-by-Design Methodology for Learning Materials Development](https://zenodo.org/records/8419242)
- [FAIR Signposting](https://signposting.org/FAIR/)
- [Skills4EOSC FAIR-by-Design Methodology Publishing Preparations](https://fair-by-design-methodology.github.io/FAIR-by-Design_ToT/latest/Stage%205%20–%20Publish/16-Publishing%20Preparations/16-Publishing%20Preparations/)
- [Skills4EOSC FAIR-by-Design Methodology Zenodo Publishing](https://fair-by-design-methodology.github.io/FAIR-by-Design_ToT/latest/Stage%205%20–%20Publish/17-Zenodo%20Publishing/17-Zenodo%20Publishing/)



