The project is an implementation of a Web Service to provide the list of currently week nightlife events in United Kingdom, geolocated from postcode, within a chosen search radius area (expressed in Km). Detailed information can be found [here](https://drive.google.com/file/d/1ipDawFD93zCwDzfc2OdotbiCFsWiTWgg/view).

### Source code guide

A brief description of the files/folders listed above:
  * *UK_Nightlife-BPMN.bpm* file containing the modeled BPMN of the project; It can be opened with [Bizagi Modeler](https://www.bizagi.com/uk/products/bpm-suite/modeler);
  * *UK_Nightlife-BPMN-workflow_net.pnml* file containing the modeled workflow net of the BPMN representation of the project. It can be opened with [WoPeD](https://woped.dhbw-karlsruhe.de/);
  * *UK_Nightlife-project* folder containing the source code of the developed project by using [OpenESB](http://www.open-esb.net/):
    * *UkNightlife* folder containing the BPEL implementation of the project and UkNightlifeCA folder that contains the relative composite application to be deployed;
    * *GetCityByPostCodeProxy* folder containing the BPEL implementation of the proxy service and GetCityByPostCodeCA folder that contains the associated composite application to be deployed;
    * *GetCityByPostCodeLocal* folder containing the BPEL implementation of the SOAP local dummy service and *GetCityByPostCodeLocalCA* folder that contains the relative composite application to be deployed;
 * *UK_Nightlife-workflow_net.pnml* file containing the modeled workflow net of the project.
 
 ### Deployment guide
 
 In order to run the project you have to follow the steps below:
 
 1. Lunch OpenESB
 2. From the menu, File > Open Project
 3. Search the unzipped uknightlife-master folder and select all the folders that it contains and click Open Project
 4. In the Project tab right click and select Clean and Build for every projects starting from those without * *CA* in the name and subsequently to those with * *CA* in the name
 5. Right click and select Deploy for all the projects with * *CA* in the name
 6. Run the test cases located in the *UkNightlifeCA* > *Test*
