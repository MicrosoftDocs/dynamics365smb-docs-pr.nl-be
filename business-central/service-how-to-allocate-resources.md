---
title: Resources toewijzen | Microsoft Docs
description: U kunt het jaarlijkse bedrag van het servicecontract of de servicecontractofferte wijzigen om het bedrag te corrigeren dat jaarlijks wordt gefactureerd.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Resources toewijzen
Het belangrijkste element van servicebeheer bestaat uit de personen die de service uitvoeren. U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat de juiste personen aan de betreffende projecten worden toegewezen. Toewijzingen kunnen worden gebaseerd op serviceregio's waarin de personen zich bevinden of waarin de service plaatsvindt. U kunt resources ook groeperen in reactie op serviceaanvragen. Zie [Resourcetoewijzing instellen](service-how-setup-resource-allocation.md) voor meer informatie.

U kunt resources, bijvoorbeeld technici, toewijzen via het **planbord** of vanuit een serviceorder. U kunt de beschikbaarheid van resources gebruiken om resources toe te wijzen die de servicetaken in de orders of offertes moeten uitvoeren.

U kunt dezelfde resource, bijvoorbeeld een technicus, of resourcegroep toewijzen aan alle serviceartikelen in een serviceorder. Er worden toewijzingsposten gemaakt voor de andere serviceartikelen in de order met hetzelfde resourcenummer en dezelfde toewijzingsdatum als de regel die u hebt toegewezen. De toegewezen uren zijn de uren die u hebt toegewezen, gedeeld door het aantal serviceartikelen op de order. Het veld **Status** wordt automatisch ingesteld op **Actieve** voor alle posten die zijn gemaakt.

## Een overzicht weergeven van de serviceorders en serviceoffertes  
U hebt misschien vaak het overzicht nodig van serviceorders of serviceoffertes die voldoen aan bepaalde voorwaarden, zodat u specifieke acties er één voor één op kunt uitvoeren. U moet bijvoorbeeld resources toewijzen aan serviceorders van een bepaalde klant.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planbord** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het veld **Documentfilter** het soort documenten dat u wilt bekijken.
3. Als u een lijst met documenten wilt krijgen die servicetaken bevatten waaraan een bepaalde resource of resourcegroep is toegewezen, vult u de velden **Resourcefilter** en **Resourcegroepfilter** in en drukt u op <kbd>Enter</kbd>.  
4. Als u een lijst wilt krijgen met documenten met een bepaalde responsdatum of responsdatums binnen een bepaalde periode, vult u het veld **Responsdatumfilter** in en drukt u op <kbd>Enter</kbd>.  
5. Als u een lijst wilt krijgen met documenten met een bepaalde toewijzings- of documentstatus, vult u het veld **Toewijzingsfilter/Statusfilter** in en drukt u op <kbd>Enter</kbd>.  
6. Als u een lijst wilt krijgen met documenten die bij een bepaald(e) contract/klant/zone horen, vult u het veld **Contractfilter/Klantfilter/Zonefilter** in en drukt u op <kbd>Enter</kbd>.  
7. Kies een regel die bij een serviceorder of -offerte hoort en kies de actie **Document weergeven**.  

    De pagina **Serviceorder** of **Serviceofferte** wordt geopend en u kunt werken met het document. Klik op **OK** om terug te keren naar de pagina **Planbord**.

## Resources toewijzen op basis van resource- of resourcegroepbeschikbaarheid    
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planbord** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de serviceorder en kies vervolgens de actie **Resourcetoewijzingen**.  
3. Kies de post met de servicetaak waaraan u een resource wilt toewijzen.  
4. Kies de actie **Resourcebeschikbaarheid** of **Res.-groepbeschikbaarheid**.  
5. Op de pagina **Res.-beschikbaarheid (Service)** kiest u **Matrix weergeven**.  
6. Kies een resource om toe te wijzen. U kunt uw selectie baseren op bekwaamheid van de resource, op het feit of deze zich bevindt zich in de zone van de klant en/of de klant de voorkeur geeft aan deze resource.  
7. Geef een datum op waarop de resource voldoende beschikbare uren voor de taak heeft en die dicht bij de responsdatum van de serviceorder ligt.  
8. Voer in het veld **Toe te wijzen aantal** het aantal uren in waarvoor u de resource wilt toewijzen aan de servicetaak.  
9. Kies de actie **Toewijzen** om de geselecteerde resource op de geselecteerde datum toe te wijzen.  

     Het veld **Status** staat automatisch ingesteld op **Actief**.  

 Herhaal deze stappen voor elke datum waarvoor u de resource aan de servicetaak wilt toewijzen.  

