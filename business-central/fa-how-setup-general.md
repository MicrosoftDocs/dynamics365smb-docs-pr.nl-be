---
title: Algemene gegevens voor vaste activa instellen
description: 'Voordat u werkt met vaste activa, moet u standaardgrootboekrekeningen instellen, boekingsgroepen, verdeelsleutels, dagboeksjablonen en batches, en klassecodes.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Algemene gegevens voor vaste activa instellen

Voordat u vaste activa (VA) kunt beheren, moet u standaardgrootboekrekeningen, verdeelsleutels en dagboeksjablonen en batches instellen om vaste activa te boeken en opnieuw te classificeren. Definieer ook een classificatiehiërarchie (klassen en subklassen) om uw activa te structureren en, indien nodig, de locaties te definiëren waar u activa opslaat.

## Algemeen gedrag instellen voor de functionaliteit voor vaste activa

Definieer het algemene gedrag van de functionaliteit voor vaste activa en de bijbehorende documentnummerreeks op de pagina **VA-instellingen**.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Boekingsgroepen voor vaste activa instellen

Boekingsgroepen gebruiken om groepen vaste activa te definiëren. Posten voor deze boekingsgroepen worden naar dezelfde grootboekrekeningen geboekt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-boekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **VA-boekingsgroep** in.

    > [!NOTE]  
    >   Om ervoor te zorgen dat tegenrekeningen voor verschillende boekingen van vaste activa automatisch worden ingevoegd als u de actie **VA-tegenrekening invoegen** op dagboekregels kiest, voert u op basis van boeking van waardevermeerdering de volgende stap uit.
4. Selecteer op het sneltabblad **Tegenrekening** in het veld **Tegenrekening waardevermeerdering** de grootboekrekening waarnaar u tegenrekeningsposten wilt boeken voor afschrijving.

Zie voor meer informatie over het gebruik van de actie **VA-tegenrekening invoegen** voor dagboekregels voor vaste activa [Vaste activa herwaarderen](fa-how-revalue.md).

## Dagboeksjablonen voor vaste activa instellen

Een sjabloon is een vooraf gedefinieerd model voor een dagboek. De sjabloon bevat informatie over traceringscodes, lijsten en nummerreeksen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.

In [!INCLUDE[prod_short](includes/prod_short.md)] wordt automatisch een dagboeksjabloon voor vaste activa gemaakt als u de pagina **Dagboek voor vaste activa** voor het eerst opent, maar het is ook mogelijk om andere dagboeksjablonen in te stellen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in.

## Categorie- en subcategoriecodes voor vaste activa instellen

Bij vaste activa kunt u een classificatiehiërarchie definiëren die kan worden gebruikt om activa te groeperen. De hiërarchie heeft twee niveaus: categorieën en subcategorieën.

### Categoriecodes voor vaste activa

Categorieën voor vaste activa zijn de vermeldingen op het hoogste niveau in de classificatiehiërarchie waarin u activa groepeert. Gebruik bijvoorbeeld categorieën om activa in materiële of immateriële activa te verdelen. U moet ten minste één categorie voor vaste activa in uw configuratie maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-categorieën** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de categorieën van vaste activa die u wilt maken.

### Subcategoriecodes voor vaste activa

Subcategorieën voor vaste activa zijn de vermeldingen op het tweede niveau in de classificatiehiërarchie waarin u activa groepeert. Elke subcategorie verwijst naar een klasse op het hoogste niveau. Gebruik subcategoriecodes voor vaste activa om vaste activa in specifiekere categorieën te groeperen, bijvoorbeeld gebouwen, voertuigen, meubels of machines. U moet ten minste één subcategorie voor vaste activa in uw configuratie maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-subcategorieën** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de subcategorieën van vaste activa die u wilt maken.

## Beginnen met het registreren van activa

Als u de vaste activa in [!INCLUDE[prod_short](includes/prod_short.md)] voor het eerst gebruikt, moet u eerst het grootboektoepassingsgebied instellen voordat u vaste activa gaat instellen. Bepalend voor de manier waarop deze informatie wordt ingevuld, is de vraag of u vaste activa met het grootboek integreert.  

Als VA-transacties naar het grootboek moeten worden geboekt, wordt de onderstaande procedure gebruikt.  

