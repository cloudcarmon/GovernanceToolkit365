# Governance Toolkit 365

The Governance Toolkit 365 (GT365) provides a compliance coverage across multiple workloads. The toolkit runs as Software-as-a-Service and automatically requests usage data from the Microsoft 365 services and delivers summarized and detailed information to custom users and administrators. 

GT365 does not provide a user interface, but collects data in the background and provides that accumulated data for use with clients such as Microsoft Power-BI or Excel. Also, email notifications are sent to team owners and IT Administrators.

Additionally, the Governance Toolkit 365 provides an API for provisioning a new Office 365 Group or a new Microsoft Team. See a feature overview at [www.governancetoolkit365.com](https://governancetoolkit365.com/).

[![link](./images/governance_toolkit_logo.png)](./governance_toolkit_logo.png "GT365 logo")

<div style="page-break-after: always;"></div>

## Setup

The GT365 is provided as SaaS solution. Depending on the planned usage, you can use the reporting part only, the newsletters and the API if required. The  onboarding includes these steps.

1. Open the [www.governancetoolkit365.com](https://governancetoolkit365.com/) website. At the end, there´s a Register link. Open that link.
2. Fill out the form and ensure that you enter **your email address and a valid Microsoft 365 domain**. The domain name is usually your email address domain, such as "contoso.com". Then, submit the form. When submitted, you will see a confirmation such as "Thank you for submitting your request. You will receive an email when the approval is done.".

[![link](./images/register-1.png)](./images/register-1 "Click to enlarge")

[![link](./images/register-2.png)](./images/register-2 "Click to enlarge")

4. The request will be manually approved usually within one business day. You will receive an email with the subject "GT365: Pls. grant the app consent: {your-domain}".
Send this email (or the provided [link](https://login.microsoftonline.com/common/adminconsent?client_id=f6108159-1168-475d-b3ca-be8104781bf8)) to a Global Administrator of your Microsoft 365 tenant.

[![link](./images/setup-1.png)](./images/setup-1.png "Click to enlarge")

5. A Global Admin must open that link and confirm the app access.When working with multiple identities, we recommend to open the link in a browser In-Private mode.

[![link](./images/setup-2.png)](./images/setup-2 "Click to enlarge")

Sign-in with the Global Admin and the password (and additional sign-options if configured). After the login, click "Accept" the Governance Toolkit 365 app.

[![link](./images/setup-3.png)](./images/setup-3 "Click to enlarge")

The app only asks for reading permissions for directory data, groups and users. You will be redirected to a confirmation page.

[![link](./images/setup-4.png)](./images/setup-4 "Click to enlarge")

6. Now the GT365 app is allowed to access the tenant. The statistics generation is done during the night. So, you will receive emails with the Storage Account access data on the next day automatically. Wait for that emails. They contain the Storage name and key, similar as in the following screenshots.
The first email has the subject "GT365: Your storage for "{your-domain}" and contains the Storage Account name.

[![link](./images/setup-5.png)](./images/setup-5 "Click to enlarge")

The second email has the subject "GT365: Your storage data part two" and contains the (long) Storage Account key.

[![link](./images/setup-6.png)](./images/setup-6 "Click to enlarge")

Note that data in a secure place. You need that for accessing the daily generated data. The keys are randomly generated.

## Usage

- Access the data with the Storage Account name and key with a client tool, such as [Power BI](https://powerbi.microsoft.com/en-us/downloads/). You can download a GT365 dashboard sample zip-file from [here](https://governancetoolkit365.com/download/GovernanceToolkit365-Template.zip).
- Adapt the Power BI dashboard as needed. See some sample dashboards here: 

[![link](./images/bi-demo-1.png)](./images/bi-demo-1 "Click to enlarge")

[![link](./images/bi-demo-2.png)](./images/bi-demo-2 "Click to enlarge")

[![link](./images/bi-demo-3.png)](./images/bi-demo-3 "Click to enlarge")

[![link](./images/bi-demo-4.png)](./images/bi-demo-4 "Click to enlarge")

[![link](./images/bi-demo-5.png)](./images/bi-demo-5 "Click to enlarge")

[![link](./images/bi-demo-6.png)](./images/bi-demo-6 "Click to enlarge")


## Setup newsletters (optional)

Automatic newsletters inform about orphaned groups and guest access.

If you want to use automatic newsletters, follow these steps described at [Governance Toolkit 365 ReadMe]((https://github.com/delegate365/GovernanceToolkit365).

## Use the API (optional)

The API allows to provision a new group out of an application or a workflow.

If you want to use the GT365 API, follow these steps described at [Governance Toolkit 365 API](https://github.com/delegate365/GovernanceToolkit365/blob/master/API.md).

## Security in GT365

Security is an important topic for any system. We care about security and privacy. 
The concept of GT365 is to work with least privileges and without storing any user credentials. So, a Global Admin has to allow access for the GT365 app to read directory data and groups. This creates an application in the customer´s Microsoft 365 tenant that the GT365 can use programmatically and generate the statistics for that tenant. After the app access has been granted, the customer receives a private Storage Account key to get access to the generated data.
When using the API, the GT365 expects a valid token from the customer´s tenant to provision a new Office 365 Group or Team. The token grants access only to provision a group with the required user data. The token is usually valid just for up to one hour and expires then.
GT365 never stores any user credentials. To remove the access, the GT365 app can be removed in the customer´s tenant anytime.

## Contact

In case of questions, pls. contact 

atwork

[support@atwork.at](mailto:support@atwork.at?subjectGT365)

[www.atwork-it.com](https://www.atwork-it.com/contact/)


Enjoy!