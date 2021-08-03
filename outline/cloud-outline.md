# Cloud Identity Playbook

This playbook is designed to assist federal agencies as they either **start to or expand the use of Identity, Credential, and Access Management (ICAM) Services in a cloud operating model**. While each agency should tailor it's Cloud Identity implementation to their agency's current and desired outcome, this playbook **offers guidance and lessons learned** from the Cloud Identity Working Group of the Federal Chief Information Officer (CIO) Council’s Identity, Credential, and Access Management Subcommittee (ICAMSC) in collaboration with the General Services Administration (GSA) Data Center and Cloud Optimization Initiative (DCCOI).

This playbook contains both a Cloud Identity 101 Executive Briefing and a journey map to be used by agencies to **identify, plan, and implement cloud-operated ICAM services**.

## Executive Summary
About a page that summarizes the playbook.

### Key Terms
- **Cloud Identity** - Broad term to define activities that extend on-prem identity services to a cloud provider as well as identity processes in cloud operated services.
- **Cloud Computing** - A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.
- **Cloud Service Model** - A Cloud Service Provider service model that includes Software as a Service (SaaS), Platform as a Service (PaaS), Infrastructure as a Service (IaaS).
- **Identity as a Service** - Industry term for SaaS providers of ICAM services.

### Audience
This playbook is written for Agency ICAM Program Managers as the primary audience. The below table lists secondary audience members and how to engage them with this playbook.

| **Stakeholder** | **Stakeholder Type** | **Engagement Point** |
| ----------- | ---------------- | ---------------- |
| *ICAM Steering Committee* | Agency Governance Group | The enterprise should govern all agency identities to reduce cyber risk. |
| *Business Line Program Managers* | Interested Party | Create a unified user experience by leveraging existing enterprise ICAM services. |
| *Cloud Management Office* | Office | Integrate your identity processes with existing enterprise ICAM services. |
| *Security Management Office* | Office | Generate a holistic view of security activities and events across platforms and environments. |
| *DevOps Office* | Office | Secure and automate DevOps identities. |

