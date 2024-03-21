---
title: De connector voor e-documenten instellen met externe eindpunten
description: In dit artikel wordt uitgelegd hoe u de functionaliteit van e-documenten instelt wanneer deze is verbonden met externe eindpunten.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="set-the-e-documents-connector-with-external-endpoints"></a>De connector voor e-documenten instellen met externe eindpunten

In dit artikel wordt uitgelegd hoe u de functionaliteit van e-documenten instelt wanneer deze is verbonden met externe eindpunten.

Voordat u de functionaliteit gebruikt die in dit artikel wordt beschreven, installeert u de app **Connector voor e-documenten met externe eindpunten** boven op de algemene app **E-documentkern**. Deze app kan voor standaardintegratie met de toegangspunten van de externe (derde) partij worden gebruikt om de e-documentstroom te automatiseren. Omdat deze app slechts enkele geselecteerde connectoren vertegenwoordigt, bent u niet beperkt tot bestaande integraties daarin. De meeste connectoren zullen in de toekomst beschikbaar zijn op AppSource .

## <a name="set-up-the-connection"></a>De verbinding instellen

Om met de installatie te beginnen volgt u de stappen in [App E-documentkern](finance-how-setup-edocuments.md). Nadat u deze stappen heeft voltooid, gaat u terug naar dit artikel en voert u de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-documentservices** in en selecteer vervolgens de gerelateerde koppeling
2. Selecteer in het veld **Service-integratie** een van de integratiecodes die worden aangeboden voor de instelling van de eindpuntservice.
3. Selecteer **Service-integratie instellen**.
4. Selecteer op de pagina **Instelling van externe verbinding van e-document** **Autorisatiecode aanvragen**. U wordt omgeleid naar de webpagina voor autorisatie van de externe service en wordt om uw aanmeldingsgegevens gevraagd.
5. Kopieer de autorisatiecode naar het veld **Autorisatiecode invoeren**.
6. Selecteer **Toegangstoken vernieuwen** om er zeker van te zijn dat u de token kunt vernieuwen.

    > [!NOTE]
    > Deze verbinding vereist communicatie met externe serviceproviders die mogelijk extra moeten betalen en contracten met hen vereisen. Neem contact op met de serviceproviders voor alle benodigde inloggegevens.

7. Vul op de pagina **Instelling van externe verbinding van e-document** de volgende velden in:

    | Veldnaam | Omschrijving |
    |---|---|
    | URL van bestands-API | Geef de URL van de bestands-API op. |
    | URL van bestandsonderdelen | Geef de URL van de bestandsonderdelen op. |
    | URL van document-API | Geef de URL van de document-API op. |
    | Bedrijfs-id | Geef de bedrijfs-id op. |
    | Verzendmodus | Geef de verzendmodus op. U kunt **Productie**, **Test** of **Certificering** selecteren. |

    > [!NOTE]
    > Vraag uw serviceprovider naar alle voorgaande details om verbinding te maken met hun toegangspunt.

## <a name="set-up-company-information"></a>Bedrijfsgegevens instellen

Voordat u e-documenten gaat gebruiken, moet u uw pagina **Bedrijfsgegevens** bijwerken door de volgende stappen te voltooien:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsgegevens** in en selecteer vervolgens de gerelateerde koppeling.
2. Naast het invullen van de gebruikelijke velden, moet u ook de volgende velden invullen:

    | Veldnaam | Omschrijving |
    |---|---|
    | SWIFT-code | Geef de SWIFT-code (internationale bank-id) op van uw primaire bank. |
    | Bankfiliaalnr. | Vermeld het viercijferige filiaalnummer van de bank. |
    | Btw-nr. | Geef het btw-registratienummer van het bedrijf op. |

3. De pagina sluiten.

## <a name="set-up-customers-to-receive-e-documents"></a>Klanten instellen om e-documenten te ontvangen

Om klanten in staat te stellen uw e-documenten te ontvangen, voert u de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en selecteer vervolgens de gerelateerde koppeling.
2. Open de kaart **Klant**.
3. Naast het invullen van de gebruikelijke velden, specificeert u in het veld **GLN** de klant in verband met het verzenden van elektronische documenten.
4. Markeer het veld **GLN gebruiken in elektronische documenten** om aan te geven of het Global Location Number (GLN) wordt gebruikt als partij-identificatienummer in elektronische documenten.
5. De pagina sluiten.

## <a name="other-setup"></a>Overige instelling

Voordat u met e-documenten gaat werken, stelt u de **werkstromen** voor e-documenten en de **documentverzendprofielen** in om uw werkstromen te gebruiken. Nadat de serviceverbinding tot stand is gebracht, kunt u uw e-documentoplossing gaan gebruiken.

## <a name="available-service-providers"></a>Beschikbare serviceproviders

Microsoft wil providers van toegangspunten aanmoedigen om hun connectoren boven op ons framework **E-documentkern** toe te voegen.

Momenteel is Pagero de enige toegangspuntprovider die onder dit systeem valt. Microsoft heeft geen contractuele verplichting met Pagero. Daarom moet u een contract met hen afsluiten om alle benodigde inloggegevens te verkrijgen.

We zullen deze lijst bijwerken zodra we nieuwe aanbieders van toegangspunten voor de uitwisseling van e-documenten krijgen.

## <a name="see-also"></a>Zie ook

[Hoe u belastingen instelt in Business Central](finance-how-setup-edocuments.md)  
[Hoe u e-documenten gebruikt in Business Central](finance-how-use-edocuments.md)  
[Hoe u e-documenten uitbreidt in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Financieel beheer](finance.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Aankopen registreren met inkoopfacturen en orders](purchasing-how-record-purchases.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
