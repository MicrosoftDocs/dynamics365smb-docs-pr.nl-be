---
title: Werk beheren tussen meerdere bedrijven in de bedrijfshub
description: 'Lees meer over de bedrijfshub in Dynamics 365 Business Central, die u gebruikt om uw werk in meerdere bedrijven te beheren.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Werk beheren tussen meerdere bedrijven in de bedrijfshub

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Sommige mensen werken in meerdere bedrijven in [!INCLUDE [prod_short](includes/prod_short.md)] en sommige werken ook in meer dan één organisatie, zoals externe accountants, of werknemers en managers van bedrijven met meerdere dochterondernemingen. Voor deze gebruikers, en vele anderen, dient de bedrijfshub als een landingspagina die een financieel overzicht geeft voor meerdere bedrijven en omgevingen. Dit is een hulpmiddel voor gebruikers voor het beheren van werk in de verschillende omgevingen waarin ze werken, tussen bedrijven, omgevingen en regio's.  

U krijgt toegang tot de bedrijfshub door over te schakelen naar de rol **Bedrijfshub** in Mijn instellingen of door de pagina **Bedrijfshub** rechtstreeks te openen. U kunt op beide plaatsen hetzelfde werk doen, maar acties worden in menu's iets anders geplaatst.  

[![Toont de bedrijfshubpagina met een lijst van alle bedrijven.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> U kunt de bedrijfshub met zoveel bedrijven verbinden als u nodig heeft. U kunt de bedrijfshub echter alleen verbinden met bedrijven die worden gehost in [!INCLUDE [prod_short](includes/prod_short.md)] online.

## Startpagina van de bedrijfshub

Als u de rol **Bedrijfshub** gebruikt, toont uw startpagina een lijst met bedrijven waartoe u toegang hebt, inclusief informatie over KPI's en koppelingen om elk bedrijf te openen. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Kies de actie **Bedrijfshub** om de bedrijfshub te openen, waar u nauwer kunt samenwerken met elk bedrijf.  

> [!TIP]
> Om toegang te krijgen tot een specifiek bedrijf in [!INCLUDE [prod_short](includes/prod_short.md)] kiest u de naam van het bedrijf of kiest u het menu-item **Ga naar bedrijf**. U wordt automatisch aangemeld op een nieuw browsertabblad.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Acties voor een bedrijf dat wordt vermeld in de bedrijfshub":::

U kunt nieuwe bedrijven toevoegen, bijvoorbeeld wanneer u een nieuwe klant krijgt of wanneer uw bedrijf een nieuwe dochteronderneming toevoegt. Zie voor meer informatie [Bedrijven toevoegen aan uw bedrijfshub](company-hub-add-company.md).  

> [!TIP]
> Om de gegevens in de bedrijfshub te vernieuwen moet u toegang hebben tot de gegevens in de bedrijven waar de gegevens vandaan komen.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## Toegewezen taken

In [!INCLUDE [prod_short](includes/prod_short.md)] kunt u taken toewijzen aan uzelf en anderen, en anderen kunnen taken aan u toewijzen. De bedrijfshub biedt u een overzicht van toegewezen taken voor elk bedrijf en u kunt een lijst met alle toegewezen taken openen door **Mijn gebruikerstaken** op de **Startpagina** te kiezen.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### Mijn gebruikerstaken

Met de lijst **Mijn gebruikerstaken** kunt u de prioriteiten voor uw dag bepalen door meer informatie over aan u toegewezen taken in al uw bedrijven weer te geven.  

U kunt bijvoorbeeld sorteren op vervaldatum of een ander gegevenstype op basis waarvan u uw dag kunt indelen op prioriteiten. Standaard worden in de lijst alle taken weergegeven die aan u zijn toegewezen, maar u kunt filters instellen, bijvoorbeeld om alleen taken weer te geven die als hoge prioriteit zijn gemarkeerd.  

Als u aan een taak wilt beginnen, kiest u deze in het overzicht met wachtende gebruikerstaken. Op het lint wordt met **Ga naar taakitem** de pagina geopend waarin u het werk kunt uitvoeren.  

Wanneer u een taak hebt voltooid, moet u deze als voltooid markeren.  

Zie voor meer informatie over bedrijven en omgevingen [Omgevingskoppelingen](company-hub-add-company.md#environment-links).  

## Toegang tot de bedrijfshub

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Om toegang te krijgen tot de bedrijfshub moet u toegang hebben via de gebruikersgroep *D365 BEDRIJFSHUB* of via de machtigingenset *D365 BEDRIJFSHUB*. U moet ook toegang hebben tot de bedrijven die in uw bedrijfshub worden vermeld, wat betekent dat u een gebruiker in die bedrijven moet zijn. Zie [Gebruikers maken volgens licenties](ui-how-users-permissions.md) voor meer informatie.  

> [!IMPORTANT]
> De bedrijfshub is een bedrijvenlijst, zodat elke gebruiker die toegang heeft tot de bedrijfshub, alle bedrijven in de eigen [!INCLUDE [prod_short](includes/prod_short.md)]-tenant kan zien en alle KPI's voor de bedrijven waartoe ze toegang hebben.

Als u de bedrijfshub niet kunt vinden en u weet dat u er toegang toe hebt gekregen, neem dan contact op met uw beheerder als de bedrijfshub wordt vermeld op de pagina **Extensiebeheer**. Zie [Business Central aanpassen met extensies](ui-extensions.md) voor meer informatie.  

## De bedrijfshub instellen

Om de bedrijfshub te gaan gebruiken moet u een of meer bedrijven aan uw dashboard toevoegen. Zie voor meer informatie [Bedrijven toevoegen aan uw bedrijfshub](company-hub-add-company.md).  

Maar om een bedrijf toe te voegen moet u toegang hebben gekregen tot een of meer exemplaren van [!INCLUDE [prod_short](includes/prod_short.md)], naast het bedrijf waarin u de bedrijfshub gebruikt.  

Als u bijvoorbeeld accountant bent, kunnen uw klanten u uitnodigen voor hun [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Uw externe accountant uitnodigen voor uw Business Central](finance-accounting.md#inviteaccountant).  

Beheerders kunnen dezelfde begeleide instelling gebruiken om u toe te voegen aan hun [!INCLUDE [prod_short](includes/prod_short.md)] of ze kunnen u toevoegen aan het relevante Microsoft Entra-account in het Microsoft 365-beheercentrum. Zie [Gebruikers en groepen beheren](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true) voor meer informatie.  

## Zie ook

[Bedrijven toevoegen aan uw bedrijfshub](company-hub-add-company.md)  
[Accountantervaringen in Business Central](finance-accounting.md)  
[De extensie Bedrijfshub voor Business Central](ui-extensions-company-hub.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]