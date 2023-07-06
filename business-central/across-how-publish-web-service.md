---
title: Objecten openstellen als webservices
description: Publiceer objecten als webservices om ze meteen beschikbaar te maken voor uw Business Central-oplossing.
author: edupont04
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="publish-a-web-service"></a><a name="publish-a-web-service"></a><a name="publish-a-web-service"></a>Een webservice publiceren

Webservices zijn een lichtgewicht manier om toepassingsfunctionaliteit aan allerlei soorten externe systemen en gebruikers beschikbaar te maken. Standaard stelt [!INCLUDE[prod_short](includes/prod_short.md)] een aantal objecten bloot als webservices voor een betere integratie met andere Microsoft-services. U kunt andere webservices toevoegen als uw bedrijf dit vereist.  

Stel een webservice in [!INCLUDE[prod_short](includes/prod_short.md)] in en publiceer vervolgens de webservice zodat deze beschikbaar is voor geverifieerde gebruikers. Alle bevoegde gebruikers hebben toegang tot metagegevens voor webservices, maar alleen gebruikers die beschikken over voldoende machtigingen hebben toegang tot de werkelijke gegevens.  

## <a name="creating-and-publishing-a-web-service"></a><a name="creating-and-publishing-a-web-service"></a><a name="creating-and-publishing-a-web-service"></a>Een webservice maken en publiceren

In de volgende stappen wordt uitgelegd hoe u een webservice maakt en publiceert.  

### <a name="to-create-and-publish-a-web-service"></a><a name="to-create-and-publish-a-web-service"></a><a name="to-create-and-publish-a-web-service"></a>Een webservice maken en publiceren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Webservices** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Webservices** de optie **Nieuw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** en **Pagina** zijn geldige typen voor SOAP-webservices. **Pagina** en **Query** zijn geldige typen voor OData-webservices. Vanaf versie 16.3, is **Codeunit** ook een geldig type voor OData v4-webservices, maar dan wordt er geen URL weergegeven in de gebruikersinterface. Als de database meerdere bedrijven bevat, kunt u een specifieke object-id voor een van de bedrijven kiezen.  
    > De servicenaam is zichtbaar voor consumenten die uw webservice gebruiken en is de basis voor het identificeren en onderscheiden van webservices. Zorg dus dat de naam duidelijk is.

3. Schakel het selectievakje in de kolom **Gepubliceerd** in.  

Wanneer u de webservice publiceert, bevatten de velden **OData-URL** en **SOAP-URL** de nieuwe URL's. Voor codeunits die worden weergegeven als ongebonden OData v4-acties, worden de URL-velden echter niet weergegeven.  

U kunt de webservice direct controleren door de koppelingen in de velden **OData-URL** en **SOAP-URL** te kiezen. U kunt eventueel de waarde van het veld kopiëren en opslaan voor later gebruik. Om codeunits te testen die worden weergegeven als ongebonden OData v4-acties, volgt u de instructies in de sectie [Beschikbaarheid van webservice verifiëren](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) in de ontwikkelaarscontent.

> [!NOTE]
> Als de objecten die u beschikbaar maakt als webservices, niet toegankelijk mogen zijn vanuit [!INCLUDE[prod_short](includes/prod_short.md)] online, moet u de methoden die in de code beschikbaar worden gemaakt, markeren als `[Scope('OnPrem')]`. Zie voor meer informatie [Bereikkenmerk](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Wanneer u een webservice publiceert, is deze beschikbaar voor externe partijen. U kunt de beschikbaarheid van die webservice verifiëren door een browser te gebruiken of u kunt de koppeling in de velden **OData-URL** en **SOAP-URL** kiezen op de pagina **Webservices**. In de volgende procedure wordt beschreven hoe u de beschikbaarheid van de webservice kunt controleren voor later gebruik.  

### <a name="to-verify-the-availability-of-a-web-service"></a><a name="to-verify-the-availability-of-a-web-service"></a><a name="to-verify-the-availability-of-a-web-service"></a>De beschikbaarheid van een webservice verifiëren

1. Voer in de browser de relevante URL in. De volgende tabel illustreert de soorten URL's die u kunt invullen voor verschillende soorten webservices.  

    > [!div class="mx-tdBreakAll"]
    > |Soort|Syntaxis|Voorbeeld|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    De bedrijfsnaam is hoofdlettergevoelig.|

2. Controleer de informatie die verschijnt in de browser. Controleer of u de naam ziet van de webservice die u hebt gemaakt.  

Als u toegang hebt tot een webservice en gegevens wilt terugschrijven naar [!INCLUDE[prod_short](includes/prod_short.md)], moet u de bedrijfsnaam opgeven. U kunt het bedrijf opgeven als onderdeel van de URI zoals weergegeven in de volgende voorbeelden, of u kunt het bedrijf opgeven als onderdeel van de queryparameters. De volgende URI's wijzen bijvoorbeeld naar dezelfde OData-webservice en zijn beide geldige URI's.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Beheer](admin-setup-and-administration.md)  
[Business Central-webservices voor ontwikkelaars](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData-aanvraaglimieten](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
