---
title: Gebruikersactiviteit bijhouden in een wijzigingslogbestand| Microsoft Docs
Description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="logging-changes-in-dynamics-365-for-financials"></a>Wijzigingen in Dynamics 365 for Financials registreren
U kunt het wijzigingslogbestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] inschakelen, zodat u een overzicht van activiteiten hebt. Het logboek is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. In het wijzigingslogbestand worden posten chronologisch geordend en worden wijzigingen weergeven die worden aangebracht in de velden in de opgegeven tabellen. In het wijzigingslogbestand verzamelt alle wijzigingen die in de tabel worden aangebracht.  

## <a name="working-with-the-change-log"></a>Werken met het wijzigingslogbestand
Een vaak voorkomend probleem in veel financiële systemen is het lokaliseren van de oorzaak van fouten en wijzigingen in gegevens. Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek. Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens. U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.  

U activeert en deactiveert het wijzigingslogbestand in het venster **Wijzigingslogbestandinstellingen**. Als u het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd. Dit kan niet worden uitgeschakeld.  

In het venster **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.

Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren in het venster **Wijzigingslogposten**. Als u posten wilt verwijderen, kunt u dat doen in het venster **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.  

## <a name="see-also"></a>Zie ook
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteren](ui-sorting.md)  
[Zoeken naar pagina of rapport gebruiken](ui-search.md)  
[Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

