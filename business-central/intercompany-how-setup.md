---
title: IC-transactieboeking instellen| Microsoft Docs
description: Maak uw IC-leveranciers en -klanten als zogenaamde IC-partners en stel een IC-rekeningschema in.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 418dac3a6d909d3eb07525ab537a94f85016ad19
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-intercompany"></a>Intercompany instellen
Als u een transactie (zoals een verkoopdagboekregel) wilt verzenden vanaf een bedrijf en de bijbehorende transactie (zoals een inkoopdagboekregel) automatisch wilt maken in het partnerbedrijf, moeten de betrokken bedrijven afspreken welk rekeningschema en welke set dimensies ze willen gebruiken voor IC-transacties. Het IC-rekeningschema kan bijvoorbeeld een vereenvoudigde versie van het rekeningschema van het moederbedrijf zijn. Elk bedrijf koppelt het volledige rekeningschema aan het gedeelde IC-rekeningschema, en elk bedrijf koppelt de dimensies aan de IC-dimensies.  

U moet ook een IC-partnercode instellen voor elk partnerbedrijf, waarover alle bedrijven het eens zijn, en deze vervolgens toewijzen aan klant- en leverancierskaarten respectievelijk door het veld **IC-partnercode** in te vullen.  

Als u IC-regels maakt of ontvangt bij artikelen, kunt u uw eigen artikelnummer gebruiken of kunt u de artikelnummers van uw partner instellen voor elk gewenst artikel. Dit kunt u doen in het veld **Artikelnr. leverancier** of in het veld **Gemeenschappelijk artikelnr.** op de artikelkaart. U kunt ook de functie **Artikelkruisverwijzing** gebruiken: als u de nummers van uw artikelen aan uw omschrijvingen van de leveranciersartikelen wilt toewijzen, opent u de kaart en kiest u vervolgens de actie **Kruisverwijzingen** om kruisverwijzingen tussen uw artikelomschrijvingen en die van de IC-partner in te stellen.  

Als u IC-verkooptransacties uitvoert waarin resources zijn opgenomen, moet u het veld **IC-partner Ink. Grootb.rek.nr.** invullen op de resourcekaart van elke gewenste resource. Dit is het nummer van de IC-grootboekrekening waarnaar het bedrag voor deze resource wordt geboekt in het partnerbedrijf. Zie voor meer informatie.  

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Bedrijven instellen voor IC-transacties
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bedrijfsgegevens** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul in het venster **Bedrijfsgegevens** de velden **IC-partnercode**, **IC-inboxsoort**. en **IC-inboxdetails** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>IC-partners instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-partners** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul in het venster **IC-partner** indien nodig de velden in.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>IC-leveranciers en IC-klanten instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.
2. U kunt ook toegang tot de leverancier krijgen vanuit het veld **Leveranciersnr.** in het venster **IC-partner**.
3. Open de kaart voor een leverancier die een IC-partner is. Zie voor meer informatie [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).
4. Selecteer in het veld **IC-partnercode** de desbetreffende IC-partnercode.
5. Herhaal stappen 1 tot en met 4 voor klanten.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>IC-rekeningschema instellen
Als een groep bedrijven IC-transacties wil uitvoeren, moeten de bedrijven afspreken welk rekeningschema wordt gebruikt als algemene referentie. U moet met uw partnerbedrijven afspreken welke rekeningnummers er worden gebruikt bij het uitvoeren van IC-transacties. Het moederbedrijf van de groep kan bijvoorbeeld een vereenvoudigde versie van zijn rekeningschema maken, dit IC-rekeningschema exporteren van de database naar een XML-bestand en dit verspreiden onder de bedrijven in de groep.  

Als uw bedrijf het bovenliggende bedrijf is en het definiërende IC-rekeningschema heeft dat uw groep gaat gebruiken als gemeenschappelijke naslag, volgt u de procedure 'IC-rekeningschema instellen'.  

