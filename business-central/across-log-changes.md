---
title: Gebruikersactiviteit bijhouden in een wijzigingslogbestand| Microsoft Docs
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: nl-be
ms.lasthandoff: 12/05/2018

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

## <a name="see-also"></a>Zie ook
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteervolgorde](ui-sorting.md)  
[Zoeken naar pagina of rapport gebruiken](ui-search.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

