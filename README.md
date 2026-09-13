# Azure-Storage-Access-Control-Lab
The lab covers storage redundancy, networking, data protection, encryption, Blob Storage, Shared Access Signatures (SAS), access keys, and Microsoft Entra ID role-based access control (RBAC).
The lab covers storage redundancy, networking, data protection, encryption, Blob Storage, Shared Access Signatures (SAS), access keys, and Microsoft Entra ID role-based access control (RBAC).

Objectives

Create and configure an Azure Storage Account

Review redundancy and resiliency options

Configure storage networking

Review access tiers

Configure data protection settings

Review encryption options

Create a Blob Storage container

Upload and validate a file

Review Access Keys and Shared Access Signatures (SAS)

Use Microsoft Entra ID and Azure RBAC to control access

Validate the completed storage configuration

Technologies Used

Microsoft Azure

Azure Storage Accounts

Azure Blob Storage

Microsoft Entra ID

Azure Role-Based Access Control (RBAC)

Shared Access Signatures (SAS)

Azure Portal

Architecture

flowchart TD
    A[Administrator / User] --> B[Microsoft Entra ID]
    B --> C[Azure RBAC]
    C --> D[Azure Storage Account]
    D --> E[Blob Container]
    E --> F[Uploaded File]

Lab Steps

-- 1. Create the Storage Account

In the Azure Portal, I navigated to Storage accounts and created a new storage account.

Configuration included:

Subscription

Resource group

Unique storage account name

Azure region

Performance tier

Redundancy option

Screenshot:

<img width="632" height="667" alt="image" src="https://github.com/user-attachments/assets/3044580f-911f-495a-ac97-9ec0ec994cba" />





2. Review Storage Redundancy

I reviewed Azure Storage redundancy options to understand how data can be replicated for availability and resiliency.

Common options include:

Locally Redundant Storage (LRS)

Zone-Redundant Storage (ZRS)

Geo-Redundant Storage (GRS)

Geo-Zone-Redundant Storage (GZRS)

Screenshot: 

<img width="628" height="666" alt="image" src="https://github.com/user-attachments/assets/2f936f32-09fc-4d5b-847a-e34c3892296e" />





3. Review Advanced Storage Options

I reviewed the advanced configuration settings available for the storage account, including security-related options such as:
Secure transfer requirements

Blob public access

Minimum TLS version

Hierarchical namespace

SFTP / NFS options when available

Screenshots: 

<img width="624" height="668" alt="image" src="https://github.com/user-attachments/assets/d9597635-f519-4934-826d-659c01cbeb5f" />

<img width="632" height="673" alt="image" src="https://github.com/user-attachments/assets/2b78745e-188d-4066-bdff-6d470aff0c60" />






4. Review Access Tiers

I reviewed Azure Blob Storage access tiers and when each tier should be used.

Hot: Frequently accessed data

Cool: Infrequently accessed data

Cold / Archive: Long-term data that is rarely accessed

Screenshot: screenshots/04-access-tier.png



5. Configure Networking

I reviewed the networking configuration for the storage account.

Azure Storage can be accessed through:

Public network access

Selected virtual networks

Selected IP addresses

Private Endpoints

Restricting unnecessary public access reduces the attack surface of the storage account.

Screenshot:


<img width="631" height="660" alt="image" src="https://github.com/user-attachments/assets/38c69dc2-f814-4be7-9907-61103b588b73" />




6. Configure Data Protection

I reviewed data protection features designed to help recover deleted or modified objects.

Examples include:

Blob soft delete

Container soft delete

Blob versioning

Point-in-time restore

Screenshot: 

<img width="630" height="689" alt="image" src="https://github.com/user-attachments/assets/33903868-f952-42a8-b025-f09b92837c88" />




7. Review Encryption

Azure Storage encrypts data at rest by default.

I reviewed the available key-management options:

Microsoft-managed keys

Customer-managed keys

Screenshot:

<img width="630" height="683" alt="image" src="https://github.com/user-attachments/assets/5ab97984-59fe-4cff-8056-876b661738f8" />




8. Deploy and Verify the Storage Account

After completing the configuration, I deployed the storage account and verified the resource from the Overview page.

I confirmed items such as:

Resource group

Region

Replication type

Performance tier

Storage account status

Screenshot: 

<img width="638" height="674" alt="image" src="https://github.com/user-attachments/assets/3b57c034-f8df-4ca8-833e-c0618d9c6693" />







9. Create a Blob Container

Under Data storage > Containers, I created a Blob Storage container.

The container provides a logical location for storing unstructured objects such as documents, images, logs, and backups.

Screenshot: screenshots/09-blob-container.png



10. Upload a File

I uploaded a test file to the Blob container and verified that it appeared successfully.

Screenshot: screenshots/10-file-upload.png



11. Review Access Keys and SAS

I reviewed the authentication options available for Azure Storage.

Access Keys provide broad account-level access and must be protected carefully.

Shared Access Signatures (SAS) provide delegated access that can be restricted by:

Permissions

Services

Resource types

Start time

Expiration time

IP address

Allowed protocol

For production environments, identity-based access with Microsoft Entra ID is generally preferable when supported.

Screenshot: screenshots/11-sas-settings.png



12. Review Microsoft Entra ID and Azure RBAC

I opened Access Control (IAM) for the Storage Account and reviewed Azure roles used to control access to storage data.

Examples include:

Storage Blob Data Reader

Storage Blob Data Contributor

Storage Blob Data Owner

Azure RBAC supports least-privilege access by granting users, groups, service principals, or managed identities only the permissions they require.

Screenshot: screenshots/12-rbac.png



13. Validate Access

I validated the final configuration by confirming that the Blob container and uploaded file were accessible according to the configured permissions.

Screenshot: screenshots/13-final-validation.png



Security Concepts Demonstrated

Least privilege

Identity-based authorization

Role-Based Access Control

Secure cloud storage

Data-at-rest encryption

Network access restrictions

Data resiliency

Data recovery

Shared Access Signatures

Skills Demonstrated

Azure Storage administration

Azure Blob Storage

Microsoft Entra ID

Azure RBAC

Cloud access management

Azure networking

Data protection

Storage encryption

Cloud security fundamentals

Azure Portal administration

Key Takeaways

This lab demonstrated that Azure Storage security is built through multiple layers rather than a single setting.

Microsoft Entra ID and Azure RBAC provide identity-based authorization, while network restrictions, encryption, redundancy, and data protection features provide additional security and resiliency.

The project also reinforced the importance of limiting the use of highly privileged access methods such as storage account keys and using least-privilege access whenever possible.

Repository Structure

Azure-Storage-Access-Control-Lab/
├── README.md
├── SCREENSHOT-CHECKLIST.md
├── notes/
│   └── key-concepts.md
└── screenshots/
    ├── 01-create-storage-account.png
    ├── 02-redundancy.png
    ├── 03-advanced-options.png
    ├── 04-access-tier.png
    ├── 05-networking.png
    ├── 06-data-protection.png
    ├── 07-encryption.png
    ├── 08-storage-overview.png
    ├── 09-blob-container.png
    ├── 10-file-upload.png
    ├── 11-sas-settings.png
    ├── 12-rbac.png
    └── 13-final-validation.png

Author

Kameron Southerland

Cloud / Azure Engineering Portfolio
