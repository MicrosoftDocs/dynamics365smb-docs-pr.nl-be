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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4d35c0774fc777fd5b45983f03e6204daed0a3af
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755729"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Geautomatiseerd systeem voor gegevensvastlegging (ADCS) gebruiken

> [!NOTE]
> De oplossing Automated Data Capture System (ADCS) biedt [!INCLUDE[prod_short](includes/prod_short.md)] een manier om te communiceren met draagbare apparaten via webservices. U moet samenwerken met een Microsoft-partner die de koppeling tussen de webservice en het specifieke draagbare apparaat kan verzorgen. 

Met het ADCS-systeem kunt u alle verplaatsingen van artikelen in het magazijn registreren. Bovendien worden sommige dagboekactiviteiten vastgelegd, waaronder voorraadmutaties in het artikeldagboek van magazijnen en inventarisaties. ADCS omvat meestal scannen van een barcode.

Als u ADCS wilt gebruiken, moet u elk artikel dat in het magazijn is opgeslagen een artikel-id geven. Ook moet u miniformulieren, draagbare functies en gegevensuitwisseling instellen en de instellingen opgeven voor de velden die ADCS bepalen. Op de locatiekaart van een magazijn kunt u opgeven of ADCS gebruikt wordt.

Op basis van de magazijnbehoeften bepaalt u welke informatie wordt weergegeven in het miniformulier dat op het draagbare apparaat verschijnt. Hier volgen enkele voorbeelden van informatie die kan worden weergegeven:  

- Gegevens uit tabellen binnen [!INCLUDE[prod_short](includes/prod_short.md)], zoals een lijst van de pickdocumenten waaruit de gebruiker kan selecteren.  
- Tekstgegevens.  
- Berichten die bevestigingen of fouten weergeven over activiteiten die zijn uitgevoerd en geregistreerd door de gebruiker van draagbare apparatuur .

## <a name="to-enable-web-services-for-adcs"></a>Webservices inschakelen voor ADCS
Om Automated Data Capture System te gebruiken moet u de ADCS-webservice inschakelen.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>De ADCS-webservice inschakelen en publiceren  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Webservices** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.  
3. Voer op de pagina **Webservices** de volgende informatie in op een nieuwe regel:  

    |Veld|Waarde|  
    |---------------------------------|-----------|  
    |**Objecttype**|Codeunit|  
    |**Object-id**|7714|  
    |**Servicenaam**|ADCS **Belangrijk:** U moet de service een naam geven **ADCS**.|  

5. Selecteer het vakje **Gepubliceerd**.  
6. Kies de knop **Ok**.  

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

> [!NOTE] 
> Als u de functionaliteit van een miniformfunctie wilt implementeren of wijzigen, moet u een nieuwe codeunit maken voor het veld **Afhandeling codeunit** om de vereiste actie of reactie uit te voeren. U kunt meer leren over ADCS-functionaliteit door codeunits te onderzoeken, zoals 7705, 7706, 7712 en 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Een miniform voor ADCS maken  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Miniforms** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3.  Voer in het veld **Code** een code in voor het miniform. Geef desgewenst in alle andere velden waarden op.  

    Schakel het selectievakje **Start miniform** in om aan te geven dat het miniform het eerste formulier is dat de gebruiker bij het aanmelden ziet.  

4.  Definieer op het sneltabblad **Regels** de velden die op het miniform worden weergegeven. De volgorde waarin u de regels invoert, is de volgorde waarin de regels op het draagbare apparaat worden weergegeven.  

Wanneer u een miniform hebt gemaakt, volgt u de volgende stappen om functies te maken en functionaliteit aan verschillende toetsenbordinvoerwaarden te koppelen.  

### <a name="to-customize-miniform-functions"></a>Miniformfuncties aanpassen  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Miniforms** in en kies de gerelateerde koppeling.  
2.  Selecteer een miniform in de lijst en kies vervolgens de actie **Bewerken**.  
3.  Kies de actie **Functies**.  
4.  Selecteer in de vervolgkeuzelijst **Functie** een code voor de functie die u wilt koppelen aan het miniform. U kunt bijvoorbeeld ESC selecteren, zodat u functionaliteit koppelt aan het drukken op de toets ESC.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]