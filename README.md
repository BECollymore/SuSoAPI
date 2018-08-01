# Survey Solutions API

Different functions that use the Survey Solutions API to different functions. Currently, there is only functions to download data.

## Getting Started
### Prerequisites
These programs uses R to interact with the Survey Solutions API so you will need to install R and R Studio on your computer.

* [R](https://cran.rstudio.com/)
* [RStudio](https://www.rstudio.com/products/rstudio/download/)

You will also need to make an API user account on your survey server. Learn how to make an API user account on the [support page](http://support.mysurvey.solutions/customer/en/portal/articles/2844104-survey-solutions-api?b_id=12728).

### How to use?
Download the the repository by clicking on the green **Clone or download** button on the right side under the respository name.This will download all the code and read me files onto your computer in a zip file.

You can use the function in one of two ways:
1. Run the R file for the function in R Studio by opening it and pressing **Ctrl+Shift+Enter**. This will run all the code for the function in the file and now the function will be in the working environment for use for this session.
2. In the menu, go to **Code -> Source File...** or use the **Ctrl+Alt+G** keyboard shortcut. Select the function you would like to use and now it will be available for use in the working environment.

### Running R code in Stata
It is possible to call R code in Stata using the [rcall package](https://github.com/haghish/rcall) that can be installed using ssc in Stata. To install rcall from inside Stata, run 
```
ssc install rcall
```

This packages allows R and Stata to exchange data so it is possible to use these API functions in Stata with rcall. However, this will require writing a script in R to download the data from the API. Use it only after reading the documentation for rcall thoroughly.

## Description of functions currently available:
* [dl_one](help/dl_one.md): Downloads the data for the specified version for the specified questionnaire
* **dl_similar**: Downloads the data for all questionnaire that matches a specified pattern. Can use regex patterns.
* **dl_allvers**: Downloads all versions of the specified questionnaire.
* **get_qx**: Gets information about all the questionnaires imported on the server
* **get_qx_id**: Returns the template ID of the specified questionnaire
