---
title: "New Client - Infra to Development Handover Checklist"
status: INPROGRESS
---

This is checklist that should be carried out when the new client environment is handed over to the Development Team from the Infrastrucure Team.

- Port 22 open on webserver
	- Use PuTTy to connect via ssh from local machine
- SQL server set to Trustworthy, and has has the schema from iVector_Blank
	- select dbo.encrypt('Test')
- DBMail setup
	- dbo.emailsend 'admin@intuitivesystems.co.uk', 'test', sama@intuitivesystems.co.uk','','','test','Test Email',0
- Folder structure for web applications with web.configs
	- Test
	- Live
- IIS setup to point to the empty folders
- Internal DNS setup
- Credentials for RDP and SQL on the intranet
