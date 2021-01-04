---
title: Installieren und Konfigurieren des  [!DNL Experience Manager] -Desktop-Programms, Version 1.x
description: Installieren und konfigurieren Sie  [!DNL Experience Manager] desktop app version 1.x to work with [!DNL Assets] -Server und ordnen Sie die Assets für die Bereitstellung als Laufwerk auf Ihrem Desktop zu.
translation-type: tm+mt
source-git-commit: a25c1fa13895ae9eb7268e3e01c83a5f0b9d7d1d
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 100%

---


# Installieren und Konfigurieren des [!DNL Experience Manager]-Desktop-Programms, v1.x {#install-and-configure-aem-desktop-app}

Mithilfe des [!DNL Experience Manager]-Desktop-Programms können Sie über Ihren lokalen Desktop problemlos auf die Assets in [!DNL Experience Manager] zugreifen und sie in beliebigen Desktop-Applikationen verwenden. Assets können in Mac Finder oder Windows Explorer leicht angezeigt, in Desktop-Applikationen geöffnet und lokal geändert werden. Die Änderungen werden beim Upload dann wieder unter einer neuen, im Repository erstellten Version in [!DNL Experience Manager] gespeichert.

Dank dieser Integration können unterschiedliche Rollen in der Organisation die Assets in Assets zentral verwalten und in Creative Cloud und anderen Programmen darauf zugreifen. Gleichzeitig können diverse Standards einschließlich Branding-Vorgaben leichter eingehalten werden.

Wenn Sie das [!DNL Experience Manager]-Desktop-Programm verwenden möchten,

* stellen Sie sicher, dass Ihre [!DNL Experience Manager]-Server-Version vom [!DNL Experience Manager]-Desktop-Programm unterstützt wird. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Laden Sie das Programm herunter und installieren Sie es.

