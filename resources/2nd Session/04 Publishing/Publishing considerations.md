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

- examine the content of the accompanying files for publishing 
- define the publishing steps from the Skills4EOSC FAIR by design methodology
- use the FAIR signposting to include metadata in the resulting html pages


# Introduction

The Skills4EOSC FAIR-by-design Methodology defines a set of steps to make sure that the produced learning materials are published respecting the FAIR principles. To prepare for this, a set of files needs to be manually edited, making sure all the necessary information needed to accompany the materials is present. The methodology also uses the FAIR signposting, enabling metadata to be present in the resulting html files. 


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

Contributors.....


## FAIR Signposting 

[Signposting](http://signposting.org/), presents a lightweight, but powerful approach to increase the FAIRness of learning materials.   
Landing pages of learning materials support humans interaction with learning materials on the web, by providing descriptive metadata and links to content. Signposting helps machine agents by providing this information, and more, in a standards-based way. It contributes to FAIR's Findable, Accessible, and Reusable by uniformly conveying to machines what the persistent identifier of a scholarly object is, where its landing page is, where and what its content is, where metadata that describes it is, and what the persistent identifier of its author is. It conveys this by means of meaningful links that have web locations (HTTP URIs) as their target.

There are two levels of compliance to FAIR Signposting. Level 1 provide a minimal set of typed links with the landing page as the link origin. Level 2 elevates the compliance by providing a comprehensive set of typed links for landing pages, content, and metadata resources.

The publishing workflow of the Methodology described in the next chapter provides an easy way of implementing Signposting for the developed content.

As a result of running the Signposting workflow a `linkset.json` file is placed in the root of the repository.


## Automated publishing workflow


The [templates](https://github.com/FAIR-by-Design-Methodology/templates) repository of the FAIR-by-design Methodology includes a set of Git actions that implement the publishing workflow. The workflow is triggered with each new Github release. When triggered they automate the complete Zenodo publishing process. The steps performed by these actions include validation of the information provided in the accompanying files, implementation of the signposting, draft entry creation in Zenodo, updating the DOI in all files that reference it, including slides and syllabus, rebuilding and releasing a new version of the Git book. 

Important to note is that any other fields also present in the `CITATION.cff` file such as: `version`, `doi`, `date-released` **should not be manually edited**. They will be updated automatically when publishing the repository to Zenodo.



# Summary 



# Suggested Reading

- [Skills4EOSC FAIR-by-Design Methodology for Learning Materials Development](https://zenodo.org/records/8419242)
- [FAIR Signposting](https://signposting.org/FAIR/)



