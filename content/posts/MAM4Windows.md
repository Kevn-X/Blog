---
title: "Was it worth the wait?"
date: 2023-08-22T11:10:36+08:00
draft: false
language: en
featured_image: ../assets/images/featured/MAM4Windows.png
summary: The latest Intune update brings Mobile Application Management (MAM) support for Microsoft Edge for Business on Windows. Lets dive in!
description: Deep diving MAM for Windows and the caveats to it's current feature set.
author: Kevin O.
authorimage: ../assets/images/global/bio-small.jpg
categories: Intune
tags: ['MAM','Intune', 'BYOD']
---
In a recent unveiling, Microsoft introduced the eagerly anticipated Mobile Application Management (MAM) for Windows. As of July 7th, 2023, this new addition has entered the Public Preview phase, allowing us to explore and experiment with its capabilities firsthand.

MAM brings a unique dimension to the table, enabling the application of policies to corporate applications. This measure ensures the safeguarding of sensitive organizational data and effectively prevents its inadvertent exposure on personal devices. This capability proves particularly valuable in Bring Your Own Device (BYOD) scenarios, eliminating the need for extensive device management through Microsoft Intune.

While MAM has long been available for Android and iOS platforms, its integration with Windows comes at a crucial juncture. This transition comes in light of the discontinuation of its predecessor, Windows Information Protection (WIP), in future Windows versions.

In this blog post, we will embark on an initial exploration of MAM for Windows. Please bear in mind that this review is based on the current public preview, and the landscape is subject to evolution.

### Sections Covered:

#### <u>Prerequisites</u>
- MAM User Scope
- Integration of Mobile Threat Defense Connector
- Configuration of Application Protection Policy
- Implementation of MAM through Conditional Access
- User Experience
- Conclusive Thoughts
- Essential Prerequisites:

To set up MAM for Windows during this Public Preview, enrollment in the program and tenant enrollment are prerequisites. Furthermore, there are specific requirements tied to Windows OS, Windows Security, and Microsoft Edge versions. Given the dynamic nature of these requirements, they are continually updated within the preview program.

It's essential that devices aren't Azure AD joined or enrolled in Mobile Device Management (MDM) for a seamless setup process.

#### <u>Scoping MAM for Users:</u>

Configuring MAM user scope correctly is paramount. This step ensures that user groups are properly enabled, allowing users to register devices without enrollment. Additionally, corporate client apps can benefit from Application Protection policies.

#### <u>The Mobile Threat Defense Connector:</u>

Integration of the Mobile Threat Defense (MTD) connector is a pivotal step. It integrates seamlessly with Microsoft Intune, detecting local health threats and enabling the blocking of access from vulnerable or compromised devices. Upon device enrollment in MAM, the connector should activate both in the portal and on the device.

#### <u>Setting Up Application Protection Policy:</u>

A crucial aspect of MAM involves configuring the Application Protection policy. Presently, this policy is applicable only to the Microsoft Edge app. While limited in scope, this will likely expand to encompass other Microsoft applications in the future.

The policy also entails data protection restrictions, enabling specification of data source origins, organizational data destinations, cut-copy-paste actions, and more. While the current options are limited, they are expected to evolve during the public preview.

#### <u>Enforcing MAM through Conditional Access:</u>

Enforcing MAM for Windows involves configuring a conditional access policy. This policy mandates the application protection policy previously established, ensuring users cannot access resources without the protective umbrella of Mobile Application Management.

#### <u>Exploring User Experience:</u>

Upon completing the setup, users on personal Windows devices, not linked to Azure AD or MDM, gain access to the Microsoft 365 portal. Creation of a new Microsoft Edge profile and sign-in with a corporate account become seamless. Corporate app data remains secure within the Microsoft Edge profile, even as users navigate beyond the Microsoft 365 environment.

#### <u>A Glimpse into the Future:</u>

The current capabilities of MAM for Windows mirror those achievable through session policies in Microsoft Defender for Cloud Apps. However, the promise of MAM's future potential is truly exciting. As it advances towards general availability, it holds the potential to play a pivotal role in granting secure access to corporate resources on personal devices. The inclusion of the Mobile Threat Defense connector positions it as a frontrunner in comparison to existing methods.

While certain features like support for a broader range of applications and enhanced security measures are not yet available in this preview, the future of MAM for Windows certainly looks promising. With the ability to maintain data integrity and user experience on personal devices, MAM is undoubtedly carving a path toward a more secure and efficient digital workspace.