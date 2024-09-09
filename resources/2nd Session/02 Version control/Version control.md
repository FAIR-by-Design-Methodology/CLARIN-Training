---
title: "Version control"
author: "Skills4EOSC"
tags: 
    - Version control
    - 
---

# Slides (new)

[Download the slides regarding the FAIR-by-Design Methodology here](https://github.com/FAIR-by-Design-Methodology/IDCC24workshop/raw/main/resources/02%20Skills4EOSC/Skills4EOSC-IDCCworkshop_FAIR-by-Design_Methodology.pptx){:download}


# Introduction

## Version Management

Git is the most popular version management system in use today. It is available for all popular platforms either as a first-party command line utility or through third-party graphical user interface (GUI) clients. Git uses the concept of repositories which can granularly manage the versions of all objects placed within it. File changes are **committed** to a repository and each commit is automatically associated a unique and random identifier. In addition to this identifier, each commit is also described by its author, commit title and commit description. A single Git repository can be used by multiple users, each contributing and committing their changes. To facilitate remote collaboration, a Git repository can be shared publicly or privately. Git hosting services, such as GitHub and GitLab offer this functionality today for free. While Git can also be used independently from such hosting services, either completely locally and offline or by devising a custom synchronization workflow with third parties, in reality this is rarely the case. 

Git repositories can also be **forked**, meaning that their current state is copied to a brand new repository, preserving all history. The user who has initiated the fork can then make any desired changes directly to their own fork of the repository. If desired, such changes can optionally be reconciled and added to the original repository from which the fork was created, provided that they are accepted by the original owner. This is possible due to the fact that the repositories will have a shared history at least up until the point when the fork was made. In case their files have diverged (e.g., both the original and forked repository contain changes to the same files), and if these changes are conflicting (e.g., changes to the same part of a given document), Git will mark these changes and leave it up to the owner of the repository to decide how to proceed, and what version to accept. 

Below is a list of common Git related terminology which will be useful for the remaining of the training:

 - **Git repository** – a collaborative space where files can be versioned
 - **Git commit** – a granular change of a single or multiple files in the repository, identified by a random unique identifier, the committer's name, email address, short commit title and an optional longer commit description. A commit can contain file additions, modifications, removal, or relocation to a different directory.
 - **Git clone** – an action to download locally an existing Git repository. A repository hosted on a public Git hosting service such as GitHub can be cloned by anyone (assuming it is public) on their local machines. Once downloaded, users can explore the repository and optionally send their contributed changes upstream, if they have been assigned the necessary permissions.
 - **Git fork** – a 1:1 copy of an existing Git repository. A fork of an existing repository results with the creation of a brand new repository which will have a shared history with the original one up until the fork was made. The owner of the forked repository will be the user who initiated the fork. The original owner of the repository does not have any right in the forked repository by default. 
- **Pull request/Merge request** – when changes are made to a forked repository, they can be contributed back to the original repository by creating a merge request or a pull request (the terms are synonyms, depending on the platform either one can be used). With this approach a privileged user from the original repository from which the fork was initiated can review the changes and decide whether to accept them, modify them, or outright reject them. Forks can exist independently of the original repository forever.




### Filling out RELEASE_NOTES.md

1. Open the RELEASE_NOTES.md` file by clicking on its name from the left-hand directory tree.
2. The file uses a special Markdown syntax which allows its contents to be shown as collapsed on the syllabus home page, thus preserving space. 
3. For the initial release, alter the text below the `1.0.0` heading and make sure to also update the date of the release in the heading itself.
4. For all subsequent releases, add a new level two heading using two hash symbols on a new line, (`##`) just below `<summary>Release Notes <summary>`. Ideally, the RELEASE_NOTES.md file should list the various versions in a descending order, sorted by the release date.


### New iteration

The work on a new iteration starts once the list of identified improvements that will be incorporated into the new version is finalised.

The next step is to organise the work regarding the required changes to the learning materials. Depending on the identified improvements, the changes may bring you back to the Produce stage implementing changes in learning units, or even to Design if restructuring of the learning material is needed.

---
When all planned changes are implemented following the requirements and recommendations of the ([Design](../../Stage%203%20–%20Design/04-Conceptualisation/04-Conceptualisation.md) and) [Produce](../../Stage%204%20–%20Produce/08-Development%20Tools/08-Introduction%20to%20Markdown%20and%20Git.md) stage(s), you can then move again through the [Publish](../../Stage%205%20–%20Publish/16-Publishing%20Preparations/16-Publishing%20Preparations.md) stage and create a new release with a new version number that will then be added as a new version on Zenodo. 

Note that the provided automated workflow will not create a new independent record on Zenodo, but will **add a new version to the already existing Zenodo record**. For the specific steps of the publication process please refer back to the [respective lesson unit](../../Stage%205%20–%20Publish/17-Zenodo%20Publishing/17-Zenodo%20Publishing.md) in the Publish stage. 

--- 

The **version number** is one of the things that you will need to provide when activating a new release. The recommendation based on best practices is to keep the versioning in the Major.Minor.Patch version number sequence.

- You will **increment the minor number** if the incremental improvement does not change the overall structure of the learning materials.
- You will **increment the major number** if the changes include change in the overall structure of the learning materials.
- **Increment the Patch number** in case of only technical fixes. 

The image below depicts the best practices of semantic versioning.

![A simple diagram of Semantic Versioning](./attachments/Semantic-versioning.png){: style="height:250px;"}

[Semantic Versioning](https://commons.wikimedia.org/wiki/File:Semantic-versioning.svg) by [Surjit Bains](https://commons.wikimedia.org/w/index.php?title=User:SurjBains&action=edit&redlink=1) on [Wikimedia Commons](https://commons.wikimedia.org/) licensed under the [Creative Commons Attribution-Share Alike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/deed.en) license.

Don't forget to update the resource on the Learning Platform. This is a requirement if the learning material is provided as a self-paced course for an example, but might not be needed if it was a one-time training workshop event after which it is not expected that the learners will keep coming back to the learning content.

Note that if you are using the `/latest` links when adding the resources to the learning platform, you don't need to update any of the external links on the learning platform. However, be careful if the new iteration changes involved changes in the assessment or slide decks. 


# Summary 



# Suggested Reading

- [Skills4EOSC FAIR-by-Design Methodology for Learning Materials Development](https://zenodo.org/records/8419242)



