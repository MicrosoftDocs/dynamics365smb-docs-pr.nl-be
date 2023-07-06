---
title: Werken met periodieke inkomsten
description: Meer informatie over de beschikbare opties om te automatiseren hoe u abonnementsfacturen naar uw klanten verzendt en periodieke inkomsten registreert.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
---
# <a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a>Werken met periodieke inkomsten in [!INCLUDE[prod_short](includes/prod_short.md)]

Veel bedrijven gaan over van een bedrijfsinkomstenmodel waarbij inkomsten worden gegenereerd uit de eenmalige aankoop van een klant naar een abonnementsmodel waarbij inkomsten worden verdiend op een periodieke basis, in ruil voor consistente toegang tot de levering van een goed of dienst.
[!INCLUDE[prod_short](includes/prod_short.md)] heeft de volgende opties om te automatiseren hoe u abonnementsfacturen naar uw klanten verzendt en periodieke inkomsten registreert. 

## <a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a>Inkomsten registreren met een periodiek dagboek

Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u regelmatig boekt met weinig of geen wijzigingen, zoals huur, abonnementen, elektriciteit of verwarming. Met de speciale velden voor periodieke transacties kunt u zowel vaste als variabele bedragen boeken. Als u een periodiek dagboek gebruikt, hoeft u de gegevens slechts éénmaal in te voeren. De ingevulde gegevens, zoals rekeningen, dimensies en dimensiewaarden, worden na het boeken in het dagboek bewaard. Later kunt u eventueel wijzigingen aanbrengen en de informatie opnieuw boeken.

### <a name="why-use-this-option"></a><a name="why-use-this-option"></a><a name="why-use-this-option"></a>Waarom deze optie gebruiken?

Met deze optie definieert u flexibele factureringsperioden met [datumformules](ui-enter-date-ranges.md#use-date-formulas).

Met deze optie kunt u echter geen facturen afdrukken en verzenden in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)].  

