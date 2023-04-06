---
title: IC-transactieboeking instellen
description: Maak uw IC-leveranciers en -klanten als zogenaamde IC-partners en stel een IC-rekeningschema in.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
ms.date: 03/09/2022
ms.author: edupont
---
# IC-transactieboeking instellen

Intercompany-boekingen maken de boekhouding voor twee of meer bedrijven tot een eenvoudigere taak voor een gecentraliseerde financiële afdeling en voor boekhouders in intercompany-partnerbedrijven. Als u een transactie (zoals een verkoopdagboekregel) wilt verzenden vanaf een bedrijf en de bijbehorende transactie (zoals een inkoopdagboekregel) automatisch wilt maken in het partnerbedrijf, moeten de betrokken bedrijven afspreken welk rekeningschema en welke set dimensies ze willen gebruiken met IC-transacties. Het IC-rekeningschema kan bijvoorbeeld een vereenvoudigde versie van het rekeningschema van het moederbedrijf zijn. Elk bedrijf koppelt het volledige rekeningschema aan het gedeelde IC-rekeningschema, en elk bedrijf koppelt de dimensies aan de IC-dimensies.  

U moet ook een IC-partnercode instellen voor elk [!INCLUDE [prod_short](includes/prod_short.md)]-bedrijf, waarover alle bedrijven het eens zijn, en die vervolgens toewijzen aan respectievelijk klant- en leverancierskaarten door het veld IC-partnercode in te vullen.  

Als u IC-regels maakt of ontvangt bij artikelen, kunt u uw eigen artikelnummer gebruiken of kunt u de artikelnummers van uw partner instellen voor elk gewenst artikel. Dit kunt u doen in het veld **Artikelnr. leverancier** of in het veld **Gemeenschappelijk artikelnr.** op de artikelkaart. U kunt ook de functie **Artikelverwijzing** gebruiken. Als u de nummers van uw artikelen aan uw omschrijvingen van de leveranciersartikelen wilt toewijzen, opent u de kaart en kiest u vervolgens de actie **Artikelverwijzingen** om verwijzingen tussen uw artikelomschrijvingen en die van de IC-partner in te stellen. Zie voor meer informatie [Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md).

Als u IC-verkooptransacties uitvoert waarin resources zijn opgenomen, moet u het veld **IC-partner Ink. Grootb.rek.nr.** invullen op de resourcekaart van elke gewenste resource. Dit is het nummer van de IC-grootboekrekening waarnaar het bedrag voor deze resource wordt geboekt in het partnerbedrijf. Zie [Resources instellen](projects-how-setup-resources.md) voor meer informatie.

> [!NOTE]
> Intercompany-inkooptransacties die resources, vaste activa en artikeltoeslagen omvatten, worden niet volledig ondersteund. In het bedrijf van uw intercompany-partner is het veld **Regelsoort** leeg op inkoopdocumentregels die deze entiteiten bevatten. U moet het veld handmatig bijwerken.

## Transacties van intercompany-partners automatisch accepteren

2022 release wave 1 introduceerde een nieuwe pagina **Intercompany-instelling** waarmee u transacties van uw intercompany-partners sneller kunt verwerken. Op de pagina kunt u opgeven of dit bedrijf automatisch journaalregels maakt op basis van de berichten van een intercompany-partner uit de pagina **IC-diversendagboek**. De journaalregels worden voor u gemaakt, maar niet geboekt. U kunt de volgende velden op de nieuwe pagina Intercompany-instelling gebruiken om op te geven waar u ontvangen intercompany-journaaltransacties wilt maken:

* **Standaard-IC-dagboeksjabloon**
* **Standaard-IC-dagboekbatch**

> [!NOTE]
> Als uw organisatie intercompany-functies heeft gebruikt in [!INCLUDE [prod_short](includes/prod_short.md)] vóór 2022 release wave 1, om transacties automatisch te accepteren, moet uw beheerder de functieschakelaar **Automatisch IC-dagboektransacties accepteren** op de pagina **Functiebeheer** aanzetten.

