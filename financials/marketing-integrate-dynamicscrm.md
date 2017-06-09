---
title: Uw klantrelaties beheren met Dynamics 365 for Sales vanuit Dynamics 365 for Financials | Microsoft Docs
description: "Als u Dynamics 365 for Sales gebruikt voor contacten met klanten, kunt u Dynamics 365 for Financials gebruiken voor orderverwerking en financiën en profiteren van naadloze integratie in het proces van potentiële klant naar inkomsten."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Uw klantrelaties beheren met Dynamics 365 for Sales vanuit Dynamics 365 for Financials
Als u Dynamics 365 for Sales gebruikt voor contacten met klanten, kunt u [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken voor orderverwerking en financiën en profiteren van naadloze integratie in het proces van potentiële klant naar inkomsten.

Als uw toepassing is ingesteld voor integratie met Dynamics 365 for Sales, hebt u toegang tot gegevens in Sales vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] en in sommige gevallen ook andersom. Dankzij deze integratie kunt u werken met gegevenstypen die voor beide services worden gebruikt, zoals klanten, contacten en verkoopinformatie, deze gegevenstypen synchroniseren en de gegevens in beide locaties up-to-date houden.  

**Opmerking:** In de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt Dynamics 365 for Sales ook wel Dynamics CRM genoemd. Omwille van de overzichtelijkheid wordt in de rest van dit artikel de terminologie aangehouden die wordt gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

De verkoper in Dynamics CRM kan bijvoorbeeld prijslijsten van [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken bij het opstellen van een verkooporder. Als hij het artikel toevoegt aan de verkooporderregel in Dynamics CRM, kan hij ook het voorraadniveau (de beschikbaarheid) van het artikel zien vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]. Deze informatie wordt gepubliceerd als onderdeel van de begeleide instelling **Dynamics CRM-verbinding instellen**.  

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.  

## <a name="setting-up-the-connection"></a>De verbinding instellen
Vanaf de startpagina kunt u de begeleide instelling **Dynamics CRM-verbinding instellen** starten, die u helpt bij het instellen van de verbinding. Als dat is uitgevoerd, hebt u een naadloze koppeling tussen records in Dynamics CRM en records in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

**Opmerking:** Hierna wordt de begeleide instelling toegelicht, maar u kunt dezelfde stappen ook handmatig uitvoeren in het venster **Instellingen CRM-verbinding**.

In de begeleide instelling kunt u kiezen welke gegevens tussen de twee services moeten worden gesynchroniseerd. U kunt ook opgeven dat u uw bestaande Dynamics CRM-oplossing wilt importeren. In dat geval moet u een beheeraccount opgeven.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>De gebruikersaccount voor het importeren van de oplossing instellen
Om een bestaande oplossing in Dynamics CRM te importeren, maakt de begeleide instelling gebruik van een beheeraccount. Deze account moet een geldige gebruiker in Dynamics CRM zijn met de volgende beveiligingsrollen:

* Systeembeheerder  
* Oplossingsaanpasser  

