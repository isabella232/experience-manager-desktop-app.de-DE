---
title: Installieren und konfigurieren Sie [!DNL Experience Manager] die Desktop-App-Version 1.x
description: 'Installieren und konfigurieren Sie die Server und ordnen Sie die Assets als Laufwerk auf Ihrem Desktop zu. [!DNL Experience Manager] desktop app version 1.x to work with [!DNL Assets] '
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


# [!DNL Experience Manager] Desktop-App v1.x {#install-and-configure-aem-desktop-app} installieren und konfigurieren

Mit der Desktop-App [!DNL Experience Manager] können die Elemente innerhalb von [!DNL Experience Manager] problemlos auf Ihrem lokalen Desktop aufgerufen werden und können in allen Desktop-Anwendungen verwendet werden. Assets können einfach in Mac Finder oder Windows Explorer angezeigt, in Desktop-Anwendungen geöffnet und lokal geändert werden - die Änderungen werden beim Hochladen auf [!DNL Experience Manager] zurückgespeichert und eine neue Version wird im Repository erstellt.

Dank dieser Integration können unterschiedliche Rollen in der Organisation die Assets in  Assets zentral verwalten und in Creative Cloud und anderen Applikationen darauf zugreifen. Gleichzeitig können diverse Standards einschließlich Branding-Vorgaben leichter eingehalten werden.

So verwenden Sie die Desktop-App [!DNL Experience Manager]

