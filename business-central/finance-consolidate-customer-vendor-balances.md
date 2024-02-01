---
title: Saldi consolideren voor een bedrijf dat een klant en een leverancier is
description: Hierin wordt beschreven hoe u saldi kunt consolideren voor een klant die tevens leverancier is.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Saldi consolideren voor een bedrijf dat een klant en een leverancier is
Een bedrijf waarmee u zaken doet, kan zowel een klant als een leverancier zijn. In dat geval kunt u voorkomen dat u onnodige betalingen of ontvangsten doet, en misschien besparen op transactiekosten, door de klant- en leverancierssaldi van het bedrijf te consolideren. Bij consolidatie worden de saldi van het bedrijf als leverancier en als klant vergeleken en wordt het bedrag vervolgens gesaldeerd, zodat het saldo van de klant of leverancier overblijft, afhankelijk van welk bedrag hoger was. 

Als u de saldi wilt consolideren, moet u eerst de klant- en leveranciersbedrijven koppelen via een contactpersoon met het type **Bedrijf**. Een klant of leverancier kan slechts één contactpersoon van het type **Bedrijf** hebben. Zie [Contactpersonen maken](marketing-create-contact-companies.md) voor meer informatie.

Nadat u de bedrijven hebt gekoppeld, biedt de pagina **Klantenkaart** het veld **Saldo als leverancier** en bevat de pagina **Leverancierskaart** het veld **Saldo als klant**.

Hoewel het geen vereiste is, zijn de klant- en leveranciersbedrijven doorgaans dezelfde rechtspersoon. 

## Voordat u begint
Voordat u saldi consolideert, moet u enkele instellingen opgeven op de pagina **Marketinginstellingen**. 

* Op het sneltabblad **Interacties** moet u zakelijke relatiecodes opgeven in de velden **Klanten** en **Leveranciers**. [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt deze informatie om te bepalen welk type relatie moet worden weergegeven voor contactpersonen. 
* Optioneel: schakel op het sneltabblad **Duplicaten** de optie voor het zoeken van duplicaten in of uit. Zoeken naar duplicaten is standaard ingeschakeld. Zie [Duplicaten verwerken](#handling-duplicates) voor meer informatie. 

## Een bestaand klant- en leveranciersbedrijf koppelen via een contact
In de volgende stappen wordt beschreven hoe u een klant en een leverancier kunt koppelen via een contactpersoon.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant of leverancier en kies vervolgens de actie **Contactpersoon**.   
3. Kies het contact en kies vervolgens de actie **Koppelen aan bestaande**.
4. Kies het type entiteit waarmee u een zakenrelatie wilt aangaan.
5. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Een klant maken van een leverancier of omgekeerd
U kunt een nieuwe leverancier maken van een bestaande klant of een nieuwe klant van een leverancier. Open op de pagina **Klant** of **Leverancier** de pagina **Contactpersoon**. Kies de actie **Maken als** en kies vervolgens de optie **Klant** of **Leverancier**. 

## Een nieuwe klant of leverancier maken en deze koppelen via een contactpersoon voor leverancier of klant
1. Maak een nieuwe klant of leverancier. Zie [Nieuwe klanten registreren](sales-how-register-new-customers.md) of [Nieuwe leveranciers registreren](sales-how-register-new-customers.md) voor meer informatie.
2. Nadat u de klant of leverancier hebt ingesteld, kiest u de actie **Maken** en kiest u vervolgens de optie **Klant** of **Leverancier**. 

## De klant- en leverancierssaldi consolideren voor een contactpersoon Bedrijf
Gebruik op de pagina **Betalingsdagboek** de actie **Nettosaldi van klanten/leveranciers** om de klant- en leverancierssaldi te consolideren tot een enkel nettobedrag. De actie maakt betalingsdagboekregels die de nettosaldi bevatten, maar boekt deze niet.

> [!NOTE]
> Als de klant- of leverancierssaldi bedragen in verschillende valuta's bevatten, wordt een regel gemaakt voor het bedrag in elke valuta.

## Duplicaten verwerken
Als u duplicaten zoeken inschakelt op het sneltabblad **Duplicaten** op de pagina **Marketinginstellingen**, wordt er een waarschuwing weergegeven wanneer u de waarden wijzigt van velden die deel uitmaken van de instellingen voor dubbele zoekreeksen. Wanneer een duplicaat wordt gevonden, kunt u de volgende acties ondernemen:

* Combineer de dubbele contactpersonen tot een enkele contactpersoon die hetzelfde is voor zowel de klant als de leverancier met behulp van de mogelijkheid **Samenvoegen met** op de pagina **Contactkaart**. Gewoonlijk wordt het samenvoegen van contactpersonen alleen uitgevoerd als de klant en de leverancier dezelfde rechtspersoon zijn. Zie voor meer informatie [Dubbele records samenvoegen](sales-how-merge-duplicate-records.md). 
* Verwijder de zakelijke relatie van de leverancier voor de leverancier- of klantcontactpersoon en gebruik vervolgens de actie **Koppelen aan bestaande** om aan een andere contactpersoon te koppelen.    

## Zie ook
[Verkoop](sales-manage-sales.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
