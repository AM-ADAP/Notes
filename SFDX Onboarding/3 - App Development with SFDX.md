# Set Up Salesforce DX Tools

https://trailhead.salesforce.com/content/learn/modules/sfdx_app_dev/sfdx_app_dev_setup_dx?trailmix_creator_id=tschuitemaker&trailmix_slug=sfdx-developer-onboarding-trailmix

## Getting Started with Source-Driven Development

- SFDX shifts source of truth from the org to your VCS
- It shifts dev focus from org dev to package dev

## What is a Scratch Org?

- A dedicated, configurable short term SF Env

### Use Scratch Orgs For

- Start a new project.
- Start a new feature branch.
- Test a new feature.
- Start automated testing.
- Perform development tasks directly in an org.
- Start from “scratch” with a fresh new org.

- Although Scratch orgs are disposable, the scratch org conf files are the real brawn
- Through the conf you can configure the org w/ different sf editions and features and settings

### Do Scratch Orgs Replace Sandboxes?

- No, they have a max 30 day lifespan.
- Sandboxes which contain all the metadata of prod, are still necessary for final user-acceptence testing CICD and staging

### Enable Dev Hub

- A Dev Hub provides you and your team with the ability to create and manage scratch orgs. Scratch orgs are temporary Salesforce environments where you do the bulk of your development work in this source-driven development paradigm.

### Log Into Dev Hub

`sf org login web --set-default-dev-hub --instance-url <url> --alias DevHub`

### The Power of Aliasing

`sf org open --target-org DevHub`
`sf limits api display --target-org DevSandbox`

- Aliasing is a powerful way to manage and track orgs

### View All Orgs

`sf org list`

# Lesson 2 - Get Ready to Create an App

## Create a SFDX Project

- Before you can build your first app, create a project and connect it to your source control repo
- A SFDX Project is a lcoal copy of your package metadata, a group of related code and customizations
- It contaiqns the core assets required to sync local project source and metadata with scratch orgs

`sf project generate --name geolocation`

- This creates a folder called geolocation, and scaffolds a new project w/ all assets in file structure

`sfdx-project.json`

- File indicates that the directory is a SFDX Project. It contains project info and facilitates auth of orgs.
- In this file you specify
  - Paths to source code, classes, metadata
  - The namespace, optional
  - The api version of your source

`/config/project-scratch-def.json`

- Determines the configuration of scratch org, including which features and settings define its org shape.
- You can create a conf that your whole dev team can share.

`/force-app`

- Dir that contains source for proj

## Configure a Scratch Org Definition File

- Let you create scratch orgs easily w/ different features or preferences for testing.
  - EX. YHou can toggle sf mobile web caching
- Optionally update to make it more personal, like changing orgName

## Create a Scratch Org

### Basic Workflow for Using Scratch Org

1. Push local source and metadata to scratch org.
2. Pull any changes you make in scratch org back to local project
3. Sync this project w/ source control repo

`org delete scratch`

- This command deletes a scratch org.
