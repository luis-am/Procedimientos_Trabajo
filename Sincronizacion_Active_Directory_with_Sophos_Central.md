# Active Directory 

Need to set API credentials for using Sophos Central APIs & Windows Active Directory Sync Tool.

	- Max 10 API credentials

#### Global Settings > API Credentials Management > Add credentials

- Credential name: []
- Description: []
- Role: Service Principle Directory Sync

- Get:
	- Client ID: []
	- Client Secret: []

#### People > Set up directory service > Download AD Sync Installer

#### Launch the installer

- Tab Sophos Credentials > Client ID
	- Client ID: []
	- Client Secret: []

- Tab AD Configuration
	- Use LDAP ... ✅
	- Hostname or IP: []
	- Port number: 636
	- Active Directory username: [format: ]
	- Active Directory password: []

#### User domain does not need administrative rights.

- Tab AD Domains
	- Include all domains ✅

- Tab AD filters
	- Sync devices ✅
	- Sync UO ✅
	- Sync users and groups ✅
	- Sync public folders ✅

- Tab Sync Schedule
	- Daily sincronization (Sophos recomendation)
	- Finish

- Tab Users to add
	- Approve Changes and Continue


---


# Setup Azure Application

- Create azure application
- Create client secret
- Configure application permissions
- Find tenant domain information

1. Register an application

	- Name: []
	- Who can use this application: [First option]
	- Redirect URI: Web | https://central.sophos.com

2. Create a client secret

	- Certificates and secrets > new client secret
	- Get:
		- Value: []
		- Expiration Date: []

3. Configure application permisions

	- API permissions > Add a permision > Microsoft Graph > Directory.Read.All
	- Grant admin consent for your Azure AD ✅

4. Find tenant domain information

	- Get:
		- Application (client) ID
		- Primary domain

#### Setup Sophos Central Azure

	- Global Settings > Directory Service > Azure config
	- Put the data obtained in Azure Active Directory
