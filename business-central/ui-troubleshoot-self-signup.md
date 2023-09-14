---
title: Probleemoplossing met aanmelden bij Self-Service | Microsoft Docs
description: 'Meer informatie over de meest voorkomende redenen waarom u de inschrijving bij Business Central niet kunt voltooien, en manieren om het op te lossen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: bholtorf
---
# Probleemoplossing voor aanmelden bij Self-Service
Aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] is eenvoudig en kan erg snel worden uitgevoerd. U kunt een gratis account maken, zelfs als u een bestaande organisatie bent. In dit artikel worden problemen behandeld die u tijdens het aanmelden kunt tegenkomen.

## Welk e-mailadres kan ik gebruiken met Business Central?
Voor [!INCLUDE[prod_short](includes/prod_short.md)] moet u voor aanmelding een e-mailadres van het werk of van school gebruiken. In [!INCLUDE[prod_short](includes/prod_short.md)] worden geen e-mailadressen ondersteund die worden geleverd door consumentene-mailservices of telecommunicatieproviders. Dit omvat outlook.com, hotmail.com, gmail.com en andere.

Als u zich met een persoonlijk e-mailadres probeert aan te melden, ontvangt u een bericht dat u een e-mailadres van het werk of van school moet gebruiken.

## Problemen oplossen
In veel gevallen kunt u uw registratie voor [!INCLUDE[prod_short](includes/prod_short.md)] uitvoeren door het aanmeldingsproces te volgen. Er zijn echter verschillende redenen waarom u zich mogelijk niet kunt aanmelden bij de Self-Service. In de tabel hierna wordt een aantal van de meest voorkomende redenen samengevat waarom u de aanmelding niet kunt voltooien en worden manieren beschreven waarop u deze problemen kunt oplossen.