> [!NOTE]  
>  Voor ieder serviceartikel op een serviceorder kunnen er slechts toewijzingsposten **Actief** zijn voor één resource of resourcegroep tegelijkertijd.  

## Resources toewijzen met een serviceorder  
Als u een serviceorder of contractofferte hebt gemaakt en ingevuld, kunt u resources, bijvoorbeeld technici, toewijzen voor het uitvoeren van servicetaken die zijn geregistreerd als serviceartikelregels in het document.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de serviceorder en kies **Bewerken**.  
3. Kies de serviceartikelregel die overeenkomt met de servicetaak waaraan u een resource wilt toewijzen.  
4. Kies **Resourcetoewijzingen**.
5. Kies op de pagina **Resourcetoewijzingen** een niet-actieve toewijzingspost met de servicetaak waaraan u de resource wilt toewijzen. Als de toewijzingspost niet bestaat, kunt u een nieuwe post maken door **Nieuw** te kiezen.  
7. Geef de servicetaak op door het veld **Serviceartikelnr.** op dezelfde regel in te vullen.  
8. Kies de resource in het veld **Resourcenr.** Als de resource deel uitmaakt van een resourcegroep, wordt het nummer van de resourcegroep automatisch ingevoerd in het veld **Resourcegroepnr**. te kiezen.  
9. Vul de velden **Toewijzingsdatum** en **Toegewezen uren** in. Het veld **Status** wordt ingesteld op de status **Actief**. Dit betekent dat de resource is toegewezen aan de servicetaak.  
10. U kunt de resource desgewenst aan alle artikelen toewijzen door **Aan alle serviceartikelen toewijzen** te kiezen.

> [!NOTE]  
>  Voor elk serviceartikel in een serviceorder kunnen er slechts actieve toewijzingsposten met één resource of resourcegroep tegelijkertijd zijn.

## Resources opnieuw toewijzen in een serviceorder  
U kunt resources rechtstreeks opnieuw toewijzen vanuit een serviceorder of serviceofferte wanneer u daarmee werkt. De oude post blijft bestaan, maar de status wordt als volgt bijgewerkt:  

* Als de service is begonnen terwijl de toewijzing de waarde **Actief** had, dat wil zeggen, als de herstelstatus van het serviceartikel in de post is gewijzigd in **In verwerking**, verandert de toewijzingsstatus van **Hertoewijzing vereist** in **Gereedgemeld**.  
* Als de service niet is gestart terwijl de toewijzing de waarde **Actief** heeft, verandert de toewijzingsstatus van **Hertoewijzing vereist** in **Geannuleerd**.  
* Bij het opnieuw toewijzen van een serviceorder die is ontstaan vanuit een offerte wordt de status van de geregistreerde toewijzingsposten voor de offerte altijd gewijzigd in **Gereedgemeld** tijdens het opnieuw toewijzen van de serviceartikelen in de serviceorder.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de betreffende serviceorder.  
3. Selecteer de serviceartikelregel die overeenkomst met de servicetaak waaraan u een resource wilt toewijzen en kies de actie **Resourcetoewijzingen** action.  
4. Selecteer op de pagina **Resourcetoewijzingen** een toewijzingspost met de servicetaak waaraan u de resource opnieuw wilt toewijzen. Selecteer de juiste resource in het veld **Resourcenr.**. Hiermee wordt de bestaande resource in het veld overschreven.  
5. Selecteer <kbd>Enter</kbd>. Er wordt een dialoogvenster geopend waarin u wordt gevraagd of u deze post opnieuw wilt toewijzen. Vul eventueel het veld **Redencode** in en klik op de knop **Ja** om de hertoewijzing te bevestigen.  
6. Vul de velden **Toewijzingsdatum** en **Toegewezen uren** in. De nieuwe resource is nu opgenomen in de post en de status is **Actief**.

