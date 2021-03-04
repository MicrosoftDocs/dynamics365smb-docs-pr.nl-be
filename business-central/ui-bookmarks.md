---
title: Een bladwijzer maken van een koppeling naar een pagina of rapport in uw rolcentrum | Microsoft Docs
description: Leer hoe u een koppeling toevoegt aan uw rolcentrum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1bcbd23658ff2a74ae0ab88b6020e1d859f37355
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747730"
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Een bladwijzer van een pagina of rapport maken in uw rolcentrum
Met het bladwijzerpictogram kunt u een actie toevoegen waarmee een pagina of rapport wordt geopend vanuit het navigatiemenu van uw rolcentrum. Hierdoor bereikt u snel uw favoriete inhoud of zakelijke taken. U voegt de bladwijzer toe vanaf de doelpagina of het doelrapport, dat wil zeggen het scherm dat u wilt dat de koppeling in het rolcentrum opent.

Het bladwijzerpictogram wordt weergegeven in de rechterbovenhoek van een pagina's en ook in het venster **Vertel me**, waar u efficiënt bladwijzers kunt maken van meerdere pagina's of rapporten. Als er al een bladwijzer voor de pagina bestaat, is het pictogram donker en bevat de knopinfo 'Bladwijzer'.

## <a name="to-bookmark-the-target-page"></a>Een bladwijzer maken van de doelpagina
1. Open een pagina waarvoor u een koppeling wilt maken in uw rolcentrum.
2. Kies het pictogram ![Bladwijzer](media/ui_bookmark_icon.png "Bladwijzer").

Een naar de pagina genoemde actie wordt nu toegevoegd aan het navigatiemenu in uw rolcentrum.

## <a name="to-bookmark-the-target-report"></a>Een bladwijzer maken van het doelrapport
1. Open een rapportaanvraagpagina waarvoor u een koppeling wilt maken in uw rolcentrum.
2. Kies het pictogram ![Bladwijzer](media/ui_bookmark_icon.png "Bladwijzer").

Een naar het rapport genoemde actie wordt nu toegevoegd aan het navigatiemenu in uw rolcentrum.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Een bladwijzer voor een pagina of rapport maken vanuit het venster Vertel me
1. Open het venster **Vertel me** en voer bijvoorbeeld **Verkooporders** in.
2. Plaats de aanwijzer boven het zoekresultaat voor de pagina of het rapport **Verkooporders** en kies vervolgens het pictogram ![Bladwijzer](media/ui_bookmark_icon.png "Bladwijzer").

Een naar de pagina of het rapport genoemde actie wordt nu toegevoegd aan het navigatiemenu in uw rolcentrum.


## <a name="frequently-asked-questions"></a>Veelgestelde vragen  

- **Kan ik mijn bladwijzers reorganiseren?**  
Ja. U kunt uw rolcentrum personaliseren en acties in een betere volgorde plaatsen of ze naar bestaande groepen of subgroepen verplaatsen.  
Leer hoe u [uw werkruimte personaliseert](ui-personalization-user.md).

- **Hoe verwijder ik een bladwijzer?**  
Kies op de doelpagina of het doelrapport nogmaals het bladwijzerpictogram om de betrokken actie uit uw rolcentrum te verwijderen. U kunt uw rolcentrum ook personaliseren en acties tijdelijk verbergen zonder ze volledig te verwijderen.

- **Waar vind ik mijn bladwijzers?**  
Wanneer u een bladwijzer aan een pagina of rapport toevoegt, wordt de nieuwe actie toegevoegd aan het bovenste navigatiemenu op uw huidige startscherm (rolcentrum). Als u veel acties hebt, moet u mogelijk de knop **Meer** activeren om ze allemaal weer te geven, omdat de nieuwe actie altijd aan het einde van die acties wordt toegevoegd.
<!-- Should we add a screenshot here? -->

- **Ik heb geen bladwijzerpictogram. Is er iets mis?**  
De mogelijkheid om een pagina of rapport als bladwijzer in te stellen is een van de vele personalisatiefuncties voor gebruikers in Business Central. Als het bladwijzerpictogram niet wordt weergegeven, is het waarschijnlijk dat uw beheerder personalisatie heeft uitgeschakeld.

- **Waarom kan ik geen bladwijzers maken van bepaalde pagina's of rapporten?**  
Niet van alle pagina's en rapporten kan een bladwijzer worden gemaakt. Wanneer een pagina of rapport wordt uitgevoerd binnen een speciale context die wordt beheerst door de bedrijfstoepassing, wordt het bladwijzerpictogram niet weergegeven. Bijvoorbeeld pagina's die niet in het venster **Vertel me** kunnen worden gevonden, maar vanuit elders worden gestart, bevatten geen bladwijzerpictogram. Evenzo zullen rapportaanvraagpagina's die alleen worden gebruikt om filters te verzamelen zonder het rapport uit te voeren, geen bladwijzerpictogram bevatten.

Zie technische details over [RunRequestPage](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) en [FilterPageBuilder](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Worden mijn bladwijzers ook gewist bij het wissen van mijn personalisatie?**  
Ja. Bladwijzers bevinden zich in het navigatiemenu. Als u wijzigingen in het navigatiemenu op een pagina wist of alle personalisatie in het rolcentrum wist, worden al uw nieuwe acties permanent verwijderd.

- **Waarom blijft het bladwijzerpictogram aangeven dat er nog geen bladwijzer is gemaakt?**  
Wanneer u een bladwijzer toevoegt, wordt de nieuwe actie toegevoegd aan het navigatiemenu in het rolcentrum en bij volgende bezoeken aan de pagina of het rapport wordt een donker bladwijzerpictogram weergegeven. Als u uw rolcentrum personaliseert en uw acties reorganiseert door ze in groepen te plaatsen, is het bladwijzerpictogram niet langer donker en kunt u nog een bladwijzer aan dezelfde pagina of hetzelfde rapport toevoegen. Hierdoor kunt u meerdere acties aan dezelfde pagina of hetzelfde rapport toevoegen en deze in verschillende groepen indelen.

- **Waarom geeft mijn koppeling naar een rapport een ander rapport weer?**  
Sommige rapporten kunnen worden vervangen door andere rapporten na het toepassen van een extensie op Business Central. Wanneer vervanging plaatsvindt, wordt de tekst van de nieuwe actie niet bijgewerkt en blijft de naam van het oorspronkelijke rapport staan, maar wordt naar het nieuwere rapport genavigeerd. Om de tekst van de nieuwe actie te corrigeren, kunt u de nieuwe actie verwijderen en opnieuw toevoegen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Zijn bladwijzers beschikbaar voor XMLports?**  
Nee. Op dit moment is het toevoegen van acties om XMLports te openen niet mogelijk vanuit de gebruikersinterface.

- **Worden mijn bladwijzers vertaald wanneer ik mijn taal wijzig in Business Central?**  
Wanneer u een nieuwe actie toevoegt, wordt alle vertaalde tekst die op dat moment beschikbaar was gebruikt voor de bladwijzer. Als er later nieuwe vertaalde tekst wordt toegevoegd, omvat de nieuwe actie niet de nieuwere vertalingen.


## <a name="see-also"></a>Zie ook
[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]