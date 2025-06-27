# Data Repositories, Data Pipelines, and Data Integration Platforms

## RDBMS (Relational Database Management Systems)
A relational database is a collection of data organized into a table structure, where the tables can be linked, or related, based on data common to each.

---
## NoSQL(not only SQL)
Is a non-relational database design that provides flexible schemas for the storage and retrieval of data.

### 1. Key-Value Store
- Stores data as key-value pairs
- Simple and fast
- **Examples:** Redis, DynamoDB

```json
{ "user123": "John Doe" }
```


### 2. Document Store
- Stores structured documents (JSON, BSON)
- Flexible and queryable
- **Examples:** MongoDB, CouchDB

```json
{
  "id": "user123",
  "name": "John Doe",
  "email": "john@example.com"
}
```


### 3. Column-Family Store
- Data stored in rows and columns (wide tables)
- Great for large-scale analytics
- **Examples:** Cassandra, HBase

```
RowKey: user123
-------------------------
| name     | email             |
| John Doe | john@example.com  |
```


### 4. Graph Database
- Data as nodes and relationships
- Ideal for connected data
- **Examples:** Neo4j, Amazon Neptune

---
## Data Warehouses, Data Marts, and Data Lakes
A single source of truth that stores data that has been cleansed, conformed and categorized.

### Data Warehouse:
A Data Warehouse has a 3-tier architecture:
1. Database Servers (extracting data from different sources)
2. OLAP Server (process and analyze information coming from database servers)
3. Client Front-End Layer (querying, reporting, and analyzing data)

Examples:
Oracle exadata, IBM Db2, Google BigQuery, Amazon Redshift, Snowflake

### Data Marts:
A data mart is a sub-section of the data warehouse, built specifically for a particular business function, purpose, or community of users.

There are 3 types of Data Marts:
1. Dependent Data Marts offer analytical capabilities for a restricted area of a
Data Warehouse.
2. Independent Data Marts are created from sources other than an Enterprise Data Warehouse, such as Internal Operational Systems or External Data.
3. Hybrid Data Marts combine inputs from Data Warehouses, Operational Systems, and External Systems.

#### 📊 Data Warehouse vs. Data Mart

- **Data Warehouse** = All of a company's data, stored in a centralized system  
- 🗂️ **Data Mart** = A subset of the data warehouse, filtered for a specific purpose or department

### Data Lakes:
Store large amounts of structured, semi-structured, and unstructured data in their native format.
Data can be loaded without defining the structure and schema of data

#### 🏢 Data Warehouse vs. 🏞️ Data Lake

- **Data Warehouse** = Structured, processed data for reporting and analytics  
- **Data Lake** = Raw, unstructured or semi-structured data stored for flexibility and future use

---
## ETL, ELT, and Data Pipelines

### Extract - Extraction can be through:
- Batch processing-large chunks of data moved from source to destination at scheduled intervals
- Stream processing-data pulled in real-time from source, transformed in transit, and loaded into data repository
### Load - Loading is the transportation of processed data in to a data repository. It can be:
- Initial loading-populating all of the data in the repository
- Incremental loading-applying updates and modifications periodically
- Full refresh-erasing a data table and reloading fresh data

Extract, Load, and Transform Process:
* The data is extracted and loaded in a Data Repository than move in a Data Lake or Data Warehouse

ELT is more suited to work with Big Data

---
Data Integration Platforms
