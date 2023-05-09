# Schema

## Accounts

<!--
This table will store information about various accounts, such as tools, consumables, vehicle expenses, insurances, education costs, etc. Each account will have a unique identifier and other relevant attributes, such as the account name and description.
-->

accounts
------------------------------------------------
account_id (primary key)
account_name
description

## Transactions

<!--
This table will record individual transactions for each account, capturing the inflows and outflows of money associated with the accounts. Each transaction will have a unique identifier and will be linked to an account through a foreign key relationship.
-->

## Vehicles

<!--
This table will store details such as the vehicle's make, model, year, registration number, and any other relevant information.
-->

vehicles
------------------------------------------------
vehicle_id (primary key)
make
model
year
registration_number

## Expenses

<!--
This table can be used to record various expenses associated with your business, such as vehicle expenses, tool purchases, consumables, insurances, education costs, travel expenses, etc. It can include attributes like the expense type, description, amount, and date.
-->

expenses
------------------------------------------------
expense_id (primary key)
expense_type
description
amount
expense_date

## Clients

<!--
This table will store information about your clients or customers.
-->

clients
------------------------------------------------
client_id (primary key)
client_name
contact_person
contact_email
contact_phone
address

## Projects

<!--
This table will capture information about the different projects you undertake for your clients.
-->

projects
------------------------------------------------
project_id (primary key)
project_name
client_id (foreign key to clients)
start_date
end_date
total_cost

## Invoices

<!--
This table will track the details of your invoices raised for the projects.
-->

invoices
------------------------------------------------
invoice_id (primary key)
project_id (foreign key to projects)
invoice_date
due_date
amount
payment_status
