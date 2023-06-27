---
title: Btw-nummers valideren
description: 'Laat Business Central btw-registratienummers en andere bedrijfsinformatie voor uw contacten, klanten en leveranciers valideren, op basis van de EU VIES btw-nummervalidatieservice.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="validate-vat-registration-numbers"></a>Btw-nummers valideren

Het is belangrijk dat de btw-registratienummers die u voor klanten, leveranciers en contacten hebt, geldig zijn als u [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt in een land/regio die btw gebruikt. Bedrijven wijzigen bijvoorbeeld soms hun belastingplichtigheidsstatus en in sommige landen/regio's kan de belastingdienst u vragen om rapporten te verschaffen, zoals het rapport **Verkoopoverzicht EU**, waarin de btw-registratienummers worden weergegeven die u gebruikt wanneer u zaken doet.

De Europese commissie verschaft de VIES-service voor btw-nummervalidatie op de website. Deze service is openbaar en gratis. [!INCLUDE [prod_short](includes/prod_short.md)] kan u moeite besparen. U kunt namelijk de VIES-service gebruiken om btw-nummers en andere bedrijfsgegevens voor klanten, leveranciers en contacten te valideren en bij te houden. De service in [!INCLUDE [prod_short](includes/prod_short.md)] heet **Instelling van validatieservice van EU-btw-nummers**. De service is beschikbaar op de pagina **Serviceverbindingen** en u kunt deze service meteen gebruiken. De serviceverbinding is gratis en er is geen extra aanmelding vereist.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically"></a>Configureer de service om btw-registratienummers automatisch te verifiëren

Als u de **validatieservice van EU-btw-nummers** wilt inschakelen, opent u het item op de pagina **Serviceverbinding**. Als het veld **Eindpunt van service** nog niet is ingevuld, gebruikt u de actie **Standaardeindpunt instellen**. Stel vervolgens het veld **Geactiveerd** in en u bent klaar.  

> [!IMPORTANT]
> Als u de validatieservice wilt inschakelen, moet u over beheerdersmachtigingen beschikken.

Stel optioneel sjablonen in voor de soorten btw-gerelateerde gegevens die u ook door de service wilt laten controleren. Zie het gedeelte [Validatiesjablonen](#validation-templates) voor meer informatie.

Wanneer u onze serviceverbinding gebruikt, registreren we een overzicht van btw-nummers en verificaties voor elke klant, leverancier of contactpersoon in het **Btw-log**, zodat u deze eenvoudig kunt bijhouden. Het logboek is specifiek voor elke klant. Het logboek is bijvoorbeeld handig om te bewijzen dat u hebt gecontroleerd dat het huidige btw-nummer juist is. Wanneer u een btw-nummer verifieert, wordt in de kolom **Aanvraag-id** in het logboek aangegeven dat u actie hebt ondernomen.

U kunt het btw-log weergeven op de klanten-, leveranciers- of contactkaarten, op het sneltabblad **Facturering**, door de zoekknop te kiezen in het veld **Btw-nummer**.  

Er zijn een paar dingen waarmee u rekening moet houden met betrekking tot de VIES-service voor btw-nummervalidatie:

* De service gebruikt het http-protocol, wat betekent dat gegevens die door de server worden overgebracht, niet zijn versleuteld.  
* Deze service wordt mogelijk onderbroken. Hiervoor is Microsoft niet verantwoordelijk. De service maakt deel uit van een breed EU-netwerk van nationale btw-journalen.

> [!IMPORTANT]
> Het is uw verantwoordelijkheid om te controleren of de gegevens kloppen. Soms worden gegevens met fouten geretourneerd door de VIES-service voor btw-nummervalidatie. Als de validatie mislukt, valideert u de btw-registratienummers op de [website](https://ec.europa.eu/taxation_customs/vies/), drukt u het resultaat af of slaat u het op een gedeelde locatie op, en voegt u vervolgens de koppeling toe aan de record voor uw klant, leverancier of contactpersoon. Zie voor meer informatie [Bijlagen, koppelingen en notities op kaarten en in documenten beheren](ui-how-add-link-to-record.md).

## <a name="validation-templates"></a>Validatiesjablonen

U kunt de VIES-service gebruiken om ook andere bedrijfsinformatie, zoals het adres en het btw-nummer, te controleren. Maak op de pagina **Validatiesjablonen voor btw-nummers** een vermelding voor elk land/regio waarvoor u verdere validatie wilt krijgen, en specificeer vervolgens de informatie die u automatisch wilt laten valideren.  

Voeg bijvoorbeeld een vermelding toe voor Spanje waar u validatie wilt krijgen voor naam, straat, stad en postcode, en vervolgens een vermelding voor Duitsland waar u bijvoorbeeld alleen validatie voor postcode wilt. Geef vervolgens op de pagina **Instelling van validatieservice van EU-btw-nummers** de standaardsjabloon op.  

> [!NOTE]
> Zorg er altijd voor dat de standaardsjabloon werkt voor uw behoeften. U kunt de standaardinstelling aanpassen aan uw vereisten, zoals validatie voor alle velden of geen velden.

De volgende keer dat u een btw-nummer opgeeft, valideert de service het nummer en eventuele aanvullende gegevens zoals bepaald door uw validatiesjablonen. Als de opgegeven waarden verschillen van de waarden die door de service worden geretourneerd, ziet u de details op de pagina **Validatiegegevens**, waar u de waarden kunt accepteren of resetten.  

## <a name="see-also"></a>Zie ook

[Btw instellen](finance-setup-vat.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)  
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Lokale functionaliteit in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
