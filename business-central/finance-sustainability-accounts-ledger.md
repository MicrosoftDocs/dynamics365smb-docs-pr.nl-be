---
title: Duurzaamheidsrekeningschema en grootboek
description: 'Leer hoe u de duurzaamheidsrekeningschema''s, categorieën en subcategorieën beheert en details over duurzaamheidsgrootboekposten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="chart-of-sustainability-accounts-and-ledger"></a>Diagram van duurzaamheidsrekeningschema en -grootboek

## <a name="chart-of-sustainability-accounts"></a>Duurzaamheidsrekeningschema

Het duurzaamheidsrekeningschema (CoSA) vormt de fundamentele gestructureerde lijst die wordt gebruikt voor het vastleggen van alle uitstootgegevens. Het dient als een raamwerk dat duurzaamheidsrekeningen categoriseert en organiseert op basis van hun kenmerken, zoals de reikwijdte of andere groeperingen. Aan elke rekening wordt doorgaans een unieke code of nummer toegewezen, zodat u deze gemakkelijk kunt raadplegen en volgen. Het heeft dezelfde structuur als een traditioneel rekeningschema, maar is specifiek aangepast om duurzaamheidsgerelateerde gegevens en statistieken in een organisatie te monitoren.

Gebruikers kunnen duurzaamheidsrekeningcategorieën en duurzaamheidsrekeningsubcategorieën toevoegen om te definiëren hoe het systeem zich gedraagt. Op deze manier kunnen ze specifieke uitstoot selecteren om te volgen, emissiefactoren, formules en soortgelijke configuraties.

> [!NOTE]
> Op basis van de broeikasgasnormen (BKG) zijn er drie uitstootbereiken:
>
> - **Bereik 1-uitstoot**: omvat uitstoot van stationaire en mobiele verbranding, en van onbedoelde vluchtige uitstoot.
> - **Bereik 2-uitstoot**: omvat indirecte uitstoot van de opwekking van energie die wordt ingekocht bij nutsbedrijven.
> - **Bereik 3-uitstoot**: omvat een breed spectrum aan uitstoot, van gekochte goederen en diensten en kapitaalgoederen, brandstof- en energiegerelateerde activiteiten, upstream- en downstream-transport, geproduceerd afval, zakenreizen en woon-werkverkeer van medewerkers, enzovoort.

Vanuit het duurzaamheidsrekeningschema kunt u onder andere het volgende doen:

- Rapporten weergeven waarin duurzaamheidsgrootboekposten en -saldi worden weergegeven.
- De duurzaamheidsrekeningkaart openen om instellingen toe te voegen of te wijzigen.
- De categorie en subcategorie voor die rekening weergeven. 
- Afzonderlijke saldi voor elke uitstoot voor één rekening weergeven.
- Afzonderlijke of meerdere dimensies toevoegen aan elke rekening en dimensiefilters instellen.

U kunt duurzaamheidsrekeningen toevoegen, wijzigen of verwijderen. Om discrepanties te voorkomen kunt u echter een duurzaamheidsrekening niet verwijderen als er een of meer grootboekposten aan deze rekening zijn gekoppeld.

### <a name="add-or-change-accounts"></a>Rekeningen toevoegen of wijzigen

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsrekeningschema** in en selecteer de gerelateerde koppeling.
2. Op de pagina **Duurzaamheidsrekeningschema** kunt u elke duurzaamheidsrekening openen en vervolgens instellingen toevoegen of veranderen. Wijs een veld aan om een korte omschrijving te lezen.

Voor rekeningen van het rekeningsoort **Totaal** moet u het veld **Samentelling** instellen.

Voor rekeningen van het type **Eindtotaal** stelt de functie Inspringen automatisch het veld **Samentelling** in. Nadat u alle rekeningen heeft ingesteld, selecteert u de actie **Duurzaamheidsrekeningschema laten inspringen** om de functie Inspringen uit te voeren en het veld **Samentelling** in te vullen.

> [!IMPORTANT]
> De functie Inspringen overschrijft de waarde van alle velden voor **Eindtotaal**-rekeningen. Als u definities in de velden **Samentelling** voor **Eindtotaal**-rekeningen hebt ingevoerd voordat u de inspringfunctie uitvoerde, moet u deze daarna daarom opnieuw invoeren.

### <a name="delete-accounts"></a>Rekeningen verwijderen

