# Lesson 1 - Understanding What Application Lifecycle Management Is

## ALM - Application Lifecycle Management

## 3 Main Development Models

1. Change Set Development
2. Org Development
3. Package Development

## What is safe to change in Prod?

Things that don't affect data <br>

- Dashboards
- Reports
- Email Templates

## Steps in ALM

1. Plan Release

   - Get Requirements

2. Develop

   - Work, following design specs
   - Perform the work in a test environment

3. Test

   - Test out the changes, through unit testing. Test out the functionality

4. Build Release

   - Aggregate all the assets made or modified during dev into a single release artifact

5. Test Release

   - Test what you are going to deploy but in a staging env

6. Release

# Lesson 2 - Learn the Basics of Release Management

## Release Types

Typically releases fall into one of three categories

1. Patch bug fixes and simple changes
   - Simple changes include reports, dashboards, list views, and email templates.
2. Minor changes w/ limited impact
   - These releases typically require testing, but only limited training and change management. Typically, a team delivers the changes for a minor release within a few weeks.
3. Major changes w/ significant impact
   - including changes with one or more dependencies. Because these releases can greatly affect the user experience and data quality, they require thorough testing, training, and careful change management. Major releases are typically delivered once a quarter (Salesforce does it three times a year).

## Change Set Development Tracks Changes

- Each developer tracks any changes made in their customization for the release
- Changes are migrated manually between environments

# Lesson 3 - Manage Changes in Increasingly Complex Releases

- Salesforce CLI can extract Metadata from a dev env to integrate w/ a VCS
- Salesforce CLI can also script routing tasks

# Lesson 4 - Use Package Development for More Flexible Releases

- When you use scratch orgs for development, you first push the source from your project in the VCS to sync the scratch org with the same metadata. If you are planning to use Setup for development, the changes you make are tracked automatically. You can pull down the modifications you made to include them in your project and use your VCS to commit all the changes.