| Symptoom/foutmelding | Oorzaak en oplossing |
| --------------------- | -------------------- |
| Voor Microsoft 365-e-mailadressen die niet in een ondersteund land zijn geregistreerd, ontvangt u tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw land of regio wordt nog niet ondersteund.** |[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt momenteel alleen Microsoft 365 e-mailaccounts die zijn geregistreerd in een beperkt aantal markten. Zie voor meer informatie [Regionale beschikbaarheid](#regional-availability). |
| Persoonlijke e-mailadressen, zoals nancy@gmail.com, worden niet ondersteund. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**U hebt een persoonlijk e-mailadres ingevoerd: voer het e-mailadres van uw werk in zodat de gegevens van uw bedrijf veilig kunnen worden opgeslagen.**<br> of <br> **Dit ziet eruit als een persoonlijk e-mailadres. Voer uw werkadres in zodat we u met anderen in uw bedrijf kunnen verbinden. Maak u geen zorgen. Uw adres wordt met niemand gedeeld.** |In [!INCLUDE[prod_short](includes/prod_short.md)] worden geen e-mailadressen ondersteund die worden geleverd door consumentene-mailservices of telecommunicatieproviders. Om de aanmelding te voltooien moet u opnieuw proberen een e-mailadres te gebruiken dat door uw werk of school is toegewezen. Als u zich nog niet kunt aanmelden en bereid bent een geavanceerder instellingsproces uit te voeren, kunt u zich registreren voor een nieuw Microsoft 365-proefabonnement en dat e-mailadres voor aanmelding gebruiken. |
| .gov- of .mil-e-mailadressen U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] niet beschikbaar: [!INCLUDE[prod_short](includes/prod_short.md)] is momenteel niet beschikbaar voor gebruikers met .gov- of .mil-e-mailadressen. Gebruik een ander werke-mailadres of kom later nog eens terug.** <br>of <br>**Uw aanmelding kan niet worden voltooid. Het lijkt erop dat [!INCLUDE[prod_short](includes/prod_short.md)] momenteel niet beschikbaar is voor uw werk of school.** |[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt momenteel geen .gov- of .mil-adressen. |
| Self-Service-aanmelding is niet ingeschakeld. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw aanmelding kan niet worden voltooid. Uw IT-afdeling heeft aanmelding voor [!INCLUDE[prod_short](includes/prod_short.md)] uitgeschakeld. Neem contact op met de IT-afdeling om de aanmelding te voltooien.** <br>of <br> **Dit ziet eruit als een persoonlijk e-mailadres. Voer uw werkadres in zodat we u met anderen in uw bedrijf kunnen verbinden. Maak u geen zorgen. Uw adres wordt met niemand gedeeld.** |De IT-beheerder van uw organisatie heeft Self-Service-aanmelding voor [!INCLUDE[prod_short](includes/prod_short.md)] uitgeschakeld. Om aanmelding te voltooien neemt u contact op met uw IT-beheerder en vraagt u deze de instructies op [deze pagina](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) te volgen om bestaande gebruikers toe te staan zich aan te melden voor [!INCLUDE[prod_short](includes/prod_short.md)] en nieuwe gebruikers toe te staan deel te nemen aan uw bestaande tenant. U kunt dit probleem ook tegenkomen als u zich hebt aangemeld voor Microsoft 365 via een partner. |
| E-mailadres is geen Microsoft 365-ID. U ontvangt tijdens de aanmelding een bericht zoals het volgende:<br /><br />**We kunnen u niet vinden op contoso.com. Gebruikt u een andere ID op het werk of op school? Probeer daarmee aan te melden en als het niet werkt, neemt u contact op met de IT-afdeling.** |Uw organisatie gebruikt ID´s voor aanmelding bij Microsoft 365 en andere Microsoft-services die anders zijn dan uw e-mailadres. Uw e-mailadres kan bijvoorbeeld Nancy.Smith@contoso.com zijn, maar uw id is nancys@contoso.com. Om de aanmelding te voltooien, gebruikt u de ID die uw organisatie heeft toegewezen voor aanmelding bij Microsoft 365 of andere Microsoft-services. Als u niet weet wat dit is, neemt u contact op met uw IT-beheerder. Als u zich nog niet kunt aanmelden en een geavanceerder configuratieproces kunt uitvoeren, kunt u zich registreren voor een nieuw Microsoft 365-proefabonnement en dat e-mailadres voor aanmelding gebruiken. |
| Als het Microsoft 365-account is geregistreerd in een ondersteund land en u zich aanmeldt voor [!INCLUDE[prod_short](includes/prod_short.md)] terwijl u zich in een ander land bevindt, ontvangt u tijdens de aanmelding een bericht zoals het volgende:<br /><br />**Uw land of regio wordt nog niet ondersteund.**| Het abonnement op Microsoft 365 van uw organisatie is geregistreerd in een specifiek land in de beheerportal van Microsoft 365. De inschrijvingservaring voor [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de taal en de land/regio-instellingen die uw huidige browser gebruikt en daardoor kunt u de foutmelding krijgen hoewel u zich in een ondersteund land/regio bevindt. Vraag de IT-beheerder om het land te verifiëren dat is opgegeven in het organisatieprofiel in de [beheerportal van Microsoft 365](https://portal.office.com/adminportal/home#/companyprofile). U moet een ander account gebruiken voor [!INCLUDE[prod_short](includes/prod_short.md)].|

## Regionale beschikbaarheid

[!INCLUDE[prod_short](includes/prod_short.md)] is beschikbaar in een aantal landen of regio's met lokalisatie geleverd door Microsoft of een goedgekeurde lokalisatiepartner. Zie voor een volledige lijst van momenteel ondersteunde landen/regio's [Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

Voor een overzicht van momenteel ondersteunde markten voor Dynamics 365 raadpleegt u de presentatie [Internationale beschikbaarheid van Microsoft Dynamics 365](/dynamics365/get-started/availability). Voor een overzicht van de lokale functionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] raadpleegt u de landingspagina [Lokale functionaliteit](about-localization.md).  

## Zie ook

[Aanmelden voor een gratis Dynamics 365 Business Central-proefversie](trial-signup.md)  
[Veelgestelde vragen (FAQ) over Dynamics 365 Business Central-proefversie](trial-faq.md)  
[Welkom bij [!INCLUDE[prod_short](includes/prod_long.md)]](welcome.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lokale functionaliteit](about-localization.md)  
[Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Internationale beschikbaarheid van Microsoft Dynamics 365](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]