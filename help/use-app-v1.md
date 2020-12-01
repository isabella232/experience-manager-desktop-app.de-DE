---
title: Verwenden Sie [!DNL Experience Manager] Desktop-App Version 1.x.
description: Erfahren Sie, wie Sie das Adobe Experience Manager-Desktop-Programm, Version 1.x verwenden und Ihre Arbeit mit Assets auf dem Desktop optimieren können.
contentOwner: AG
translation-type: tm+mt
source-git-commit: 2893fc1f8aad02e1436a1a281a320e6837487220
workflow-type: tm+mt
source-wordcount: '2379'
ht-degree: 64%

---


# Verwenden Sie [!DNL Experience Manager] Desktop-App v1.x {#use-aem-desktop-app-v1x}

Mit der App können die Elemente innerhalb von [!DNL Experience Manager] auf Ihrem lokalen Desktop leicht zugänglich gemacht und in allen Desktop-Anwendungen verwendet werden. Assets können einfach in Mac Finder oder Windows Explorer angezeigt, in Desktop-Anwendungen geöffnet und lokal geändert werden - die Änderungen werden mit einer neuen Version, die im Repository erstellt wurde, wieder auf [!DNL Experience Manager] gespeichert.

Dank dieser Integration können unterschiedliche Rollen in der Organisation die Assets in  Assets zentral verwalten und in Creative Cloud und anderen Applikationen darauf zugreifen. Gleichzeitig können diverse Standards einschließlich Branding-Vorgaben leichter eingehalten werden.

Die wichtigsten Aufgaben, die Sie mit der [!DNL Experience Manager] Desktop-App v1 ausführen, sind:

