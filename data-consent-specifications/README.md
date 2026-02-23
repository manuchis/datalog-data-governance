Our consent protocol works by using three different files. The separation of files are designed to ensure privacy and control over the process. 

The three documents are the following:
- Data Sharing Consent (DSC): The DSC defines the permissions and limitations granted to third parties. The DSC is only created if the User opts for Broad Consent. If the User instead chooses Dynamic Consent, each time a Data User requests access to one of the User’s datasets, a DSR (Data Sharing Request) is generated, and a DSA (Data Sharing Agreement) is created for both parties (the User and the Data User) to review and sign.
- Data Sharing Request (DSR): The DSR specifies the information requested by a data users. This is a document that is created in order to collect the necessary information to handle the consent process. Its desirable, but is not mandatory in all the cases.
- Data Sharing Agreement (DSA): Describes how the Data User can get access to the requested datasets. Depending on the type of consent previously granted by the user (Dynamic Consent or Broad Consent), the system either automatically validates the request against the existing permissions (DSC) or prompts the user to provide new consent before creating — or rejecting — a Data Sharing Agreement (DSA).

# Dynamic and Broad Consent in the DSC
Literature on data consent discusses if, in the case of non-personal data, is necessary. Non-personal information is not regulated under GDPR, however, in some cases we want to make sure that users have control of their data. 
There is always a trade-off on requesting specific consent, because it can become a heavy workload for the data donnor. Dynamic consent could be a burden if too many requests are sent and data donnors could be desincentivised to participate in data altruism or data intermediation. 
This is why, a broad consent can be specified only for specific categories or uses. A data intermediary, then, follows the donnor's preferences, and, can decide accordingly. 

# The Agreement workflow

![DSR drawio (11)](https://github.com/user-attachments/assets/fdbb1736-f532-4f86-afa2-75eac0863104)

![DSR_temp drawio (8)](https://github.com/user-attachments/assets/d6882d46-1f80-4753-bc27-41f30fb32988)

