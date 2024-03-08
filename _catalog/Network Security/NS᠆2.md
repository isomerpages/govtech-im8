---
title: NS᠆2
permalink: /catalog/ns/ns-2/
variant: markdown
description: ""
third_nav_title: Network Security
---
# NS-2: Access Restrictions on CSP Resources Outside Virtual Network

* **Group:** [Network Security](/catalog/ns)

## Control Statement

Restrict access to CSP resources outside of a virtual network (e.g., Lambda, DynamoDb, API Gateways, S3, CloudFront) using access controls or application layer authorisation.

## Control Recommendations

Apply access restrictions appropriate to the resource type. Access through interface VPC endpoints is only required if the client is hosted in a private subnet. For example:

* Restrict access to DynamoDB with IAM policies.

* Restrict access to API Gateway with Lambda Authorizers or authorisation middlewares at the application layer. If the API Gateway is exposed to private subnets, create a [private API](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-private-apis.html).

* Restrict access to S3 Buckets with IAM policies and block public access from the internet.

## Risk Statement

Lack of access restrictions raises the risk of unauthorised access, data exposure, and potential misuse of critical services, compromising the overall security posture.



### References


 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S2](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.5/S5](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)
 * [IM8 Cloud Security (IaaS and PaaS): 1.7/S23](https://intranet.mof.gov.sg/portal/IM/Themes/IT-Management/Cloud/Topics/Cloud-Security.aspx)