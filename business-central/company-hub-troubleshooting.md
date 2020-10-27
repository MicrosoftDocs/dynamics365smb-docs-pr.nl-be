---
title: Problemen met uw bedrijfshub oplossen
description: Leer hoe u problemen omzeilt in de bedrijfshub in Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927805"
---
# <a name="troubleshooting-your-company-hub"></a>Problemen met uw bedrijfshub oplossen

Bedrijven toevoegen aan de bedrijfshub is gemakkelijk, maar in dit artikel komen problemen aan bod die zich onderweg kunnen voordoen.  

## <a name="check-errors"></a>Controleren op fouten

Gebruik de actie **Fouten controleren** om een lijst met recente fouten te bekijken. U kunt voor elke fout aanvullende details zien en u kunt het logboek opschonen door oudere vermeldingen te verwijderen.  

## <a name="connection-failed"></a>Verbinding mislukt

Er kan een aantal redenen zijn waarom u geen verbinding kunt maken met een bedrijf, waaronder de volgende:

- De URL in het veld **Omgevingskoppeling** is ongeldig  

  Ga naar de pagina **Omgevingskoppelingen** , open de omgeving waarmee u geen verbinding kunt maken en kies vervolgens de actie **De verbinding testen** .  
- Het bedrijf van de cliënt is momenteel offline, bijvoorbeeld als dit wordt bijgewerkt

  Kies in het dashboard de menuopdracht **Extra** en vervolgens **Fouten controleren** . Vervolgens wordt er een lijst met technische gegevens weergegeven. Als u fouten ziet, kunt u contact opnemen met uw beheerder. Het foutbericht " *De server heeft de cliëntreferenties geweigerd* " wijst erop dat u geen toegang hebt.  
- U hebt geen toegang tot alle bedrijven in de omgeving waarmee u verbinding probeert te maken

  In [!INCLUDE [prodshort](includes/prodshort.md)] kan een organisatie meerdere bedrijfsunits hebben, bedrijven genaamd, en hebt u mogelijk geen toegang tot alle bedrijven. Werk samen met uw beheerder of cliënt om ervoor te zorgen dat u toegang hebt tot de bedrijven waarin u moet werken.  

## <a name="data-does-not-refresh"></a>Gegevens worden niet vernieuwd

Wanneer u een bedrijf toevoegt of om vernieuwen van de gegevens verzoekt, worden de gegevens opgehaald door [!INCLUDE [prodshort](includes/prodshort.md)]. U moet de pagina echter zelf vernieuwen, bijvoorbeeld door de actie **Alle bedrijven opnieuw laden** te kiezen, de browserpagina te vernieuwen of uit en vervolgens weer naar het dashboard te navigeren.  

Als u een bedrijf hebt toegevoegd, maar het wordt niet weergegeven in de lijst, kunt u ook de actie **Alle bedrijven opnieuw laden** gebruiken om de lijst bij te werken.

## <a name="see-also"></a>Zie ook

[Werk beheren tussen meerdere bedrijven in de bedrijfshub](company-hub.md)  
[Bedrijven toevoegen aan uw bedrijfshub](company-hub-add-company.md)  
[Accountantervaringen in Business Central](finance-accounting.md)  
