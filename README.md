# Info
The tool is currently beeing implemented using Django DRF and React with Material-UI. Since I'm neither a front- nor a backend developer, I'm pretty sure the code has a lot of potential for improvement :-))

> [!IMPORTANT]  
> The project has a rather advanced state, as I'm using it for my own purposes already. There are a lot of tasks at hand:
> 
> - Continue development of features and functionality in frontend and backend
> - Check and improve software architecture
> - Starup-Guide (on Frontend)
> - ...
>   
> **So if anyone is interested in contributing, please let me know!**

Deployment is planned as two containers, one for frontend (vite) and one for the backend (django, redis, celery, LaTeX environment). Currently frontend is based on node:20-alpine and backend on phusion/baseimage:jammy.

Documentation creation is done with LaTeX via celery and redis, so if you know your way around a little the templates are highly customizable, so you can design whatever you like!

If anyone should be interested in helping with development please let me know and I'll move the project to github!

## 💖 Help Me Keep This Project Going

Maintaining and improving this project takes time, energy, and resources. If you like the idea and want to see the project progressing and released, consider supporting its development! Ideally you're a frontend (react) or backend (python) dev and you're in need of a tool like this! 

## 🙌 Ways You Can Help

- **Contribute** – Are you a frontend or backend developer? Let me know if you want to contribute!
- **Share the project** – Spread the word!
- **Open issues** – Found a bug or have a feature suggestion? Open an issue and let me know!
- **Support financially** – If you’d like to support this work directly, consider:

  - ❤️ [Sponsor me on GitHub](https://github.com/sponsors/bee-eater)
  - 🧡 [Donate via PayPal](https://www.paypal.com/donate/?hosted_button_id=MUS7QJU8YB9CY)

Your support makes a real difference — thank you!

# Features
Currently planned features are something like:
- [x] Create companies (--> The user could manage multiple companies)
- [x] Create customers and employees of the customer with detailed info
- [x] Automatic creation of customer numbers and document numbers
- [x] Default discount values etc. can be set for a customer
- [x] Create document templates containing opening, closing etc.
- [x] Create service templates for quicker building of quotes etc.
- [x] Create and manage workflows, where a workflow defines the process of quote, order, confirmation, downpayment, invoice, dunning, etc...
- [x] Dashboard with overview tiles: ToDo, open workflows, open invoices, overdue invoices, some statistics?!
- [x] Button bar on dashboard for common tasks like "New document", "New workflow", "New customer", ...
- [x] Export documents as PDF via LaTeX templates
- [x] Saving of exported documents
- [x] Support of ZUGFeRD invoicing using [python-drafthorse](https://github.com/pretix/python-drafthorse)
- [x] Locking of documents as soon as it's required. (e.g. protect / lock an invoice document as soon as it's exported, so it can't be changed anymore...)
- [ ] Create customer actions, to track what was already done (e.g. Call because of something etc...)
- [ ] Manage travel times including pdf export of overview including amounts for meals per diem (Verpflegungspauschale)
- [ ] EPC QR code on invoices

Some checked features are implemented just rudimentary and could be improved. 

# Ideas
- Audit log to get best possible GoDB conformity
- Test and increase data validation and error handling (frontend / backend)
- Provide own rules for number creation (customers, docs, ...)
- Export for tax inspections
- Asset management (computers etc...)
- Create more templates for different doc types
- Make everything more customizable via the frontend
- Add document signing via [pyHanko](https://github.com/MatthiasValvekens/pyHanko)
