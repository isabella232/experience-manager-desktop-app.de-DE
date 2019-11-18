---
title: Bewährte Verfahren und Fehlerbehebung für die AEM-Desktop-App
description: Befolgen Sie die Best Practices und führen Sie eine Fehlerbehebung durch, um gelegentliche Probleme im Zusammenhang mit Installation, Aktualisierung, Konfiguration usw. zu beheben.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 850d2c21a796599ed40164e7d6f892967563c16b

---


# Troubleshoot AEM desktop app {#troubleshoot-v2}

Die Adobe Experience Manager (AEM)-Desktop-App stellt eine Verbindung zum DAM-Repository (Digital Asset Management) einer Remote-AEM-Bereitstellung her. Die App ruft Repository-Informationen und Suchergebnisse auf Ihrem Computer ab, lädt Dateien und Ordner herunter und lädt sie hoch und bietet Funktionen zum Verwalten von Konflikten mit der Benutzeroberfläche von AEM Assets.

Lesen Sie weiter, um Fehler in der App zu beheben, lernen Sie die Best Practices kennen und lernen Sie die Einschränkungen kennen.

## Best Practices {#best-practices-to-prevent-troubles}

Befolgen Sie die folgenden Best Practices, um einige häufige Probleme und die Fehlerbehebung zu vermeiden.

