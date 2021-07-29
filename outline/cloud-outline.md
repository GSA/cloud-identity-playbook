# Cloud Identity Playbook

This playbook is designed to assist federal agencies as they either **start to or expand the use of Identity, Credential, and Access Management Services in a cloud operationg model**. While each agency should tailor it's Cloud Identity implementation to their agency's current and desired outcome, this playbook **offers guidance and lessons learned** from Cloud Identity Working Group of the Federal CIO Council Identity, Credential, and Access Management Subcommittee in collaboration with the General Services Administration (GSA) Data Center and Cloud Optimization Initiative (DCCOI).

This playbooks contains both a cloud identity 101 and a journey map used by agencies to **identify, plan, and implement cloud-operated ICAM services**.

## Executive Summary
About a page that summarizes the playbook.
#SaaS Bullets from Bala:
SaaS for Cloud Identity:

Most of the agencies may have some sort of Identity and Access Management system already in place.  Moving to the cloud there are options for agencies to evaluate.

  1. Move the Identity and Access Management system to the cloud and continue with the service that agency already support.

  2. Agencies can look at the SaaS providers that offer Identity services like Authentication and Federation, Identity Store to take advantage of the capabilities that comes with the offerings the vendors provide.
    a. Agencies need to consider if they would like to keep the Identity store within their network boundary whether it is on-prem or in their private cloud.
    b. The other option is they can adopt to the SaaS provider offerings and store the identity in their cloud hosting.

### Key Terms
- **Cloud Identity** - Broad term to define activities that extend on-premise identity services to a cloud provider and also identity processes in cloud operated services.
- **Cloud Computing** - A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.
- **Cloud Service Model** - A Cloud Service Provider service model that includes Software as a Service (SaaS), Platform as a Service (PaaS), Infrastructure as a Service (IaaS).
- **Identity as a Service** - Industry term for Software-as-a-Service providers of ICAM services.

### Audience
This playbook is written for Agency ICAM Program Managers as the primary audience. The below table lists secondary audience members and how to engage them with this playbook.

| Stakeholder | Stakeholder Type | Engagement Point |
| ----------- | ---------------- | ---------------- |
| ICAM Steering Committee | Agency Governance Group | The enterprise should govern all agency identities to reduce cyber risk. |
| Business Line Program Managers | Interested Party | Create a unified user experience by leveraging existing enterprise ICAM services. |
| Cloud Management Office | Office | Integrate your identity processes with existing enterprise ICAM services. |
| Security Management Office | Office | Generate a holistic view of security activities and events across platforms and environments. |
| DevOps Office | Office | Secure and automate DevOps identities. |

### Disclaimer
This playbook was developed by the Cloud Identity Working Group of the Federal CISO Council Identity, Credential, and Access Management subcomittee in collaboration with the GSA Data Center and Cloud Optimization Initiative (DCCOI). This playbook is meant to help U.S. Federal Executive Branch agenices understand and plan use of cloud infrastructure as it relates to the [FICAM Architecture Services Framework](https://playbooks.idmanagement.gov/arch/services/). This playbook is not official policy or mandated action and does not provide authoritative information technology terms. This playbook includes best practices to supplement existing federal policies and builds upon [Executive Order 14028](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity) and [Office Management and Budget Memorandum 19-17](https://www.bing.com/search?q=omb+memo+19-17&cvid=d6a3d59cfc214bc383193a26f643e239&aqs=edge.0.69i59j0.1774j0j4&FORM=ANAB01&PC=U531), as well as existing federal identity guidance and playbook. Subject areas with intersecting scope, such as cloud operating models, Federal Risk and Authorization Management Program (FedRAMP) and enterprise governance, are considered only to the extent that they relate to either operating FICAM services or performing FICAM processes in a cloud operating model.

## Cloud Identity 101 (Create an Exec-Style One-Pager from this section)
- [ ] Cloud operating model comparison
- [ ] Link to DCCOI Cloud Strategy Guide on CIO.gov and Cloud Smart Strategy
- [ ] Cloud Identity encompasses extending on-premise idenities to cloud identity providers and managing ICAM process in XaaS.

## Cloud Identity Journey
Use themes/callouts.  
  - Zero Trust Alignment
  - Challenges aligned with Governance, Risk Management, Vendor Capability, Team/Workforce Capability
    - Enforcing identity governance - Mapping users to roles/lifecycle management.
    - Enforcing least privilege - Understanding full access of a role within IaaS/PaaS.
  - Cloud Myths
     - More secure on-prem = Zero Trust debunked this

**MVP Content**
- [ ] Define cloud integration journey. Using cloud services may not be ultimate solution for everything. Most agenices are either all on-premise or extended some identity services to a cloud provider. Journey should start all on-premise.
- [ ] Include use of virtual directories.
- [ ] Include multi-cloud considerations.
- [ ] Identify how to consolidate identity services.
- [ ] Secondary Content - Non-person entity interaction and use.

## Journey Steps

### Gain Support  

  a. Develop department policy
  
  b. Draft a business case including funding consideration.
  
  c. Define cloud identity strategy. Prevent capability sprawl.

### Plan Journey

  a. Identify a capability to extend.
  - [ ] Representative architecture
  - [ ] Table of FedRAMP identity vendors.
  - [ ] SSO is usually for the first step to extend your on-premise ICAM services to a cloud provider.
  
  b. Security Analysis
- [ ] Not all SaaS are "enterprise-ready" meaning they may not support audit logs and modern authentication using OAuth or Open ID Connect.
- [ ] Per TIC, traffic must be monitored and analyzed for malicious activity. This may mean increasing VPN usage for on network monitoring, acquiring a cloud monitoring solution such as a Cloud Access Security Broker or Secure Access Service Edge solution for off-network monitoring, and potentially additional Security Information and Event Management storage for the increased traffic.

### Architecture Considerations  

  a. Identity Management
  - [ ] Entitlement Management (sometimes referred to as Identity Governance) can be more complex in IaaS and PaaS than with on-premise. Plan for this and the use of tools which leverage entitlement management protocols such as [System for Cross-domain Identity Management (SCIM)](http://www.simplecloud.info/) to sync information between your directory and applications.
  - [ ] Provisioning and Deprovisioning - Just because a user is removed from a directory or single sign-on, that account may still exist in the XaaS. Leverage automated lifecycle management processes that enable lifecycle management simultaneously or a manual workflow integrated with an ITSM to track and audit processes.
  - [ ] Quick Tip - Most identity products price by user, # of authentications, # of integrated applications, or per application connector. Factor this into your budget.
  b. Credential Management
  
  c. Access Management
  - [ ] Users must be able to reach the XaaS. This means creating network paths for users coming from an agency network (direct or through VPN), but also potentially for users not on an agency network. "Use Case - Gmail is accessible off-network but requires Single Sign-On which is only accessible on network".
  - [ ] Access comes in many protocols. Monitor access attempts over all possible protocols such as https and ssh. Also, factor in the use of port translation technology.
  - [ ] Consider federation.
  
  d. Governance

### Test  

  a. ?

### Deploy  

  a. ?

## Policies, Standards, and Guidance
### Policies
1. [Executive Order 14028 - Improving the Nation's Cybersecurity](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity)
2. [Federal Cloud Computing Strategy](https://cloud.cio.gov/)
3. [OMB Memo 19-17](https://www.whitehouse.gov/wp-content/uploads/2019/05/M-19-17.pdf)
4. FICAM Governance Framework

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
?