Zie voor meer informatie [Gebruikers maken en beveiligingsrollen voor Microsoft Dynamics 365 (online) toewijzen](https://technet.microsoft.com/library/jj191623.aspx) op techNet en [Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md).  

Deze account wordt alleen gebruikt tijdens het instellen. Nadat de oplossing is geïmporteerd [!INCLUDE[d365fin](includes/d365fin_md.md)], is de account niet meer nodig.

### <a name="setting-up-the-user-account-for-synchronization"></a>De gebruikersaccount instellen voor synchronisatie
De integratie is gebaseerd op een gedeelde gebruikersaccount. In uw Office 365-abonnement moet u een specifieke gebruiker maken die voor synchronisatie tussen de twee services wordt gebruikt. Deze rekening moet al een geldige gebruiker in Dynamics CRM zijn, maar u hoeft geen beveiligingsrollen aan de account toe te wijzen, omdat de begeleide instelling dit voor u doet. U moet deze gebruikersaccount een of meerdere malen opgeven in de begeleide instelling, afhankelijk van hoeveel synchronisatie u wilt inschakelen. Zie voor meer informatie [Gebruikers maken en beveiligingsrollen voor Microsoft Dynamics 365 (online) toewijzen](https://technet.microsoft.com/library/jj191623.aspx) op techNet.

Als u ervoor kiest *artikelbeschikbaarheid* in te schakelen, moet de account van de integratiegebruiker een webservicetoegangssleutel hebben. Deze instelling omvat twee stappen: in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-pagina voor deze gebruikersaccount moet u op de knop **Sleutel van webservice wijzigen** klikken; en in de begeleide instelling voor de CRM-verbinding moet u die gebruiker opgeven als de gebruiker van de OData-webservice.

Als u ervoor kiest *verkooporderintegratie* in te schakelen, moet u een gebruiker opgeven die de synchronisatie verwerkt: de integratiegebruiker of een andere gebruikersaccount.

### <a name="coupling-records"></a>Records koppelen
In de begeleide instelling kunt u kiezen dat tussen de twee services moeten worden gesynchroniseerd. Maar later kunt u ook synchronisatie voor bepaalde soorten gegevens instellen. Dit wordt aangeduid als *koppelen* en in deze sectie vindt u aanbevelingen voor waar u rekening mee moet houden.

Als u bijvoorbeeld Dynamics CRM-accounts wilt zien als klanten in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de twee soorten records koppelen. Het is niet ingewikkeld: open het venster **Klantenoverzicht** in [!INCLUDE[d365fin](includes/d365fin_md.md)] en zoek in het lint de actie om deze gegevens met Dynamics CRM te koppelen. Vervolgens geeft u op welke [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten overeenkomen met welke accounts in Dynamics CRM.

In bepaalde gebieden koppelt de functie waar u gebruik van maakt bepaalde gegevenssets vóór andere gegevenssets, zoals getoond in de volgende lijst:

* Klanten en accounts  
  * Koppel verkopers eerst aan Dynamics CRM-gebruikers  
* Artikelen en resources  
  * Koppel eenheden eerst aan eenhedengroepen in Dynamics CRM  
* Artikelen en resourceprijzen  
  * Koppel klantenprijsgroepen eerst aan Dynamics CRM-prijzen  

**Opmerking:** Als u prijzen in een vreemde valuta gebruikt, moet u ervoor zorgen dat u valuta's koppelt aan transactievaluta in Dynamics CRM.

Verkooporders in Dynamics CRM zijn afhankelijk van aanvullende informatie zoals klanten, eenheden, valuta, klantenprijsgroepen, artikelen en/of resources. Om verkooporders in Dynamics CRM naadloos te laten werken, moet u eerst klanten, eenheden, valuta, klantprijsgroepen, artikelen en/of resources koppelen.

### <a name="synchronizing-records-fully"></a>Records volledig synchroniseren
Aan het eind van de begeleide instelling kunt u de actie **Volledige synchronisatie uitvoeren** kiezen om alle records in [!INCLUDE[d365fin](includes/d365fin_md.md)] te synchroniseren met alle gerelateerde records in de verbonden Dynamics CRM-oplossing. Kies in het venster **Controle van volledige CRM-synchronisatie** de actie **Starten**. De synchronisatie begint dan taken uit te voeren volgens de afhankelijkheden. Valutarecords worden bijvoorbeeld gesynchroniseerd vóór klantenrecords. De volledige synchronisatie kan lange tijd duren en wordt daarom uitgevoerd in de achtergrond, zodat u verder kunt werken in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Als u de voortgang van afzonderlijke taken in een volledige synchronisatie wilt controleren, zoomt u in op een van de velden **Status van taakwachtrijpost**, **Naar projectstatus van integratietabel** of **Van projectstatus van integratietabel** in het venster **Controle van volledige CRM-synchronisatie** in.

Vanuit het venster **Instellingen CRM-verbinding** kunt u informatie over de volledige synchronisatie op ieder gewenst moment oproepen. Van hieruit kunt u ook het venster **Toewijzingen van integratietabellen** openen, waarin u details van de tabellen in Financials en in de te synchroniseren Dynamics CRM-oplossing kunt zien.

## <a name="see-also"></a>Zie ook
[Relatiebeheer](marketing-relationship-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md)  
[Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Uw organisatie en gebruikers onboarden in Dynamics 365 (online)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
