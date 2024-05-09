# Info
The tool is currently beeing implemented using Django DRF and React with Material-UI. Since I'm neither a front- nor a backend developer, I'm pretty sure the code has a lot of potential for improvement :-))

Deployment is planned as two containers, one for frontend and one for the backend (django, redis, celery, LaTeX environment). Currently frontend is based on node:20-alpine and backend on phusion/baseimage:jammy.

Documentation creation is done with LaTeX via celery and redis, so if you know your way around a little the templates are highly customizable, so you can design whatever you like!

If anyone should be interested in helping with development please let me know and I'll move the project to github!

# Features
Currently planned features are something like:
- Create companies (--> The user could manage multiple companies)
- Create customers and employees of the customer with detailed info
- Automatic creation of customer numbers and document numbers
- Default discount values etc. can be set for a customer
- Create document templates containing opening, closing etc.
- Create service templates for quicker building of quotes etc.
- Create and manage workflows, where a workflow defines the process of quote, order, confirmation, downpayment, invoice, dunning, etc...
- Dashboard with overview tiles: ToDo, open workflows, open invoices, overdue invoices, some statistics?!
- Button bar on dashboard for common tasks like "New document", "New workflow", "New customer", ...
- Manage travel times including pdf export of overview including amounts for meals per diem (Verpflegungspauschale)
- Export documents as PDF via LaTeX templates
- EPC QR code on invoices
- Saving of exported documents
- Support of ZUGFeRD invoicing using (https://github.com/pretix/python-drafthorse)[python-drafthorse]
- Locking of documents as soon as it's required. (e.g. protect / lock an invoice document as soon as it's exported, so it can't be changed anymore...)


# Ideas
- Audit log to get best possible GoDB conformity
- Export for tax inspections
- Asset management (computers etc...)
- Create more templates for different doc types
- Make everything more customizable via the frontend
