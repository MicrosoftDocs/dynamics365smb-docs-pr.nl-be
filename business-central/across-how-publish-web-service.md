---
title: Objecten openstellen als webservices | Microsoft Docs
description: Publiceer objecten als webservices om ze meteen beschikbaar te maken voor uw Business Central-oplossing.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: c9f12f2b15c379ad1f4765f1a20e773150f33b84
ms.sourcegitcommit: d4a77522859c5561c1f3dc43178d45657ffa31b5
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3402465"
---
# <a name="publish-a-web-service"></a>Een webservice publiceren

Webservices zijn een lichtgewicht manier om toepassingsfunctionaliteit aan allerlei externe systemen en gebruikers beschikbaar te maken. [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal objecten die standaard als webservices worden opengesteld vanwege de integratie met andere Microsoft-services, maar u kunt ook andere webservices toevoegen.  

U stelt een webservice in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-cliënt in. U moet vervolgens de webservice publiceren zodat deze beschikbaar is voor service-aanvragen via het netwerk. Gebruikers kunnen controleren of webservices actief zijn door een browser te laten kijken naar de serverlocatie en een overzicht van de beschikbare services aan te vragen. Wanneer u een webservice publiceert, is deze onmiddellijk beschikbaar via het netwerk voor geverifieerde gebruikers. Alle bevoegde gebruikers hebben toegang tot metagegevens voor webservices, maar alleen gebruikers die beschikken over voldoende machtigingen hebben toegang tot de werkelijke gegevens.

## <a name="creating-and-publishing-a-web-service"></a>Een webservice maken en publiceren

In de volgende stappen wordt uitgelegd hoe u een webservice maakt en publiceert.  

### <a name="to-create-and-publish-a-web-service"></a>Een webservice maken en publiceren  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Webservices** in en kies de desbetreffende koppeling.  
2. Kies op de pagina **Webservices** de optie **Nieuw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** en **Pagina** zijn geldige typen voor SOAP-webservices. **Pagina** en **Query** zijn geldige typen voor OData-webservices.  
    > Als de database meerdere bedrijven bevat, kunt u een specifieke object-id voor een van de bedrijven kiezen.  
    > De servicenaam is zichtbaar voor consumenten die uw webservice gebruiken en is de basis voor het identificeren en onderscheiden van webservices. Zorg dus dat de naam duidelijk is.

3. Schakel het selectievakje in de kolom **Gepubliceerd** in.  

Wanneer u de webservice publiceert, ziet u in de velden **OData-URL** en **SOAP-URL** de URL's die voor de webservice zijn gegenereerd. U kunt de webservice direct controleren door de koppelingen in de velden **OData-URL** en **SOAP-URL** te kiezen. U kunt eventueel de waarde van het veld kopiëren en opslaan voor later gebruik.  

> [!NOTE]
> Als de objecten die u beschikbaar maakt als webservices, niet toegankelijk mogen zijn vanuit [!INCLUDE [prodshort](includes/prodshort.md)] online, moet u de methoden die in de code beschikbaar worden gemaakt, markeren als `[Scope('OnPrem')]`. Zie voor meer informatie [Bereikkenmerk](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Wanneer u een webservice publiceert, is deze beschikbaar voor externe partijen. U kunt de beschikbaarheid van de webservice verifiëren door een browser te gebruiken, of u kunt de koppeling in de velden **OData-URL** en **SOAP-URL** kiezen op de pagina **Webservices**. In de volgende procedure wordt beschreven hoe u de beschikbaarheid van de webservice kunt controleren voor later gebruik.  

### <a name="to-verify-the-availability-of-a-web-service"></a>De beschikbaarheid van een webservice verifiëren  

1. Voer in de browser de relevante URL in. De volgende tabel illustreert de soorten URL's die u kunt invullen voor verschillende soorten webservices.  

    > [!div class="mx-tdBreakAll"]
    > |Soort|Syntaxis|Voorbeeld|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    De bedrijfsnaam is hoofdlettergevoelig.|

2. Controleer de informatie die verschijnt in de browser. Controleer of u de naam ziet van de webservice die u hebt gemaakt.  

Als u toegang hebt tot een webservice en gegevens wilt terugschrijven naar [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de bedrijfsnaam opgeven. U kunt het bedrijf opgeven als onderdeel van URI zoals weergegeven in de volgende voorbeelden, of u kunt het bedrijf opgeven als onderdeel van de queryparameters. De volgende URI's wijzen bijvoorbeeld naar dezelfde OData-webservice en zijn beide geldige URI's.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  
[Business Central-webservices voor ontwikkelaars](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData-aanvraaglimieten](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
