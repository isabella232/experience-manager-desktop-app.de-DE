---
title: Best Practices und Fehlerbehebung für das AEM-Desktop-Programm
description: Befolgen Sie die Best Practices und führen Sie eine Fehlerbehebung durch, um gelegentliche Probleme im Zusammenhang mit Installation, Aktualisierung, Konfiguration usw. zu beheben.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: ad5337c8e1697d0a37d3020d25802dc1d732f320

---


# Fehlerbehebung für das AEM-Desktop-Programm {#troubleshoot-v2}

Das Adobe Experience Manager (AEM)-Desktop-Programm stellt eine Verbindung zum DAM-Repository (Digital Asset Management) einer Remote-AEM-Bereitstellung her. Das Programm ruft Repository-Informationen und Suchergebnisse auf Ihrem Computer ab, lädt Dateien und Ordner herunter und lädt sie hoch und bietet Funktionen zum Verwalten von Konflikten mit der Benutzeroberfläche von AEM Assets.

Lesen Sie weiter, um Fehler im Programm zu beheben, lernen Sie die Best Practices kennen und erfahren Sie mehr über Einschränkungen.

## Best Practices {#best-practices-to-prevent-troubles}

Befolgen Sie die folgenden Best Practices, um einige häufige Probleme und die Fehlerbehebung zu vermeiden.

