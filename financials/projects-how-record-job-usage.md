---
title: Factureerbaar en gebudgetteerd gebruik van projectresources registreren| Microsoft Docs
description: Beschrijft hoe u het verbruik of gebruik van artikelen of resources in projecten registreert om projectbeheer te vergemakkelijken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b0bd4f9a4c0963520631e1571fd182adce85fdd9
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="record-usage-for-jobs"></a>Gebruik voor projecten vastleggen
In het venster **Projectplanningsregels** kunt u het gebruik bekijken en vastleggen voor verschillende delen van uw project. Het gebruik wordt automatisch bijgewerkt wanneer u gegevens wijzigt en uitwisselt tussen projecten en projectdagboeken of projectfacturen. Hiervoor moet u een project hebt ingesteld zodat **Gebruikslink toepassen** is ingeschakeld. Zie [Projecten instellen](projects-how-setup-jobs.md) voor meer informatie.  

Zo kunt u bijvoorbeeld voor planningsregels van het soort **Budget** de hoeveelheid van een resource invoeren en aangeven welke hoeveelheid moet worden overgebracht naar het projectdagboek. Als het soort van de planningsregel **Factureerbaar** is, kunt u de hoeveelheid van de resource invoeren en aangeven welke hoeveelheid moet worden overgebracht naar een factuur. Door de hoeveelheid die is doorgegeven aan het dagboek of de factuur te vergelijken met het resterend aantal, kunt u snel informatie over het gebruik bekijken.

In de volgende procedures wordt beschreven hoe u werkelijke (factureerbare) of gebudgetteerde projectprijzen en -kosten vastlegt. Voor informatie over het inschatten van gebudgetteerde waarde tijdens planning raadpleegt u [Projectbudgetten beheren](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Gebruik vastleggen voor een projectplanningsregel van het soort Budget
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer het betreffende project en kies vervolgens de actie **Projectplanningsregels**.
3. Selecteer een projectplanningsregel van het soort **Budget** of het soort **Budget en factureerbaar** waarvoor u gebruik wilt vastleggen.
4. In het veld **Aantal te verplaatsen naar dagboek** voert u het aantal in dat u wilt overbrengen. De standaardhoeveelheid is de waarde die u invoert in het veld **Aantal**.

    Het **Resterend aantal** bevat het resterende aantal om het project te voltooien en dat moet worden overgebracht naar het dagboek.  
5. Kies de actie **Projectdagboekregels maken**.
6. Vul in het venster **Projectplanningsregel taakoverdracht** de velden in zoals gewenst en kies vervolgens de knop **OK**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Kies de actie **Projectdagboek openen**.  
8. Selecteer in het venster **Projectdagboek** de relevante regel en kies vervolgens de actie **Boeken**.
9. Bekijk in het venster **Projectplanningsregels** het vastgelegde gebruik door te kijken naar de velden **Aantal**, **Resterend aantal** en **Aantal te verplaatsen naar dagboek**.  
10. Herhaal stap 3 tot en met 8 om aanvullend gebruik vast te leggen.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Gebruik vastleggen voor een projectplanningsregel van het soort Factureerbaar
In de volgende taak kunt u eveneens gebruik bijhouden, maar dan voor een projectplanningsregel van het soort **Factureerbaar**. Meestal factuurt u in dit geval uw gebruik, maar u kunt het ook overbrengen naar een dagboek. Wanneer u dat echter doet, wordt een projectplanningsregel van het type **Budget** gemaakt voor afstemming met de factureerbare regel. Zie [Projectbudgetten beheren](projects-how-manage-budgets.md) voor meer informatie.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het betreffende project en kies vervolgens de actie **Projectplanningsregels**.  
3. Selecteer een projectplanningsregel van het soort **Factureerbaar** waarvoor u gebruik wilt vastleggen.
4. Voer in het veld **Aantal te verplaatsen naar factuur** het aantal in dat u wilt overbrengen. De standaardhoeveelheid is de waarde die u invoert in het veld **Aantal**.

    Het **Te factureren aantal** bevat het resterende aantal om het project te voltooien en dat moet worden gefactureerd.  
5. Kies de actie **Verkoopfactuur maken**.
6. Vul in het venster **Project - Naar verkoopfactuur overbrengen** desgewenst de velden in en kies vervolgens de knop **OK**.
7. Selecteer in het venster **Projectplanningsregels** de relevante regel en kies vervolgens de actie **Boeken**.
8. Bekijk het vastgelegde gebruik door te kijken naar de velden **Aantal**, **Te factureren aantal**, **Aantal te verplaatsen naar factuur** en, als de verkoopfactuur is geboekt, **Aantal gefactureerd**.
9. Herhaal stap 3 tot en met 8 om aanvullend gebruik vast te leggen.  
10. Als u een gerelateerde, geboekte verkoopfactuur wilt bekijken, kiest u de actie **Verkoopfacturen/-creditnota's**.  
11. Selecteer in het venster **Projectfacturen** de relevante factuur en kies vervolgens de actie **Verkoopfactuur/creditnota openen**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Projectdagboekregels maken uit projectplanningsregels
Wanneer u klaar bent om financiële gegevens voor projecten te boeken, moet u projectdagboekregels maken die u kunt boeken.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer een relevant open project en kies vervolgens de actie **Projectplanningsregels**.  
3. Voer in het venster **Projectplanningsregels** op een relevante projectplanningsregel in het veld **Aant. te verplaatsen naar dagboek** het aantal in dat u wilt verplaatsen naar een projectdagboek.  
4. Kies de actie **Projectdagboekregels maken**.
5. Vul in het venster **Projectplanningsregel taakoverdracht** de benodigde velden in.  
6. Kies de knop **Ok**. Er worden dagboekregels gemaakt.
7. Controleer de overdracht door de relevante projectdagboekbatch te openen en de posten te controleren.  
8. Wanneer de projectdagboekregels zijn voltooid, kiest u de actie **Boeken**.  

## <a name="to-create-job-journal-lines-manually"></a>Handmatig projectdagboekregels maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het veld **Batchnaam** een relevante projectdagboekbatch.  
3. Voer op een nieuwe regel documentnummer, projectnummer, projecttaaknummer, soort en aantal van het verbruikte soort in.  
4. Wanneer de projectdagboekregels zijn voltooid, kiest u de actie **Boeken**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Planningsregels voor een projectpost controleren
Nadat u projectdagboekregels hebt geboekt, kunt u de planningsregels zien die zijn gekoppeld aan de projectdagboekposten die zijn geboekt.

> [!NOTE]  
>   Hiertoe moet het selectievakje **Gebruikslink toepassen** zijn ingeschakeld voor het project of de standaardinstelling voor alle projecten in uw organisatie zijn. Zie [Projecten instellen](projects-how-setup-jobs.md) voor meer informatie.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer een relevant projectdagboek en kies vervolgens de actie **Posten**.  
3. Kies in het venster **Projectposten** de actie **Gekoppelde projectplanningsregels weergeven**.

## <a name="see-also"></a>Zie ook
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

