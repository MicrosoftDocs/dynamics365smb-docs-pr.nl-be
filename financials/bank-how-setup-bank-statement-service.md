---
title: Yodlee Bank Feeds instellen| Microsoft Docs
description: U kunt betalingsgegevens naar elke gegevensindeling converteren die uw bank vereist en het exporteren of importeren van bankbestanden inschakelen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ef5c6f4b9106b1b289cc5ed060fc28426fde0ae2
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-envestnet-yodlee-bank-feeds-service"></a>Procedure: De service Envestnet Yodlee Bank Feeds instellen
U kunt elektronische bankafschriften van uw bank importeren om snel het venster **Betalingsreconciliatiedagboek** in te vullen, zodat u betalingen kunt vereffenen en de bankrekening kunt reconciliëren. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

De feedservice van de Envestnet Yodlee Bank wordt geïnstalleerd als een extensie voor [!INCLUDE[d365fin](includes/d365fin_md.md)] en kan worden ingeschakeld. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md).

Nadat u de bankfeedservice hebt ingeschakeld, moet u een bankrekening koppelen aan de online bankrekening waar de feed vandaan zal komen. U koppelt bankrekeningen aan online bankrekeningen in de volgende scenario's:

* Er bestaat geen bankrekening in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor uw online bankrekening. Daarom kunt u de bankrekening maken door te koppelen vanuit de online bankrekening.
* Er bestaat een bankrekening in [!INCLUDE[d365fin](includes/d365fin_md.md)], die u aan een online bankrekening wilt koppelen.
* Een gekoppelde bankrekening moet worden ontkoppeld omdat u de bankfeedservice niet meer voor de rekening wilt gebruiken.
* Online bankrekeningen zijn gewijzigd en u wilt de informatie over bankrekeningen bijwerken in [!INCLUDE[d365fin](includes/d365fin_md.md)] .

Als de bankfeedservice is ingeschakeld, kunt u een bankrekening instellen om elke twee uur automatisch nieuwe bankafschriften te importeren in het venster **Betalingsreconciliatiedagboek**. Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd in het venster **Betalingsreconciliatiedagboek**, worden niet geïmporteerd. Zie voor meer informatie het gedeelte “Automatische import van bankafschriften inschakelen”.