Zie [Werken met periodieke dagboeken](ui-work-general-journals.md#work-with-recurring-journals) voor meer informatie.  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Meerdere facturen maken op basis van een periodiek taakdagboek

Het periodieke taakdagboek is een geavanceerder alternatief voor het dagboek. U definieert artikelen, resources en grootboekrekeningen, die voor elke taak moeten worden herhaald, en u specificeert de frequentie van herhaling.  

Na het plaatsen van een periodiek taakdagboek, kunt u meerdere facturen maken met de taak **Projectverkoopfactuur maken**. U kunt gemaakte facturen bekijken en boeken op de pagina **Verkoopfacturen**.

### <a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a>Waarom deze optie gebruiken?

Met deze optie volgt u de standaardfactureringsprocedure met alle voordelen daarvan, inclusief standaard- en klantlay-outs voor communicatievoorkeuren. U kunt ook prijzen voor elke taak afzonderlijk definiëren.

Voor elke nieuwe klant moet u echter een nieuwe taak maken en regels toevoegen aan het periodieke dagboek. 

Zie voor meer informatie [Projectdagboekregels maken](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) en [Meerdere projectverkoopfacturen maken](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Meerdere facturen maken op basis van periodieke verkoopregels

Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u periodieke verkoopregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders. Gebruik de batchverwerking **Periodieke verkoopfacturen maken** om verkoopfacturen te maken volgens de periodieke verkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u op de periodieke verkoopregels opgeeft.  

### <a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a>Waarom deze optie gebruiken?

Met deze optie kunt u dezelfde terugkerende regels aan meerdere klanten toewijzen. U kunt een geldigheidsperiode definiëren voor de periodieke verkoopregels voor een specifieke klant. U kunt meerdere periodieke regels aan dezelfde klant toewijzen en ze worden allemaal op de factuur vermeld.

Er is echter geen manier om vaste prijzen voor artikelen in te stellen, omdat [!INCLUDE[prod_short](includes/prod_short.md)] de werkelijke prijzen en kortingen zal gebruiken die geldig zijn op documentdatum, in een poging de beste combinatie te vinden die de laagste prijs oplevert.  

Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a>Periodieke facturen met servicecontract maken

Een servicecontract bevat de servicecontractovereenkomsten tussen uw klanten en uw bedrijf. Een servicecontract omvat afspraken over het serviceniveau en de serviceartikelen die onder het contract vallen.  

U kunt de begindatum van het contract definiëren en de factuurperiode, of het contract al dan niet vooruitbetaald is, specificaties voor prijsupdates, als u van plan bent de prijzen te wijzigen terwijl het contract actief is. U kunt zowel serviceartikelen als artikelen op servicecontractregels gebruiken.
U kunt contractsjablonen maken om te definiëren hoe bepaalde soorten contracten worden gemaakt.  

### <a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a>Waarom deze optie gebruiken?

Met deze optie gebruikt u een deel van de geavanceerde servicebeheerfunctionaliteit dat niet beperkt is tot het uitgeven van periodieke facturen, maar ondersteunt u de reparatiewerkplaats en servicewerkzaamheden.

Voor deze optie is echter de Premium-licentie vereist. Servicebeheer instellen en onderhouden biedt mogelijk geen enorme voordelen in eenvoudiger abonnementsscenario's.  

Zie voor meer informatie [Werken met servicecontracten en offertes voor servicecontracten](service-how-to-create-service-contracts-and-service-contract-quotes.md) en [Meerdere servicecontracten factureren](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a><a name="related-features"></a><a name="related-features"></a>Gerelateerde functies
Er zijn verschillende gerelateerde mogelijkheden in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a>Verkoopraamcontracten

Een verkoopraamcontract biedt een kader voor een langdurige overeenkomst tussen uw bedrijf en uw klant.
Een raamcontract wordt meestal gemaakt als uw klant ermee heeft ingestemd grote hoeveelheden aan te kopen die in meerdere kleinere zendingen moeten worden geleverd gedurende een bepaalde periode. Inkoopraamcontracten hebben vaak betrekking op slechts één artikel met vooraf vastgestelde leverdatums. De belangrijkste reden voor het gebruik van een raamcontract in plaats van een verkooporder is dat de ingevoerde hoeveelheden op een raamcontract niet van invloed zijn op de artikelbeschikbaarheid, maar echter wel gebruikt kunnen worden voor planningsdoeleinden.

#### <a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a>Waarom deze optie gebruiken?

Met deze optie gebruikt u de verwachte vraag, zodat de informatie wordt overwogen tijdens de normale planningsroutines. Zie voor meer informatie [Vraagprognoses en raamcontracten](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

De standaardversie biedt echter geen kant-en-klare mogelijkheid om meerdere raamcontracten in bulk te verwerken.

Zie [Werken met verkoopraamcontracten](sales-how-to-create-blanket-sales-orders.md) voor meer informatie.

### <a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a>Periodieke orders (Noorwegen)

U kunt periodieke orders gebruiken om raamcontractsjablonen te maken, zodat verkooporders kunnen worden gemaakt op basis van door u gedefinieerde datumintervallen. Als u bijvoorbeeld elke twee weken dezelfde verkooporder levert, kunt u een algemene verkooporder gebruiken en periodieke orders maken.
U kunt periodieke groepen gebruiken om een reeks parameters te definiëren die laten zien hoe u de orders plaatst. Deze groepen zijn toegewezen aan raamcontracten die regelmatig moeten worden gemaakt. Om de periodieke orders te maken moet u periodiek het proces voor het maken van periodieke orders uitvoeren. 

#### <a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a>Waarom deze optie gebruiken?

Met deze optie kunt u kiezen tussen vaste en "beste" prijzen.

Deze optie is echter alleen beschikbaar in Noorwegen. De geldigheidsperiode kan worden gedefinieerd op het periodieke groepsniveau.

Zie [Periodieke orders](LocalFunctionality/Norway/recurring-orders.md) voor meer informatie.

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Periodieke inkomsten en abonnementsfacturering door andere providers

Op [AppSource.microsoft.com](https://appsource.microsoft.com/) kunt u extensies krijgen voor Business Central. Sommige extensies worden verstrekt door Microsoft en andere extensies worden verstrekt door andere bedrijven. Het overzicht van de extensies door andere bedrijven groeit elke maand. Houd [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) dus in de gaten en krijg apps om u te helpen met uw werk in Business Central.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Datumformules](ui-enter-date-ranges.md#use-date-formulas)  
[Werken met periodieke dagboeken](ui-work-general-journals.md#work-with-recurring-journals)  
[Projectdagboekregels maken](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Meerdere projectverkoopfacturen maken](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md)  
[Werken met servicecontracten en servicecontractoffertes](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Meerdere servicecontracten factureren](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Vraagprognoses en raamcontracten](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Werken met verkoopraamcontracten](sales-how-to-create-blanket-sales-orders.md)  
[Periodieke orders (Noorwegen)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
