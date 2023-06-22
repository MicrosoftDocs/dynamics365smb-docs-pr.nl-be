---
title: Overzicht van printerinstelling en -beheer
description: Ontdek wat de verschillende printermogelijkheden zijn in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview" />Overzicht van printerinstelling en -beheer

Documenten en rapporten afdrukken vanuit [!INCLUDE[prod_short](includes/prod_short.md)] is een belangrijke taak voor zakelijke gebruikers. U wilt afdruktaken meestal rechtstreeks naar een van de printers van uw organisatie sturen&mdash;ongeacht welke [!INCLUDE[prod_short](includes/prod_short.md)]-client of -app u gebruikt. Omdat [!INCLUDE[prod_short](includes/prod_short.md)] online een cloudservice is, kan het lokale printers die zijn aangesloten op de apparaten van gebruikers niet rechtstreeks bereiken, maar het kan wel verbinding maken met cloud-compatibele printers.

## <a name="what-are-your-printer-possibilities-in-business-central" />Wat zijn uw printermogelijkheden in Business Central?

Om uw printbehoeften te ondersteunen, biedt [!INCLUDE[prod_short](includes/prod_short.md)] de volgende functies:

|Functie|Omschrijving|Webclient| Mobiele app|App voor Teams|
|-------|-----------|----------|-----------|--------------|
|Universeel afdrukken|Universeel afdrukken is een oplossing voor printerbeheer die beschikbaar is als cloudservice van Microsoft. Met deze functie kunt u uw printers instellen in Universeel afdrukken en ze vervolgens registreren voor gebruik in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze functie vereist een Universeel afdrukken-abonnement en de extensie **Integratie met Universeel afdrukken**.|![werkt online.](media/check.png)|![werkt online.](media/check.png)|![werkt online](media/check.png)|
|E-mail afdrukken|Met deze functie kunt u printers met e-mail instellen. [!INCLUDE[prod_short](includes/prod_short.md)] stuurt vervolgens afdruktaken naar een printer met behulp van het e-mailadres van de printer. Voor deze functie zijn printers met e-mailfunctie vereist en de extensie **Verzenden naar e-mailprinter**.|![werkt online.](media/check.png)|![werkt online](media/check.png)|![werkt online](media/check.png)|
|Afdrukken met browser|Afdruktaken worden afgehandeld door de afdrukfunctionaliteit van de browser van de gebruiker. Als geen cloudprinter is geïnstalleerd en ingesteld of als een geïnstalleerde printer niet werkt, wordt het afdrukken standaard ingesteld op de afdrukopties voor de browser. Het veld **Printer** op de rapportverzoekpagina bevat *(Door de browser afgehandeld)*.|![werkt online](media/check.png)|||

Het meeste werk voor het instellen van printers kan worden gedaan vanaf de pagina **Printerbeheer** in [!INCLUDE[prod_short](includes/prod_short.md)]. Hoewel u met Universeel afdrukken-printers mogelijk ook in het Microsoft 365-beheercentrum of de Azure Portal moet werken.

> [!IMPORTANT]
> Voor Business Central on-premises vereisen Universeel afdrukken en E-mail afdrukken dat Azure Active Directory- (AD)- of NavUserPassword-authenticatie wordt gebruikt.

## <a name="custom-printer-extensions" />Aangepaste printerextensies

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt ook andere aangepaste printerextensies die nog meer afdrukfuncties toevoegen. Dus als u aangepaste printerextensies hebt geïnstalleerd, bevat uw toepassing mogelijk afdrukfuncties die niet in dit artikel worden beschreven.

Als u een AL-ontwikkelaar bent en wilt leren hoe u printerextensies maakt, gaat u naar [Printerextensies ontwikkelen in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps" />Volgende stappen

- [Printers voor Universeel afdrukken instellen](admin-printer-setup-universal-print.md)  
- [E-mailprinters instellen](admin-printer-setup-email.md)  
- [Standaardprinters instellen](ui-specify-printer-selection-reports.md)
