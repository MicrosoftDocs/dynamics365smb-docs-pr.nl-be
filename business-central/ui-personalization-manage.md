---
title: Pagina's aanpassen voor rollen
description: 'Leer hoe u de gebruikersinterface voor een profiel (rol) kunt aanpassen, zodat alle gebruikers aan wie die rol is toegewezen, een aangepaste werkruimte zien.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="customize-pages-for-profiles"></a>Pagina's aanpassen voor profielen

Business Central biedt zowel [personalisatie](ui-personalization-user.md) voor gebruikers als aanpassing voor beheerders. Met personalisatie kunnen gebruikers hun werkruimte aanpassen door pagina-indelingen aan te passen aan hun eigen voorkeuren. Beheerders kunnen pagina-indelingen voor een specifiek profiel aanpassen, op basis van bedrijfsrollen of afdelingen, zodat alle toegewezen gebruikers dezelfde aangepaste pagina zien. Terwijl personalisatie gebruikers in staat stelt velden en acties op een pagina weer te geven, te verbergen en te verplaatsen, biedt aanpassing extra mogelijkheden. Met aanpassing kunt u bijvoorbeeld velden weergeven die zich in de brontabel of uitbreidingstabellen van de pagina bevinden, maar die niet zijn gedefinieerd in het paginaobject&mdash;dat is met personalisatie niet mogelijk.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Het typische zakelijke gebruik van een profiel is een rol. Een profiel wordt daarom genoemd *Profiel (rol)* in de gebruikersinterface.

Pagina-aanpassing begint vanaf de pagina **Profielen (rollen)**, het startpunt van de beheerder voor het beheren van gebruikersprofielen op individuele profielkaarten. Naast het aanpassen van de pagina-indeling kunt u verschillende andere instellingen voor profielen kiezen op de pagina **Profiel (rol)** voor elk profiel. Zie [Profielen beheren](admin-users-profiles-roles.md) voor meer informatie.

## <a name="prerequisites"></a>Vereisten

- Uw Business Central-account moet de machtigingenset **D365 Profielbeheer** of gelijkwaardige machtigingen hebben. 

   De machtigingenset **D365 Profielbeheer** omvat de uitvoeringsmachtiging voor het systeemobject **9026 Veld aan tabel toevoegen**. Als u deze machtiging niet heeft, mag u geen velden aan de pagina toevoegen, tenzij deze zijn gedefinieerd in het paginaobject. 

## <a name="customize-pages-for-a-profile"></a>Pagina's aanpassen voor een profiel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Profielen (rollen)** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor het profiel waarvoor u pagina's wilt aanpassen en kies de actie **Bewerken**.
3. Kies de actie **Pagina's aanpassen**.

    [!INCLUDE[prod_short](includes/prod_short.md)] wordt geopend met een nieuw browsertabblad voor het geselecteerde profiel met de banner **Aanpassen** geactiveerd. De banner **Aanpassen** biedt dezelfde functionaliteit als de banner **Personaliseren** die beschikbaar is voor gebruikers.

4. Pas pagina's aan volgens de behoeften van de betreffende rol of afdeling op dezelfde manier als een gebruiker zou doen bij het personaliseren. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

    > [!NOTE]
    > Gebruik <kbd>Ctrl</kbd>+<kbd>klik</kbd> op een actie om te navigeren tijdens personalisatie als de actie wordt gemarkeerd door de pijlpunt.

5. Wanneer u klaar bent met het wijzigen van de indeling van een of meer pagina's, kiest u de knop **Gereed** op de banner **Aanpassen**.
6. Sluit het browsertabblad.

De aanpassing van pagina's is nu vastgelegd voor het profiel.

## <a name="view-all-customized-pages-for-a-profile"></a>Alle aangepaste pagina's voor een profiel weergeven

U kunt een overzicht krijgen van welke pagina's zijn aangepast voor een profiel, bijvoorbeeld om te plannen welke pagina's u verder wilt aanpassen of verwijderen.

- Kies op de pagina **Profiel (rol)** de actie **Aangepaste pagina's beheren**.

Op de pagina **Aangepaste pagina's** kunt u aanpassingen verwijderen en problemen oplossen door te scannen op mogelijke problemen.  

## <a name="delete-all-customizations-for-a-profile"></a>Alle aanpassingen voor een profiel verwijderen

