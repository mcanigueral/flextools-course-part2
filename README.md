
# Introduction

This RMarkdown document aims to be a tutorial to use the `flextools` package. First, install the latest development version of `evsim`, `flextools` and  `dutils`:

```
# install.packages("remotes")
remotes::install_github("mcanigueral/flextools")
remotes::install_github("mcanigueral/evsim")
remotes::install_github("mcanigueral/dutils")
```

And import them:

```
library(flextools)
library(evsim)
library(dutils)
```

The `flextools` packages provides the framework to simulate smart charging of a charging sessions data set, through `smart_charging()` function. The smart charging concept is widely used in different fields and applications. In `flextools` package, we define *smart charging* as a tool to coordinate individual EV charging sessions in order to obtain the optimal aggregated demand profile according to a certain objective. 

There are different practical **methods** to coordinate each session, such as:

* **Postpone**: shifting charging start time over time
* **Interrupt**: stop charging during certain time
* **Curtail**: limiting charging power during certain time
* **Vehicle-to-grid (V2G)**: combine charge and discharge during connection time. Not available in flextools yet.

At the same time, the charging sessions can be coordinated with different objectives or goals, such as minimizing the interaction with the power grid, minimizing the energy cost, participating in flexibility or imbalance markets, not surpassing grid constraints or capacity limits, accomplishing with demand-response programs, etc. 

Through this project you will have to complete some exercises for simulating:

* Custom EV sessions in a charging hub
* A maximum grid connection for the charging hub
* Net power minimization
* Energy cost minimization
* Combined optimization

In all exercises we will compare different smart charging methods and we will evaluate the results taking into account the performance of the charging hub together with the impact to the EV user.
