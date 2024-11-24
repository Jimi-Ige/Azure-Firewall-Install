# Azure-Firewall-Install

**Overview:** This lab demonstrates configuring an Azure Firewall to secure Azure resources. The focus is on deploying the firewall, setting up rules, and validating its effectiveness through testing and monitoring.

**Prerequisites:**
✅ Active Azure subscription with sufficient permissions (Owner/Contributor/Network Contributor).
✅ A virtual network with at least two subnets (AzureFirewallSubnet and VMSubnet).
✅ Networking knowledge for subnets, routing, and security rules.
✅ A test virtual machine to validate firewall rules.
✅ Diagnostic settings enabled for Azure Firewall.

**High-Level Steps with Explanations:**

 **1: Use a template to deploy the lab environment:** I start by using a pre-configured ARM template to deploy the foundational lab environment. This includes setting up a virtual network with required subnets and resources and ensuring I have the necessary infrastructure to work with Azure Firewall.

 **2: Deploy an Azure firewall:** Next, I deploy an Azure Firewall in the dedicated AzureFirewallSubnet. This will be a centralized, cloud-native security solution to protect and monitor traffic across my virtual network.

 **3: Create a default route:** To route all traffic through the Azure Firewall, I configure a default route in the route table associated with the VM subnet. This ensures all outbound and inbound traffic passes through the firewall for inspection.

 **4: Configure an application rule:** I created an application rule in the Azure Firewall to control outbound web traffic based on specific FQDNs. This will allow or deny access to certain websites, ensuring application-layer security.

 **5: Configure a network rule:** I set up a rule to allow or block specific traffic based on protocol, source, destination, and ports. This enables me to define more granular control over my network traffic.

 **6: Configure DNS servers:** I configure DNS servers for the Azure Firewall to resolve domain names efficiently and ensure the firewall can correctly process application rules that rely on FQDN filtering.

 **7: Test the firewall:** I deploy a test virtual machine and validate the firewall configuration. I’ll test both allowed and blocked traffic to ensure the rules function as expected and secure the environment.

**Reference Link(s):**
* [https://microsoftlearning.github.io/AZ-104-MicrosoftAzureAdministrator/Instructions/Labs/LAB_02b-Manage_Governance_via_Azure_Policy.html](https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/Instructions/Labs/LAB_03_AzureFirewall.html)
