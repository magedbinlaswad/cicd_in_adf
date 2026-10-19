# Azure Data Factory CI/CD Automation

**Azure Data Engineering | Hands-on Training Project**  
**Digital Edify Technologies | 2025**

---

## Project Overview

This project demonstrates how GitHub Actions can support **Continuous Integration and Continuous Deployment (CI/CD)** for Azure Data Factory (ADF).

Developed during a five-month Azure Data Engineering training program, it covers version control, validation of ADF resources, generation of ARM templates, and deployment workflow configuration. It is a **training project**, not a production system.

## Key Components

- Created sample ADF pipelines using **Wait**, **Copy Data**, and **Delete** activities.
- Configured sample **datasets** and **linked services** for Azure Storage and Data Lake.
- Stored ADF resource definitions in GitHub for version control.
- Set up GitHub Actions to **validate ADF resources** and **export ARM templates**.
- Configured a release stage for Azure authentication and template-based ADF deployment.

## Technologies Used

| Technology | Purpose |
| --- | --- |
| Azure Data Factory | Data pipelines and resource configuration |
| GitHub Actions | CI/CD workflow automation |
| ADF Utilities | Resource validation and ARM template export |
| ARM Templates / JSON | Deployment and configuration files |
| Azure Storage / Data Lake | Sample data sources and destinations |

## CI/CD Workflow

The workflow is defined in `.github/workflows/main.yml` and runs when changes are pushed to the `main` branch.

1. **Source control:** Keep ADF pipelines, datasets, and linked services in GitHub.
2. **Validate:** Use ADF Utilities to check resource definitions.
3. **Export:** Generate ARM deployment templates and upload them as a build artifact.
4. **Release:** Download the artifact, authenticate to Azure, and attempt deployment to the configured target Data Factory.

## Repository Structure

| Path | Contents |
| --- | --- |
| `.github/workflows/main.yml` | CI/CD workflow |
| `build/package.json` | ADF Utilities package setup |
| `factory/` | Data Factory definition |
| `pipeline/` | Sample pipelines |
| `dataset/` | Dataset definitions |
| `linkedService/` | Storage connection definitions |
| `publish_config.json` | ADF publishing configuration |

## How to Run

1. Clone the repository and set up your own Azure Data Factory and storage resources.
2. Update the Azure resource IDs, resource group names, and Data Factory names in the workflow file.
3. Configure Azure identity permissions and the required GitHub Actions secrets: `AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, and `AZURE_SUBSCRIPTION_ID`.
4. Review the sample pipelines and their data sources before execution.
5. Push a change to `main`, then check the results under **GitHub Actions**.

**Safety note:** One sample pipeline runs a Delete activity after a successful copy. Use test data only and verify the source and destination settings before running it.

## Workflow Status

Earlier training runs completed both **build** and **release** stages successfully. The [latest visible run](https://github.com/magedbinlaswad/cicd_in_adf/actions/runs/19789313813) failed during Azure authentication/subscription access; the workflow may need updated credentials and configuration before it can be reused.

## Key Learning Outcomes

- Working with ADF pipelines, datasets, and linked services.
- Using GitHub to track data integration resource changes.
- Validating ADF resources and generating ARM templates.
- Understanding build and release stages in a data engineering CI/CD workflow.

---

**Project type:** Professional Training Project  
**Training provider:** Digital Edify Technologies  
**Repository:** https://github.com/magedbinlaswad/cicd_in_adf
