---
title: 'Procedure: Berichtsjablonen beheren | Microsoft Docs'
description: "Berichten worden verzonden naar werkstroomgebruikers om ze te informeren over stappen die ze moeten zetten, of om ze te informeren over de status van werkstroomstappen. U stelt in wie berichten ontvangt en wanneer door goedkeuringsgebruikers, een planning van gebruikersberichten en de betrokken werkstroomantwoorden in te stellen om de ontvanger van het bericht te definiëren. Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 31a6cd72e7e7c3fda27803a995b7282c8a2c3751
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="manage-notification-templates"></a>Berichtsjablonen beheren
Berichten worden verzonden naar werkstroomgebruikers om ze te informeren over stappen die ze moeten zetten of om ze te informeren over de status van werkstroomstappen. U stelt in wie berichten ontvangt en wanneer door goedkeuringsgebruikers, een planning van gebruikersberichten en de betrokken werkstroomantwoorden in te stellen om de ontvanger van het bericht te definiëren. Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).  

 Berichten zijn gebaseerd op sjablonen waarin de lay-out en inhoud van het bericht zijn vastgelegd. U kunt de inhoud van een berichtsjabloon exporteren, bewerken en vervolgens de inhoud importeren in dezelfde of een nieuwe berichtsjabloon. Dit wordt in de volgende procedures beschreven.  

 De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt geleverd met drie berichtsjablonen: een voor informeren over goedkeuringsverzoeken, een voor informeren over nieuwe records en een voor informeren over vervallen goedkeuringsaanvragen. De drie vooraf gedefinieerde berichtsjablonen ondersteunen **E-mail** en **Opmerking** als berichtmethode. Voor informatie over het weergeven van de inhoud van de drie berichtsjablonen raadpleegt u het onderdeel "Inhoud van de berichtsjablonen" in dit onderwerp.

## <a name="to-create-a-new-notification-template"></a>Een nieuwe berichtsjabloon maken  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Berichtjablonen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in het venster **Berichtsjablonen** de actie **Nieuw** .  
3.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Identificeer de berichtsjabloon.|  
    |**Beschrijving**|Beschrijf de berichtsjabloon.|  
    |**Berichtmethode**|Geef aan of het bericht wordt verzonden als e-mail of als opmerking.|  
    |**Soort**|Geef het bedrijfsproces aan waarvoor het bericht wordt gebruikt.<br /><br /> Selecteer een van de volgende typen:<br /><br /> -   **Goedkeuring** geeft aan dat de sjabloon wordt gebruikt om gebruikers te informeren in goedkeuringswerkstromen.<br />-   **Nieuwe record** geeft aan dat de sjabloon wordt gebruikt om fiatteurs te melden dat een nieuwe record, zoals een klantenkaart, hun goedkeuring nodig heeft.<br />-   **Vervallen** geeft aan dat de sjabloon wordt gebruikt om gebruikers te melden dat goedkeuringsaanvragen vervallen zijn.|  
    |**Standaard**|Geef aan of de berichtsjabloon standaard wordt gebruikt.|  

## <a name="to-modify-a-notification-template"></a>Een berichtsjabloon wijzigen  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Berichtjablonen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het venster **Berichtsjablonen** de berichtsjabloon die u wilt wijzigen.  
3.  Kies de actie **Sjablooninhoud exporteren**.  
4.  Klik in het venster **Bestand exporteren** op de knop **Opslaan**, voer de bestandsnaam in en sla het HTML-bestand in een geschikte locatie op.  
5.  Klik met de rechtermuisknop op het bestand, kies **Openen met** en kies vervolgens het desbetreffende programma.  

    > [!NOTE]  
    >  Inhoud voor berichtsjablonen van het type E-mail is in HTML-indeling. Inhoud voor berichtsjablonen van het type Opmerking is in TXT-indeling.  
6.  Bewerk de inhoud van de berichtsjabloon door parametervariabelen toe te voegen, te wijzigen of te verwijderen om de gewenste berichtinhoud te definiëren. Zie voor meer informatie het onderdeel "Inhoud van de berichtsjablonen".  

    Importeer vervolgens de aangepaste inhoud terug in dezelfde of een nieuwe berichtsjabloon.  
7.  Om de berichtsjabloon te wijzigen die u hebt geëxporteerd, selecteert u in het venster **Berichtsjablonen** de sjabloon die u in stap 2 hebt geselecteerd.  

    U kunt ook de gewijzigde sjablooninhoud in een nieuwe berichtsjabloon importeren. Hiervoor voert u de procedure "Een nieuwe berichtsjabloon maken" uit en selecteert u vervolgens de nieuwe berichtsjabloon.  
8.  Kies de actie **Sjablooninhoud importeren**.  
9. Als u een bestaande berichtsjabloon wijzigt, kiest u de knop **Ja** in het bericht over het overschrijven van de bestaande sjabloon.  
10. Kies in het venster **Selecteer een bestand om te importeren** het HTML-bestand dat u in stap 6 hebt gewijzigd, en kies vervolgens de knop **Openen**.  

De nieuwe of bestaande berichtsjabloon in het venster **Berichtsjablonen** wordt nu bijgewerkt met de gewijzigde inhoud.  

### <a name="content-of-the-notification-templates"></a>Inhoud van de berichtsjablonen  
De drie soorten berichtsjablonen, **Nieuwe Record**, **Goedkeuring** en **Vervallen**, hebben verschillende inhoud.  

Parameterwaarden worden automatisch in berichten ingevoegd op basis van het soort berichtsjabloon.  

#### <a name="new-record"></a>Nieuwe record  
 ![NAV&#95;bericht&#95;sjabloon&#95;nieuw&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_bericht_sjabloon_nieuwe_record")  

#### <a name="approval"></a>Goedkeuring  
 ![NAV&#95;bericht&#95;sjabloon&#95;goedkeuring&#95;type](media/nav_notification_template_approval_type.png "NAV_bericht_sjabloon_goedkeuring_type")  

#### <a name="overdue"></a>Achterstallig  
 ![NAV&#95;bericht&#95;achterstallig&#95;type](media/nav_notification_overdue_type.png "NAV_bericht_achterstallig_type")  

## <a name="see-also"></a>Zie ook  
 [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)   
 [E-mail instellen](admin-how-setup-email.md)   
 [Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)   
 [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)   
 [Werkstromen maken](across-how-to-create-workflows.md)   
 [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md)   
 [Werkstroom](across-workflow.md)   

