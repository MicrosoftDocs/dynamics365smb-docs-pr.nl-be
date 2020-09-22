---
title: Bedrijfsconfiguratie instellen | Microsoft Docs
description: Het implementatieproces begint met de gegevens die de Business Central-oplossing vereist. U bundelt al deze gegevens in configuratiepakketten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5698110875799fe39cf3544dce0ea39f7c3dd5ba
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786233"
---
# <a name="set-up-company-configuration"></a>Een bedrijfsconfiguratie instellen
Het implementatieproces begint met de Microsoft-partner. Het is de verantwoordelijkheid van de partner om de configuratiedetails uit te werken en een pakket op te stellen dat een klant eenvoudig kan toepassen. Voordat u een nieuw bedrijf maakt, moet u plannen hoe dit zal worden geconfigureerd. U moet rekening houden met elementaire instellingsgegevens en de soorten gegevens die uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplossing nodig zal hebben. U bundelt al deze gegevens in configuratiepakketten.

RapidStart Services bieden u ook de hulpmiddelen die u gebruikt om uw oude gegevens te migreren, zoals klanten en leveranciers.  

Het is raadzaam om configuratiepakketten te maken met de meeste van de instellingentabellen al ingevuld, zodat klanten slechts enkele instellingen hoeven te wijzigen nadat het pakket is toegepast. Bijvoorbeeld wanneer u een nieuw bedrijf maakt, worden de tabellen, **Nr.-reeksen** en **Nr.-reeksregel**, gevuld met een verzameling nummerreeksen en begingetallen. De bijbehorende **Nr.-reeks**-velden in de instellingentabellen worden ook automatisch ingevuld. U hoeft de nummerreeksen en andere basisinstellingsgegevens niet zelf in te voeren. U kunt alle standaardgegevens die worden gebruikt met RapidStart Services, ook handmatig wijzigen met behulp van het configuratiewerkblad.  

De configuratiepakketten zijn gebaseerd op een vooraf geconfigureerd bedrijf. Nadat u een bedrijf hebt ingesteld dat aan uw behoeften voldoet, kunt u een configuratiepakket met relevante gegevens maken op basis van dit bedrijf. U kunt deze dan gebruiken wanneer u een nieuw bedrijf maakt dat op dezelfde manier moet worden geconfigureerd.  

U kunt het importeren van hoofdgegevens, zoals klant- en leveranciersinformatie, vergemakkelijken door configuratiesjablonen te gebruiken. Configuratiesjablonen bevatten een set standaardinstellingen die automatisch worden toegewezen aan de records die zijn geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].

In de volgende tabel wordt een reeks taken beschreven met koppelingen naar de beschrijvende onderwerpen.

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Plan een bedrijfsconfiguratie door het configuratiewerkblad in te vullen.|[De bedrijfsconfiguratie beheren in een werkblad](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Maak een configuratiepakket, pas een pakket aan, wijs tabellen aan een pakket toe, controleer of bewerk bestaande klantgegevens, maak het nieuwe bedrijf en verplaats vervolgens testgegevens naar de productieomgeving.|[Een configuratiepakket voorbereiden](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Zie ook  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
