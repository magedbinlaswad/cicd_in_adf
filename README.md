Azure Data Factory CI/CD Automation
Hands-on Azure Data Engineering Training Project | Digital Edify Technologies
Project Overview
This project demonstrates the fundamentals of Continuous Integration and Continuous Deployment (CI/CD) for Azure Data Factory using GitHub Actions.
Developed as part of my 5-month Azure Data Engineering training, the project focuses on version-controlling Azure Data Factory resources, validating configurations, generating ARM templates, and practicing automated deployment between Azure environments.
Technologies Used
• Azure Data Factory (ADF) – Data pipelines and integration workflows
• GitHub Actions – CI/CD workflow automation
• Azure Resource Manager (ARM) – Deployment templates
• Azure Storage / Data Lake – Sample data integration
• JSON – Pipeline and resource configurations
• ADF Utilities – Resource validation and template generation
Project Implementation
The repository contains sample Azure Data Factory resources and a GitHub Actions workflow.
Key components include:
• Created sample ADF pipelines using Wait, Copy Data, and Delete activities.
• Configured datasets and linked services for Azure Storage and Data Lake connections.
• Used GitHub for version control of Data Factory resources.
• Configured GitHub Actions to validate ADF configurations and export ARM templates.
• Added a deployment stage using Azure authentication and ARM-based deployment.
CI/CD Workflow
The workflow is defined in .github/workflows/main.yml and is triggered by pushes to the main branch.
1. Source Control
ADF resource definitions are maintained in GitHub.
2. Build & Validation
GitHub Actions installs the Azure Data Factory Utilities package, validates the ADF resources, and generates ARM deployment templates.
3. Build Artifacts
The generated ARM templates and parameters are uploaded as GitHub Actions artifacts.
4. Deployment
The release stage uses Azure authentication and the Azure Data Factory deployment action to deploy the generated templates to a configured target environment.
Repository Structure
• .github/workflows/main.yml – GitHub Actions CI/CD configuration
• build/package.json – ADF Utilities package configuration
• factory/ – Data Factory definition
• pipeline/ – Sample ADF pipelines
• dataset/ – Dataset configurations
• linkedService/ – Azure storage connections
• publish_config.json – ADF publishing configuration
Running the Project
To reproduce the project in your own Azure environment:
1. Clone this repository.
2. Prepare the required Azure Data Factory and storage resources.
3. Update the source and target Azure resource references in the workflow.
4. Configure the required GitHub Actions secrets:


AZURE_CLIENT_ID
AZURE_TENANT_ID
AZURE_SUBSCRIPTION_ID
5. Configure the appropriate Azure identity permissions and federated credentials.
6. Review the sample pipelines before execution.
7. Push changes to main and review the results in GitHub Actions.
Note: The sample Copy/Delete pipeline includes a Delete activity after a successful copy. Use test data and verify the source and destination configuration before execution.
Project Status
This repository is a training implementation rather than a production deployment.
The CI/CD workflow has recorded successful build and release runs during training. Later runs also encountered Azure authentication and subscription-access issues, so the configuration may require updates before reuse in another environment.
Key Learning Outcomes
Through this project, I gained practical exposure to:
• Creating and managing Azure Data Factory pipelines
• Configuring datasets and linked services
• Using Git for version control
• Understanding CI/CD workflows in data engineering
• Validating ADF resources and generating ARM templates
• Working with GitHub Actions and Azure deployment configurations
The project helped me understand how source control and deployment automation support more consistent management of data integration workflows.


⸻


Project Type: Professional Training Project
Training Provider: Digital Edify Technologies
Year: 2025
GitHub: https://github.
