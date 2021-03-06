# Opsgenie Cloudformation Integration



## Supported Resources


*Link to documentation*
 
- Opsgenie User

  
- Opsgenie Team


- Opsgenie Integration



## Installation

### Install from S3


- Opsgenie User resource
```
aws cloudformation register-type \
--region us-west-2 \
--type-name "Atlassian::Opsgenie::User" \
--schema-handler-package "s3://opsgeniedownloads/cloudformation/atlassian-opsgenie-user.zip" \
--type RESOURCE
```

- Opsgenie Team resource
```
aws cloudformation register-type \
--region us-west-2 \
--type-name "Atlassian::Opsgenie::Team" \
--schema-handler-package "s3://opsgeniedownloads/cloudformation/atlassian-opsgenie-team.zip" \
--type RESOURCE
```


- Opsgenie Integration resource
```
aws cloudformation register-type \
--region us-west-2 \
--type-name "Atlassian::Opsgenie::Integration" \
--schema-handler-package "s3://opsgeniedownloads/cloudformation/atlassian-opsgenie-integration.zip" \
--type RESOURCE
```


### Install using cfn-cli

- clone this repo

- navigate to desired resource (such as /opsgenie_user)

- run `cfn-cli submit` command 
