---
title: Projectvoorraden beheren
description: Beschrijft de verschillende manieren om de voorraad en aankoop van materiaal en services voor projecten te beheren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-supplies"></a>Projectvoorraden beheren

U moet projectgoederen van artikelen, services en onkosten beheren als een integraal en zeer belangrijk aspect van de uitvoering van alle projecten. U kunt voorraadhoeveelheden gebruiken of projectspecifieke inkopen doen met behulp van inkooporders of inkoopfacturen. Stel bijvoorbeeld dat bij een serviceproject voor een computer een nieuwe schijf vereist is. U maakt een inkoopfactuur om een nieuwe schijf te kopen en legt het project vast waarvoor deze wordt gebruikt.

Als voor het inkoopproces de fysieke transactie niet apart hoeft te worden vastgelegd, kunt u een aankoop verwerken op de pagina **GB-dagboek project**. Zie voor meer informatie [Projectkosten boeken](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## <a name="to-purchase-items-or-services-for-a-project"></a>Artikelen of services inkopen voor een project

In de volgende procedure wordt beschreven hoe u een inkoopfactuur gebruikt om producten voor een project te kopen. Dezelfde stappen gelden bij gebruik van een inkooporder.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Kies in het veld **Projectnr.** en **Projecttaaknr.** de gegevens van het project waarvoor u artikelen of services wilt inkopen. Gebruik de personalisatietools als een veld niet zichtbaar is. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

    De waarde die u selecteert in het veld **Projectregelsoort** definieert of een planningsregel wordt gemaakt wanneer u het gebruik van het artikel boekt. Als het veld **Factureerbaar** bevat, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant. Zie [Projecten factureren](projects-how-invoice-jobs.md) voor meer informatie.
4. Kies de actie **Boeken**.

## <a name="to-view-the-value-of-purchases-for-a-project"></a>De waarde van aankopen voor een project weergeven

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Open de betreffende projectkaart.

    In het sneltabblad **Taken** bevat het veld **Openstaande orders** het totale uitstaande bedrag in de lokale valuta van voorraadartikelen en -services op inkoopdocumenten voor de projecttaakregel.  

    Het veld **Ontv./Niet gefact. bedrag** bevat de waarde van artikelen die worden geleverd op inkoopdocumenten, maar die nog niet zijn gefactureerd.  
3. Kies een van de velden om de pagina **Inkoopregels** te openen. Op deze pagina kunt u informatie bekijken over de gerelateerde inkoopdocumentregels, inclusief welke artikelen of services zijn ontvangen.

## <a name="to-post-a-project-related-expense"></a>Projectkosten boeken

Als u buitengewone of eenmalige projectkosten maakt, kunt u de pagina **GB-dagboek project** gebruiken om ze direct te boeken naar de relevante projectrekening.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **GB-dagboeken voor project** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel en voer gegevens over de kosten in, zoals informatie in de velden **Projectnr.** en **Projecttaaknr.**,  
3. Wanneer het dagboek compleet is, kiest u de actie **Boeken**.

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
