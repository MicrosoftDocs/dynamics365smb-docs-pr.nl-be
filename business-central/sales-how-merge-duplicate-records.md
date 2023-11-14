---
title: Klant- of leveranciersrecords samenvoegen
description: Beschrijft hoe u informatie over klanten of leveranciers kunt consolideren wanneer u dubbele vermeldingen over sommige van hen heeft.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: bholtorf
---
# Dubbele records samenvoegen

Aangezien verschillende gebruikers in de loop van de tijd nieuwe klant-, leveranciers- of contactkaarten maken, of de nieuwe records automatisch worden gemaakt tijdens migratie, kan een klant, leverancier of contact in het systeem worden voorgesteld door meer dan één record. In dit geval kunt u de pagina **Dubbele records samenvoegen** gebruiken vanaf de kaart of de record die u wilt behouden. De pagina geeft u een overzicht van dubbele veldwaarden en biedt functies om te selecteren welke waarden worden behouden of verwijderd wanneer twee records tot één worden samengevoegd.

> [!NOTE]
> Alleen gebruikers met de machtigingenset DUBBELE RECORDS SAMENVOEGEN kunnen deze functionaliteit gebruiken.

> [!TIP]
> De pagina **Dubbele records samenvoegen** toont alle velden waar de waarden verschillen voor de twee records die worden vergeleken. Daarom wordt een dubbele record aangeduid doordat de pagina erg weinig velden bevat. Als de pagina veel velden bevat, is de verdachte record waarschijnlijk geen duplicaat.

De volgende procedure is gebaseerd op een klantenkaart. De stappen zijn voor leveranciers- en contactkaarten vergelijkbaar.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de klant voor wie u vermoedt dat er een dubbele record bestaat en kies vervolgens de actie **Bewerken**.
3. Kies op de pagina **Klantenkaart** de actie **Samenvoegen met**.
4. Selecteer op de pagina **Dubbele records samenvoegen** in het veld **Samenvoegen met** de klant die u denkt dat een duplicaat is van de klant die u hebt geopend, die wordt aangegeven in het veld **Actueel**.

    Het sneltabblad **Velden** bevat velden waarvan de waarden voor de twee klanten verschillen. Dit houdt in dat als de geselecteerde klant echt een dubbele record is, slechts weinig velden worden vermeld, zoals typefouten en andere foutieve gegevensinvoer.

    Het sneltabblad **Gerelateerde tabellen** bevat tabellen die velden bevatten met een relatie met beide klanten. De velden **Huidig aantal** en **Aantal dubbele records** geven het aantal velden in gerelateerde tabellen aan waarin de waarde **Nr.** van zowel de huidige als de dubbele klant wordt gebruikt. Op de pagina **Dubbele records samenvoegen** is deze sectie echter alleen informatief. Als er samenvoegingsconflicten bestaan, lost u deze op de pagina **Conflicten met samenvoegen van dubbele records** op. Zie stap 8 t/m 12.   

5. Voor elk veld waarin u een andere waarde wilt gebruiken dan de huidige, schakelt u het selectievakje **Overschrijven** in. De waarde in het veld **Alternatieve waarde** wordt dan overgedragen naar de huidige record wanneer u het proces voltooit.
6. Wanneer u klaar bent met selecteren welke waarden moeten worden behouden of overschreven, kiest u de actie **Samenvoegen**.

    Er wordt gecontroleerd of de samenvoeging van waarden voor de dubbele klant met de huidige klant conflicten veroorzaakt. Er is een conflict als een waarde in ten minste één primaire-sleutelveld voor beide klanten hetzelfde is, terwijl de waarde in het veld **Nr.** voor de twee klanten verschilt.

7. Als geen conflicten worden gevonden, kiest u de knop **Ja** in het bevestigingsberichtvenster.

    De dubbele klant krijgt een nieuwe naam, zodat al het gebruik van de waarde **Nr.** ervan in alle velden met relaties met de klantentabel wordt vervangen door de waarde **Nr.** van de huidige klant.
8. Als er conflicten bestaan, kiest u de actie **(xx) conflicten oplossen alvorens samen te voegen** op het sneltabblad **Conflicten**, dat wordt weergegeven als er conflicten bestaan.
9. Selecteer op de pagina **Conflicten met samenvoegen van dubbele records** de regel voor een gerelateerde tabel met een conflict en kies vervolgens de actie **Details weergeven**.

    De pagina **Dubbele records samenvoegen** bevat nu de velden in de geselecteerde tabel die een samenvoegingsconflict veroorzaken tussen de twee klantrecords. U ziet zowel in de samengevatte waarden in de velden **Actueel** en **Conflicteert met** als op de regels dat ten minste één primaire-sleutelveld hetzelfde is voor beide klanten en dat de waarde van het veld **Nr.** verschilt voor de twee klanten.   
10. Als u de dubbele klantrecord niet wilt houden, kiest u de actie **Dubbele record verwijderen** en kiest u de knop **Sluiten**.

    Identieke veldwaarden, anders dan de waarde in het veld **Nr.**, worden verwijderd uit de dubbele record en ingevoegd in de huidige record.
11. Als u de dubbele klantrecord na de samenvoeging wilt houden, kiest u **Dubbele record hernoemen**.
12. Bij regels, anders dan het veld **Nr.**, waar het veld dezelfde waarde heeft in beide records, wijzigt u de waarde in het veld **Alternatieve waarde** en kiest u vervolgens de knop **Sluiten**.

    De conflicterende veldwaarde wordt bijgewerkt in de dubbele record, zodat deze kan worden samengevoegd met de huidige record. De dubbele record blijft na de samenvoeging bestaan.
13. Herhaal stap 8 tot en met 12 totdat alle conflicten worden opgelost. Het sneltabblad **Conflicten** verdwijnt.
14. Kies op de pagina **Dubbele records samenvoegen** de actie **Samenvoegen** opnieuw en selecteer vervolgens de knop **Ja** in het bevestigingsberichtvenster.

> [!NOTE]
> Voor contacten kunt u functionaliteit gebruiken om te zoeken naar dubbele contacten voordat u de pagina **Dubbele records samenvoegen** gebruikt. Zie voor meer informatie [Zoeken naar dubbele contacten](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Contacten instellen](marketing-setup-contacts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
