---
# required metadata

title: Install Advanced Threat Analytics - Step 7 | Microsoft Docs
description: In the final step of installing ATA, you configure the Honeytoken user.
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 08/20/2017
ms.topic: get-started-article
ms.prod:
ms.service: advanced-threat-analytics
ms.technology:
ms.assetid: 8980e724-06a6-40b0-8477-27d4cc29fd2b

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: bennyl
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

*Applies to: Advanced Threat Analytics version 1.8*



# Install ATA - Step 7

>[!div class="step-by-step"]
[« Step 6](install-ata-step6.md)

## Step 7. Configure IP address exclusions and Honeytoken user
ATA enables the exclusion of specific IP addresses or users from a number of detections. 

For example, a **DNS Reconnaissance exclusion** could be a security scanner that uses DNS as a scanning mechanism. The exclusion helps ATA ignore such scanners. An example of a *Pass-the-Ticket* exclusion is a NAT device.    

ATA also enables the configuration of a Honeytoken user, which is used as a trap for malicious actors - any authentication associated with this (normally dormant) account will trigger an alert.

To configure the above, follow these steps:

1.  From the ATA Console, click on the settings icon and select **Configuration**.

    ![ATA configuration settings](media/ATA-config-icon.png)

2.  Under **Detection**, click **General**.

2. Under **Honeytoken accounts** enter the Honeytoken account name. The Honeytoken accounts field is searchable and will automatically display entities in your network.

   ![Honeytoken](media/honeytoken.png)

3. Click **Exclusions**. For each type of threat, enter a user account or IP address to be excluded from the detection of these threats and click the *plus* sign. The **Add entity** (user or computer) field is searchable and will autofill with entities in your network. For more information, see [Excluding entities from detections](excluding-entities-from-detections.md)

   ![Exclusions](media/exclusions.png)


  > [!NOTE]
  > To find the SID for a user, search for the user in the ATA Console, and then click on the **Account Info** tab. 

4.  Click **Save**.


Congratulations, you have successfully deployed Microsoft Advanced Threat Analytics!

Check the attack time line to view detected suspicious activities and search for users or computers and view their profiles.

ATA will start scanning for suspicious activities immediately. Some activities, such as some of the suspicious behavior activities, will not be available until ATA has had time to build behavioral profiles (minimum of three weeks).

To check that ATA is up and running and catching breaches in your network, you can check out the [ATA attack simulation playbook](https://docs.microsoft.com/enterprise-mobility-security/solutions/ata-attack-simulation-playbook).


>[!div class="step-by-step"]
[« Step 6](install-ata-step6.md)



## Related Videos
- [Choosing the right ATA Gateway type](https://channel9.msdn.com/Shows/Microsoft-Security/ATA-Deployment-Choose-the-Right-Gateway-Type)


## See Also
- [ATA POC deployment guide](http://aka.ms/atapoc)
- [ATA sizing tool](http://aka.ms/atasizingtool)
- [Check out the ATA forum!](https://social.technet.microsoft.com/Forums/security/home?forum=mata)
- [Configure event collection](configure-event-collection.md)
- [ATA prerequisites](ata-prerequisites.md)