* **So funktioniert** die Desktop-App: Bevor Sie mit der Verwendung der Anwendung beginnen, sollten Sie einige Minuten damit verbringen, wie die App funktioniert. Erfahren Sie mehr über die Verknüpfung zwischen Web-Benutzeroberfläche und Desktop, Repository-Zuordnung, Asset-Zwischenspeicherung, Lokales Speichern und Hochladen im Hintergrund. See [how it works](release-notes.md#how-app-works).

* **Vermeiden Sie nicht unterstützte Zeichen in Ordnernamen**:Verwenden Sie beim Erstellen oder Hochladen von Ordnern keine Leerzeichen und ungültige Zeichen. Eine Liste der Zeichen finden Sie unter Ordner [erstellen in AEM Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders). In einigen AEM-Anwendungsfällen können nicht unterstützte Zeichen im Ordnernamen betroffen sein.

* **Bewährte Verfahren zur Vermeidung von Konflikten**: Um mögliche Konflikte bei der Zusammenarbeit mit mehreren Assets zu vermeiden, lesen Sie [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Verwenden Sie den Ordner-Upload für große, hierarchische Ordner**: Verwenden Sie anstelle der Assets-Weboberfläche oder anderer Methoden die AEM-Desktop-App, um große Ordner hochzuladen. Die App lädt die Assets mit Protokollierung und Überwachung im Hintergrund hoch. Siehe [Massen-Upload-Assets](using.md#bulk-upload-assets).

* **Verwenden Sie die neueste Version**: Verwenden Sie die neueste App-Version und prüfen Sie immer, ob die Kompatibilität gewährleistet ist, bevor Sie eine neue App-Version installieren oder bevor Sie auf eine neuere AEM-Version aktualisieren. See [release notes](release-notes.md).

* **Verwenden Sie denselben Laufwerksbuchstaben**: Verwenden Sie denselben Laufwerksbuchstaben für die Zuordnung zum AEM DAM innerhalb eines Unternehmens. Um von anderen Benutzern platzierte Assets anzuzeigen, müssen die Pfade identisch sein. Mit demselben Laufwerksbuchstaben wird ein konstanter Pfad zu DAM-Assets sichergestellt. Die Assets bleiben platziert und werden auch dann nicht entfernt, wenn verschiedene Laufwerksbuchstaben von verschiedenen Benutzern verwendet werden.

* **Beachten Sie das Netzwerk**: Die Netzwerkleistung ist von entscheidender Bedeutung für die Leistung der AEM-Desktop-App. Wenn die Reaktion auf Dateiübertragungen oder Massenvorgänge verlangsamt ist, deaktivieren Sie die Funktionen oder Apps, die zu viel Netzwerkverkehr führen können.

* **Nicht unterstützte Anwendungsfälle für Desktop-Apps**: Verwenden Sie die App nicht für die Migration von Assets (sie erfordert Planung und andere Werkzeuge). für DAM-Vorgänge mit hoher Leistung (z. B. Verschieben großer Ordner, große Uploads, Suchen von Dateien mithilfe erweiterter Metadaten-Suchen); und als Synchronisierungs-Client (Design- und Nutzungsmuster unterscheiden sich von In-Sync-Clients wie Microsoft OneDrive oder Adobe Creative Cloud-Desktop-Synchronisierung).

## Fehlerbehebung {#troubleshooting-prep}

Um Probleme mit Desktop-Apps zu beheben, beachten Sie die folgenden Informationen. Außerdem werden Sie darauf vorbereitet, die Probleme besser an die Adobe-Kundenunterstützung zu übermitteln, wenn Sie sich für den Support entscheiden.

### Debugging-Modus aktivieren {#enable-debug-mode}

Zur Fehlerbehebung können Sie den Debug-Modus aktivieren und weitere Informationen in den Protokollen abrufen. Um die App im Debug-Modus auszuführen, verwenden Sie die folgenden Befehlszeilenoptionen in einem Terminal oder an der Eingabeaufforderung.

* Windows: `SET AEM_DESKTOP_LOG_LEVEL=DEBUG & "C:\Program Files\Adobe\Adobe Experience Manager Desktop\Adobe Experience Manager Desktop.exe"`

* Mac: `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`

### Speicherort der Protokolldateien {#check-log-files-v2}

Die Protokolldateien für die AEM-Desktop-App finden Sie in den folgenden Verzeichnissen. Wenn beim Hochladen vieler Assets einige Dateien nicht hochgeladen werden können, finden Sie Informationen zu den fehlgeschlagenen Uploads in der `backend.log` Datei oben.

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

>[!NOTE]
>
>Wenn Sie mit dem Adobe-Kundendienst an einer Supportanfrage/einem Ticket arbeiten, werden Sie möglicherweise aufgefordert, die Protokolldateien freizugeben, damit das Supportteam das Problem verstehen kann. Archivieren Sie den gesamten `Logs` Ordner und geben Sie ihn für die Kundenunterstützung frei.

### Clear cache {#clear-cache-v2}

Das Löschen des Cache der AEM-Desktop-App ist eine vorläufige Aufgabe zur Fehlerbehebung, die mehrere Probleme beheben kann. Löschen Sie den Cache in den App-Voreinstellungen. Siehe [Voreinstellungen](install-upgrade.md#set-preferences)festlegen. Der Standardspeicherort des Cache-Ordners ist:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Der Speicherort kann sich jedoch je nach AEM Desktop-konfiguriertem AEM-Endpunkt ändern. Der Wert ist eine codierte Version der Ziel-URL. For example, if the application is targeting `http://localhost:4502`, the directory name is `http%3A%2F%2Flocalhost%3A4502%2F`. Um den Cache zu leeren, löschen Sie den entsprechenden Ordner. Ein weiterer Grund, den Cache zu leeren, ist, Speicherplatz freizugeben, wenn Sie wenig Speicherplatz auf der Festplatte haben.

>[!CAUTION]
>
>Wenn Sie den AEM-Desktop-Cache löschen, gehen Änderungen an lokalen Elementen, die nicht mit dem AEM-Server synchronisiert werden, unwiderruflich verloren.

### AEM Desktop-App-Version {#know-app-version-v2}

Klicken Sie auf ![App-Menü](assets/do-not-localize/more_options_da2.png) , um das Menü der App zu öffnen, und klicken Sie auf **[!UICONTROL Help]** &gt; **[!UICONTROL About]**.

## Platzierte Assets können nicht angezeigt werden {#placed-assets-missing}

Wenn die Assets, die Sie oder andere Kreativprofis in den Unterstützungsdateien abgelegt haben (z. B. INDD-Dateien), nicht angezeigt werden, prüfen Sie Folgendes:

* Verbindung zum Server. Flackernde Netzwerkverbindungen können Asset-Downloads anhalten.
* Dateigröße. Das Herunterladen und Anzeigen großer Assets dauert länger.
* Erhöhen Sie die Briefkonsistenz. Wenn Sie oder ein anderer Mitarbeiter die Assets platziert haben, während Sie den AEM DAM einem anderen Laufwerksbuchstaben zuordnen, werden die platzierten Assets nicht angezeigt.
* Berechtigungen. Wenden Sie sich an Ihren AEM-Administrator, um zu prüfen, ob Sie berechtigt sind, die platzierten Assets abzurufen.

## Probleme beim Aktualisieren auf macOS {#issues-when-upgrading-on-macos}

Gelegentlich können Probleme auftreten, wenn Sie die AEM-Desktop-App auf macOS aktualisieren. Dies wird durch den alten Systemordner für die AEM-Desktop-App verursacht, der verhindert, dass neue Versionen der AEM-Desktop-App korrekt geladen werden. Zur Behebung dieses Problems können die folgenden Ordner und Dateien manuell entfernt werden.

Ziehen Sie die `Adobe Experience Manager Desktop` Anwendung vor dem Ausführen der folgenden Schritte aus dem Ordner "macOS-Anwendungen"in den Papierkorb. Öffnen Sie dann Terminal, führen Sie den folgenden Befehl aus und geben Sie bei Aufforderung Ihr Kennwort ein.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Dateien können nicht hochgeladen werden {#upload-fails}

Wenn Sie eine Desktop-App mit AEM 6.5.1 oder höher verwenden, aktualisieren Sie S3 oder Azurblase Connector auf Version 1.10.4 oder höher. Es wird ein Fehler beim Hochladen von Dateien im Zusammenhang mit [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599)behoben. Siehe [Installationsanweisungen](install-upgrade.md#install-v2).

## Problem bei SSL-Konfiguration {#ssl-config-v2}

Die Bibliotheken, die die AEM-Desktop-App für die HTTP-Kommunikation verwendet, verwenden eine strikte SSL-Durchsetzung. Manchmal kann eine Verbindung mit einem Browser erfolgreich sein, aber die Verwendung der AEM-Desktop-App ist fehlgeschlagen. Installieren Sie für eine ordnungsgemäße SSL-Konfiguration das fehlende Zwischenzertifikat in Apache. Siehe [How to install an Intermediate CA cert in Apache](https://access.redhat.com/solutions/43575) (nur auf Englisch verfügbar).

## App reagiert nicht {#unresponsive}

In seltenen Fällen reagiert die Anwendung möglicherweise nicht mehr, zeigt nur einen weißen Bildschirm an oder zeigt einen Fehler am unteren Rand der Oberfläche an, ohne dass irgendwelche Optionen auf der Oberfläche vorhanden sind. Versuchen Sie Folgendes in der Reihenfolge:

1. Klicken Sie mit der rechten Maustaste auf die Anwendungsoberfläche und klicken Sie auf **[!UICONTROL Refresh]**.
1. Beenden Sie die Anwendung und starten Sie sie neu.

Bei beiden Methoden beginnt die App im DAM-Stammordner.

>[!MORELIKETHIS]
>
>* [Bekannte Probleme](release-notes.md#known-issues-v2)
>* [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts)