---
title: 'Procedure: artikelen opslaan met magazijnopslag'
description: Hier vindt u meer informatie over de verschillende manieren om magazijnopslag te gebruiken om ontvangen artikelen op te slaan.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Artikelen opslaan met magazijnopslag

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Lees meer op [Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

Dit artikel verwijst naar methode D in de tabel en gaat ervan uit dat de ontvangst al heeft plaatsgevonden. Zie voor meer informatie [Artikelen ontvangen](warehouse-how-receive-items.md).

Wanneer voor een vestiging magazijnopslag- en -ontvangstverwerking is vereist, beheert u de opslag van artikelen met de functie voor magazijnopslagdocumenten. Wanneer u een magazijnontvangst boekt, worden brondocumenten zoals inkooporders, inkomende transferorders of verkoopretourorders bijgewerkt. Het ontvangen aantal wordt in het artikeldagboek geboekt en de regels voor de ontvangen artikelen worden naar de opslagfunctie in het magazijn verzonden.

Afhankelijk van de waarde in het veld **Opslagvoorstel gebruiken** op de **Vestigingskaart**, worden de regels beschikbaar gesteld voor het opslagvoorstel of worden ze gebruikt om onmiddellijk opslagdocumenten te genereren. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

Naast de standaard manieren waarop magazijnopslag gemaakt kan worden die in dit artikel worden beschreven, kunt u opslag maken vanuit de bijbehorende geboekte magazijnontvangst. Dit is nuttig als u opslagregels hebt verwijderd of als u het opslagvoorstel niet wilt gebruiken omdat u opslaginstructies (opnieuw) kunt maken van de geboekte ontvangstregels.

## <a name="zone-and-bin-codes"></a>Zone- en opslaglocatiecodes

Op vestigingen die zijn ingesteld voor gestuurde opslag en pick, zijn de volgende instellingen vereisten om te bepalen wat de beste plek voor het plaatsen van de artikelen is:  

* Er wordt een opslagsjablonen ingesteld. Zie voor meer informatie [Opslagsjablonen instellen](warehouse-how-to-set-up-put-away-templates.md).  
* Het gewicht, de kubieke inhoud en de speciale opslagvereisten van het artikel of de SKU worden opgegeven.
* De capaciteit, het soort en de rangorde van de opslaglocaties worden gedefinieerd.  

De opslaglocatievolgorde wordt gebruikt wanneer meerdere opslaglocaties voldoen aan de opslagsjablooncriteria. Als meerdere opslaglocaties voldoen aan de criteria van de opslagsjabloon en dezelfde rang in de opslaglocatievolgorde hebben, wordt de opslaglocatie met het hoogste opslaglocatienummer gebruikt.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Bulksgewijs opslagdocumenten maken met het opslagvoorstel

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

U kunt opslagdocumenten voor meerdere ontvangsten tegelijk maken op de pagina **Opslagvoorstel**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslagvoorstellen** in en kies de gerelateerde koppeling.  
2. Kies de actie **Magazijndocumenten ophalen**. De pagina **Opslagselectie** verschijnt.  

    De lijst bevat alle geboekte ontvangsten die klaar zijn om opgeslagen te worden, inclusief die waarvoor al opslaginstructies zijn gemaakt. De lijst bevat geen documenten met opslagregels die volledig zijn uitgevoerd en geregistreerd.  
3. Selecteer de documenten waaraan u wilt werken. U kunt tegelijkertijd werken aan regels uit verschillende documenten.  

    > [!NOTE]  
    > Als u een ontvangstdocument of interne-opslagdocument selecteert waarvoor u al instructies hebt gemaakt voor alle regels, meldt [!INCLUDE[prod_short](includes/prod_short.md)]] dat er niets is om te verwerken.  

4. Vul het veld **Sorteermethode** in om de regels te sorteren.  

    > [!NOTE]  
    > De manier waarop de regels in het werkblad worden gesorteerd, wordt niet automatisch doorgevoerd in de opslaginstructie. Er zijn echter dezelfde mogelijkheden voor sorteren en opslaglocatievolgorde. U kunt de regelvolgorde die u in het voorstel plant opnieuw maken wanneer u de opslaginstructies maakt of sorteert.

5. Vul het veld **Te verwerken aantal** in. Kies de actie **Te verwerken aantal autom. invullen** of vul de velden handmatig in.  
6. U kunt de regels zo nodig handmatig bewerken. U kunt bijvoorbeeld regels verwijderen als artikelen moeten worden opgeslagen in opslaglocaties die ver van elkaar liggen.  

    > [!NOTE]  
    > Wanneer u regels verwijdert, worden ze alleen uit dit voorstel verwijderd. Ze worden niet verwijderd uit de opslagselectie.  

