---
title: Veelgestelde vragen over OneDrive voor Bedrijven
description: Krijg antwoorden op enkele veelvoorkomende vragen over het werken met OneDrive voor Bedrijven en Business Central.
author: brentholtorf
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="onedrive-for-business-faq"></a>Veelgestelde vragen over OneDrive voor Bedrijven

[!INCLUDE [online_only](includes/online_only.md)]

In dit artikel worden enkele van de vragen beantwoord die u mogelijk hebt over het werken met OneDrive en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all--clients"></a>Werkt dit met alle [!INCLUDE[prod_short](includes/prod_short.md)]-clients?

Ja. U kunt bestanden openen in OneDrive vanuit de mobiele [!INCLUDE[prod_short](includes/prod_short.md)]-apps, bij het bekijken van kaartgegevens in Microsoft Teams of zelfs vanuit de Outlook-invoegtoepassing.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Is OneDrive hetzelfde als SharePoint voor het opslaan van bestanden?

Als onderdeel van uw Microsoft 365-abonnement biedt uw organisatie u OneDrive, uw bestandsopslag in de cloud. OneDrive is standaard privé, waar u uw inhoud ordent en kiest welke bestanden of mappen u wilt delen en met wie. SharePoint biedt aan de andere kant een bestandsopslag in de cloud die wordt gedeeld met anderen in uw organisatie.  

## <a name="does--support-consumer-onedrive"></a>Ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] OneDrive voor consumenten?

