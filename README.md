# SIEM (Microsoft Sentinel) Implementation

The project is undertaken in a controlled environment, using Microsoft's native training lab, to set up a cloud-based Security Information and Event Management tool (Microsoft Sentinel), for detecting cyber attacks. The primary focus is to ingest and analyze logs, to deepen understanding of network security, attack patterns and defensive strategies.

To create a Microsoft Sentinel instance, you have to first create a resource group, which is a container for grouping Azure resources. A log analytics workspace will next be created, the solution that Sentinel uses for storing data and interacting with it.

## Steps

Log into the Azure Portal and search for "resource groups". Select it and it will take you to the resources portal. Select "Create" and provide the resource group name, and select the region. In a production environment, best practice is to create all resources in the same region as the resource group.


<img width="900" alt="Screenshot 2024-02-20 at 11 39 54" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/199f9726-7212-40ad-9b76-a63ed3262730">

<img width="888" alt="Screenshot 2024-02-20 at 11 54 23" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/0611f34c-d643-42c5-9a32-56cf50876f90">

<img width="809" alt="Screenshot 2024-02-20 at 12 02 29" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/e577d5e3-b102-4fc8-b216-3309723690e2">


Click "Review+create", and then click "Create" on the bottom left of the screen and the resource group will be created:


<img width="819" alt="Screenshot 2024-02-20 at 12 05 51" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/ed34aed7-3125-427b-b8b8-d6087e149b51">

<img width="913" alt="Screenshot 2024-02-20 at 12 07 36" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/fb62f891-4a5b-4ea1-937a-a64ab71769b6">


The next step is to create the Log Analytics Workspace. 

Click on the recently created resource group, and then select "Create". In the search bar, search for "log analytics workspace". Select "create" and then "Log Analytics Workspace" on the Log Analytics Workspace results card:


<img width="1059" alt="Screenshot 2024-02-20 at 12 19 30" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/49084d8d-41f3-40c2-a9a4-8a753d6b87ea">

<img width="792" alt="Screenshot 2024-02-20 at 12 20 26" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/88a17729-7d22-470e-a721-7aa1decff8d1">


The resource group will be automatically populated. Provide a name for the analytics workspace and click on "Review+Create", and then "Create":


<img width="790" alt="Screenshot 2024-02-20 at 12 21 04" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/e74ff07b-8288-41a2-a174-2fc9c8d323cb">


Once the deployment has completed you can click on "Go to resource" to navigate to the Log Analytics Workspace:


<img width="1054" alt="Screenshot 2024-02-20 at 12 29 55" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/a37016c2-bd15-4ead-b3c0-8688e979486f">


With the resource group and Log Analytics Workspace created, we can now create Microsoft Sentinel on top of that. Search for Microsoft Sentinel and then select it:


<img width="980" alt="Screenshot 2024-02-20 at 12 28 53" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/0a84e4e0-025c-4709-83b9-87070bb13446">


Select "Create", and then select the Log Analytics Workspace just created and click on "Add":


<img width="905" alt="Screenshot 2024-02-20 at 12 31 40" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/82266b7e-1097-4688-acd8-c4118163418e">

<img width="772" alt="Screenshot 2024-02-20 at 12 32 51" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/a0f75984-fe32-447b-acb1-d7dde17440d1">

<img width="783" alt="Screenshot 2024-02-20 at 12 33 22" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/fd4a9e58-0cde-41fa-9622-19e72694595d">


The Microsoft Sentinel page will open.

Select "Content hub" and search for "training". Select the "Microsoft Sentinel Training Lab" solution. This will ingest pre-recorded data into Sentinel. Click on "Install":


<img width="880" alt="Screenshot 2024-02-20 at 12 37 04" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/d63dc751-aad8-4c26-995e-155fd55752f1">

<img width="1020" alt="Screenshot 2024-02-20 at 12 37 33" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/f5fd1dd2-1011-49ce-9f85-c9057040ebd0">

<img width="922" alt="Screenshot 2024-02-20 at 12 38 51" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/b887e778-6724-427b-a66a-522d6f118391">

You will move to a new page, and click on "Create":

<img width="1041" alt="Screenshot 2024-02-20 at 12 51 44" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/3f0e038f-71b2-42e0-af09-1d7e6023b018">


