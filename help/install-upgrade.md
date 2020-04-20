---
title: Installieren und Konfigurieren des Adobe Experience Manager-Desktop-Programms
description: Installieren und konfigurieren Sie das Adobe Experience Manager-Desktop-Programm für die Verwendung mit Adobe Experience Manager Assets-Servern und laden Sie die Assets in Ihr lokales Dateisystem herunter.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0301538b5cc00a187709b484bed8f0ca7b799f03

---


# Installieren des Adobe Experience Manager-Desktop-Programms {#install-app-v2}

Mit der Adobe Experience Manager-Desktop-App sind die Assets in Experience Manager einfach auf Ihrem lokalen Desktop verfügbar und können in allen nativen Desktop-Anwendungen verwendet werden. Assets können in der Vorschau angezeigt, in nativen Desktop-Anwendungen geöffnet, in Mac Finder oder Windows Explorer zur Platzierung in anderen Dokumenten angezeigt und lokal geändert werden. Die Änderungen werden beim Hochladen in Experience Manager gespeichert und eine neue Version wird im Repository erstellt.

Eine solche Integration ermöglicht es verschiedenen Rollen in der Organisation,

* Verwalten Sie die Assets zentral in Experience Manager Assets.
* Greifen Sie auf die Assets in allen nativen Desktop-Anwendungen zu, einschließlich Anwendungen von Drittanbietern und in der Adobe Creative Cloud. Dabei können die Benutzer die verschiedenen Standards, einschließlich des Branding, problemlos einhalten.

Stellen Sie zur Verwendung des Experience Manager-Desktop-Programms sicher,

