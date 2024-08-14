

<div style="vertical-align:center; width:100%;"><img alt="# cometa - Complete Meta Test Automation" src="img/logos/COMETAROCKS_LogoEslog_Y_W.png"></div>

Co.Meta was created to help DevOps, SDETs, QA Engineers, Software Developers, and Business Teams easily repeat testing with a codeless and coding-based approach be it on-premise or on cloud.

Cometa stands for complete meta test platform.

Meta (from the Greek μετα-, meta-, meaning "after" or "beyond") is a prefix meaning more comprehensive or transcending. [source Wikipedia](https://en.wikipedia.org/wiki/Meta). 

With Co.Meta you can test over system boundaries, you can go to one application, fetch data, and save it in variables. Then, go to another application and use the data to test against content or use it as search input. This is just a glimpse of the versatility and flexibility of the tool. As the product is being improved and upgraded, its versatility and flexibility will only be enhanced for the sake of user satisfaction and usefulness.


Co.Meta uses both codeless and code based approach to define test steps and executes them using behave (BDD approach) against selenium web-driver, which grabs virtual or real browsers from Selenium Hub. The results from the execution (timing, steps execution logs, screenshots, video, etc.) are stored in the filesystem and referenced in the database. The results can be consumed via REST API or easily in your browser with Co.Meta's User Interface is built with Angular. 

Co.meta is available on cloud and on-prem.

You are looking at the Cometa Community Edition (CE) [licensed](#license) under AGPLv3. See [Cometa Versions](#cometaversions) to understand the difference from Cloud Edition (CEE) and the Enterprise Edition (EE).

# Table of Contents 

- [Cometa Versions](#cometaversions)
- [Cometa History](#cometahistory)
- [Cometa Features](./cometa_features.md)
- [Cometa Actions](./cometa_actions.md)  

All about testing
- [Cometa Overview - 5W1H](#cometamindmap)
- [What is a Testplan / Feature](#whatis_a_testplan)  
- [Your first test](#general) 
- [All about cometa steps](#allaboutsteps)
- [All about selectors](#selectors) 
- [Data Driven Testing](#datadriventesting) 
- [Execute](#execute-javascript)
- [Compare values](#compare-selector-values)
- [Create sub-feature](#create-sub-feature)
- [Up- and Downloading Files](#up-and-download)
- [Questions](questions.md)

All about integration
- [Integration with Webhooks](#integration) 
- [Integration with Git](#integrationgit) 
- [REST API](#restapi) 
- [Security](#security) 
- [Housekeeping](#housekeeping)

Last but not least
- [Sponsors](#sponsors) 
- [Want to help?](#wanttohelp) 
- [Need support/help?](#needhelp) 
- [Design and Logos](#design) 
- [License](#license) 

<a name="cometaversions"></a>

# Cometa Versions

Cometa comes in various flavors:

**Community Edition** 

The public github repo containing the source code for installation is at [github.com/cometa-rocks/cometa](https://github.com/cometa-rocks/cometa/).  The Community Edition does not include cloud and enterprise features and in general lags behind the leading cloud/enterprise repo.

Co.Meta Community edition is licensed under AGPLv3. See the [license details](#license).


**Cloud Edition Enterprise**

A hosted-by-us version is ready for you to use. There are 4 plans: Standard, Silver, Gold, and Enterprise Cloud for you to choose from. The details of these plans are subject to official interactions. 

<a name="cometahistory"></a>

**Enterprise Edition**

To use the Enterprise (On-premise) Edition, you need an Enterprise License. It has all the features of the Premium Plan under Cloud Edition and comes with exciting perks such as onboarding support for the QA team, unlimited projects, unlimited users, all web browsers, priority support, and many more exciting advantages.

# Cometa History

Development started around 2014-2015, when Daimler AG, Germany asked for an agile process of testing financial enterprise reporting web applications. Since then Co.Meta has come a long way.

| Year | What was done |
| :---: | :--- |
| 2014 | First Proof-of-Concept (PoC) with Daimler |
| 2016 | Starting Development of Version 0.1 of Co.Meta |
| 2018 | Co.Meta goes into Production |
| 2019 | Second major PoC with Daimler |
| 2020 | Development + Enhancement of pre-built steps to be more intelligent and robust |
| 2021 | Chaining of execution via automated scheduling, development of new landing (beta). Inauguration of public repo on GitHub |
| 2022 | New customers signup for Enterprise-Grade Testing. Pilot promotional activities begin within a select community of software engineers for feedback |
| 2023 | With the confidence established in Co.Meta, a global legal entity is formed to promote the product for we firmly believe that the future is open source with enterprise grade architecture and security. With our 1st of its kind concept in the world, we are on the way to make a difference in the world |
| 2024 | Roadmap: Enhance Data Driven Editor, Import and Migrate Tests from other platforms, Database Testing, AI usage for finding better selectors, Load Testing, Show Network and Browser KPIs via CDP (Chrome) | 


<a name="cometamindmap"></a>

# Cometa Overview - 5W1H

To get a high-level overview in mindmap format - find the "5W's" and "1H" ... [What, When, Where, Why, Who, & How about Cometa - here](https://www.xmind.net/m/U8BJXc).

You can also watch this [video](https://www.youtube.com/watch?v=8uv-QAJkOLY) to understand the "5W's" and "1H" of Cometa with practical demonstration.


<a name="whatis_a_testplan"></a>

# What is a Testplan versus Feature

A testplan or feature consists of general information, browser selection, and the steps/actions that should be executed one after the other. 

So what is the difference between a Testplan and a Feature?

When we speak of something that we want to test - what do we mean?  Do we want to test a login or a menu functionality? Do we want to test a navigation path?
Is that a feature of our application? Or is that a testplan?

So, to get things right:

* A feature in our world is a building block. We want to test a feature (one single behavior) on mobile and on desktop. That means: can we click on every element of the menu and is the result as expected? That is a feature. We call the feature "menu".
* Several features will then be grouped into a test plan. So testing an application consists of: test menu, test upload, test searching and test backend.

So testing a whole application consists of testing many features on different devices. That is a testplan.

With Co.meta you can include anything anywhere. A Login feature may be always necessary and from there, you test different sections of your applications.
Co.meta does not have a hierarchy. You can run anything anywhere else.

This being said, it is your part to structure your tests and working with Co.meta will help you reuse anything anywhere else. Whenever you encounter something that you did before - just include it.

Somehow Co.meta is like wikipedia, anything depends, may depend or may be singular.

A common hierarchy we encounter is:
```
| Call some URL (DEV/STAGE/PROD)
|-- From there do the login (but this login is used anywhere else)
   |-- On Stage test using parameters xzy
   |-- On Prod test using parameters xyz
```

So, we end up tying parameters and URLS to environments.

Is this still a feature or a test plan? It is complex, where anything depends on how you want to use it and how you structure it. Co.meta provides you the possibilities. At the end, it is you who structures everything in a way that is good for your application.

<a name="general"></a>

# Your first test 

The first Chapter provides information on steps/actions to be used in your test plan.

A good way to start is to just [grab our example](feature_example_your_first_testcase.json) and paste it into the cometa using the ``Import Json`` button in the feature editor.


<a name="allaboutsteps"></a>

# All about Cometa steps

Cometa comes with over 70 predefined steps like "Goto {URL}", "Wait until I can see {something} on page". 

See the detailed documentation on every possible step grouped by mouse-actions, keyboard actions, selector option, etc. 
[documentation of steps](cometa_actions.md). 

You want to see the code running below? See [actions.py](https://github.com/cometa-rocks/cometa/blob/master/backend/behave/cometa_itself/steps/actions.py)

<a name="selectors"></a>

# All about selectors 

In cometa, you can use selectors. Cometa automatically tests for ID, tag name, class name, inner HTML, and XPath.

Therefore, in most cases, you do not have to worry about separating XPath or css selectors. Just use them and cometa will understand what you are looking for.

Q: How do I select a button? 
A: Use the step `"I move mouse to {selector} and click"`. Replace "{selector}" with a xpath selector "//button[.='Text seen on button']" or using css e.g. button:nth-of-type(1)
A: Use the step `I can click on button "{button_name}"`. Where button name translates into the text of the button or any attribute with that text.

We have put together a huge summary about selectors and differences between CSS and X-Path. [learn about selectors like CSS and xpath](css-xpath.md). 


<a name="datadriventesting"></a>

# Data Driven Testing (DDT)

Cometa can store content from selectors in variables, which can then be used in any other step ... to compare, send keys, wait for ... .

A general use case is: go to application A, read the products from selector xyz and store that into variable $foo. Goto application B and test selector zyx to contain values from $foo. 

Steps to use for this:
```
Save selector "//h3[1]" value to environment variable "SEARCHRESULTS"
Save list values in selector "{css_selector}" and save them to variable "{variable_name}"
```

Variables can then be used in any other step like this:

```
Send keys "$SEARCHTERM"
```

Variables can be based on `Environment`, `Department` or `Feature`, which the user is able to specify in the process of it's creation.
* If user specifies that variable must be based on `Feature`, it will be private to the feature that is currently being edited, meaning that it will not be accessible from other features, independently of department or environment these belongs to.
* If variable is based on department or environment, it will be accessible from any feature that belongs to same department or environment.


Since quantity of variables tends to gradually increase, at certain point it can becomes somewhat time consuming to track the desired variable. For this reason we developed a popup that you can make use of to efficiently search and insert variables directly into steps. With this new implementation, user has no need to first search for desired variable and then manually write it's name in step.

* For popup to open, write `$` character in step's predetermined slot for variable insertion - `"{$variable_name}" > "$"`, this will display all the accessible variables.
* To filter variables, follow up `$` character with desired key word.  Ex: `"$foo"`.
* Variables are filtered `inclusively`, meaning that provided keyword does not have to be exact name of variable, if variable's name contains provided keyword, it will be displayed.
* By clicking any of the variables in the popup, you will be able to insert it into step automatically.
* If match can not be found for provided key word, popup will display a message, informing user that no variable can be found based on current key word.

Variables depend on the environment set in your feature, so you can store different variables for DEV, INTEGRATION, STAGE and PROD environments. 


Another use case for illustration could be: Search result validation
* Go to google and search for `cometa rocks`
* Save the value from the first search result to variable `VARIABLE_SEARCHRESULT` (note: this is without the `$` sign!!).
* Go to bing and search for `$VARIABLE_SEARCHRESULT` (note: here we use the variable with the `$` sign!!).

See this [JSON File](feature_example_your_first_testcase.json) as a starting point.

Another use case is: Order validation
* Go to application A, order a product, and save the order confirmation number to variable `XYZ`.
* Go to application Backend, select the new orders list, and search for order number `XYZ`.


<a name="execute-javascript"></a>

# Execute your own Javascript

Use the step: `Run Javascript function "{function}"`
   
Replace "{function}" with `alert('foo')` to get a basic understanding. Inside the ""(quotes) you can place anything any valid JavaScript code. You do not need to escape quotes (") — Cometa handles that for you.

If you want to use  x-path selectors in Javascript, use document.evaluate() function. See details at: https://developer.mozilla.org/en-US/docs/Web/API/Document/evaluate

<a name="compare-selector-values"></a>

# Compare the values of two selectors over system boundaries

To compare selector values between System A and System B, use the following step:

This steps does the magic for you:
`Test list of "{css_selector}" elements to contain "{all_or_partial}" values from list variable "{variable_names}" use prefix "{prefix}" and suffix "{suffix}"`

```
List A: Featured;Price: Low to High;Price: High to Low;Avg. Customer Review;Newest Arrivals
List B: Featured;Price> Low to High;Price> High to Low;Avg. Customer Review;Newest Arrivals
```

The ":" and ">" in the middle cannot be handled by the Prefix/Suffix from cometa.

Solution:
Use the `"Execute Java-Script"` beforehand and get the formatting right. 

* Get the value from the selector via Javascript.
* In the same function, split it and write it to the DOM.
* Use a next step in cometa to fetch your updated selector to a variable.
* Then compare.

Another Example: "Assert for a string to have a certain format, e.g. the string is longer then 5 characters"

To acomplish this, save the string you want to assert in an environment variable. You can do this manually or let cometa do this using the step `Save selector "{css_selector}" value to environment variable "{variable_name}"`. This step looks for a value-tag or innerHTML, creates the specified variable, and saves the value into it. A typical use case is a data entry system with values need to be checked in a reporting system or a summary list. So, first grab the value from a selector, e.g. `//input[@id='ordernumber']` and save it into a variable MYORDERNUMBER.

Then use `Run Javascript "{function}"` as step and assert with javascript on the format, e.g. the following code checks that the string is longer then 5 characters: `Run Javascript function " if ( !"$MYORDERNUMBER".length>5 ) throw "Found an Error: Order Number is not greater than zero" "`.

Other examples:
* Assert that ordernumber starts with "X-": `Run Javascript function " if ( !"$MYORDERNUMBER".substring(0,2)=='X-' ) throw "Found an Error: Order Number is not greater than zero" "`
* Assert that ordernumber is exactly 10 characters and ends with "-0": `Run Javascript function " if ( !"$MYORDERNUMBER".substring("$MYORDERNUMBER".length-2)=='-0' || !"$MYORDERNUMBER".length==10  ) throw "Found an Error: Order Number is not greater than zero" "`

<a name="create-sub-feature"></a>

# Create a sub-features

Sub-features are useful for including repeating tasks in other steps.

For example, if you always need to log in to your system before testing, you would create a feature called "Logon System XYZ" and include this feature in all other features using the step "Run feature with {name or id} before continuing".

<a name="up-and-download"></a>
# Upload and Download Files

For **Uploading** use the step `Upload a file by clicking on "{selector}" using file "{filename}"`.

`selector` is the XPath, ID, or CSS selector of the input field to be used.

`filename` is the path of the upload file in the headless browser's home directory. 

Inside the home directory of the virtual browsers, there are two folders: "Downloads" and "uploads". In "Downloads," all downloaded files from any test case can be found in a subfolder with the feature ID.

Files in the "uploads" folder can only be provided by system administration. The files must be copied to <cometainstallation>/backend/behave/uploads/.

The following dummy files are located in the uploads folder: dummy.mp4, dummy.pdf, dummy.png, dummy.txt, and dummy.xlsx.

In general, Selenium cannot control the upload window that normally pops up when you click "Upload something."

Question: How do we upload something if we cannot control the window responsible for this?

Answer: We select the input field in HTML where the file should be stored and send the upload filename via send_keys() into that item.

Question: What if my input field is hidden and I cannot select it?

Answer: Make it visible with JavaScript by setting the correct attributes, such as display: inline.

For **Downloading** use the step `Download a file by clicking on "{linktext}"` ... downloads a file, watch which file is downloaded and assign them to feature_result and step_result, linktext can be a text, css_selector or even xpath

The downloaded file can be reused for uploading somewhere else.

<a name="step-timeouts"></a>
# Step timeouts
Timeouts are an important part of a feature's steps, as execution time may vary based on the step's description. We provide three mechanisms to work with timeouts:
* Manual Timeout: Set timeouts manually for each step.
* Department Default Timeout: Edit a department to set a global timeout for that department. By default, every department has a timeout of 60 seconds. Changing the department's default step timeout will only affect steps created after the change. Steps created before the change will maintain their original timeout.
* Global Timeout Adjustment: Modify the timeout for all steps in a department, adjusting from {x} seconds to {y} seconds.

<a name="integration"></a>


# Integration with Webhooks

Integration with Webhooks allows you to receive feedback on test results. Any application supporting webhooks can be notified by Cometa at the end of a test execution, either on error or always.

The integration is user and department-dependent. Each user can have different notifications. If two users use the same webhook, the webhook will be executed for each user.

<a name="integrationgit"></a>

# Integration with Gitlab / Github

To integrate Cometa into your CI/CD pipeline, use the REST API. You can trigger any action that you would perform from the UI via REST API. It is straightforward.

See [`integration with gitlab`](https://github.com/cometa-rocks/cometa/blob/master/scripts/integration-with-gitlab.sh)  as an example. Depending on your authentication provider and URL endpoints, you may need to adapt the variables and URL endpoints in the script.

<a name="restapi"></a>

# REST API
   
The Cometa REST API is Django-based. See the [REST API](/REST-API.md) for details.


<a name="housekeeping"></a>

# Housekeeping

Cometa generates a lot of videos and images. Every night, Cometa performs housekeeping by removing all images and videos from executions older than 60 days (default).

The housekeeping time frame can be set per department.

To save a Cometa execution result for legal documentation, select "Save this run." This will mark the result as saved and it will disappear from the standard view. Select "View saved runs" to view your saved results.

Saved results will not be affected by housekeeping.

<a name="security"></a>

# Security

Cometa is secured via [OIDC](https://en.wikipedia.org/wiki/OpenID). OIDC is state-of-the-art enterprise security that integrates with the authentication provider of your choice.

The Free and Cloud Versions of Cometa use Google OAuth and GitLab OAuth as options. 
If you wish to integrate with other authentication providers, please let us know or contribute. We would be happy to accept your pull request.

<a name="sponsors"></a>

# Sponsors

* Mercedes-Benz AG and Daimler Trucks AG, Stuttgart


<a name="wanttohelp"></a>

# Want to Help with Cometa Development?

A good starting point is the documentation. If you see something that could be described better or where information is missing, clone the repo, make the necessary changes or additions, and send us a pull request.

We will then review and update the master branch.

The cometa community thanks you for you help.

<a name="needhelp"></a>

# You are stuck and need some help?

We are here to help you. Please contact us via email <tec_dev@cometa.rocks> or on Discord at https://discord.gg/e3uBKHhKW5  

<a name="design"></a>

# Design

You may use the cometa.rocks logo as long as you respect the layout in any publication. Let us know of your publication, so that we can backlink to it.

## Fonts

Cometa uses Comfortaa as primary font and Montserrat as the secondary font.

## Color

Orange: #f4b829
Black: #191919
## Logos

 <img style="background-color:white" src="img/logos/COMETA_Logo_Y_B.png">

 <img src="img/logos/COMETA_Logo_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETA_LogoEslog_Y_B.png">

 <img src="img/logos/COMETA_LogoEslog_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETAROCKS_Logo_Y_B.png">

 <img src="img/logos/COMETAROCKS_Logo_Y_W.png">

 <img style="background-color:white" src="img/logos/COMETAROCKS_LogoEslog_Y_B.png">

 <img src="img/logos/COMETAROCKS_LogoEslog_Y_W.png">

<a name="license"></a>

# License
   
Cometa.Rocks is licensed under AGPLv3 - see details in `LICENSE`(https://github.com/cometa-rocks/cometa_documentation/blob/main/LICENSE)
