---
title: Documentlay-outs aan klanten of leveranciers toewijzen
description: Gebruik documentlay-outs om het uiterlijk en de indeling te bepalen van documenten zoals facturen en orders die u naar klanten en leveranciers verzendt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 04/07/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Documentlay-outs definiëren voor klanten en leveranciers

Documentlay-outs gebruiken rapportlay-outs om het uiterlijk te definiëren van documenten die u naar klanten en leveranciers verzendt. Business Central biedt standaardlay-outs, maar u kunt ook aangepaste lay-outs aanpassen voor elk van uw zakenpartners. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md). U selecteert standaard en aangepaste documentlay-outs van klanten- en leverancierskaarten door de actie **Documentlay-outs** te kiezen. De waarde in het veld **Gebruik** definieert het proces waarvoor de documentlay-out wordt gebruikt. Voor klanten kunt u bijvoorbeeld de soorten documentlay-outs **Aanmaning**, **Verzending** en **Bevestiging** gebruiken.

Documentlay-outs kunnen u ook tijd besparen wanneer u documenten per e-mail naar klanten- of leverancierscontacten verzendt. Voor elke lay-out die u aan de klant of het contact toewijst, kunt u een of meer contact-e-mailadressen opgeven. U kunt bijvoorbeeld een factuur sturen naar de inkoop- en magazijncontacten van de klant. Het toevoegen van contact-e-mailadressen is eenvoudig. Op de pagina **Documentlay-outs** kunt u met de actie **E-mail selecteren vanuit contacten** kiezen uit een lijst met de contact-e-mailadressen die u hebt geregistreerd voor de klant of leverancier. U kunt e-mailadressen ook handmatig toevoegen. Als u meerdere adressen invoert, scheid ze dan met een puntkomma en voeg geen spaties toe tussen de adressen.

Voordat u kunt definiëren welke documentlay-out wordt gebruikt voor welke processen en naar welke contactpersoon het document moet worden verzonden, moet u alle beschikbare rapporten (documenten) laden vanaf de pagina **Selecties rapporteren**. U kunt de documenten snel laden met behulp van de actie **Kopiëren uit rapportselectie** op de pagina **Documentlay-outs**.

De stappen in de volgende secties beschrijven hoe u verkoopdocumentlay-outs definieert vanuit de pagina **Klantenkaart**. Voor leveranciers zijn de stappen hetzelfde vanaf de pagina **Leverancierskaart**.

## De standaarddocumentlay-outs voor verkoopdocumenten voor een klant laden

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de pagina **Klantenkaart** voor de klant en kies vervolgens de actie **Documentlay-outs**.
3. Kies op de pagina **Documentlay-outs** de actie **Kopiëren uit rapportselectie**.

De pagina **Documentlay-outs** toont alle lay-outs die beschikbaar zijn voor verkoopdocumenten. 

## Een aangepaste rapportlay-out selecteren om te gebruiken voor de lay-out van het verkoopdocument

Als u nog geen aangepaste rapportlay-out voor het type document heeft gemaakt, moet u dat eerst doen. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de pagina **Klantenkaart** voor de klant en kies vervolgens de actie **Documentlay-outs**.
3. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out waarvoor u een aangepaste lay-out wilt gebruiken, het veld **Aangepaste lay-outbeschrijving**.
4. Selecteer op de pagina **Aangepaste rapportlay-outs** de speciale documentlay-out die u wilt gebruiken voor het type verkoopdocument. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

## Opgeven welk contact welke documentlay-out voor een klant ontvangt

Om tijd te besparen wanneer u documenten per e-mail naar contacten van klanten en leveranciers verzendt, geeft u hun e-mailadressen op in documentlay-outs. U kunt bijvoorbeeld altijd klantafschriften verzenden naar accountantcontacten van klanten, verkooporders naar inkopers van klanten en inkooporders naar verkopers van leveranciers.

1. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out die u naar een specifiek contact voor de klant wilt verzenden, de actie **E-mail selecteren vanuit contacten**.
2. Selecteer op de **Contacten** een of meer contacten en kies vervolgens **OK**.

## Zie ook

[Aangepaste rapportlay-outs bijwerken](ui-update-report-layouts.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Een aangepaste indeling voor een rapport of document importeren of exporteren](ui-how-import-and-export-report-layout.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
