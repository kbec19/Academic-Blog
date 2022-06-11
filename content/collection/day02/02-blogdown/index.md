---
date: "2022-05-01"
excerpt:
subtitle: Getting Comfy With R
title: DACSS 601
weight: 2
---

# R Workflow

## Understand the Elements of Your New Workflow

+ Complete these [installation instructions](https://happygitwithr.com/install-intro.html).
    
+ Test your connection between GitHub and RStudio following [these steps](https://happygitwithr.com/connect-intro.html). 
    
+ **NOTE:** Experts *strongly recommend* that if you are not already a fluent GitHub user you choose [HTTPS over SSH](https://happygitwithr.com/credential-caching.html).

+ Read through as much as possible on [Happy Git With R](https://happygitwithr.com/index.html) to understand how Git, GitHub, R, and RStudio and how they all work together.

## Installations

After installing Git/GitHub/R/RStudio, there are some packages you will use from the beginning, which you can install by connecting to the internet, opening RStudio, and running at the command line:

    ```r
    > install.packages(c("usethis", "remotes", "distill", 
                       "postcards", "here", "tidyverse"))
    ```

## Get Down with Markdown

+ It's easy to complete this [10-minute interactive tutorial on Markdown](https://commonmark.org/help/tutorial/). 

+ This is your resource for [RMarkdown](https://rmarkdown.rstudio.com/)

## Configure Your GitHub Profile

+ [Personalize your profile](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/personalizing-your-profile)

+ [Pin projects to profile](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/pinning-items-to-your-profile)

## Customize Your Profile README

You can share information about yourself with the community on GitHub by creating a profile README. GitHub shows your profile README at the [top of your profile page.](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/managing-your-profile-readme)

---

# Postcards

## Pre-requisites

First, make sure you have the latest version of the postcards package installed from CRAN:

```
install.packages("postcards")
```

Restart your R session. If you use RStudio, use the menu item *Session > Restart R* or the associated keyboard shortcut:

+ <kbd>Ctrl + Shift + F10</kbd> (Windows and Linux) or
+ <kbd>Command + Shift + F10<kbd> (Mac OS). 

```
packageVersion("postcards")
[1] ‘0.2.3’
```

## Create GitHub repo

Online.

## Clone GitHub repo

```
usethis::create_from_github("https://github.com/apreshill/global-postcard.git")
```

:sparkles: Commit & Push! :sparkles:

You should be committing these files:

+ `*.Rproj`

+ `.gitignore`

## Create a postcard {#templates}

Inside your current postcards project, use the R console:

```
library(postcards)
```

Then you could run (wait- don't do this yet!):

```
create_postcard()
```

But you could also pick one of four templates:

1. `"jolla"` (<https://seankross.com/postcards-templates/jolla/>) [the default]

1. `"jolla-blue"` (<https://seankross.com/postcards-templates/jolla-blue/>)

1. `"trestles"` (<https://seankross.com/postcards-templates/trestles/>)

1. `"onofre"` (<https://seankross.com/postcards-templates/onofre/>)

```
create_postcard(template = "jolla") #default
create_postcard(template = "jolla-blue")
create_postcard(template = "trestles")
create_postcard(template = "onofre")
```

<aside>
Want to know more? Under the hood, these are R Markdown templates, which you can include in a package.
</aside>

## Anatomy of a postcard

YAML, body, name is index- this is special

:sparkles: Commit & Push! :sparkles:

You should be committing these files:

+ `index.Rmd`

+ `*.jpg`

But! There is no `.html` file (yet...)


## Knit the postcard

Knit button or

```
rmarkdown::render("index.Rmd")
```

What is new in your Git pane?

:sparkles: Commit & Push! :sparkles:

You should be committing this files:

+ `index.html`

(You may get a warning in RStudio IDE that this file is too big- go right ahead)

## Publish a postcard

+ Push, publish to GitHub pages
https://docs.github.com/en/github/working-with-github-pages/creating-a-github-pages-site#creating-your-site

## Share your postcard!

Add it to your repository details

---

# Create a Distill Blog/Site

## Pre-requisites

First, make sure you have the latest version of the distill package installed from CRAN:

    install.packages("distill")

Restart your R session. If you use RStudio, use the menu item *Session \> Restart R* or the associated keyboard shortcut:

-   <kbd>Ctrl + Shift + F10</kbd> (Windows and Linux) or
-   <kbd>Command + Shift + F10<kbd> (Mac OS).

```{=html}
<!-- -->
```
    packageVersion("distill")
    [1] ‘1.3’

## Create GitHub repo

Online.

## Clone GitHub repo

    usethis::create_from_github("https://github.com/yourname/global-distill.git")

:sparkles: Commit & Push! :sparkles:

You should be committing these files:

-   `*.Rproj`

-   `.gitignore`

## Create a new distill site

Inside your current distill project, use the R console:

    library(distill)

Let's start with a simple website:

    create_website(dir = ".", title = "global-distill", gh_pages = TRUE)

Now, let's commit all these new files and push to GitHub.

## Build site

Please *close* RStudio and re-open it. Look in your Git pane, you should see a single file has changed:

<center>

<img src="rproj-git.png" width="500"/>

</center>

Let's look at the diff:

<center>

<img src="rproj-diff.png" width="500"/>

</center>

Let's go ahead and commit this file before we start adding to our site.

You should see:

![RStudio build site tab](https://rstudio-education.github.io/sharing-short-notice/images/screenshots/build-site.png)

## Add a postcard

Docs: <https://rstudio.github.io/distill/website.html#postcards>

Now, delete your `about.Rmd` (trust me!). We'll create a new one with the postcards package.

```
create_article(file = "about",         # future name of .Rmd file
               template = "jolla",    # name of template
               package = "postcards")
```

[Reminder: templates]({{< ref "/02-postcards#templates" >}} "Postcards templates")


## Site navigation

`_site.yml`

## Theme

Docs: <https://rstudio.github.io/distill/website.html#theming>

    distill::create_theme("me")

Remember your `_site.yml` file? Add the theme line there:

``` {.yaml}
name: "Me"
title: "Personal website of Me"
description: |
  This is my personal website.
output_dir: "docs"
theme: me.css
navbar:
  right:
    - text: "Home"
      href: index.html
    - text: "About"
      href: about.html
output: distill::distill_article
```

## Publish a distill site

Easy:

-   Push, publish to GitHub pages <https://docs.github.com/en/github/working-with-github-pages/creating-a-github-pages-site#creating-your-site>

Medium:

```
> use_github_pages(branch = "main", path = "/docs")
✓ Setting active project to '/Users/me/rscratch/global-distill'
✓ Activating GitHub Pages for 'yourname/global-distill'
✓ GitHub Pages is publishing from:
● URL: 'https://yourname.github.io/global-distill/'
● Branch: 'main'
● Path: '/docs'
```

  



