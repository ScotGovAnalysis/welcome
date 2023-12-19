# Scottish Government Analysis

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)

New to GitHub or this organisation? Welcome!

This GitHub organisation is for analysts in the Scottish Government and its agencies to code and collaborate in the open.

Analysts in Scottish Government and departments should use this GitHub organisation. This keeps everything in one place and makes it simpler to manage membership.

## Get started
- Read the guidance below
- Create a GitHub account with your work email address
  - Some people use their GitHub accounts for things that aren’t part of their job, such as personal projects or freelance work. If this applies to you, add a personal email address and then make sure you author commits with the appropriate email address, depending on the project you’re working on.
- Enable [two-factor authentication](https://help.github.com/en/articles/about-two-factor-authentication) (@jsphdms personally finds LastPass Authenticator user friendly)
- Add a (work appropriate) photo and username
- Add your contact details and employer
- [Request to join](https://github.com/ScotGovAnalysis/welcome/issues/new?assignees=alicebyers5%2Ctomwilsonsco%2Cjsphdms&labels=member-request&template=new-member-request.yml&title=New+member+request) the [Scottish Government Analysis](https://github.com/ScotGovAnalysis) organisation.
- [Set your membership to public](https://help.github.com/en/articles/publicizing-or-hiding-organization-membership)
- [Create a repo](https://help.github.com/en/articles/create-a-repo) and set ScotGovAnalysis as the owner. Make sure it’s relevant to other analysts within Scotland’s public sector. A relevant example might be: source code for an R Shiny app that accompanies an official statistic. A non-relevant example might be: code for a personal learning project.
- [Add topics to your repo](https://help.github.com/en/articles/classifying-your-repository-with-topics) to help keep them organised. Your topics can include things about what area your repo is used for (e.g. exports) or what organisation it is for.
- Tell people about your repo

## Why code in the open?
There are many [benefits to coding in the open](https://gds.blog.gov.uk/2017/09/04/the-benefits-of-coding-in-the-open/) and the UK government has published guidance on [how to do it securely](https://technology.blog.gov.uk/2017/09/27/dont-be-afraid-to-code-in-the-open-heres-how-to-do-it-securely/). [Governments across the world](https://government.github.com/community/) are coding in the open and Scotland’s public sector is no exception (see [Public Health Scotland](https://github.com/Public-Health-Scotland), [Marine Scotland](https://github.com/MarineScotlandScience/), and the [Improvement Service](https://github.com/improvement-service)).

> Public services are built with public money. So unless there’s a good reason not to, the code they’re based should be made available for people to reuse and build on. **UK Government - [Digital Service Standard](https://www.gov.uk/service-manual/service-standard) (12. Make new source code open)**

> Writing code is much easier if you don’t do it alone. Your goal should not be to strive in solitude for years before releasing the perfect package. Instead, work in the open, publishing not only the final product but every intermediate stage. If you work this way, you’ll get feedback much earlier in the process, and your motivation will remain high because you know people care. **Hadley Wickham - [Impact the world by being useful](http://bulletin.imstat.org/2014/12/hadley-wickham-impact-the-world-by-being-useful/)**

## Your responsibilities
You are responsible for anything you share online. Before sharing anything on GitHub, reflect on your ethical, legal and professional obligations. Things to consider:

- Certain legislation may apply to your work such as [the GDPR](https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/) and the [Data Protection Act 2018](https://ico.org.uk/for-organisations/data-protection-act-2018/)
- You may be bound by the [Code of Practice for Statistics](https://www.statisticsauthority.gov.uk/code-of-practice/) (in particular [T6: Data governance](https://www.statisticsauthority.gov.uk/code-of-practice/the-code/trustworthiness/t6-data-governance/))
- GitHub stores a full history of your files and this GitHub organisation is a public space
- Your organisation may have an internal policy that covers coding in the open (e.g. an IT code of conduct)
- It might be appropriate to do a risk assessment
- Check with your line manager if you’re unsure of anything

## Security
Don’t share anything you shouldn’t share. Store these separately from your code (e.g. as [environment variables](https://csgillespie.github.io/efficientR/r-startup.html#renviron)):

- Usernames
- Passwords
- API keys
- Secrets
- Tokens
- Absolute filepaths

Use [pre-commit and pre-push hooks](https://github.com/ukgovdatascience/dotfiles) for an extra layer of protection. If you accidentally publish a secret; [assume it is compromised](https://www.gov.uk/government/publications/open-source-guidance/security-considerations-when-coding-in-the-open#assume-accidental-publications-are-compromised), revoke and refresh the secret. Do this no matter how quickly the secret was removed.

## Good practices
These practices might be a little overwhelming if you’re new to coding in the open. It’s not vital to adopt everything from the beginning and some practices may not be appropriate for a given project. These are suggestions to learn over time. The easier ones are near the top:

- Write [good READMEs](http://r-pkgs.had.co.nz/release.html#important-files)
- Add a [lifecycle badge](https://www.tidyverse.org/lifecycle/) to your README
- Use GitHub to [manage projects](https://youtu.be/nI5VdsVl0FM)
- Use a [workflow strategy](https://youtu.be/aJnFGMclhU8)
- Write [good commit messages](https://github.com/alphagov/styleguides/blob/master/git.md)
- Raise [good pull requests](https://www.annashipman.co.uk/jfdi/good-pull-requests.html)

## Resources
If you’re new to Git/GitHub it’s worth reflecting on how you learn best. A mix of structured study and practice works for many people. Teaching others can also be an effective way to learn.

- Coding in the open
  - Anna Shipman (previous Open Source Lead at GDS) compiled these [resources for coding in the open](https://www.annashipman.co.uk/jfdi/open-code-resources.html)
  - The National Archives advise that code created by civil servants is [subject to Crown copyright](https://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/uk-government-licensing-framework/open-government-licence/open-software-licences/). The default licence for that is the Open Government Licence.
- Networks
  - The [datasciencescotland](datasciencescotland.slack.com) slack has a version control channel
  - The [govdatascience](govdatascience.slack.com) slack has a git channel
- Git and GitHub
  - Jenny Bryan (Software engineer at RStudio) authored [Git and GitHub with R](https://happygitwithr.com/)
  - A number of SAS products have [Git integration](https://blogs.sas.com/content/sasdummy/2019/01/17/git-in-sas/)
  - GitHub has a [community forum](https://github.community/), [guides](https://guides.github.com/), [YouTube tutorials](https://www.youtube.com/githubguides), a [learning lab](https://lab.github.com/), and this article on how to [set up Git](https://help.github.com/en/articles/set-up-git)
  - RStudio has an article on [version control with RStudio](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
  - [Pro Git](https://git-scm.com/book/en/v2/) covers using Git on the command line

# Licence
This repository is available under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
