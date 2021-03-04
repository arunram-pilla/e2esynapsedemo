## Healthcare CMS Demo using Azure Synapse, Azure Data Factory and Power BI

UPDATE: As of 2/17/2021, a new and updated version of this solution is now available. It includes new 2018 data (now 148M total rows), optimized ADF data flows, a more efficient dimensional design, and a new Power BI report titled 'Medicare Part D Report V2.' More info about these changes is coming soon.

#### Audience
If you belong to one of the below categories, you have landed at the right place!

1. If you are new to Azure Synapse and/or Azure Data Factory or just getting started on them.
2. If you are looking to set up a Data Warehousing environment using Azure Synapse, Azure Data Factory and PowerBI in just four steps.
3. If you are interested in reporting on Centers for Medicare and Medicaid Services (CMS) data with Azure Synapse and PowerBI.
4. If you are interested in testing a combination of PowerShell script and ARM template that deploys multiple Azure Services for an end-to-end solution.
5. If you want to explore a Power BI solution over Azure Synapse that uses a Composite Model with Aggregations and Materialized Views.

#### Purpose
The purpose of this project is to 1) automate the deployment of Azure Resources (Azure Resource Group, Azure Data Lake Storage, Azure Synapse and Azure Data Factory) 2) automate downloading CMS data from https://cms.gov and load into Azure Synapse Tables. This CMS data can then be used for reporting using Power BI.

### Pre-requisites:
Azure Account with permissions to create Azure Resources (Storage, Azure Data Factory, Synapse). A tutorial of deploying the Azure ARM Template is here: https://youtu.be/-YnF2EHzTzs

### 4 Easy Steps to Deployment:
1. Login to Azure Portal and open Cloud Shell from the top navigation bar (see below image). Make sure to select PowerShell prompt.  Alternatively, if you want to use PowerShell from your local machine, <a href="https://github.com/kunal333/E2ESynapseDemo/UsingPowerShellFromLocal.md" title="UsingPowerShellFromLocal">click here</a>.

    ![Command Shell](https://github.com/kunal333/E2ESynapseDemo/images/CommandShell.png)
2. Clone this Git Repository and switch to new directory (using commands below)

    `git clone https://github.com/kunal333/E2ESynapseDemo.git`
    
    `cd E2ESynapseDemo`

    ![Clone Git Repository](https://github.com/kunal333/E2ESynapseDemo/images/CloneGitRepo.png)
3. Start script and provide Resource Group Name and User credentials (See example below. **Note:** Don't use the same names in example!)

    `PS /home/kunal/E2ESynapseDemo> ./deploySynapseStorageADF.ps1`

    `Do you want to use existing resource(s) for this CMS Demo or create everything new from scratch?  Enter 1 for New or 2 for Existing: 1`

    `Enter New Resource Group Name: SynapseDemo1`

    `Enter SQL Server Administrator Name: synapsedemo1server`

    `Enter SQL Server Password: Passw0rd!`

    ![Enter Details](https://github.com/kunal333/E2ESynapseDemo/images/EnterDetails.png)
4. Next step is to get the Power BI tempate and connect to the Synapse instance. A tutorial of deploying the parameterized Power BI Template file is here: https://youtu.be/_mslQZM7NrU

**Note**:If you are using Azure Portal Cloud Shell, you might see errors due to inactivity. Please ignore them as the script would continue to run in the background. Total time for end to end deployment is around 1 hour. 

### Architectures
Documentation for the Medicare Fee-For Service Provider Utilization & Payment Part D Prescriber Data can be found <a href="https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Medicare-Provider-Charge-Data/Downloads/Prescriber_Methods.pdf" title="CMS Documentation">here</a>

All related Architectures for this solution and PowerBI dashboard images can be found <a href="https://github.com/kunal333/E2ESynapseDemo/blob/master/Architectures.md" title="Architectures">here</a>

### Script Explained
Step by step process how the deployment script performs is explained <a href="https://github.com/kunal333/E2ESynapseDemo/blob/master/ScriptExplained.md" title="ScriptExplained">here</a>

### Contributing
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com)
with any additional questions or comments.

### License
Copyright (c) Microsoft Corporation. All rights reserved. Licensed under the MIT License. This project has adopted the Microsoft Open Source Code of Conduct. For more information see the Code of Conduct FAQ or contact opencode@microsoft.com with any additional questions or comments.
