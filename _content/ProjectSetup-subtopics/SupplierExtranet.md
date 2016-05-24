---
title: "Supplier Extranet"
status: TODO
---

## Infrastructure Setup
TBC

## Web Config Setup
- Direct the web config to the generic style folder
	<pre>&lt;add key="CustomFolder" value="generic"/&gt;</pre>
- Add the company name to the web config
	<pre>&lt;add key="CompanyName" value="TBC"/&gt;</pre>
- Set CMS URL
	<pre>&lt;add key="CMSBaseURL" value="http://localhost:4031/Content/"/&gt;</pre>
- Set Client Templates Folder
	<pre>&lt;add key="ClientTemplateFolder" value="c:\projectsvault\ivector\clienttemplates\tcb\"/&gt;</pre>


## Optional Further Setup
- Set map key in web config
	<pre>&lt;add key="GoogleMapsKeyOverride" value="xxxxxxxxxx"/&gt;</pre>
- Create custom styling folder (Note: there should be a roadmap dev to simplify this in future so that it is possible to override just a fixed amount of styling)
	- Copy the generic styling folder to /Custom/[CustomerName]
	- Change the styling as required to override the base (generally it will only be required to use a customer specific logo)