## Een bedrijf instellen voor intercompany-transacties

Deze in te vullen velden verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Intercompany-instelling** de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## IC-partners instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **IC-partners** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul op de pagina **IC-partner** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor alle andere bedrijven die deel uitmaken van deze intercompany-instelling.

> [!NOTE]
> In [!INCLUDE[prod_short](includes/prod_short.md)] online kunt u geen bestandslocaties gebruiken om transacties over te brengen naar uw partners omdat [!INCLUDE[prod_short](includes/prod_short.md)] geen toegang heeft tot uw lokale netwerk. Daarom is als u **Bestandslocatie** kiest in het veld **Overdrachtstype**, het veld **Pad naar map** niet beschikbaar. In plaats daarvan wordt het bestand gedownload naar de map Downloads op uw computer. U kunt het bestand vervolgens bijvoorbeeld per e-mail naar iemand in het partnerbedrijf sturen. Voor een directer proces raden we u aan om geen bestandslocatie maar de optie **E-mail** te kiezen.

> [!NOTE]
> Voor intercompany-boekingen, wanneer u de schakeloptie **Transactie automatisch accepteren** hebt ingeschakeld op de pagina **IC-partnerkaart**[!INCLUDE[prod_short](includes/prod_short.md)] onderdrukt waarschuwingsberichten over inkoopfacturen die de oorspronkelijke inkooporder dupliceren. Daarom is het belangrijk om een bedrijfsproces te hebben voor het beheren van duplicaten. Bijvoorbeeld door dergelijke inkooporders te verwijderen wanneer de inkoopfactuur wordt ontvangen van de intercompany-partner.


## IC-leveranciers en IC-klanten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. U kunt ook toegang tot de leverancier krijgen vanuit het veld **Leveranciersnr.** op de pagina **IC-partner**.
3. Open de kaart voor een leverancier die een IC-partner is. Zie voor meer informatie [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).
4. Selecteer in het veld **IC-partnercode** de desbetreffende IC-partnercode.
5. Herhaal stappen 1 tot en met 4 voor klanten.

## IC-rekeningschema instellen

Als een groep bedrijven IC-transacties wil uitvoeren, moeten de bedrijven afspreken welk rekeningschema wordt gebruikt als algemene referentie. U moet met uw partnerbedrijven afspreken welke rekeningnummers er zullen worden gebruikt bij het uitvoeren van IC-transacties. Het moederbedrijf van de groep kan bijvoorbeeld een vereenvoudigde versie van het eigen rekeningschema maken en deze vervolgens exporteren naar een XML-bestand dat onder de bedrijven in de groep wordt verspreid.  

