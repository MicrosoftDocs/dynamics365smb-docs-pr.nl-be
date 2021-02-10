---
title: VA-afschrijving instellen| Microsoft Docs
description: U geeft in een afschrijvingsboek op hoe u wilt dat vaste activa worden afgeschreven of in waarde verminderd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c9eea613db52d327caa1c3d5449864900fc867d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749281"
---
# <a name="set-up-fixed-asset-depreciation"></a>Afschrijving van vaste activa instellen
 U kunt diverse afschrijvingsmethoden gebruiken ter voorbereiding van financiële stukken en de aangifte van inkomstenbelasting. Veel grote ondernemingen gebruiken lineaire afschrijving voor hun jaarverslag omdat deze methode in het algemeen tot hogere netto-inkomsten leidt. Voor inkomstenbelastingdoeleinden gebruiken veel bedrijven echter een versnelde afschrijvingsmethode, zoals boekwaarde-afschrijving. U definieert de afschrijvingsmethode van een activum met het veld **Afschrijvingsmethode** op de pagina **Vast activum**. Zie voor meer informatie over wat de verschillende methoden doen [Afschrijvingsmethoden](fa-depreciation-methods.md).

 In afschrijvingsboeken definieert u de verschillende manieren waarop afschrijvingen moeten worden berekend voor uw verschillende vaste activa. In elk boek kunt u afzonderlijke afschrijvingsvoorwaarden opgeven. U kunt bijvoorbeeld opgeven dat een vast activum binnen een periode van drie jaar moet worden afgeschreven in het ene boek, en binnen een periode van vijf jaar in een ander boek.

 Wanneer u de betreffende afschrijvingsboeken hebt ingesteld, moet u aan elk vast activum een of meer afschrijvingsboeken toewijzen. Naar een afschrijvingsboek dat aan een vast activum wordt toegewezen, wordt als een afschrijvingsboek voor vaste activa verwezen. Het aantal afschrijvingsboeken dat u kunt instellen, is oneindig voor een vast activum. 

## <a name="to-create-a-depreciation-book"></a>Een afschrijvingsboek maken
In een afschrijvingsboek voor vaste activa geeft u op hoe vaste activa worden afgeschreven. Het is mogelijk om meerdere afschrijvingsboeken in te stellen om diverse afschrijvingsmethoden toe te passen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afschrijvingsboeken** in en kies de desbetreffende koppeling.
2. Kies op de pagina **Lijst met afschrijvingsboeken** de actie **Nieuw**.
3. Vul op de pagina **Afschrijvingsboek** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   U kunt transacties voor vaste activa registreren op de pagina **VA fin. dagboek** of op de pagina **VA-dagboek**, afhankelijk van de vraag of de transacties zijn bedoeld voor financiële rapportage of intern beheer. Voer de volgende stap uit om te definiëren welk soort dagboek standaard wordt gebruikt voor de verschillende activiteiten voor vaste activa.
4. Schakel op het sneltabblad **Integratie** het selectievakje in voor elke activiteit voor vaste activa waarvan u transacties wilt boeken met de pagina **Financieel dagboek voor vaste activa**.
5. Herhaal stap 2 t/m 4 voor elke afschrijvingsmethode of boekingsmethode die u aan vaste activa als afschrijvingsboek wilt toewijzen.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Een afschrijvingsboek aan een vast activum toewijzen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies de gerelateerde koppeling.
2. Selecteer het vaste activum waarvoor u een afschrijvingsboek voor vaste activa wilt instellen.
3. Vul op het sneltabblad **Afschrijvingsboek** indien nodig de velden in.
4. Als u meer dan één afschrijvingsboek aan het vaste activum moet toewijzen, kiest u de actie **Meer afschrijvingsboeken toevoegen**.
5. U kunt ook de actie **Afschrijvingsboeken** kiezen om een of meer afschrijvingsboeken voor vaste activa op te geven.

    > [!NOTE]  
    >   Als u de handmatige afschrijvingsmethode gebruikt, moet u de afschrijving handmatig invoeren in het financieel dagboek voor vaste activa. Uit de functie **Afschrijving berekenen** worden de vaste activa weggelaten die handmatig worden afgeschreven. U kunt deze methode gebruiken voor activa waarop niet wordt afgeschreven, zoals grond.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Een afschrijvingsboek aan meerdere vaste activa toewijzen met een batchverwerking
