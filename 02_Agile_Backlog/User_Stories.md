## User Stories – Salesforce CRM

•	BA-001 Create Account Types (School, Business, Organization)
As a business owner
I want to classify customer accounts by type
So that I can segment customers and analyze revenue by category
•	Acceptance Criteria
Given Account Type picklist field exists on the Account object
	Picklist values include:
o	School
o	Business
o	Organization
Account Type is required on Account creation
Field is visible on page layout
Field is available in reporting
Priority: High
Story Points: 3
Definition of Done
•	Field created and deployed
•	Tested in sandbox
•	Demonstrated in sprint review


•	BA-002 Add Contact Role field (Buyer, PTO Member, Administrator)
User Story
As a business owner
I want to define each contact’s role
So that I know who the primary decision-maker is
	Acceptance Criteria
Given a Contact Role picklist field is created, I should see
Values include:
o	Buyer
o	PTO Member
o	Administrator
Field visible on Contact layout
Field included in reports
Priority: High
Story Points: 3


•	BA-003 Create Apparel Order Opportunity Record Type
As a business owner
I want a dedicated Opportunity record type for apparel orders
So that orders follow a standardized lifecycle
 Acceptance Criteria
Given that the Record Type named “Apparel Order” is created
Custom stages assigned to record type
Record type assigned to appropriate profiles
Page layout associated orders will follow a standard process
Priority: High
Story Points: 5



•	BA-004 Add Order Detail Fields (Garment Type, Quantity, Decoration Method, Rush Order)
As a business owner
I want to capture detailed order information
So that production requirements are clearly defined
	Acceptance Criteria
Given Fields created on Opportunity I should see:
•	Garment Type (Picklist)
•	Quantity (Number)
•	Decoration Method (Picklist)
•	Rush Order (Checkbox)
•	Fields added to Apparel Order layout
•	Fields available for reporting
	Priority: High
Story Points: 5



•	BA-005 Configure Opportunity Stages for Order Lifecycle
As a business owner
I want defined opportunity stages
So that all orders move through a consistent process
•	Acceptance Criteria Given opportunity stages are defined I should see
Stages include:
•	Inquiry
•	Quoted
•	Approved
•	In Production
•	Completed
•	Closed Lost
•	Stage probabilities configured
•	Stages aligned with Apparel Order record type
Priority: High
Story Points: 3


•	BA-006 Create Validation Rule to Enforce Required Fields Before Approval
As a business owner
I want Salesforce to prevent incomplete orders from being approved
So that production errors are minimized
•	Acceptance Criteria: given that an incomplete order is created, there will be 
•	Validation rule prevents Stage = Approved if:
o	Garment Type is blank OR
o	Quantity is blank OR
o	Decoration Method is blank
•	User sees clear error message
•	Rule tested successfully
•	Priority: High
Story Points: 3


•	BA-007 Design Opportunity Page Layout for Order Intake
As a business owner
I want an optimized Opportunity page layout
So that order intake is efficient and structured
  Acceptance Criteria given that the page layout have been updated I should see:
•	Order detail fields grouped logically
•	Required fields clearly marked
•	Clean section layout
•	Layout assigned to Apparel Order record type
•	Priority: Medium
Story Points: 3


•	BA-008 Create Orders by Stage Report
As a business owner
I want to see orders grouped by stage
So that I understand the is workload and bottlenecks
•	Acceptance Criteria
Given that the orders are grouped by stages I should see
•	Report grouped by Opportunity Stage
•	Filtered to Apparel Order record type
•	Date filter available
•	Summary totals displayed
•	Priority: Medium
Story Points: 3


•	BA-009 Create Revenue by Customer Type Report
As a business owner
I want revenue segmented by Account Type
So that I know my strongest customer segments
  Acceptance Criteria
Given that the revenue is segmented by account, I should see
•	Revenue grouped by Account Type
•	Total revenue displayed
•	Filtered to Apparel Orders
•	Report validated for accuracy
•	Priority: Medium
Story Points: 3


•	BA-010 Build Sales Dashboard
	User Story
As a business owner
I want a dashboard summarizing sales performance
So that I can make informed decisions quickly
 	Acceptance Criteria
Given that a Dashboard has been created, the Dashboard should include:
•	Orders by Stage chart
•	Revenue by Customer Type chart
•	Monthly sales trend chart
•	Dashboard refresh enabled
•	Priority: Medium
Story Points: 5


•	BA-011 Create Flow to Auto-Create Follow-Up Tasks
	User Story
As a business owner
I want a follow-up task automatically created when a new order is logged
So that no inquiries are missed
•	Acceptance Criteria
•	Record-triggered Flow created
•	Flow runs when Stage = Inquiry
•	Task includes:
o	Due date (2 business days)
o	Clear description
•	No duplicate tasks created
•	Priority: Medium
Story Points: 5


•	BA-012 Configure Stage-Based Automation Tasks
	User Story
As a business owner
I want tasks automatically created when orders move stages
So that next steps are consistently followed
 	Acceptance Criteria
Tasks created when Stage moves to:
•	Quoted
•	Approved
•	Completed
•	Tasks related to Opportunity
•	Task owner assigned correctly
•	Priority: Medium
Story Points: 5


•	BA-013 Create Approval Process for Rush or High-Volume Orders
User Story
As a business owner
I want approval required for high-risk orders
So that financial and operational risks are controlled
•	Acceptance Criteria
Approval triggered when:
•	Rush Order = true OR
•	Quantity exceeds defined threshold
•	Opportunity cannot move to Approved until approved
•	Approval notification sent
•	Priority: Low
Story Points: 5


