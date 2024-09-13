---
title: Duurzaamheidskaarten en doelen
description: Leer hoe u duurzaamheidsscorecards en -doelen kunt opstellen en gebruiken.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Duurzaamheidsscorecards en doelstellingenoverzicht

Dit artikel biedt richtlijnen voor het maken van scorecards en doelen en voor het bijwerken van de status van doelen. Met scorecards en doelen kunnen organisaties duurzaamheidsstatistieken verzamelen en deze vergelijken met belangrijke bedrijfsdoelstellingen. Doelen kunnen worden gecreëerd op basis van huidige en streefwaarden, zodat gebruikers de voortgang van de huidige emissies kunnen vergelijken met voorgaande perioden.  

## Maak een scorekaart  

Om een nieuwe  *Sustainability Scorecard* te maken, volgt u de volgende stappen: volgen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **Sustainability Scorecards** in en selecteer vervolgens de gerelateerde koppelen. 
2. Selecteer op de pagina  **Scorecards voor duurzaamheid** de optie  **Nieuw**  om een nieuwe scorecard te maken.  
3. Geef het **nr. op.** En de velden **Naam** op het sneltabblad **Algemeen**  en voeg vervolgens de **Eigenaar** toe. 

> [LET OP!] In het veld  **Eigenaar**  kunt u alleen gebruikers selecteren die het veld  **Duurzaamheidsmanager** in de tabel  **gebruikersinstellingen** hebben geselecteerd. 

## Doelen creëren  

Om een nieuw  *Duurzaamheidsdoel* te creëren, volgen de stappen:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **Sustainability Scorecards** in en selecteer vervolgens de gerelateerde koppelen.
2. Kies de actie  **Doelen** om een nieuw **Duurzaamheidsdoel** te maken voor de geselecteerde scorecard.  
3. Selecteer  **Nieuw** om een nieuw doel te maken.
4. Scorekaart nr. **·** Wordt automatisch toegevoegd op basis van de waarde van de gekoppelde  **Sustainability Scorecard**. De gebruiker kan dit veld niet bewerken. Het systeem stelt ook het veld  **Meeteenheid** in op basis van de  **Meeteenheidcode emissie** op de pagina  **instellingen duurzaamheid** .  
5. U moet **Nee invullen.** en **Naam** van nieuwe **Duurzaamheidsdoelstelling**. Het veld  **Eigenaar** wordt automatisch ingevuld op basis van de waarde uit de gekoppelde  **Duurzaamheidsscorekaart**.   
6. Gebruikers kunnen ervoor kiezen om een  *Duurzaamheidsdoel* te maken voor het hele bedrijf, een specifiek land/regio of een specifieke faciliteit. Als gebruikers een specifiek doel willen maken, moeten ze het land of de regio selecteren in het veld  **Land-/regiocode** of de faciliteit in het veld  **Verantwoordelijkheidscentrum** .  
7. Selecteer de velden **Startdatum** en **Einddatum** om een specifieke periode in te stellen voor het bijhouden van huidige waarden. Deze configuratie bepaalt de waarden in de volgende velden: **Huidige waarde voor CO2**, **Huidige waarde voor CH4** en **Huidige waarde voor N2O**. 
8. Selecteer de velden **Startdatum basislijn** en **Einddatum basislijn** om een speciale basislijnperiode in te stellen voor het vergelijken van huidige waarden. Deze configuratie bepaalt de waarden in de volgende velden: **Basislijn voor CO2**, **Basislijn voor CH4** en **Basislijn voor N2O**.
9. Gebruikers kunnen ook streefwaarden toevoegen in het geselecteerde veld  **Meeteenheid** voor de huidige periode met behulp van de volgende velden:  **Streefwaarde voor CO2**,  **Streefwaarde voor CH4** en  **Streefwaarde voor N2O**.   
10. Eén van deze doelen kan worden geselecteerd als  **hoofddoel**. Waarden uit het hoofddoel worden gebruikt in het rolcentrum van de  **Duurzaamheidsmanager** .  

Als u veel doelen op de pagina hebt, kunt u de actie  **Mijn doelen weergeven**  gebruiken om alleen uw doelen weer te geven. Als u ze allemaal wilt weergeven, moet u de actie  **Alle doelen weergeven**  uitvoeren.  

> [!NOTE]
> *Duurzaamheidsdoelen kunnen alleen worden gemaakt voor een specifieke Duurzaamheidsscorecard. U kunt geen doelen maken die niet gerelateerd zijn aan de scorecard. U kunt echter wel meerdere doelen maken voor één scorecard.*  *·* U kunt slechts één **Duurzaamheidsdoel** markeren als het **Hoofddoel**.

> [!NOTE]
> Gebruikers kunnen verschillende combinaties van doelen instellen voor het hele bedrijf, specifieke landen of regio's en een verantwoordelijkheidscentrum voor één Duurzaamheidsscorecard *.* Gebruikers kunnen ook verschillende periodes gebruiken voor hetzelfde trackingmodel. 

## Zie ook

[Duurzaamheidsinstellingen](finance-sustainability-setup.md)    
[Duurzaamheidsrekeningschema en grootboek](finance-sustainability-accounts-ledger.md)    
[Hoe duurzaamheidsposten registreren](finance-sustainability-journal.md)    
[Adhoc-analyse van duurzaamheidsgegevens](ad-hoc-analysis-sustainability.md)    
[Duurzaamheidsrapporten en analyses in Business Central](sustainability-reports.md)   
[Duurzaamheid-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Financiën](finance.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
