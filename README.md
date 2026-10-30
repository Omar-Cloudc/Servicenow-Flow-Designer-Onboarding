Servicenow-Flow-Designer-Onboarding
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
![Catalog Item & Variables](screenshots/catalog-item-variables-list.png)

### Catalog Variables List - 5 Fields Configured
![Variables List](screenshots/catalog-new-employee-onboarding.png)

### Workflow Studio - New Flow Creation
![Workflow Studio](screenshots/workflow-studio-employee-onboarding-flow-creation.png)

### Flow Action - Create Catalog Task
![Create Task](screenshots/flow-action-create-catalog-task-facilities-setup.png)

### Full Flow Logic - Approval and Tasks
![Full Flow](screenshots/flow-full-approval-tasks-logic.png)

### Output - RITM and Catalog Tasks Proof
![RITM Output](screenshots/ritm0010001-requested-item-tasks-output-proof.png)

-------

### Key Learning:
- Service Catalog Variable Configuration
- Flow Designer - Approval & If Conditions
- Automated Catalog Task Creation 

