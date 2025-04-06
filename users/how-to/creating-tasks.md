---
layout: default
title: creating-tasks
parent: how-to
grand_parent: users
nav_order: 1
---

# Configuring Data Feeds

## Overview

This guide covers configuration for a new Data Feed.
Follow and setup standard settings for processing source data.

## Quick Tab Reference

* [**Details**](#details-tab) - Identification information.
* [**Settings**](#settings-tab) - File type, delimiters, and parsing configuration.
* [**Columns**](#columns-tab) - Field mapping and data type definitions.
* [**Preprocessor**](#preprocessor-tab) - Text manipulation before parsing.
* [**Parameters**](#parameters-tab) - Variable definitions for use across configurations.
* [**Validation**](#validation-tab) - Data validation rules for flagging errors.
* [**Post Execution**](#post-execution-tab) - Tasks to run after processing.

Standard configurations typically only require the **Details**, **Settings**,
and **Columns** tabs. More complex setups might involve additional tabs,
such as **Advanced** or **Mapping**, which are beyond this guide's scope.

## Prerequisites

Ensure you have:

* AutoRek V6 account credentials.
* Permission to create and configure Data Feeds.
* A sample data file.

## Accessing Data Feeds

Access the Data Feed Editor from the Data Feeds List page:

![Data Feeds List](/assets/images/dashboard/common-process-csv.png)

* Click the *Add* button to create a new Data Feed.
* Select an existing Data Feed from the list to view or edit it.

Once you have opened a new or selected an existing Data Feed, the
configuration process follows these main stages:

![Data Feed Configuration Flow](/assets/images/dashboard/data-flow-diagram.png)

## Configuration Steps (Tabs)

Data Feed configuration covers several tabs.

### Details Tab

Capture identifying information for the Data Feed.

![Details Tab](/assets/images/dashboard/details-tab.png)

* **Data feed name:** Assign a clear, descriptive name.
* **Summary:** Briefly describe the feed's purpose.

**Next Steps:** Proceed to the Settings tab.

### Settings Tab

Define how the file is read and parsed here.

![Settings Tab](/assets/images/dashboard/settings-tab.png)

* **Import sample file:** Use the *Choose File* button to upload your
  representative sample file.
* **File pattern:** Define the naming convention in the *File pattern* field
  (e.g., `*.csv`).
* **Input/Error/Output directory:** Specify file paths if applicable.
* **Encoding:** Click the *Encoding* dropdown.
  Select the correct file encoding (e.g., UTF-8).
* **File Type:** Ensure `Delimited` is selected.
* **Delimiters:** In the *Delimiters* section:
  * Select `Comma` for standard CSV.
  * Verify the **`Row delimiter`** dropdown matches your file's line
    endings (e.g., `[CR][LF]` for Windows).
  * Check the **`Column headers`** box if your first row contains headers.
  * Set the **`Header rows`** count accordingly.
  * Verify the **`Date format`** dropdown matches your data.
* **Parse Settings From File:** Use after uploading a file to populate.
* **Preview content:** Review this area.
  Confirm that the settings are parsing the sample correctly.

**Next Steps:** Define your data structure in the Columns tab.

### Columns Tab

Define the structure and data types for source file columns.

![Columns Tab](/assets/images/dashboard/columns-tab.png)

* **Auto-Generate Columns:** Use after configuring the Settings Tab and
  parsing a sample file.
* **Column Name and Data Type:** Review the generated values for each column.
  Adjust as needed.
* **Key checkbox:** Mark columns that form a unique record identifier.
* **Add/Delete buttons:** Manually adjust columns if auto-generation is incorrect.

**Next Steps:** Our main tabs are complete. You can now:

* Proceed to the Preprocessor tab.
* Skip to the Validation tab.
* Go directly to the Post Execution tab.

### Preprocessor Tab

Manipulate raw data text (e.g., find/replace) *before* parsing.

![Preprocessor Tab](/assets/images/dashboard/preprocessor-tab.png)

* **Add Preprocessing Rule:** Define text manipulation rules to apply to the
  raw input before parsing.

**Next Steps:** Proceed to the Parameters tab.

### Parameters Tab

Define parameters for use in later configuration steps.

![Parameters Tab](/assets/images/dashboard/parameters-tab.png)

* **Add Parameter:** Create named values referenced throughout the
  configuration.

**Next Steps:** Proceed to the Validation tab.

### Validation Tab

Define validation rules after parsing for flagging errors or warnings.

![Validation Tab](/assets/images/dashboard/validation-tab.png)

* **Add Validation Rule:** Create rules to flag issues.

**Next Steps:** Move to the Post Execution tab.

### Post Execution Tab

Configure tasks to run after data feed processing completes (e.g., triggering
another process).

![Post Execution Tab](/assets/images/dashboard/post-execution-tab.png)

* **Add Post Execution Task:** Define processes to run automatically after the
  data feed completes.

**Next Steps:** Review your settings, then *save* your Data Feed.

## Final Steps

Once you have completed the configuration:

1. **Run the Data Feed:** From the Data Feeds List, select your feed
   and click *Execute*.
2. **Monitor Progress:** The system will display a progress indicator while processing.
3. **Review Results:** After processing completes, check the results
   for any warnings or errors.
4. **View Imported Data:** Navigate to your imported data.

For troubleshooting assistance, refer to the system logs or contact your system administrator.