## Resources opnieuw toewijzen met het planbord  
Als de resource die is toegewezen aan een servicetaak het werk niet kan uitvoeren, moet deze servicetaak opnieuw worden toegewezen. Meestal wijst u resources opnieuw toe aan een servicetaak met behulp van het **planbord**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planbord** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het veld **Toewijzingsfilter** de optie **Hertoewijzing vereist**. Op de pagina **Planbord** wordt nu de lijst met serviceorders weergegeven met servicetaken die u opnieuw moet toewijzen.  
3. Selecteer de desbetreffende serviceorder en kies de actie **Resourcetoewijzingen**. De pagina **Brontoewijzingen** wordt geopend.  
4. Selecteer de toewijzingspost met de servicetaak waaraan u opnieuw een resource wilt toewijzen.  
5. Selecteer de juiste resource in het veld **Resourcenr.**. Deze vervangt de bestaande resource in het veld.  
6. Selecteer <kbd>Enter</kbd>. Het dialoogvenster **Hertoewijzingspostredenen** wordt geopend waarin u wordt gevraagd of u wilt deze post opnieuw wilt toewijzen. Vul eventueel het veld **Redencode** in en klik op de knop **Ja** om de hertoewijzing te bevestigen.  
7.  Vul de velden **Toewijzingsdatum** en **Toegewezen uren** in. De nieuwe resource is nu opgenomen in de post en de status is **Actief**.  

    > [!NOTE]  
    >  De oude post bestaat nog steeds, maar de status wordt als volgt bijgewerkt:  
    >   
    >  * Als de service is begonnen terwijl de toewijzing de waarde **Actief** had, dat wil zeggen, als de herstelstatus van het serviceartikel in de post is gewijzigd in **In verwerking**, verandert de toewijzingsstatus van **Hertoewijzing vereist** in **Gereedgemeld**.  
    > * Als de service niet is gestart terwijl de toewijzing de waarde **Actief** heeft, verandert de toewijzingsstatus van **Hertoewijzing vereist** in **Geannuleerd**.  
    > * Bij het opnieuw toewijzen van een serviceorder die is ontstaan vanuit een offerte wordt de status van de geregistreerde toewijzingsposten voor de offerte altijd gewijzigd in **Gereedgemeld** tijdens het opnieuw toewijzen van de serviceartikelen in de serviceorder.  

## Resource-uren registreren  
Wanneer u werkt aan serviceartikelen in serviceorders, moet u de gebruikte resource-uren voor de service registreren. Met de volgende procedure wordt aangegeven hoe u de resource-uren op de pagina **Serviceartikelwerkbon** kunt registreren.  

U kunt dezelfde procedure gebruiken om uren te registreren op de pagina **Serviceregels** die u opent vanaf de pagina Serviceorder. Open de desbetreffende servicekaart en kies de actie **Serviceregels**.  

Als dezelfde resource werkt aan alle serviceartikelen in de serviceorder, hoeft u de totale resource-uren slechts voor één serviceartikel te registreren. Vervolgens kunt u de resourceregel opsplitsen om de resource-uren aan andere serviceartikelen toe te wijzen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel met het betreffende serviceartikel en kies de actie **Artikelwerkbon**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Een resource toewijzen aan alle serviceartikelen in een order
Als dezelfde resource, bijvoorbeeld een technicus, werkt aan alle serviceartikelen in de serviceorder, hoeft u de totale resource-uren slechts voor één serviceartikel te registreren. Vervolgens kunt u de resourceregel opsplitsen om de resource-uren aan andere serviceartikelen toe te wijzen.  

Met de volgende procedure wordt aangegeven hoe u resourceregels op de pagina **Servicefactuurregels** kunt opsplitsen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de betreffende serviceorder.  
3. Kies op het sneltabblad **Regels** de actie **Serviceregels**. De pagina **Serviceregels** wordt geopend.  
4. Selecteer de resourceregel die u wilt opsplitsen. De inhoud van het veld **Aantal** wordt verdeeld over alle serviceartikelen in de order.  
5. Kies de actie **Resourceregel splitsen**. Kies **Ja** om te bevestigen.  

    Er worden resourceregels gemaakt voor de andere serviceartikelen in de order met hetzelfde resourcenummer als de opgesplitste regel. Het aantal voor de opgesplitste regel, gedeeld door het aantal serviceartikelen in de order, levert het uiteindelijke aantal.  

## Toewijzingen annuleren  
U kunt resourcetoewijzingen voor servicetaken annuleren zonder de taken opnieuw toe te wijzen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planbord** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de serviceorder en kies vervolgens de actie **Resourcetoewijzingen**.  
3. Kies de toewijzingspost met de servicetaak waarvoor u de toewijzing wilt annuleren.  
4. Kies de actie **Toewijzing annuleren**.  
5. Kies de juiste redencode in het veld **Redencode**.  
6. Kies **Ja** om de annulering te bevestigen.  

    > [!NOTE]  
    > De optie **Hertoewijzing vereist** wordt automatisch geselecteerd in het veld **Status**. Als de herstelstatus van het serviceartikel in de post de waarde **Eerste** heeft, wordt de herstelstatus gewijzigd in **Toegewezen**, dat wil zeggen, er is nog geen service begonnen. Heeft de herstelstatus de waarde **In verwerking**, dan wordt de herstelstatus gewijzigd in **Deels service verleend**, dat wil zeggen, een deel van de service is voltooid.

## Zie ook
[Resourcetoewijzing instellen](service-how-setup-resource-allocation.md)  
[Toewijzingsstatus en herstelstatus](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]