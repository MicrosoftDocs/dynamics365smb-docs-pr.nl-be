---
title: Servicecontracten converteren | Microsoft Docs
description: Omdat het wijzigingstool btw-tarief servicecontracten niet kan converteren, moeten deze contracten handmatig worden geconverteerd. In dit onderwerp worden diverse alternatieve methoden beschreven die u voor de conversie van het servicecontract kunt gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ed1f0d928299a1f72b40be6e7fe1ac1567c4906c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194944"
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Servicecontracten met btw-bedragen converteren
Omdat het wijzigingstool btw-tarief servicecontracten niet kan converteren, moeten deze contracten handmatig worden geconverteerd. In dit onderwerp worden diverse alternatieve methoden beschreven die u voor de conversie van het servicecontract kunt gebruiken.  

> [!NOTE]  
>  Dit onderwerp biedt een verkorte versie van de werkstroom.  

 In de volgende procedure wordt beschreven hoe u een factuur kunt corrigeren die een jaar van tevoren in het kader van een vooruitbetaald servicecontract is gemaakt.  

> [!NOTE]  
>  In dit voorbeeld moet u de werkdatum wijzigen in 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Een factuur voor een vooruitbetaald servicecontract corrigeren  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Contractbeheer** in en kies de gerelateerde koppeling.  
2. Onder **Lijsten** kiest u **Servicecontracten**.  
3. Maak een nieuw vooruitbetaald servicecontract. Voer de begindatum **01-01-2017** en een factuurperiodejaar in voor de klant **20000**.  
4. Als u het contract wilt tekenen, kiest u de actie **Contract tekenen**.  
5. Een servicefactuur maken.
6. De factuur wordt vermeld als een niet geboekte servicefactuur. Als u de servicefactuur wilt weergeven, kiest u de actie **Service**, de actie **Contractbeheer** en tot slot de actie **Servicefacturen**.  
7. Boek de servicefactuur.  

> [!NOTE]  
>  Wijzig de niet geboekte servicefactuur niet. Aangezien de serviceposten worden gemaakt wanneer de factuur is gemaakt, zal een wijziging in de niet geboekte factuur de reeds gemaakte serviceposten niet wijzigen. De btw-posten worden echter gemaakt wanneer de factuur wordt geboekt. Zo kunt u de algemene productboekingsgroep en de APS productboekingsgroep op de niet geboekte servicefactuur wijzigen.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Creditnota's voor het btw-verschil maken  
In de volgende procedure wordt beschreven hoe u een creditnota kunt maken die alleen het btw-verschil bevat voor de reeds gefactureerde periode die begint op **01-07-2017**. In dit voorbeeld wordt het btw-bedrag alleen geboekt naar de module Financieel beheer en niet naar de module Servicebeheer. De btw-posten die zijn gekoppeld aan de servicepost worden niet gecorrigeerd.  

1. Een nieuwe grootboekrekening maken voor het btw-verschil. Deze account wordt gebruikt voor de directe boeking van de btw-correctie.  
2. Voeg een nieuwe regel toe aan de btw-boekingsinstellingen.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Contractvervaldatums in contractregels maken  
In de volgende procedure wordt beschreven hoe u nieuwe contracten kunt maken door te werken met contractvervaldatums in servicecontractregels.  

1. Stel op de pagina **Servicecontract** de contractvervaldatum in op **30-06-2017**.  
2. Kies de actie **Creditnota maken** om automatisch een creditnota te maken voor juli 2017 tot december 2017.  
3. Omdat het contract is verlopen, moet u een nieuw contract maken voor de periode met het nieuwe btw-tarief voor 1 juli 2017 tot en met 31 december 2017.  

### <a name="to-create-a-new-credit-memo"></a>Een nieuwe creditnota maken  
In de volgende procedure wordt beschreven hoe u een nieuwe creditnota met de batchtaak **Vooruitbetaalde contractposten ophalen** kunt maken. Posten van januari 2017 tot en met juni 2017 die u niet wilt corrigeren, worden verwijderd.  

1. Voer de Wijzigingstool btw-tarief op 1 juli 2017 uit. De algemene productboekingsgroep of de btw-productboekingsgroep wordt gewijzigd. Zie voor meer informatie [Met btw werken bij verkoop en inkoop](finance-work-with-vat.md).  
2. Voer na het uitvoeren van het wijzigingstool btw-tarief een contractvervaldatum voor het servicecontract in. U kunt nu de servicecontractregel verwijderen en een nieuwe regel maken die identiek is aan de oude.  
3. Maak een nieuwe factuur voor de periode januari 2017 tot en met december 2012 met het nieuwe btw-tarief.  
4. Als u nog een creditnota wilt maken, kiest u op de pagina **Servicecreditnota's** de actie **Nieuw** om een nieuwe servicecreditnota te maken.  
5. Kies de actie **Vooruitbet. contractposten ophalen**.  
6. Nadat de conversie is voltooid, zijn de btw en de serviceposten correct.  

## <a name="see-also"></a>Zie ook  
[Werken met servicecontracten en servicecontractoffertes](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Financiën](finance.md)  
[Btw rapporteren aan de belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