7. Kies de actie **Opslag maken**. De pagina **Document maken** wordt geopend, waar u informatie kunt toevoegen aan de opslaginstructies die u aan het maken bent.  

    * U kunt de opslaginstructie toewijzen aan een bepaalde magazijnmedewerker.  
    * U kunt de regels met opslaginstructies sorteren als in het werkblad of door middel van rangschikking van opslaglocaties. Wanneer u sorteert op volgorde van opslaglocaties, verschijnen de regels voor *Nemen* als eerste, omdat de meeste ontvangstopslaglocaties de volgorde 0 hebben. De regels voor *Plaatsen* verschijnen als laatste, te beginnen met de opslaglocaties met de laagste volgorde. Indien u uw magazijn hebt gestructureerd zodat opslaglocaties met een soortgelijke opslaglocatie-rangschikking bij elkaar staan, bespaart het sorteren van regels op deze manier stappen voor magazijnmedewerkers.  
    * U kunt ervoor kiezen de regels die [!INCLUDE [prod_short](includes/prod_short.md)] heeft gemaakt bij de conversie van een grote maateenheid naar kleinere maateenheden niet op te nemen door het veld **Breakbulkfilter plaatsen** te selecteren. Zie voor meer informatie over breakbulk [Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * U kunt het veld **Te verwerken aantal** op de opslaginstructies automatisch laten invullen.  
    * Indien gewenst kunt u het document direct afdrukken.  

8. Kies **OK** om de opslag te maken.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Een magazijnopslag maken vanuit een geboekte ontvangst

Als bij een vestiging zowel opslagverwerking als ontvangstverwerking wordt gebruikt en u opslagregels hebt verwijderd, of als u gestuurde opslag en pick gebruikt en het opslagwerkblad niet wilt gebruiken, kunt u opslaginstructies (opnieuw) maken voor de geboekte ontvangstregels.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte magazijnontvangsten** in en kies de gerelateerde koppeling  
2. Selecteer een geboekte ontvangst om op te slaan.  
3. Kies de actie **Kaart**.  

    Als het veld **Documentstatus** leeg is, is de ontvangst nog niet opgeslagen. Anders geeft het veld aan dat of ontvangst gedeeltelijk of volledig opslaan betreft.  

4. Als de ontvangst gedeeltelijk is opgeslagen of nog niet is opgeslagen, kiest u de actie **Opslag maken**.  
5. Vul de overige velden desgewenst in en kies **OK**.  

## <a name="to-put-items-away"></a>Artikelen opslaan

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnopslag** in en kies de gerelateerde koppeling.

2. Open de magazijnopslag die klaar is om te verwerken.  
3. Voer indien dit voor uw magazijn vereist is uw gebruikers-id in wanneer u aan een opslag begint.  

    U kunt de opslagregels op grond van diverse criteria sorteren, bijvoorbeeld op artikel, schapnummer of vervaldatum. Sorteren kan helpen bij het optimaliseren van het opslagproces, bijvoorbeeld:

    * Als de regels voor Nemen en Plaatsen op de ontvangstregels niet opeenvolgend worden weergegeven, kunt u de regels sorteren door **Artikel** te selecteren in het veld **Sorteermethode**.  
    * Als de volgorde van de opslaglocaties de fysieke indeling van het magazijn weerspiegelt, gebruikt u de sorteermethode **Opslaglocatievolgorde** om het werk volgens de opslaglocaties te organiseren.

  > [!NOTE]  
  > Regels worden in oplopende volgorde gesorteerd op de geselecteerde criteria. Als u op document sorteert, wordt er eerst gesorteerd op documenttype op basis van het veld **Brondocument magazijnactiviteit**. Als u op verzending sorteert, wordt er eerst gesorteerd op bestemming op basis van het veld **Type magazijnbestemming**.

4. Voer de acties uit.

    Als een opslaglocatie verplicht is voor de vestigingen, wordt elke ontvangstregel als volgt minimaal twee regels in de magazijnopslag.  

    * De eerste regel met **Nemen** in het veld **actiesoort** geeft aan waar de artikelen zich in het ontvangstgebied bevinden. U kunt de zone en de opslaglocatie op deze regel niet wijzigen.  
    * De volgende regel met **Plaatsen** in het veld **Actiesoort** geeft aan waar u de artikelen in het magazijn moet plaatsen. Als u een groot aantal artikelen via één ontvangstregel ontvangt, moeten de artikelen mogelijk op verschillende opslaglocaties worden opgeslagen en wordt er een Plaatsen-regel voor elke opslaglocatie weergegeven. 

    > [!NOTE]
    > Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.

5. Als u alle artikelen volgens de instructies op de opslaglocaties hebt geplaatst, kiest u de actie **Opslag registreren**.  

## <a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
