---
title: Koppelen en synchroniseren (bevat video)
description: 'Als een integratietabeltoewijzing wordt gesynchroniseerd, kunnen gegevens in alle records in een tabel in Business Central en Dynamics 365 Sales worden gesynchroniseerd die zijn gekoppeld.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
ms.service: dynamics-365-business-central
---

# Records koppelen en synchroniseren tussen Dataverse en Business Central

In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[prod_short](includes/prod_short.md)] koppelt aan records in Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)]. Door records te koppelen kunt u Dataverse-informatie vanuit [!INCLUDE[prod_short](includes/prod_short.md)]bekijken en andersom. Door de koppeling kunt u ook gegevens synchroniseren tussen de records. U kunt bestaande records koppelen of nieuwe records maken en koppelen.

> [!NOTE]
> Gegevens koppelen en synchroniseren is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt. Een snelle manier om dat te controleren is de **Klant**-kaart te openen en de actie **Koppeling instellen** te zoeken. Als de actie beschikbaar is, zijn de apps verbonden.

## Videovoorbeeld

Deze video toont het koppelen en synchroniseren van gegevens in het kader van een integratie met [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Een record koppelen  

1. In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  

    U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.  

2. Kies de actie **Koppeling instellen**.  
3. Vul de velden in en kies de knop **OK**.  

## Eén record synchroniseren  

1. In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  
2. Kies de actie **Nu synchroniseren**.  
3. Als een record in één richting kan worden gesynchroniseerd, selecteert u de optie die de richting van de gegevensupdate opgeeft, en kiest u vervolgens **OK**.  

## Eén record synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)]  

1. In [!INCLUDE[crm_md](includes/crm_md.md)] opent u het formulier voor de record die u wilt koppelen. Bijvoorbeeld het formulier Accountkaart of Contactkaart.  
2. Kies de actie **[!INCLUDE[prod_short](includes/prod_short.md)]** op het lint om een record automatisch te openen en te koppelen.

    > [!Note]
    > U kunt één record alleen automatisch synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)] wanneer **Alleen gekoppelde records synchr**. is uitgeschakeld en de synchronisatierichting is ingesteld op **Bidirectioneel** of **Van integratietabel** op de pagina **Toewijzing van integratietabel** voor de record. Zie voor meer informatie [De tabellen en velden toewijzen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## Meerdere records koppelen met behulp van op overeenkomsten gebaseerde koppeling

Specificeer de gegevens die moeten worden gesynchroniseerd voor een entiteit, zoals een klant of contactpersoon, door records te koppelen op basis van overeenkomsten. Verfijn de overeenkomsten door de zoekopdracht hoofdlettergevoelig te maken en een prioriteit toe te kennen aan elke overeenkomst. Als er geen overeenkomst wordt gevonden, kunt u ook aangeven dat u de entiteit wilt maken in Dataverse. Ga voor meer informatie naar [De koppeling op basis van overeenkomsten aanpassen](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Het koppelingsproces op basis van overeenkomsten slaat records over die al zijn gekoppeld. Om die records op te nemen wanneer u koppeling op basis van overeenkomsten uitvoert, ontkoppelt u de records en probeert u het opnieuw. Ga voor meer informatie over het ontkoppelen van records naar [Records ontkoppelen](#uncoupling-records).

1. Open in [!INCLUDE[prod_short](includes/prod_short.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.
2. Kies de actie **Op overeenkomsten gebaseerde koppeling**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Meerdere records synchroniseren  

1. Open in [!INCLUDE[prod_short](includes/prod_short.md)] de lijstpagina voor de record, zoals de lijstpagina Klanten of Contacten.  
2. Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren**.  
3. Als records in één richting kunnen worden gesynchroniseerd, selecteert u de optie die de richting opgeeft, en kiest u vervolgens **OK**.  

## Records bulk-invoegen en koppelen

Als u een groot aantal Dataverse-entiteiten hebt die overeenkomen met records in [!INCLUDE [prod_short](includes/prod_short.md)], kunt u ze in bulk invoegen en koppelen. U kunt bijvoorbeeld records bulksgewijs invoegen en koppelen wanneer u voor het eerst synchronisatie instelt.

U gebruikt de **wizard Gegevens importeren** in het **Microsoft Power Platform-beheercentrum**.

In het volgende voorbeeld wordt beschreven hoe u klanten met accounts in bulk invoegt en koppelt in Dataverse. Gebruik hetzelfde proces voor andere typen entiteiten, zoals leveranciers, artikelen en resources.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Openen in Excel** om klantgegevens in Excel te openen. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Als u gegevens wilt toewijzen en importeren in de entiteit **Account** in Dataverse, volgt u de stappen die worden beschreven in [Gegevens (alle recordtypen) importeren uit meerdere bronnen](/power-platform/admin/import-data-all-record-types).  

    Als de accountentiteit een kolom **bcbi_companyid** heeft, moet u er bij het toewijzen van de gegevenskolommen voor zorgen dat de import de juiste bedrijfs-id in de kolom toewijst voor elke geïmporteerde record. Volg deze stappen om de bedrijfs-id te vinden in [!INCLUDE [prod_short](includes/prod_short.md)]:

    1. Open de pagina **Toewijzingen van integratietabellen**.
    2. Kies de toewijzing **KLANT** en kies vervolgens **Lijst bewerken**.
    3. Schuif naar rechts en kies de knop AssistEdit :::image type="icon" source="media/assist-edit-icon.png" border="false"::: in het veld **Filter integratietabel**. Dit toont het standaardfilter voor klanttoewijzing en bevat de bedrijfs-id. De bedrijfs-id is het eerste deel van de waarde. Kopieer alleen dat deel en negeer de nullen. In het volgende voorbeeld wordt het gedeelte gemarkeerd dat moet worden gekopieerd.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Toont het gedeelte van de bedrijfs-id dat moet worden gekopieerd.":::

    > [!NOTE]
    > Niet alle namen van Dataverse-entiteiten en Business Central-records komen overeen. Controleer na het importeren of de volgende kolommen de volgende waarden hebben, afhankelijk van wat u importeert:
    >
    >* Voor klanten moet de kolom **CustomerTypeCode** **Klant** bevatten.
    >* Voor leveranciers moet de kolom **CustomerTypeCode** **Leveranciers** bevatten. 
    >* Voor artikelen moet de kolom **ProductTypeCode** **Verkoopvoorraad** bevatten.
    >* Voor resources moet de kolom **ProductTypeCode** **Service** bevatten.
 
4. Nadat u gegevens in de Dataverse-omgeving hebt geïmporteerd, volgt u in [!INCLUDE [prod_short](includes/prod_short.md)] de stappen om [meerdere records te koppelen met op overeenkomsten gebaseerde koppeling](#to-couple-multiple-records-using-match-based-coupling) om de Dataverse-entiteiten te koppelen met [!INCLUDE [prod_short](includes/prod_short.md)]-records. 

## Records ontkoppelen

U kunt een of meer records loskoppelen van lijstpagina's of de pagina **Fouten met gekoppelde gegevenssynchronisatie** door een of meer regels te kiezen en **Koppeling verwijderen** te kiezen. U kunt ook alle koppelingen verwijderen voor een of meer tabeltoewijzingen op de pagina **Integratietabeltoewijzingen**.

## Zie ook  

[Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]