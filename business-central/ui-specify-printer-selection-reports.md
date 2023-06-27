---
title: Een standaardprinter opgeven
description: Meer informatie over verschillende manieren om printers in te stellen die standaard worden gebruikt voor afdruktaken.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer" /><a name="default"></a>Een standaardprinter opgeven

Nadat printers zijn ingesteld in Business Central, kunt u aangeven welke printer u standaard wilt gebruiken. Er is een aantal manieren om printers op te geven die standaard worden gebruikt voor rapporten en andere afdruktaken. Een standaardprinter is handig als u met verschillende rapporten werkt waarvoor verschillende printers nodig zijn vanwege hun plaatsing in het bedrijf of hun uitvoermogelijkheden.

> [!IMPORTANT]
> De enige printers die u als standaard kunt specificeren zijn **Microsoft Print to PDF** en cloudprinters die al zijn ingesteld voor gebruik in Business Central, zoals e-mailprinters en Universeel afdrukken-printers. Cloudprinters worden meestal ingesteld door een beheerder. Zie [Printer instellen en beheren](admin-printer-setup-overview.md) voor meer informatie.   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs" />Een printer instellen als standaardprinter voor alle afdruktaken

Op de pagina **Printerbeheer** kunt u een printer instellen als standaardprinter voor alle afdruktaken. U kunt de printer als standaard instellen, alleen voor u of voor alle gebruikers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerbeheer** in en selecteer vervolgens de gerelateerde koppeling.

    > [!TIP]
    > U kunt de pagina **Printerbeheer** ook openen vanuit de pagina **Printerselecties** door **Printerbeheer** te kiezen.  
2. Selecteer op de pagina **Printerbeheer** een printer in de lijst en kies **Beheren**. Kies vervolgens **Instellen als mijn standaardprinter** of **Instellen als standaardprinter voor alle gebruikers**.

> [!NOTE]
> Als u een standaardprinter instelt vanuit het **Printerbeheer**, wordt een vermelding toegevoegd aan de **printerselecties**.

## <a name="set-a-default-printer-for-specific-reports" />Een standaardprinter instellen voor specifieke rapporten

Op de pagina **Printerselecties** kunt u de printer opgeven die een rapport standaard zal gebruiken. Standaardprinters worden ingesteld per gebruikersaccount. U kunt een standaardprinter instellen voor alleen uzelf, een andere gebruiker of alle gebruikers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Printerselecties** in en selecteer vervolgens de gerelateerde koppeling. Als alternatief selecteert u een printer op de pagina **Printerbeheer** en kiest u vervolgens de actie **Printerselecties**.
2. Kies de actie **Nieuw** om een printerselectie toe te voegen voor een specifiek rapport.
3. Vul de vereiste velden in.

Het opgegeven rapport is nu ingesteld om standaard te worden afgedrukt op de geselecteerde printer.

> [!NOTE]
> Wanneer u het betreffende rapport afdrukt, kunt u een andere printer selecteren met het veld **Afdrukken** op de rapportaanvraagpagina.

> [!NOTE]
> Als u geen rapport instelt voor een specifieke printer op de pagina **Printerselecties**, wordt het afgedrukt op de standaardprinter van het bedrijf, zoals gedefinieerd op de pagina **Printerbeheer**.

U of de beheerder kan ook de pagina **Printerselecties** gebruiken om andere afdrukvarianten voor gebruikers en rapporten te definiëren. De volgende tabel beschrijft de combinatie van waarden wanneer u andere printerinstellingen instelt voor een rapport.

|Tot                                                 |Stel de volgende waarden in                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Een rapport afdrukken naar een specifieke printer voor alle gebruikers |Geef waarden op in de velden **Rapport-id** en **Printernaam** en laat het veld **Gebruikers-ID** leeg.|
|Alle rapporten naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden op in de velden **Gebruikers-ID** en **Printernaam** en laat het veld **Rapport-id** leeg. Deze vermelding doet hetzelfde als de actie **Instellen als mijn standaardprinter** op de pagina **Afdrukbeheer**.|
|De standaardprinter voor alle gebruikers instellen|Geef een waarde op in het veld **Printernaam** en laat de velden **Gebruikers-ID** en **Rapport-id** leeg. Deze vermelding doet hetzelfde als de actie **Als standaardprinter voor alle gebruikers instellen** op de pagina **Afdrukbeheer**.|
|Een specifiek rapport afdrukken naar de standaardprinter van de gebruiker|Geef een waarde op in het veld **Rapport-id** en laat de velden **Printernaam** en **Gebruikers-ID** leeg.|
|Een specifiek rapport naar een specifieke printer afdrukken voor een specifieke gebruiker|Geef waarden in alle drie de velden op.|

> [!NOTE]
> Specifiekere printerselecties hebben voorrang op algemenere printerselecties. Bijvoorbeeld een printerselectie met waarden in de velden **Gebruikers-ID**, **Rapport-id** en **Printernaam** heeft voorrang op een printerselectie met lege vermeldingen in de velden **Gebruikers-ID** of **Rapport-id**.

## <a name="choosing-the-printer-when-running-a-report" />De printer kiezen bij het uitvoeren van een rapport

In plaats van de standaardprinter te gebruiken bij het uitvoeren van een rapport, kunt u deze instelling overschrijven vanaf de aanvraagpagina. Kies eenvoudig welke printer u wilt gebruiken voor het genereren van dit rapport in het vervolgkeuzemenu **Printer**.

## <a name="sizing-print-jobs" />Formaat van afdruktaken wijzigen

Cloudafdrukken zijn ontworpen voor documenten van een redelijk formaat. De meeste cloudservices, inclusief PrintNode en HP ePrint, hebben een limiet van 10 MB per taak. Als u grotere rapporten wilt afdrukken, moet u deze mogelijk in meerdere afdrukken splitsen.

[Microsoft-training](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Printerbeheer](admin-printer-setup-overview.md)  
[Printers voor Universeel afdrukken instellen](admin-printer-setup-universal-print.md)  
[E-mailprinters instellen](admin-printer-setup-email.md)  
[Een rapport afdrukken](ui-work-report.md#PrintReport)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Batchverwerkingen uitvoeren](ui-how-run-batch-jobs.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
