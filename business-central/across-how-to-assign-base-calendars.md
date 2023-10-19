---
title: Basisagenda's instellen
description: U kunt een basisagenda aan uw bedrijf en de zakenpartners ervan toewijzen om leverings- en ontvangstdatums te berekenen op basis van de opgegeven werkdagen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: bholtorf
---
# <a name="set-up-base-calendars"></a>Basisagenda's instellen

U kunt een basisagenda toewijzen aan uw bedrijf en aan uw zakelijke partners, zoals klanten, leveranciers of vestigingen. Leverdatums en ontvangstdatums op regels voor toekomstige verkooporders, inkooporders, transferorders en productieorders worden berekend aan de hand van de werkdagen die zijn opgegeven in de agenda. De belangrijkste taak bij het instellen van een nieuwe basisagenda is het opgeven en definiëren van de vrije dagen die u wilt toepassen.  

## <a name="to-set-up-a-base-calendar"></a>Een basisagenda instellen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Basisagenda** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul het veld **Code** in.  
4. Kies de actie **Basisagendawijzigingen bewerken**.
5. Gebruik op de pagina **Basisagendawijzigingen** het veld **Periodiek systeem** om een bepaalde datum of dag te markeren als terugkerende vrije dag. U kunt de optie **Jaarlijks** of **Wekelijks** selecteren.  

    Als u **Jaarlijks** selecteert, moet u ook de relevante datum invoeren in het veld **Datum**.  

    Als u **Wekelijks** selecteert, moet u ook de relevante dag van de week invoeren in het veld **Dag**. Als u het veld leeg laat, moet u het veld **Datum** invullen. Het veld **Dag** wordt automatisch ingevuld.  

Wanneer u een post aanmaakt, wordt het veld **Vrije dag** geselecteerd. U deze in een werkdag veranderen door het vinkje te verwijderen.  
 Wanneer u teruggaat naar de basisagendakaart, ziet u dat de posten voor vrije dagen die u hebt gemaakt, zijn bijgewerkt. Deze posten worden nu in het rood weergegeven en het veld **Vrije dag** is geselecteerd.  

> [!NOTE]  
>  Wanneer u een nieuwe basisagenda instelt, kunt u regels selecteren en kopiëren vanuit een bestaande agenda. U kunt dit doen op de bijbehorende pagina **Basisagendawijzigingen**.  