Als het rekeningschema van uw bedrijf het IC-rekeningschema voor uw partnerbedrijven definieert, volgt u het proces dat wordt beschreven in [Het definiërende IC-rekeningschema instellen](intercompany-how-setup.md#to-set-up-the-intercompany-chart-of-accounts).  

Als uw bedrijf een dochteronderneming is en u een XML-bestand ontvangt met het gemeenschappelijke IC-rekeningschema, volgt u de procedure [Het IC-rekeningschema importeren](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### Het IC-rekeningschema instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-rekeningschema** in en kies de gerelateerde koppeling.
2. Voer op de pagina **IC-rekeningschema** elke rekening in op een regel op de pagina.  
3. Als uw IC-rekeningschema identiek is aan uw normale rekeningschema of erop lijkt, kunt u de pagina automatisch invullen door de actie **Kopiëren uit rekeningschema** te kiezen. U kunt de nieuwe regels zo nodig bewerken.

### Het IC-rekeningschema exporteren

Als u uw IC-partners wilt toestaan het rekeningschema te importeren, moet u het naar een bestand exporteren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-rekeningschema** in en kies de gerelateerde koppeling.
2. Kies op de pagina **IC-rekeningschema** de actie **Exporteren** en kies de knop **Opslaan**.
3. Geef de bestandsnaam en de locatie op waar u het XML-bestand wilt opslaan en klik vervolgens op **Opslaan**.  

### Het IC-rekeningschema importeren  

Wanneer een bestand bestaat voor het definiëren van het IC-rekeningschema, kunnen IC-partners het importeren om ervoor te zorgen dat ze dezelfde rekeningen hebben.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-rekeningschema** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **IC-rekeningschema** de actie **Importeren**.  
3. Selecteer de bestandsnaam en de locatie van het XML-bestand en klik op **Openen**.  

De pagina **IC-rekeningschema** wordt gevuld met nieuwe of bewerkte grootboekregels volgens het IC-rekeningschema in het bestand. Bestaande niet-gerelateerde regels op de pagina blijven ongewijzigd.

### Het IC-rekeningstelsel koppelen aan het rekeningstelsel van uw bedrijf  

Wanneer u het IC-rekeningschema hebt gedefinieerd of geïmporteerd dat u en uw IC-partners hebben afgesproken te gebruiken, moet u elk van de IC-grootboekrekeningen koppelen aan een van de grootboekrekeningen van uw bedrijf. Geef op de pagina **IC-rekeningschema** op hoe IC-grootboekrekeningen worden vertaald in grootboekrekeningen uit het rekeningschema van uw bedrijf.

Als rekeningen in het IC-rekeningschema dezelfde rekeningnummers hebben als de corresponderende rekeningen in het rekeningschema van uw bedrijf, kunt u de rekeningen automatisch koppelen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-rekeningschema** in en kies de gerelateerde koppeling.  
2. Selecteer de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan schema met hetzelfde nr.**  
3. Voor elke IC-grootboekrekening waarnaar die niet automatisch is gekoppeld, vult u het veld **Toegewezen grootboekrek.nr.** in.  

## Standaardgrootboekrekeningen voor IC-partners instellen  

Wanneer u een IC-verkoopregel of -inkoopregel maakt om te verzenden als uitgaande transactie, moet u een rekening uit het IC-rekeningschema opgeven als standaardrekening waarop het bedrag in het bedrijf van uw partner wordt geboekt. Op de pagina **Rekeningschema** kunt u een standaard IC-grootboekrekening voor partners opgeven voor rekeningen die u regelmatig gebruikt op uitgaande IC-verkoop- of inkoopregels. Voor uw tegoedenrekeningen kunt u bijvoorbeeld de corresponderende schuldenrekeningen opgeven uit het IC-rekeningschema.  

Wanneer u nu een grootboekrekening opgeeft in het veld **Tegenrekeningnr.** op een IC-regel met **IC-partner** in het veld **Rekeningsoort**, wordt het veld **Grootboekrekeningnr. IC-partner** automatisch ingevuld.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Voer op de regel voor een grootboekrekening die wordt gebruikt voor IC-transacties, in het veld **Standaard IC-partnergrootboekrekening** de IC-grootboekrekening in waarnaar uw partner boekt wanneer u boekt naar de grootboekrekening op de regel.  
3. Herhaal stap 2 voor elke rekening die u vaak invoert in het veld **Tegenrekeningnr.** op een regel in een IC-dagboek of -document.

## IC-dimensies instellen

Als u en uw IC-partners transacties willen uitwisselen waaraan dimensies zijn gekoppeld, moet u afspreken welke IC-dimensies u allemaal gebruikt. Het moederbedrijf van de groep kan bijvoorbeeld een vereenvoudigde versie van de eigen set van dimensies maken en deze vervolgens exporteren naar een XML-bestand dat onder de bedrijven in de groep wordt verspreid. Alle dochterbedrijven importeren het XML-bestand vervolgens naar de pagina **IC-dimensies** en koppelen de IC-dimensies aan de dimensies op hun eigen pagina **Dimensies**.  

> [!NOTE]
> Elk bedrijf in [!INCLUDE [prod_short](includes/prod_short.md)] moet dimensies toewijzen aan intercompany-dimensies voor uitgaande documenten, en intercompany-dimensies toewijzen aan hun eigen dimensies voor inkomende documenten. Deze toewijzing zorgt voor consistentie tussen de bedrijven. Zie voor meer informatie de sectie [IC-dimensies koppelen aan dimensies van uw bedrijf](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Als uw bedrijf het hoofdbedrijf is en de definiërende set IC-dimensies heeft die uw groep gaat gebruiken als gemeenschappelijke naslag, volgt u de procedure [De IC-dimensies definiëren](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Als uw bedrijf een dochteronderneming is en u een XML-bestand ontvangt met de IC-dimensies die uw groep gaat gebruiken als algemene referentie, volgt u de procedure [IC-dimensies importeren](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### IC-dimensies definiëren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-dimensies** in en kies vervolgens de gerelateerde koppeling.  
2. Voer elke dimensie in op een regel op de pagina **IC-dimensies**.

    Als uw IC-dimensies lijken op of identiek zijn aan de dimensies van uw bedrijf, kunt u de pagina automatisch invullen door de functie **Kopiëren van dimensies** te gebruiken. Vervolgens kunt u de resulterende regels bewerken.  
3. Als u de IC-dimensies wilt exporteren naar een XML-bestand voor distributie naar uw partnerbedrijven, kiest u de actie **Exporteren**.  
4. Geef de bestandsnaam en de locatie op waar u het XML-bestand wilt opslaan en klik vervolgens op **Opslaan**.  

### De IC-dimensies importeren  

Wanneer een bestand bestaat voor de definiërende IC-dimensies, kunnen IC-partners het importeren om ervoor te zorgen dat ze dezelfde dimensies hebben.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-dimensies** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **IC-dimensies** de actie **Importeren**.  
3. Geef de bestandsnaam en de locatie van het XML-bestand op en klik op **Openen**.  

De regels op de pagina **IC-dimensies** en de pagina **IC-dimensiewaarden** worden geïmporteerd.  

### IC-dimensies koppelen aan dimensies van uw bedrijf

Wanneer u de dimensies hebt gedefinieerd of geïmporteerd die u en uw IC-partners hebben afgesproken te gebruiken, moet u elk van de IC-dimensies koppelen aan een van de dimensies van uw bedrijf en vice versa. Geef op de pagina **IC-dimensies** op hoe IC-dimensies voor *inkomende transacties* worden vertaald in dimensies uit de lijst met dimensies van uw bedrijf. Op de pagina **Dimensies** geeft u op hoe uw dimensies worden vertaald in IC-dimensies voor *uitgaande transacties*.

Als IC-dimensies dezelfde code hebben als de corresponderende dimensies in de lijst met dimensies van uw bedrijf, kunt u de dimensies automatisch koppelen en vervolgens de rekeningen automatisch toewijzen.  

In de volgende stappen wijst u eerst intercompany-dimensies toe aan dimensies voor inkomende documenten op de pagina **Intercompany-dimensies**. Vervolgens wijst u dimensies toe aan intercompany-dimensies voor uitgaande documenten op de pagina **Dimensies**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **IC-dimensies** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **IC-dimensies** de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan dim. met dezelfde code**.
3. Voor elke IC-dimensie die niet automatisch wordt gekoppeld, vult u het veld **Toewijzing dimensiecode** in.

    Mogelijk moet u het veld aan uw weergave toevoegen. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.
4. Kies de actie **IC-dimensiewaarden**.
5. Vul op de pagina **IC-dimensiewaarden** het veld **Toegewezen dimensiewaardecode** in.

    Koppel dimensies aan IC-dimensies door soortgelijke stappen uit te voeren.
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dimensies** in en kies vervolgens de gerelateerde koppeling.
7. Selecteer op de pagina **IC-dimensies** de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan IC-dim. met dezelfde code**.
8. Voor elke IC-dimensie die niet automatisch wordt gekoppeld, vult u het veld **Toegewezen IC-dim.waardecode** in.
9. Kies de actie **Dimensiewaarden**.
10. Vul op de pagina **IC-dimensiewaarden** het veld **Toegewezen IC-dim.waardecode** in.

## Zie ook

[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]