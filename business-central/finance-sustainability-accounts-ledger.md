---
title: Diagram van duurzaamheidsrekeningschema en -grootboek
description: 'Leer hoe u duurzaamheidsrekeningschema, rekeningcategorieën en subcategorieën beheert en details over duurzaamheidsgrootboekposten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="chart-of-sustainability-accounts-and-ledger"></a>Diagram van duurzaamheidsrekeningschema en -grootboek

## <a name="chart-of-sustainability-accounts"></a>Duurzaamheidsrekeningschema

Het **Duurzaamheidsrekeningschema** (CoSA) vormt de fundamentele gestructureerde lijst die wordt gebruikt voor het vastleggen van alle uitstootgegevens. Het functioneert als een raamwerk dat duurzaamheidsrekeningen categoriseert en organiseert op basis van hun kenmerken, zoals reikwijdte of andere groeperingen. Aan elke rekening wordt doorgaans een unieke code of nummer toegewezen, zodat u deze gemakkelijk kunt raadplegen en volgen. Deze volgt dezelfde structuur als een traditioneel **rekeningschema** maar is specifiek aangepast voor het monitoren van duurzaamheidsgerelateerde gegevens en meetgegevens binnen een organisatie. 
 
Gebruikers kunnen **Rekeningcategorieën** en **Subcategorieën** toevoegen om te definiëren hoe het systeem zich gedraagt, door speciale uitstoot te selecteren voor tracking, emissiefactoren, formules en vergelijkbare configuraties.  

>[!NOTE]
>Om vertrouwd te raken met bereiken, zijn er, gebaseerd op de normen voor broeikasgassen, drie uitstootbereiken:  
>- **Scope 1-emissies**: omvat emissies die worden uitgestoten door stationaire en mobiele verbranding, en door onbedoelde vluchtige uitstoot. 
>- **Scope 2-emissies**: omvatten indirecte uitstoot van de opwekking van energie die wordt ingekocht bij nutsbedrijven. 
>- **Scope 3-emissies**: omvatten een breed spectrum aan uitstoot, van gekochte goederen en diensten en kapitaalgoederen, brandstof- en energiegerelateerde activiteiten, upstream- en downstream-transport, geproduceerd afval, zakenreizen en woon-werkverkeer van medewerkers, enzovoort. 

Vanuit het **Duurzaamheidsrekeningschema** kunt u onder andere het volgende doen:  

-   Rapporten weergeven waarin duurzaamheidsgrootboekposten en -saldi worden weergegeven. 
-   Het **Duurzaamheidsrekeningschema** openen om instellingen toe te voegen of te wijzigen.  
-   De categorie en subcategorie voor die rekening weergeven.   
-   Afzonderlijke saldi voor elk van de emissies voor één rekening weergeven. 
-   Enkele of meerdere **Dimensies** toevoegen aan elk van de rekeningen en het dimensiefilter instellen. 
    
U kunt **duurzaamheidsrekeningen** toevoegen, wijzigen of verwijderen. Om discrepanties te voorkomen kunt u echter een **Duurzaamheidsrekening** niet verwijderen als er een of meer grootboekposten aan deze rekening zijn gekoppeld.  

### <a name="add-or-change-accounts"></a>Rekeningen toevoegen of wijzigen

1. Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsrekeningschema** in en selecteer de gerelateerde koppeling. 
2. Op de pagina **Duurzaamheidsrekeningschema** (CoSA) kunt u elke **duurzaamheidsrekening** openen en vervolgens instellingen toevoegen of veranderen. Wijs een veld aan om een korte omschrijving te lezen. 

Voor rekeningen van het rekeningsoort **Totaal** moet u het veld **Samentelling** invullen. Voor rekeningen met het soort **Eind-totaal** wordt dit veld automatisch ingevuld met de inspringfunctie. Nadat u alle rekeningen hebt ingesteld, kiest u de actie **Duurzaamheidsrekeningschema laten inspringen** om dat te doen.  

>[!IMPORTANT]
>Als u vóór het uitvoeren van de inspringfunctie definities hebt ingevoerd in de velden **Samentelling** voor rekeningen van het type **Eindtotaal**, moet u deze daarna nogmaals invoeren, omdat de functie de waarden in alle **Eindtotaal**-velden overschrijft.  

### <a name="delete-accounts"></a>Rekeningen verwijderen

U kunt een **duurzaamheidsrekening** verwijderen. Voordat u deze echter verwijdert, moet u er zeker van zijn dat er een of meer grootboekposten aan deze rekening zijn gekoppeld, aangezien Business Central voorkomt dat u een **Duurzaamheidsrekening** verwijdert in deze situatie.  

