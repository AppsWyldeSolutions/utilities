---
services: ETL, API
platforms: Microsoft Fabric, Power Automate
author: Wylde Solutions Labs
level: 200
---
# ETL data from API into Microsoft Fabric Lakehouse tables bypassing file storage

> This is using Microsoft Fabric - Data Engineering and Data Factory, Web API calls, Power Automate

## Scenario

In order to ingest data from API endpoints of various useful systems into Microsoft Fabric Lakehouse for further manipulations before making it available for reporting in e.g. Power BI, we can bypass storing the intermediate CSV or JSON files in the Lakehouse and go straight to the Lakehouse tables in Delta format.
In the designed Data Solution the Lakehouse tables will serve as a Direct Lake source for reporting consumption.

There's two options that will be presented in this article in dealing with API - direct API call where available, e.g. we call a Web method of an endpoint and the data is returned in CSV format or JSON format, and setting up a scheduled file import via email using Power Automate as an API gateway where direct API to the relevant system is not available for some reason.
