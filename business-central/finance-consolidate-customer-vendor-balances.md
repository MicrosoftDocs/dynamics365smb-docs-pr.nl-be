---
title: Saldi consolideren voor een bedrijf dat een klant en een leverancier is
description: Hierin wordt beschreven hoe u saldi kunt consolideren voor een klant die tevens leverancier is.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor" />Saldi consolideren voor een bedrijf dat een klant en een leverancier is
Een bedrijf waarmee u zaken doet, kan zowel een klant als een leverancier zijn. In dat geval kunt u voorkomen dat u onnodige betalingen of ontvangsten doet, en misschien besparen op transactiekosten, door de klant- en leverancierssaldi van het bedrijf te consolideren. Bij consolidatie worden de saldi van het bedrijf als leverancier en als klant vergeleken en wordt het bedrag vervolgens gesaldeerd, zodat het saldo van de klant of leverancier overblijft, afhankelijk van welk bedrag hoger was. 

Als u de saldi wilt consolideren, moet u eerst de klant- en leveranciersbedrijven koppelen via een contactpersoon met het type **Bedrijf**. Een klant of leverancier kan slechts één contactpersoon van het type **Bedrijf** hebben. Zie [Contactpersonen maken](marketing-create-contact-companies.md) voor meer informatie.

Nadat u de bedrijven hebt gekoppeld, biedt de pagina **Klantenkaart** het veld **Saldo als leverancier** en bevat de pagina **Leverancierskaart** het veld **Saldo als klant**.

Hoewel het geen vereiste is, zijn de klant- en leveranciersbedrijven doorgaans dezelfde rechtspersoon. 

## <a name="before-you-start" />Voordat u begint
Voordat u saldi consolideert, moet u enkele instellingen opgeven op de pagina **Marketinginstellingen**. 

* Op het sneltabblad **Interacties** moet u zakelijke relatiecodes opgeven in de velden **Klanten** en **Leveranciers**. [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt deze informatie om te bepalen welk type relatie moet worden weergegeven voor contactpersonen. 
* Optioneel: schakel op het sneltabblad **Duplicaten** de optie voor het zoeken van duplicaten in of uit. Zoeken naar duplicaten is standaard ingeschakeld. Zie [Duplicaten verwerken](#handling-duplicates) voor meer informatie. 

## <a name="link-an-existing-customer-and-vendor-company-thorough-a-contact" />Een bestaand klant- en leveranciersbedrijf koppelen via een contactpersoon
In de volgende stappen wordt beschreven hoe u een klant en een leverancier kunt koppelen via een contactpersoon.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant of leverancier en kies vervolgens de actie **Contactpersoon**.
3. Als het veld **Zakenrelatie contact** een andere waarde dan **Geen** bevat, moet u de relatie verwijderen. Gebruik hiervoor de actie **Zakenrelatie** en verwijder vervolgens de relatie. 
4. Afhankelijk van of u **Klant** of **Leverancier** kiest in stap 1, kiest u de ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"). pictogram en voer vervolgens de tegenpartij in. Dat wil zeggen, als u **Leverancier** kiest, moet u zoeken naar **Klant**.
5. Kies de leverancier of klant en kies vervolgens de actie **Contactpersonen**.
6. Kies de actie **Koppelen aan bestaande** en kies vervolgens de optie **Klant** of **Leverancier**.
7. Kies de klant of leverancier.

## <a name="create-a-vendor-from-a-customer-or-vice-versa" />Een klant maken van een leverancier of omgekeerd
U kunt een nieuwe leverancier maken van een bestaande klant of een nieuwe klant van een leverancier. Open op de pagina **Klant** of **Leverancier** de pagina **Contactpersoon**. Kies de actie **Maken als** en kies vervolgens de optie **Klant** of **Leverancier**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact" />Een nieuwe klant of leverancier maken en deze koppelen via een contactpersoon voor leverancier of klant
1. Maak een nieuwe klant of leverancier. Zie [Nieuwe klanten registreren](sales-how-register-new-customers.md) of [Nieuwe leveranciers registreren](sales-how-register-new-customers.md) voor meer informatie.
2. Nadat u de klant of leverancier hebt ingesteld, kiest u de actie **Maken** en kiest u vervolgens de optie **Klant** of **Leverancier**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company" />De klant- en leverancierssaldi consolideren voor een contactpersoon Bedrijf
Gebruik op de pagina **Betalingsdagboek** de actie **Nettosaldi van klanten/leveranciers** om de klant- en leverancierssaldi te consolideren tot een enkel nettobedrag. De actie maakt betalingsdagboekregels die de nettosaldi bevatten, maar boekt deze niet.

> [!NOTE]
> Als de klant- of leverancierssaldi bedragen in verschillende valuta's bevatten, wordt een regel gemaakt voor het bedrag in elke valuta.

## <a name="handling-duplicates" />Duplicaten verwerken
Als u duplicaten zoeken inschakelt op het sneltabblad **Duplicaten** op de pagina **Marketinginstellingen**, wordt er een waarschuwing weergegeven wanneer u de waarden wijzigt van velden die deel uitmaken van de instellingen voor dubbele zoekreeksen. Wanneer een duplicaat wordt gevonden, kunt u de volgende acties ondernemen:

* Combineer de dubbele contactpersonen tot een enkele contactpersoon die hetzelfde is voor zowel de klant als de leverancier met behulp van de mogelijkheid **Samenvoegen met** op de pagina **Contactkaart**. Gewoonlijk wordt het samenvoegen van contactpersonen alleen uitgevoerd als de klant en de leverancier dezelfde rechtspersoon zijn. Zie voor meer informatie [Dubbele records samenvoegen](sales-how-merge-duplicate-records.md). 
* Verwijder de zakelijke relatie van de leverancier voor de leverancier- of klantcontactpersoon en gebruik vervolgens de actie **Koppelen aan bestaande** om aan een andere contactpersoon te koppelen.    

## <a name="see-also" />Zie ook
[Verkoop](sales-manage-sales.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
