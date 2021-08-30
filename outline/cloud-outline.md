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
The adoption of cloud services also adds challenges as well and one of those challenges relates to security. Cloud services operate on a “shared responsibility” model where some of the responsibility is with the cloud provider and some with the cloud consumer. In no cases should one consider the cloud to be “secure” simply because the cloud provider is “responsible for security”. The shared responsibility model can be viewed as an administration model where the cloud provider is responsible for securing the things that they have administrator access to and the consumer has responsibility for securing the things that they have administrator access to.
- both security of the cloud and security in the cloud. Security of the cloud relates to authentication and access control, including managing the keys used in the cloud as well as securely storing and operating on assets that are the “build” artifacts. Security in the cloud relates to things like automated security testing, performing static analysis of code, evaluation of software components for known vulnerabilities.

*(One Page Executive Briefing based on this section)*
- Why cloud identity?
- Cloud operating model comparison
- Links to [DCCOI Cloud Strategy Guide](https://community.max.gov/display/Egov/Agency+IT+Modernization%3A+Educational+Resources+Building+Blocks) on CIO.gov and [Cloud Smart Strategy](https://cloud.cio.gov/strategy/)
- Explanation of how Cloud Identity encompasses extending on-prem identities to cloud identity providers and manages the ICAM process in XaaS
- Graphic that shows cloud management model for ICAM.
- Graphi that shows modern cloud access. traditional vs modern access. basic diagram of vpn to agency and then device to cloud and cloud to cloud communication.
- Primary advantage to cloud services is moving from a capex to opex budget model. Capital Expenses include buying the resources to anticipate demand. More upfront cost in buying equipment and labor cost in configuration and operations. Operational Expense converts to more of a demand model where you pay for infrastructure based on real-time consumption rather than anticipating consumption.
- Monitor activity in real-time and at rest.

| Challenge | Governance | Risk Management | Vendor Capability | Workforce Capability |
| --------- | :--------: | :-------------: | :---------------: | :------------------: |
| The product I want is not fedramped. |  | X |  |  |
| I can't find experienced people or training |  |  |  | X |

## Journey Steps

### Gain Support  
1. Highlight outcomes in user stories. Explain in simple terms what and how operations will improve. Cloud presents a different engagement model. Now, the focus lies on business and mission products: how can ICAM enable business owners to articulate what they seek to accomplish with a cloud service? Single Sign-On (SSO) is an important concept to cloud. It helps aggregate how users access cloud services, but also why they access cloud services. In the past, on-prem ICAM was mainly concerned with how employees and contractors behaved within a trusted perimeter. Cloud presents a different engagement model. Now, the focus lies on business and mission products: how can ICAM enable business owners to articulate what they seek to accomplish with a cloud service? Additionally, is a business owner responsible for specifying access policies to a cloud service and how sensitive its data is?
2. Identify what is success and set metrics based on operational challenges (e.g. length of time to deprovision account, # of orphaned accounts, length of time to reset password, # of roles under management, # of applications integrated, # of identity manual identity processes, # of manual processes automated). Track metrics by operations efficiency (how you're improving) and operational volume (size of transactions). Align this back to federal policy and agency mission objectives. Examples may include
    - Audit and compliance performance
    - Cost savings or diversion
    - Operational improvements (fewer manual tasks, faster review cycles, faster identity processes).
    - Support federal mandate (e.g. Zero Trust, Cloud Smart)
6. **Define cloud identity strategy and goals**
   1. *Prevent capability sprawl* - *Identify how to consolidate identity services* Example of contained environments and federating between. On-prem to cloud, cloud-to-cloud.
   2. Most of the agencies may have some sort of Identity and Access Management system already in place. Moving to the cloud there are options for agencies to evaluate. Move the Identity and Access Management system to the cloud and continue with the service that the agency already supports. 
   3. Agencies can look at the SaaS providers that offer Identity services like Authentication and Federation, Identity Store to take advantage of the capabilities that come with the offerings the vendors provide.
   4. Agencies need to consider if they would like to keep the Identity store within their network boundary whether it is on-prem or in their private cloud.
   5. The other option is they can adapt to the SaaS provider offerings and store the identity in their cloud hosting.
   6. Scope of strategy should include people and various categories of non-people including elements of devops (secrets, api, tokens).
   7. Factor in various authenticators based on the platform and use case.
4. **Develop department policy** 
    1. Exclusively using cloud services may not be the ultimate solution for everything. Most agencies are either all on-prem or extend some identity services to a cloud provider. Journey should start with assumption of all on-prem.
    2. Include multi-cloud considerations
    3. Include NPE - Bullet from Ross (CISA) on CDM and NPE or CDM/PAM and NPE.
    4. How does PIV fit with Cloud IAM.
5. **Draft a business case including funding consideration**
7. - **Zero Trust Alignment** - ICAM capabilities to support zero trust and intersection with cloud. Potential call-out to TIC and CASB. NIST 800-207 page 9 graphic with ICAM callouts

### Plan Journey

The first step in any journey is identifying the desitination. Your agency can take an incremental approach and identify single services or a complete migration with incremental steps. The ICAM Practice Areas and Services Framework is a great starting point to map business requirements to technical solutions.

[![Five boxes that each correspond to a FICAM practice area or supporting element. Each box lists the agency services that correspond to that area. You can find the services and definitions in the following pages.](../../assets/ficamservices.png)](../../assets/arch/services/ServicesOverview.png){:target="_blank"}{:rel="noopener noreferrer"}

1. **Identify a capability to extend**
   1. *Representative architecture*
   2. Link to FedRAMP and key terms to search.
   3. *Leveraging Single Sign-on (SSO) capabilities* - SSO is usually part of the first step to extend your on-prem ICAM services to a cloud provider.
   4. Written in reference to ICAM services framework.
2. **Security Analysis**
   1. *Enterprise-wide capabilities* - Not all SaaS are "enterprise-ready," meaning they may not support audit logs and modern authentication using OAuth or Open ID Connect.
   2. *Additional web traffic monitoring* - Per TIC, traffic must be monitored and analyzed for malicious activity. This may mean increasing VPN usage for on network monitoring, acquiring a cloud monitoring solution such as a Cloud Access Security Broker or Secure Access Service Edge solution for off-network monitoring, and potentially additional Security Information and Event Management storage for the increased traffic.

**CLoud Myth** On-prem operating model more secure than cloud (Debunked by Zero Trust)* - Alex (Treasury) to provide an example/bullet.

### Architecture Considerations  
- Call out DIRA to identity NIST levels.
1. **Identity Management**
   1. *Entitlement Management* - Sometimes referred to as Identity Governance, it can be more complex in IaaS and PaaS than with on-prem. Plan for this and the use of tools which leverage entitlement management protocols such as [System for Cross-domain Identity Management (SCIM)](http://www.simplecloud.info/) to sync information between your directory and applications.
   2. *Provisioning and Deprovisioning* - Just because a user is removed from a directory or SSO, that account may still exist in the XaaS. Leverage automated lifecycle management processes that enable lifecycle management simultaneously or a manual workflow integrated with an ITSM to track and audit processes.
   3. *Budgeting Quick Tip* - Most identity products are priced by user, number of authentications, number of integrated applications, or per application connector. Factor this into your budget.
   4. Critical to conduct an on-prem directory clean-up. 
   5. Use of virtual directories
   6. *Enforcing least privilege* - Understanding full access of a role within IaaS/PaaS
   7. Call out for NPE identity management. RPA, service accounts.
   8. *Enforcing identity governance* - Mapping users to roles/lifecycle management

Call out - Manage permissions by group rather than individual. Base groups on roles such as government admin, contractor admin, contribruter, or reader. All users in a group inherit those permissions.

Challenge Governance - Enforcing Least Privilege - Least privilege is granting only the privileges necessary to perform a task. For example, if someone is assigned responsibility to manage user passwords they should not be assigned a role that also manages resources. This may require some testing to determine the appropriate mix of privileges to complete a task. Gather 30 days of admin activity to analyze what permissions are necessary and then create a role or group-based on that group. 

2. **Credential Management**
   1. Use the best authenticator for the use case
   2. NPE credentialling. Service account password. Agenices should make a risk decision about managing non-person credentials including if, how, and when to enforce for stringent controls. Digital playbook contains a risk assessment framework for digital workers. PAM solutions operate by managing secrets and these secrets must be stored securely. Secrets can be passwords but can also be tokens or x.509 certificates and the best PAM solutions can manage all types. Secrets should be available when validly requested and approved, and this may include nonhuman (API) requests for secret upon access requests to a target system. The secrets must be rotated regularly to reduce the period an attacker who has acquired a secret can operate. Some secrets are ephemeral in nature and expire automatically. All secrets should be revocable so that they can ensure they can’t be used after an attack on the secret is discovered.
   3. Cloud allows for a greater variety of authenticators and protocols which aren't supported by legacy ICAM access tools. WebAuthN, FIDO authenticators, and one-time pin applications.
   4. Password (otherwise known as memorized secrets) use is inevidatble. Follow NIST guidelines for passwords:
      1. Should be an alphanumeric between 8 - 64 characters
      2. Shall be checked against breach corpuses, dictionary words, repetive characters, or context-specific and denied
      3. Should offer a password strength meter
      4. Shall limit the number of failed attempts before a lock-out or require a password reset.
      5. Should not require periodic password updates.
      6. Should be used as part of a multi-factor authenticator
      7. Should support the use of a password manager through allowing a cut-and-paste function

Call-out - Rotate access keys and not passwords - NIST recommends not to require password rotation. Programmatic access keys should be rotated and not embedded in unencrypted code. Where keys and secrets are used, consider using a secrets management tool.

Call out - do not share credentials - Credentials should be assigned on an individual basis and not shared. This could be a username and password, an access key, an API token, or other authenticator form. 

4. **Access Management**
   1. *User Access to XaaS* - Users must be able to reach the XaaS. This means creating network paths for users coming from an agency network (direct or through VPN), but also potentially for users not on an agency network. "Use Case - Gmail is accessible off-network but requires SSO which is only accessible on network".
   2. *Protocols* - Access comes in many protocols. Monitor access attempts over all possible protocols such as https and ssh. Also, factor in the use of port translation technology.
   3. *Federation*
   4. Prevent access to personal instances.
   5. RBAC
   6. Admin portals may be secured differenlty for COOP. Break glass admin accounts. Not linked to an individual and uses MFA that is different form other methods.
   7. Device health as attribute.
   8. Proxies
   9. Budget tip: Leverage DIRA to determine number of users, applications, and authentication volume. These are important metrics to determine a cost for cloud services. Most identity cloud services are based on these three metrics.
   10. Cloud embeds access based on policies that are machine-readable and executable. Everything a user does in the cloud is policy based.
   11. Call out - Useful skills - A majority of cloud ICAM patterns are based-on open protocols such as JSON, SCIM, oAuth, SAML, open policy agent (OPA) and Open ID Connect. Good workforce training to become familiar with these protocols.
   12. Enable MFA

call out - Determine your access policy based on user type - By conducting a DIRA, Application owners can determine ideal conditions for access such as during working hours, from the United States, on a GFE or approved device. By analying ideal access conditions, access policies and exceptions are identified and implemented or tracked through access tools and audit logs.

5. **Governance**
   1. Policies to monitor for configuration changes. Controls to prevent misconfiguration (e.g. default private).
   2. Training admins on existing policies and when policies change.
   3. Monitor activity - Enable activity logging for privileged users and all users if possible.

- Any change to the user experience should come with communication and potentially training.

### Test and Deploy
While also relatively new category with Puppet and Chef leading the way and Ansible a newer entrant. Puppet and Chef both use a RubyDSL (domain-specific language) whereas Ansible and others in the field, such as CircleCI support YAML (Yet Another Markup Language). Increasingly the tools in the category are expanding into being able to manage the entire environment in cloud use cases. This increased use of code to configure infrastructure places a greater demand on ensuring that the secrets that are used in these environments (passwords, service account credentials, tokens and ssh keys) are well managed. PAM tools can provide several mechanisms to help in this regard but there may be then need for other tools, specifically Certificate Management tools and API management tools that will be necessary as configuration of cloud environments becomes more highly automated. The total code and configuration needs to be packaged as a configuration item so that the entire content of a delivery can be known and tracked in operation.
1. **Plan a Pilot**
   1. *Document a manual process*
   2. *Identify how to automate it*

  ***Additional Sub-sections needed***
  1. Document existing process
  2. Review process workflow
  3. Identify challenge / pain point
  4. Update workflow with desired outcome
  5. Implement workflow

### Deploy
  ***Sub-sections needed***

## Policies, Standards, and Guidance
### Policies
1. [Executive Order 14028 - Improving the Nation's Cybersecurity](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity)
2. [Federal Cloud Computing Strategy](https://cloud.cio.gov/)
3. [OMB Memo 19-17](https://www.whitehouse.gov/wp-content/uploads/2019/05/M-19-17.pdf)
4. FICAM Governance Framework *(not yet published)*

### Standards
1. [NIST Special Publication 800-63 - Digital Identity Guidelines](https://csrc.nist.gov/publication/detail/sp/800-63/final)
2. [NIST Special Publication 800-145 - NIST Definition of Cloud Computing](https://csrc.nist.gov/publications/detail/sp/800-145/final)
3. [NIST Special Publication 800-207 - Zero Trust Architecture](https://csrc.nist.gov/publications/detail/sp/800-207/final)
4. [NIST Special Publication 800-210 - General Access Control Guidance for Cloud Systems](https://csrc.nist.gov/publications/detail/sp/800-210/final)

### Guidance
1. [Digital Identity Risk Assessment Playbook](https://playbooks.idmanagement.gov/docs/playbook-dira.pdf)
2. [FedRAMP Digital Identity Requirements (Version 1.0)](https://s3.amazonaws.com/sitesusa/wp-content/uploads/var/www/html/sites/www/app/wordpress/wp-content/blogs.dir/482/files/2016/06/FedRAMP_Digital_Identity_Requirements_v1.0.pdf)
3. [ICAM Program Management Playbook](https://playbooks.idmanagement.gov/pm/)
4. [General Services Administration - Cloud Information Center](https://cic.gsa.gov/acquisitions/pricing)
5. [NIST Interagency Report 8335 - Identity as a Service for Public Safety](https://csrc.nist.gov/publications/detail/nistir/8335/draft)
6. [National Security Agency Cybersecurity Information Sheet - Mitigating Cloud Vulnerabilities](https://media.defense.gov/2020/Jan/22/2002237484/-1/-1/0/CSI-MITIGATING-CLOUD-VULNERABILITIES_20200121.PDF)
7. [Single Sign-On Playbook](https://playbooks.idmanagement.gov/docs/playbook-sso.pdf)

## Examples and Templates
  ***Examples and Templates needed***
  - AWS policy to require MFA