* Stellen Sie sicher, dass Ihre Experience Manager-Version von der Experience Manager-Desktop-App unterstützt wird. Siehe die [Systemanforderungen](release-notes.md#system-requirements-and-prerequisites-v2) unten.
* Laden Sie das Programm herunter und installieren Sie es. Siehe [Installieren der Desktop-App](#install-v2) unten.
* Testen Sie die Verbindung mithilfe einiger Assets. Erfahren Sie, [wie Sie Assets](using.md#browse-search-preview-assets)durchsuchen und suchen.

## Systemanforderungen, Voraussetzungen und Download-Links {#tech-specs-v2}

Detaillierte Informationen finden Sie unter [Versionshinweise zum Adobe Experience Manager-Desktop-Programm](release-notes.md).

## Upgrade from a previous version {#upgrade-from-previous-version}

Wenn Sie Benutzer der Version 1.x der Desktop-App sind, sollten Sie die Unterschiede und Ähnlichkeiten zwischen der vorherigen und der neuesten Version der App kennen. [Neue Funktionen in der Desktop-App](introduction.md#whats-new-v2) und [Funktionsweise der App](release-notes.md#how-app-works)

>[!NOTE]
>
>Zwei Versionen der Desktop-App können auf einem Computer nicht nebeneinander bestehen. Deinstallieren Sie vor der Installation einer Version die andere Version.

Gehen Sie wie folgt vor, um eine Aktualisierung von einer früheren Version der App durchzuführen:

1. Synchronisieren Sie vor dem Upgrade alle Assets und laden Sie Ihre Änderungen in Experience Manager hoch. Dadurch soll vermieden werden, dass Änderungen beim Deinstallieren der App verloren gehen.
1. Deinstallieren Sie die vorherige Version der App. Wählen Sie bei der Deinstallation die Option zum Löschen des Cache.
1. Starten Sie den Computer neu.
1. [Laden Sie die neueste Version des Programms herunter und installieren Sie sie.](release-notes.md)[](#install-v2) Befolgen Sie die unten stehenden Anweisungen.

## Installieren {#install-v2}

Gehen Sie wie folgt vor, um das Desktop-Programm zu installieren. Deinstallieren Sie ein eventuell vorhandenes Adobe Experience Manager-Desktop-Programm v1.x, bevor Sie die neueste Version des Programms installieren. Weitere Informationen finden Sie oben.

1. Laden Sie das neueste Installationsprogramm von der Seite mit den [Versionshinweisen](release-notes.md) herunter.
1. Halten Sie die URL und die Anmeldeinformationen Ihrer Experience Manager-Bereitstellung bereit.
1. Wenn Sie ein Upgrade von einer anderen Version der App durchführen, finden Sie weitere Informationen unter [Aktualisieren der Desktop-App](#upgrade-from-previous-version).
1. Überspringen Sie diesen Schritt, wenn Sie Experience Manager als Cloud-Dienst, Experience Manager 6.4.4 oder höher oder Experience Manager 6.5.0 oder höher verwenden. Ensure that your Experience Manager setup meets the compatibility requirements mentioned in the [release notes](release-notes.md). If necessary, download the applicable [compatibility package](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) and install it using the Experience Manager Package Manager as an Experience Manager administrator. Weitere Informationen zur Installation eines Pakets finden Sie unter [Arbeiten mit Paketen](https://helpx.adobe.com/de/experience-manager/6-5/sites/administering/using/package-manager.html).
1. Führen Sie die Binärdatei des Installationsprogramms aus und befolgen Sie die Anweisungen auf dem Bildschirm, um die Installation durchzuführen.
1. Unter Windows werden Sie vom Installationsprogramm möglicherweise zur Installation von `Visual Studio C++ Redistributable 2015` aufgefordert. Folgen Sie den Anweisungen auf dem Bildschirm, um es zu installieren. Wenn die Installation fehlschlägt, installieren Sie es manuell. Laden Sie das Installationsprogramm [hier](https://www.microsoft.com/de-de/download/details.aspx?id=52685) herunter und installieren Sie die Dateien `vc_redist.x64.exe` und `vc_redist.x86.exe`. Führen Sie das Installationsprogramm für das AEM-Desktop-Programm erneut aus.
1. Starten Sie den Computer nach Aufforderung neu. Starten und konfigurieren Sie die Desktop-App.
1. Um das Programm mit einem AEM-Repository zu verbinden, klicken Sie auf das Programmsymbol in der Ablage, um das Programm zu starten. Geben Sie die Adresse der AEM-Instanz ein. Klicken Sie auf **[!UICONTROL Connect]** und geben Sie die Anmeldeinformationen ein.

   ![Verbindungsbildschirm des Desktop-Programms zur Eingabe der Server-Adresse](assets/connect_da2.png "Verbindungsbildschirm zur Eingabe der Server-Adresse")

   >[!CVorsicht]
   >
   >Stellen Sie sicher, dass vor oder nach der Adresse des AEM-Servers keine führenden oder nachfolgenden Leerzeichen vorhanden sind. Andernfalls kann das Programm keine Verbindung zum AEM-Server herstellen.

1. Nach erfolgreicher Verbindung können Sie die Liste der Ordner und Assets anzeigen, die im Stammordner von AEM DAM verfügbar sind. Sie können die Ordner im Programm durchsuchen.

   ![Bei Anmeldung zeigt das Programm den DAM-Inhalt an](assets/firstview_da2.png "Bei Anmeldung zeigt das Programm den DAM-Inhalt an")

1. (Experience Manager 6.5.1 oder höher) Wenn Sie eine Desktop-App mit Experience Manager 6.5.1 oder höher verwenden, aktualisieren Sie den S3- oder Azurblase-Connector auf Version 1.10.4 oder höher. Siehe [Azure-Connector](https://helpx.adobe.com/de/experience-manager/6-5/sites/deploying/using/data-store-config.html#AzureDataStore) oder [S3-Connector](https://helpx.adobe.com/de/experience-manager/6-5/sites/deploying/using/data-store-config.html#AmazonS3DataStore).

   Wenn Sie Adobe Managed Services (AMS)-Kunde sind, wenden Sie sich an den Adobe-Kundendienst.

## Festlegen von Voreinstellungen {#set-preferences}

Um die Voreinstellungen zu ändern, klicken Sie auf das Symbol ![Weitere Optionen](assets/do-not-localize/more_options_da2.png) und auf das Symbol **[!UICONTROL Preference]**![ Voreinstellungen](assets/do-not-localize/preferences_icon_da2.png). Passen Sie die Werte im Fenster **[!UICONTROL Preferences]** wie folgt an:

* [!UICONTROL Launch application on login].
* [!UICONTROL Show window when application starts].
* **[!UICONTROL Cache Directory]**: Speicherort des lokalen Cache des Programms (enthält die lokal heruntergeladenen Assets).
* **[!UICONTROL Network Drive Letter]**: Der Laufwerksbuchstabe, der für die Zuordnung zu AEM DAM verwendet wird. Ändern Sie diesen Wert nur, wenn Sie sich absolut sicher sind. Das Programm kann jedem Laufwerksbuchstaben unter Windows zugeordnet werden. Wenn zwei Benutzer Assets aus unterschiedlichen Laufwerksbuchstaben platzieren, können sie die Assets des jeweils anderen nicht sehen. Der Pfad der Assets ändert sich. Die Assets bleiben in der Binärdatei (z. B. INDD) und werden nicht entfernt. Das Programm listet alle verfügbaren Laufwerksbuchstaben auf und verwendet standardmäßig den letzten verfügbaren Buchstaben, also meist `Z`.
* **[!UICONTROL Maximum Cache Size]**: Zulässiger Cache auf der Festplatte in GB zum Speichern lokal heruntergeladener Assets.
* **[!UICONTROL Current cache size]**: Speichergröße der lokal heruntergeladenen Assets. Die Informationen werden erst angezeigt, nachdem Assets mit dem Programm heruntergeladen wurden.
* **[!UICONTROL Automatically download linked assets]**: Die Assets, die in den unterstützten nativen Creative Cloud-Applikationen platziert wurden, werden automatisch abgerufen, wenn Sie die Originaldatei herunterladen.
* **[!UICONTROL Maximum number of downloads]**: Beim erstmaligen Herunterladen von Assets (über die Option „Anzeigen“, „Öffnen“, „Bearbeiten“, „Herunterladen“ usw.) werden die Assets nur heruntergeladen, wenn der Stapel weniger als diese Zahl enthält. Der Standardwert ist 50. Ändern Sie sie nicht, wenn Sie sich nicht sicher sind. Eine Erhöhung des Werts kann zu längeren Wartezeiten führen und eine Verringerung des Werts verhindert womöglich, dass Sie die erforderlichen Assets oder Ordner in einem Schritt herunterladen können.
* **[!UICONTROL Upload Acceleration]**: Beim Hochladen von Assets kann die Anwendung gleichzeitige Uploads verwenden, um die Upload-Geschwindigkeit zu verbessern. Sie können die Gleichzeitigkeit des Uploads erhöhen, indem Sie den Schieberegler nach rechts verschieben. Der Schieberegler ganz links bedeutet keine Parallelität (Upload mit nur einem Thread), die mittlere Position entspricht 10 parallelen Threads, und die maximale Grenze auf der rechten Seite entspricht 20 parallelen Threads. Eine höhere Parallelitätsgrenze erfordert einen höheren Ressourcenverbrauch des lokalen Prozessors.

Um die nicht verfügbaren Voreinstellungen zu aktualisieren, melden Sie sich beim AEM-Server ab. Nachdem Sie die Voreinstellungen aktualisiert haben, klicken Sie auf ![Voreinstellungen speichern](assets/do-not-localize/save_preferences_da2.png), um die Änderungen zu speichern.

![Voreinstellungen und Einstellungen für das AEM-Desktop-Programm](assets/preferences_da2.png "Einstellungen für das Desktop-Programm")

## Deinstallieren des Programms {#uninstall-the-app}

Gehen Sie wie folgt vor, um das Programm unter Windows zu deinstallieren:

1. Laden Sie alle Änderungen auf AEM hoch, um den Verlust von Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in AEM](using.md#edit-assets-upload-updated-assets). Melden Sie sich ab und beenden ([!UICONTROL Exit]) Sie das Programm.
1. Entfernen Sie das Programm so, wie Sie auch jede andere Applikation entfernen würden. Deinstallieren Sie sie unter Windows über „Programme hinzufügen und entfernen“.
1. Um den Cache und die Protokolle zu entfernen, aktivieren Sie das entsprechende Kontrollkästchen.
   ![Deinstallations-Dialogfeld zum Entfernen von Protokollen und Cache](assets/uninstall_da2.png "Deinstallations-Dialogfeld zum Entfernen von Protokollen und Cache")
1. Folgen Sie den angezeigten Anweisungen. Starten Sie nach Abschluss des Vorgangs den Computer neu.

Gehen Sie wie folgt vor, um das Programm auf einem Mac zu deinstallieren:

1. Laden Sie alle Änderungen auf AEM hoch, um den Verlust von Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in AEM](using.md#edit-assets-upload-updated-assets). Melden Sie sich ab und beenden ([!UICONTROL Exit]) Sie das Programm.
1. Entfernen Sie `Adobe Experience Manager Desktop.app` aus `/Applications`.

Alternativ können Sie den folgenden Befehl im Terminal ausführen, um interne Applikations-Caches auf dem Mac zu löschen und das Programm zu deinstallieren:
`/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh`
