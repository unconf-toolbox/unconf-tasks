# unconf-planner

Planning an unconference is a lot of work! Since many of the steps (setting up a website, facilitating participant communication, etc.) occur on GitHub, it may be useful for organizers to conduct their project management on GitHub as well. 

This repo can help create a set of milestones and issues related to unconference planning. This can help organizers track their progress towards unconference preparation, assign tasks, and monitor progress. Please feel free to make PRs to the existing YAML template for tasks or to add new templates for different types of planning.

Edit the included `YAML` file to contain the steps you feel pertain to your unconference. Note that, besides title, issues can also contain a `body`, `labels`, and `assignees`. Similarly, milestones can contain a `due_on` date. More information on writing your YAML file can be found [here](https://emilyriederer.github.io/projmgr/articles/building-custom-plans.html)

Once you feel you have fully articulated the main project-management tasks, you can post them to GitHub with the following code.

```r
# install_github("emilyriederer/projmgr")
library(projmgr)
repo <- create_repo_ref("unconf_org", "planning_repo")
plan <- read_plan("unconf_planning.yml")
post_plan <- post_plan(repo, plan)
```
