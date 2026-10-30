# Servicenow-Flow-Designer-Onboarding
# ServiceNow Employee Onboarding Automation

An automated Service Catalog item and Flow Designer workflow built in ServiceNow to streamline new hire onboarding across IT, HR, OT, and Facilities.

## Overview
This project automates the end-to-end onboarding process when a new employee is requested. It features a custom Service Catalog item, dynamic form variables, manager approval logic, parallel task assignment, and automated email notifications.

---

## Key Components

### 1. Service Catalog Item
* **Name:** Employee Onboarding - New Hire
* **Category:** Onboarding
* **Description:** Onboarding request for new employee - IT, OT & HR access

### 2. Variables Configured
* **Employee Full Name** (Single Line Text - Mandatory)
* **Department** (Select Box - IT, HR, OT, Operations, Finance)
* **Date of Joining** (Date - Mandatory)
* **Hiring Manager** (Reference to `sys_user` table - Mandatory)
* **Work Location** (Select Box - Hyderabad, Bangalore, Remote)

### 3. Flow Designer Workflow
* **Trigger:** Service Catalog Item Submitted (`Employee Onboarding - New Hire`)
* **Approval Step:** Dynamically routes an approval request to the selected **Hiring Manager**.
* **Parallel Tasks (Executed upon Manager Approval):**
  * **Task 1 (IT):** Create Email & Active Directory Account.
  * **Task 2 (OT):** Provision Laptop & OT System Access (tailored to department).
  * **Task 3 (Facilities):** Issue ID Card & Facility Access (tailored to work location).
  * **Task 4 (HR):** Complete HR Documentation.
* **Notification:** Sends an automated completion email to the Hiring Manager.

---

## Screenshots

### Service Catalog Item & Variables
![Catalog Item & Variables](screenshots/variables.png)

### Catalog Variables List - 5 Fields Configured
![Variables List](

### Variable Creation - Sngle 



### Flow Designer Workflow
![Flow Designer](screenshots/flow-designer.png)

### Test Execution & Generated Tasks
![Test Result](screenshots/test-result.png)
