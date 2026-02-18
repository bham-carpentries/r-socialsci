---
title: Setup
---

## Setup instructions

**R** and **RStudio** are separate downloads and installations. R is the
underlying statistical computing environment, but using R alone is no
fun. RStudio is a graphical integrated development environment (IDE) that makes
using R much easier and more interactive. You need to install R before you
install RStudio. Once installed, because RStudio is an IDE, RStudio will run R in
the background.  You do not need to run it separately.

After installing both programs,
you will need to install the **`tidyverse`** package from within RStudio. The
**`tidyverse`** package is a powerful collection of data science tools within **R**
see the [**`tidyverse`** website](https://tidyverse.tidyverse.org) for more details.
Follow the instructions below for your operating system, and then follow the
instructions to install **`tidyverse`**.

:::::::::::::::: spoiler

### Personal Laptop

#### Windows

- Download R from
  the [CRAN website](http://cran.r-project.org/bin/windows/base/release.htm).
- Run the `.exe` file that was just downloaded.
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select **RStudio x.yy.zzz - Windows.
  Vista/7/8/10** (where x, y, and z represent version numbers).
- Double click the file to install it.
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

#### macOS

- Download R from
  the [CRAN website](http://cran.r-project.org/bin/macosx/).
- Select the `.pkg` file for the latest R version.
- Double click on the downloaded file to install R.
- It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
  by some packages).
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)**
  (where x, y, and z represent version numbers).
- Double click the file to install RStudio.
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

### Linux

- Follow the instructions for your distribution
  from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
  to get the most recent version of R for common distributions. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this approach are
  usually out of date. In any case, make sure you have at least R 3.2.
- Go to the
  [RStudio download page](https://posit.co/download/rstudio-desktop/).
- Under *Installers* select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-x.yy.zzz-amd64.deb` at the terminal).
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.
- Before installing the `tidyverse` package, **Ubuntu** (and related) users may
  need to install the following dependencies: `libcurl4-openssl-dev libssl-dev libxml2-dev`
  (e.g. `sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev`).

::::::::::::::::::::::::

:::::::::::::::: spoiler

### University of Birmingham Managed Laptop

#### Windows
To install R and RStudio on a University managed Windows machine:

- Connect your computer to the university network and open the Software Centre from the Start Menu

- Search for and install "RStudio". 

- This will also automatically install R for Windows 4.5.1 and Rtools.

#### Mac

To install R and RStudio on a University managed Mac machine:

- Connect your computer to the university network and open the Software Centre from the Start Menu

- Search for and install "R Language". 

- Search for and install "RStudio with R". 

- This will also automatically install R for Mac 4.5.1 and Rstudio.

::::::::::::::::::::::::


### For everyone

**After installing R and RStudio, you need to install the `tidyverse` and `here` packages.**

- After starting RStudio, at the console type:

```r
install.packages("tidyverse")
```
followed by the enter key. Once this has installed, type

```r
install.packages("here")
```
followed by the enter key. There will be a number of messages displayed during installation. After the installation has completed you should see a message containing:

```output
** testing if installed package can be loaded
* DONE (tidyverse)
```

Or:

```output
package ‘tidyverse’ successfully unpacked and MD5 sums checked
```

Both packages should now be installed.

- For reference, the lesson uses `SAFI_clean.csv`. The direct download link for
  this file is: [https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv](https://github.com/datacarpentry/r-socialsci/blob/main/episodes/data/SAFI_clean.csv).
  This data is a slightly cleaned up version of the SAFI Survey Results available on
  [figshare](https://figshare.com/articles/dataset/SAFI_Survey_Results/6262019).
  Instructions for downloading the data with R are provided in the
  [Before we start episode](https://datacarpentry.org/r-socialsci/00-intro.html).

## Check Your Installation

Type the following commands at the > prompt:
```r
library(tidyverse)
ggplot(cars, aes(x=speed, y=dist)) + geom_point()
```

(any message about conflicts can be safely ignored)
This should produce a plot in the lower right hand window of RStudio.