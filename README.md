# Log Processing Automation

This automation tool simplifies the process of handling log files by following a set of steps:

## Initialization

The automation tool reads the path of the folder to be processed from the `Config` file located within the automation folder.

## Processing

1. It compiles a list of all files found within the specified folder, excluding files with names starting with "stats-full-orders-received-..."

## Data Extraction

2. The filenames contain timestamps of when the logs were sent. The automation tool extracts these date and time values using regular expressions and inserts this information into the dashboard.

3. The filenames also indicate the type of log (gen, fail, and received) corresponding to total, failed, and successful logs, respectively. This information is extracted using regular expressions.

## Finalization

4. The automation tool updates the dashboard file within the automation folder.

5. In case of failed logs, it sends an email to the recipient specified in the `Config` file.

With this tool, you can streamline the process of processing log files, extracting essential information, and maintaining an up-to-date dashboard.