Select your resource group and the Log Analytics Workspace and click on "Review+Create" and then "Create":


<img width="1003" alt="Screenshot 2024-02-20 at 12 53 01" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/f72f6e2e-4678-4cfb-8bfb-b47a550d185f">

<img width="832" alt="Screenshot 2024-02-20 at 12 57 46" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/88327213-41bf-43a3-b9d9-bd693fd8c649">


The deployment of the training lab will then commence and once completed, search for and navigate to "Microsoft Sentinel":


<img width="927" alt="Screenshot 2024-02-20 at 12 58 49" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/8528ac5b-d7e7-471b-8b50-aca055a4ddb8">

<img width="1016" alt="Screenshot 2024-02-20 at 12 59 49" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/9f435ac7-7157-4a61-851c-eaacea755d0b">

<img width="1034" alt="Screenshot 2024-02-20 at 13 01 11" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/a1bc0060-a247-404c-b1c7-74cfaf47a317">


You will be greeted by a dashboard that presents some basic information. You will notice 3 new incidents, which were created by the training solution installed:


<img width="1438" alt="Screenshot 2024-02-20 at 13 25 22" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/b407f4c3-f8a5-4c01-ae61-d11ac791d52b">

The "Data Connectors" are how data is ingested into Microsoft Sentinel, into the Log Analytics Workspace. It shows the sources of the data in Sentinel. There will be one data connector, the "Cisco Umbrella":


<img width="1330" alt="Screenshot 2024-02-20 at 13 29 33" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/b0dce5d1-ba41-499a-9e36-7191c1b1d489">


We can now search the data using "Logs":


<img width="1028" alt="Screenshot 2024-02-20 at 13 02 07" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/fdbe4744-6a0b-43ef-a171-1666c7a543e5">


To search the data, we use KQL, Kusto Query Language. If not familiar with the syntax, Microsoft provides built-in functionality that makes it easy to get started. The landing page of the "Logs" section is  "Tables", grouped into 2 different sections for the training lab; Microsoft Sentinel and Custom Logs:


<img width="937" alt="Screenshot 2024-02-20 at 14 12 11" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/28a731af-f646-4fe0-8ff2-5251e3637b83">

Expand "Custom Logs" to reveal more tables and double-click the "AzureActivity_CL" table.


<img width="976" alt="Screenshot 2024-02-20 at 14 13 53" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/6114a174-94d1-4daa-97fe-d0811963a459">


Click on "Run" and the results will show at EVERYTHING that happens inside the Azure subscription:


<img width="834" alt="Screenshot 2024-02-20 at 14 15 58" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/3cf01e94-401d-44f3-8364-e6d1245a0198">


<img width="1432" alt="Screenshot 2024-02-20 at 14 18 16" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/70c255d7-f629-43b1-a50c-ffee592f98ef">


You can then expand one of the results to get more information. In the example below, a log of a deleted virtual machine is observed. Scroll down for more details and under "Caller_s", right-click the username and select "Include", to add the user to the KQL query and run a new search query for results related only to the user:


<img width="1067" alt="Screenshot 2024-02-20 at 14 35 04" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/885789bb-365e-4437-ae0f-2dba59c72151">

<img width="1069" alt="Screenshot 2024-02-20 at 14 38 04" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/e666047f-d760-479d-b515-a0767d7fe8b2">

<img width="963" alt="Screenshot 2024-02-20 at 14 38 36" src="https://github.com/cyberkels/SIEM_Implementation_and_Incident_Investigation/assets/147159632/f2fa5110-1768-4768-917c-44a630744ad0">

From here you can then continue your investigations in the environment, using the "Threat Management" menu, using "Hunting" to proactively hunt for cyber security threats inside the data, "Workbooks" for performing detailed investigations by running queries, visualizations and analytics, "Entity Behavior" for the patterns exhibited by different entities (eg, users, hosts, IP addresses) and "Threat Intelligence" for building your own database for different Indicators of Compromise (IOC).

There is also "Automation", which allows automation of incident handling, integrating with third-party services like virus-totals, AbuseIP DB and other solutions that are not natively integrated with Microsoft Sentinel.



