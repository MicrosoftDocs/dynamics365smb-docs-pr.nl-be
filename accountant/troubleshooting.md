---
title: Manieren om problemen op te lossen of te omzeilen | Microsoft Docs
description: Leer hoe u problemen omzeilt in Accountant Hub voor Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.openlocfilehash: 0ebd99e9097e4c701038f3b8be7a07d1e80a4b31
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816593"
---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a>Problemen met [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)] oplossen
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Aanmelden bij [!INCLUDE [d365acc](includes/d365acc_md.md)] is eenvoudig en kan erg snel worden uitgevoerd. Het toevoegen van cliënten aan het dashboard is ook gemakkelijk, maar in dit artikel komen problemen aan bod die zich onderweg kunnen voordoen.

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a>Welk e-mailadres kan ik gebruiken voor [!INCLUDE [d365acc](includes/d365acc_md.md)]?
Voor [!INCLUDE [d365acc](includes/d365acc_md.md)] moet u voor aanmelding een e-mailadres van het werk of van school gebruiken. In [!INCLUDE [d365acc](includes/d365acc_md.md)] worden geen e-mailadressen ondersteund die worden geleverd door consumentene-mailservices of telecommunicatieproviders. Dit omvat outlook.com, hotmail.com, gmail.com en andere.  

Als u zich met een persoonlijk e-mailadres probeert aan te melden, ontvangt u een bericht dat u een e-mailadres van het werk of van school moet gebruiken.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Waarom kan ik geen verbinding maken met de gegevens van mijn cliënt?
Dit kan een aantal oorzaken hebben, waaronder de volgende:

- De URL in het veld **Cliënt-URL** is ongeldig  

  Ga naar **Cliënten beheren**, open de cliënt waarmee u geen verbinding kunt maken en kies **Cliënt-URL testen**.  
- Het bedrijf van de cliënt is momenteel offline, bijvoorbeeld als dit wordt bijgewerkt

  Kies in het dashboard de menuopdracht **Extra** en vervolgens **Fouten controleren**. Vervolgens wordt er een lijst met technische gegevens weergegeven. Als u fouten ziet, kunt u contact opnemen met uw beheerder. Het foutbericht De server heeft de cliëntreferenties geweigerd lijkt erop te wijzen dat u geen toegang hebt.  
- U hebt geen e-mail van uw cliënt ontvangen waarin u wordt uitgenodigd voor hun [!INCLUDE [d365fin](includes/d365fin_md.md)], u hebt de koppeling in de e-mail niet geopend of u hebt de uitnodiging niet geaccepteerd

  U moet de koppeling in de uitnodiging openen en de stappen accepteren waarmee u wordt toegevoegd aan de [!INCLUDE [d365fin](includes/d365fin_md.md)]-omgeving van uw cliënt. Tot die tijd hebt u geen toegang tot hun gegevens.  
- U hebt niet toegang tot alle bedrijven in de [!INCLUDE [d365fin](includes/d365fin_md.md)]-omgeving van uw cliënt

  Uw cliënt kan meerdere bedrijfsunits of bedrijven in [!INCLUDE [d365fin](includes/d365fin_md.md)] hebben opgenomen en uw uitnodiging omvat niet altijd alle bedrijven. Werk samen met uw cliënt om ervoor te zorgen dat u toegang hebt tot de juiste bedrijven.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Waarom worden de gegevens in mijn dashboard niet vernieuwd?
Wanneer u een cliënt toevoegt of om het vernieuwen van gegevens verzoekt, worden de gegevens opgehaald door [!INCLUDE [d365acc](includes/d365acc_md.md)]. U moet de pagina echter zelf vernieuwen, bijvoorbeeld door de actie Alle bedrijven opnieuw weergeven te kiezen, de browserpagina te vernieuwen of uit en vervolgens weer naar het dashboard te navigeren. Dit is een bekend probleem waarvoor we in een latere update hopelijk een oplossing kunnen bieden.  

## <a name="see-also"></a>Zie ook
[Aan de slag met [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Cliënten toevoegen aan uw dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
