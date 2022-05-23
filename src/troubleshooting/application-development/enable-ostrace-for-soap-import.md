---
summary: Enable OSTrace to troubleshoot incompatibility issues when importing SOAP web wervices.
tags: support-application_development; support-Integrations_Extensions
locale: en-us
guid: 5BB9566B-1A9F-45B9-81D9-4F93D3BECDFC
---

# Enabling OSTrace for SOAP web service consumption in Service Studio

**OutSystems** has a robust mechanism for identifying errors when parsing a SOAP web service. In **Service Studio**, when importing a SOAP web service, errors such as unsupported cases, internal exceptions, or grammatical errors in the WSDL can occur. In these cases, an error message window detailing the root cause of the error is displayed.

However, sometimes a SOAP consume error message does not include enough information to find out the root cause. In this case, you can enable OSTrace, which increases the log levels and collects more information about what happened during the import process. Examining the generated logs can give you a helpful start in finding the root cause of the error and to identify problematic segments of definition files.


## Correcting recognized SOAP web service errors

When the information displayed in the error message is specific enough, you can pinpoint the exact root cause, as seen below. 

![SOAP import issues window](<images/soap-import-fixable-issue-ss.png>)

In this example, the root cause of the error is an undeclared prefix named ``` asdf```  that is used in the ``` Historikk.xsd``` external schema file.

Follow the procedure below to correct this error:

