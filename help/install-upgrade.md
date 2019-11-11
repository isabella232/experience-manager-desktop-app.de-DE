---
title: Installieren und Konfigurieren der AEM Desktop-App
seo-title: Installieren und Konfigurieren der AEM Desktop-App
description: Installieren und konfigurieren Sie die AEM-Desktop-App für die Verwendung mit AEM Assets-Servern und laden Sie die Assets auf Ihr lokales Dateisystem herunter.
seo-description: Installieren und konfigurieren Sie die AEM-Desktop-App für die Verwendung mit AEM Assets-Servern und laden Sie die Assets auf Ihr lokales Dateisystem herunter.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: Agupta
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a46660a3d56100e0d767e7f2b54656782bb5e7a7

---


# Installieren der AEM-Desktop-App {#install-app-v2}

## Systemanforderungen {#tech-specs-v2}

For detailed information, see the [AEM desktop app release notes](release-notes.md).

## Von App v1.x auf App v2 aktualisieren {#upgrade-from-previous-version}

Wenn Sie bereits Benutzer der App sind, sollten Sie die Unterschiede und Ähnlichkeiten zwischen der vorherigen und der neuesten Version der App kennen. Befolgen Sie außerdem die folgenden Richtlinien, um von v1.x zur neuesten Version zu wechseln.

>[!NOTE]
>
>Die Desktop-App v1.x und v2 können auf einem Computer nicht nebeneinander bestehen. Deinstallieren Sie vor der Installation einer Version die andere Version.

Gehen Sie wie folgt vor, um von v1.x auf die neueste Version der App zu aktualisieren:

1. Synchronisieren Sie vor dem Upgrade alle Assets. Laden Sie alle Änderungen mit App v1.x hoch. Dadurch soll vermieden werden, dass Änderungen beim Deinstallieren der App v1.x verloren gehen.
1. Deinstallieren Sie die App v1.x. Löschen Sie bei der Deinstallation von v1.x den Cache.
1. Starten Sie den Computer neu.
1. Laden Sie die neueste App herunter und installieren Sie sie. Befolgen Sie die unten stehenden Anweisungen.

## Installieren von {#install-v2}

Gehen Sie wie folgt vor, um die Desktop-App zu installieren. Deinstallieren Sie alle vorhandenen Adobe Experience Manager Desktop-Apps der Version 1.x, bevor Sie die neueste App installieren. Weitere Informationen finden Sie oben.