1. [Verbindung mit  [!DNL Experience Manager] einem Server](#installandconnect)
1. [Assets direkt auf dem Desktop öffnen](#openondesktop)
1. [Assets auf dem Desktop bearbeiten und auschecken](#workonassets)
1. [Assets und Ordner stapelweise hochladen](#bulkupload)

Informationen zu den empfohlenen und nicht empfohlenen Vorgehensweisen finden Sie unter [Best Practices zur Verwendung des Programms](best-practices-for-v1.md). Wenn Sie bei der Verwendung des Programms Probleme haben, finden Sie weitere Informationen unter [ [!DNL Experience Manager] Fehlerbehebung für Desktop](troubleshoot-app-v1.md).

>[!NOTE]
>
>[!DNL Experience Manager] Die Desktop-App wurde in Version  [!DNL Experience Manager] 6.1 eingeführt und aufgerufen  [!DNL Experience Manager Assets Companion App].

## [!DNL Experience Manager] Touchpoints der Desktop-App im kreativen Workflow  {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] Die Desktop-App integriert zusammen mit  [!DNL Assets]den folgenden Touchpoints in Ihren kreativen Workflow und Angebote.

![[!DNL Experience Manager] Touch-Points für die Desktop-App im kreativen Workflow](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] Touch-Points für die Desktop-App im kreativen Workflow

## Installieren und Verbinden der App mit dem [!DNL Experience Manager]-Server {#installandconnect}

Bevor Sie mit der Erstellung oder Bearbeitung der kreativen Assets beginnen können, verbinden Sie die Desktop-Anwendung mit dem Server [!DNL Assets], um Assets herunterzuladen und in das Repository hochzuladen. Führen Sie die folgenden Aufgaben durch:

1. [Installieren Sie das Programm](#installapp).
1. [Legen Sie Ihre Voreinstellungen](#inapppref) und Verbindungsdetails fest.
1. [Stellen Sie eine Verbindung zum  [!DNL Experience Manager] ](#connect) Server her und binden Sie das Asset-Repository als lokales Laufwerk ein.
1. [Aktivieren Sie Desktop-](#desktopactions) Aktionen auf dem  [!DNL Experience Manager] Server.

[!DNL Experience Manager] Die Desktop-App verwendet eine HTTPS-Verbindung, um eine Verbindung zum  [!DNL Experience Manager] Server herzustellen, um Ihre Assets zuverlässig und sicher zu übertragen.

>[!NOTE]
>
>Für einen Teil oder alle der Installations- und Konfigurationsschritte benötigen Sie möglicherweise Hilfe von Ihrem [!DNL Experience Manager]-Administrator oder Systemadministrator.

### Installieren des Programms {#installapp}

Um die [!DNL Experience Manager]-Desktop-App zu verwenden, stellen Sie sicher, dass Ihre [!DNL Experience Manager]-Serverversion von der App unterstützt wird. Laden Sie die entsprechende Installationsdatei (binär) für Ihr Betriebssystem (Mac oder Windows) herunter und installieren Sie das Programm.

Je nach Netzwerk- und Systemvoreinstellungen kann eine detaillierte Konfiguration erforderlich sein. Weitere Informationen finden Sie unter [Installieren und konfigurieren [!DNL Experience Manager] Desktop-App](install-configure-app-v1.md).

1. Gehen Sie zur Download-Seite [[!DNL Experience Manager] Desktop-App](https://helpx.adobe.com/de/experience-manager/kb/download-companion-app.html) und laden Sie die entsprechende Binärdatei für Ihr Betriebssystem herunter.
1. Starten Sie die heruntergeladene Installationsdatei und befolgen Sie die Bildschirmanweisungen, um das Programm zu installieren.

   >[!NOTE]
   >
   >Es kann jeweils nur eine Instanz der Desktop-App [!DNL Experience Manager] installiert und aktiv sein.

### Grundlegendes zu den Optionen und Voreinstellungen des Programms {#inapppref}

Die Anwendung ermöglicht die Verbindung und Trennung von [!DNL Experience Manager]-Servern, die Ansicht von Uploads, die Verwaltung des lokalen Cache usw. Typische Benutzer des Programms können die Standardeinstellungen verwenden. Sie können die Einstellungen anpassen, um mehr aus der Anwendung und aus der Integration mit dem [!DNL Experience Manager]-Server herauszuholen. Die verschiedenen Einstellungen werden im Folgenden detailliert beschrieben.

**Assets durchsuchen**[!DNL Assets] Öffnen Sie das lokale Laufwerk, auf dem das Repository für bereitgestellt wurde. Durchsuchen Sie also die Assets, die Ihnen nun auf Ihrem lokalen Computer zur Verfügung stehen.

**Status** von Ansichten-AssetsWenn geänderte Assets hochgeladen oder neue Assets zum  [!DNL Assets] Repository hinzugefügt werden, lädt die Anwendung die Assets im Hintergrund hoch. Der Upload im Hintergrund ermöglicht die reibungslose Ausführung von Vorgängen, ohne dass der Abschluss des Uploads abgewartet werden muss. Dies ist insbesondere bei umfangreichen Assets hilfreich. Sie können die Änderungen lokal speichern und müssen sich nicht mehr darum kümmern. Je nach verfügbarer Bandbreite nimmt das Senden dieser Assets an den Server durch das Programm etwas Zeit in Anspruch. Sie können den Status des Uploads sowie weitere grundlegende Informationen überprüfen.

**** OptionenKlicken Sie auf Optionen aus dem Ablage der Desktop-App, um auf die Einstellungen zuzugreifen und die Anwendung zu starten, wenn Ihr System Beginn hat. Verbindung zum  [!DNL Experience Manager] Server beim Starten der App herstellen; und um den lokalen Laufwerksbuchstaben zu ändern, wo er nach der Montage verfügbar  [!DNL Assets] ist.

**Advanced > Manage cache (Erweitert > Cache verwalten)** Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte des [!DNL Assets]-Servers werden lokal zwischengespeichert, um ein reibungsloseres Erlebnis zu erhalten. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Assets, die nicht in den [!DNL Experience Manager]-Server eingecheckt sind, werden beibehalten und nicht gelöscht.

### Verbindung zu einem [!DNL Experience Manager]-Server {#connect}

Das Programm unterstützt die Proxy-Konfiguration unter Mac und Windows. Die Konfiguration wird gelesen, wenn das Programm gestartet wird. Wenn Sie die Proxy-Einstellungen ändern, müssen Sie das Programm neu starten, damit die Änderungen übernommen werden.

>[!NOTE]
>
>Wenn Sie die Proxy-Einstellungen ändern, müssen Sie das Programm neu starten, damit die Änderungen übernommen werden. Andernfalls verwendet das Programm weiterhin den zuvor konfigurierten Proxyserver.

1. Starten Sie die Desktop-App [!DNL Experience Manager]. Um die [!DNL Experience Manager]-Instanz der App zuzuordnen, geben Sie den [!DNL Experience Manager]-Server im Format `https://[aem-server-url]:[port]` an.

   ![Authentifizierung auf einem Mac und Bereitstellen der  [!DNL Experience Manager] Server-URL](assets/aem_desktop_app_server_url.png)

1. Geben Sie im Anmeldebildschirm den Benutzernamen und das Kennwort für Ihre Instanz an. Um eine alternative [!DNL Experience Manager]-Instanz anzugeben, wählen Sie die Option **[!UICONTROL Alternate Login URL]**.

   ![Geben Sie  [!DNL Experience Manager] Serverberechtigungen auf dem Anmeldebildschirm der  [!DNL Experience Manager] Desktop-App an](assets/login_screen_v1.png)

### Aktivieren von Desktop-Aktionen in der [!DNL Experience Manager]-Weboberfläche {#desktopactions}

Über die Assets-Benutzeroberfläche können Sie zu den Asset-Speicherorten navigieren oder Assets auschecken und öffnen, um sie in Ihrem Desktop-Programm zu bearbeiten. Diese Optionen werden als Desktop-Aktionen bezeichnet und sind standardmäßig nicht aktiviert. Führen Sie die folgenden Schritte aus, um sie zu aktivieren.

1. Klicken/tippen Sie in der Assets-Benutzeroberfläche rechts oben in der Symtolleiste auf das Benutzersymbol.
1. Klicken Sie auf **[!UICONTROL My Preferences]**, um das Dialogfeld **[!UICONTROL Preferences]** anzuzeigen.

   ![[!DNL Experience Manager] Benutzeroberfläche mit Benutzereinstellungen](assets/aem_ui_user_preferences.png)

1. Wählen Sie im Dialogfeld „Benutzereinstellungen“ die Option **[!UICONTROL Show Desktop Actions For Assets]**. Klicken Sie auf **[!UICONTROL Accept]**.

   ![Aktivieren Sie [!UICONTROL Show Desktop Actions For Assets], um Desktop-Aktionen zu aktivieren.](assets/enable_desktop_actions.png)

   *Abbildung: Aktivieren von „Desktop-Aktionen für Assets anzeigen“ zur Ermöglichung von Desktop-Aktionen.*

## Zugreifen auf und Öffnen von Assets über den Desktop {#openondesktop}

Wenn Sie auf **Öffnen** klicken, um ein Asset auf einem lokalen Computer zu öffnen, lädt das Programm das Asset in den internen Cache herunter. Das Programm startet das native Desktop-Programm, das dem Dateityp des heruntergeladenen Assets zugeordnet ist.

Wählen Sie unter Mac **Öffnen** aus dem Kontextmenü, um ein Asset über die [!DNL Experience Manager] Desktop-App zu öffnen. Wählen Sie unter Windows im Kontextmenü die Option „Open on Web“ (Im Web öffnen) aus, um das Asset zu öffnen. Klicken Sie im Fenster „Asset Status“ (Asset-Status) auf das Symbol ![Auf dem Desktop öffnen](assets/do-not-localize/aemassets_icon_openondesktop.png), bzw. tippen Sie darauf, um das Asset zu öffnen.

Wählen Sie bei Adobe InDesign-Dateien (INDD) im Kontextmenü die Option **[!UICONTROL Open]** aus. Wenn Sie auf diese Option klicken, lädt das Programm die verknüpften Assets in Ihr lokales Dateisystem herunter und öffnet anschließend die INDD-Datei in Adobe InDesign. Mithilfe dieser Methode wird sichergestellt, dass die erforderlichen Assets beim Bearbeiten einer INDD-Datei lokal verfügbar sind.

![Kontextmenüoptionen zum Zugriff auf und Öffnen von Assets mit der  [!DNL Experience Manager] Desktop-App](assets/aem_desktopapp_mac_context_menu.png)

*Abbildung: Optionen im Kontextmenü, um mit der  [!DNL Experience Manager] Desktop-App auf Assets zuzugreifen und sie zu öffnen.*

>[!NOTE]
>
>Unter Windows verhindert die Einstellung [Windows 7 standardmäßig, dass ](https://support.microsoft.com/de-de/kb/2668751)-Desktop-App Assets verarbeitet, die größer als 50 MB sind.[!DNL Experience Manager]

>[!NOTE]
>
>Adobe empfiehlt, unter Mac die Optionen **Elementinformationen anzeigen**, **Element-Vorschau anzeigen** und **Vorschau anzeigen** für den gemounteten Ordner [!DNL Assets] zu deaktivieren. Dadurch wird die Leistung verbessert.

### Zusätzliche Optionen in der [!DNL Experience Manager]-Schnittstelle {#additional-options-in-aem-assets}

Nachdem Sie das [!DNL Assets]-Repository Ihrem lokalen Laufwerk zugeordnet haben, können Sie zusätzliche Symbole und die Funktion &quot;Ordner hochladen&quot;aktivieren, die für die zugeordneten Assets und Ordner angezeigt werden.

1. Öffnen Sie die [!DNL Assets]-Schnittstelle und bewegen Sie den Mauszeiger über einen Ordner oder ein Asset, um die Desktop-Aktionen als Schnellaktionen in der Ansicht &quot;Karte&quot;anzuzeigen.

   ![Schnellaktionsmenü in der Assets-Benutzeroberfläche öffnen, um Desktop-Aktionen anzuzeigen](assets/desktop_actions_in_card_view.png)

   *Abbildung: Schnellaktionsmenü in der Assets-Benutzeroberfläche öffnen, um Desktop-Aktionen anzuzeigen.*

   Sie können auch auf diese Desktop-Aktionen zugreifen, indem Sie in der Symbolleiste auf die Option **Desktop-Aktionen** klicken, nachdem Sie das Asset ausgewählt haben. Eine weitere Möglichkeit bietet die Symbolleiste auf der Asset-Seite.

1. Wenn Sie das Asset in der Desktop-Applikation öffnen möchten, die der jeweiligen Dateierweiterung zugeordnet ist, klicken Sie auf die Schnellaktion **Auf dem Desktop öffnen**![Auf dem Desktop öffnen](assets/do-not-localize/aemassets_icon_openondesktop.png).

   Alternativ können Sie die Option **Öffnen** über das Menü **Desktop-Aktionen** in der Symbolleiste auswählen.

Um das gewünschte Asset in Ihrem lokalen Dateisystem zu finden, klicken Sie auf die Schnellaktion **Anzeigen** ![Symbol „Anzeigen“](assets/do-not-localize/aemassets_reveal_icon.png). Alternativ können Sie die Option **Anzeigen** über das Menü **Desktop-Aktionen** in der Symbolleiste auswählen.

## Grundlegendes zu den Asset-Status  {#understand-the-asset-statuses}

| ![Windows-Standardapplikationssymbol](assets/do-not-localize/win_default.png) | Das Programm ist mit dem Server verbunden und alle Assets sind synchronisiert. |
--- |--- |
| ![Symbol für Windows deaktiviert](assets/do-not-localize/win_disabled.png) | Das Programm wurde gestartet, es ist jedoch nicht mit dem Server verbunden. Bei einigen Assets steht möglicherweise die Synchronisierung aus. |
| ![Symbol für die Windows-Dateisynchronisierung](assets/do-not-localize/win_sync.png) | Assets werden synchronisiert. Dateien werden hoch- oder herunterladen. Im Fenster „Asset Status“ (Asset-Status) können Sie den exakten Status anzeigen und die Übertragungen pausieren. |
| ![Symbol für Windows-Neuverbindung](assets/do-not-localize/win_refresh.png) | Das Programm versucht, eine erneute Verbindung herzustellen. Möglicherweise führen Netzwerkprobleme zur Trennung der Verbindung. |

## Bearbeiten von Assets {#workonassets}

### Assets aus der [!DNL Experience Manager]-Weboberfläche {#check-out-assets-from-the-aem-web-interface} auschecken

[!DNL Assets]Mit können Sie Assets zum Bearbeiten auschecken und dann wieder einchecken, wenn Sie keine weiteren Änderungen vornehmen möchten. Wenn Sie ein Asset ausgecheckt haben, können nur Sie das Asset bearbeiten, mit Anmerkungen versehen, veröffentlichen, verschieben oder löschen. Durch das Auschecken eines Assets wird das Asset gesperrt und andere Benutzer können derartige Vorgänge nicht durchführen. Um Assets aus-/einchecken zu können, benötigen Sie entsprechenden Schreibzugriff.

Es gibt zwei Möglichkeiten, Assets über die [!DNL Experience Manager]-Weboberfläche auszuchecken. Ausführliche Informationen zur ersten Methode finden Sie unter [Ein- und Auschecken von Dateien über die Assets-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/check-out-and-submit-assets.html?lang=de). Führen Sie die folgenden Schritte aus, um die zweiten Methoden zum Auschecken und Öffnen des Assets zu verwenden, wenn die [!DNL Experience Manager] Desktop-App installiert ist.

1. Öffnen Sie die [!DNL Assets]-Schnittstelle und bewegen Sie den Mauszeiger über einen Ordner oder ein Asset, um die Desktop-Aktionen als Schnellaktionen in der Ansicht &quot;Karte&quot;anzuzeigen.

   ![Option „Eigenschaften“ in der Kartenansicht](assets/desktop_actions_in_card_view.png)

   Sie können auch auf diese Desktop-Aktionen zugreifen, indem Sie in der Symbolleiste auf das Symbol „Desktop-Aktionen“ klicken/tippen, nachdem Sie das Asset ausgewählt haben. Eine weitere Möglichkeit bietet die Symbolleiste auf der Asset-Seite.

1. Klicken/tippen Sie zum Öffnen des Assets auf die Schnellaktion „Auf dem Desktop öffnen“ ![Auf dem Desktop öffnen](assets/do-not-localize/aemassets_icon_openondesktop.png).

   Alternativ können Sie die Option „Öffnen“ über das Menü „Desktop-Aktionen“ in der Symbolleiste auswählen.

   >[!NOTE]
   >
   >Wenn Sie eine Datei bearbeiten, die gerade geöffnet ist und nicht ausgecheckt wurde, erfahren andere Benutzer nicht, dass Sie ein Asset aktualisieren.

1. Wenn Sie ein Asset für die Bearbeitung in einer Adobe Creative Cloud-Applikation öffnen möchten, klicken/tippen Sie auf die Schnellaktion ![Desktop bearbeiten](assets/do-not-localize/aemassets_icon_editdesktop.png). Dadurch wird das Asset auch zur Bearbeitung ausgecheckt. Nachdem Sie die Bearbeitung abgeschlossen haben, checken Sie das Asset ein, um die Änderungen in [!DNL Assets] zu aktualisieren.

   Alternativ können Sie die Option „Bearbeiten“ über das Menü „Desktop-Aktionen“ in der Symbolleiste auswählen.

1. Wählen Sie die Menüoption „Öffnen“ aus. Die ausgewählten Assets werden im Vorschaumodus geöffnet.
1. Um die Assets zu bearbeiten, wählen Sie die Option „Bearbeiten“ aus. Die Assets werden im Bearbeitungsmodus geöffnet.

### Auschecken von Assets aus dem Finder unter macOS {#check-out-assets-on-mac}

Mithilfe des Programms können Sie Dateien auschecken, damit andere Benutzer keine Änderungen an den Dateien vornehmen können, an denen Sie gerade arbeiten.

1. Wählen Sie im Mac-Kontextmenü die Option &quot;AEM Assets-Ordner öffnen&quot;, um den Finder zu öffnen.

   ![Kontextmenüoptionen zum Zugriff auf und Öffnen von Assets mit der  [!DNL Experience Manager] Desktop-App](assets/aem_desktopapp_mac_context_menu.png)

   *Abbildung: Optionen im Kontextmenü, um mit der  [!DNL Experience Manager] Desktop-App auf Assets zuzugreifen und sie zu öffnen.*

1. Navigieren Sie zu dem Asset, das Sie auschecken möchten.
1. Klicken Sie mit der rechten Maustaste auf das Asset und wählen Sie im Kontextmenü die Option „More Assets Info“ (Weitere Asset-Informationen) aus.
1. Klicken/tippen Sie im Dialogfeld „Asset Info“ (Asset-Informationen) auf das Symbol „Auschecken“, um das Asset auszuchecken. Das Symbol „Auschecken“ wird zum Symbol „Einchecken“, nachdem Sie darauf geklickt/getippt haben.

   ![Zum Asset navigieren um auszuchecken](assets/browse_assets_to_checkout.png)

1. Wenn Sie das Asset einchecken möchten, sodass es für andere Benutzer verfügbar ist, klicken/tippen Sie im Dialogfeld „Asset Info“ (Asset-Informationen) auf das Symbol „Einchecken“.

### Auschecken von Assets unter Windows {#check-out-assets-on-windows}

Mithilfe des Programms können Sie Dateien auschecken, damit andere Benutzer keine Änderungen an den Dateien vornehmen können, an denen Sie gerade arbeiten.

1. Wählen Sie im Kontextmenü die Option „Explore Assets“ (Assets durchsuchen), um Explorer zu öffnen.
1. Navigieren Sie in Explorer zum Speicherort des Assets, das Sie auschecken möchten.
1. Klicken Sie mit der rechten Maustaste auf das Asset und wählen Sie aus dem Kontextmenü die Option „Open on Web“ (Im Web öffnen) aus.
1. Klicken/tippen Sie im Dialogfeld „Asset Info“ (Asset-Informationen) auf das Symbol „Checkout“ (Auschecken). Das Symbol „Auschecken“ wird zum Symbol „Einchecken“

   ![Symbol „Auschecken“](assets/checkout_icon_toggles.png)

1. Prüfen Sie das Asset in Explorer. Das Sperrsymbol auf dem Asset ![Asset-Sperrsymbol](assets/do-not-localize/aemassets_icon_lockcheckout.png) gibt an, dass Sie das Asset ausgecheckt haben.

   >[!NOTE]
   >
   >Das Schlosssymbol wird möglicherweise mit einiger Verzögerung angezeigt. [!DNL Experience Manager] Die Desktop-App speichert die Assets für schnellen Zugriff zwischen, sodass es einige Augenblicke dauern kann, den gesperrten Status zu aktualisieren.

1. Wenn Sie das Asset einchecken möchten, sodass es für andere Benutzer verfügbar ist, klicken/tippen Sie im Dialogfeld **Asset Info** (Asset-Informationen) auf das Symbol „Einchecken“.

### Einchecken eines Assets mit Finder oder Explorer und der Web-Benutzeroberfläche  {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

Wenn Sie mit dem Bearbeiten der Assets fertig sind, speichern Sie sie in Ihrem Desktop-Programm. Wählen Sie im Kontextmenü die Option **Weitere Asset-Informationen** aus und klicken/tippen Sie auf „Einchecken“.

Die Assets werden auf den Server [!DNL Experience Manager] hochgeladen. Optional können Sie den Status des Uploads überprüfen, indem Sie unter dem Ablagesymbol die Option **Asset-Status anzeigen** auswählen. Alternativ können Sie ein Asset über die [!DNL Experience Manager]-Weboberfläche einchecken. Klicken Sie auf die ausgecheckten Assets oder wählen Sie sie aus. Klicken Sie in der Symbolleiste auf das Symbol ![Einchecken](assets/do-not-localize/aemassets_icon_checkin.png).

Ein Asset wird automatisch nach [!DNL Experience Manager] hochgeladen, nachdem alle Änderungen lokal gespeichert wurden. Durch das Einchecken wird das Asset anderen [!DNL Experience Manager]-Benutzern zur Bearbeitung zur Verfügung gestellt.

### Massen-Upload von Assets und Ordnern auf [!DNL Experience Manager] Server {#bulkupload}

Mit der Desktop-App [!DNL Experience Manager] können Sie einen gesamten Ordner hochladen, der Elemente aus Ihrem lokalen Dateiverzeichnis enthält, in [!DNL Assets]. Auf diese Weise werden alle Assets innerhalb des Ordners gemeinsam hochgeladen und Sie müssen sie nicht einzeln hochladen.

1. Klicken/tippen Sie in der Symbolleiste der Assets-Benutzeroberfläche auf **Erstellen** und wählen Sie die Option **Ordner hochladen** aus dem Menü aus.
1. Navigieren Sie zu dem Ordner, den Sie hochladen möchten, und wählen Sie ihn aus.
1. Klicken/tippen Sie auf „OK“. Im Dialogfeld „Asset Status“ (Asset-Status) wird der Status des Uploads angezeigt.

   ![Status des Uploads im Fenster „Assets Status“ anzeigen](assets/aem_desktopapp_bulkupload_status.png)

   Status des Uploads im Fenster „Assets Status“ anzeigen

   >[!NOTE]
   >
   >Sie können den Upload manuell pausieren oder abbrechen, indem Sie auf das entsprechende Symbol klicken/tippen.

1. Wenn der Upload abgeschlossen ist, schließen Sie das Dialogfeld und navigieren Sie zur Assets-Benutzeroberfläche. Der hochgeladene Ordner wird in der Web-Benutzeroberfläche angezeigt.

Adobe empfiehlt nicht, eine größere Anzahl von Dateien oder verschachtelten Ordnern aus dem lokalen Dateisystem zu kopieren und in den Freigabebereich des Netzwerks einzufügen. Das Programm kann den Upload-Vorgang aufgrund technischer Einschränkungen nicht steuern und die Leistung ist schlecht.

Alternativ können Sie Dateien/Ordner, die Sie in [!DNL Experience Manager] hochladen möchten, im Finder oder Explorer auswählen, sie in die Systemzwischenablage kopieren, zum Ordner &quot;Zielgruppe&quot;im Bereich &quot;Network Share&quot;navigieren und im Kontextmenü der Desktop-App [!DNL Experience Manager] **Assets einfügen** wählen. Auf diese Weise laden [!DNL Experience Manager] Desktop-App-Beginn die eingefügten Assets hoch, ähnlich wie die Option **Ordner hochladen**, die in der [!DNL Experience Manager]-Weboberfläche verfügbar ist.

>[!MORELIKETHIS]
>
>* [ [!DNL Experience Manager] Fehlerbehebung bei der Anwendung der Desktop-App](troubleshoot-app-v1.md)

