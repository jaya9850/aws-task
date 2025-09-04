The most common **basic Splunk search commands** use simple keywords, fields, Boolean operators, and filtering commands to extract and analyze data from Splunk indexes.[1][2]

## Core Search Syntax

- Use spaces as implied **AND** between search terms:  
  `index="myIndex" error` finds events with "error" in the `myIndex`.[2]

- **Field-value search**:  
  `status=404` filters events where the status is 404.[3]

- **Exact phrases**:  
  `"User Login Failed"` finds the full phrase irrespective of case.[2]

- **Wildcards**:  
  `status=50*` matches any status starting with "50", e.g., 500, 503.[3]

- **Boolean operators**:  
  `error OR warning` for events with either term.[3]
  `error NOT warning` finds "error" but excludes "warning".

## Essential Search Commands

| Command      | Description                                        |
|--------------|----------------------------------------------------|
| `search`     | Filters results to match a search expression[2]|
| `table`      | Displays fields in tabular format[2]           |
| `stats`      | Provides statistics, grouped by fields[2]      |
| `dedup field`| Removes duplicate events for a field[2]        |
| `sort field` | Sorts results by field values[2]               |
| `top field`  | Shows most common values for the field[2]      |
| `head N`     | Returns first N results[2]                     |
| `rex`        | Extracts fields using regex[2]                 |
| `where`      | Advanced filtering using eval expressions[2]   |

## Practical Examples

- Find all error logs in "app_logs":
  ```
  index="app_logs" error
  ```


- Show top 5 URIs with errors:
  ```
  sourcetype=access_combined error | top 5 uri
  ```


- Show HTTP 503 errors:
  ```
  status=503
  ```


- Filter events for a specific host:
  ```
  host="myblog" source="/var/log/syslog" Fatal
  ```


- Table of username and status fields:
  ```
  index="myIndex" | table username, status
  ```


These basics provide a foundation for building more advanced Splunk SPL commands and queries for data analysis.[1][2][3]

[1] https://www.splunk.com/en_us/blog/learn/splunk-cheat-sheet-query-spl-regex-commands.html
[2] https://www.stationx.net/splunk-cheat-sheet/
[3] https://www.youtube.com/watch?v=GWl-TuAAF-k
[4] https://dev.splunk.com/enterprise/docs/devtools/customsearchcommands
[5] https://www.splunk.com/en_us/resources/videos/basic-search-in-splunk-enterprise.html
