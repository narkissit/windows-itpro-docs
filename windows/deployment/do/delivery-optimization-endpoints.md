---
title: Delivery Optimization and Microsoft Connected Cache content endpoints
description: List of fully qualified domain names, ports, and associated content types to use Delivery Optimization and Microsoft Connected Cache.
ms.date: 07/26/2022
ms.prod: windows-client
ms.technology: itpro-updates
ms.topic: reference
ms.localizationpriority: medium
author: cmknox
ms.author: carmenf
ms.reviewer: mstewart
manager: naengler
---

# Delivery Optimization and Microsoft Connected Cache content type endpoints

_Applies to:_

- Windows 11
- Windows 10

> [!NOTE]
> All ports are outbound.

This article lists the endpoints that need to be allowed through the Firewall to ensure that cloud content downloaded via Delivery Optimization or Microsoft Connected Cache is properly delivered. 
There are two versions of Microsoft Connected Cache (MCC):
1. Microsoft Connected Cache with Configuraiton Manager Distribution Point ("MCC on a DP")
2. Microsoft Connected Cache Managed in Azure ("MCC Standalone")

Use the table below to reference the endpoints required for cloud content downloads, the Delivery Optimization service and a particular version of Microsoft Connected Cache (MCC):

|Domain Name  |Protocol/Port(s)  | Type | Additional Information | MCC Version |
|---------|---------|---------------|-------------------|-----------------|
| *.b1.download.windowsupdate.com, *.dl.delivery.mp.microsoft.com, *.download.windowsupdate.com, *.au.download.windowsupdate.com, *.au.b1.download.windowsupdate.com, *.tlu.dl.delivery.mp.microsoft.com, *.emdl.ws.microsoft.com, *.ctldl.windowsupdate.com   |  HTTP / 80  | Windows Update, </br> Windows Defender, </br> Windows Drivers | [Complete list](/windows/privacy/manage-windows-2004-endpoints) of endpoints for Windows Update services and payload. | Both versions |
| *.delivery.mp.microsoft.com  |  HTTP / 80  | Edge Browser | [Complete list](/deployedge/microsoft-edge-security-endpoints) of endpoints for Edge Browser. | Both versions |
| *.officecdn.microsoft.com.edgesuite.net, *.officecdn.microsoft.com, *.cdn.office.net |  HTTP / 80  | Office CDN updates | [Complete list](/office365/enterprise/office-365-endpoints) of endpoints for Office CDN updates. | Both versions |
| *.manage.microsoft.com, *.swda01.manage.microsoft.com, *.swda02.manage.microsoft.com, *.swdb01.manage.microsoft.com, *.swdb02.manage.microsoft.com, *.swdc01.manage.microsoft.com, *.swdc02.manage.microsoft.com, *.swdd01.manage.microsoft.com, *.swdd02.manage.microsoft.com, *.swda01-mscdn.manage.microsoft.com, *.swda02-mscdn.manage.microsoft.com, *.swdb01-mscdn.manage.microsoft.com, *.swdb02-mscdn.manage.microsoft.com, *.swdc01-mscdn.manage.microsoft.com, *.swdc02-mscdn.manage.microsoft.com, *.swdd01-mscdn.manage.microsoft.com, *.swdd02-mscdn.manage.microsoft.com |  HTTP / 80 </br> HTTPs / 443  | Intune Win32 Apps | [Complete list](/mem/intune/fundamentals/intune-endpoints) of endpoints for Intune Win32 Apps updates. | Both versions |
| *.statics.teams.cdn.office.net |  HTTP / 80 </br> HTTPs / 443  | Teams | | Both versions |
| *.assets1.xboxlive.com, *.assets2.xboxlive.com, *.dlassets.xboxlive.com, *.dlassets2.xboxlive.com, *.d1.xboxlive.com, *.d2.xboxlive.com, *.assets.xbox.com, *.xbl-dlassets-origin.xboxlive.com, *.assets-origin.xboxlive.com, *.xvcb1.xboxlive.com, *.xvcb2.xboxlive.com, *.xvcf1.xboxlive.com, *.xvcf2.xboxlive.com |  HTTP / 80 | Xbox | | Both versions |
| *.tlu.dl.adu.microsoft.com, *.nlu.dl.adu.microsoft.com, *.dcsfe.prod.adu.microsoft.com |  HTTP / 80 | Device Update for Azure IoT Hub | [Complete list](/azure/iot-hub-device-update/) of endpoints for Device Update updates.  | Both versions |
| *.do.dsp.mp.microsoft.com |  HTTP / 80 </br> HTTPs / 443 | Delivery Optimization Services | [Complete list](../do/waas-delivery-optimization-faq.yml) of endpoints for Delivery Optimization only.  | Microsoft Connected Cache Managed in Azure |
| *.azure-devices.net, *.global.azure-devices-provisioning.net, *.azurecr.io, *.blob.core.windows.net, *.mcr.microsoft.com, github.com |  AMQP / 5671 </br>  MQTT / 8883 </br> HTTPs / 443 | Microsoft Connected Cache services in Azure, IoT Edge / IoT Hub services| [Complete list](/azure/iot-hub/iot-hub-devguide-protocols) of Azure IoT Hub communication protocols and ports. </br>[Azure IoT Guide](/azure/iot-hub/iot-hub-devguide-endpoints) to understanding Azure IoT Hub endpoints. | Microsoft Connected Cache Managed in Azure |
