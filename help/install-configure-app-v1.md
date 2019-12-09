---
title: Installieren und Konfigurieren der AEM-Desktop-App, Version 1.x
description: Installieren und konfigurieren Sie die AEM-Desktop-App, Version 1.x, um mit AEM Assets-Servern zu arbeiten und die Assets für die Bereitstellung als Laufwerk auf Ihrem Desktop zuzuordnen.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ad5337c8e1697d0a37d3020d25802dc1d732f320

---


# Installieren und Konfigurieren der AEM-Desktop-App, v1.x {#install-and-configure-aem-desktop-app}

Installieren und konfigurieren Sie die AEM-Desktop-App für die Verwendung mit AEM Assets-Servern und laden Sie die Assets in Ihr lokales Dateisystem herunter. Wenn Sie die AEM-Desktop-App verwenden möchten,

* stellen Sie sicher, dass Ihre AEM-Server-Version von der AEM-Desktop-App unterstützt wird. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).
* Laden Sie die Applikation herunter und installieren Sie sie.
* Testen Sie die Verbindung mithilfe einiger Assets. Siehe [Zugreifen auf und Öffnen von Assets über den Desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

Detaillierte Informationen finden Sie unter [AEM-Desktop-App – Versionshinweise](release-notes-of-v1.md).

## Installieren der AEM-Desktop-App und Verbinden mit dem AEM-Server {#install-and-connect-aem-desktop-app-to-aem-server}

Einzelheiten dazu finden Sie unter [Installieren der AEM-Desktop-App und Verbinden mit dem AEM-Server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Es kann immer nur eine Instanz der AEM-Desktop-App installiert und aktiv sein.

## Proxy-Unterstützung {#proxy-support}

Die AEM-Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Internet-Verbindung herzustellen. Die App kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie Proxyserver-Einstellungen für Windows konfigurieren oder ändern (Internetoptionen &gt; LAN-Einstellungen), starten Sie die AEM-Desktop-App neu, damit die Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von AEM Assets in den Proxyserver-Einstellungen der Whitelist hinzufügen, um den Applikationsdatenverkehr durchzulassen.

## Dateiverarbeitung {#file-handling}

Beim Ändern einer Datei unter einem von der Desktop-App bereitgestellten Netzwerkfreigabe-Speicherort werden die Dateien in zwei Phasen in diesem Verzeichnis gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In der zweiten Phase lädt die Desktop-App die aktualisierte Datei nach einer festgelegten Verzögerung (z. B. 30 Sek.) auf den AEM-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in AEM Assets.
1. Klicken/tippen Sie in der Symbolleiste auf das Symbol „AEM-Desktop-App“.
1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.
1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>Die AEM-Desktop-App kann Assets mit einer Größe von bis zu 40 GB verarbeiten.

## Herstellen einer Verbindung mit einer AEM-Instanz hinter einem Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Die Kopieren- und Verschieben-Methoden in der Assets-API erfordern, dass die folgenden zusätzlichen Header an AEM übergeben werden:

* X-Ziel
* X-Tiefe
* X-Überschreiben

AEM Desktop stellt Verbindungen mit AEM über eine URL her, die einen standardmäßigen Port enthält. Daher sollte die Einstellung `virtualhosts` in der Dispatcher-Konfiguration die standardmäßige Port-Nummer enthalten. For more information around `virtualhosts` configuration, see [Identifying Virtual Hosts](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts).

Weitere Informationen zum Konfigurieren des Dispatchers, sodass diese zusätzlichen Header übermittelt werden können, finden Sie unter [Festlegen der HTTP-Header](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders).

## Anpassen des Dialogfelds „Asset Info“{#customize-the-asset-info-dialog}

Sie können das Dialogfeld „Asset Info“ (Asset-Informationen) anpassen, indem Sie es mit mindestens einer dieser beiden Komponenten überlagern:

* Seite der Granite-Benutzeroberfläche unter `/libs/dam/gui/content/assets/moreinfo`
* HTL-Komponente `/css/javascript` unter `/libs/dam/gui/components/admin/moreinfo`

Welche Komponente überlagert wird, hängt von der Art der Personalisierung ab. Wenn Sie die Komponenten ändern möchten, die als Teil des Dialogfelds „Asset Info“ angezeigt werden, überlagern Sie die Seite der Granite-Benutzeroberfläche. Um den HTML/CSS/Javascript-Inhalt des Dialogfelds zu ändern, überlagern Sie die HTL-Komponente.

## Verwalten des Cache  {#manage-cache}

In Windows befindet sich der Cache unter `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, wo eine codierte Version des in der Desktop-App konfigurierten AEM-Hosts gespeichert ist. Beispiel: `http://localhost:4502` wird als `http%3A%2F%2Flocalhost%3A4502%2F` angezeigt.

Unter Mac OS X befindet sich unter `~/Library/Group Containers/group.com.adobe.aem.desktop/cache` ein ähnliches Verzeichnis.

### Option zum Verwalten des Cache in der App {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom AEM Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Klicken Sie zum Festlegen der gewünschten Optionen auf das Symbol der Applikation und klicken Sie auf **[!UICONTROL Advanced]** &gt; **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Assets, die nicht auf dem AEM-Server eingecheckt wurden, werden beibehalten und nicht gelöscht.

### Ändern des Cache-Verzeichnisses unter Windows  {#change-location-of-cache-on-windows}

Der Standardspeicherort des Caches für die AEM-Desktop-App lautet:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`
* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` ist die konfigurierte AEM-Endpunkt-URL der AEM-Desktop-App. Der Wert ist eine codierte Version der Ziel-URL für den AEM-Server. Wenn das Ziel der Applikation beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cache-Verzeichnis in diesem Beispiel lautet „%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502“.

Um die App auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei der Applikation.

1. Navigieren Sie zum Installationsverzeichnis der App. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.
1. Bearbeiten Sie die Datei „Adobe Experience Manager Desktop.exe.config“ mit einem Texteditor.

   Zum Speichern von an dieser Datei vorgenommenen Änderungen sind Administratorberechtigungen erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot“. Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis „%LocalAppData%\Adobe\AssetsCompanion\Cache“ festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >Die App erstellt automatisch ein Unterverzeichnis mit der Bezeichnung *&lt;Codierter AEM-Endpunkt&gt;*. Dieses Verhalten kann nicht konfiguriert werden.

## Zusätzliche Ressourcen {#additional-resources}

* [Einführung in die AEM-Desktop-App](https://helpx.adobe.com/experience-manager/kt/eseminars/ccoo-aem-desktop-app.html)
* [Verwenden der AEM-Desktop-App](use-app-v1.md)

* [Grundlegendes zum Ein- und Auschecken mit der AEM-Desktop-App](https://helpx.adobe.com/experience-manager/kt/assets/using/checkin-checkout-technical-video-understand.html)
* [Verwenden der Desktop-App mit AEM Assets](https://helpx.adobe.com/experience-manager/kt/assets/using/checkin-checkout-technical-video-understand.html)
* [Fehlerbehebung für die AEM-Desktop-App](troubleshoot-app-v1.md)