Als uw bedrijf een dochteronderneming is en u een XML-bestand ontvangt met het gemeenschappelijke IC-rekeningschema, volgt u de procedure 'Het IC-rekeningschema importeren'.  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Het definiërende IC-rekeningschema instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-rekeningschema** in en klik vervolgens op de gerelateerde koppeling.
2. Voer in het venster **IC-rekeningschema** elke rekening in op een regel in het venster.  
3. Als uw IC-rekeningschema identiek is aan uw normale rekeningschema of erop lijkt, kunt u het venster automatisch invullen door de actie **Kopiëren uit rekeningschema** te kiezen. U kunt de nieuwe regels zo nodig bewerken.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Het IC-rekeningschema exporteren
Als u uw IC-partners wilt toestaan het rekeningschema te importeren, moet u het naar een bestand exporteren.      
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-rekeningschema** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **IC-rekeningschema** de actie **Exporteren** en kies de knop **Opslaan**.
3. Geef de bestandsnaam en de locatie op waar u het XML-bestand wilt opslaan en klik vervolgens op **Opslaan**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Het IC-rekeningschema importeren  
Wanneer een bestand bestaat voor het definiërende IC-rekeningschema, kunnen IC-partners het importeren om ervoor te zorgen dat ze dezelfde rekeningen hebben.  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **IC-rekeningschema** de actie **Importeren**.  
3. Selecteer de bestandsnaam en de locatie van het XML-bestand en klik op **Openen**.  

Het venster **IC-rekeningschema** wordt gevuld met nieuwe of bewerkte grootboekregels volgens het IC-rekeningschema in het bestand. Bestaande niet-gerelateerde regels in het venster blijven ongewijzigd.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Het IC-rekeningstelsel koppelen aan het rekeningstelsel van uw bedrijf  
Wanneer u het IC-rekeningschema hebt gedefinieerd of geïmporteerd dat u en uw IC-partners hebben afgesproken te gebruiken, moet u elk van de IC-grootboekrekeningen koppelen aan een van de grootboekrekeningen van uw bedrijf. Geef in het venster **IC-rekeningschema** op hoe IC-grootboekrekeningen van inkomende transacties worden vertaald in grootboekrekeningen uit het rekeningschema van uw bedrijf.

Als rekeningen in het IC-rekeningschema dezelfde rekeningnummers hebben als de corresponderende rekeningen in het rekeningschema van uw bedrijf, kunt u de rekeningen automatisch koppelen.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan schema met hetzelfde nr.**  
3. Voor elke IC-grootboekrekening waarnaar die niet automatisch is gekoppeld, vult u het veld **Toegewezen grootboekrek.nr.** in.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Standaardgrootboekrekeningen voor IC-partners instellen  
Wanneer u een IC-verkoopregel of -inkoopregel maakt om te verzenden als uitgaande transactie, moet u een rekening uit het IC-rekeningschema opgeven als standaardrekening waarop het bedrag in het bedrijf van uw partner wordt geboekt. In het venster **Rekeningschema** kunt u een standaard IC-grootboekrekening voor partners opgeven voor rekeningen die u vaak gebruikt op uitgaande IC-verkoop- of inkoopregels. Voor uw tegoedenrekeningen kunt u bijvoorbeeld de corresponderende schuldenrekeningen opgeven uit het IC-rekeningschema.  

Wanneer u nu een grootboekrekening opgeeft in het veld **Tegenrekeningnr.** op een IC-regel met **IC-partner** in het veld **Rekeningsoort**, wordt het veld **Grootboekrekeningnr. IC-partner** automatisch ingevuld.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer op de regel voor een grootboekrekening die wordt gebruikt voor IC-transacties, in het veld **Standaard IC-partnergrootboekrekening** de IC-grootboekrekening in waarnaar uw partner boekt wanneer u boekt naar de grootboekrekening op de regel.  
3. Herhaal stap 3 voor elke rekening die u vaak invoert in het veld **Tegenrekeningnr.** op een regel in een IC-dagboek of -document.