1. Export the definition files, according to the instructions in [Export definition files in a SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Export_definition_files_in_a_SOAP_web_service#Exporting_definition_files) to obtain all files that define the service with updated schema locations.
1. Open ``` Historikk.xsd```  in a text editor. As can be seen below, ``` asdf```  is an undeclared prefix.
    
        <xs:group name="customerGroup">
        	<asdf:sequence>	
        		<xs:element name="customer" type="xs:string"/>
        		<xs:element name="orderdetails" type="xs:string"/>
        	</xs:sequence>
        </xs:group>
    

1. Correct this prefix.

    <div class="info" markdown="1">

    Some possible ways to correct this prefix include:

    * Declare the ```asdf``` prefix by writing ```xmlns:asdf="http://www.w3.org/2001/XMLSchema"``` in the beginning of the file.
    * Replace the ```asdf``` prefix with a previously declared prefix used in the code snippet, such as ```xs```.

    </div>

1. Save the file and import the modified definition files into **Service Studio** with the **Choose From File** option, as explained in [Export definition files in a SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Export_definition_files_in_a_SOAP_web_service#Exporting_definition_files). 

The SOAP web service should now perform as expected.

## Troubleshooting using OSTrace

In some cases the information displayed in **Service Studio** is not sufficient to pinpoint the root cause of the error, as can be seen in the message window below:

![SOAP import issues window](<images/soap-import-issues-ss.png>)


The root cause of the error seems to be a name collision issue involving ``` SoccerTeam``` , but it may be difficult to understand where to find the code in order to examine it and begin the process of correcting it.

In this case, you can increase the log levels of SOAP web services  consumption by enabling OSTrace.


### Enabling OSTrace

To enable OSTrace for SOAP web service consumption, first delete the problematic SOAP web service and exit **Service Studio**.

Then modify the configuration file, according to the **Service Studio** edition you are using.

1. Go to the folder of the configuration file:

    * Windows:

        * Windows-only Service Studio: ```C:\Users\<user_name>\AppData\Local\OutSystems\ServiceStudio 11```.  

        * Cross-platform Service Studio: ```C:\Users\<user_name>\AppData\Local\OutSystems\ServiceStudio 11 XPlatform```.  

    * macOS: ```~/.local/share/Outsystems/ServiceStudio 11 XPlatform```.

    <div class="info" markdown="1">

    AppData (Windows) and .local (macOS) folders are hidden by default. You need to enable the setting to show hidden folders.

    </div>
    
1. Open ```Settings.xml```  in a text editor and add the following line to the file:

     ```<SystemDiagnosticsSwitches>SoapConsume</SystemDiagnosticsSwitches>```


    <div class="info" markdown="1">

    If the line is commented out, remove the prefix ```<!--```  and the suffix ```-->```.

    </div>

1. Add a listener file to collect the logs. You may use any name.  
    In this example the ```general.txt``` log file is added.

    * Windows:
        * Windows-only Service Studio:
         ```<SystemDiagnosticsListenerFile>C:/Users/<user_name>/AppData/Local/OutSystems/ServiceStudio 11/general.txt</SystemDiagnosticsListenerFile>```

        * Cross-platform Service Studio:
     ```<SystemDiagnosticsListenerFile>C:/Users/<user_name>/AppData/Local/OutSystems/ServiceStudio 11 XPlatform/general.txt</SystemDiagnosticsListenerFile>```

    * macOS:
     ```<SystemDiagnosticsListenerFile>~/.local/share/Outsystems/ServiceStudio 11 XPlatform/general.txt</SystemDiagnosticsListenerFile>```

    <div class="info" markdown="1">

    If the line is commented out, remove the prefix ```<!--```  and the suffix ```-->```.

    </div>

1. Save the file and launch **Service Studio**.

<div class="info" markdown="1">

Keeping OSTrace enabled at all times can negatively impact the performance of your machine and disk space usage. Check [how to disable OSTrace](#disable-ostrace).

</div>


### Using OSTrace

With OSTrace enabled, logs are written to a local file every time you consume a new SOAP web service.

The example below describes a typical troubleshooting workflow.

1. In **Service Studio**, consume the problematic SOAP service that generated the error message.
1. Go to the folder of the ```general.txt``` file.
    * Windows:

        * Windows-only Service Studio: ```C:\Users\<user_name>\AppData\Local\OutSystems\ServiceStudio 11```.  

        * Cross-platform Service Studio: ```C:\Users\<user_name>\AppData\Local\OutSystems\ServiceStudio 11 XPlatform```.  

    * macOS: ```~/.local/share/Outsystems/ServiceStudio 11 XPlatform```.

1. Open ```general.txt``` in a text editor.

1. In the ```Name Collision Issue``` section, examine the name, namespace, and XML kind of the elements that are causing the conflict.

    <table>
    <tr>
    <td colspan="4" >
    <code>"Name Collision Issue"</code>
    </td>
    </tr>
    <tr>
    <td><code>Original Name</code>
    </td>
    <td><code>Namespace</code>
    </td>
    <td><code>Is Anonymous?</code>
    </td>
    <td><code>XML Kind</code>
    </td>
    </tr>
    <tr>
    <td><code>SoccerTeam</code>
    </td>
    <td><code>http://SoccerTeam/aux</code>
    </td>
    <td><code>False</code>
    </td>
    <td><code>attributeGroup</code>
    </td>
    </tr>
    <tr>
    <td><code>SoccerTeam</code>
    </td>
    <td><code>http://SoccerTeam/aux</code>
    </td>
    <td><code>False</code>
    </td>
    <td><code>complexType</code>
    </td>
    </tr>
    </table>


The root cause of the problem is that a ```xs:complexType``` and a ```xs:attributeGroup``` share the same name: ```SoccerTeam```.

To correct this issue follow the procedure below:

1. Export the definition files, according to the instructions in [Export definition files in a SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Export_definition_files_in_a_SOAP_web_service#Exporting_definition_files), to obtain all files that define the service with updated schema locations.
1. Go to the location where you saved the definition files and run a text search for all files in that folder that have the name ``` SoccerTeam``` .
1. Open the files where this appears and analyze the offending namespace. As can be seen in the code snippet below, in this specific namespace there is more than one XML node with the name ``` SoccerTeam``` . 


        line 1: <xs:complexType name="SoccerTeam">
        line 2:     <xs:attributeGroup ref="tns:SoccerTeam"/>
        line 3: </xs:complexType>
        line 4: <xs:attributeGroup name="SoccerTeam">
        line 5:     <xs:attribute name="Name" type="xs:string"/>
        line 6:     <xs:attribute name="Country" type="xs:string"/>
        line 7:     <xs:attribute name="City" type="xs:string"/>
        line 8: </xs:attributeGroup>

1. Modify line 4 of the code snippet by changing ```<xs:attributeGroup name="SoccerTeam">``` to ```<xs:attributeGroup name="SoccerTeamAttr">``` .
1. Update the references to this element in line 2 of the code snippet by changing ``` <xs:attributeGroup ref="tns:SoccerTeam"/>```  to ``` <xs:attributeGroup ref="tns:SoccerTeamAttr"/>``` .
1. Save the file.

Import the modified definition files into **Service Studio** with the **Choose From File** option, as explained in [Export definition files in a SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Export_definition_files_in_a_SOAP_web_service#Exporting_definition_files). If there are no additional error messages, the SOAP web service should work as expected. 

### Disabling OSTrace { #disable-ostrace }

When OSTrace is enabled, **Service Studio** runs additional code and writes additional log information to the disk when consuming a SOAP web service. Since these logs may be long and extensive,  you should disable OSTrace logging when the troubleshooting session ends. 

To disable OSTrace for SOAP web services’ consumption: 

1. Exit **Service Studio**.
2. Open the configuration file you modified earlier. Comment out the lines you edited by adding the prefix ``` <!-- ```  and the suffix ``` -->```  to both lines.
3. Save the file.

New SOAP web service consumption logs are no longer written to the ```general.txt``` logs.