* **So funktioniert das Desktop-Programm**: Bevor Sie mit der Verwendung des Programms beginnen, sollten Sie sich kurz mit ihrer Funktionsweise vertraut machen. Erfahren Sie mehr über Verknüpfung zwischen Web-Benutzeroberfläche und Desktop, Repository-Zuordnung, Asset-Zwischenspeicherung, lokales Speichern und Hochladen im Hintergrund. Machen Sie sich mit der [Funktionsweise](release-notes.md#how-app-works) vertraut:

* **Vermeiden Sie nicht unterstützte Zeichen in Ordnernamen**: Verwenden Sie beim Erstellen oder Hochladen von Ordnern keine Leerzeichen und ungültigen Zeichen. Eine Liste der Zeichen finden Sie unter [Erstellen von Ordnern in AEM Assets](https://helpx.adobe.com/de/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders). In einigen AEM-Anwendungsfällen können durch nicht unterstützte Zeichen im Ordnernamen Probleme auftreten.

* **Best Practices zur Vermeidung von Konflikten**: Um mögliche Konflikte bei der Zusammenarbeit mit mehreren Assets zu vermeiden, lesen Sie [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Verwenden Sie den Ordner-Upload für große, hierarchische Ordner**: Verwenden Sie anstelle der Assets-Web-Oberfläche oder anderer Methoden das AEM-Desktop-Programm, um große Ordner hochzuladen. Das Programm lädt die Assets mit Protokollierung und Überwachung im Hintergrund hoch. Siehe [Massen-Upload von Assets](using.md#bulk-upload-assets).

* **Verwenden Sie die neueste Version**: Verwenden Sie die neueste Programm-Version und prüfen Sie immer, ob die Kompatibilität gewährleistet ist, bevor Sie eine neue Programm-Version installieren oder bevor Sie auf eine neuere AEM-Version aktualisieren. Siehe [Versionshinweise](release-notes.md).

* **Verwenden Sie denselben Laufwerksbuchstaben**: Verwenden Sie im gesamten Unternehmen denselben Laufwerksbuchstaben für das AEM DAM. Damit von anderen Benutzern platzierte Assets angezeigt werden können, müssen die Pfade identisch sein. Mit demselben Laufwerksbuchstaben wird ein konstanter Pfad zu DAM-Assets sichergestellt. Die Assets bleiben platziert und werden auch dann nicht entfernt, wenn verschiedene Laufwerksbuchstaben von verschiedenen Benutzern verwendet werden.

* **Beachten Sie das Netzwerk**: Die Netzwerkleistung ist von entscheidender Bedeutung für die Leistung des AEM-Desktop-Programms. Wenn die Reaktion auf Dateiübertragungen oder Massenvorgänge verlangsamt ist, deaktivieren Sie die Funktionen oder Applikationen, die zu viel Netzwerkverkehr führen können.

* **Nicht unterstützte Anwendungsfälle für das Desktop-Programm**: Verwenden Sie das Programm nicht für die Migration von Assets (sie erfordert Planung und andere Werkzeuge), für DAM-Vorgänge mit hoher Leistung (z. B. Verschieben großer Ordner, große Uploads, Suchen von Dateien mithilfe erweiterter Metadaten-Suchen) oder als Synchronisierungs-Client (Design- und Nutzungsmuster unterscheiden sich von In-Sync-Clients wie Microsoft OneDrive oder Adobe Creative Cloud-Desktop-Synchronisierung).

## Fehlerbehebung {#troubleshooting-prep}

Um Probleme mit dem Desktop-Programm zu beheben, beachten Sie die folgenden Informationen. Außerdem werden Sie darauf vorbereitet, die Probleme besser an die Adobe-Kundenunterstützung zu übermitteln, wenn Sie sich für den Support entscheiden.

### Aktivieren des Debugging-Modus {#enable-debug-mode}

Zur Fehlerbehebung können Sie den Debug-Modus aktivieren und weitere Informationen in den Protokollen abrufen. Um das Prorgamm im Debug-Modus auszuführen, verwenden Sie die folgenden Befehlszeilenoptionen in einem Terminal oder in der Eingabeaufforderung.

* Windows: `SET AEM_DESKTOP_LOG_LEVEL=DEBUG & "C:\Program Files\Adobe\Adobe Experience Manager Desktop\Adobe Experience Manager Desktop.exe"`

* Mac: `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`

### Speicherort der Protokolldateien {#check-log-files-v2}

Die Protokolldateien für das AEM-Desktop-Programm finden Sie in den folgenden Verzeichnissen. Wenn beim Hochladen vieler Assets einige Dateien nicht hochgeladen werden können, finden Sie Informationen zu den fehlgeschlagenen Uploads in der Datei `backend.log` im oben genannten Verzeichnis.

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

>[!NOTE]
>
>Wenn Sie mit dem Adobe-Kundendienst an einer Support-Anfrage/einem Ticket arbeiten, werden Sie möglicherweise aufgefordert, die Protokolldateien freizugeben, damit das Supportteam das Problem verstehen kann. Archivieren Sie den gesamten Ordner `Logs` und geben Sie ihn für die Kundenunterstützung frei.

### Löschen des Cache {#clear-cache-v2}

Beim Löschen des Caches von handelt es sich um eine vorläufige Aufgabe zur Fehlerbehebung, durch die verschiedene Probleme mit dem AEM-Desktop-Programm gelöst werden können. Löschen Sie den Cache in den Programm-Voreinstellungen. Siehe [Festlegen von Voreinstellungen](install-upgrade.md#set-preferences). Der Standardspeicherort des Cache-Ordners ist:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Das Verzeichnis kann sich jedoch in Abhängigkeit vom konfigurierten AEM-Endpunkt des AEM-Desktop-Programms ändern. Der Wert ist eine codierte Version der Ziel-URL. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502%2F`. Um den Cache zu leeren, löschen Sie den entsprechenden Ordner. Ein weiterer Grund, den Cache zu leeren, besteht darin, Speicherplatz freizugeben, wenn Sie wenig Speicherplatz auf der Festplatte haben.

>[!CAUTION]
>
>Wenn Sie den AEM-Desktop-Cache löschen, gehen dabei nicht mit AEM synchronisierte Änderungen lokaler Assets unwiderruflich verloren.

### Ermitteln der AEM-Desktop-Programm-Version {#know-app-version-v2}

Klicken Sie auf das ![Programmmenü](assets/do-not-localize/more_options_da2.png), um das Menü des Programms zu öffnen, und klicken Sie auf **[!UICONTROL Help]** &gt; **[!UICONTROL About]**.

## Platzierte Assets werden nicht angezeigt {#placed-assets-missing}

Wenn Sie die Assets, die Sie oder andere Kreativprofis in den Support-Dateien gespeichert haben (z. B. INDD-Dateien), nicht sehen können, überprüfen Sie Folgendes:

* Verbindung zum Server. Instabile Netzwerkverbindungen können das Herunterladen von Assets verzögern.
* Dateigröße. Das Herunterladen und Anzeigen großer Assets dauert länger.
* Konsistenz der Laufwerksbuchstaben. Wenn Sie oder ein anderer Mitarbeiter die Assets platziert haben, während das AEM DAM einem anderen Laufwerksbuchstaben zugeordnet wurde, werden die platzierten Assets nicht angezeigt
* Berechtigungen. Wenden Sie sich an Ihren AEM-Administrator, um zu prüfen, ob Sie berechtigt sind, die platzierten Assets abzurufen.

## Probleme beim Aktualisieren unter macOS {#issues-when-upgrading-on-macos}

Gelegentlich können bei einem Upgrade des AEM-Desktop-Programms unter macOS Probleme auftreten. Die Ursache liegt darin, dass der alte Systemordner des AEM-Desktop-Programms verhindert, dass neue Versionen des AEM-Desktop-Programms korrekt geladen werden. Zur Behebung dieses Problems können die folgenden Ordner und Dateien manuell entfernt werden.

Ziehen Sie das `Adobe Experience Manager Desktop`-Programm vor dem Ausführen der folgenden Schritte aus dem Ordner „macOS-Applikationen“ in den Papierkorb. Öffnen Sie dann Terminal, führen Sie den folgenden Befehl aus und geben Sie Ihr Kennwort ein, wenn Sie dazu aufgefordert werden.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Dateien können nicht hochgeladen werden {#upload-fails}

Wenn Sie das Desktop-Programm mit AEM 6.5.1 oder höher verwenden, aktualisieren Sie den S3- oder Azure-Connector auf Version 1.10.4 oder höher. Dadurch wird das Problem mit dem Hochladen von Dateien im Zusammenhang mit [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599) behoben. Siehe [Installationsanweisungen](install-upgrade.md#install-v2).

## Problem bei SSL-Konfiguration {#ssl-config-v2}

Die Bibliotheken, die das AEM-Desktop-Programm zur HTTP-Kommunikation nutzt, setzen auf strikte SSL-Durchsetzung. Mitunter kann zwar über einen Browser eine Verbindung erfolgreich hergestellt werden, aber nicht über das AEM-Desktop-Programm. Installieren Sie für eine ordnungsgemäße SSL-Konfiguration das fehlende Zwischenzertifikat in Apache. Siehe [How to install an Intermediate CA cert in Apache](https://access.redhat.com/solutions/43575) (nur auf Englisch verfügbar).

## Das Programm reagiert nicht {#unresponsive}

In seltenen Fällen reagiert das Programm möglicherweise nicht mehr, zeigt nur einen weißen Bildschirm an oder zeigt einen Fehler am unteren Rand der Benutzeroberfläche an, ohne dass Optionen auf der Benutzeroberfläche vorhanden sind. Versuchen Sie Folgendes in genannter Reihenfolge:

1. Klicken Sie mit der rechten Maustaste auf die Programm-Oberfläche und klicken Sie auf **[!UICONTROL Refresh]**.
1. Beenden Sie das Programm und starten Sie es neu.

Bei beiden Methoden startet das Programm im Stammordner des DAM.

>[!MORELIKETHIS]
>
>* [Bekannte Probleme](release-notes.md#known-issues-v2)
>* [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts)