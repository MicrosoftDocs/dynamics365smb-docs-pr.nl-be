---
title: Bijlagen, koppelingen en notities aan records toevoegen | Microsoft Docs
description: Koppel een hyperlink aan een document of een website aan een bepaalde record, zoals een klant of document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315288"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Bijlagen, koppelingen en notities op kaarten en in documenten beheren

In het feitenblok op de meeste kaarten en documenten kunt u bestanden bijvoegen, koppelingen toevoegen en notities schrijven. Voor koppelingen en notities kunt u dit ook op de lijstpagina doen door eerst de bijbehorende regel te selecteren.

Als u een van deze bijgevoegde informatietypen wilt bekijken of wijzigen, moet u eerst het tabblad **Bijlagen** openen in het feitenblok. Het getal achter de titel van het tabblad geeft aan hoeveel bijgevoegde bestanden, koppelingen of notities er zijn voor de kaart of het document.

Bijlagen, koppelingen en notities blijven gekoppeld terwijl de kaart of het document wordt verwerkt in andere staten, zoals van een lopende verkooporder naar een geboekte verkoopfactuur. Geen van de bijlagetypen wordt echter door het systeem uitgevoerd, bijvoorbeeld bij het afdrukken of bij het opslaan in een bestand.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Een bestand bijvoegen bij een inkoopfactuur
U kunt elk type bestand met tekst, afbeelding of video aan een kaart of document toevoegen. Dit is bijvoorbeeld handig als u de factuur van een leverancier wilt opslaan als PDF-bestand op de bijbehorende inkoopfactuur in [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Bestanden die zijn gekoppeld met de functie Inkomende documenten, worden niet opgenomen op het tabblad **Bijlagen**. Zie voor meer informatie [Inkomende documenten](across-income-documents.md).

De volgende procedure is gebaseerd op een verkooporder. De stappen lijken op alle andere ondersteunde documenten en kaarten.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open de verkooporder waaraan u een bestand wilt koppelen.
3. Open het feitenblok **Bijlagen**.
4. Kies de waarde achter het veld **Documenten**, zoals '0'.
5. Kies op de pagina **Gekoppelde documenten**, in het veld **Bijlage** de knop **Bestand selecteren**.
5. Selecteer een bestand van een willekeurige locatie en kies de knop **Openen**.

Het bestand wordt nu gekoppeld aan de inkoopfactuur.

## <a name="to-add-a-link-from-an-item-card"></a>Een koppeling toevoegen vanuit een artikelkaart
U kunt een koppeling vanuit een kaart of document toevoegen aan een URL of pad. Dit is bijvoorbeeld handig als u een artikelkaart wilt koppelen aan de artikelcatalogus van de leverancier.

De volgende procedure is gebaseerd op een artikelkaart. De stappen lijken op alle andere ondersteunde documenten en kaarten.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het item waaruit u een koppeling wilt toevoegen en kies vervolgens het tabblad **Bijlagen** in het feitenblok.
3. Kies in de **Koppelingen** het pictogram **+**.
4. Voer in het veld **Koppelingsadres** de koppeling in.

    - Als u een koppeling wilt maken met een bestand op uw computer of netwerk, voert u het volledige pad en de bestandsnaam in, bijvoorbeeld **C:\My Documents\invoice1.doc**.
    - Als u een koppeling met een website wilt toevoegen, voert u het internetadres (URL) in, bijvoorbeeld **www.microsoft.com**.
    - Als u een koppeling met een programma wilt toevoegen, voert u een bepaalde tekenreeks in om het programma te openen. Als u Outlook bijvoorbeeld wilt openen met een nieuwe lege e-mail naar een bepaalde alias, voert u **mailto:testalias** in.  

5. Voer in het veld **Beschrijving** informatie over de koppeling in.  
6. Kies de knop **Ok**.

De koppeling is nu gekoppeld aan de artikelkaart.  

## <a name="to-write-a-note-on-a-sales-order"></a>Een notitie over een klantorder schrijven
U kunt bijvoorbeeld een notitie op een document of kaart schrijven om speciale instructies aan andere gebruikers van het document of de kaart te communiceren. U kunt bestandskoppelingen en URL's opnemen in notities.

> [!NOTE]
> Opmerkingen over het tabblad **Bijlagen** zijn niet gerelateerd aan interne notitiefunctionaliteit, die voornamelijk wordt gebruikt om te communiceren tussen werkstroomgebruikers. Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).

De volgende procedure is gebaseerd op een verkooporder. De stappen lijken op alle andere ondersteunde documenten en kaarten.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de verkooporder waarin u een notitie wilt schrijven en kies vervolgens het tabblad **Bijlagen** in het feitenblok.
3. Kies in de sectie **Notities** het pictogram **+**.
4. Schrijf in het veld **Notitie** tekst, zoals "Dit is een dringende bestelling."
5. Kies de knop **Ok**.

De notitie is nu aan de verkooporder toegevoegd.

## <a name="see-also"></a>Zie ook  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Inkomende documenten](across-income-documents.md)  
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)  
