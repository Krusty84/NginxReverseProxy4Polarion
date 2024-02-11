# NginxReverseProxy4Polarion

Example configuration of Reverse Proxy based on Nginx for Polarion. This can be useful for OSLC implementation and security.

After setting up Nginx, you need to make the following changes to **...\polarion\configuration\polarion.properties** :

** ... ... ...**

#com.siemens.polarion.previewgenerator.external.param3=$in
#com.siemens.polarion.previewgenerator.external.param4=-out
#com.siemens.polarion.previewgenerator.external.param5=$out
#com.siemens.polarion.previewgenerator.external.param6=-page
#com.siemens.polarion.previewgenerator.external.param7=1
#com.siemens.polarion.previewgenerator.external.param8=-quiet
#com.siemens.polarion.previewgenerator.external.param9=-size
#com.siemens.polarion.previewgenerator.external.param10=1600x?px

**#Start. IP address(es) of revers-proxy to Receive requests from them**

**TomcatService.request.safeListedHosts=*192.168.01.01, 192.168.01.02***

**#End. IP address(es) of revers-proxy to Receive requests from them**

***#You may add it for enabling restapi, swagger, etc.***

com.siemens.polarion.oslc.secureVault=D:\\Temp\\Polarion\\oslc
com.siemens.polarion.rest.enabled=true
com.siemens.polarion.rest.swaggerUi.enabled=true
com.siemens.polarion.rest.cors.allowedOrigins=*
com.siemens.polarion.rest.security.restApiToken.enabled=true

#End property file

Restart Polarion service (or daemon) and enjoy it