* Stellen Sie sicher, dass Ihre [!DNL Experience Manager]-Serverversion von der [!DNL Experience Manager]-Desktop-App unterstützt wird. Weitere Informationen finden Sie in der [Kompatibilitätsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Laden Sie das Programm herunter und installieren Sie es.

* Testen Sie die Verbindung mithilfe einiger Assets. Siehe [Zugreifen auf und Öffnen von Assets über den Desktop](use-app-v1.md#openondesktop).

## Systemanforderungen, Voraussetzungen und Download-Links {#system-requirements-prerequisites-and-download-links}

Ausführliche Informationen finden Sie unter [[!DNL Experience Manager] Versionshinweise zur Desktop-App](release-notes-of-v1.md).

## Installieren und Verbinden der App mit dem [!DNL Experience Manager]-Server {#install-and-connect-aem-desktop-app-to-aem-server}

Weitere Informationen finden Sie unter [Installieren und Verbinden [!DNL Experience Manager] desktop app to [!DNL Experience Manager] Server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Es kann jeweils nur eine Instanz der Desktop-App [!DNL Experience Manager] installiert und aktiv sein.

## Dateiverarbeitung {#file-handling}

Beim Ändern einer Datei unter einem vom Desktop-Programm bereitgestellten Netzwerkfreigabe-Speicherort werden die Dateien in zwei Phasen in diesem Verzeichnis gespeichert. In der ersten Phase wird eine Datei lokal gespeichert. Ein Benutzer kann die Datei speichern und deren Bearbeitung fortsetzen, ohne auf den Abschluss der Übertragung warten zu müssen.

In der zweiten Phase lädt die Desktop-App die aktualisierte Datei nach einer vordefinierten Verzögerung (z. B. 30 s) auf den [!DNL Experience Manager]-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option „View Asset Status“ (Asset-Status anzeigen), um den Status des Upload-Vorgangs anzuzeigen.

1. Hochladen eines Assets in  Assets.

1. Klicken Sie in der Symbolleiste auf das Symbol für die Desktop-App.[!DNL Experience Manager]

1. Wählen Sie im Menü die Option „View Asset Status“ (Asset-Status anzeigen) aus.

1. Überprüfen Sie im Dialogfeld den Status des Upload-Vorgangs.

>[!NOTE]
>
>[!DNL Experience Manager] Mit der Desktop-App können Assets mit einer Größe von bis zu 40 GB verarbeitet werden.

## Verbindung zu einer [!DNL Experience Manager]-Instanz hinter einem Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Die Kopieren- und Verschieben-Methoden in der Assets-API erfordern, dass die folgenden zusätzlichen Kopfzeilen an [!DNL Experience Manager] übergeben werden:

* X-Ziel
* X-Tiefe
* X-Überschreiben

[!DNL Experience Manager] Desktop stellt eine Verbindung  [!DNL Experience Manager] mit einer URL her, die den Standardanschluss enthält. Daher sollte die Einstellung `virtualhosts` in der Dispatcher-Konfiguration die standardmäßige Port-Nummer enthalten. Weitere Informationen zur Konfiguration von `virtualhosts` finden Sie unter [Identifizieren von virtuellen Hosts](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#identifying-virtual-hosts-virtualhosts).

Weitere Informationen zum Konfigurieren des Dispatchers, sodass diese zusätzlichen Header übermittelt werden können, finden Sie unter [Festlegen der HTTP-Header](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=de#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxy-Unterstützung {#proxy-support}

[!DNL Experience Manager] Die Desktop-App verwendet den vordefinierten Proxy des Systems, um über HTTPS eine Verbindung mit dem Internet herzustellen. Das Programm kann die Verbindung nur mit einem Netzwerk-Proxy herstellen, für den keine gesonderte Authentifizierung erforderlich ist.

Wenn Sie die Proxy-Servereinstellungen für Windows konfigurieren oder ändern (Internetoptionen > LAN-Einstellungen), starten Sie die [!DNL Experience Manager] Desktop-App neu, damit die Änderungen wirksam werden.

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

Unter Windows befindet sich der Cache unter `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, wobei es sich um eine kodierte Version des [!DNL Experience Manager]-Hosts handelt, der in der Desktop-App konfiguriert wurde. Beispiel: `http://localhost:4502` wird als `http%3A%2F%2Flocalhost%3A4502%2F` angezeigt.

Unter Mac OS X befindet sich unter `~/Library/Group Containers/group.com.adobe.aem.desktop/cache` ein ähnliches Verzeichnis.

### Option zum Verwalten des Cache im Programm {#in-app-option-to-manage-cache}

Sie können festlegen, wie viel Festplattenspeicher für lokale Caching-Zwecke zur Verfügung gestellt wird. Die Artefakte vom Assets-Server werden für ein reibungsloseres Erlebnis lokal zwischengespeichert. Sie können die Standardeinstellungen Ihren Anforderungen entsprechend anpassen. Außerdem können Sie den Cache löschen, um alle Assets erneut abzurufen. Klicken Sie zum Festlegen der gewünschten Optionen auf das Symbol des Programms und klicken Sie auf **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**.

>[!NOTE]
>
>Wenn Sie den Cache löschen, werden nicht gespeicherte Änderungen beibehalten. Alle Assets, die nicht in den [!DNL Experience Manager]-Server eingecheckt sind, werden beibehalten und nicht gelöscht.

### Ändern des Cache-Verzeichnisses unter Windows  {#change-location-of-cache-on-windows}

Der Standardspeicherort für den Cache für die [!DNL Experience Manager]-Desktop-App lautet wie folgt:

* Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`

* Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`

`EncodedAEMEndpoint` ist die konfigurierte  [!DNL Experience Manager] Endpunkt-URL der App. Der Wert ist eine kodierte Version der Targeting-URL des Servers [!DNL Experience Manager]. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502`. Der Windows-Pfad zum Cache-Verzeichnis in diesem Beispiel lautet `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Um das Programm auf einen anderen Ordner oder ein anderes Laufwerk zu verweisen, bearbeiten Sie die Konfigurationsdatei des Programms.

1. Navigieren Sie zum Installationsverzeichnis des Programms. Der Standardspeicherort unter Windows ist `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bearbeiten Sie die Datei „Adobe Experience Manager Desktop.exe.config“ mit einem Texteditor.

   Zum Speichern von an dieser Datei vorgenommenen Änderungen sind Administratorberechtigungen erforderlich.

1. Suchen Sie nach der Zeichenfolge „ProxyCacheRoot“. Sie stellen fest, dass der zugehörige Wert auf das Cache-Verzeichnis `%LocalAppData%\Adobe\AssetsCompanion\Cache` festgelegt ist. Ändern Sie diesen Wert einfach in einen beliebigen gültigen Pfad.

   >[!NOTE]
   >
   >Das Programm erstellt automatisch ein Unterverzeichnis mit der Bezeichnung *&lt;Encoded AEM Endpoint>*. Dieses Verhalten kann nicht konfiguriert werden.

>[!MORELIKETHIS]
* [Einführung  [!DNL Experience Manager] in die Desktop-App](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html?lang=de).
* [Verwenden Sie die  [!DNL Experience Manager] Desktop-App](use-app-v1.md).
* [ [!DNL Experience Manager] Fehlerbehebung bei der Desktop-App](troubleshoot-app-v1.md).

