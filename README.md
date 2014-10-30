# Bioinformatics Testing Consortium: Codebase Peer-review to improve robustness of bioinformatic pipelines

## The Problem
Over the last decade, biology has become one of the most data-rich sciences: Next-generation sequencing has been democratized as a result of exponentially decreasing sequencing costs; rapid improvements to mass-spectrometry throughput allow for unprecedented analysis of proteomes and metaproteomes across all domains of life. To deal with this data, a concomitant rapid expansion of the tools required for computational analysis of this data has also arisen. Such tools are typically written by individuals or small teams and are then propagated to the rest of the bioinformatics community through publications as open-source programs. 

The great strength of this model is that rapid sharing of tools prevents individual groups from re-inventing the same tool to solve a similar problem and rapid adoption of tools as the ?industry-standard? way of analyzing a particular dataset is common. However, the current review process for the publication describing a tool seldom involves a quality check of the tool itself, particularly if the tool is published as part of a broader biological study describing the results generated by the tool. Documentation is often sparse and code is often only tested on a single runtime environment prior to publication. As a result, initial use of a new bioinformatics tool is often preceded by a period of troubleshooting; email conversations with the author and/or internet forums etc. In the worst case, this increase in activation energy can deter use and prevent broader adoption.


## Parallels to the IT industry
In the early 1990s the use of open source software libraries in the IT industry typically suffered from the issues seen in today?s bioinformatics pipelines. However, a paradigm shift in the late 90s/early 2000s recognized the critical weakness of allowing software testing to be performed by the software developers themselves. The intimate knowledge software developers have with their own code leads to several problems:

1. Unconsciously avoiding pitfalls and during their own unit testing (?walking the known path?);
2. Assuming user interaction patterns (The ?why would anyone do that?? problem); 
3. Severe lack of documentation (The ?its obvious how it works? problem).

When the industry started hiring professional testers, whose role consisted entirely of systematically running software as a na�ve user down each possible path, these problems soon came to light and were quickly corrected. It is now commonplace for developers to release their code to testers, who then raise bugs in function and documentation for the developers to fix prior to general release.

## The Aims of the Bioinformatics Testing Consortium
While the use of professional testing in bioinformatics is undoubtedly out of the budgetary constraints of most projects, there are significant parallels to be drawn with the review process of manuscripts. The Bioinformatics Testing Consortium aims to promote and facilitate peer-testing of bioinformatics software prior to publication. A suggested project lifecycle would be as follows:

1. Dr Doe finishes his novel bioinformatics pipeline and submits it to [GitHub](http://www.github.com) for peer-review
2. The project is registered with a Continuous Integration service such as [Travis](https://travis-ci.org/) for automation of building and running of unit tests.
3. The project is registered with the BTC, where administrators assign available testers to perform a code review and verify the code using supplied test-data sets, with issues raised on GitHub.
4. Once issues have been resolved or appropriately closed, the repository is branched and tagged and a DOI is generated for use in publications.
5. The BTC website retains a database of BTC-approved software versions and DOIs.

Post-Continuous Integration testing will follow a model similar to the reviewing consortium for the journal [Standards in Genomic Sciences (SIGS)](http://www.standardsingenomics.org/index.php/sigen) and consist of a core set of volunteer reviewers from a wide range of disciplines and computational experience. As public GitHub repositories, projects would also be open to public testing, which would be promoted via the BTC twitter feed at the request of the scientist. 

## The Benefits
The benefits to the developer of such as system would include fewer setup query emails; improved confidence in deployment; suggestions on how to improve the efficiency of algorithms used and exposure of the software to a broader range of data, improving applicability and ultimately, a stamp of approval that their codebase has been rigorously tested. End-users would ultimately benefit from better quality software with lower activation energy, broadening bioinformatics accessibility to those who are confounded at the first compilation error. Journals would benefit as the codebase presented in the manuscript would be more stable and thus less subject to changes from the reported methods.

