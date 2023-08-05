---
title: Export van controlebestand
description: In dit artikel wordt uitgelegd hoe u verschillende exportindelingen instelt en vervolgens gebruikt op basis van vereisten voor auditors of autoriteiten.
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# Export van controlebestand

Export van boekhoudkundige informatie uit het systeem is een veel voorkomend verzoek van sommige lokale autoriteiten of auditors. Exports van indelingen en vereiste informatie kunnen verschillen. Posten voor export zijn meestal grootboekposten of btw-posten. Soms is echter andere informatie vereist.

**Export van controlebestand** is een vooraf geïnstalleerde extensie waarmee u verschillende posten kunt exporteren op basis van de vereisten van de auditor of autoriteit. Ongeacht het indelingstype of de posten kunt u de functionaliteit van de extensie gebruiken om het gegevensexportproces te beheren. De functionaliteit heeft geen vooraf geïnstalleerde bestandsindeling voor export. Daarom moet u een app installeren met een specifieke indeling (bijvoorbeeld SIE, SAF-T of FAC) of uw eigen app ontwikkelen.

> [!NOTE]
> Momenteel kunt u SIE- (Zweden), FEC- (Frankrijk) en SAF-T-indeling selecteren als een extra app. Partners kunnen ook een aangepaste indeling ontwikkelen. Het aantal beschikbare indelingen zal in de loop van de tijd toenemen.

## Controlebestand instellen

