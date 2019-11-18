# Opsgenie Integration

## Atlassian::Opsgenie::Integration

Allows creation of an Opsgenie Integration which is then associated with a team.<br>
This integration allows Opsgenie's incident management capabilities to your third-party tools used in your technology stack.

## Fields

| Property                 	| Description                                                                                                                                                                                                         	| Required 	| Limit                                                                                                                                                       	|
|--------------------------	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|----------	|-------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| OpsgenieApiKey           	| Your Opsgenie provided API Key                                                                                                                                                                                      	| Required 	|                                                                                                                                                             	|
| OpsgenieApiEndpoint      	| Endpoint of API according to your preferred environment                                                                                                                                                             	| Required 	| api.eu.opsgenie.com, api.opsgenie.com                                                                                                                       	|
| Enabled                  	| This parameter is for specifying whether the integration will be enabled or not. Defaults to true                                                                                                                   	| Required 	| Boolean value defaults to true.                                                                                                                             	|
| Name                     	| Name of the integration                                                                                                                                                                                             	| Required 	| Name must be unique for each integration.                                                                                                                   	|
| IntegrationType          	| The API integration supported tool that is to be created. List of integrations on Opsgenie's,Integrations page                                                                                                      	| Optional 	| Can only create API integrations. Please filter by API in the list of integrations shown in your Opsgenie console to know which integrations are supported. 	|
| OwnerTeamId              	| The identifier of the team associated with the integration.                                                                                                                                                         	| Required 	|                                                                                                                                                             	|
| OwnerTeamName            	| The name of the team associated with the integration.                                                                                                                                                               	| Optional 	|                                                                                                                                                             	|
| AllowReadAccess          	| This parameter is for configuring the read access of integration. If read access is restricted, the integration will not be authorized to read within any domain.                                                   	| Optional 	| Boolean value defaults to true.                                                                                                                             	|
| AllowWriteAccess         	| This parameter is for configuring the write access of integration. If write access is restricted, the integration will not be authorized to write within any domain.                                                	| Optional 	| Boolean value defaults to true.                                                                                                                             	|
| AllowDeleteAccess        	| This parameter is for configuring the delete access of integration. If delete access is restricted, the integration will not be authorized to delete within any domain.                                             	| Optional 	| Boolean value defaults to true.                                                                                                                             	|
| AllowConfigurationAccess 	| This parameter is for allowing or restricting the configuration access. If configuration access is restricted, the integration will be limited to Alert API requests, Incident API requests and sending heartbeats. 	| Optional 	| Boolean value defaults to true.                                                                                                                             	|
| Responders               	| Optional user, schedule, teams or escalation names to calculate which users will receive the notifications of the alert. Responders which are exceeding the limit are ignored.                                      	| Optional 	|                                                                                                                                                             	|

- Responder property

| Property 	| Description                                                                                 	| Required 	| Limit                                            	|
|----------	|---------------------------------------------------------------------------------------------	|----------	|--------------------------------------------------	|
| Type     	| The responder entity associated with the integration's alerts.                              	| Required 	| Limited to one of the following:ScheduleTeamUser 	|
| Name     	| Name of the schedule or team acting as responder to the alerts generated by the integration 	| Required 	|                                                  	|
| Username 	| Name of the user acting as responder to the alerts generated by the integration             	| Required 	|                                                  	|