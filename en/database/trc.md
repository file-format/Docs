{
  "date": "2021-08-24",
  "keywords": [
    "trc file",
    "trc file format",
    "what is a trc file",
    "file",
    "trc example",
    "trc file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about TRC file format and APIs that can create and open TRC files.",
  "title": "TRC - SQL Server Trace File",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-trc"
    }
  },
  "lastmod": "2021-08-24"
}

## What is a TRC file?
A file with .trc extension contains the trace results of the activity of a Miscrosoft SQL server database. These files are created by a software SQL Server Profiler; usually packaged with Microsoft SQL Server software. The database administrators can analyze a sequence of database statements and can review the trace log if some kind of errors or warnings are suspected. These files are usually located in the typical LOG folder of MSSQL inside the Program Files directory on a Windows operating system.

## TRC file format
The TRC file format is used by SQL Server Profiler to automatically generate a new trace of the recently executed statements by MS SQL server. The SQL Server Profiler uses the default template for any new trace. However, the software includes several predefined templates for monitoring certain types of events. Also SQL Server Profiler can be used to create templates that define the event classes and data columns to include in traces.

### Predefined Templates
Here is the list of some predefined templates included in SQL Server Profiler:
- **SP_Counts**: Captures stored procedure execution behavior over time.
- **Standard**: Generic starting point for creating a trace.
- **TSQL**: Captures all Transact-SQL statements that are submitted to SQL Server by clients and the time issued.
- **TSQL_Duration**: Captures all Transact-SQL statements submitted to SQL Server by clients, their execution time, and groups them by duration. 
- **TSQL_Grouped**: Use to investigate queries from a particular client or user.
- **TSQL_Locks**: Use to troubleshoot deadlocks, lock time-out, and lock escalation events.
- **TSQL_Replay**: Use to perform iterative tuning, such as benchmark testing.
- **TSQL_SPs**: Use to analyze the component steps of stored procedures.
- **Tuning**: Use to produce trace output that Database Engine Tuning Advisor can use as a workload to tune databases.
### Correlate a trace with Windows Performance Log data
The SQL Server Profiler can be used to open a Microsoft Windows performance log, to choose the counters to correlate with a trace, and display the selected performance counters alongside the trace in the MS SQL Server Profiler GUI. To indicate the performance log data that correlates with the selected trace event, a vertical red bar in the System Monitor data window pane of SQL Server Profiler. 


## References ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)
