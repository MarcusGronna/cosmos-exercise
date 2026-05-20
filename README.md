# Cosmos DB Lab Project

This is a DotNet 10 console application designed to demonstrate connection to and interaction with an Azure Cosmos DB database using the `Microsoft.Azure.Cosmos` SDK and environment configurations loaded via `dotenv.net`.

## Prerequisites

- .NET 10.0 SDK
- Azure Cosmos DB Account URL and Primary/Secondary Auth Key

## Setup & Configuration

1. **Clone/Open the workspace**
2. **Configure Environment Variables**
   Create a `.env` file in the root of the project with the following keys:
   ```env
   DOCUMENT_ENDPOINT=your_cosmos_db_account_url
   ACCOUNT_KEY=your_cosmos_db_account_key
   ```

## Features Demonstrated

- **Initialization**: Creating and configuring a `CosmosClient` using endpoints and keys loaded from `.env`.
- **Database Operations**: Ensuring a database (`myDatabase`) is created if it does not already exist.
- **Container Operations**: Initializing a container (`myContainer`) with `/id` as the partition key.
- **Item Creation**: Creating and serializing a strongly-typed C# object (`Product`) and storing it in Cosmos DB with printout of the Azure Request Charges (RUs).

## How to Run

Restore packages and run the console application:
```bash
dotnet restore
dotnet run
```