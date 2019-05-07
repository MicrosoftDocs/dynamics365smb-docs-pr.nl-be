---
title: Definiëren hoe gegevens elektronisch worden uitgewisseld | Microsoft Docs
description: U kunt een externe provider van OCR-services gebruiken om PDF- of afbeeldingsbestanden te laten omzetten naar elektronische documenten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 382a95a579482a56597ffae053c53dab92f3739a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "914442"
---
# <a name="set-up-data-exchange-definitions"></a>Definities voor gegevensuitwisseling instellen
U kunt instellen dat [!INCLUDE[d365fin](includes/d365fin_md.md)] gegevens in bepaalde tabellen uitwisselt met gegevens in externe bestanden, bijvoorbeeld elektronische documenten verzendt en ontvangt, bankgegevens of andere gegevens importeert en exporteert, zoals loonlijsten, wisselkoersen en artikelcatalogi. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.  

Als voorbereiding voor het maken van een gegevensuitwisselingdefinitie voor een gegevensbestand of -stroom kunt u het gerelateerde XML-schema gebruiken om te definiëren welke gegevenselementen moeten worden opgenomen in het sneltabblad **Kolomdefinities**. Zie stap 6 in [De opmaak van regels en kolommen in het bestand beschrijven](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Zie [XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md) voor meer informatie.  

Doorgaans stelt u gegevensuitwisselingsdefinities op de pagina **Definitie van gegevensuitwisseling** in. Maar als u een gegevensuitwisselingsdefinitie instelt voor de service voor het vernieuwen van wisselkoersen, begint u het proces op de vereenvoudigde pagina **Kaart update-instellingen wisselkoersen**.  

> [!NOTE]  
>  Als het bestand dat wordt geconverteerd, in XML-indeling is, moet de term *kolom* in dit onderwerp worden geïnterpreteerd als *een XML-element dat gegevens bevat*.  

Dit onderwerp bevat de volgende procedures:  

* Definitie van gegevensuitwisseling maken  
* De definitie van een gegevensuitwisseling exporteren als een XML-bestand voor gebruik door anderen  
* Een XML-bestand importeren voor een bestaande definitie van gegevensuitwisseling  

## <a name="to-create-a-data-exchange-definition"></a>Definitie van gegevensuitwisseling maken  
Een definitie voor gegevensuitwisseling maken bestaat uit twee taken:  

1. Op de pagina **Definitie van gegevensuitwisseling** beschrijft u de opmaak van regels en kolommen in het bestand.  
2. Op de pagina **Toewijzing gegevensuitwisseling** wijst u kolommen in het gegevensbestand toe aan velden in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Dit wordt in de volgende procedures beschreven.  

> [!TIP]
> Als u wilt zien welke codeunits Microsoft gebruikt in bestaande definities in het standaardproduct, controleert u de drie **Codeunit**-velden in de kop van de pagina **Veldtoewijzing** voor elke definitie.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>De opmaak van regels en kolommen in het bestand beschrijven  
1. Voer in het tekstvak **Zoeken** de tekst **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Geef op het sneltabblad **Algemeen** de definitie voor gegevensuitwisseling en de soort gegevensbestand op door de velden in te vullen zoals beschreven in de volgende tabel.  

    |Veld|Definitie|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Voer een code in ter identificatie van de definitie van de gegevensuitwisseling.|  
    |**Naam**|Voer een naam in voor de definitie van gegevensuitwisseling.|  
    |**Bestandssoort**|Geef op voor welk soort bestand de definitie van gegevensuitwisseling wordt gebruikt. U kunt kiezen uit vier bestandstypen:<br /><br /> -   **XML**: laagsgewijze strings met inhoud en opmaak, omringd door labels die functies aangeven.<br />-   **Variabele tekst**: records hebben een variabele lengte en worden gescheiden door een teken, zoals een komma of puntkomma. Ook *gescheiden bestand* genoemd.<br />-   **Vaste tekst**: records hebben dezelfde lengte, gebruiken opvultekens en elke record staat op een afzonderlijke regel. Ook *bestand met vaste breedte* genoemd.<br />- **Json**: gelaagde strings met inhoud in JavaScript.|  
    |**Soort**|Geef op voor welke soort bedrijfsactiviteit de gegevensuitwisselingdefinitie wordt gebruikt, bijvoorbeeld **Betalingsexport**.|  
    |**Codeunit geg.afhandeling**|Geef de codeunit op die gegevens overbrengt in en uit tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit validatie**|Geef de codeunit op die wordt gebruikt om gegevens te valideren tegen vooraf bepaalde bedrijfsregels.|  
    |**Codeunit lezen/schrijven**|Geef de codeunit op die geïmporteerde gegevens verwerkt vóór het toewijzen en geëxporteerde gegevens na het toewijzen.|  
    |**Lezen/schrijven XMLport**|De XMLport opgeven waardoor een geïmporteerd gegevensbestand of een service binnenkomt vóór de toewijzing en waardoor geëxporteerde gegevens naar buiten gaan wanneer deze na de toewijzing naar een gegevensbestand of een service worden geschreven.|  
    |**Codeunit ext. geg.afhandeling**|Geef de codeunit op die externe gegevens overbrengt in en uit het kader voor gegevensuitwisseling.|  
    |**Codeunit feedback gebruiker**|Geef de codeunit op die opschoning verzorgt na het koppelen, zoals de regels markeren als geëxporteerd en tijdelijke records verwijderen.|  
    |**Bestandscodering**|Geef de codering van het bestand op. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Kolomscheidingsteken**|Geef op hoe kolommen in het gegevensbestand van elkaar zijn gescheiden, als het bestand het type **Variabele tekst** is.|  
    |**Kopregels**|Geef op hoeveel kopregels in het bestand zijn opgenomen.<br /><br /> Hierdoor wordt gezorgd dat de koptekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Koptag**|Als er op verschillende posities in het bestand een koptekstregel bestaat, voert u de tekst van de eerste kolom op de koptekstregel in.<br /><br /> Hierdoor wordt gezorgd dat de koptekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Voetteksttag**|Als er op verschillende posities in het bestand een voettekstregel bestaat, voert u de tekst van de eerste kolom op de voettekstregel in.<br /><br /> Hierdoor wordt gezorgd dat de voettekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  

4. Geef op het sneltabblad **Regeldefinities** de opmaak van regels in het gegevensbestand op door de velden in te vullen zoals beschreven in de volgende tabel.  

    > [!NOTE]  
    >  Voor importeren van bankafschriften kunt u slechts één regel maken voor de enkele notatie van het bankafschriftbestand dat u wilt importeren.  
    >   
    >  Voor export van betalingen kunt u een regel voor elk betalingstype maken dat u wilt exporteren. In dat geval toont het sneltabblad **Kolomdefinities** verschillende kolommen voor elke betalingssoort.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Voer een code in om de regel in het bestand te identificeren.|  
    |**Naam**|Voer een naam in die de regel in het bestand beschrijft.|  
    |**Kolomtelling**|Geef op hoeveel kolommen de regel in het gegevensbestand heeft. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Label voor gegevensregel**|Geef de positie op in het gerelateerde XML-schema van het onderdeel dat de belangrijkste post van het gegevensbestand vertegenwoordigt. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Naamruimte**|Geef de naamruimte op die wordt verwacht in het bestand, om naamruimtevalidatie mogelijk te maken. U kunt dit veld leeg laten als u geen naamruimtevalidatie mogelijk wilt maken.|  

5. Herhaal stap 4 om een regel te maken voor elk type bestandsgegevens dat u wilt exporteren.  

     Geef op het sneltabblad **Kolomdefinities** de opmaak van kolommen in het gegevensbestand op door de velden in te vullen zoals beschreven in de onderstaande tabel. U kunt het structuurbestand, zoals een .XSD-bestand, voor het gegevensbestand gebruiken om het sneltabblad vooraf te vullen met de relevante elementen. Zie [XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md) voor meer informatie.  

6. Kies op het sneltabblad **Kolomdefinities** de optie **Bestandsstructuur ophalen**.  
7. Selecteer op de pagina **Bestandsstructuur ophalen** het gerelateerde structuurbestand en kies vervolgens de knop **OK**. De regels op het sneltabblad **Kolomdefinities** worden ingevuld op basis van de structuur van het gegevensbestand.  
8. Vul op het sneltabblad **Kolomdefinities** de velden in of bewerk ze zoals in de volgende tabel wordt beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Kolomnr.**|Geef het nummer op dat de kolompositie op de regel in het bestand aangeeft.<br /><br /> Geef voor XML-bestanden het nummer op dat het type element in het bestand aangeeft dat de gegevens bevat.|  
    |**Naam**|Geef de naam van de kolom op.<br /><br /> Geef voor XML-bestanden de markering op waarmee de uit te wisselen gegevens worden gemarkeerd.|  
    |**Gegevenstype**|Geef op of de uit te wisselen gegevens van het type **Tekst**, **Datum** of **Decimaal** zijn.|  
    |**Gegevensopmaak**|Geef de eventuele indeling van de gegevens op. Bijvoorbeeld **MM-dd-yyyy** als de gegevenssoort **Datum** is. **Opmerking:** voor exporteren geeft u de gegevensindeling op volgens [!INCLUDE[d365fin](includes/d365fin_md.md)]. Voor importeren geeft u de gegevensindeling op volgens .NET Framework. Zie [Standaardnotaties voor datum en tijd](https://go.microsoft.com/fwlink/?LinkID=323466) voor meer informatie.|  
    |**Cultuur gegevensopmaak**|Geef de eventuele cultuur van de gegevensindeling op. Bijvoorbeeld **en-US** als het gegevenstype **Decimaal** is om te zorgen dat de komma wordt gebruikt als .000-scheidingsteken, volgens de Amerikaanse indeling. Zie [Standaardnotaties voor datum en tijd](https://go.microsoft.com/fwlink/?LinkID=323466) voor meer informatie. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Lengte**|Geef de lengte op van de regel met vaste breedte die de kolom bevat als het gegevensbestand het type **Vaste tekst** is.|  
    |**Beschrijving**|Voer een omschrijving van de kolom in, ter informatie.|  
    |**Pad**|Geef de positie op van het element in het gerelateerde XML-schema.|  
    |**Identificatie voor een negatief teken**|Voer de waarde in die in het gegevensbestand wordt gebruikt om negatieve bedragen te identificeren in gegevensbestanden die geen negatieftekens kunnen bevatten. Deze id wordt vervolgens gebruikt om de geïdentificeerde aantallen naar negatieftekens tegen te boeken tijdens het importeren. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Constant**|Geef alle gegevens op die u wilt exporteren in deze kolom, zoals extra informatie over het betalingstype. **Opmerking:** dit veld is alleen relevant voor exporteren.|  

9. Herhaal stap 8 voor alle kolommen of XML-elementen in het gegevensbestand met gegevens die u wilt uitwisselen met [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 De volgende stap bij het maken van de definitie van een gegevensuitwisseling bestaat uit het bepalen van welke kolommen of XML-elementen in het gegevensbestand worden gekoppeld aan welke velden in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  De specifieke koppeling is afhankelijk van het bedrijfsdoel van het gegevensbestand dat wordt uitgewisseld, en van lokale variaties. Zelfs de SEPA-bankstandaard heeft lokale variaties. [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt standaard de import van SEPA CAMT-bankafschriftbestanden. Dit wordt aangeduid door de code in de definitierecord voor gegevensuitwisseling **SEPA CAMT** op de pagina **Definities van gegevensuitwisseling**. Zie [Veldtoewijzing bij het importeren van SEPA CAMT-bestanden](across-field-mapping-when-importing-sepa-camt-files.md) voor informatie over de specifieke veldtoewijzing van deze CAMT SEPA-ondersteuning.  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Kolommen in de gegevensbestanden toewijzen aan velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Selecteer op het sneltabblad **Regeldefinities** de regel waarvoor u kolommen aan velden wilt toewijzen en kies vervolgens **Veldtoewijzing**. De pagina **Toewijzing gegevensuitwisseling** wordt geopend.  
2. Geef op het sneltabblad **Algemeen** de toewijzingsinstelling op door de velden in te vullen zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Tabel-id**|Geef de tabel op met de velden waarheen of vanwaar gegevens worden uitgewisseld volgens de toewijzing.|  
    |**Gebruiken als tussentijdse tabel**|Geef op dat de tabel die u selecteert in het veld **Tabel-id** een tussentijdse tabel is waarin de geïmporteerde gegevens worden opgeslagen voordat deze aan de doeltabel worden toegewezen.<br /><br /> Meestal gebruikt u een tijdelijke tabel als de definitie van de gegevensuitwisseling wordt gebruikt om elektronische documenten te importeren en om te zetten, zoals leveranciersfacturen naar inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.|  
    |**Naam**|Voer een naam in voor de instelling van de toewijzing.|  
    |**Codeunit toewijzing vooraf**|Geef de codeunit aan die de koppeling voorbereidt tussen velden in [!INCLUDE[d365fin](includes/d365fin_md.md)] en externe gegevens.|  
    |**Toewijzing van codeunit**|Geef de codeunit op die wordt gebruikt om de opgegeven kolommen of XML-gegevenselementen toe te wijzen aan velden in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit toewijzing achteraf**|Geef de codeunit op die de koppeling voltooit tussen velden in [!INCLUDE[d365fin](includes/d365fin_md.md)] en externe gegevens. **Opmerking:** wanneer de functie Conversieservice voor bankgegevens wordt gebruikt, zet de codeunit geëxporteerde gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)] om in een algemene indeling die gereed is voor export. Voor het importeren zet de codeunit externe gegevens om in een indeling die gereed is voor importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  Geef op het sneltabblad **Veldtoewijzing** op welke kolommen aan welke velden in [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn toegewezen door de velden in te vullen zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Kolomnr.**|Geef op voor welke kolom in het gegevensbestand u een toewijzing wilt definiëren.<br /><br /> U kunt alleen kolommen selecteren die worden vertegenwoordigd door regels op het sneltabblad **Kolomdefinities** op de pagina **Definitie van gegevensuitwisseling**.|  
    |**Veld-id**|Geef op aan welk veld de kolom in het veld **Kolomnr.** wordt toegewezen.<br /><br /> U kunt alleen velden selecteren die bestaan in de tabel die u hebt opgegeven in het veld **Tabel** op het sneltabblad **Algemeen**.|  
    |**Optioneel**|Geef op dat de toewijzing wordt overgeslagen als het veld leeg is. **Opmerking:** als u dit selectievakje niet inschakelt, treedt een exportfout op als het veld leeg is. **Opmerking:** dit veld is alleen relevant voor exporteren.|  
    |**Doeltabel-id**|Alleen zichtbaar als het selectievakje **Gebruiken als tussentijdse tabel** is ingeschakeld.<br /><br /> Geef de tabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|  
    |**Bijschrift bij doeltabel**|Alleen zichtbaar als het selectievakje **Gebruiken als tussentijdse tabel** is ingeschakeld.<br /><br /> Geef de naam op van de tabel in het veld **Doeltabel-id**. Dit is de tabel waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|  
    |**Doelveld-id**|Alleen zichtbaar als het selectievakje **Gebruiken als tussentijdse tabel** is ingeschakeld.<br /><br /> Geef het veld in de doeltabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|  
    |**Bijschrift bij doelveld**|Alleen zichtbaar als het selectievakje **Gebruiken als tussentijdse tabel** is ingeschakeld.<br /><br /> Geef de naam van het veld in de doeltabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|  
    |**Optioneel**|Alleen zichtbaar als het selectievakje **Gebruiken als tussentijdse tabel** is ingeschakeld.<br /><br /> Geef aan of de toewijzing moet worden overgeslagen als het veld leeg is. Als u dit selectievakje niet inschakelt, treedt een exportfout op als het veld leeg is.|  

De definitie van de gegevensuitwisseling is nu gereed en kan worden ingeschakeld voor gebruikers. Zie [Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md), [SEPA-krediettransfer instellen](finance-how-to-set-up-sepa-credit-transfer.md), [Automatische incasso via SEPA instellen](finance-how-to-set-up-sepa-direct-debit.md) en [Betalingen verrichten met de conversieservice van bankgegevens of SEPA-overmaking](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md) voor meer informatie.  

Wanneer u de definitie van gegevensuitwisseling hebt gemaakt voor een specifiek gegevensbestand, kunt u de definitie van gegevensuitwisseling exporteren als XML-bestand dat kan worden gebruikt om de import van het gegevensbestand in kwestie snel in te schakelen. Dit wordt in de volgende procedure beschreven.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>De definitie van een gegevensuitwisseling exporteren als een XML-bestand voor gebruik door anderen  
1. Voer in het tekstvak **Zoeken** de tekst **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de definitie van de gegevensuitwisseling die u wilt exporteren.  
3. Kies de actie **Definitie van gegevensuitwisseling exporteren**.  
4. Sla het XML-bestand dat de definitie van de gegevensuitwisseling vertegenwoordigt, op een geschikte locatie op.  

    Als er al een definitie voor gegevensuitwisseling is gemaakt, hoeft u slechts het XML-bestand in het kader voor gegevensuitwisseling te importeren. Dit wordt in de volgende procedure beschreven.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Een bestaande definitie van gegevensuitwisseling importeren  
1. Sla het XML-bestand dat de definitie van de gegevensuitwisseling vertegenwoordigt, op een geschikte locatie op.  
2. Voer in het tekstvak **Zoeken** de tekst **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de actie **Nieuw**. De pagina **Definitie van gegevensuitwisseling** wordt geopend.  
4. Kies de actie **Definitie van gegevensuitwisseling importeren**.  
5. Kies het bestand dat u in stap 1 hebt opgeslagen.  

## <a name="see-also"></a>Zie ook  
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[SEPA-krediettransfer instellen](finance-how-to-set-up-sepa-credit-transfer.md)  
[Automatische incasso via SEPA instellen](finance-how-to-set-up-sepa-direct-debit.md)  
[Betalingen verrichten met de conversieservice van bankgegevens of SEPA-overmaking](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
