<a name='assembly'></a>
# BlitzkriegSoftware.PgSql

## Contents

- [PgSqlHelper](#T-BlitzkriegSoftware-PgSql-PgSqlHelper 'BlitzkriegSoftware.PgSql.PgSqlHelper')
  - [Timeout_Default](#F-BlitzkriegSoftware-PgSql-PgSqlHelper-Timeout_Default 'BlitzkriegSoftware.PgSql.PgSqlHelper.Timeout_Default')
  - [CleanParameters(parameters)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-CleanParameters-System-Collections-Generic-List{Npgsql-NpgsqlParameter}- 'BlitzkriegSoftware.PgSql.PgSqlHelper.CleanParameters(System.Collections.Generic.List{Npgsql.NpgsqlParameter})')
  - [ExecuteSqlWithParametersNoReturn(connectionString,SQL,parameters,TimeOut)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersNoReturn-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32- 'BlitzkriegSoftware.PgSql.PgSqlHelper.ExecuteSqlWithParametersNoReturn(System.String,System.String,System.Collections.Generic.List{Npgsql.NpgsqlParameter},System.Int32)')
  - [ExecuteSqlWithParametersToDataTable(connectionString,SQL,parameters,TimeOut)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersToDataTable-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32- 'BlitzkriegSoftware.PgSql.PgSqlHelper.ExecuteSqlWithParametersToDataTable(System.String,System.String,System.Collections.Generic.List{Npgsql.NpgsqlParameter},System.Int32)')
  - [ExecuteSqlWithParametersToScaler\`\`1(connectionString,SQL,parameters,TimeOut)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersToScaler``1-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32- 'BlitzkriegSoftware.PgSql.PgSqlHelper.ExecuteSqlWithParametersToScaler``1(System.String,System.String,System.Collections.Generic.List{Npgsql.NpgsqlParameter},System.Int32)')
  - [FixSqlInText(inText,defaultValue,textDelimiter)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-FixSqlInText-System-String,System-String,System-Char- 'BlitzkriegSoftware.PgSql.PgSqlHelper.FixSqlInText(System.String,System.String,System.Char)')
  - [HasRows(dt)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-HasRows-System-Data-DataTable- 'BlitzkriegSoftware.PgSql.PgSqlHelper.HasRows(System.Data.DataTable)')
  - [HasTables(ds)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-HasTables-System-Data-DataSet- 'BlitzkriegSoftware.PgSql.PgSqlHelper.HasTables(System.Data.DataSet)')
  - [ParameterBuilder(name,dbType,value)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-ParameterBuilder-System-String,System-Data-SqlDbType,System-Object- 'BlitzkriegSoftware.PgSql.PgSqlHelper.ParameterBuilder(System.String,System.Data.SqlDbType,System.Object)')
  - [SqlTextClean(inText)](#M-BlitzkriegSoftware-PgSql-PgSqlHelper-SqlTextClean-System-String- 'BlitzkriegSoftware.PgSql.PgSqlHelper.SqlTextClean(System.String)')

<a name='T-BlitzkriegSoftware-PgSql-PgSqlHelper'></a>
## PgSqlHelper `type`

##### Namespace

BlitzkriegSoftware.PgSql

##### Summary

ADO.NET Helper for PostgreSQL

Uses: `Npgsql` NuGet Package

<a name='F-BlitzkriegSoftware-PgSql-PgSqlHelper-Timeout_Default'></a>
### Timeout_Default `constants`

##### Summary

Default Timeout (seconds)

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-CleanParameters-System-Collections-Generic-List{Npgsql-NpgsqlParameter}-'></a>
### CleanParameters(parameters) `method`

##### Summary

Clean a list of SQL Parameters to fix up strings by calling  for each parameter that is 
NText, NVarChar, Test, VarChar.

##### Returns



##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| parameters | [System.Collections.Generic.List{Npgsql.NpgsqlParameter}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{Npgsql.NpgsqlParameter}') | Parameters to clean |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersNoReturn-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32-'></a>
### ExecuteSqlWithParametersNoReturn(connectionString,SQL,parameters,TimeOut) `method`

##### Summary

Execute SQL with parameters with no return of data or values

##### Returns

Rows affected

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| connectionString | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Connection String |
| SQL | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | SQL Statement |
| parameters | [System.Collections.Generic.List{Npgsql.NpgsqlParameter}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{Npgsql.NpgsqlParameter}') | Parameters |
| TimeOut | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | Timeout in seconds, with default |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersToDataTable-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32-'></a>
### ExecuteSqlWithParametersToDataTable(connectionString,SQL,parameters,TimeOut) `method`

##### Summary

Execute SQL with parameters with a DataTable return

##### Returns

DataTable

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| connectionString | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Connection String |
| SQL | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | SQL Statement |
| parameters | [System.Collections.Generic.List{Npgsql.NpgsqlParameter}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{Npgsql.NpgsqlParameter}') | Parameters |
| TimeOut | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | Timeout in seconds, with default |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-ExecuteSqlWithParametersToScaler``1-System-String,System-String,System-Collections-Generic-List{Npgsql-NpgsqlParameter},System-Int32-'></a>
### ExecuteSqlWithParametersToScaler\`\`1(connectionString,SQL,parameters,TimeOut) `method`

##### Summary

Execute a parameterized SQL statement with a single value return

##### Returns

T

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| connectionString | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Connection String |
| SQL | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') |  |
| parameters | [System.Collections.Generic.List{Npgsql.NpgsqlParameter}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{Npgsql.NpgsqlParameter}') |  |
| TimeOut | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') |  |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| T | Type |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-FixSqlInText-System-String,System-String,System-Char-'></a>
### FixSqlInText(inText,defaultValue,textDelimiter) `method`

##### Summary

Fixes comma separated lists to be quoted correctly and removes last list delimiter for SQL 'IN' clauses

##### Returns

fixed up list

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| inText | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | text to process |
| defaultValue | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | default value (can be empty) |
| textDelimiter | [System.Char](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Char 'System.Char') | delimiter to wrap around each item |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-HasRows-System-Data-DataTable-'></a>
### HasRows(dt) `method`

##### Summary

Does data table have rows?

##### Returns

true if so

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| dt | [System.Data.DataTable](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Data.DataTable 'System.Data.DataTable') | DataTable |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-HasTables-System-Data-DataSet-'></a>
### HasTables(ds) `method`

##### Summary

Does data set have any tables?

##### Returns

true if so

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| ds | [System.Data.DataSet](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Data.DataSet 'System.Data.DataSet') | DataSet |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-ParameterBuilder-System-String,System-Data-SqlDbType,System-Object-'></a>
### ParameterBuilder(name,dbType,value) `method`

##### Summary

Parameter Builder

##### Returns

NpgsqlParameter

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Name, please include (at) |
| dbType | [System.Data.SqlDbType](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Data.SqlDbType 'System.Data.SqlDbType') | Type |
| value | [System.Object](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Object 'System.Object') | Values |

<a name='M-BlitzkriegSoftware-PgSql-PgSqlHelper-SqlTextClean-System-String-'></a>
### SqlTextClean(inText) `method`

##### Summary

Encodes apostrophe to two apostrophe keeping SQL statements from bombing

##### Returns

Clean text

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| inText | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Text to clean |