* Testen Sie die Verbindung mithilfe einiger Assets. Siehe [Zugreifen auf und Öffnen von Assets über den Desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

Detaillierte Informationen finden Sie in den Versionshinweisen zum [[!DNL Experience Manager] -Desktop-Programm](release-notes-of-v1.md).

## Installieren und Verbinden des Programms mit dem [!DNL Experience Manager]-Server {#install-and-connect-aem-desktop-app-to-aem-server}

Weitere Informationen finden Sie unter [Installieren und Verbinden des  [!DNL Experience Manager] desktop app to [!DNL Experience Manager] -Servers](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Es kann immer nur eine Instanz des [!DNL Experience Manager]-Desktop-Programms installiert und aktiv sein.

## Dateiverarbeitung {#file-handling}

Beim Ändern einer Datei unter einem vom Desktop-Programm bereitgestellten Netzwerkfreigabe-Speicherort werden die Dateien in zwei Phasen in diesem Verzeichnis gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In der zweiten Phase lädt das Desktop-Programm die aktualisierte Datei nach einer festgelegten Verzögerung (z. B. 30 Sek.) auf den [!DNL Experience Manager]-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in Assets.

1. Klicken Sie in der Symbolleiste auf das Symbol für das [!DNL Experience Manager]-Desktop-Programm.

1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.

1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>Das [!DNL Experience Manager]-Desktop-Programm kann Assets mit einer Größe von bis zu 40 GB verarbeiten.

## Herstellen einer Verbindung mit einer [!DNL Experience Manager]-Instanz hinter einem Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Für die Methoden zum Kopieren und Verschieben in der Assets-API ist es erforderlich, dass die folgenden Header an [!DNL Experience Manager] weitergeleitet werden:

* X-Ziel
* X-Tiefe
* X-Überschreiben

[!DNL Experience Manager]-Desktop stellt Verbindungen mit [!DNL Experience Manager] über eine URL her, die einen standardmäßigen Port enthält. Daher sollte die Einstellung `virtualhosts` in der Dispatcher-Konfiguration die standardmäßige Port-Nummer enthalten. Weitere Informationen zur Konfiguration von `virtualhosts` finden Sie unter [Identifizieren von virtuellen Hosts](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#identifying-virtual-hosts-virtualhosts).

Weitere Informationen zum Konfigurieren des Dispatchers, sodass diese zusätzlichen Header übermittelt werden können, finden Sie unter [Festlegen der HTTP-Header](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxy-Unterstützung {#proxy-support}

Das [!DNL Experience Manager]-Desktop-Programm verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Internet-Verbindung herzustellen. Das Programm kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie Proxyserver-Einstellungen für Windows konfigurieren oder ändern (Internetoptionen > LAN-Einstellungen), starten Sie das [!DNL Experience Manager]-Desktop-Programm neu, damit die Änderungen wirksam werden.

>[!NOTE]
>
>Proxy-Konfiguration wird nur angewendet, wenn Sie das Desktop-Programm starten. Schließen Sie das Programm und starten Sie es erneut, damit Änderungen wirksam werden.

Wenn für den Proxy eine Authentifizierung erforderlich ist, kann die IT-Abteilung die URL von Experience Manager Assets in den Proxyserver-Einstellungen zulassen, um den Applikationsdatenverkehr durchzulassen.

## Anpassen des Dialogfelds „Asset Info“ {#customize-the-asset-info-dialog}

Sie können das Dialogfeld „Asset Info“ (Asset-Informationen) anpassen, indem Sie es mit mindestens einer dieser beiden Komponenten überlagern:

* Seite der Granite-Benutzeroberfläche unter `/libs/dam/gui/content/assets/moreinfo`.

* HTL-Komponente `/css/javascript` unter `/libs/dam/gui/components/admin/moreinfo`.

Welche Komponente überlagert wird, hängt von der Art der Personalisierung ab. Wenn Sie die Komponenten ändern möchten, die als Teil des Dialogfelds „Asset Info“ angezeigt werden, überlagern Sie die Seite der Granite-Benutzeroberfläche. Um den HTML-, CSS- oder JavaScript-Inhalt des Dialogfelds zu ändern, überlagern Sie die HTL-Komponente.

## Verwalten des Caches {#manage-cache}

In Windows befindet sich der Cache unter `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, wo eine kodierte Version des im Desktop-Programm konfigurierten [!DNL Experience Manager]-Hosts gespeichert ist. Beispiel: `http://localhost:4502` wird als `http%3A%2F%2Flocalhost%3A4502%2F` angezeigt.

Unter Mac OS X befindet sich unter `~/Library/Group Containers/group.com.adobe.aem.desktop/cache` ein ähnliches Verzeichnis.

### Option zum Verwalten des Cache im Programm {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Klicken Sie zum Festlegen der gewünschten Optionen auf das Symbol des Programms und klicken Sie auf **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**.

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Elemente, die nicht auf dem [!DNL Experience Manager]-Server eingecheckt wurden, werden beibehalten und nicht gelöscht.

### Ändern des Cache-Verzeichnisses unter Windows  {#change-location-of-cache-on-windows}

Der Standardspeicherort des Caches für das [!DNL Experience Manager]-Desktop-Programm lautet:

* Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`

* Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` ist die konfigurierte [!DNL Experience Manager]-Endpunkt-URL des Programms. Der Wert ist eine kodierte Version der Ziel-URL für den [!DNL Experience Manager]-Server. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cache-Verzeichnis in diesem Beispiel lautet `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Um das Programm auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei des Programms.

1. Navigieren Sie zum Installationsverzeichnis des Programms. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bearbeiten Sie die Datei „Adobe Experience Manager Desktop.exe.config“ mit einem Texteditor.

   Zum Speichern von an dieser Datei vorgenommenen Änderungen sind Administratorberechtigungen erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot“. Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis `%LocalAppData%\Adobe\AssetsCompanion\Cache` festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >Das Programm erstellt automatisch ein Unterverzeichnis mit der Bezeichnung *&lt;Encoded AEM Endpoint>*. Dieses Verhalten kann nicht konfiguriert werden.

>[!MORELIKETHIS]
* [Einführung in das  [!DNL Experience Manager] -Desktop-Programm](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html?lang=de).
* [Verwenden des  [!DNL Experience Manager] -Desktop-Programms](use-app-v1.md).
* [Fehlerbehebung für das  [!DNL Experience Manager] -Desktop-Programm](troubleshoot-app-v1.md).

