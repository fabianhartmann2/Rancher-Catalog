# Jamf Pro

This template provides a high available Jamf Pro instance including provisioning the instance.

## Topology
The setup includes three Jamf Pro pods, including the Application and some logging containers. A MySQL Database pod including a container for MySQL Logging.
Two Services, one for MySQL and one for the WebApplication. The webaplication is exposed by an Ingress.

```
									 	 	    	------------
										  /  –	|JamfWebapp| – \
										 /	    ------------	  \
---------		------------	 ------------		-----------	  ------------
|Ingress| – |webapp-srv| – |JamfWebapp| –	|mysql-srv| – |mysqlserver|
---------		------------	 ------------		-----------	  ------------
									 	 \	   ------------	  	/
										  \  – |JamfWebapp| –  /
										 	  	 ------------
```
