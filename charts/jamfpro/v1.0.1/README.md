# Jamf Pro

This template provides a high available Jamf Pro instance including provisioning the instance.

## Topology
The setup includes three Jamf Pro pods, including an application and some logging containers. A MySQL Database pod including a container for MySQL Logging.
Two Services, one for MySQL and one for the WebApplication. The webapplication is exposed by an Ingress.

After a sucessfull deployment, the instance will be provisioned. This includes:

 - Activate the License
 - Create an Administrator Account
 - Setup Cluster mode
 - Set Master Node

The name of the instance is used to build the public available FQDN. <INSTANCE NAME>.jamf.dq.solutions

All nessesary configuration parameters are available as rancher questions down bellow.