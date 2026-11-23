
# Organizational Charts Automation
### SQL Server | Visio | Power Automate | Change Detection

## Overview

Developed and progressively enhanced a semi-automated organizational chart system supporting more than 500 employees across multiple locations.

The solution combines SQL Server data processing, Microsoft Visio, and Power Automate to simplify chart maintenance, improve visual organization, and automatically identify changes requiring attention.

Rather than attempting to automate every aspect of Visio editing, the system uses SQL to determine what has changed and provides actionable instructions for maintaining accurate, published organizational charts.

## The Challenge

Maintaining organizational charts for a large, geographically distributed organization presents several challenges:

- Employees change positions, supervisors, and locations.
- Organizational charts must reflect current reporting relationships.
- Manually comparing employee records is time-consuming.
- Updates to individual charts can be overlooked.
- Staff need an accessible, reliable version of the current organizational structure.

The original process required substantial manual review and maintenance.

The goal was to reduce repetitive work while preserving the flexibility of Visio for chart design and publication.

## Solution Architecture

The solution evolved into a workflow involving four primary components:

1. **SQL Server:** Retrieves and organizes employee and supervisory information from the HR system.
2. **Microsoft Visio:** Presents reporting relationships using organizational chart shapes and location-based color coding.
3. **SQL Change Detection:** Compares current organizational information against a previous snapshot to identify changes requiring updates.
4. **Power Automate:** Delivers organized notifications describing the changes that need attention.

The resulting workflow combines automated detection with human-reviewed chart maintenance.

## Implementation

### 1. Data-Driven Organizational Charts

SQL Server provides the employee information needed to support organizational chart generation and maintenance.

The underlying data includes employee identifiers, names, job titles, locations, and supervisory relationships.

Using a centralized data source reduces the need to manually assemble employee information and provides a consistent foundation for Visio charts.

### 2. Location-Based Color Coding

The organizational charts were enhanced with location-based color coding.

Employee shapes use colors to distinguish locations, making large charts easier to interpret visually.

This enhancement also introduced an additional maintenance requirement: when an employee's location changes, their chart representation may need to be updated even when their reporting relationship remains unchanged.

### 3. Automated Change Detection

A SQL-based comparison process identifies differences between current organizational information and a previous snapshot.

The logic evaluates changes such as:

- New employees appearing in the organizational structure.
- Employees no longer present in the current structure.
- Supervisor changes requiring organizational chart movement.
- Job title changes requiring shape updates.
- Location changes affecting chart placement or color coding.

These differences are translated into actionable instructions rather than simply presenting raw data changes.

For example, a supervisor change may require moving an employee's shape, while a job title change may only require editing existing text.

The comparison logic also supports situations where multiple attributes change together.

### 4. Automated Update Notifications

Power Automate runs a scheduled process that retrieves outstanding organizational chart changes from SQL Server.

When changes are detected, an email notification provides instructions for updating the charts.

The notification is designed to communicate what action is needed, which employee is affected, and the relevant previous and current information.

The process runs daily and avoids sending routine change emails when no updates are needed.

### 5. Publication and Ongoing Maintenance

The charts remain editable in Visio, allowing organizational changes to be reviewed and applied before publication.

Updated charts are published as PDFs for staff access through Microsoft 365 collaboration tools.

This approach preserves human oversight while automating the repetitive work of identifying and communicating changes.

## Engineering Decisions

### Automate Detection, Not Every Editing Action

Full automation of complex Visio chart editing would introduce additional development and maintenance requirements.

Instead, the solution focuses on reliably detecting changes and providing clear instructions.

This balances automation with maintainability and human review.

### Separate Current Data From Comparison Data

Maintaining a comparison snapshot allows the system to identify meaningful differences rather than repeatedly reviewing the entire organizational structure.

This supports consistent change detection and reduces unnecessary manual effort.

### Make Notifications Actionable

A list of changed database fields is not necessarily useful to someone maintaining an organizational chart.

The solution translates data differences into practical actions such as adding, moving, editing, or removing employee shapes.

### Incorporate Visual Design Into the Data Logic

Location-based color coding is more than a presentation feature.

Because location determines how an employee appears on the chart, location changes must also be considered by the maintenance workflow.

This connects visual design requirements directly to the underlying data processing.

## Results and Impact

The system provides several operational improvements:

- Reduced manual comparison of HR records and organizational charts.
- More consistent identification of staffing and reporting changes.
- Clearer instructions for maintaining Visio diagrams.
- Improved visual readability through location-based color coding.
- Centralized access to published organizational charts.
- A repeatable maintenance workflow supporting more than 500 employees.

The solution continues to support ongoing organizational chart maintenance as staffing and reporting relationships evolve.

## Lessons Learned

**Practical automation does not always mean eliminating every manual step.**

Automating the most repetitive and error-prone portions of a workflow can provide substantial value while retaining human judgment where it is useful.

This project also demonstrates the importance of designing for ongoing maintenance. What began as a way to simplify organizational chart creation evolved into a system for detecting, communicating, and managing organizational changes.

## Technologies Used

- Microsoft SQL Server
- T-SQL
- SQL Views and Stored Procedures
- Microsoft Visio
- Power Automate
- SharePoint / Microsoft Teams

## Engineering Skills Demonstrated

- Data integration and transformation
- Change detection and snapshot comparison
- Business-rule implementation
- Workflow automation
- Data-driven visualization
- Operational process improvement
- Maintainable system design
