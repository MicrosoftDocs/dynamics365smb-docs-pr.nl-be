---
title: Aan de slag met een preview-versie van Business Central voor Copilot
description: Legt uit hoe u een Business Central-omgeving krijgt met de nieuwe AI-mogelijkheid voor het genereren van tekstsuggesties voor artikel/product-beschrijvingen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# <a name="get-started-with-a-business-central-preview-version-for-copilot" />Aan de slag met een preview-versie van Business Central voor Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

U kunt met Copilot door AI aangestuurde artikelmarketingtekst uitproberen, of u nu een bestaande Business Central-klant bent of een potentiële klant, dat wil zeggen iemand die alleen geïnteresseerd is in het verkennen van Business Central en het uitproberen van de nieuwe mogelijkheid. Om aan de slag te gaan, hebt u toegang nodig tot een online versie van Business Central Online die de nieuwe mogelijkheid ondersteunt. Vul hieronder het gedeelte in dat voor u van toepassing is.

## <a name="your-organization-already-uses-business-central" />Uw organisatie maakt al gebruik van Business Central

Als bestaande klant of partner hebt u een beheerder nodig met toegang tot het Business Central-beheercentrum om een sandbox-omgeving in te stellen waarop de preview-versie met Copilot wordt uitgevoerd. Zodra de omgeving actief is, kunnen gebruikers de nieuwe functie uitproberen.

Als u een omgevingsbeheerder bent, voert u de volgende stappen uit:

1. Meld u aan bij het beheercentrum van Business Central.
2. Selecteer **Omgevingen** > **Nieuw**.
3. Geef in het deelvenster **Omgeving maken** een naam op voor de nieuwe omgeving in het veld **Omgevingsnaam**.
4. Stel **Omgevingstype** in op **Sandbox** of **Productie**.
5. Stel **Land** in op een land/regio in de lijst, maar houd er rekening mee dat in het voorbeeld de door AI gegenereerde marketingtekst van Copilot alleen in het Engels is.
6. Kies in het vak **Versie** de versie 22 of een hogere versie uit de lijst.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Selecteer **Maken**.  

Ga voor meer informatie over het maken van sandbox-omgevingen naar [Een omgeving maken](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Als u preview-sandboxen hebt die draaien op **22.0.54157.54311 (Preview - Copilot-editie)**, houd er dan rekening mee dat deze omgevingen slechts beschikbaar zijn tot 1 mei 2023. Na deze datum moet u een nieuwe omgeving inrichten of een van uw andere omgevingen upgraden naar versie 22.0 of hoger om de preview van door AI aangedreven artikelmarketingtekst te blijven proberen.

## <a name="your-organization-doesnt-use-business-central" />Uw organisatie maakt geen gebruik van Business Central

Als u geen Business Central-klant bent, meld u dan aan voor een gratis proefversie om de nieuwe AI-mogelijkheden uit te proberen. Aanmelden voor de proefperiode is eenvoudig. U wordt door een paar stappen geleid waarbij u wat informatie moet verstrekken, zoals uw e-mailadres, telefoonnummer en naam. Voer de volgende stappen uit om de proef te krijgen:

1. Ga naar [deze proefsite](https://go.microsoft.com/fwlink/?linkid=2227167) om aan de slag te gaan met het aanmeldingsproces.
2. Volg de instructies op het scherm.

   U wordt gevraagd om informatie zoals uw e-mailadres, naam en telefoonnummer te verstrekken. De exacte ervaring kan variëren, afhankelijk van de informatie die u verstrekt. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Gebruik voor uw e-mailadres uw werk- of schoole-mailadres. We stellen uw proefperiode in voor het account van uw organisatie. U kunt geen e-mailadressen gebruiken die worden verstrekt door e-maildiensten voor consumenten of telecommunicatieproviders, zoals outlook.com, hotmail.com, gmail.com en anderen.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Wanneer u bij de stap **Bevestigingsdetails** komt, bent u klaar om de proefperiode te starten.

   - Selecteer **Overslaan en naar Dynamics 365 Business Central** gaan > **Aan de slag**.
   - U hebt ook de mogelijkheid om anderen in uw organisatie uit te nodigen voor de gratis proefperiode. Voer gewoon de e-mailadressen van elke persoon in en selecteer vervolgens **Uitnodigingen verzenden**. Selecteer **Aan de slag** om naar Business Central te gaan.  

   U wordt omgeleid naar uw proefversie op [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Het kan enkele minuten duren voordat de proefversie gereed is wanneer u zich voor het eerst aanmeldt.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Nadat u bent ingelogd, ziet u de startpagina van Business Central, het rolcentrum genaamd, die lijkt op de volgende afbeelding:

   [![Toont het Business Central-rolcentrum en de controlelijst voor Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Voor een begeleide inleiding tot het maken van AI-aangedreven artikelmarketingtekst met Copilot, selecteert u onder **Uw controlelijst** boven aan de pagina **Maken met Copilot** > **Rondleiding starten**. Volg daarna de instructies op het scherm.

   > [!TIP]
   > Als u **Uw controlelijst** niet ziet, selecteert u eerst de knop **Rondleidingen weergeven** .

## <a name="next-steps" />Volgende stappen

De AI-mogelijkheden van Copilot moeten worden ingeschakeld voordat u of iemand anders Copilot kan gebruiken. Om de AI-mogelijkheden in te schakelen moet een beheerder instemmen met de voorwaarden van de [preview](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) en de [Microsoft-privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=521839) namens de organisatie.

> [!NOTE]
> Als u een proefversie gebruikt, bent u de beheerder. Als u tijdens de aanmelding andere mensen in uw organisatie heeft uitgenodigd voor de proefperiode, kunnen zij Copilot pas gebruiken als u akkoord gaat met de algemene voorwaarden.

Er zijn twee manieren om toestemming te geven als beheerder:

- De gemakkelijkste manier is om Copilot te gebruiken. De eerste keer dat u Copilot als beheerder gebruikt, wordt u gevraagd de voorwaarden te lezen en vervolgens te accepteren of af te wijzen. Ga voor meer informatie over het gebruik van Copilot naar [Marketingtekst toevoegen aan artikelen](item-marketing-text.md).  

- De andere manier is om de pagina **Status van privacyverklaringen** in Business Central te gebruiken en akkoord te gaan met de **Azure OpenAI**-integratie voor alle gebruikers. Ga voor meer informatie naar [Instemmen met voorwaarden](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## <a name="see-also" />Zie ook

[Overzicht van op AI gebaseerde artikelmarketingtekst met Copilot configureren](ai-overview.md)  
[Op AI gebaseerde artikelmarketingtekst met Copilot configureren als beheerder](enable-ai.md)  
[Marketingteksten voor artikelen maken met Copilot](item-marketing-text.md)  
[Veelgestelde vragen over door AI aangestuurde artikelmarketingtekst (preview) met Copilot](ai-faq.md)  
