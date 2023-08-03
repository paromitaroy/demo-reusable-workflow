# :rocket: Reusable Workflow

Demo repository for reusable workflow

- :exclamation: **This is a template repository**
- :exclamation: **This demo contains GHEC/GHES-specific features**
  - The **Reusable Workflow** feature is only available for GHEC, GHES (>=v3.4), and public repositories 
- **If you have a GHEC organization available**, then please click ***Use this template*** to clone the repo into that organization
- **If you do not have a GHEC organization available**, please run the demo in this repository. Just make sure to complete the **Cleanup** steps afterwards :house_with_garden:

## Usage 

### Creating environments

1. In the repository, go to **Settings** --> **Environments**
1. Create an environment (e.g. `test`)
    - No additional settings
1. Create another environment (e.g. `prod`) 
    - Add a required reviewer (you can set yourself as the required reviewer)
    - The protection rules will be used later in the demo

### Using reusable workflow

:bulb: Ensure that environments added above corresponds to what is defined in the caller workflow's inputs.

1. Walk through syntax of `.github/workflows/caller.yml`
    - Demo how it defines a callee workflow
1. Walk through syntax of `.github/workflows/callee.yml`
1. Go to the Actions tab, select `Caller Workflow` then trigger the wokflow mannually via `Run Workflow`
    - Select environment to run as `test` or `prod`
1. If **Required reviewers** were added to the environment, the workflow should be halted until it is reviewed
1. Show how to review a deployment, and ensure the job proceeds
1. Show logs and how callee workflow is ingested params passed by caller workflow

### :house_with_garden: Cleanup

1. If the workflow was run in this repository, perform the following steps:
    - Delete all environments created
