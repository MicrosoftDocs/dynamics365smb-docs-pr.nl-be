---
title: Geautomatiseerd systeem voor gegevensvastlegging (ADCS) gebruiken | Microsoft Docs
description: Met het ADCS-systeem kunt u alle verplaatsingen van artikelen in het magazijn registreren. Bovendien worden sommige dagboekactiviteiten vastgelegd, waaronder voorraadmutaties in het artikeldagboek van magazijnen en inventarisaties.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 11/20/2019
ms.author: sgroespe
ms.openlocfilehash: 209bbe3539fb99c626376149c22c419b4b476608
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832347"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Geautomatiseerd systeem voor gegevensvastlegging (ADCS) gebruiken

> [!NOTE]
> In de standaardversie van [!INCLUDE[d365fin](includes/d365fin_md.md)] werkt ADCS alleen in on-premises implementaties. Een Microsoft-partner kan het echter in online implementaties laten werken met behulp van Power Apps of iets soortgelijks.

Met het ADCS-systeem kunt u alle verplaatsingen van artikelen in het magazijn registreren. Bovendien worden sommige dagboekactiviteiten vastgelegd, waaronder voorraadmutaties in het artikeldagboek van magazijnen en inventarisaties. ADCS omvat meestal scannen van een barcode.

Als u ADCS wilt gebruiken, moet u elk artikel dat in het magazijn is opgeslagen een artikel-id geven. Ook moet u miniformulieren, draagbare functies en gegevensuitwisseling instellen en de instellingen opgeven voor de velden die ADCS bepalen. Op de locatiekaart van een magazijn kunt u opgeven of ADCS gebruikt wordt.

Op basis van de magazijnbehoeften bepaalt u welke informatie wordt weergegeven in het miniformulier dat op het draagbare apparaat verschijnt. Hier volgen enkele voorbeelden van informatie die kan worden weergegeven:  

