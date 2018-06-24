# AtlantisToulouseUML

### DeploymentDiagram

![DeploymentDiagram](./DeploymentDiagram.png)

### ComponentJEEDiagram

![ComponentJEE](./ComponentJEE.png)

### WindowsPlatform_ComponentDiagram

![WindowsPlatform_ComponentDiagram](WindowsPlatform_ComponentDiagram.png)

### MobileApplicationComponentDiagram

![MobileApplicationComponentDiagram](./MobileApplicationComponentDiagram.PNG)

### ActivityDiagram_CalculationEngineFlow

![ActivityDiagram_CalculationEngineFlow](./ActivityDiagram_CalculationEngineFlow.PNG)

### ActivityDiagram_SendMessageToDevice

![ActivityDiagram_SendMessageToDevice](ActivityDiagram_SendMessageToDevice.png)

### ActivityDiagram_DisplayMetricOnMobileApplication

![ActivityDiagram_DisplayMetricOnAndroidApplication](./ActivityDiagram_DisplayMetricOnAndroidApplication.png)

This diagram represents the flow generated when metrics are diaplayed on the mobile application.

The user first has to log in through **EliotCloud** using their API. The received token will be used for **authentication** with the **Mobile Web Service** hosted on the JEE Platform.

Once logged in, the mobile application will fetch the **user's devices** through the **Mobile Web Service**. As these information are stocked on the .NET Platform, The Mobile Web Service will fetch it using the **UserData Web Service**. Once returned to the device, devices will be displayed.

On the selection of one of the device, **both Raw and Calculated Metrics** will be retrieved using a **single request** to the Mobile Web Service. This last will fetch the Calculated Metrics directly in the database located on the same platform, and the Raw Metrics through the **RawMetrics WebService** since the data is located on the .NET Platform. Once the Mobile Web Serive has gathered all metrics, it will send it back to the device for display.