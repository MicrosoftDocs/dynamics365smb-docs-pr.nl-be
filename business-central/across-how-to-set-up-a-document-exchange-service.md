---
title: Een service voor documentuitwisseling instellen | Microsoft Docs
description: U gebruikt een externe serviceprovider om elektronische documenten uit te wisselen met uw handelspartners.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-a-document-exchange-service"></a>Een service voor documentuitwisseling instellen

Als onderdeel van het Data Exchange Framework kunt u zonder extra stappen verkoop- en inkoopdocumenten uitwisselen met uw handelspartners, zoals het toevoegen van de documenten aan e-mailberichten als PDF-bestanden. Als u bijvoorbeeld klaar bent om een klant te factureren, kunt u de factuur boeken en voor betaling verzenden als een bestand dat uw klant kan ontvangen in hun bedrijfsbeheertoepassing. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.

> [!NOTE]
> Het opzetten van een documentuitwisselingsservice voor Business Central on-premises vereist enkele aanvullende stappen voor autorisatie. Zie voor meer informatie [Instellingen voor Business Central On-Premises](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Verbinding maken met handelspartners

Het uitwisselen van elektronische documenten vereist een verbinding met uw handelspartners. Om het eenvoudig te maken om een beveiligde verbinding tot stand te brengen, is [!INCLUDE[prod_short](includes/prod_short.md)] online geconfigureerd om de app voor Business Central-integratie te gebruiken. De app is beschikbaar in de Tradeshift App Store en u en uw zakenpartners hoeven alleen maar een Tradeshift-account te maken en vervolgens de app in te schakelen. De app Business Central-integratie is verkrijgbaar in productie- en sandboxversies. Het gebruik van de sandboxversie is bijvoorbeeld goed voor het testen van de documentuitwisseling. U kunt schakelen tussen productie- en sandboxversies door de schakelaar **Sandbox** aan of uit te zetten op de pagina **Instellingen service doc.uitw.**. Als u dat doet, wordt de informatie op het sneltabblad **Onderhoud** voor u bijgewerkt.

Als u een andere service wilt gebruiken, moet u informatie verstrekken om de verbinding tot stand te brengen. Zie [Verbinding maken met een documentuitwisselingsservice](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service) voor meer informatie.

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Verbinding maken met de app Business Central-integratie op Tradeshift

U kunt snel een Tradeshift-account maken en aan de slag gaan met de app Business Central-integratie vanaf de pagina **Instellingen service doc.uitw.**. Kies de koppeling **App activeren** in het bericht of het veld **App-URL** om naar de app in de Tradeshift app store te gaan. Op de aanmeldpagina voor Tradeshift logt u in of meldt u zich aan.

> [!NOTE]
> Nadat u bent ingelogd op uw Tradeshift-account, brengt de site u mogelijk niet naar de pagina waar u de app activeert. Om dat te doen kunt u op de koppeling op de pagina **Instellingen service doc.uitw.** klikken in Business Central om direct naar de app te gaan.

Als u besluit de app Business Central-integratie niet meer te gebruiken, moet u deze uitschakelen in de Tradeshift-app store. 

## <a name="to-connect-to-a-document-exchange-service"></a>Verbinding maken met een documentuitwisselingsservice

Als u liever een andere documentuitwisselingsservice gebruikt, moet u wat informatie verstrekken om verbinding te maken met de service.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Documentuitwisselingsservice instellen** in en kies de gerelateerde koppeling.  
2. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Gebruikersagent**|Voer tekst in die kan worden gebruikt om uw bedrijf te identificeren in processen voor documentuitwisseling.|  
    |**Ingeschakeld**|Geef op of de verbinding met de service is ingeschakeld.<br><br> **Opmerking:** als u de service inschakelt, worden ten minste twee taakwachtrijposten gemaakt om elektronische documenten te verzenden en ontvangen. Wanneer u de service uitschakelt, worden de taakwachtrijposten verwijderd.|  
    |**Sandbox**|Geef op of u verbinding maakt met een sandboxversie van de documentuitwisselingsservice.|
    |**Aanmeld-URL**|Geef de webpagina op waarop u zich aanmeldt voor de service voor documentuitwisseling.|  
    |**App-URL**|Kies de koppeling om de app store te openen en de app Business Central-integratie in of uit te schakelen.|
    |**Service-URL**|Geef het adres op van de service voor documentuitwisseling die wordt aangeroepen wanneer u elektronische documenten verzendt en ontvangt.|  
    |**Aanmeld-URL**|Geef de URL op voor de pagina waarop u zich aanmeldt voor de service voor documentuitwisseling. Dit is de pagina waar u de gebruikersnaam en het wachtwoord van uw bedrijf invoert.|  
    
    > [!NOTE]  
    > Uw aanmeldgegevens worden automatisch versleuteld. U kunt versleuteling niet uitschakelen.

    > [!NOTE]
    > Als u geen verbinding kunt maken met de documentuitwisselingsservice vanwege een autorisatieprobleem, kan dat zijn omdat [!INCLUDE[prod_short](includes/prod_short.md)] het toegangstoken niet automatisch kan vernieuwen. Dit kan bijvoorbeeld gebeuren als u de service enige tijd niet hebt gebruikt. U kunt het token handmatig vernieuwen met behulp van de actie **Token vernieuwen**.

## <a name="settings-for-business-central-on-premises"></a>Instellingen voor Business Central On-Premises

Om Business Central on-premises te verbinden, moet u een app maken in de Tradeshift App Store. Als u dat doet, gebruikt u de omleidings-URL uit het veld **Omleidings-URL** op de pagina **Documentuitwisselingsservice instellen**. Nadat u uw app hebt geregistreerd, verstrekt Tradeshift een klant-id en een klantgeheim. Voer deze waarden in [!INCLUDE[prod_short](includes/prod_short.md)] in op het tabblad **Autorisatie** op de pagina **Instellingen voor documentuitwisselingsservice**.

Als u de app-id en het geheim liever op een andere locatie opslaat, kunt u de velden Client-id en Clientgeheim leeg laten en een extensie schrijven om de id en het geheim van de locatie op te halen. U kunt het geheim tijdens runtime verstrekken door u te abonneren op de gebeurtenissen OnGetClientId en OnGetClientSecret events in codeunit 1410 'Beheer service doc.uitw.'

## <a name="see-also"></a>Zie ook

[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
