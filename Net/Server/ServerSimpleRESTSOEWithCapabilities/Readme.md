##Simple REST SOE with capabilities

###Purpose  
The purpose of this sample is to show the capabilities of a server object extension (SOE).  This sample SOE has two subresources, busstations and trainstations, and two operations, findBusStationId and findTrainStationId. It also has two capabilities: Bus Services and Train Services. The Bus Services capability controls access to the busstations subresource and the findBusStationById operation, while the Train Services capability controls access to the trainstations subresource and the findTrainStationById operation.  


###Usage
####Using this sample  
1. Deploy the NetSimpleRESTSOEWithCapabilities.soe file to the server.   
1. Enable the SOE on a map service of your choice. Ensure that the map service has at least one feature layer and one raster layer.  
1. After the map service has started with the SOE enabled on it, open the Services Directory and access the http://<server name>:6080/arcgis/rest/services page.  
1. Click the map service on which you enabled your SOE.  
1. Scroll down and click NetSimpleRESTSOEWithCapabilities listed in the Supported Extensions section. If your REST SOE isn't listed here, log in to the Services Directory as an administrator and clear the cache. Repeat steps 3, 4, and 5 as needed.  
1. The NetSimpleRESTSOEWithCapabilities web page displays the root resource details, such as name and description, along with the Child Resources and Supported Operations sections.  
1. Click the layers subresource. It displays information about all the feature layers in JSON format.   
1. Log in to ArcGIS Manager and edit the map service on which you enabled the SOE. On the map service's editing page, click Capabilities, then click Simple REST SOE With Capabilities. A section called Operations Allowed will appear below the SOE. Check the BusServices check box. Click the Save and Restart button.  
1. Open the SOE page in the Services Directory again and click the NumberOfBusStations subresource. This subresource will display a number of bus stations, confirming this subresource is accessible.  
1. Navigate back to the SOE page and click findBusStationById. Provide text in the busStationId text box and click the findBusStationById button. The text you entered in the text box will be displayed, confirming this operation is accessible.  
1. Access the NumberOfTrainStations subresource and findTrainStationById operation. In each case, the SOE will return an error message indicating that these are inaccessible. This is because the TrainServices capability is not enabled on this SOE.  
1. Log in to ArcGIS Manager, edit the map service, select ".Net Simple REST SOE With Capabilities", and enable the TrainServices capability. Test your access to the NumberOfTrainStations subresource and findTrainStationById operation. You'll find that these are now accessible.   









---------------------------------

####Licensing  
| Development licensing | Deployment licensing | 
| :------------- | :------------- | 
|  |  |  


