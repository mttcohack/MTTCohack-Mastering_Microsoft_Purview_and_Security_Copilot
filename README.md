# MTT CoHack Challenge : Secure Data CoHack: Mastering Microsoft Purview & Security Copilot.
## Challenge 1 (Business User - Insider)
### Goal: 
Objective of this challenge is to take up the role of an insider who performs multiple data security incidents/policy violations as a business user.
Users with Business User Persona: 
1.	ChristieC@M365DS12345.OnMicrosoft.com
2.	DebraB@M365DS12345.OnMicrosoft.com
3.	DiegoS@M365DS12345.OnMicrosoft.com
4.	GradyA@M365DS12345.OnMicrosoft.com
5.	IrvinS@M365DS12345.OnMicrosoft.com
6.	JohannaL@M365DS12345.OnMicrosoft.com
7.	LeeG@M365DS12345.OnMicrosoft.com
### Tools:
Outlook for Web, Microsoft Teams, SharePoint Online, OneDrive for Business.
### Activities:
1.	Use Microsoft 365 services to perform Data Loss activity: 
Login to office.com (Coach will share the credentials)
Insider tries (but fails) to share sensitive information (credit card numbers) to other users via Email, Teams (1:1, 1:N chat, public channel, private channel, Teams meeting body content), create a document in SPO site with sensitive information (Global Sales: https:// M365DS12345.sharepoint.com/sites/GlobalSales). 
Try any other Microsoft 365 service to Perform Data Loss Activity.  
_Hint: OneDrive for Business._

2.	Perform Data Exfiltration Activity – by priority users. 
Business users who handle Critical Data, downloads multiple documents from priority SharePoint site (Global Sales: https:// M365DS12345.sharepoint.com/sites/GlobalSales) and sends to personal email address.
_Tip: The more data exfiltrated, more severe alerts._

## Challenge 2 (Data Protection Officer-Data Security Administrator)
### Goal: 
Secures Data in Microsoft 365 services by triaging, investigating and customizing the policies (DLP, Insider Risk Management).
Users with Security & Compliance Administrator Persona: 
1.	AdeleV@M365DS12345.OnMicrosoft.com
2.	AlexW@M365DS12345.OnMicrosoft.com
### Tools:
Microsoft Purview portal, Microsoft Defender portal.
### Activities:
1.	Monitor and investigate Data Security Events and Activities using 
a.	Alerts, Activity Explorer in Purview portal > DLP Solution. 
b.	Incidents page in Defender portal > Export Incident Summary PDF.
2.	Tune the existing policies – to fix misconfiguration causing data loss (Hint: OneDrive for Business)
3.	Add a new rule in the existing DLP policy to detect and restrict SSN (Social Security Number) and block sharing in all Microsoft 365 services.
4.	Edit the Insider Risk Management policy to add one more priority SharePoint site (‘The Landing’ site: https:// M365DS12345.sharepoint.com).
## Challenge 3 (SOC- Security Operations)
### Goal:
To use Defender to Monitor Data Security incidents. To utilize Copilot (Microsoft Copilot & Security Copilot) to Detect, Investigate and Respond to Insider threat activities performed in Challenge 1.
### Tools:
Microsoft Defender portal, Microsoft Copilot, Microsoft 365 Copilot Chat-Web, Security Copilot.
### Activities:
1.	Use Microsoft Defender portal to https://security.microsoft.com > Advanced hunting page to find the table schema that stores ‘Alert Information’ records.
Or use Microsoft Copilot for the same:
Sample Prompt: _Give me the table schema name to use in KQL query, where "Alert information" is found in latest Microsoft Defender portal security.microsoft.com, Hunting, Advanced hunting page._

3.	Use Microsoft Copilot to find KQL queries to perform Advanced Hunting in AlertsInfo table.
Follow up prompt to previous chat: _Can you provide example KQL queries using AlertInfo?_

4.	Use Security Copilot to perform investigation in Insider risks, Generate Incident report and Export Incident as PDF:
Note: You’ll now switch to the Security Copilot demo environment
- DLP policy (U.S. Financial Data): https://security.microsoft.com/incident2/1990/overview?tid=0527ecb7-06fb-4769-b324-fd4a3bb865eb
- DLP policy: https://security.microsoft.com/incident2/2337/overview?tid=0527ecb7-06fb-4769-b324-fd4a3bb865eb
- Incident: https://security.microsoft.com/incident2/5583/overview?tid=0527ecb7-06fb-4769-b324-fd4a3bb865eb
## Reference resources
- [Learn about investigating data loss prevention alerts](https://learn.microsoft.com/purview/dlp-alert-investigation-learn)
- [Create and Deploy data loss prevention policies](https://learn.microsoft.com/purview/dlp-create-deploy-policy)
- [Create and manage insider risk management policies - Prioritize content in policies](https://learn.microsoft.com/purview/insider-risk-management-policies?tabs=purview-portal#prioritize-content-in-policies)
- [Summarize an incident with Copilot in Microsoft Defender](https://learn.microsoft.com/defender-xdr/security-copilot-m365d-incident-summary)
- [Security Copilot in Microsoft Purview Overview](https://learn.microsoft.com/purview/copilot-in-purview-overview )
## Appendix:
### Sample Sensitive Information:
- Credit Card Account number: Visa 4012888888881881 
- Debit Card Account number: MasterCard 5420923878724339
- visa 5293-8502-0071-3058 1/20/2022
- visa 345389698201044
- Amex 30204861594838
- visa 38520000023237
- visa 4539-0031-3703-0728
- amex 30569309025904
- visa 4929-3813-3266-4295  
- mastercard 5105105105105100
- [More sample Sensitive information](https://dlptest.com/sample-data) 
