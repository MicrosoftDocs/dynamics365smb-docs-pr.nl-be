---
title: Objecten openstellen als webservices | Microsoft Docs
description: Publiceer objecten als webservices om deze direct beschikbaar te maken in het netwerk.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 428dc281d34c374940d0c3fd187dd8a1d3d3ad9b
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="publish-a-web-service"></a>Een webservice publiceren
Webservices zijn een lichtgewicht manier om toepassingsfunctionaliteit aan allerlei externe systemen en gebruikers beschikbaar te maken. [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal objecten die standaard als webservices worden opengesteld vanwege de integratie met andere Microsoft-services, maar u kunt ook andere webservices toevoegen.  

U kunt een webservice in de Windows-client of de webclient instellen. U moet vervolgens de webservice publiceren zodat deze beschikbaar is voor service-aanvragen via het netwerk. Gebruikers kunnen controleren of webservices actief zijn door een browser te laten kijken naar de serverlocatie en een overzicht van de beschikbare services aan te vragen. Wanneer u een webservice publiceert, is deze onmiddellijk beschikbaar via het netwerk voor geverifieerde gebruikers. Alle bevoegde gebruikers hebben toegang tot metagegevens voor webservices, maar alleen gebruikers die beschikken over voldoende machtigingen hebben toegang tot de werkelijke gegevens.

## <a name="creating-and-publishing-a-web-service"></a>Een webservice maken en publiceren  
In de volgende stappen wordt uitgelegd hoe u een webservice maakt en publiceert.  

### <a name="to-create-and-publish-a-web-service"></a>Een webservice maken en publiceren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Webservices** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies op de pagina **Webservices** de optie **Nieuw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Codeunit** en **Pagina** zijn geldige typen voor SOAP-webservices. **Pagina** en **Query** zijn geldige typen voor OData-webservices.  
    Als de database meerdere bedrijven bevat, kunt u een specifieke object-id voor een van de bedrijven kiezen.  
    De servicenaam is zichtbaar voor consumenten die uw webservice gebruiken en is de basis voor het identificeren en onderscheiden van webservices. Zorg dus dat de naam duidelijk is.

3.  Schakel het selectievakje in de kolom **Gepubliceerd** in.  

Wanneer u de webservice publiceert, ziet u in de velden **OData-URL** en **SOAP-URL** de URL's die voor de webservice zijn gegenereerd. U kunt de webservice direct controleren door de koppelingen in de velden **OData-URL** en **SOAP-URL** te kiezen. U kunt eventueel de waarde van het veld kopiëren en opslaan voor later gebruik.  

Wanneer u een webservice publiceert, is deze beschikbaar voor externe partijen. U kunt de beschikbaarheid van de webservice verifiëren door een browser te gebruiken, of u kunt de koppeling in de velden **OData-URL** en **SOAP-URL** kiezen in het venster **Webservices**. In de volgende procedure wordt beschreven hoe u de beschikbaarheid van de webservice kunt controleren voor later gebruik.  

### <a name="to-verify-the-availability-of-a-web-service"></a>De beschikbaarheid van een webservice verifiëren  

1.  Voer in de browser de relevante URL in. De volgende tabel illustreert de soorten URL's die u kunt invullen voor verschillende soorten webservices.  
> [!div class="mx-tdBreakAll"]
> |Type|Syntaxis|Opmerking|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    De bedrijfsnaam is hoofdlettergevoelig.|

2.  Controleer de informatie die verschijnt in de browser. Controleer of u de naam ziet van de webservice die u hebt gemaakt.  

Als u toegang hebt tot een webservice en gegevens wilt terugschrijven naar [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de bedrijfsnaam opgeven. U kunt het bedrijf opgeven als onderdeel van URI zoals weergegeven in de volgende voorbeelden, of u kunt het bedrijf opgeven als onderdeel van de queryparameters. De volgende URI's wijzen bijvoorbeeld naar dezelfde OData-webservice en zijn beide geldige URI's.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Zie ook  
[Installatie en beheer](admin-setup-and-administration.md)  

