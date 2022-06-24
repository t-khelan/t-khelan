---
title: Change Log for Mongo
description: Notifies our customers of any minor/medium updates that were pushed
ms.service: cosmos-db
ms.subservice: cosmosdb-mongo
ms.topic: 
ms.date: 06/22/2022
author: t-khelan
ms.author: t-khelanmodi
---

## Pre-requisites

To look into your Cosmos DB account, you must:
* Have your [Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/create-mongodb-python) ready 
* You can get started in [.NET](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/create-mongodb-dotnet), [Java](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/create-mongodb-java), [Node.js](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/quickstart-javascript), [Golang](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/create-mongodb-go)

## CosmosDB's API for MongoDB updates

### Azure Data Studio MongoDB extension for Azure Cosmos DB
You can now use the free and lightweight tool feature, Azure Data Studio MongoDB extension for Azure Cosmos DB, to manage and query your MongoDB resources using mongo shell. This feature allows you to manage multiple account all in one view by connecting your Mongo resources, configuring the database settings, and performing create, read, update, and delete (CRUD) across Windows, macOS, and Linux. 

[Learn more](https://aka.ms/cosmosdb-ads)


### Continuous backup enhancements in Azure Cosmos DB
Take advantage of new data backup and restore options available with your Azure Cosmos DB account. Continuous backup and point-in-time restore are valuable features that allow you to use Azure Cosmos DB Core (SQL) API, API for MongoDB, Gremlin API, or Table API to recover from accidental data changes and restore the data in your database. The two continuous backup options free continuous backup with seven-day data retention or paid continuous backup with 30-day data retention. The free continuous backup option is a recommended replacement for accounts currently using periodic backup.

[Learn more](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-introduction)

### Linux emulator with Azure Cosmos DB API for MongoDB 
The Azure Cosmos DB Linux emulator with API for MongoDB support provides a local environment that emulates the Azure Cosmos DB service for development purposes on Linux and macOS. Using the emulator, you can develop and test your MongoDB applications locally, without creating an Azure subscription or incurring any costs. When you are satisfied with how your application is working in the Azure Cosmos DB emulator, you can switch to using an Azure Cosmos DB account in the cloud.

[Learn more](https://aka.ms/linux-emulator-mongo)


### 16MB limit per document in API for MongoDB
The 16MB document limit in the Azure Cosmos DB API for MongoDB provides developers the flexibility to store more data per document. With the new limit, you don’t have to worry about hitting the previous 2MB limit. You have the flexibility to create new applications that store larger documents. You also have the flexibility to migrate apps that already use larger documents. This ease-of-use feature will speed up your development process in these cases. 

[Learn more](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb/mongodb-introduction)


### Azure Cosmos DB API for MongoDB data plane RBAC
The API for MongoDB now offers a built-in role-based access control (RBAC) that allows you to authorize your data requests with a fine-grained, role-based permission model. Users and roles residing within your database and can be managed using the Azure CLI, Azure PowerShell, or Azure Resource Manager. With this feature, you can audit each of the user’s actions via the Azure Cosmos DB diagnostic logs. Using this role-based access control (RBAC) allows you access with more options for control, security, and auditability of your database account data.

[Learn more](https://docs.microsoft.com/azure/cosmos-db/mongodb/how-to-setup-rbac)


### Unique partial indexes in Azure Cosmos DB API for MongoDB
The unique partial indexes feature allows you more flexibility to specify exactly which fields in which documents you’d like to index, all while enforcing uniqueness of that field’s value. This feature is used by specifying a partialFilterExpression when creating the index along with a 'unique' constraint in your Azure Cosmos DB API for MongoDB index. This results in the unique constraint being applied only to the documents that meet the specified filter expression. 

[Learn more](https://docs.microsoft.com/azure/cosmos-db/mongodb/feature-support-42)


### Azure Cosmos DB API for MongoDB unique index re-indexing
The unique index feature for Azure Cosmos DB allows you to create unique indexes when your collection was empty and did not contain documents. This feature provides you with more flexibility by giving you the ability to create unique indexes whenever you want to—meaning there’s no need to plan unique indexes ahead of time before inserting any data into the collection. 

[Learn more](https://docs.microsoft.com/azure/cosmos-db/mongodb/mongodb-indexing#unique-indexes) and enable the feature today by [submitting a support ticket request](https://azure.microsoft.com/support/create-ticket/)


### Azure Cosmos DB API for MongoDB supports version 4.2
The Azure Cosmos DB API for MongoDB version 4.2 includes new aggregation functionality and improved security features such as client-side field encryption. These features help you accelerate development by leveraging the new functionality instead of developing it yourself. The Azure Cosmos DB API for MongoDB 4.2 can be enabled in the Azure Portal with any new or existing database account in seconds, with zero downtime. 

[Learn more](https://docs.microsoft.com/azure/cosmos-db/mongodb/feature-support-42)


### Support $expr in Mongo 3.6 and 4.0.
We have added support for both in memory and backend. Additionally, we have the infrastructure to support compute only query operators. This allows us to support 3.6 style $lookup. 
`$expr` allows the use of [aggregation expressions](https://www.mongodb.com/docs/manual/meta/aggregation-quick-reference/#std-label-aggregation-expressions) within the query language. 
`$expr` can build query expressions that compare fields from the same document in a `$match` stage.  
<!-- There are future improvement available including more push down, point lookup, and _id/shard key constraints. -->

<!-- ### Expose Mongo native userId in diagnostic logs
Reach out to Ashwini for this  -->

###  RBAC for $merge stage
Added Role-Based Access Control for `$merge` stage. 

### Add Hyperbolic trigonometric operators
`$cosh` returns the hyberbolic cosine of a value that is measured in radians. `$cosh` takes any valid expression that resolves to a number measured in radians. By default `$cosh` returns values as a double. 

<!-- ### Use federation host name for RoutingGatewayConfiguration calls
Reach out to Dmitri  -->

### Bump packages and .NET TargetRuntime versions
* Bumped more packages and removed VersionOverrides under Compute, Mongo and CLuB. 
* Migrated more projects to `.NET` 6.0
* We removed references to the CBT Symbol Indexing package. Symbol indexing is performed by CloudBuild that requires pushing to `symweb` which is no longer supported. 


## Next steps

- Learn how to [use Studio 3T](connect-using-mongochef.md) with Azure Cosmos DB API for MongoDB.
- Learn how to [use Robo 3T](connect-using-robomongo.md) with Azure Cosmos DB API for MongoDB.
- Explore MongoDB [samples](nodejs-console-app.md) with Azure Cosmos DB API for MongoDB.
- Trying to do capacity planning for a migration to Azure Cosmos DB? You can use information about your existing database cluster for capacity planning.
    - If all you know is the number of vCores and servers in your existing database cluster, read about [estimating request units using vCores or vCPUs](../convert-vcore-to-request-unit.md). 
    - If you know typical request rates for your current database workload, read about [estimating request units using Azure Cosmos DB capacity planner](estimate-ru-capacity-planner.md).