- Gegevens uit tabellen binnen [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals een lijst van de pickdocumenten waaruit de gebruiker kan selecteren.  
- Tekstgegevens.  
- Berichten die bevestigingen of fouten weergeven over activiteiten die zijn uitgevoerd en geregistreerd door de gebruiker van draagbare apparatuur .

Raadpleeg [Een geautomatiseerd systeem voor gegevensvastlegging configureren](/dynamics-nav/Configuring-Automated-Data-Capture-System) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Magazijn instellen om ADCS te gebruiken  
Als u ADCS wilt gebruiken, moet u opgeven welke magazijnlocaties de technologie gebruiken.  

> [!NOTE]  
>  Het is raadzaam om geen magazijn in te stellen voor het gebruik van ADCS als het magazijn tevens een opslaglocatiecapaciteitbeleid heeft.

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies de gerelateerde koppeling.
2.  Selecteer een magazijn in de lijst waarvoor u ADCS wilt inschakelen en kies de actie **Bewerken**.
3. Op de pagina **Vestiging** schakelt u het selectievakje **ADCS gebruiken** in.  

## <a name="to-specify-an-item-to-use-adcs"></a>Een artikel opgeven om ADCS te gebruiken  
Aan elk magazijnartikel dat u wilt gebruiken met ADCS, moet een id-code worden toegewezen om dit aan het bijbehorende artikelnummer te koppelen. U kunt bijvoorbeeld de streepjescode van het artikel als de id-code gebruiken. Een artikel kan ook meerdere id-codes hebben. Dit kan nuttig zijn in gevallen waarin een artikel beschikbaar is in verschillende eenheden, zoals stuks en pallets. Wijs in dit geval aan elk artikel een id-code toe.    

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2.  Selecteer in de lijst een artikel dat deel uitmaakt van uw ADCS-oplossing en kies de actie **Bewerken**.
3. Kies op de pagina **Artikelkaart** de actie **Identificaties**.
4. Kies op de pagina **Artikelidentificaties** de actie **Nieuw**.
5. Geef in het veld **Code** de identificatiecode voor het artikel op. U kunt bijvoorbeeld de streepjescode van het artikel gebruiken.  

    U kunt ook een **variantcode** en een **Maateenheid** opgeven.  

6. Voer, indien nodig, meerdere codes voor de afzonderlijke artikelen in.
7. Kies de knop **OK**.  
8.  Als u deze gegevens wilt controleren, kiest u het veld **Identificatie** om de pagina **Artikelidentificaties** te openen.

## <a name="to-add-an-adcs-user"></a>Een ADCS-gebruiker toevoegen  
U kunt elke gebruiker toevoegen als een gebruiker van een ADCS-systeem (Automated Data Capture System). Wanneer u dit doet, moet de gebruiker ook een wachtwoord opgeven. Desgewenst kunt u ook een verbinding bieden op basis waarvan de ADCS-gebruiker kan worden geïdentificeerd als een magazijnwerknemer. Het ADCS-gebruikerswachtwoord kan afwijken van het Windows-wachtwoord van de gebruiker. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **ADCS-gebruikers** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3.  Voer in het veld **Naam** een naam voor de gebruiker in. De naam mag maximaal 20 tekens bevatten, inclusief spaties.  
4.  Voer in het veld **Wachtwoord** wachtwoord in. Het wachtwoord wordt gemaskeerd.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Opgeven dat een magazijnwerknemer een ADCS-gebruiker is  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies de gerelateerde koppeling.  
2.  Voeg, indien nodig, een nieuwe magazijnwerknemer toe. Zie voor meer informatie [Magazijnmedewerkers instellen](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Kies de actie **Lijst bewerken**.  
4.  Selecteer een magazijnmedewerker in de lijst. Klik in het veld **ADCS-gebruiker** op de vervolgkeuzelijstpijl en selecteer vervolgens de naam van een ADCS-gebruiker in de lijst.  

> [!NOTE]  
>  Het standaardmagazijn voor de medewerker moet een magazijn zijn dat gebruikmaakt van ADCS.

## <a name="to-create-and-customize-miniforms"></a>Miniforms maken en aanpassen
U kunt miniforms gebruiken om de informatie te beschrijven die u op een draagbaar apparaat wilt presenteren. U kunt bijvoorbeeld miniforms maken ter ondersteuning van de magazijnactiviteit artikelen picken. Nadat u een miniform hebt gemaakt, kunt u functies voor algemene acties toevoegen die een gebruiker met een draagbaar apparaat kan uitvoeren, zoals een regel omhoog of omlaag verplaatsen.  

Als u de functionaliteit van een miniformfunctie wilt implementeren of wijzigen, moet u een nieuwe codeunit maken of een bestaande codeunit wijzigen voor het uitvoeren van de vereiste actie of reactie. U kunt meer informatie over ADCS-functionaliteit verkrijgen door het bestuderen van codeunits, zoals 7705, de afhandelingscodeunit voor aanmeldingsfunctionaliteit. Codeunit 7705 laat zien hoe een kaarttype-miniform werkt.  

### <a name="to-create-a-miniform-for-adcs"></a>Een miniform voor ADCS maken  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Miniforms** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3.  Voer in het veld **Code** een code in voor het miniform. Geef desgewenst in alle andere velden waarden op.  

    Schakel het selectievakje **Start miniform** in om aan te geven dat het miniform het eerste formulier is dat de gebruiker bij het aanmelden ziet.  

4.  Definieer op het sneltabblad **Regels** de velden die op het miniform worden weergegeven. De volgorde waarin u de regels invoert, is de volgorde waarin de regels op het draagbare apparaat worden weergegeven.  

Wanneer u een miniform hebt gemaakt, volgt u de volgende stappen om functies te maken en functionaliteit aan verschillende toetsenbordinvoerwaarden te koppelen.  

### <a name="to-add-support-for-a-function-key"></a>Ondersteuning voor een functietoets toevoegen  
1.  Voeg aan het bestand the.xsl voor de invoegtoepassing code toe die vergelijkbaar is met het volgende voorbeeld. Hiermee maakt u een functie voor de **F6**-toets. De toetsencombinatie-informatie kan worden verkregen via de apparaatfabrikant.  
    ```xml  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  
    ```  
2.  Open in de ontwikkelomgeving [!INCLUDE[d365fin](includes/d365fin_md.md)] tabel 7702 en voeg een code toe die de nieuwe toets vertegenwoordigt. In dit voorbeeld maakt u een toets met de naam **F6**.  
3.  Voeg C/AL-code toe aan de desbetreffende functie van de miniformgebonden codeunit voor het afhandelen van de functietoets.  

### <a name="to-customize-miniform-functions"></a>Miniformfuncties aanpassen  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Miniforms** in en kies de gerelateerde koppeling.  
2.  Selecteer een miniform in de lijst en kies vervolgens de actie **Bewerken**.  
3.  Kies de actie **Functies**.  
4.  Selecteer in de vervolgkeuzelijst **Functie** een code voor de functie die u wilt koppelen aan het miniform. U kunt bijvoorbeeld ESC selecteren, zodat u functionaliteit koppelt aan het drukken op de toets ESC.  

Bewerk in de ontwikkelomgeving [!INCLUDE[d365fin](includes/d365fin_md.md)] de code voor het veld **Afhandeling codeunit** om code te maken of te wijzigen voor het uitvoeren van de vereiste actie of reactie.

Raadpleeg [Een geautomatiseerd systeem voor gegevensvastlegging configureren](/dynamics-nav/Configuring-Automated-Data-Capture-System) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
