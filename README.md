# Copy data from Azure Blob Storage to Azure SQL Database

This template creates a data factory of version 2 with a pipeline that copies data from a folder in an Azure Blob Storage to a table in an Azure SQL database. 

Here are a few important points about the template: 

- The prerequisites for this template are mentioned in the [Quickstart: Create a data factory by using Azure PowerShell](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#prerequisites) article.


When you deploy this Azure Resource Manager template, a data factory of version 2 is created with the following entities: 

- Azure Storage linked service
- Azure SQL Database linked service
- Azure Blob input datasets
- Azure SQL Datbase output dataset
- Pipeline with a copy activity


The following sections provide steps for running and monitoring the pipeline. For more information, see [Quickstart: Create a data factory by using Azure PowerShell](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-powershell).

## Run and monitor the pipeline
After you deploy the template, to run and monitor the pipeline, do the following steps: 

1. Download [runmonitor.ps1](https://github.com/Azure/azure-quickstart-templates/tree/master/101-data-factory-v2-blob-to-sql-copy/scripts) to a folder on your machine.
2. Launch Azure PowerShell.
3.  Run the following command to log in to Azure. 

	```powershell
	Login-AzureRmAccount
	```
4. Switch to the folder where you copied the script file. 
5. Run the following command to log in to Azure after specifying the names of your Azure resource group and the data factory. 

	```powershell
	.\runmonitor.ps1 -resourceGroupName "<name of your resource group>" -DataFactoryName "<name of your data factory>"
	```