1. Voltooi de basisinstellingen voor vaste activa.  
2. Vul een vaste-activakaart voor ieder bestaand activum in.  
3. Maak een VA-afschrijvingsboek voor elk afschrijvingsdoel (zoals voor belasting en financiële overzichten). Voor elk afschrijvingsboek definieert u de voorwaarden en bepalingen instellen, zoals integratie met het grootboek.

    Schakel grootboekintegratie in door de volgende stappen uit te voeren. Eerst moet u ervoor zorgen dat de grootboekintegratie voor alle afschrijvingsboeken is uitgeschakeld en dan boekt u de openingsposten. Tenslotte schakelt u grootboekintegratie in.  
4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
5. Selecteer het desbetreffende afschrijvingsboek en kies de actie **Bewerken** om de pagina **Afschrijvingsboekkaart** te openen.
6. Schakel op het sneltabblad **Integratie** alle schakelopties uit. Als u meer dan één afschrijvingsboek hebt, herhaalt u deze stap voor elk boek.  
7. In het dagboek voor vaste activa voert u voor elk activum de volgende regels in:
   * Een regel met de aanschafkosten.
   * Een regel met de gecumuleerde afschrijving tot het einde van het vorige boekjaar.
   * Een regel met de gecumuleerde afschrijving vanaf het begin van het lopende boekjaar tot de datum waarop [!INCLUDE[prod_short](includes/prod_short.md)] is ingesteld om te beginnen met het berekenen van de afschrijving.

    Als er nog andere beginsaldi zijn, zoals waardevermindering of waardevermeerdering, kunt u deze nu ook opgeven.  
8. Nadat u de dagboekregels voor elk activum hebt ingevoerd en geboekt, schakelt u grootboekintegratie in de afschrijvingsboeken in.

Als de vaste activa niet zijn geïntegreerd met het grootboek, slaat u stap 6 en 8 over.

## Vestigingscodes voor vaste activa instellen (optioneel)

Met vestigingscodes voor vaste activa worden id´s gedefinieerd waarvoor activa kunnen worden gevonden, bijvoorbeeld afdeling verkoop, receptie, administratie, productie of magazijn. U kunt ze gebruiken om de locatie van een vast activum te registreren. Dit is nuttige informatie voor de verzekering en voorraadbepaling.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-locaties** in en kies vervolgens de gerelateerde koppeling.
2. Voer codes en namen in voor de vestigingen van vaste activa die u wilt maken.

## Verdeelsleutels voor vaste activa instellen (optioneel)

Gebruik verdeelsleutels om transacties over diverse afdelingen of projecten te verdelen. U kunt bijvoorbeeld een verdeelsleutel instellen waarbij de afschrijvingskosten op voertuigen voor 35 procent worden toegewezen aan de administratie en voor 65 procent aan de verkoopafdeling. Zie voor meer informatie [Kosten en inkomsten toewijzen](year-allocate-costs-income.md).

Verdeelsleutels zijn van toepassing op klassen voor vaste activa en niet op afzonderlijke activa.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-boekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **VA-boekingsgroepen** de actie **Verdeelsleutels** en kies vervolgens een boekingssoort.
3. Vul indien nodig op de pagina **VA-verdeelsleutels** de velden in.
4. Herhaal stap 2 en 3 voor elk boekingssoort waarvoor u verdeelsleutels wilt definiëren.

## Dagboekbatches voor vaste activa instellen (optioneel)

U kunt meerdere dagboekbatches instellen, die individuele dagboeken voor elke dagboeksjabloon zijn. Werknemers kunnen bijvoorbeeld hun eigen dagboekbatch hebben, waarbij de initialen van de werknemer als batchnaam worden gebruikt. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende dagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul op de pagina **VA-dagboekbatches** indien nodig de velden in.

## Herindelingsdagboeksjablonen voor vaste activa instellen (optioneel)

Gebruik specifieke herindelingsdagboeken om vaste activa te verplaatsen, combineren of splitsen. In [!INCLUDE[prod_short](includes/prod_short.md)] wordt automatisch een herindelingsdagboeksjabloon voor vaste activa gemaakt wanneer u de pagina **VA-herindelingsdagboek** voor het eerst opent, maar u kunt andere VA-herindelingsdagboeksjablonen instellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-herindelingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in.

## Herindelingsdagboekbatches voor vaste activa instellen (optioneel)

U kunt meerdere dagboekbatches instellen, die individuele dagboeken voor elke herindelingsdagboeksjabloon zijn. Werknemers kunnen bijvoorbeeld hun eigen herindelingsdagboekbatch hebben, waarbij de initialen van de werknemer als herindelingsbatchnaam worden gebruikt. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-herindelingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de betreffende dagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul op de pagina **VA-herindelingsdagboekbatches** indien nodig de velden in.

## Zie ook

[Vaste activa instellen](fa-setup.md)  
[Overzicht van vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
