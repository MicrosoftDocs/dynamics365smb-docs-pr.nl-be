---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
---

> [!NOTE]
> In de volgende secties wordt ervan uitgegaan dat u beheerderstoegang hebt tot Exchange Online.

Voordat u e-mailregistratie kunt instellen, moet u [openbare mappen](/exchange/collaboration-exo/public-folders/public-folders) voor Office 365 voorbereiden. U kunt dit doen in het [Exchange-beheercentrum](/exchange/exchange-admin-center?preserve-view=true) of u kunt de [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true) gebruiken.

> [!TIP]
> Als u de [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) wilt gebruiken, vindt u inspiratie voor het instellen van uw script in een voorbeeldscript dat we hebben gepubliceerd in [de BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging)..

Volg de onderstaande stappen om Exchange Online in te stellen, met koppelingen naar waar u meer kunt leren.

### <a name="create-an-admin-role-group"></a><a name="create-an-admin-role-group"></a>Een beheerdersrolgroep maken

Maak een beheerdersrolgroep voor openbare mappen op basis van de informatie in de volgende tabel:

|Eigenschap        |Waarde                     |
|----------------|--------------------------|
|Name            |Beheer van openbare mappen |
|Geselecteerde rollen  |Openbare mappen            |
|Geselecteerde gebruikers  |Het e-mailadres van het gebruikersaccount dat Business Central zal gebruiken om de e-mailregistratietaak uit te voeren|

Zie voor meer informatie [Rolgroepen beheren in Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a><a name="create-a-new-public-folder-mailbox"></a>Een nieuwe openbare mappostbus maken

Maak een nieuwe openbare mappostbus op basis van de informatie in de volgende tabel:

|Eigenschap        |Waarde                     |
|----------------|--------------------------|
|Name            |Openbare postbus            |

Zie [Een openbare mappostbus maken](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox) voor meer informatie.

### <a name="create-new-public-folders"></a><a name="create-new-public-folders"></a>Nieuwe openbare mappen maken

1. Maak een nieuwe openbare map met de naam **E-mailregistratie** in de root, zodat het volledige pad naar de map `\Email Logging\` wordt.
2. Maak twee submappen zodat het resultaat de volgende volledige paden naar de mappen is:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Zie [Een openbare map maken](/exchange/collaboration-exo/public-folders/create-public-folder) voor meer informatie.

### <a name="set-public-folder-ownership"></a><a name="set-public-folder-ownership"></a>Eigendom van openbare mappen instellen

Stel de gebruiker voor e-mailregistratie in als eigenaar van beide openbare mappen, *Wachtrij* en *Opslag*.

Zie voor meer informatie [Machtigingen voor openbare mappen toewijzen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a><a name="mail-enable-the-queue-public-folder"></a>De openbare map *Wachtrij* inschakelen voor post

  Zie [Een openbare map in- of uitschakelen voor post](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder) voor meer informatie.

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a><a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>E-mail inschakelen voor het verzenden van e-mails naar de openbare map *Wachtrij*

Schakel e-mail in voor het verzenden van e-mails naar de openbare map *Wachtrij* met behulp van Outlook of de Exchange Management Shell.

Zie voor meer informatie [Anonieme gebruikers toestaan om e-mail te verzenden naar een voor e-mail geschikte openbare map](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a>Regels voor e-mailstroom maken

Maak twee e-mailstroomregels op basis van de informatie in de volgende tabel:

|Doel  |Name |Pas deze regel toe als...             |Ga als volgt te werk...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Een regel voor inkomende e-mail |Naar deze organisatie verzonden e-mail registreren|*De afzender* bevindt zich *buiten de organisatie* en *de ontvanger* bevindt zich *binnen de organisatie*|BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*|
|Een regel voor uitgaande e-mail | Uit deze organisatie verzonden e-mail registreren |*De afzender* bevindt zich *binnen de organisatie* en *de ontvanger* bevindt zich *buiten de organisatie*|BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*|

Zie voor meer informatie [Poststroomregels beheren in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) en [Poststroomregelacties in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Als u wijzigingen aanbrengt in de Exchange Management Shell, worden de wijzigingen met vertraging zichtbaar in het Exchange-beheercentrum. De wijzigingen die in Exchange zijn aangebracht, zijn ook beschikbaar in [!INCLUDE[prod_short](prod_short.md)] na een vertraging. De vertraging kan enkele uren duren.
