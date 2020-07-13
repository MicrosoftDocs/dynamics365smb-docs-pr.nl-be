---
title: Wijzigingen controleren | Microsoft Docs
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen. U kunt ook activiteiten volgen met bepaalde soorten activiteitenlogboeken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 201716238ddd42ac19cd769a8635d726e27e1509
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528825"
---
# <a name="auditing-changes-in-business-central"></a>Wijzigingen controleren in Business Central

U kunt het wijzigingslogbestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] inschakelen, zodat u een overzicht van activiteiten hebt. Het logboek is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden wijzigingen weergeven die worden aangebracht in de velden in de opgegeven tabellen. In het wijzigingslogbestand verzamelt alle wijzigingen die in de tabel worden aangebracht.

> [!Important]
> Wijzigingen van een gebruiker zijn pas zichtbaar in de **Wijzigingslogposten** als de sessie van de gebruiker opnieuw wordt gestart, wat in de volgende gevallen gebeurt:
<br />
> * De sessie is verlopen en vernieuwd.
> * De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.
> * De gebruiker heeft zich af- en weer aangemeld.

## <a name="working-with-the-change-log"></a>Werken met het wijzigingslogbestand

Een vaak voorkomend probleem in veel financiële systemen is het lokaliseren van de oorzaak van fouten en wijzigingen in gegevens. Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek. Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens. U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.  

U activeert en deactiveert het wijzigingslogbestand op de pagina **Wijzigingslogbestandinstellingen**. Wanneer een gebruiker het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.

Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.

Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten**. Als u posten wilt verwijderen, kunt u dat doen op de pagina **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.  

## <a name="working-with-activity-logs"></a>Werken met activiteitenlogboeken

Vanaf enkele pagina's in [!INCLUDE[prodshort](includes/prodshort.md)] kunt u een activiteitenlogboek bekijken dat de status en eventuele fouten weergeeft van bestanden waarnaar u exporteert vanuit of importeert in [!INCLUDE[prodshort](includes/prodshort.md)].  

De informatie wordt weergegeven in het venster **Activiteitenlogboek**, volgens de context van waaruit het wordt geopend. U kunt het venster bijvoorbeeld openen vanuit de pagina's **Documentuitwisselingsservice instellen**, **Inkomend document**, **Geboekte verkoopfactuur**en **Geboekte verkoopkredietnota**. U kunt de lijst met logboekvermeldingen leegmaken of gewoon de lijst met vermeldingen ouder dan 7 dagen wissen.  

## <a name="see-also"></a>Zie ook
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteren, zoeken en filteren](ui-enter-criteria-filters.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
