# EHR Payroll XML Upload

## Project Summary

| **Category**             | **Details**                                                                |
| ------------------------ | -------------------------------------------------------------------------- |
| **Project Type**         | Enterprise Systems Integration                                             |
| **Role**                 | Solution Developer (SQL Server, XML Generation, Power Apps)                |
| **Collaboration**        | Partnered with Network Administration for Power Automate and SFTP delivery |
| **Primary Technologies** | SQL Server, T-SQL, Power Apps, XML, Power Automate, SFTP                   |
| **Business Area**        | Finance / Payroll                                                          |
| **Status**               | Production                                                                 |
| **Primary Outcome**      | Automated generation and secure delivery of vendor-ready payroll XML files |

---

## Skills Demonstrated

* SQL Server Development
* T-SQL
* XML Generation
* Power Apps
* Systems Integration
* Business Process Automation
* Enterprise Application Integration
* Workflow Design
* Data Validation
* Cross-functional Collaboration

---

## Overview

The EHR Payroll XML Upload project automated the generation of vendor-specific payroll files used for importing payroll information into an external system.

The solution combined SQL Server, XML generation, and a Power App interface to create a streamlined workflow that transformed payroll data into a vendor-compliant XML document. Once generated, the file was placed into a Microsoft Teams folder where an automated Power Automate workflow securely transferred it to the vendor using SFTP.

The result was a dependable end-to-end process that reduced manual effort while improving consistency, accuracy, and confidence in payroll data exchange.

---

## Business Problem

Payroll staff regularly needed to submit payroll information to an external vendor.

The vendor required a very specific XML format, making manual preparation both time-consuming and susceptible to formatting errors. Any mistakes could delay payroll processing and require additional troubleshooting.

The organization needed a reliable solution that would consistently generate vendor-compliant XML while simplifying the overall submission process.

---

## Objectives

The project was designed to:

* Automate creation of vendor-compliant payroll XML files.
* Eliminate manual XML formatting.
* Provide a simple user interface for payroll staff.
* Improve consistency and reliability.
* Support review and validation before transmission.
* Integrate securely with the vendor's file transfer process.

---

## Technical Challenges

Several engineering challenges were addressed during development.

### Vendor-Specific XML Requirements

The payroll vendor required XML documents that followed a strict structure. The solution needed to generate files that precisely matched the required schema without requiring manual editing.

### Business Rule Validation

Payroll information needed to be validated before XML generation to ensure that only accurate and complete information was included in the final file.

### User Accessibility

The process needed to be usable by payroll staff without requiring SQL knowledge. A Power App provided a straightforward interface that allowed users to generate the XML file with minimal technical complexity.

### Secure Integration

The completed XML file needed to move securely from the organization's environment to the external payroll vendor. The overall solution required coordination between database processes, Microsoft technologies, and secure file transfer.

---

## Solution Architecture

```text
Payroll Staff
        │
        ▼
Power App
        │
        ▼
SQL Server
(Stored Procedure)
        │
        ▼
Business Validation
        │
        ▼
Vendor XML Generation
        │
        ▼
XML File
        │
        ▼
Microsoft Teams Folder
        │
        ▼
Power Automate
        │
        ▼
SFTP Transfer
        │
        ▼
Payroll Vendor
```

The architecture separates business logic, user interaction, file generation, and secure delivery into independent components. This modular design simplifies maintenance while allowing each part of the system to evolve independently.

---

## System Components

| **Component**    | **Responsibility**                             |
| ---------------- | ---------------------------------------------- |
| Power App        | User interface for payroll staff               |
| SQL Server       | Business logic and data processing             |
| Stored Procedure | Validation and XML generation                  |
| Microsoft Teams  | Temporary staging location for generated files |
| Power Automate   | Workflow automation                            |
| SFTP             | Secure transmission to external vendor         |

---

## Implementation

The solution centered around SQL Server, where payroll data was validated and transformed into a vendor-compliant XML document.

Payroll staff initiated the process through a Power App, eliminating the need to interact directly with the database. The generated XML file was saved to a Microsoft Teams folder, creating a natural checkpoint where staff could review and validate the file before it was transmitted.

A Power Automate workflow, developed in collaboration with the organization's Network Administrator, monitored the Teams folder and securely transferred approved files to the payroll vendor using SFTP.

This division of responsibilities created a clean separation between business processing and file delivery while allowing each component to be maintained independently.

---

## Engineering Decisions

Several design decisions contributed to the long-term success of the solution.

### Separation of Responsibilities

Business logic, XML generation, user interaction, and secure delivery were intentionally separated into distinct components. This architecture simplified testing, improved maintainability, and allowed each portion of the system to evolve independently.

### Human Validation Checkpoint

Rather than immediately transmitting generated files, the workflow intentionally paused after XML creation by placing the file in a Microsoft Teams folder. This gave payroll staff an opportunity to review and validate the output before transmission.

As confidence in the automated process increased, the review step became less critical for day-to-day operations, but retaining the checkpoint provides an important safeguard when needed.

### Vendor-Compliant Output

The XML was generated in its final vendor-required format, eliminating manual editing and reducing opportunities for formatting errors.

### User-Centered Design

The Power App simplified the process for payroll staff by hiding technical implementation details behind an intuitive interface.

### Collaborative Architecture

The project leveraged the strengths of multiple disciplines. SQL Server handled business rules and XML generation, while the Network Administrator implemented the Power Automate workflow responsible for secure SFTP delivery. This division of responsibilities produced a clean, maintainable enterprise solution.

---

## Results

The completed solution delivered several significant improvements.

* Eliminated manual XML file creation.
* Reduced payroll processing time.
* Improved consistency of vendor submissions.
* Reduced formatting errors.
* Simplified payroll staff workflow.
* Added a built-in review and validation step before transmission.
* Integrated multiple Microsoft technologies into a seamless business process.
* Created a scalable solution that continues to support payroll operations in production.

---

## Lessons Learned

This project reinforced the value of separating complex systems into clearly defined responsibilities.

Rather than building one large solution that handled every task, each component was designed to perform a specific role exceptionally well. This modular architecture improved maintainability while making future enhancements easier to implement.

The project also demonstrated that effective automation does not eliminate human oversight—it supports it. By intentionally including a review point before secure transmission, the solution balanced efficiency with operational confidence, allowing trust in the automation to grow over time.

Finally, the project highlighted the importance of cross-functional collaboration. Combining database development, application design, workflow automation, and secure networking resulted in a solution that was more robust than any single technology could have provided on its own.

---

## Technologies Used

* Microsoft SQL Server
* T-SQL
* XML
* XML Generation
* Power Apps
* Power Automate
* Microsoft Teams
* SFTP
* Systems Integration
* Workflow Automation
* Enterprise Application Development