## <a name="account-categories"></a>Rekeningcategorieën

Gebruikers moeten de **Categorie van duurzaamheidsrekening** aan elk van de **Duurzaamheidsrekeningen** toevoegen om te definiëren hoe het systeem zich gedraagt en uitstootbereiken, speciale emissies voor tracking, formules en soortgelijke configuraties selecteren.  

Volg de stappen om **Duurzaamheidsrekeningcategorieën** te bekijken: 

1.  Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Duurzaamheidsrekeningcategorieën** in en selecteer de gerelateerde koppeling. 
2.  Op de pagina **Duurzaamheidsrekeningcategorieën** kunt u de bestaande lijst bewerken of een nieuwe categorie maken. Om een nieuwe categorie te maken selecteert u de actie **Nieuw**.  
3.  Vul de velden **Code** en **Omschrijving** in.   
4.  Stel het veld **Uitstootbereik** in en kies een van de bereikopties.  
5.  Selecteer de gasuitstoot die u wilt volgen. Momenteel kunt u een van de volgende opties gebruiken: **CO2**, **CH4** of **N2O**. U kunt elke combinatie kiezen die u wilt volgen, maar u moet minimaal één uitstoot hebben om te volgen.  
6.  In het veld **Berekeningsbasis** kunt u een van de formules kiezen die u wilt gebruiken voor het geval u de nauwkeurige uitstoothoeveelheid niet weet. Hier kunt u de berekeningsbasis (formule) opgeven voor uitstootberekening. U kunt een van de volgende opties kiezen: **Brandstof/elektriciteit**, **Afstand**, **Installatie** of **Aangepast**. 
7.  Als u **Aangepaste** formule kiest, kunt u een aangepaste beschrijving configureren in het veld **Aangepaste waarde**.  

>[!NOTE]
>Als deze reeks aangeboden formules in het veld **Berekeningsbasis** niet voldoende is, kunt u dit veld uitbreiden en meer berekeningen toevoegen aan het systeem die in de **Duurzaamheidsdagboeken** moeten worden gebruikt.  

Als u gebruik maakt van de **Berekeningsbasis** (formules) is er een uitleg hoe het systeem zal rekenen op basis van de optie die u hebt gekozen (**EF** is de **Uitstootfactor** die u kunt configureren op de pagina **Subcategorie van duurzaamheidsrekening**): 

|  Uitstoottype  |  Berekeningsbasis  |  Formule         | Opmerking      |
|------------|--------------|------------------------------|---------------------------------|
| **BEREIK 1**  |
| Stationaire verbranding | Brandstof/elektriciteit | Uitstoot = Brandstof * EF | _dat wil zeggen, brandstof = hoeveelheid brandstof die wordt gebruikt voor ketels, verwarmingstoestellen, thermische oxidatiemiddelen..._ |
| Mobiele verbranding | Brandstof/elektriciteit | Uitstoot = Brandstof * EF | _dat wil zeggen, brandstof = hoeveelheid brandstof die wordt verbruikt voor wegvoertuigen, of the road-voertuigen, spoorwegen..._ |
|  |  |  Uitstoot = Afstand * EF | _dat wil zeggen Afstand = Kilometerstand van wegvoertuigen, off the road-voertuigen, spoor..._ |
| Vluchtige uitstoot | Installatie | Uitstoot = Installatievermenigvuldiger * Aangepast bedrag / 100 * tijdfactor | _dat wil zeggen Aangepast bedrag = Assemblageverliezen, Jaarlijks lekpercentage..._ |
| **BEREIK 2**  |
| Nutsbedrijven | Brandstof/elektriciteit | Uitstoot = Elektriciteit * EF | _dat wil zeggen Brandstof/elektriciteit =hoeveelheid elektriciteit, hoeveelheid stoom, verwarmingseenheid..._ |
|  | Aangepast | Uitstoot = Aangepast bedrag * EF | _dat wil zeggen Aangepast bedrag = thermische eenheid, ton-uur..._ |
| **BEREIK 3**  |
| Gekochte goederen en diensten, en kapitaalgoederen | Aangepast | Uitstoot = Aangepast bedrag * EF | _dat wil zeggen, Aangepast bedrag = Kosten (GB)..._ |
| Stroomopwaarts transport en distributie | Afstand | Uitstoot = Afstand * EF |  |
|  | Afstand | Uitstoot = Afstand * Vermenigvuldiger * EF | _Vermenigvuldiger = Tonnen vracht_ |
| Stroomafwaarts transport en distributie | Afstand | Uitstoot = Afstand * EF |  |
|  | Afstand | Uitstoot = Afstand * Vermenigvuldiger * EF | _Vermenigvuldiger = Tonnen vracht_ |
| Afval gegenereerd tijdens de bedrijfsvoering en de verwerking aan het einde van de levensduur van verkochte producten | Aangepast | Uitstoot = Aangepast bedrag * EF | _dat wil zeggen Aangepast bedrag = Afval_ |
| Zakenreizen en woon-werkverkeer van werknemers | Afstand | Uitstoot = Afstand * EF | _dat wil zeggen Afstand = Kilometerstand van de gebruikte bedrijfsauto, huurauto, trein, vlucht..._ |
|  | Aangepast | Uitstoot = Aangepast bedrag * EF | _dat wil zeggen Aangepast bedrag = hotelverblijven..._ |
|  | Brandstof/elektriciteit | Uitstoot = Brandstof * EF | _dat wil zeggen Brandstof = hoeveelheid brandstof die is verbruikt in de bedrijfswagen, huurauto..._ |