Nee. Deze integratie is uitsluitend bedoeld voor OneDrive voor Bedrijven en ondersteunt alleen uw werkaccount. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Worden alle OneDrive voor Bedrijven-abonnementen ondersteund?

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt geen zelfstandige abonnementen voor OneDrive voor Bedrijven. OneDrive moet worden gekocht als onderdeel van een Microsoft 365-bedrijfs- of ondernemingsplan. Voor meer informatie zie [Prijzen en abonnementen van OneDrive-cloudopslag vergelijken](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Waar kan ik de status van de OneDrive-service zien?

Beheerders hebben toegang tot het servicestatusdashboard als onderdeel van het Microsoft 365-beheercentrum. Het dashboard bevat de beschikbaarheid van de OneDrive-service. Ga naar [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## <a name="is-onedrive-integration-available-to--on-premises"></a>Is OneDrive-integratie beschikbaar voor [!INCLUDE[prod_short](includes/prod_short.md)] on premises?

Ja, maar in tegenstelling tot [!INCLUDE[prod_short](includes/prod_short.md)] online, zijn er meer instellingen vereist. Zie voor meer informatie [Business Central On-Premises configureren](admin-onedrive-integration-onpremises.md).  

## <a name="does--on-premises-connect-with-sharepoint-server"></a>Maakt [!INCLUDE[prod_short](includes/prod_short.md)] on premises verbinding met SharePoint Server?

Nr. Deze implementatiecombinatie wordt niet ondersteund, zelfs niet als SharePoint Server Mijn sites heeft ingeschakeld.  

## <a name="does--online-connect-with-sharepoint-server"></a>Maakt [!INCLUDE[prod_short](includes/prod_short.md)] online verbinding met SharePoint Server?

Nr. Deze implementatiecombinatie wordt niet ondersteund, zelfs niet als SharePoint Server Mijn sites heeft ingeschakeld.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Hoe werkt dit in een organisatie met meerdere omgevingen?

De integratie gaat ervan uit dat bedrijfsnamen uniek zijn in de [!INCLUDE[prod_short](includes/prod_short.md)]-omgevingen. Wanneer bedrijfsnamen uniek zijn in de hele organisatie, kopieert het openen van een bestand in OneDrive het bestand naar een map met de naam van het huidige bedrijf. Als bedrijfsnamen niet uniek zijn in omgevingen, kunnen bestanden met identieke bedrijfsnamen samen in dezelfde map worden geplaatst.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>We hebben de bedrijfsnaam gewijzigd. Wat gebeurt er met mijn vorige bestanden?

[!INCLUDE[prod_short](includes/prod_short.md)] migreert niet automatisch bestanden die u eerder hebt geopend in OneDrive naar de nieuwe map. Na het hernoemen van uw bedrijf, kopieert de actie Openen in OneDrive bestanden naar een map met de nieuwe bedrijfsnaam.   

## <a name="when-attaching-files-to--how-do-i-pick-a-file-from-onedrive"></a>Bij het toevoegen van bestanden aan [!INCLUDE[prod_short](includes/prod_short.md)], hoe kies ik dan een bestand uit OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] biedt geen cloud-bestandskiezer. U moet het bestand downloaden van OneDrive naar uw apparaat en het vervolgens uploaden naar [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Ik wil bestanden in plaats daarvan openen in SharePoint. Hoe doe ik dit?

[!INCLUDE[prod_short](includes/prod_short.md)] biedt geen functies om bestanden naar SharePoint te kopiëren en ze te openen vanuit een SharePoint-bibliotheek. Neem contact op met uw Microsoft-partner voor meer informatie over uw opties, of zoek naar apps op AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Hoe schakel ik integratie met OneDrive uit?

Voer de begeleide instelling **Configuratie van OneDrive** uit en schakel de schakelaars **OneDrive voor app-functies gebruiken** en **OneDrive voor systeemfuncties gebruiken** uit. 

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Moet ik de pagina Instellingen SharePoint-verbinding gebruiken om verbinding te maken met SharePoint?

Dit is een verouderde functie waarbij alle [!INCLUDE[prod_short](includes/prod_short.md)]-bestanden van alle gebruikers worden verzonden naar één SharePoint-map. We raden u aan het sneltabblad Gedeelde documenten niet te configureren op de pagina **Instellingen SharePoint-verbinding** omdat deze pagina is [verouderd](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) en in releasewave 2 van 2023, versie 23.0 wordt verwijderd.  We raden u aan om in plaats daarvan **Configuratie van OneDrive** te gebruiken.  

## <a name="which-version-of--supports-onedrive"></a>Welke versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt OneDrive?

Integratie met OneDrive kwam beschikbaar in releasewave 2 van 2021.  

## <a name="which-features-are-affected-by-onedrive-integration"></a><a name="features"></a>Welke functies worden beïnvloed door OneDrive-integratie?

In de begeleide instelling **Configuratie van OneDrive** voor het instellen van OneDrive-integratie, kunt u functies voor het verwerken van Business Central-bestanden in OneDrive in- of uitschakelen. De functies zijn verdeeld over twee opties:

|Optie|Omschrijving|
|------|----------|
|**OneDrive voor app-functies gebruiken**|Als u deze optie inschakelt, worden de acties **Openen in OneDrive** en **Delen** beschikbaar gemaakt in bestanden in Business Central, zoals bestanden die zijn bijgevoegd bij documenten of in de rapportinbox. Met deze acties kunnen gebruikers bestanden kopiëren, openen en delen in OneDrive. Zie [Business Central-bestanden openen en delen in OneDrive](across-share-onedrive.md) voor meer informatie.
|**OneDrive voor systeemfuncties gebruiken**|Als u deze optie inschakelt, worden de volgende functies geactiveerd:<ul><li> Met de acties **Openen in Excel** en **Bewerken in Excel** op lijstpagina´s wordt het Excel-bestand naar OneDrive gekopieerd en vervolgens in Excel Online geopend. Zie [Weergeven en bewerken in Excel](across-work-with-excel.md) voor meer informatie.</li><li> Als u een rapport naar een Excel- of Word-bestand exporteert, wordt het bestand automatisch gekopieerd naar OneDrive en vervolgens geopend in Excel Online of Word Online. Zie [Een rapport in een bestand opslaan](ui-work-report.md#saving-a-report-to-a-file) voor meer informatie.|

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Zal Microsoft de integratie met OneDrive blijven verbeteren?

Bij Microsoft luisteren we constant naar feedback van onze zeer uiteenlopende gebruikerscommunity en handelen we naar de beste suggesties. Zie [Releaseplan voor Dynamics 365](/dynamics365-release-plan/2021wave1) voor meer informatie over wat de toekomst biedt voor integraties met Microsoft 365-apps.  

Als u wilt meewerken aan verbetering van OneDrive-integratie, of u een idee hebt dat het delen van bestanden en samenwerking in [!INCLUDE[prod_short](includes/prod_short.md)] zou verbeteren, voegt een idee toe of stemt u op bestaande ideeën op [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Problemen oplossen

Dit gedeelte biedt informatie over het identificeren en oplossen van problemen die u kunt ondervinden bij het gebruik van OneDrive met [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central kan mijn OneDrive niet vinden

Wanneer dit bericht wordt weergegeven: "Kan de locatie van uw OneDrive voor Bedrijven niet bepalen. Neem contact op met uw partner om dit in te stellen", controleert u of de gebruiker ten minste eenmaal toegang heeft gehad tot zijn of haar OneDrive. Als dat niet het geval is, vraagt u de persoon naar portal.office.com/onedrive te gaan om het in te stellen. Dat kan even duren. Als het bericht na 24 uur nog steeds wordt weergegeven, neemt u contact op met de ondersteuning.  
 
### <a name="im-having-problems-sharing-from-outlook"></a>Ik heb problemen met delen vanuit Outlook

Zie [Kan OneDrive-bestanden niet delen vanuit Outlook.com](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) voor Microsoft-ondersteuning.

### <a name="actions-open-in-onedrive-and-share-are-missing"></a>Acties Openen in OneDrive en Delen ontbreken

Er zijn enkele dingen die u kunt controleren:

- Controleer of de toepassingsfuncties voor OneDrive zijn ingeschakeld in de begeleide instelling **Configuratie van OneDrive**. Zie [OneDrive configureren met Configuratie van OneDrive](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Controleer of Microsoft OneDrive is ingesteld op **Akkoord** op de pagina **Status van privacyverklaringen**. Zie [Status van privacyverklaringen](privacy-notices-status.md).

## <a name="see-also"></a>Zie ook

[Integratie van Business Central en OneDrive](across-onedrive-overview.md)  
[OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