U kunt alle aanpassingen die u hebt gemaakt voor een profiel, annuleren. Aanpassingen die met een extensie zijn aangebracht en door een gebruiker gemaakte personalisaties worden niet verwijderd. U kunt alle personalisaties met een andere actie verwijderen. Zie voor meer informatie [Alle aanpassingen verwijderen die door een gebruiker zijn aangebracht](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Kies op de pagina **Profiel (rol)** voor een aangepast profiel de actie **Aangepaste pagina's wissen**.

De indeling op pagina's voor het profiel wordt opnieuw ingesteld op de standaardindeling.  

## <a name="delete-customization-for-specific-pages-for-a-profile"></a>Aanpassing verwijderen voor specifieke pagina's voor een profiel

U kunt ook afzonderlijke pagina-aanpassingen verwijderen die u voor een profiel hebt aangebracht. Aanpassingen die met een extensie zijn aangebracht en door een gebruiker gemaakte personalisaties worden niet verwijderd. U kunt specifieke paginapersonalisaties met een andere actie verwijderen. Zie voor meer informatie [Personalisaties voor specifieke pagina's verwijderen](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Kies op de pagina **Profiel (rol)** de actie **Aangepaste pagina's beheren**.
2. Selecteer op de pagina **Aangepaste pagina's** een of meer regels voor pagina-aanpassingen die u wilt verwijderen en kies vervolgens de actie **Verwijderen**.

De indeling op de geselecteerde pagina's wordt aangepast aan de wijzigingen die u hebt aangebracht.

## <a name="add-a-field"></a>Een veld toevoegen

U voegt velden toe aan de pagina toe vanuit het deelvenster **Veld toevoegen aan pagina**, dat u opent door de actie **+ Veld** te selecteren in de aanpassingsmodus. Het is belangrijk om te begrijpen dat het deelvenster **Veld toevoegen aan pagina** wordt gebruikt om velden weer te geven die al bestaan&mdash;hetzij op de pagina en de brontabellen ervan&mdash;maar die momenteel aan het zicht zijn onttrokken. U kunt geen nieuwe velden maken.

Het deelvenster **Veld toevoegen aan pagina** toont alle velden die op de pagina kunnen worden weergegeven. Velden zijn onderverdeeld in de volgende categorieën, zoals bepaald door het onderliggende ontwerp van de pagina zelf, de brontabel en extensies:

|Categorie|Omschrijving|
|-|-|
|Tabelvelden niet in het paginaobject|Omvat velden die zijn gedefinieerd in de basistabel of uitbreidingstabellen, maar niet op de pagina zijn gedefinieerd. De knopinfo voor deze velden bevat het label **Gedefinieerd door de tabel**.<br><br>|
|Paginavelden die zijn verbonden met een tabel|Omvat velden die zijn gedefinieerd in de basistabel of tabelextensies en die ook op de pagina zijn gedefinieerd als weergegeven of verborgen. De knopinfo voor deze velden bevat het label **Gedefinieerd door de pagina**.|
|Paginavelden die niet verbonden zijn met een tabel| Velden die alleen zijn gedefinieerd op de pagina, maar niet in de basistabel of uitbreidingstabellen. Deze velden worden doorgaans gebruikt voor variabelen of berekeningen. De knopinfo voor deze velden bevat het label **Gedefinieerd door de pagina**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Gebruik de filterknop boven de lijst om te wijzigen welke categorie velden wordt weergegeven in het deelvenster **Veld toevoegen aan pagina**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Toont de filterknop in het deelvenster Een veld toevoegen in de personalisatiemodus.":::
 
### <a name="add-table-field-thats-not-on-the-page-object"></a>Tabelveld toevoegen dat zich niet in het paginaobject bevindt

Als u een alleen-tabelveld op een pagina beschikbaar wilt maken voor gebruikers, moet u dit eerst aan de pagina toevoegen. Nadat u het veld heeft toegevoegd, kunnen gebruikers ervoor kiezen om het veld naar wens weer te geven of te verbergen met behulp van personalisatie. Er zijn verschillende manieren om een veld toe te voegen.

- Eén manier is om het uit het deelvenster **Veld toevoegen aan pagina** naar de gewenste positie te slepen.
- Een andere manier is om het veld in het deelvenster te selecteren om de aanbevolen locatie op de pagina weer te geven. Ga vervolgens naar de veldlocatie op de pagina's, selecteer de pijlpunt en selecteer vervolgens **Toevoegen**. 

Zodra het veld is toegevoegd, schakelt de knopinfo voor het veld in het deelvenster **Veld toevoegen aan pagina** over naar **Gedefinieerd door de pagina**. Het toegevoegde veld is vergrendeld voor bewerken en kan niet worden ontgrendeld.

## <a name="remove-a-field"></a>Een veld verwijderen

Als u een tabelveld hebt toegevoegd dat oorspronkelijk niet in het paginaobject stond, kunt u dit weer verwijderen. Het verwijderen van een veld is iets anders dan het verbergen ervan. Wanneer u een veld verbergt, kunnen gebruikers het via personalisatie nog steeds op hun werkruimte weergeven. Als u echter een veld verwijdert, kan het veld niet langer door gebruikers worden weergegeven of verborgen. Als het veld momenteel wordt weergegeven in de werkruimte van een gebruiker, verdwijnt het uit werkruimte van de gebruiker wanneer u het verwijdert. 

Als u een veld wilt verwijderen, selecteert u de pijlpunt op het veld op de pagina en selecteert u vervolgens **Verwijderen**. Als u het veld niet kunt vinden, selecteert u het in het deelvenster **Veld toevoegen aan pagina** om de verborgen locatie aan te geven. 

> [!IMPORTANT]
> Als u een veld verwijdert, worden de gegevens die in het veld of in de brontabellen ervan zijn opgeslagen niet verwijderd. Het verwijdert alleen het veld uit het zicht. 

## <a name="lock-and-unlock-editing"></a>Bewerking vergrendelen en ontgrendelen

Met aanpassing kunt u de meeste velden op een pagina vergrendelen (bewerken toestaan) of ontgrendelen (bewerken voorkomen). Als u het bewerken wilt vergrendelen of ontgrendelen, selecteert u het veld op de pagina, selecteert u de pijlpunt en selecteert u vervolgens **Bewerking vergrendelen** of **Bewerking ontgrendelen**. Het is belangrijk om een aantal regels in gedachten te houden over het vergrendelen en ontgrendelen van velden:

- Velden die oorspronkelijk niet op het paginaobject stonden, maar door aanpassing aan de pagina zijn toegevoegd, zijn altijd vergrendeld en kunnen niet worden ontgrendeld met behulp van aanpassing of personalisatie.
- Het ontwerp van het veld kan ook voorkomen dat het wordt bewerkt. Als de AL-ontwikkelaar de [eigenschap Bewerkbaar](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) van het veld instelt op `false`, is het altijd vergrendeld en kan het niet worden ontgrendeld.
- Het is belangrijk op te merken dat de functie voor het bewerken van vergrendelingen bedoeld is om de nauwkeurigheid, consistentie en betrouwbaarheid van gegevens te bevorderen. Het is niet bedoeld om de gegevensintegriteit te waarborgen.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## <a name="important-information-and-tips"></a>Belangrijke informatie en tips

- Mogelijk zijn niet alle tabelvelden beschikbaar voor aanpassing via het deelvenster **Veld toevoegen aan pagina**. De ontwikkelaar van een tabel kan ervoor kiezen om te voorkomen dat een veld bij aanpassing wordt weergegeven door de [eigenschap AllowInCustomization](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) van het veld in te stellen op `false`.
- U kunt een pagina die zich in de [analysemodus](analysis-mode.md) bevindt, niet aanpassen. De schakelaar **Analyseren** is gedeactiveerd. Als u naar de aanpassingsmodus overschakelt terwijl de pagina zich in de analysemodus bevindt, wordt de analysemodus automatisch uitgeschakeld. 
- Sommige pagina's hebben meerdere paginavelden die aan dezelfde brontabel zijn toegewezen. In het deelvenster **Veld aan pagina toevoegen** worden al deze paginavelden onafhankelijk weergegeven. U kunt deze velden onafhankelijk weergeven, verbergen of verplaatsen zonder dat dit gevolgen heeft voor de andere.
- Als een onderdeel of groep verborgen is, kunt u nog steeds verborgen velden binnen het onderdeel of de groep identificeren, maar u kunt pas velden in het onderdeel of de groep toevoegen, verplaatsen of weergeven als ze zichtbaar zijn gemaakt. 
## <a name="see-also"></a>Zie ook

[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