## <a name="account-subcategories"></a>Rekeningsubcategorieën

Gebruikers moeten de **Subcategorie van duurzaamheidsrekening** aan elk van de **Duurzaamheidsrekeningen** toevoegen om uitstootfactoren te definiëren die in de formules zullen worden gebruikt, maar dit is gebaseerd op de keuze voor het volgen van uitstoot in de **Categorie van duurzaamheidsrekening**.  

Volg de stappen om **Subcategorieën van duurzaamheidsrekening** te bekijken:  

1.  Selecteer het ![Lampje dat de functie Vertel me opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Subcategorieën van duurzaamheidsrekening** in en selecteer de gerelateerde koppeling. 
2.  Op de pagina **Subcategorieën van duurzaamheidsrekening** kunt u de bestaande lijst bewerken of een nieuwe categorie maken. Om een nieuwe categorie te maken selecteert u de actie **Nieuw**.  
3.  Vul de velden **Code** en **Omschrijving** in.   
4.  Op basis van de gasuitstoot die u wilt volgen in de **Categorie van duurzaamheidsrekening** en waarmee u deze subcategorie wilt verbinden, kunt u ook een of meer uitstootfactoren invullen: 

   - **Uitstoot CO2**: specificeert de uitstootfactor voor CO2-uitstoot.  
   - **Uitstoot CH4**: specificeert de uitstootfactor voor CH4-uitstoot. 
   - **Uitstoot N2O**: specificeert de uitstootfactor voor N2O-uitstoot.  

5.  Als deze subcategorie gerelateerd is aan hernieuwbare energie, selecteer dan het veld **Hernieuwbare energie**.   

>[!NOTE]
>De velden **Gegevens importeren** en **Importeren uit** zijn bedoeld voor potentiële integratie met externe systemen die gebruikt worden voor het verzamelen van uitstootfactoren, maar in **releasewave 1 van 2024** kunnen ze niet standaard als functie worden gebruikt.  

## <a name="sustainability-ledger-entries"></a>Duurzaamheidsposten

**Duurzaamheidsgrootboek** slaat de geschiedenis van alle geboekte duurzaamheidstransacties op, waarbij alle uitstootgegevens worden geordend volgens het **Duurzaamheidsrekeningschema en -grootboek**. Wanneer een gebruiker het **Duurzaamheidsdagboek** boekt, worden daar alle cruciale gegevens vastgelegd. Alle actieve rapporten worden gegenereerd op basis van de **Duurzaamheidsposten**.   

De gebruiker kan dit grootboek voor één specifieke rekening openen met de actie **Grootboekposten** op de pagina **Duurzaamheidsrekeningschema** of, om alle grootboekposten te openen, selecteert de gebruiker het ![lampje dat de functie Vertel mij opent 3.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Duurzaamheidsposten** in en selecteert u vervolgens de gerelateerde koppeling. Wijs een veld aan om een korte omschrijving te lezen.  

>[!IMPORTANT]
>Zodra u uw gegevens in het duurzaamheidsgrootboek hebt geboekt, kunt u ze niet meer verwijderen. Als u een fout hebt gemaakt, kunt u de omgekeerde transactie boeken met dezelfde gegevens, maar met een minteken voor het bedrag.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)    
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)
[Duurzaamheidsinstelling](finance-sustainability-setup.md)
[Procedure: uitstoot vastleggen](finance-sustainability-journal.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