## <a name="to-set-up-intercompany-dimensions"></a>IC-dimensies instellen
Als u en uw IC-partners transacties willen uitwisselen waaraan dimensies zijn gekoppeld, moet u afspreken welke IC-dimensies u allemaal gebruikt. Het moederbedrijf van de groep kan bijvoorbeeld een vereenvoudigde versie van zijn dimensieset maken, deze IC-dimensies exporteren naar een XML-bestand en dit verspreiden onder de bedrijven in de groep. Alle dochterbedrijven importeren het XML-bestand vervolgens in de tabel **IC-dimensies** en koppelen de IC-dimensies aan de dimensies in hun eigen tabel **Dimensies**.  

Als uw bedrijf het hoofdbedrijf is en de definiërende set IC-dimensies heeft die uw groep gaat gebruiken als gemeenschappelijke naslag, volgt u de procedure: 'De IC-dimensies definiëren'.

Als uw bedrijf een dochteronderneming is en u een XML-bestand ontvangt met de IC-dimensies die uw groep gaat gebruiken als algemene referentie, volgt u de procedure: 'IC-dimensies importeren'.

### <a name="to-define-the-intercompany-dimensions"></a>IC-dimensies definiëren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-dimensies** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer elke dimensie in op een regel in het venster **IC-dimensies**.

    Als uw IC-dimensies lijken op of identiek zijn aan de dimensies van uw bedrijf, kunt u het venster automatisch invullen door de functie **Kopiëren van dimensies** te gebruiken. Vervolgens kunt u de resulterende regels bewerken.  
3. Als u de IC-dimensies wilt exporteren naar een XML-bestand voor distributie naar uw partnerbedrijven, kiest u de actie **Exporteren**.  
4. Geef de bestandsnaam en de locatie op waar u het XML-bestand wilt opslaan en klik vervolgens op **Opslaan**.  

### <a name="to-import-the-intercompany-dimensions"></a>De IC-dimensies importeren  
Wanneer een bestand bestaat voor de definiërende IC-dimensies, kunnen IC-partners het importeren om ervoor te zorgen dat ze dezelfde dimensies hebben.  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-dimensies** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **IC-rekeningschema** de actie **Importeren**.  
3. Geef de bestandsnaam en de locatie van het XML-bestand op en klik op **Openen**.  

De regels in het venster **IC-dimensies** en het venster **IC-dimensiewaarden** worden geïmporteerd.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>IC-dimensies koppelen aan dimensies van uw bedrijf
Wanneer u de dimensies hebt gedefinieerd of geïmporteerd die u en uw IC-partners hebben afgesproken te gebruiken, moet u elk van de IC-dimensies koppelen aan een van de dimensies van uw bedrijf en vice versa. Geef in het venster **IC-dimensies** op hoe IC-dimensies voor inkomende transacties worden vertaald in dimensies uit de lijst met dimensies van uw bedrijf. In het venster **Dimensies** geeft u op hoe uw dimensies worden vertaald in IC-dimensies voor uitgaande transacties.

Als IC-dimensies dezelfde code hebben als de corresponderende dimensies in de lijst met dimensies van uw bedrijf, kunt u de dimensies automatisch koppelen en vervolgens de rekeningen automatisch toewijzen.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-dimensies** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer in het venster **IC-dimensies** de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan dim. met dezelfde code**.
3. Voor elke IC-dimensie die niet automatisch wordt gekoppeld, vult u het veld **Toewijzing dimensiecode** in.
4. Kies de actie **IC-dimensiewaarden**.
5. Vul in het venster **IC-dimensiewaarden** het veld **Toegewezen dimensiewaardecode** in.

    Koppel dimensies aan IC-dimensies door soortgelijke stappen uit te voeren.
6. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dimensies** in en klik vervolgens op de gerelateerde koppeling.
7. Selecteer in het venster **Dimensies** de regels die u automatisch wilt koppelen en kies vervolgens de actie **Koppelen aan IC-dim. met dezelfde code**.
8. Voor elke IC-dimensie die niet automatisch wordt gekoppeld, vult u het veld **Toegewezen IC-dim.waardecode** in.
9. Kies de actie **Dimensiewaarden**.
10. Vul in het venster **Dimensiewaarden** het veld **Toegewezen IC-dimensiewaardecode** in.

## <a name="see-also"></a>Zie ook
[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

