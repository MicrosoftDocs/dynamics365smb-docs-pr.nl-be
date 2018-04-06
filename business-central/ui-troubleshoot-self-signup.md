---
title: Probleemoplossing met aanmelden bij Self-Service | Microsoft Docs
description: Meer informatie over de meest voorkomende redenen waarom u de inschrijving bij Business Central niet kunt voltooien, en manieren om het op te lossen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1595f5020a0da7b2899ba056f135ff5e88985d38
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-self-service-sign-up"></a>Probleemoplossing voor aanmelden bij Self-Service
Aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] is eenvoudig en kan erg snel worden uitgevoerd. U kunt een gratis account maken, zelfs als u een bestaande organisatie bent. In dit artikel worden problemen behandeld die u tijdens het aanmelden kunt tegenkomen.

## <a name="what-email-address-can-i-use-with-business-central"></a>Welk e-mailadres kan ik gebruiken met Business Central?
Voor [!INCLUDE[d365fin](includes/d365fin_md.md)] moet u voor aanmelding een e-mailadres van het werk of van school gebruiken. In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden geen e-mailadressen ondersteund die worden geleverd door consumentene-mailservices of telecommunicatieproviders. Dit omvat outlook.com, hotmail.com, gmail.com en andere.

Als u zich met een persoonlijk e-mailadres probeert aan te melden, ontvangt u een bericht dat u een e-mailadres van het werk of van school moet gebruiken.

## <a name="troubleshooting"></a>Problemen oplossen
In veel gevallen kunt u uw registratie voor [!INCLUDE[d365fin](includes/d365fin_md.md)] uitvoeren door het aanmeldingsproces te volgen. Er zijn echter verschillende redenen waarom u zich mogelijk niet kunt aanmelden bij de Self-Service. In de tabel hierna wordt een aantal van de meest voorkomende redenen samengevat waarom u de aanmelding niet kunt voltooien en worden manieren beschreven waarop u deze problemen kunt oplossen.

| Symptoom/foutmelding | Oorzaak en oplossing |
| --- | --- |
| Voor Office 365-e-mailadressen die niet in een ondersteund land zijn geregistreerd, ontvangt u tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw land of regio wordt nog niet ondersteund.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt momenteel alleen Office 365 e-mailaccounts die zijn geregistreerd in een beperkt aantal markten. Zie voor meer informatie [Regionale beschikbaarheid](#regional-availability). |
| Persoonlijke e-mailadressen, zoals nancy@gmail.com, worden niet ondersteund. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**U hebt een persoonlijk e-mailadres ingevoerd: voer het e-mailadres van uw werk in zodat de gegevens van uw bedrijf veilig kunnen worden opgeslagen.**<br> of <br> **Dit ziet eruit als een persoonlijk e-mailadres. Voer uw werkadres in zodat we u met anderen in uw bedrijf kunnen verbinden. Maak u geen zorgen. Uw adres wordt met niemand gedeeld.** |In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden geen e-mailadressen ondersteund die worden geleverd door consumentene-mailservices of telecommunicatieproviders. Om de aanmelding te voltooien moet u opnieuw proberen een e-mailadres te gebruiken dat door uw werk of school is toegewezen. Als u zich nog niet kunt aanmelden en bereid bent een geavanceerder instellingsproces uit te voeren, kunt u zich registreren voor een nieuw Office 365-proefabonnement en dat e-mailadres voor aanmelding gebruiken. |
| .gov- of .mil-e-mailadressen U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] niet beschikbaar: [!INCLUDE[d365fin](includes/d365fin_md.md)] is momenteel niet beschikbaar voor gebruikers met .gov- of .mil-e-mailadressen. Gebruik een ander werke-mailadres of kom later nog eens terug.** <br>of <br>**Uw aanmelding kan niet worden voltooid. Het lijkt erop dat [!INCLUDE[d365fin](includes/d365fin_md.md)] momenteel niet beschikbaar is voor uw werk of school.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt momenteel geen .gov- of .mil-adressen. |
| Self-Service-aanmelding is niet ingeschakeld. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw aanmelding kan niet worden voltooid. Uw IT-afdeling heeft aanmelding voor [!INCLUDE[d365fin](includes/d365fin_md.md)] uitgeschakeld. Neem contact op met de IT-afdeling om de aanmelding te voltooien.** <br>of <br> **Dit ziet eruit als een persoonlijk e-mailadres. Voer uw werkadres in zodat we u met anderen in uw bedrijf kunnen verbinden. Maak u geen zorgen. Uw adres wordt met niemand gedeeld.** |De IT-beheerder van uw organisatie heeft Self-Service-aanmelding voor [!INCLUDE[d365fin](includes/d365fin_md.md)] uitgeschakeld. Om aanmelding te voltooien, neemt u contact op met uw IT-beheerder en vraagt u de instructies op de onderstaande pagina te volgen om bestaande gebruikers toe te staan zich aan te melden voor [!INCLUDE[d365fin](includes/d365fin_md.md)] en nieuwe gebruikers toe te staan deel te nemen aan uw bestaande tenant. U kunt dit probleem ook tegenkomen als u zich hebt aangemeld voor Office 365 via een partner. |
| E-mailadres is geen Office 365-ID. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**We kunnen u niet vinden op contoso.com. Gebruikt u een andere ID op het werk of op school? Probeer daarmee aan te melden en als het niet werkt, neemt u contact op met de IT-afdeling.** |Uw organisatie gebruikt ID´s voor aanmelding bij Office 365 en andere Microsoft-services die anders zijn dan uw e-mailadres. Zo kan uw e-mailadres Nancy.Smith@contoso.com zijn, maar uw ID nancys@contoso.com. Om de aanmelding te voltooien, gebruikt u de ID die uw organisatie heeft toegewezen voor aanmelding bij Office 365 of andere Microsoft-services. Als u niet weet wat dit is, neemt u contact op met uw IT-beheerder. Als u zich nog niet kunt aanmelden en een geavanceerder configuratieproces kunt uitvoeren, kunt u zich registreren voor een nieuw Office 365-proefabonnement en dat e-mailadres voor aanmelding gebruiken. |
| Als het Office 365-account is geregistreerd in een ondersteund land en u zich aanmeldt voor [!INCLUDE[d365fin](includes/d365fin_md.md)] terwijl u zich in een ander land bevindt, ontvangt u tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw land of regio wordt nog niet ondersteund.**| Het abonnement op Office 365 van uw organisatie is geregistreerd in een specifiek land in de beheerportal van Office 365. De inschrijvingservaring voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt de taal en de landinstellingen die uw huidige browser gebruikt en daardoor kunt u de foutmelding krijgen hoewel u zich in een ondersteund land bevindt. Vraag de IT-beheerder om het land te verifiëren dat is opgegeven in het organisatieprofiel in de beheerportal van [Office 365](https://portal.office.com/adminportal/home#/companyprofile) U moet een ander account gebruiken voor [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Regionale beschikbaarheid
[!INCLUDE[d365fin](includes/d365fin_md.md)] is nu in de volgende markten verkrijgbaar:

*   Europa:
  * Oostenrijk
  * België
    * Denemarken
  * Duitsland
  * Finland
  * Frankrijk
  * Italië
  * Nederland
  * Spanje
  * Zweden
  * Zwitserland
  * Verenigd Koninkrijk
*   Noord-Amerika:
  * Canada
  * Verenigde Staten


## <a name="see-also"></a>Zie ook
[Welkom bij [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