### Disclaimer
This playbook was developed by the Cloud Identity Working Group of the Federal Chief Information Security Officer (CISO) Council's ICAMSC in collaboration with the GSA's DCCOI. This playbook is meant to help U.S. Federal Executive Branch agencies understand and plan use of cloud infrastructure as it relates to the [FICAM Architecture Services Framework](https://playbooks.idmanagement.gov/arch/services/). This playbook is not official policy or mandated action and does not provide authoritative information technology terms. This playbook includes best practices to supplement existing federal policies and builds upon [Executive Order 14028](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity) and [Office Management and Budget Memorandum 19-17](https://www.bing.com/search?q=omb+memo+19-17&cvid=d6a3d59cfc214bc383193a26f643e239&aqs=edge.0.69i59j0.1774j0j4&FORM=ANAB01&PC=U531), as well as existing federal identity guidance and playbook. Subject areas with intersecting scope, such as cloud operating models, Federal Risk and Authorization Management Program (FedRAMP) and enterprise governance, are considered only to the extent that they relate to either operating FICAM services or performing FICAM processes in a cloud operating model.

## Cloud Identity 101 
*(One Page Executive Briefing based on this section)*
- Cloud operating model comparison
- Links to [DCCOI Cloud Strategy Guide](https://community.max.gov/display/Egov/Agency+IT+Modernization%3A+Educational+Resources+Building+Blocks) on CIO.gov and [Cloud Smart Strategy](https://cloud.cio.gov/strategy/)
- Explanation of how Cloud Identity encompasses extending on-prem identities to cloud identity providers and manages the ICAM process in XaaS

## Cloud Identity Journey (Holistic Concepts)
### Use themes/callouts.  
- **Zero Trust Alignment**
- **Challenges aligned with Governance, Risk Management, Vendor Capability, Team/Workforce Capability**
  - *Enforcing identity governance* - Mapping users to roles/lifecycle management
  - *Enforcing least privilege* - Understanding full access of a role within IaaS/PaaS
- **Cloud Myths**
  - *On-prem operating model more secure than cloud (Debunked by Zero Trust)*

### Minimum Viable Product (MVP) Content
- **Define cloud integration journey**: Exclusively using cloud services may not be the ultimate solution for everything. Most agencies are either all on-prem or extend some identity services to a cloud provider. Journey should start with assumption of all on-prem.
- **Include use of virtual directories**
- **Include multi-cloud considerations**
- **Identify how to consolidate identity services**
- **Secondary Content** e.g., non-person entity (NPE) interaction and use

## Journey Steps

### Gain Support  
1. **Develop department policy**
2. **Draft a business case including funding consideration**
3. **Define cloud identity strategy**
   1. *Prevent capability sprawl*

### Plan Journey
1. **Identify a capability to extend**
   1. *Representative architecture*
   2. *Table of FedRAMP identity vendors*
   3. *Leveraging Single Sign-on (SSO) capabilities* - SSO is usually part of the first step to extend your on-prem ICAM services to a cloud provider.
2. **Security Analysis**
   1. *Enterprise-wide capabilities* - Not all SaaS are "enterprise-ready," meaning they may not support audit logs and modern authentication using OAuth or Open ID Connect.
   2. *Additional web traffic monitoring* - Per TIC, traffic must be monitored and analyzed for malicious activity. This may mean increasing VPN usage for on network monitoring, acquiring a cloud monitoring solution such as a Cloud Access Security Broker or Secure Access Service Edge solution for off-network monitoring, and potentially additional Security Information and Event Management storage for the increased traffic.

### Architecture Considerations  
1. **Identity Management**
   1. *Entitlement Management* - Sometimes referred to as Identity Governance, it can be more complex in IaaS and PaaS than with on-prem. Plan for this and the use of tools which leverage entitlement management protocols such as [System for Cross-domain Identity Management (SCIM)](http://www.simplecloud.info/) to sync information between your directory and applications.
   2. *Provisioning and Deprovisioning* - Just because a user is removed from a directory or SSO, that account may still exist in the XaaS. Leverage automated lifecycle management processes that enable lifecycle management simultaneously or a manual workflow integrated with an ITSM to track and audit processes.
   3. *Budgeting Quick Tip* - Most identity products are priced by user, number of authentications, number of integrated applications, or per application connector. Factor this into your budget.
2. **Credential Management**
3. **Access Management**
   1. *User Access to XaaS* - Users must be able to reach the XaaS. This means creating network paths for users coming from an agency network (direct or through VPN), but also potentially for users not on an agency network. "Use Case - Gmail is accessible off-network but requires SSO which is only accessible on network".
   2. *Protocols* - Access comes in many protocols. Monitor access attempts over all possible protocols such as https and ssh. Also, factor in the use of port translation technology.
   3. *Federation*
4. **Governance**

### Test  
1. **Plan a Pilot**
   1. *Document a manual process*
   2. *Identify how to automate it*

  ***Additional Sub-sections needed***

### Deploy  
  ***Sub-sections needed***

## Policies, Standards, and Guidance
### Policies
1. [Executive Order 14028 - Improving the Nation's Cybersecurity](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity)
2. [Federal Cloud Computing Strategy](https://cloud.cio.gov/)
3. [OMB Memo 19-17](https://www.whitehouse.gov/wp-content/uploads/2019/05/M-19-17.pdf)
4. FICAM Governance Framework *(not yet published)*

### Standards
1. [NIST Special Publication 800-145 - NIST Definition of Cloud Computing](https://csrc.nist.gov/publications/detail/sp/800-145/final)
2. [NIST Special Publication 800-207 - Zero Trust Architecture](https://csrc.nist.gov/publications/detail/sp/800-207/final)
3. [NIST Special Publication 800-210 - General Access Control Guidance for Cloud Systems](https://csrc.nist.gov/publications/detail/sp/800-210/final)

### Guidance
1. [Digital Identity Risk Assessment Playbook](https://playbooks.idmanagement.gov/docs/playbook-dira.pdf)
2. [FedRAMP Digital Identity Requirements (Version 1.0)](https://s3.amazonaws.com/sitesusa/wp-content/uploads/var/www/html/sites/www/app/wordpress/wp-content/blogs.dir/482/files/2016/06/FedRAMP_Digital_Identity_Requirements_v1.0.pdf)
3. [ICAM Program Management Playbook](https://playbooks.idmanagement.gov/pm/)
4. [General Services Administration - Cloud Information Center](https://cic.gsa.gov/acquisitions/pricing)
5. [NIST Interagency Report 8335 - Identity as a Service for Public Safety](https://csrc.nist.gov/publications/detail/nistir/8335/draft)
6. [National Security Agency Cybersecurity Information Sheet - Mitigation Cloud Vulnerabilities](https://media.defense.gov/2020/Jan/22/2002237484/-1/-1/0/CSI-MITIGATING-CLOUD-VULNERABILITIES_20200121.PDF)
7. [Single Sign-On Playbook](https://playbooks.idmanagement.gov/docs/playbook-sso.pdf)

## Examples and Templates
  ***Examples and Templates needed***

