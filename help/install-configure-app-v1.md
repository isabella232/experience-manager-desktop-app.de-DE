---
title: Install and configure [!DNL Experience Manager] desktop app version 1.x
description: Installieren und [!DNL Experience Manager] desktop app version 1.x to work with [!DNL Assets] konfigurieren Sie die Assets und ordnen Sie sie als Laufwerk auf Ihrem Desktop zu.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS,SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2893fc1f8aad02e1436a1a281a320e6837487220
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 62%

---


# Install and configure [!DNL Experience Manager] desktop app v1.x {#install-and-configure-aem-desktop-app}

Using the [!DNL Experience Manager] desktop app, the assets within [!DNL Experience Manager] are easily accessible on your local desktop and can be used in any desktop applications. Assets can be easily revealed in Mac Finder or Windows Explorer, opened in desktop applications, and changed locally – the changes are saved back to [!DNL Experience Manager] when you upload and a new version is created in the repository.

Dank dieser Integration können unterschiedliche Rollen in der Organisation die Assets in  Assets zentral verwalten und in Creative Cloud und anderen Applikationen darauf zugreifen. Gleichzeitig können diverse Standards einschließlich Branding-Vorgaben leichter eingehalten werden.

To use [!DNL Experience Manager] desktop app,

* Ensure that your [!DNL Experience Manager] server version is supported by [!DNL Experience Manager] desktop app. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Laden Sie das Programm herunter und installieren Sie es.

* Testen Sie die Verbindung mithilfe einiger Assets. Siehe [Zugreifen auf und Öffnen von Assets über den Desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

For detailed information, see the [[!DNL Experience Manager] desktop app release notes](release-notes-of-v1.md).

## Installieren und Verbinden der App mit dem [!DNL Experience Manager] Server {#install-and-connect-aem-desktop-app-to-aem-server}

Weitere Informationen finden Sie unter [Installieren und [!DNL Experience Manager] desktop app to [!DNL Experience Manager] Connectserver](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Only one instance of the [!DNL Experience Manager] desktop app can be installed and be active at a time.

## Dateiverarbeitung {#file-handling}

Beim Ändern einer Datei unter einem vom Desktop-Programm bereitgestellten Netzwerkfreigabe-Speicherort werden die Dateien in zwei Phasen in diesem Verzeichnis gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In the second phase, desktop app uploads the updated file to [!DNL Experience Manager] server after a predefined delay (for example, 30s). Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in  Assets.

1. Click the [!DNL Experience Manager] desktop app icon from the toolbar.

1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.

1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>[!DNL Experience Manager] Mit der Desktop-App können Assets mit einer Größe von bis zu 40 GB verarbeitet werden.

## Connect to an [!DNL Experience Manager] instance behind a dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

The copy and move methods in the Assets API require the following additional headers to be passed to [!DNL Experience Manager]:

* X-Ziel
* X-Tiefe
* X-Überschreiben

[!DNL Experience Manager] Der Desktop stellt eine Verbindung mit einer URL her, die den Standardanschluss enthält. [!DNL Experience Manager] Daher sollte die Einstellung `virtualhosts` in der Dispatcher-Konfiguration die standardmäßige Port-Nummer enthalten. Weitere Informationen zur Konfiguration von `virtualhosts` finden Sie unter [Identifizieren von virtuellen Hosts](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#identifying-virtual-hosts-virtualhosts).

Weitere Informationen zum Konfigurieren des Dispatchers, sodass diese zusätzlichen Header übermittelt werden können, finden Sie unter [Festlegen der HTTP-Header](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxy-Unterstützung {#proxy-support}

[!DNL Experience Manager] Die Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Verbindung mit dem Internet herzustellen. Das Programm kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

If you configure or modify proxy server settings for Windows (Internet Options > LAN Settings), restart the [!DNL Experience Manager] desktop app for the changes to take effect.

>[!NOTE]
>
>Proxy-Konfiguration wird nur angewendet, wenn Sie das Desktop-Programm starten. Schließen Sie das Programm und starten Sie es erneut, damit Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von Experience Manager Assets in den Proxyserver-Einstellungen zulassen, um den Applikationsdatenverkehr durchzulassen.

## Anpassen des Dialogfelds „Asset Info“ {#customize-the-asset-info-dialog}

Sie können das Dialogfeld „Asset Info“ (Asset-Informationen) anpassen, indem Sie es mit mindestens einer dieser beiden Komponenten überlagern:

* Seite der Granite-Benutzeroberfläche unter `/libs/dam/gui/content/assets/moreinfo`.

* HTL-Komponente `/css/javascript` unter `/libs/dam/gui/components/admin/moreinfo`.

Welche Komponente überlagert wird, hängt von der Art der Personalisierung ab. Wenn Sie die Komponenten ändern möchten, die als Teil des Dialogfelds „Asset Info“ angezeigt werden, überlagern Sie die Seite der Granite-Benutzeroberfläche. Um den HTML-, CSS- oder JavaScript-Inhalt des Dialogfelds zu ändern, überlagern Sie die HTML-Komponente.

## Verwalten des Caches {#manage-cache}

On Windows, the cache is at `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, where is an encoded version of the [!DNL Experience Manager] host configured in the desktop app. Beispiel: `http://localhost:4502` wird als `http%3A%2F%2Flocalhost%3A4502%2F` angezeigt.

Unter Mac OS X befindet sich unter `~/Library/Group Containers/group.com.adobe.aem.desktop/cache` ein ähnliches Verzeichnis.

### Option zum Verwalten des Cache im Programm {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Klicken Sie zum Festlegen der gewünschten Optionen auf das Symbol des Programms und klicken Sie auf **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**.

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Any assets not checked into [!DNL Experience Manager] server are retained and not deleted.

### Ändern des Cache-Verzeichnisses unter Windows {#change-location-of-cache-on-windows}

The default location of the cache for the [!DNL Experience Manager] desktop app is as follows:

* Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`

* Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` ist die konfigurierte [!DNL Experience Manager] Endpunkt-URL der App. The value is an encoded version of the targeting URL of the [!DNL Experience Manager] server. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cache-Verzeichnis in diesem Beispiel lautet `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Um das Programm auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei des Programms.

1. Navigieren Sie zum Installationsverzeichnis des Programms. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bearbeiten Sie die Datei „Adobe Experience Manager Desktop.exe.config“ mit einem Texteditor.

   Zum Speichern von an dieser Datei vorgenommenen Änderungen sind Administratorberechtigungen erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot“. Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis `%LocalAppData%\Adobe\AssetsCompanion\Cache` festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >Das Programm erstellt automatisch ein Unterverzeichnis mit der Bezeichnung *&lt;Encoded AEM Endpoint>*. Dieses Verhalten kann nicht konfiguriert werden.

>[!MORELIKETHIS]
* [Einführung [!DNL Experience Manager] in die Desktop-App](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html?lang=de).
* [Verwenden Sie die [!DNL Experience Manager] Desktop-App](use-app-v1.md).
* [ [!DNL Experience Manager] Fehlerbehebung bei der Desktop-App](troubleshoot-app-v1.md).

