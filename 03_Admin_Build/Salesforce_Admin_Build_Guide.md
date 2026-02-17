SECTION 1: SALESFORCE ADMIN BUILD GUIDE

(How to build the system in Salesforce)

Purpose

This guide explains how to configure Salesforce to support a custom apparel business CRM. It covers objects, fields, record types, stages, validation rules, reports, and dashboards.

Step 1: Prepare Your Salesforce Org

Log into a Salesforce Developer Edition or Trailhead Playground

Open the Sales App

Confirm you have System Administrator access

Step 2: Configure Accounts (Customers)

Accounts represent customer organizations.

Actions

Go to Setup → Object Manager → Account

Open the Type field (or create a custom “Account Type” field)

Set picklist values:

School

Business

Organization

Save

Step 3: Configure Contacts (People)

Contacts represent individuals tied to customer accounts.

Actions

Setup → Object Manager → Contact

Create a new Picklist field:

Field Label: Role

Values:

Buyer

PTO Member

Administrator

Save

Step 4: Configure Opportunities (Apparel Orders)

Opportunities represent apparel orders.

Create Custom Fields

Go to Setup → Object Manager → Opportunity → Fields & Relationships

Create:

Garment Type (Picklist): T-Shirt, Hoodie, Tote, Hat, Other

Quantity (Number, 0 decimals)

Decoration Method (Picklist): Print, Embroidery, Patch, Mixed

Rush Order (Checkbox)

Step 5: Configure Opportunity Stages

Stages reflect the order lifecycle.

Stages:

Inquiry

Quoted

Approved

In Production

Completed

Closed Lost

Create or edit stages in:
Setup → Object Manager → Opportunity → Stage

Step 6: Create a Record Type

Record Types separate apparel orders from other sales.

Setup → Object Manager → Opportunity

Click Record Types → New

Name: Apparel Order

Assign your custom sales stages

Assign to Admin profile

Step 7: Page Layout

Opportunity → Page Layouts

Create Apparel Order Layout

Add fields:

Opportunity Name

Account

Stage

Close Date

Garment Type

Quantity

Decoration Method

Rush Order

Step 8: Validation Rule (Data Quality)

Prevent approving incomplete orders.

Rule Logic

If Stage = Approved
AND garment, quantity, or decoration is blank
→ show error

Step 9: Reports & Dashboard

Create reports:

Orders by Stage

Revenue by Account Type

Monthly Sales Trend

Create dashboard:

Name: South Side Girl Sales Dashboard