> [!IMPORTANT]  
>  Elke basisagenda die is gedefinieerd voor de leverancier of de locatie bepaalt mede hoe de datums worden berekend en afgerond naar werkdagen.
Hiermee wordt een datumformule opgegeven voor de tijd die nodig is om het artikel aan te vullen. Het wordt gebruikt voor het berekenen van het veld **Geplande ontvangstdatum**, als er vooruit wordt gerekend, en het veld **Orderdatum**, als er achterwaarts wordt gerekend. Zie [Levertermijnberek.](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Levertermijnberek.

Elke basisagenda die is gedefinieerd voor de leverancier of de locatie bepaalt mede hoe de datums worden berekend en afgerond naar werkdagen. De twee datumvelden op inkooporderregels worden dus als volgt berekend onder verschillende omstandigheden.

|Richting van berekening|Leveranciersagenda gedefinieerd|Leveranciersagenda niet gedefinieerd|
|---------------------|-----------------------|---------------------------|
|Voorwaarts|geplande ontvangstdatum = orderdatum + doorlooptijd leverancier (volgens de leveranciersagenda en eerst afgerond op de volgende werkdag op de leveranciersagenda en vervolgens op de locatieagenda)|geplande ontvangstdatum = orderdatum + doorlooptijd leverancier (volgens de locatieagenda)|
|Achterwaarts|orderdatum = geplande ontvangstdatum - doorlooptijd leverancier (volgens de leveranciersagenda en eerst afgerond op de vorige werkdag op de leveranciersagenda en vervolgens op de locatieagenda)|orderdatum = geplande ontvangstdatum - doorlooptijd leverancier (volgens de locatieagenda)|

> [!NOTE]
> Naast de berekening van de doorlooptijd die betrekking heeft op de geplande ontvangstdatum en orderdatum, zoals in de bovenstaande tabel te zien is, kunnen magazijnverwerkingstijd en veiligheidstijd worden opgeteld bij de formules en als volgt resulteren in de waarde in het veld **Verwachte ontvangstdatum**: Geplande ontvangstdatum + Veiligheidstijd + Inslagtijd = Verwachte ontvangstdatum.

> [!Important]
> Als uw locatie gebruikmaakt van een sterk afwijkende agenda van die van uw leveranciers, is het belangrijk specifieke agenda´s voor deze leveranciers in te stellen, om optimale doorlooptijden voor de leveranciers te berekenen. Zie [Een basisagenda toewijzen](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar) voor informatie over het instellen van leveranciersagenda's.

De inhoud van het veld **Levertermijn** wordt gekopieerd uit de artikelkaart of de SKU-kaart, als de doorlooptijd is gedefinieerd voor het artikel, of op de pagina **Artikelleveranciers** als de doorlooptijd voor de leverancier is gedefinieerd.

## <a name="to-customize-a-calendar"></a>Een agenda aanpassen
De belangrijkste taak bij het aanpassen van een basisagenda voor uw bedrijf of voor een van uw zakelijke partners is het invoeren van wijzigingen in de statuswaarden Werkdag en Vrije dag.

In een basisagenda worden bijvoorbeeld alle zaterdagen gemarkeerd als vrije dagen, terwijl in een aangepaste agenda voor een bepaalde vestiging alle zaterdagen in de maanden november en december en de zaterdagen die voorafgaan aan het vakantieseizoen worden aangemerkt als werkdagen.

In de volgende procedure wordt de vestiging als voorbeeld gebruikt. De taak Een basisagenda instellen hebt u op dit moment al uitgevoerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.
2. Open de locatie die u wilt bijwerken en selecteer het veld **Gepersonaliseerde agenda**. Houd er rekening mee dat een agenda moet worden geselecteerd in het veld **Basisagendacode**.
3. Op de pagina **Gepersonaliseerde agendaposten** kiest u de actie **Gepers. agendawijzigingen bewerken**.
4. In het venster **Gepersonaliseerde agendawijzigingen** voegt u regels toe voor gepersonaliseerde agendaposten.

    Wanneer u een regel invoert, is het selectievakje **Vrije dag** ingeschakeld. U kunt het selectievakje uitschakelen als u de status wilt wijzigen in Werkdag.

    U kunt in het veld **Periodiek systeem** een bepaalde datum of dag instellen als terugkerende vrije dag. U kunt de optie **Jaarlijks** of **Wekelijks** selecteren.

    Als u **Jaarlijks** selecteert, moet u ook de relevante datum invoeren in het veld **Datum**. Als u **Wekelijks** selecteert, moet u ook de relevante dag van de week invoeren in het veld **Dag**. Als u het veld leeg laat, moet u het veld **Datum** invullen. Het veld **Dag** wordt dan automatisch ingevuld. Dit kan handig zijn als u de afzonderlijke datum wilt markeren als vrije dag of als werkdag.

5. Kies de knop **OK**.

Op de pagina **Gepersonaliseerde agendaposten** kunt u zien dat de datumposten worden bijgewerkt met de wijzigingen die u hebt aangebracht.

Op de vestigingskaart ziet u dat het veld **Gepersonaliseerde agenda** de waarde **Ja** bevat, ten teken dat er een gepersonaliseerde agenda is ingesteld.

> [!Important]
> Als u het veld **Vestiging** op een orderregel niet invult, wordt de agenda van het bedrijf gebruikt.


Als u het veld **Expediteur** op de orderregel niet invult, wordt de agenda van het bedrijf gebruikt.

> [!NOTE]  
> Als u wijzigingen aanbrengt in een basisagenda die gepersonaliseerde agendawijzigingen bevat, worden alle gepersonaliseerde agenda's automatisch bijgewerkt.

## <a name="to-assign-a-base-calendar"></a>Een basisagenda toewijzen
In de volgende procedure worden voor een klant de leverdatums op verkooporderregels als voorbeeld gebruikt.

Basiskalenders worden als volgt toegewezen aan uw eigen bedrijf, klanten, leveranciers, vestigingen en expediteurs:  

-   Op de kaarten **Bedrijfsgegevens** en **Klant** wordt de basisagenda toegewezen op het sneltabblad **Verzending**.  
-   Op de kaart **Leverancier** wordt de basisagenda toegewezen op het sneltabblad **Ontvangen**.  
-   Op de kaart **Vestiging** wordt de basisagenda toegewezen op het sneltabblad **Magazijn**.  
-   Op de pagina **Expediteurs** wordt de basisagenda toegewezen op de pagina **Expediteurservices**.  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de **Klantenkaart** waarvoor u een aangepaste agenda wilt instellen.  
3.  Op het sneltabblad **Verzending** in de het veld **Basisagendacode** selecteert u de basisagenda die u wilt toewijzen.  

> [!IMPORTANT]  
>  -   Als u geen basisagenda toewijst aan een bedrijf, worden alle datums berekend als werkdagen.  
> -   Als u geen vestiging invoert op een orderregel, worden alle datums berekend als werkdagen.  
> -   Elke basisagenda die is gedefinieerd voor de leverancier of de locatie bepaalt mede hoe de datums worden berekend en afgerond naar werkdagen.

> [!NOTE]  
>  U moet eerst een basisagenda toewijzen aan het bedrijf, voordat u aangepaste agendaposten kunt maken.  

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
