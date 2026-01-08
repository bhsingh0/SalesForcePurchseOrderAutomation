# Salesforce Purchase Order Automation

## Overview
This project demonstrates an **end-to-end automation of the Purchase Order (PO) process** in Salesforce, including **record-triggered flows, manager approvals, reports & dashboards, and metadata-driven deployment using Salesforce CLI and Git**.  

The project is designed to **reduce manual work, improve approval speed, and provide real-time visibility** for managers and stakeholders. It showcases the integration of **CRM automation with Agile project delivery principles**.

---

## Features / Components

### 1. Custom Objects : Refer Objects folder
- **Purchase_Order__c**  
  - Fields: `Status__c`, `Requested_By__c`, `PO_Amount__c`, `Approval_Comments__c`, etc.
  - Tracks individual purchase orders through the approval lifecycle.

### 2. Record-Triggered Flow: Refer flow folder
- Automatically updates PO status when a new PO is created or updated.
- Flow logic:  
  `Submitted → Pending Approval → Approved / Rejected`
- Reduces manual updates and ensures consistency.

### 3. Manager Approval Process
- Conditional routing based on PO amount or department.
- Ensures approvals are **tracked, timely, and accountable**.
- Sends notifications to relevant stakeholders.

### 4. Reports & Dashboards
- Provides real-time insights into:
  - Pending approvals
  - Total POs by status
  - Financial exposure
- Supports **data-driven decision making**.

### 5. Metadata-Driven Deployment
- Project organized using **Salesforce DX structure**.
- Deployable via **Salesforce CLI (`sf project deploy`)**.
- Version-controlled in Git for **repeatable, UI-free deployments** across environments.

---

## Installation / Deployment
```bash
1. Clone the repository
git clone <your-repo-url>
cd PO_POC

2. Authorize your Salesforce Org
sf login org --web

3. Deploy metadata to your org
sf project deploy start --source-dir force-app/main/default --target-org MyPOOrg

4. Verify objects, flows, and approval processes in Salesforce UI.