U kunt een duurzaamheidsrekening verwijderen. U moet er echter eerst voor zorgen dat er geen grootboekposten aan zijn gekoppeld. Business Central voorkomt dat u een duurzaamheidsrekening verwijdert als er een of meer grootboekposten aan zijn gekoppeld.

## <a name="account-categories"></a>Rekeningcategorieën

Gebruikers moeten een duurzaamheidsrekeningcategorie aan elke duurzaamheidsrekening toevoegen om te definiëren hoe het systeem zich gedraagt. Ze kunnen uitstootbereiken selecteren, specifieke uitstoot om formules en soortgelijke configuraties bij te houden.

Volg de stappen om duurzaamheidsrekeningcategorieën te bekijken:

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsrekeningcategorieën** in en selecteer de gerelateerde koppeling.
2. Op de pagina **Duurzaamheidsrekeningcategorieën** kunt u de bestaande lijst bewerken of een nieuwe categorie maken. Om een nieuwe categorie te maken selecteert u de actie **Nieuw**.
3. Stel de velden **Code** en **Omschrijving** in.
4. Selecteer in het veld **Uitstootbereik** een van de bereikopties.
5. Selecteer de gasuitstoot die u wilt volgen. Momenteel zijn de volgende opties beschikbaar: **CO2**, **CH4** en **N2O**. U kunt elke combinatie selecteren die u wilt volgen, maar u moet minimaal één uitstoot selecteren.
6. In het veld **Berekeningsbasis** kunt u de berekeningsgrondslag (formule) selecteren die u voor uitstootberekeningen wilt gebruiken als u de nauwkeurige uitstoothoeveelheid niet kent. U kunt een van de volgende opties selecteren: **Brandstof/elektriciteit**, **Afstand**, **Installatie** of **Aangepast**.

    > [!NOTE]
    > Als de set beschikbare formules in het veld **Berekeningsbasis** niet voldoende is, kunt u dit veld uitbreiden en meer berekeningen toevoegen aan het systeem die in de Duurzaamheidsdagboeken moeten worden gebruikt.

7. Als u **Aangepast** hebt geselecteerd in het veld **Berekeningsbasis**, kunt u een aangepaste beschrijving configureren in het veld **Aangepaste waarde**.

Als u het veld **Berekeningsbasis** instelt, legt de volgende tabel uit hoe het systeem uitstoot berekent op basis van de optie die u hebt geselecteerd. (In deze tabel vertegenwoordigt *EF* de **Uitstootfactor** die u kunt configureren op de pagina **Subcategorie van duurzaamheidsrekening**.)

| Uitstoottype | Berekeningsbasis | Formule | Opmerking |
|---------------|------------------------|---------|---------|
| **Bereik 1** | | | |
| Stationaire verbranding | Brandstof/elektriciteit | *Uitstoot* = *Brandstof* &times; *EF* | *Brandstof* = Hoeveelheid brandstof, dat wil zeggen voor ketels, verwarmingstoestellen, thermische oxidatiemiddelen, enzovoort |
| Mobiele verbranding | Brandstof/elektriciteit | *Uitstoot* = *Brandstof* &times; *EF* | *Brandstof* =Hoeveelheid brandstof die wordt verbruikt voor wegvoertuigen, off the road-voertuigen, spoorwegen, enzovoort |
| | | *Uitstoot* = *Afstand* &times; *EF* | *Afstand* = Kilometerstand van wegvoertuigen, off the road-voertuigen, spoor, enzovoort |
| Vluchtige uitstoot | Installatie | *Uitstoot* = *Installatievermenigvuldiger* &times; *Aangepast bedrag* &divide; 100 &times; *Tijdfactor* | *Aangepast bedrag* = Assemblageverliezen, Jaarlijks lekpercentage, enzovoort |
| **Bereik 2** | | | |
| Nutsbedrijven | Brandstof/elektriciteit | *Uitstoot* = *Elektriciteit* &times; *EF* | *Brandstof/elektriciteit* =Hoeveelheid elektriciteit, hoeveelheid stoom, verwarmingseenheid, enzovoort |
| | Aangepast | *Uitstoot* = *Aangepast bedrag* &times; *EF* | *Aangepast bedrag* = Thermische eenheid, ton-uur, enzovoort |
| **Bereik 3** | | | |
| Gekochte goederen en diensten, en kapitaalgoederen | Aangepast | *Uitstoot* = *Aangepast bedrag* &times; *EF* | *Aangepast bedrag* = Kosten (GB), enzovoort |
| Stroomopwaarts transport en distributie | Afstand | *Uitstoot* = *Afstand* &times; *EF* | |
| | Afstand | *Uitstoot* = *Afstand* &times; *Vermenigvuldiger* &times; *EF* | *Vermenigvuldiger* = Tonnen vracht |
| Stroomafwaarts transport en distributie | Afstand | *Uitstoot* = *Afstand* &times; *EF* | |
| | Afstand | *Uitstoot* = *Afstand* &times; *Vermenigvuldiger* &times; *EF* | *Vermenigvuldiger* = Tonnen vracht |
| Afval gegenereerd tijdens de bedrijfsvoering en de verwerking aan het einde van de levensduur van verkochte producten | Aangepast | *Uitstoot* = *Aangepast bedrag* &times; *EF* | *Aangepast bedrag* = Afval |
| Zakenreizen en woon-werkverkeer van werknemers | Afstand | *Uitstoot* = *Afstand* &times; *EF* | *Afstand* = Kilometerstand van de gebruikte bedrijfsauto, huurauto, trein, vlucht, enzovoort |
| | Aangepast | *Uitstoot* = *Aangepast bedrag* &times; *EF* | *Aangepast bedrag* = hotelverblijven |
| | Brandstof/elektriciteit | *Uitstoot* = *Brandstof* &times; *EF* | *Brandstof* = hoeveelheid brandstof die is verbruikt in de bedrijfswagen, enzovoort |