> [!NOTE]  
>   Als u de begeleide instelling Bedrijf instellen gebruikt, worden sommige stappen in de volgende procedures automatisch uitgevoerd wanneer u de instelling van de bedrijfsbankrekening uitvoert. Zie voor meer informatie [Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>De bankfeedservice inschakelen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Open de bankrekening die u voor de bankfeedservice wilt gebruiken.
3. Selecteer in het venster **Bankrekening** in het veld **Importindeling van bankafschrift** YODLEEBANKFEED.  

De bankfeedservice wordt ingeschakeld als u een bankrekening koppelt aan de gerelateerde online bankrekening. Zie de volgende procedure.  

## <a name="to-create-a-new-linked-bank-account"></a>Een nieuwe gekoppelde bankrekening maken
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening en kies vervolgens **Nieuwe gekoppelde bankrekening maken**. Het venster **Bankrekening koppelen** opent na een aantal ogenblikken.

    > [!NOTE]  
>   Dit venster bevat de werkelijke webpagina van de Envestnet Yodlee Bank Feeds-service. De terminologie en functionaliteit in het venster komen mogelijk niet overeen met de instructies in dit onderwerp.  
3. Gebruik in het venster **Koppeling aan online bankrekening** in het deelvenster **Rekening koppelen** de zoekfunctie om de bank te zoeken waar u een of meer online bankrekeningen hebt.
4. Kies de banknaam. Het deelvenster **Aanmelden** wordt geopend.
5. Voer de gebruikersnaam en het wachtwoord in die u gebruikt om u aan te melden bij de online bank en kies vervolgens de knop **Volgende**.  
6. De bankfeedservice treft voorbereidingen om de eerste online bankrekening bij de opgegeven bank te koppelen aan een nieuwe bankrekening in [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Als u meer dan één online bankrekening bij de bank hebt, moet u er extra bankrekeningen voor maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie stap 8 t/m 10.  

    Als het proces is voltooid, wordt de naam van de bank weergegeven in het deelvenster **Mijn rekeningen** op het tabblad **Gekoppeld**. Het nummer tussen haakjes geeft aan hoeveel online bankrekeningen zijn gekoppeld.  
7. Kies de knop **Ok**.

    Als u slechts één online bankrekening koppelt, wordt het venster **Bankrekeningkaart** geopend en wordt de naam van de online bankrekening weergegeven. In dit geval is de koppeling van de bankrekening voltooid. Alleen de bankrekening hoeft nog te worden ingesteld. Zie voor meer informatie [Procedure: Bankrekeningen instellen](bank-how-setup-bank-accounts.md).

    Als u meerdere online bankrekeningen koppelt, wordt het venster **Bankrekening koppelen** geopend met de aanvullende online bankrekeningen die nog niet zijn gekoppeld aan bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In dat geval volgt u de volgende stap.  
8. Selecteer in het venster **Bankrekening koppelen** de regel voor een online bankrekening en kies vervolgens de actie **Koppelen aan nieuwe bankrekening**.  

    Het venster **Bankrekeningkaart** voor een nieuwe bankrekening wordt geopend en de naam van de online bankrekening wordt weergegeven.

    Als er al een bankrekening bestaat in [!INCLUDE[d365fin](includes/d365fin_md.md)] waaraan u de extra online de bankrekening wilt koppelen, voert u de volgende stap uit.  
9. Selecteer in het venster **Bankrekening koppelen** de regel voor een online bankrekening en kies vervolgens de actie **Koppelen aan bestaande bankrekening**.
10. Selecteer in het venster **Bankenoverzicht** de bankrekening waarmee u wilt koppelen, en kies vervolgens de knop **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Een bankrekening koppelen aan een online bankrekening
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een bankrekening die niet is gekoppeld aan een online bankrekening, en kies vervolgens de actie **Koppelen aan online bankrekening**. Het venster **Koppeling aan online bankrekening** wordt geopend met de naam van de bank al ingevuld in het deelvenster **Rekening koppelen**.
3. Kies de banknaam. Het deelvenster **Aanmelden** wordt geopend.
4. Voer de gebruikersnaam en het wachtwoord in die u gebruikt om u aan te melden bij de online bank en kies vervolgens de knop **Volgende**.  

    De bankfeedservice treft voorbereidingen om uw bankrekening in [!INCLUDE[d365fin](includes/d365fin_md.md)] te koppelen aan de gerelateerde online bankrekening.  

    Wanneer het proces probleemloos is voltooid, wordt de naam van de bank weergegeven in het deelvenster **Mijn rekeningen** op het tabblad **Gekoppeld**. Als de bank meerdere bankrekeningen heeft, wordt alleen de bankrekening gekoppeld die u in stap 2 hebt geselecteerd.  
5. Kies de knop **Ok**.

In het venster **Bankenoverzicht** is het selectievakje **Gekoppeld** ingeschakeld.

## <a name="to-unlink-a-bank-account"></a>Een bankrekening ontkoppelen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de regel voor een gekoppelde bankrekening die u wilt ontkoppelen van de gerelateerde online bankrekening, en kies de actie **Online bankrekening ontkoppelen**.

> [!NOTE]  
>   Als u **Ja** kiest in het bevestigingsdialoogvenster, wordt de koppeling met de online bankrekening verwijderd en worden de logdetails gewist. Om de bankrekening weer te koppelen aan de online bankrekening, moet u zich weer aanmelden bij de bank. Zie voor meer informatie het gedeelte “Een bankrekening koppelen aan een online bankrekening“.

## <a name="to-update-bank-account-linking"></a>Koppeling aan bankrekening bijwerken
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening en kies vervolgens de actie **Koppeling aan bankrekening bijwerken**.

Als er problemen voor de gekoppelde bankrekeningen zijn in het venster **Bankenoverzicht**, wordt het venster **Bankrekening koppelen** geopend, waarin wordt aangegeven welke bankrekeningen problemen hebben. Problemen kunnen het beste worden opgelost door de online bankrekening te ontkoppelen en de koppeling vervolgens opnieuw te maken. Zie voor meer informatie het gedeelte “Een bankrekening koppelen aan een online bankrekening“.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Automatisch importeren van bankafschriften inschakelen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor een gekoppelde bankrekening, en kies vervolgens de actie **Instelling van automatische import van bankafschriften**.
3. Geef in het venster **Instelling van automatische import van bankafschriften** in het veld **Aantal opgenomen dagen** op hoe ver in het verleden u banktransacties wilt ophalen.

    > [!NOTE]  
>   U wordt aangeraden deze waarde in te stellen op 7 dagen of meer.  
4. Schakel het selectievakje **Ingeschakeld** in.  

In het venster **Betalingsreconciliatiedagboek** worden elk uur nieuwe betalingen weergegeven die worden gedaan op de online bankrekening.

> [!NOTE]  
>   Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd in het venster **Betalingsreconciliatiedagboek**, worden niet geïmporteerd.

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen beheren](bank-manage-bank-accounts.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies ](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

