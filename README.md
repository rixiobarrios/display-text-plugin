# DMC UX UI5 BAS UC

[Video tutorial from Andy Nayman](https://sap.sharepoint.com/teams/ManufacturingNA2-DigitalManufacturingHuddle-Monthly2/_layouts/15/stream.aspx?id=%2Fteams%2FManufacturingNA2%2DDigitalManufacturingHuddle%2DMonthly2%2FShared%20Documents%2FDigital%20Manufacturing%20Huddle%20%2D%20Monthly%2FMeeting%20with%20Nyman%2C%20Andy%2D20230609%5F080858%2DMeeting%20Recording%2Emp4)

## UX Use-Case-01: View Plug-in – Display Text
As a system, I want a custom view plugin that displays the text “Hello World” so that the world knows I am here.

- Step 1 - Go to Business Application Studio (BAS)

[Your Business Application Studio environment](https://dmc-az-cons-training.eu20cf.applicationstudio.cloud.sap/index.html)

- Step 2 - Enter a new Dev Space  
e.g DMCPlugin

- Step 3 - Select application kind  
SAP Fiori

- Step 4 - click the Create Dev space button

- Step 5 - Click on the newly created Dev Space

- Step 6 - Open a new terminal window

- Step 7 - Open project folder  
```cd projects```

- Step 8 - Make new project's folder  
e.g. mkdir test6podplugin

- Step 9 - Open new folder  
```cd test6podplugin```

- Step 10 - Install generator plugin  
```npm install generator-dmcpodplugin```

- Step 11 - Generate new project  
```yo dmcpodplugin```

- Step 12 - Enter the name of your plugin  
e.g. test6podplugin

- Step 13 - Enter version number  
e.g. 0.0.1

- Step 14 - What is your DMC host name?  
e.g. dmc-az-cons-training.test.execution.eu20.dmc.cloud.sap

- Step 15 - What is your plugin namespace?  
e.g. sap.custom.plugin.viewplugin

- Step 16 - Support WORK_CENTER PODS?  
Yes

- Step 17 - Support OPERATIONS PODS?  
Yes

- Step 18 - Support ORDER PODS?  
Yes

- Step 19 - Support CUSTOM PODS?  
Yes

- Step 20 Support Line Monitor PODS?  
Yes

- Step 21 - Allow Multiple Instances?  
Yes

- Step 22 - Production Process Enabled?  
No

- Step 23 - Open working folder  
e.g. user/projects/test6podplugin

- Step 24 - Open file builder.properties  
e.g. user/projects/test6podplugin/webapp/test6podplugin/builder/PropertyEditor.js

- Step 25 - Change line 37 from ```text:"test6podplugin"``` to ```"Hello World"```

- Step 26 - Right click on file mta.yaml  
e.g. user/projects/test6podplugin/mta.yaml

- Step 27 - Select Build MTA Project from popup menu

- Step 28 - Press any key to close process after finished

- Step 29 - Right click on file generated by Build MTA Project  
e.g. user/projects/test6podplugin/mta_archives/test6podplugin_0.0.1,mta_archives

- Step 30 - Select Deploy MTA Archive from popup menu

- Step 31 - On Cloud Foundry Sign In and Targets enter your endpoint  
e.g. user/projects/test6podplugin/mta.yaml

- Step 32 - On Cloud Foundry Sign In and Targets enter your credentials  
e.g. user@sap.com and password

- Step 33 - On Cloud Foundry target select desired oragnization  
e.g. Digital Manufacturing Cloud Internal tenants_DMC-AZ-CONS-training

- Step 34 - On Cloud Foundry target select desired space and click apply  
e.g. DMC_DEV

- Step 35 - Grab generated link  
e.g. Application "test6podplugin" started and available at "digital-manufacturing-cloud-internal-tenants-dmc-az-***********.******.eu20.hana.ondemand.com"

- Step 36 - Press any key to close process after finished

- Step 37 - Add to servide registry app in DMC (Digital Manufacturing Cloud)

[Your Digital Manufacturing Cluod Tenant](https://dmc-az-cons-training.test.execution.eu20.dmc.cloud.sap/cp.portal/site?sap-language=en#Shell-home)

- Step 38 - Go onto Manage Service Registry

- Step 39 - Select UI Extensions

- Step 40 - Click on Create

- Step 41 - On New UI Extension screen enter the following

- Step 42 - Enter Name  
e.g. test6podplugin

- Step 43 - Enter Description  
e.g. Test 6 Demo Pod Plugin

- Step 44 - Select Type POD plugin

- Step 45 - Enter generated link from deployment into URL adding https:// or http://

- Step 46 - Enter name space previously set at project generator with forward slashes instead of dots and add the project's name.
e.g. sap.custom.plugin.viewplugin to sap/custom/plugin/viewplugin/test6podplugin

- Step 47 - Enter PATH as the project's folder  
e.g. /test6podplugin

- Step 48 - Check the Enable Status box and click Create

- Step 49 - Custom plugin is enabled and vaialable in the DMC and can be used in a POD (Production Operation Dashboard)

- Step 50 - Select EXAMPLE VIEW PLUGIN POD

- Step 51 - Select Details

- Step 52 - Search for our newly created plugin  
e.g. test6podplugin

- Step 53 - Drag and drop test6podplugin to the "More" button with the chevron

- Step 54 - Click on the chevron and make sure test6podplugin is in the drop down menu at the end

- Step 55 - Click on test6podplugin

- Step 56 - Click the Configuration Panel button (Two gears icon)

- Step 57 - Change the title to Test 6 Hello World and save

- Step 58 - Click the Preview  button (eye glasses icon)

- Step 59 - Select PRINTER_A under resource

- Step 60 - Select DMC_PRIN under Work center

- Step 61 - Click on the SFC text box and clcik the Go button to populate Work List

- Step 62 - Seleck a Status=New SFC

- Step 63 - You will be back in the POD viewing your selction

- Step 64 - Click on test6podplugin

You should see the words "Hello World"

Build was successfully completed
