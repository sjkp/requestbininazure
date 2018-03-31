# Requestbin On Azure Container Instances

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsjkp%2Frequestbininazure%2Fmaster%2Fazuredeploy.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>

This repository contains a self-hosted version of requestbin, that run on Azure Container Instances. 

Requestbin was a great web site, that could be used for recording http request when building and using web hooks. 

Unfortunately requestb.in which was the hosted version of the site, have been closed due to abuse. This Azure ARM template 
allows you to run your own version of the site in Azure. Spinning up a site takes a couple of minutes, and it can be deleted in seconds 
when no longer needed. 

Running the request bin site on Azure have the following costs associated with its resources

* Azure Function (Dynamic Plan) - Pay Per Use
* Azure Container Instance 1 CPU / 1 GB Ram for the requestbin web site 
* Azure Container Instance 1 CPU / 1 GB Ram for thr redis cache 
* Total cost ~ 3 $ / day 

In other words don't let it run 24x7 if you want to do that you are better off installing it in a VM or on Kubernetes. 

<b>After deploying you can find your requestbin site at the ipaddress found under the container group in the resource group used when deploying</b>
