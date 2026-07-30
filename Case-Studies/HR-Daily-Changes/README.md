# HR Daily Changes Automation

## Project Summary

| **Category**             | **Details**                                                 |
| ------------------------ | ----------------------------------------------------------- |
| **Project Type**         | Production Process Automation                               |
| **Role**                 | Sole Developer                                              |
| **Primary Technologies** | SQL Server, T-SQL, Power Automate, Excel                    |
| **Business Area**        | Human Resources / IT Operations                             |
| **Status**               | Production                                                  |
| **Primary Outcome**      | Automated daily HR change detection and notification system |

---

## Skills Demonstrated

* SQL Server Development
* Process Automation
* Power Automate
* Data Integration
* Change Detection
* Business Process Analysis
* Operational Reporting
* Data Validation
* Workflow Design
* Systems Integration

---

## Overview

The HR Daily Changes Automation project replaced a manual process for identifying and communicating employee profile changes with an automated monitoring and notification system.

The solution detects meaningful changes across multiple HR data sources each day, consolidates those changes into a standardized format, and automatically delivers a clear, organized summary through Power Automate.

The result is a reliable operational workflow that ensures important personnel changes are communicated consistently without requiring manual review of multiple systems.

---

## Business Problem

Human Resources maintains information across several independent data areas, including certifications, licenses, registrations, education, and personnel records.

Before this project, identifying recent changes required manually reviewing multiple datasets and determining which updates were important enough to communicate. This process was time-consuming, repetitive, and increased the possibility of overlooking important changes.

The organization needed a dependable process that would automatically identify daily changes and present them in a format that was easy to review and act upon.

---

## Objectives

The project was designed to:

* Automatically detect meaningful HR data changes each day.
* Consolidate changes from multiple HR data sources.
* Produce a single, easy-to-read daily report.
* Eliminate manual review of multiple tables.
* Improve consistency and reliability of operational communication.
* Deliver notifications only when meaningful changes occurred.

---

## Technical Challenges

Several engineering challenges were addressed during development.

### Consolidating Multiple Data Sources

Employee information existed across several independent tables representing different business functions. The solution needed to combine these sources into a unified reporting process while preserving the context of each change.

### Detecting Daily Changes

Rather than reporting all records, the system needed to identify only changes that occurred during the current reporting period. This required consistent change tracking across multiple datasets.

### Readable Communication

Simply exporting database records would have produced a difficult-to-read report. The notification process was designed to group changes by employee and organize related updates into logical sections, making the final email useful for operational staff rather than simply technically correct.

### Data Quality

The solution needed to handle missing values, inconsistent date formats, and different field structures gracefully while maintaining a professional presentation.

### Noise Reduction

An important design objective was to avoid unnecessary notifications. If no meaningful changes were detected, the automation quietly completed without sending an email.

---

## Solution Architecture

```text
HR Source Tables
(Certifications, Licenses,
Registrations, Education,
Personnel)
          │
          ▼
Daily Change Detection
          │
          ▼
Unified Change View
          │
          ▼
Power Automate
          │
          ▼
Formatted Daily Email
          │
          ▼
HR / IT Staff
```

The architecture separates data collection, change detection, formatting, and notification into distinct stages. This modular approach simplifies maintenance while allowing each component to evolve independently.

---

## Implementation

The solution was built using SQL Server and Microsoft Power Automate.

Key implementation features included:

* Daily comparison of multiple HR data sources.
* Consolidated SQL views for standardized reporting.
* Grouping changes by employee.
* Categorization by change type.
* Automatic formatting of dates and null values.
* Conditional notification logic that suppresses unnecessary emails.
* Clear presentation designed for operational users rather than database administrators.

Development involved multiple iterations to improve readability, simplify maintenance, and ensure that the final notification contained only meaningful information.

---

## Engineering Decisions

Several design choices significantly improved the quality and maintainability of the solution.

### User-Centered Reporting

Rather than simply exposing raw database changes, the notification was designed around how HR and IT staff consume information. Grouping updates by employee and organizing them by change type dramatically improved readability.

### Modular Data Processing

The change detection logic, consolidated reporting view, and notification workflow were developed as separate components. This separation made testing easier and allows future enhancements without redesigning the entire solution.

### Meaningful Notifications

Avoiding unnecessary communication was considered just as important as reporting actual changes. The automation intentionally suppresses email delivery when no qualifying changes are detected, reducing notification fatigue.

### Standardized Output

Careful handling of dates, null values, and formatting ensures that reports remain consistent regardless of the underlying data.

---

## Results

The completed solution delivered several operational improvements.

* Eliminated manual review of multiple HR datasets.
* Automated daily identification of employee profile changes.
* Reduced repetitive administrative work.
* Improved consistency of operational reporting.
* Increased confidence that important personnel updates would not be overlooked.
* Delivered clear, organized notifications that are easy for staff to review.
* Created a scalable framework that can accommodate additional change categories in the future.

---

## Lessons Learned

This project reinforced the importance of designing automation around the people who use it rather than around the underlying database structure.

Reliable automation is not simply about detecting changes—it is about presenting those changes in a way that supports better decision-making while minimizing unnecessary work.

The project also demonstrated the value of iterative refinement. Small improvements in formatting, grouping, filtering, and notification logic collectively transformed a simple reporting process into a dependable operational tool.

---

## Technologies Used

* Microsoft SQL Server
* T-SQL
* SQL Views
* Power Automate
* Excel
* Data Integration
* Workflow Automation
* Operational Reporting
* Change Detection
* Process Automation