1. Halten Sie die URL und die Anmeldeinformationen Ihrer AEM-Bereitstellung bereit.
1. Überspringen Sie diesen Schritt, wenn Sie AEM 6.4.4 oder höher oder AEM 6.5.0 oder höher verwenden. Stellen Sie sicher, dass Ihr AEM-Setup die in den Versionshinweisen erwähnten Kompatibilitätsanforderungen erfüllt. Laden Sie bei Bedarf das entsprechende [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) herunter und installieren Sie es mit AEM Package Manager als AEM-Administrator. To install a package, see [How to work with Packages](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).
1. Führen Sie die Binärdatei des Installationsprogramms aus und befolgen Sie die Anweisungen auf dem Bildschirm, um die Installation durchzuführen.
1. Unter Windows wird das Installationsprogramm möglicherweise zur Installation aufgefordert `Visual Studio C++ Redistributable 2015`. Folgen Sie den Anweisungen auf dem Bildschirm, um es zu installieren. Wenn die Installation fehlschlägt, installieren Sie sie manuell. Laden Sie das Installationsprogramm [hier](https://www.microsoft.com/en-us/download/details.aspx?id=52685) herunter und installieren Sie sowohl `vc_redist.x64.exe` als auch `vc_redist.x86.exe` Dateien. Führen Sie das Installationsprogramm für die AEM Desktop-App erneut aus.
1. Starten Sie den Computer nach Aufforderung neu. Starten Sie die Desktop-App, um sie zu konfigurieren.
1. Um die App mit einem AEM-Repository zu verbinden, klicken Sie auf das App-Symbol in der Ablage, um die App zu starten. Geben Sie die Adresse der AEM-Instanz ein. Klicken Sie auf **[!UICONTROL Connect]** und geben Sie die Anmeldeinformationen ein.

   ![Verbindungsbildschirm der Desktop-App mit dem](assets/connect_da2.png "Adressbildschirm des Eingabeservers zur Adresse des Eingabeservers")

   >[!Caution]
   >
   >Stellen Sie sicher, dass vor oder nach der Adresse des AEM-Servers keine führenden oder nachfolgenden Leerzeichen vorhanden sind. Andernfalls kann die App keine Verbindung zum AEM-Server herstellen.

1. Nach erfolgreicher Verbindung können Sie die Liste der Ordner und Assets anzeigen, die im Stammordner von AEM DAM verfügbar sind. Sie können die Ordner in der App durchsuchen.

   ![Bei Anmeldung zeigt die App den DAM-](assets/firstview_da2.png "Inhalt anBei Anmeldung zeigt die App den DAM-Inhalt an")

1. (AEM 6.5.1 oder höher) Wenn Sie eine Desktop-App mit AEM 6.5.1 oder höher verwenden, aktualisieren Sie den S3- oder Azurblauer Connector auf Version 1.10.4 oder höher. Siehe [Azurblauer Stecker](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AzureDataStore) oder [S3-Stecker](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AmazonS3DataStore).

   Wenn Sie Adobe Managed Services (AMS)-Kunde sind, wenden Sie sich an den Adobe-Kundendienst.

## Voreinstellungen festlegen {#set-preferences}

Um die Voreinstellungen zu ändern, klicken Sie auf das Symbol![ " ](assets/do-not-localize/more_options_da2.png)Weitere Optionen"und auf das Symbol " **[!UICONTROL Preference]** Voreinstellungen"![](assets/do-not-localize/preferences_icon_da2.png). Passen Sie die Werte im **[!UICONTROL Preferences]** Fenster wie folgt an:

* [!UICONTROL Launch application on login].
* [!UICONTROL Show window when application starts].
* **[!UICONTROL Cache Directory]**: Speicherort des lokalen Cache der App (enthält die lokal heruntergeladenen Assets).
* **[!UICONTROL Network Drive Letter]**: Der Laufwerksbuchstabe, der für die Zuordnung zu AEM DAM verwendet wird. Ändern Sie dies nicht, wenn Sie sich nicht sicher sind. Die App kann jedem Laufwerksbuchstaben unter Windows zugeordnet werden. Wenn zwei Benutzer Assets aus unterschiedlichen Laufwerksbuchstaben platzieren, können sie die Assets nicht voneinander sehen. Der Pfad der Assets ändert sich. Die Assets bleiben in der Binärdatei (z. B. INDD) und werden nicht entfernt. Die App listet alle verfügbaren Laufwerksbuchstaben auf und verwendet standardmäßig den zuletzt verfügbaren Brief, der normalerweise `Z`verfügbar ist.
* **[!UICONTROL Maximum Cache Size]**: Zulässiger Cache auf der Festplatte in GB zum Speichern lokal heruntergeladener Assets.
* **[!UICONTROL Current cache size]**: Speichergröße der lokal heruntergeladenen Assets. Die Informationen werden erst angezeigt, nachdem Assets mit der App heruntergeladen wurden.
* **[!UICONTROL Automatically download linked assets]**: Die Assets, die in den unterstützten nativen Creative Cloud-Apps platziert werden, werden automatisch abgerufen, wenn Sie die Originaldatei herunterladen.
* **[!UICONTROL Maximum number of downloads]**: Beim erstmaligen Herunterladen von Assets (über die Option "Anzeigen", "Öffnen", "Bearbeiten", "Herunterladen"oder Ähnliches) werden die Assets nur heruntergeladen, wenn der Stapel weniger als diese Zahl enthält. Der Standardwert ist 50. Ändern Sie sich nicht, wenn Sie sich nicht sicher sind. Eine Erhöhung des Werts kann zu längeren Wartezeiten führen, und eine Verringerung des Werts ermöglicht es Ihnen möglicherweise nicht, die erforderlichen Assets oder Ordner in einem Schritt herunterzuladen.

Um die nicht verfügbaren Voreinstellungen zu aktualisieren, melden Sie sich beim AEM-Server ab. Nachdem Sie die Voreinstellungen aktualisiert haben, klicken Sie auf Voreinstellungen ![speichern](assets/do-not-localize/save_preferences_da2.png) , um die Änderungen zu speichern.

![Voreinstellungen und](assets/preferences_da2.png "Einstellungen für AEM Desktop-Apps")

## Deinstallieren der App {#uninstall-the-app}

Gehen Sie wie folgt vor, um die Anwendung unter Windows zu deinstallieren:

1. Laden Sie alle Änderungen auf AEM hoch, um Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in AEM](using.md#edit-assets-upload-updated-assets). Melden Sie sich ab und [!UICONTROL Exit] die App.
1. Entfernen Sie die App, während Sie eine andere OS-Anwendung entfernen. Deinstallieren Sie sie unter "Programme hinzufügen"und entfernen Sie sie unter Windows.
1. Um den Cache und die Protokolle zu entfernen, aktivieren Sie das entsprechende Kontrollkästchen.
   ![Deinstallationsdialogfeld zum Entfernen von Protokollen und](assets/uninstall_da2.png "CacheDeinstallationsdialogfeld zum Entfernen von Protokollen und Zwischenspeichern")
1. Befolgen Sie die Anweisungen auf dem Bildschirm. Starten Sie nach Abschluss des Vorgangs den Computer neu.

Gehen Sie wie folgt vor, um die Anwendung unter Mac zu deinstallieren:

1. Laden Sie alle Änderungen auf AEM hoch, um Änderungen zu vermeiden. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in AEM](using.md#edit-assets-upload-updated-assets). Melden Sie sich ab und [!UICONTROL Exit] die App.
1. Entfernen Sie den `Adobe Experience Manager Desktop.app` Inhalt `/Applications`.

Alternativ können Sie den folgenden Befehl im Terminal ausführen, um interne Anwendungs-Caches auf dem Mac zu löschen und die App zu deinstallieren:
`/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh`