1. Selecteer de knop ![Vergrootglas waarmee de functie Vertel me wordt geopend.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van export van controlebestand** in en selecteer vervolgens de gerelateerde koppeling.
2. Ga op de **Instelling van export van controlebestand** als volgt te werk:

    1. Geef op het sneltabblad **Algemeen** in het veld **Code van exportindeling van controlebestand** de code op voor de standaardindeling voor het exporteren van controlebestanden. Alleen de indelingen die zijn ingeschakeld toen een specifieke bestandsindeling werd geïnstalleerd vanuit Functiebeheer en de indelingen die zijn toegevoegd als een aangepaste indeling, zijn beschikbaar.
    2. Schakel op het sneltabblad **Gegevenskwaliteit** het selectievakje **Bedrijfsgegevens controleren** in om op de hoogte te worden gesteld van bedrijfsinformatievelden die niet correct zijn ingesteld.
    3. Schakel het selectievakje **Klant controleren** in om een melding te ontvangen over velden die niet correct zijn ingesteld voor specifieke klanten.
    4. Schakel het selectievakje **Leverancier controleren** in om een melding te ontvangen over velden die niet correct zijn ingesteld voor specifieke leveranciers.
    5. Schakel het selectievakje **Bankrekening controleren** in om een melding te ontvangen over velden die niet correct zijn ingesteld voor specifieke bankrekeningen.
    6. Schakel het selectievakje **Postcode controleren** in om een melding te ontvangen over een postcode die niet correct is ingesteld.
    7. Schakel het selectievakje **Adres controleren** in om een melding te ontvangen wanneer een adres niet correct is ingesteld.
    8. Voer in het veld **Standaardpostcode** de postcode in die u wilt gebruiken als er geen postcode is opgegeven op de klanten- of leverancierskaart.

3. Selecteer de knop ![Vergrootglas waarmee de functie Vertel me wordt geopend.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van exportindeling van controlebestand** in en selecteer vervolgens de gerelateerde koppeling.
4. Ga op de pagina **Instelling van exportindeling van controlebestand** als volgt te werk:

    1. Selecteer de exportindeling voor controlebestanden die u wilt configureren. Alleen de indelingen die zijn ingeschakeld toen een specifieke bestandsindeling werd geïnstalleerd vanuit Functiebeheer en de indelingen die zijn toegevoegd als een aangepaste indeling, zijn beschikbaar.
    2. Geef in het veld **Naam van controlebestand** de standaardbestandsnaam of de bestandsnaamsjabloon op voor het controlebestand dat u wilt exporteren.
    3. Schakel het selectievakje **Archiveren in zip** in om geëxporteerde bestanden automatisch te zippen.

## De grootboekrekeningtoewijzing opgeven voor het exporteren van controlebestanden

De meeste indelingen die door de autoriteiten worden vereist voor grootboekrekeningen vereisen een specifiek standaardrekeningschema. Nadat u uw grootboekrekeningen hebt geconfigureerd, wordt uw geëxporteerde bestand daarom gebaseerd op de toewijzingen. U kunt meer toewijzingen in uw systeem gebruiken.

Volg deze stappen om de grootboekrekeningtoewijzing op te geven voor het exporteren van controlebestanden.

1. Selecteer de zoekknop ![Vergrootglas waarmee de functie Vertel me wordt geopend.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzing van grootboekrekening** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Grootboektoewijzing** de optie **Nieuw** in om een toewijzing te maken.
3. Geef in het veld **Code** de toewijzingscode op die de rapportageperiode vertegenwoordigt.
4. Selecteer in het veld **Standaardrekeningtype** het type van standaardgrootboekrekeningen.
5. Geef in het veld **Exportindeling van controlebestand** de exportindeling voor controlebestanden op waaraan de standaardgrootboekrekeningen zijn gekoppeld.
6. In het veld **Periodetype** geeft het systeem een boekhoudperiode of een aangepast periodetype op met een flexibele begindatum en -tijd, op basis van uw selectie. Als u een specifieke boekhoudperiode selecteert, wordt het veld ingesteld op **Boekingsperiode**. Anders wordt het ingesteld op **Gegevensbereik**.
7. Geef in het veld **Boekingsperiode** de begindatum op van de boekhoudperiode die als rapportageperiode wordt gebruikt, als u wilt dat deze hetzelfde zijn.
8. Als u het veld **Boekingsperiode** instelt, worden de velden **Begindatum** en **Einddatum** automatisch ingesteld op basis van de periode die u hebt opgegeven. Anders kunt u de begin- en einddatum voor uw rapportage handmatig instellen.
9. Als u al een standaardrekeningschema hebt toegevoegd, gaat u als volgt te werk:

    1. Geef in het veld **Nr. van standaardrekeningcategorie** de categorie op van de standaardrekening- of groeperingscode die wordt gebruikt voor toewijzing.
    2. Geef in het veld **Standaardrekeningnr.** de standaardrekeningcode of groeperingscode op die wordt gebruikt voor toewijzing.

10. Schakel het selectievakje **Inkomend saldo opnemen** in om rekening met het inkomende saldo van de grootboekrekening van het type **Tegenrekening** te houden voor toewijzing in plaats van de mutatie van de rapportageperiode.
11. Ga als volgt te werk om de toewijzing te starten:

    1. Als u regels wilt genereren op de pagina **Toewijzing van grootboekrekening** op basis van een bestaand rekeningschema, selecteert u **Bron voor toewijzing initialiseren**. Als u de grootboekrekeningtoewijzing wilt kopiëren van een andere toewijzingscode, selecteert u **Kopiëren uit andere toewijzing**. Wanneer u klaar bent met het maken van regels, worden alle grootboekrekeningen die geboekte posten bevatten, groen gemarkeerd.
    2. Als u alleen grootboekrekeningen wilt markeren die posten hebben, schakelt u **Beschikbaarheid van grootboekpost bijwerken**. Als de optie **Inkomend saldo opnemen** is ingeschakeld, worden alle geboekte grootboekposten in aanmerking genomen voor berekening. Anders worden alleen grootboekposten van de rapportageperiode in aanmerking genomen.

## Het controlebestand exporteren

1. Selecteer de knop ![Vergrootglas waarmee de functie Vertel me wordt geopend.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Exportdocumenten van controlebestanden** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Exportdocumenten van controlebestanden** de optie **Nieuw**.
3. Voer op het sneltabblad **Algemeen** de volgende stappen uit:

    1. Selecteer in het veld **Exportindeling van controlebestand** de indeling die wordt gebruikt om het controlebestand te exporteren.
    2. Selecteer in het veld **Code van toewijzing van grootboekrekening** de grootboekrekeningtoewijzingscode voor de rapportageperiode.
    3. Schakel het selectievakje **Splitsen per maand** in als er meerdere controlebestanden per maand moeten worden gegenereerd.
    4. Schakel het selectievakje **Splitsen per datum** in als er meerdere controlebestanden per dag moeten worden gegenereerd.
    5. Voer in het veld **Koptekstopmerking** de opmerking in die u wilt opnemen in de koptekst van het controlebestand.
    6. Geef in het veld **Contact** het contact op dat wordt geëxporteerd naar de koptekst van het controlebestand.
    7. Schakel het selectievakje **Meerdere zip-bestanden maken** in om meerdere zip-bestanden te genereren.

        > [!IMPORTANT]
        > Schakel dit selectievakje alleen in als u eerder enkele van de indelingsapps hebt geïnstalleerd of een aangepaste app hebt gemaakt. Installatie van een of meer van de specifieke indelingen zal waarschijnlijk velden en functies toevoegen aan de functie **Export van controlebestand**, op basis van de indelingsvereisten.

4. Voer op het sneltabblad **Verwerking** de volgende stappen uit:

    1. Schakel het selectievakje **Parallelle verwerking** in als u wilt dat het genereren van controlebestanden wordt verwerkt door parallelle achtergrondtaken. Schakel het selectievakje uit om gegevens in uw huidige sessie te exporteren.
    2. Als u het selectievakje **Parallelle verwerking** hebt geselecteerd, geeft u in het veld **Max. aantal taken** het maximumaantal achtergrondtaken op dat tegelijkertijd kan worden uitgevoerd.
    3. Geef in het veld **Vroegste begindatum/-tijd** de vroegste datum en tijd op waarop de achtergrondtaak moet worden uitgevoerd. Als u het proces uitvoert door **Start** te selecteren, kunt u de status volgen op de sneltabbladen **Verwerking** en **Regels**.

5. Wanneer u klaar bent, selecteert u **Downloaden als bestand** om het controlebestand voor de geselecteerde regel te downloaden.

> [!IMPORTANT]
> Als u meerdere posten wilt exporteren, raden we u af deze in de huidige sessie te exporteren vanwege mogelijke prestatieproblemen. In plaats daarvan raden we u aan parallelle verwerking te gebruiken tijdens niet-werkdagen of -uren.

## Zie ook
[Financieel beheer](finance.md)  
[Het grootboek en het rekeningschema begrijpen](finance-general-ledger.md)  
[Werken met dimensies](finance-dimensions.md)  
[Werken met Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
