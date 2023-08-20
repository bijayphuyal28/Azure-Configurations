# Hosting a DNS Zone in Azure and adding domain to Microsoft 365 tenant

# Hosting a DNS Zone in Azure and Adding Domain to Microsoft 365 Tenant

A DNS zone is a portion of the DNS namespace that is used to host the DNS records for a particular domain. To host DNS Zone in Azure DNS, you need to create a DNS zone for that domain name in Microsoft Azure and then the records can be added inside the DNS Zone.

This guide will walk you through the process of hosting a DNS Zone in Azure and adding a domain to your Microsoft 365 tenant. This provides you with the functionality of using own custom domain name with Microsoft 365 services. Note that this project uses the third party as the domain registrar.

## Prerequisites

Before you begin, you should have the following:

- Azure Tenant
- Azure account with permissions to create a DNS Zone
- Custom domain name registered with a third party domain registrar
- Microsoft 365 tenant with global admin permissions

## Azure Services Used:

- Azure DNS

## Step 1: Create a DNS Zone in Azure

1. Log in to the Azure portal (portal.azure.com).
2. Click on the "+ Create a resource" button.
3. Navigate to “Networking” and search "DNS Zones" service.
4. Click on “Create” button and choose your subscription and resource group, name and select a “Resource group location”.
5. Click on "Review + Create" and then "Create" to create the DNS Zone.

## Step 2: Update NS Records in third party domain registrar website

1. Once your DNS Zone is created, go back to your domain registrar portal and update the NS records of the domain with the NS records shown on your recently created DNS Zone records.

Now you need to start adding the domain by logging into M365 Admin Centre. Custom Domain Name can also be added by various other methods to your tenant.

## Step 3: Add custom domain name to Microsoft 365 Admin Centre

1. Log in to Microsoft 365 Admin Centre.
2. Click on “Settings” and then the “Domains” button.
3. Click on the "+ Add domain" button.
4. Enter your domain name and click on “use this domain” button.
5. Click on “Continue” on “Connect button” tab and Microsoft will give you various records to add in the DNS Zone such as MX records, CNAME records and TXT records.

Now go back to Azure admin portal and add the following DNS records to your DNS Zone.

## Step 4: Adding DNS Records in DNS Zone

1. Click on the "+ Record set" button to add a new DNS record.
2. Enter the required information for your DNS record, such as the record type, name. IP address, TTL, etc. 
3. Click on "Ok" to create the DNS record.

Repeat this process for any additional DNS records you need to create.

## Step 5: Verify DNS Settings

1. After creating your DNS records, you need to verify that they are correctly configured.
2. Now go back to your Microsoft 365 Admin Centre window where you previously left during adding the custom domain name and click on “Continue" on “Add DNS records” window.

This will now check all the records on your DNS Zone and verifies that the domain has all the records required in the DNS Zone and add the domain successfully to the tenant. This way you can manage all your DNS records in your own Azure tenant and add the custom domain name to set up for Microsoft 365 services.