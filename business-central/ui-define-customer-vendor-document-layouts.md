---
title: Documentlay-outs aan klanten of leveranciers toewijzen
description: Gebruik documentlay-outs om het uiterlijk en de indeling te bepalen van documenten zoals facturen en orders die u naar klanten en leveranciers verzendt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Documentlay-outs definiëren voor klanten en leveranciers

Documentlay-outs gebruiken rapportlay-outs om het uiterlijk te definiëren van documenten die u naar klanten en leveranciers verzendt. Business Central biedt standaardlay-outs, maar u kunt ook aangepaste lay-outs aanpassen voor elk van uw zakenpartners. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md). U selecteert standaard en aangepaste documentlay-outs van klanten- en leverancierskaarten door de actie **Documentlay-outs** te kiezen. De waarde in het veld **Gebruik** definieert het proces waarvoor de documentlay-out wordt gebruikt. Voor klanten kunt u bijvoorbeeld de soorten documentlay-outs **Aanmaning**, **Verzending** en **Bevestiging** gebruiken.

Documentlay-outs kunnen u ook tijd besparen wanneer u documenten per e-mail naar klanten- of leverancierscontacten verzendt. Voor elke lay-out die u aan de klant of het contact toewijst, kunt u een of meer contact-e-mailadressen opgeven. U kunt bijvoorbeeld een factuur sturen naar de inkoop- en magazijncontacten van de klant. Het toevoegen van contact-e-mailadressen is eenvoudig. Op de pagina  **documentindelingen** kunt u met de actie  **e-mail selecteren uit contactpersonen**  een keuze maken uit een lijst met e-mailadressen die u voor de klant of leverancier hebt geregistreerd. U kunt e-mailadressen ook handmatig toevoegen. Als u meerdere adressen invoert, scheid ze dan met een puntkomma en voeg geen spaties toe tussen de adressen.

Voordat u kunt definiëren welke documentlay-out wordt gebruikt voor welke processen en naar welke contactpersoon het document moet worden verzonden, moet u alle beschikbare rapporten (documenten) laden vanaf de pagina **Selecties rapporteren**. U kunt de documenten snel laden met behulp van de actie **Kopiëren uit rapportselectie** op de pagina **Documentlay-outs**.

De stappen in de volgende secties beschrijven hoe u verkoopdocumentlay-outs definieert vanuit de pagina **Klantenkaart**. Voor leveranciers zijn de stappen hetzelfde vanaf de pagina **Leverancierskaart**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>De standaarddocumentlay-outs voor verkoopdocumenten voor een klant laden

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de pagina **Klantenkaart** voor de klant en kies vervolgens de actie **Documentlay-outs**.
3. Kies op de pagina **Documentlay-outs** de actie **Kopiëren uit rapportselectie**.

De pagina **Documentlay-outs** toont alle lay-outs die beschikbaar zijn voor verkoopdocumenten. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Een aangepaste rapportlay-out selecteren om te gebruiken voor de lay-out van het verkoopdocument

Bij de volgende stappen wordt ervan uitgegaan dat u al een aangepast rapport indeling hebt voor het type document. Als u nog geen aangepast rapport indeling hebt, moet u er eerst een maken. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de pagina **Klantenkaart** voor de klant en kies vervolgens de actie **Documentlay-outs**.
3. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out waarvoor u een aangepaste lay-out wilt gebruiken, het veld **Aangepaste lay-outbeschrijving**.

   > [!TIP]
   > Standaard is het veld Aangepaste indeling Beschrijving verborgen. Als het veld niet beschikbaar is, kunt u de pagina personaliseren om het toe te voegen. Om de pagina te personaliseren, kiest u het :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="instellingen-pictogram."::: Pictogram en kies vervolgens  **Personaliseren**. Ga naar  [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie over het personaliseren van pagina's.

1. Selecteer op de pagina **Aangepaste rapportlay-outs** de speciale documentlay-out die u wilt gebruiken voor het type verkoopdocument. Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>Om aan te geven welk contact welk document indeling voor een klant ontvangt

Om tijd te besparen wanneer u documenten per e-mail naar contacten van klanten en leveranciers verzendt, geeft u hun e-mailadressen op in documentlay-outs. U kunt bijvoorbeeld altijd klantafschriften verzenden naar accountantcontacten van klanten, verkooporders naar inkopers van klanten en inkooporders naar verkopers van leveranciers.

1. Kies op de pagina **Documentlay-outs** op de regel voor een rapportlay-out die u naar een specifiek contact voor de klant wilt verzenden, de actie **E-mail selecteren vanuit contacten**.
2. Selecteer op de **Contacten** een of meer contacten en kies vervolgens **OK**.

## <a name="see-also"></a>Zie ook

[Aangepaste rapportlay-outs bijwerken](ui-update-report-layouts.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Een aangepaste lay-out voor een rapport of document importeren en exporteren](ui-how-import-and-export-report-layout.md)  
[Documenten verzenden via e-mail](ui-how-send-documents-email.md)  
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