Als u een afschrijvingsboek wilt toewijzen aan meerdere vaste activa, kunt u de batchverwerking **VA-afschr.-boeken maken** gebruiken om VA-afschrijvingsboeken te maken.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies de gerelateerde koppeling.
2. Selecteer het vaste activum waaraan u een afschrijvingsboek wilt toewijzen en kies vervolgens de actie **Bewerken**.
3. Op de pagina **Afschrijvingsboek** kiest u de actie **VA-afschrijvingsboeken maken**.
4. Op de pagina **VA-afschrijvingsboeken maken** vult u het veld **Afschrijvingsboek** in.
5. Kies het veld **Kopiëren van VA-nr.** en selecteer het nummer van het vaste activum dat u als basis wilt gebruiken voor het maken van nieuwe VA-afschrijvingsboeken.

    Als u dit veld invult, bevatten de afschrijvingsvelden in de nieuwe afschrijvingsboeken voor vaste activa dezelfde gegevens als de overeenkomstige velden in het afschrijvingsboek voor vaste activa waaruit u kopieert. Laat het veld leeg als u nieuwe VA-afschrijvingsboeken met lege afschrijvingsvelden wilt maken.  
6. Op het sneltabblad **Vast activum** kunt u met behulp van een filter aangeven voor welke activa u de afschrijvingsboeken voor vaste activa wilt maken.
7. Kies de knop **Ok**.

## <a name="to-set-up-depreciation-posting-types"></a>Boekingssoorten voor afschrijving instellen
Voor elk afschrijvingsboek moet u instellen hoe [!INCLUDE[prod_short](includes/prod_short.md)] diverse boekingssoorten moet verwerken. Bijvoorbeeld, of de boeking debet of credit moet zijn, en of het boekingssoort moet worden opgenomen in de afschrijvingsbasis.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afschrijvingsboeken** in en kies de desbetreffende koppeling.  
2. Selecteer het afschrijvingsboek dat u wilt instellen en kies vervolgens de actie **VA-boekingssoortinstellingen**.
3. Vul indien nodig de velden op de pagina **Instellingen van VA-boekingstype** in.

    > [!NOTE]  
    >   Op de pagina **VA-boekingssoortinstellingen** kunt u geen regels wissen of invoegen. U kunt alleen de bestaande regels wijzigen.

Het wordt aangeraden om de instellingen van afschrijvingsboeken waarvoor al posten zijn geboekt niet te wijzigen. De wijzigingen gelden namelijk niet voor reeds geboekte posten, waardoor de statistische gegevens van het afschrijvingsboek onjuist worden.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Standaardsjablonen en batches instellen voor afschrijvingsboeken voor vaste activa
Voor elk afschrijvingsboek definieert u een standaardinstelling van sjablonen en batches. U gebruikt deze standaardwaarden om regels van het ene dagboek naar het andere dagboek te dupliceren, dagboekregels te maken met de batchverwerkingen **Afschrijving berekenen** of **Vaste activa indexeren** of aanschafkosten in het verzekeringsdagboek te dupliceren.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afschrijvingsboeken** in en kies de desbetreffende koppeling.  
2. Selecteer het afschrijvingsboek waarvoor u standaarddagboeken posten wilt definiëren en kies vervolgens de actie **VA-dagboekinstellingen**.  
3. Als u voor elke gebruiker een standaardinstelling wilt gebruiken, kiest u het veld **Gebruikers-id** om een selectie te maken op de pagina **Gebruikers**.  
4. In de andere velden selecteert u de dagboeksjabloon of dagboekbatch die standaard moet worden gebruikt.  

## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Aan de slag](product-get-started.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