## <a name="account-subcategories"></a>Rekeningsubcategorieën

Gebruikers moeten een duurzaamheidsrekeningsubcategorie aan elke duurzaamheidsrekening toevoegen. Deze subcategorie definieert de uitstootfactoren die in de formules worden gebruikt, op basis van de keuze voor het volgen van uitstoot in de duurzaamheidsrekeningcategorie.

Volg de stappen om duurzaamheidsrekeningsubcategorieën te bekijken:

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Subcategorieën van duurzaamheidsrekening** in en selecteer de gerelateerde koppeling. 
2. Op de pagina **Subcategorieën van duurzaamheidsrekening** kunt u de bestaande lijst bewerken of een nieuwe categorie maken. Om een nieuwe categorie te maken selecteert u de actie **Nieuw**.
3. Stel de velden **Code** en **Omschrijving** in.
4. Op basis van de gasuitstoot die u wilt volgen in de duurzaamheidsrekeningcategorie en waarmee u deze subcategorie wilt verbinden, kunt u ook een of meer uitstootfactoren instellen: 

    - **Uitstootfactor CO2**: de uitstootfactor voor uitstoot van kooldioxide (CO<sub>2</sub>).
    - **Uitstootfactor CH4**: de uitstootfactor voor uitstoot van methaan CO<sub>4</sub>.
    - **Uitstootfactor N2O**: de uitstootfactor voor uitstoot van lachgas (N<sub>2</sub>O).

5. Als de subcategorie gerelateerd is aan hernieuwbare energie, selecteer dan het veld **Hernieuwbare energie**.

> [!NOTE]
> De velden **Gegevens importeren** **Importeren van** zijn bedoeld voor mogelijke integratie met externe systemen die worden gebruikt om uitstootfactoren te verzamelen. Echter, in **releasewave 1 van 2024** kunnen deze velden standaard niet als een functie worden gebruikt.

## <a name="sustainability-ledger-entries"></a>Duurzaamheidsposten

Het duurzaamheidsgrootboek slaat de geschiedenis van alle geboekte duurzaamheidstransacties en ordent alle uitstootgegevens volgens het duurzaamheidsrekeningschema. Wanneer een gebruiker het duurzaamheidsdagboek boekt, worden daar alle cruciale gegevens vastgelegd. Alle actieve rapporten worden gegenereerd op basis van de duurzaamheidsposten.

Om dit grootboek voor één specifieke rekening te openen gebruikt u de actie **Grootboekposten** op de pagina **Duurzaamheidsrekeningschema**. Als u alle posten wilt zien, selecteert u het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Duurzaamheidsposten** in en selecteert u vervolgens de gerelateerde koppeling. Wijs een veld aan om een korte omschrijving te lezen.

> [!IMPORTANT]
> Nadat u uw gegevens in het duurzaamheidsgrootboek hebt geboekt, kunt u ze niet meer verwijderen. Als u een fout hebt gemaakt, kunt u de omgekeerde transactie boeken met dezelfde gegevens, maar met een minteken voor het bedrag.

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)  
[Duurzaamheidsinstelling](finance-sustainability-setup.md)  
[Procedure: uitstoot vastleggen](finance-sustainability-journal.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
