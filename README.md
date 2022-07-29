# The Single Cell Toolkit (singleCellTK or SCTK)

<!--
[![Travis build status](https://travis-ci.org/compbiomed/singleCellTK.svg?branch=master)](https://travis-ci.org/compbiomed/singleCellTK)
[![codecov](https://codecov.io/gh/compbiomed/singleCellTK/branch/master/graph/badge.svg)](https://codecov.io/gh/compbiomed/singleCellTK)
[![BioC status](https://www.bioconductor.org/shields/build/release/bioc/singleCellTK.svg)](https://bioconductor.org/checkResults/release/bioc-LATEST/singleCellTK) 
[![lifecycle](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://www.tidyverse.org/lifecycle/#stable)
-->

## Installation

### Current Release Version

You can download the release version of the Single Cell Toolkit from this repository:

```r
# install.packages("devtools")
devtools::install_github("wevanjohnson/singleCellTK")
```

### Troubleshooting Installation

For the majority of users, the commands above will install the latest version
of the singleCellTK without any errors. Occasionally, you may get an error indicating
a missing package, e.g., "there is no package called ‘GSVAdata’", when you launch the App. In this case just install the 
missing packages using CRAN or Bioconductor. In addition, rarely you may encounter an error due
to previously installed versions of some packages or missing packages that are 
required for the singleCellTK. If you encounter an error during installation, 
use the commands below to check the version of Bioconductor that is installed:

```r
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::version()
```

If the version number is not 3.14 or higher, you must upgrade Bioconductor to
install the toolkit:

```r
BiocManager::install()
```

After you install Bioconductor 3.14 or higher, you should be able to install the
toolkit using `devtools::install_github("wevanjohnson/singleCellTK")`. If you
still encounter an error, ensure your Bioconductor packages are up to date by
running the following command.

```r
BiocManager::valid()
```

If the command above does not return `TRUE`, run the following command to
update your R packages:

```r
BiocManager::install()
```

Then, try to install the toolkit again:

```r
devtools::install_github("wevanjohnson/singleCellTK")
```

If you still encounter an error, please [contact us](mailto:dfj@bu.edu) and
we'd be happy to help.

## Quick start

You can use the example data aleady available within the app, or you can upload
your own data. To get started, simply run the singleCellTK function:

```r
library(singleCellTK)
singleCellTK()
```
And then follow the point and click interface or directions to navigate the app. 
For more detailed instructions, click on the tabs at the top or links below for 
more help.

### Interactive Analysis

* [Upload Tab](https://compbiomed.github.io/sctk_docs/articles/v03-tab01_Upload.html)
* [Data Summary and Filtering Tab](https://compbiomed.github.io/sctk_docs/articles/v04-tab02_Data-Summary-and-Filtering.html)
* [Visualization and Clustering Tab](https://compbiomed.github.io/sctk_docs/articles/v05-tab03_Visualization-and-Clustering.html)
* [Batch Correction Tab](https://compbiomed.github.io/sctk_docs/articles/v06-tab04_Batch-Correction.html)
* [Differential Expression Tab](https://compbiomed.github.io/sctk_docs/articles/v07-tab05_Differential-Expression.html)
* [Pathway Activity Analysis Tab](https://compbiomed.github.io/sctk_docs/articles/v08-tab06_Pathway-Activity-Analysis.html)
* [Sample Size Tab](https://compbiomed.github.io/sctk_docs/articles/v09-tab07_Sample-Size.html)

### R Console Analysis

* [Processing and Visualizing Data in the Single Cell Toolkit](v02-Processing_and_Visualizing_Data_in_the_SingleCellTK.html)
* [Aligning and Quantifying scRNA-Seq Data](https://compbiomed.github.io/sctk_docs/articles/v10-Aligning_and_Quantifying_scRNA-Seq_Data.html)


## Develop singleCellTK

To contribute to singleCellTK, follow these steps:

__Note__: Development of the singleCellTK is done using the latest version of R.

1. Fork the repo using the "Fork" button above.
2. Download a local copy of your forked repository "```git clone https://github.com/{username}/singleCellTK.git```"
3. Open Rstudio
4. Go to "File" -> "New Project" -> "Existing Directory" and select your git repository directory

You can then make your changes and test your code using the Rstudio build tools.
There is a lot of information about building packages available here: http://r-pkgs.had.co.nz/.

Information about building shiny packages is available here: http://shiny.rstudio.com/tutorial/.

When you are ready to upload your changes, commit them locally, push them to your
forked repo, and make a pull request to the compbiomed repository.

Report bugs and request features on our [GitHub issue tracker](https://github.com/wevanjohnson/singleCellTK/issues).

Join us on [slack](https://compbiomed.slack.com/)!
