<p align="left">
  <img src="img/liquibase.png" alt="Liquibase Logo" title="Liquibase Logo" width="324" height="72">
</p>

# Welcome to Liquibase!
This repository contains demo scenarios for the "Azure DevOps and Liquibase Flows" webinar originally delivered on December 19th, 2024. Recordings of all webinars can be found [here](https://www.liquibase.com/videos).

## Demo Steps
1. Clone this repository
1. Download and Install Liquibase CLI
    * [Link](https://www.liquibase.com/download)
1. Open Command Prompt and Start the H2 Database
    ```
    liquibase init start-h2
    ```
    *Safe to close browser window*
1. Open New Command Prompt and Create Sample Flow
    ```
    liquibase flow
    ```
    *Select option 3*
1. Run the Workflow
    ```
    liquibase flow
    ```    

## Liquibase Documentation
* [Documentation Home](https://docs.liquibase.com/home.html)
* [Liquibase University](https://learn.liquibase.com/)

## Core Concepts
If you are unfamilar with Liquibase concepts, here is some information to get you started.

* [Changeset](https://docs.liquibase.com/concepts/changelogs/changeset.html): basic unit of database work
* [Changelog](https://docs.liquibase.com/concepts/changelogs/home.html): text file containing collection of changesets
* [Tracking tables](https://docs.liquibase.com/concepts/tracking-tables/tracking-tables.html): tables created and maintained by Liquibase

## Helpful Liquibase Commands
|Command |Description|Documentation
|----------|------------|------------|
| connect | Test database connection | [Link](https://docs.liquibase.com/commands/change-tracking/connect.html)
| flow | Execute a Liquibase workflow | [Link](https://docs.liquibase.com/commands/flow/flow.html)
| status | Show undeployed changes | [Link](https://docs.liquibase.com/commands/change-tracking/status.html)
| update | Run changes against target database | [Link](https://docs.liquibase.com/change-types/update.html)
| history | Show deployed changes | [Link](https://docs.liquibase.com/commands/change-tracking/history.html)
| rollback-one-update | Rollback the last or a specified update | [Link](https://docs.liquibase.com/commands/rollback/rollback-one-update.html)
| checks | Show or view policy checks | [Link](https://docs.liquibase.com/liquibase-pro/policy-checks/workflows/home.html)

## Liquibase in Automation
Liquibase Pro can work with any automation tool which supports invoking command-line tools. Liquibase provides working examples for some popular automation platforms.

* [Ansible Tower](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/Ansible_Tower/liquibase_playbook.yml
)
* [AWS CodeBuild](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/AWS_CodeBuild/buildspec.yml)
* [Azure Dev Ops](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/Azure_DevOps/azure_pipelines_docker.yml) (build)
* [Bitbucket Pipelines](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/Bitbucket/bitbucket-pipelines.yml)
* [CircleCI](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/CircleCI/config.yml)
* [GitHub Actions](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/GitHub_Actions/liquibase_workflow.yml)
* [GitLab](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/GitLab/gitlab-ci.yml)
* [Jenkins](https://github.com/liquibase/liquibase-toolbox/blob/master/build_scripts_examples/Jenkins/Jenkinsfile)

## Contact Liquibase
* Liquibase sales: https://www.liquibase.com/contact
* Liquibase support: https://support.liquibase.com

# Thank you!
Thank you for evaluating Liquibase Pro! We hope to be a part of your DevOps journey.