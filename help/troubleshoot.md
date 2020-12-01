---
title: Best Practices und Fehlerbehebung für das Adobe Experience Manager-Desktop-Programm
description: Befolgen Sie die Best Practices und führen Sie eine Fehlerbehebung durch, um gelegentliche Probleme im Zusammenhang mit Installation, Aktualisierung, Konfiguration usw. zu beheben.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS, SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2893fc1f8aad02e1436a1a281a320e6837487220
workflow-type: tm+mt
source-wordcount: '2171'
ht-degree: 91%

---


# Fehlerbehebung für das Adobe Experience Manager-Desktop-Programm {#troubleshoot-v2}

Die Adobe Experience Manager-Desktop-App stellt eine Verbindung zum DAM-Repository (Digital Asset Management) einer Remote-Bereitstellung für Experience Manager her. Das Programm ruft Repository-Informationen und Suchergebnisse auf Ihrem Computer ab, lädt Dateien und Ordner herunter und lädt sie hoch und bietet Funktionen zum Verwalten von Konflikten mit der Benutzeroberfläche von Assets.

Lesen Sie weiter, um Fehler im Programm zu beheben, lernen Sie die Best Practices kennen und erfahren Sie mehr über Einschränkungen.

## Best Practices {#best-practices-to-prevent-troubles}

Befolgen Sie die folgenden Best Practices, um einige häufige Probleme und die Fehlerbehebung zu vermeiden.

* **So funktioniert das Desktop-Programm**: Bevor Sie mit der Verwendung des Programms beginnen, sollten Sie sich kurz mit ihrer Funktionsweise vertraut machen. Erfahren Sie mehr über Verknüpfung zwischen der Web-Oberfläche von Experience Manager und dem Desktop-Programm, Repository-Zuordnung, Asset-Zwischenspeicherung, lokales Speichern und Hochladen im Hintergrund. Machen Sie sich mit der [Funktionsweise](release-notes.md#how-app-works) vertraut:

* **Vermeiden Sie nicht unterstützte Zeichen in Ordnernamen**: Verwenden Sie beim Erstellen oder Hochladen von Ordnern keine Leerzeichen und ungültige Zeichen. Eine Liste der Zeichen finden Sie unter [Erstellen von Ordnern in Experience Manager Assets](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/manage-assets.html?lang=de#creating-folders). In einigen Adobe Experience Manager-Anwendungsfällen können durch nicht unterstützte Zeichen im Ordnernamen Probleme auftreten.

* **Best Practices zur Vermeidung von Konflikten**: Um mögliche Konflikte bei der Zusammenarbeit mit mehreren Assets zu vermeiden, lesen Sie [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Verwenden Sie den Ordner-Upload für große, hierarchische Ordner**: Verwenden Sie anstelle der Assets-Web-Oberfläche oder anderer Methoden das Experience Manager-Desktop-Programm, um große Ordner hochzuladen. Das Programm lädt die Assets mit Protokollierung und Überwachung im Hintergrund hoch. Siehe [Massen-Upload von Assets](using.md#bulk-upload-assets).

* **Verwenden Sie die neueste Version**: Verwenden Sie die neueste Programmversion und prüfen Sie immer, ob die Kompatibilität gewährleistet ist, bevor Sie eine neue Programmversion installieren oder bevor Sie auf eine neuere Adobe Experience Manager-Version aktualisieren. Siehe [Versionshinweise](release-notes.md).

* **Verwenden Sie denselben Laufwerksbuchstaben**: Verwenden Sie in der gesamten Organisation denselben Laufwerksbuchstaben für Adobe Experience Manager DAM. Damit von anderen Benutzern platzierte Assets angezeigt werden können, müssen die Pfade identisch sein. Mit demselben Laufwerksbuchstaben wird ein konstanter Pfad zu DAM-Assets sichergestellt. Die Assets bleiben platziert und werden auch dann nicht entfernt, wenn verschiedene Laufwerksbuchstaben von verschiedenen Benutzern verwendet werden.

* **Beachten Sie das Netzwerk**: Die Netzwerkleistung ist von entscheidender Bedeutung für die Leistung des Experience Manager-Desktop-Programms. Wenn die Reaktion auf Dateiübertragungen oder Massenvorgänge verlangsamt ist, deaktivieren Sie die Funktionen oder Applikationen, die zu viel Netzwerkverkehr führen können.

* **Vom Desktop-Programm nicht unterstützte Anwendungsfälle**: Verwenden Sie das Programm nicht für die Asset-Migration (diese muss gründlich geplant werden und erfordert andere Tools), anspruchsvolle DAM-Operationen (z. B. Verschieben großer Ordner, Uploads großer Dateien, Suchen von Dateien anhand erweiterter Metadaten-Suchen) oder als Synchronisierungs-Client (Design- und Nutzungsmuster unterscheiden sich von In-Sync-Clients wie Microsoft OneDrive oder Adobe Creative Cloud-Desktop-Synchronisierung).

* **Timeout**: Das Desktop-Programm weist derzeit keinen konfigurierbaren Timeout-Wert auf, um die Verbindung zwischen dem Experience Manager-Server und dem Programm nach einem bestimmten Zeitintervall zu trennen. Wenn beim Hochladen großer Assets nach einiger Zeit ein Verbindungs-Timeout eintritt, versucht das Programm, das Asset einige Male hochzuladen, indem es den Timeout-Wert für den Upload erhöht. Es gibt keine empfohlene Vorgehensweise, um die Standardeinstellungen für den Timeout zu ändern.

## Fehlerbehebung {#troubleshooting-prep}

Um Probleme mit dem Desktop-Programm zu beheben, beachten Sie die folgenden Informationen. Außerdem werden Sie darauf vorbereitet, die Probleme besser an die Adobe-Kundenunterstützung zu übermitteln, wenn Sie sich für den Support entscheiden.

### Speicherort der Protokolldateien {#check-log-files-v2}

Das [!DNL Experience Manager]-Desktop-Programm speichert die Protokolldateien je nach Betriebssystem in den folgenden Verzeichnisse:

Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Unter macOS: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

Wenn beim Hochladen vieler Assets einige Dateien nicht hochgeladen werden können, finden Sie in der Datei `backend.log` Informationen zu den fehlgeschlagenen Uploads.

>[!NOTE]
>
>Wenn Sie mit der Kundenunterstützung von Adobe an einer Support-Anfrage/einem Ticket arbeiten, werden Sie möglicherweise aufgefordert, die Protokolldateien zu teilen, damit das Kundenunterstützungs-Team das Problem verstehen kann. Archivieren Sie den gesamten Ordner `Logs` und geben Sie ihn für Ihre Kontaktperson bei der Kundenunterstützung frei.

### Detailebene in Protokolldateien ändern {#level-of-details-in-log}

So ändern Sie die Detailebene in Protokolldateien:

1. Vergewissern Sie sich, dass das Programm nicht ausgeführt wird.

1. Windows-System:

   1. Öffnen Sie ein Befehlsfenster.

   1. Starten Sie das [!DNL Adobe Experience Manager]-Desktop-Programm, indem Sie diesen Befehl ausführen:

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Mac-System:

   1. Öffnen Sie ein Terminal-Fenster.

   1. Starten Sie das [!DNL Adobe Experience Manager]-Desktop-Programm, indem Sie diesen Befehl ausführen:

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

Die gültigen Protokollebenen sind DEBUG, INFO, WARN oder ERROR. Die Ausführlichkeit der Protokolle ist in DEBUG am höchsten und in ERROR am niedrigsten.

### Aktivieren des Debug-Modus {#enable-debug-mode}

Zur Fehlerbehebung können Sie den Debug-Modus aktivieren und weitere Informationen in den Protokollen abrufen.

>[!NOTE]
>
>Gültige Protokollebenen sind DEBUG, INFO, WARN oder ERROR. Die Ausführlichkeit der Protokolle ist in DEBUG am höchsten und in ERROR am niedrigsten.

So verwenden Sie das Programm im Debug-Modus auf einem Mac:

1. Öffnen Sie ein Terminal-Fenster oder eine Eingabeaufforderung.

1. Starten Sie das [!DNL Experience Manager]-Desktop-Programm, indem Sie den folgenden Befehl ausführen:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

So aktivieren Sie den Debug-Modus unter Windows:

1. Öffnen Sie ein Befehlsfenster.

1. Starten Sie das [!DNL Experience Manager]-Desktop-Programm, indem Sie den folgenden Befehl ausführen:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### Löschen des Cache {#clear-cache-v2}

Führen Sie die folgenden Schritte durch:

1. Beginn der Anwendung und Verbinden Sie eine Experience Manager-Instanz.

1. Öffnen Sie die Voreinstellungen des Programms, indem Sie auf die Auslassungspunkte in der oberen rechten Ecke klicken und die Option [!UICONTROL Preferences] auswählen.

1. Gehen Sie zum Eintrag, der die [!UICONTROL Current Cache Size] anzeigt. Klicken Sie auf das Papierkorbsymbol neben diesem Element.

Gehen Sie wie folgt vor, um den Cache manuell zu leeren.

>[!CAUTION]
>
>Dies ist ein potenziell destruktiver Vorgang. Wenn lokale Dateiänderungen vorliegen, die nicht in [!DNL Adobe Experience Manager] hochgeladen wurden, gehen diese Änderungen verloren, wenn Sie fortfahren.

Der Cache wird gelöscht, indem das Cache-Verzeichnis des Programms gelöscht wird. Zu finden ist es in den Voreinstellungen des Programms.

1. Starten Sie das Programm.

1. Öffnen Sie die Voreinstellungen des Programms, indem Sie die Auslassungspunkte in der oberen rechten Ecke auswählen und dann [!UICONTROL Preferences] auswählen.

1. Notieren Sie den Wert für [!UICONTROL Cache Directory].

   In diesem Verzeichnis befinden sich Unterverzeichnisse, die nach den codierten [!DNL Adobe Experience Manager]-Endpunkten benannt sind. Der Name ist eine codierte Version der Ziel-URL von [!DNL Adobe Experience Manager]. Wenn das Ziel des Programms beispielsweise `localhost:4502` ist, lautet der Verzeichnisname `localhost_4502`.

Wenn Sie den Cache löschen möchten, löschen Sie das Verzeichnis „Codierter [!DNL Adobe Experience Manager]-Endpunkt“. Wenn Sie stattdessen das gesamte in den Voreinstellungen angegebene Verzeichnis löschen, wird der Cache für alle vom Programm verwendeten Instanzen gelöscht.

Beim Löschen des Caches des [!DNL Adobe Experience Manager]-Desktop-Programms handelt es sich um eine vorläufige Aufgabe zur Fehlerbehebung, durch die verschiedene Probleme gelöst werden können. Löschen Sie den Cache in den Programm-Voreinstellungen. Siehe [Festlegen von Voreinstellungen](install-upgrade.md#set-preferences). Der Standardspeicherort des Cache-Ordners ist:

### Ermitteln der [!DNL Adobe Experience Manager]-Desktop-Programm-Version {#know-app-version-v2}

So zeigen Sie die Versionsnummer an:

1. Starten Sie das Programm.

1. Klicken Sie auf die Auslassungszeichen in der oberen rechten Ecke, halten Sie den Mauszeiger über [!UICONTROL Help] und klicken Sie auf [!UICONTROL About].

   Daraufhin wird die Versionsnummer auf dem Bildschirm angezeigt.

### Platzierte Assets werden nicht angezeigt {#placed-assets-missing}

Wenn Sie die Assets, die Sie oder andere Kreativprofis in den Support-Dateien gespeichert haben (z. B. INDD-Dateien), nicht sehen können, überprüfen Sie Folgendes:

* Verbindung zum Server. Instabile Netzwerkverbindungen können das Herunterladen von Assets verzögern.

* Dateigröße. Das Herunterladen und Anzeigen großer Assets dauert länger.

* Konsistenz der Laufwerksbuchstaben. Wenn Sie oder ein anderer Mitarbeiter die Assets platziert haben, während Sie den Experience Manager-DAM einem anderen Laufwerksbuchstaben zuordnen, werden die platzierten Assets nicht angezeigt.

* Berechtigungen. Wenden Sie sich an Ihren Experience Manager-Administrator, um zu prüfen, ob Sie berechtigt sind, die platzierten Assets abzurufen.

### Änderungen an Dateien in der Benutzeroberfläche des Desktop-Programms werden in [!DNL Adobe Experience Manager] nicht sofort übernommen {#changes-on-da-not-visible-on-aem}

Das [!DNL Adobe Experience Manager]-Desktop-Programm überlässt es dem Benutzer, zu entscheiden, wann alle Änderungen an einer Datei abgeschlossen sind. Je nach Größe und Komplexität einer Datei dauert es sehr lange, die neue Version einer Datei wieder zurück in [!DNL Adobe Experience Manager] zu übertragen. Das Design des Programms erfordert eine Minimierung der Anzahl der Übermittlungen einer Datei, anstatt zu vermuten, wann die Dateibearbeitungen abgeschlossen sind und automatisch hochgeladen werden können. Es wird empfohlen, dass der Benutzer die Übertragung der Datei zurück in [!DNL Adobe Experience Manager] einleitet, indem er die Änderungen einer Datei hochlädt.

### Probleme beim Aktualisieren unter macOS {#issues-when-upgrading-on-macos}

Gelegentlich können Probleme auftreten, wenn Sie die Experience Manager-Desktop-App unter macOS aktualisieren. Dies wird durch den alten Systemordner für die Desktop-App von Experience Manager verursacht, sodass neue Versionen der Experience Manager-Desktop-App nicht korrekt geladen werden. Zur Behebung dieses Problems können die folgenden Ordner und Dateien manuell entfernt werden.

Ziehen Sie das `Adobe Experience Manager Desktop`-Programm vor dem Ausführen der folgenden Schritte aus dem Ordner „macOS-Applikationen“ in den Papierkorb. Öffnen Sie dann Terminal, führen Sie den folgenden Befehl aus und geben Sie Ihr Kennwort ein, wenn Sie dazu aufgefordert werden.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

### Dateien können nicht hochgeladen werden {#upload-fails}

Wenn Sie eine Desktop-App mit Experience Manager 6.5.1 oder höher verwenden, aktualisieren Sie S3 oder Azurblase Connector auf Version 1.10.4 oder höher. Dadurch wird das Problem mit dem Hochladen von Dateien im Zusammenhang mit [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599) behoben. Siehe [Installationsanweisungen](install-upgrade.md#install-v2).

### Verbindungsprobleme mit dem [!DNL Experience Manager]-Desktop-Programm {#connection-issues}

Wenn allgemeine Verbindungsprobleme auftreten, finden Sie hier einige Möglichkeiten, weitere Informationen zum [!DNL Experience Manager]-Desktop-Programm zu erhalten.

**Überprüfen des Anfrageprotokolls**

Das [!DNL Experience Manager]-Desktop-Programm protokolliert alle gesendeten Anfragen zusammen mit dem Antwort-Code jeder Anfrage in einer dedizierten Protokolldatei.

1. Öffnen Sie `request.log` im Protokollverzeichnis des Programms, um diese Anfragen anzuzeigen.

1. Jede Zeile im Protokoll stellt entweder eine Anfrage oder eine Antwort dar. Anfragen haben ein `>`-Zeichen, gefolgt von der angeforderten URL. Antworten haben ein `<`-Zeichen, gefolgt vom Antwort-Code und der angeforderten URL. Anfragen und Antworten können mit der GUID jeder Zeile abgeglichen werden.

**Überprüfen von Anfragen, die vom eingebetteten Browser des Programms geladen wurden**

Die meisten Anfragen des Programms finden Sie im Anfrageprotokoll. Wenn es dort keine hilfreichen Informationen gibt, können Sie sich die vom eingebetteten Browser des Programms gesendeten Anfragen ansehen.
Anweisungen zur Ansicht dieser Anfragen finden Sie im [Abschnitt zu SAML](#da-connection-issue-with-saml-aem).

#### SAML-Anmeldeauthentifizierung funktioniert nicht {#da-connection-issue-with-saml-aem}

Wenn das [!DNL Experience Manager]-Desktop-Programm keine Verbindung zu Ihrer SSO-fähigen (SAML) [!DNL Adobe Experience Manager]-Instanz herstellt, lesen Sie diesen Abschnitt, um eine Fehlerbehebung durchzuführen. SSO-Prozesse sind vielfältig, manchmal komplex und das Design des Programms versucht, diese Arten von Verbindungen zu unterstützen. Einige Setups erfordern jedoch eine zusätzliche Fehlerbehebung.

Manchmal leitet der SAML-Prozess nicht zum ursprünglich angeforderten Pfad zurück oder die endgültige Umleitung erfolgt zu einem Host, der sich von dem unterscheidet, was im [!DNL Adobe Experience Manager]-Desktop-Programm konfiguriert wurde. So stellen Sie sicher, dass dies nicht der Fall ist:

1. Öffnen Sie einen Webbrowser. Zugriff auf die URL `https://[aem_server]:[port]/content/dam.json`.

1. Melden Sie sich bei der [!DNL Adobe Experience Manager]-Bereitstellung an.

1. Wenn die Anmeldung abgeschlossen ist, sehen Sie sich die aktuelle Adresse des Browsers in der Adressleiste an. Sie sollte genau mit der ursprünglich von Ihnen eingegeben URL übereinstimmen.

1. Überprüfen Sie außerdem, ob alles vor `/content/dam.json` mit dem Zielwert von [!DNL Adobe Experience Manager], der in den Einstellungen des [!DNL Adobe Experience Manager]-Desktop-Programms konfiguriert ist, übereinstimmt.

**Der SAML-Anmeldeprozess funktioniert gemäß den oben genannten Schritten korrekt, aber die Benutzer können sich trotzdem nicht anmelden**

Das Fenster innerhalb des [!DNL Adobe Experience Manager] Desktop-Programms, in dem der Anmeldevorgang angezeigt wird, ist lediglich ein Webbrowser, in dem die Web-Benutzeroberfläche der Zielinstanz von [!DNL Adobe Experience Manager] angezeigt wird:

* Die Mac-Version verwendet eine [WebView](https://developer.apple.com/documentation/webkit/webview).

* Die Windows-Version verwendet Chromium-basiertes [CefSharp](https://cefsharp.github.io/).

Stellen Sie sicher, dass der SAML-Prozess diese Browser unterstützt.

Zur weiteren Fehlerbehebung können die exakten URLs, die der Browser zu laden versucht, angezeigt werden. So sehen Sie diese Informationen:

1. Befolgen Sie die Anweisungen zum Starten des Programms im [Debug-Modus](#enable-debug-mode).

1. Reproduzieren Sie den Anmeldeversuch.

1. Navigieren Sie zum [Protokollverzeichnis](#check-log-files-v2) des Programms

1. Für Windows:

   1. Öffnen Sie „aembegleitonlog.txt“.

   1. Suchen Sie nach Meldungen, die mit „Login browser address changed to“ beginnen. Diese Einträge enthalten auch die URL, die das Programm geladen hat.

   Für Mac:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`, wobei die **n** durch die Zahlen ersetzt werden, die im neuesten Dateinamen stehen.

   1. Suchen Sie nach Meldungen, die mit „loaded frame“ beginnen. Diese Einträge enthalten auch die URL, die das Programm geladen hat.


Wenn Sie sich die URL-Sequenz ansehen, die geladen wird, können Sie die Fehlerbehebung am SAML-Ende durchführen, um festzustellen, was falsch ist.

#### Problem bei SSL-Konfiguration {#ssl-config-v2}

Die Bibliotheken, die die Experience Manager-Desktop-App für die HTTP-Kommunikation verwendet, verwenden eine strikte SSL-Durchsetzung. Manchmal kann es bei der Verwendung eines Browsers erfolgreich sein, wenn die Desktop-App von Experience Manager verwendet wird. Installieren Sie für eine ordnungsgemäße SSL-Konfiguration das fehlende Zwischenzertifikat in Apache. Siehe [How to install an Intermediate CA cert in Apache](https://access.redhat.com/solutions/43575) (nur auf Englisch verfügbar).

Die Bibliotheken, die Experience Manager Desktop für die HTTP-Kommunikation verwendet, verwenden eine strikte SSL-Durchsetzung. Es kann also Fälle geben, in denen SSL-Verbindungen, die über einen Browser erfolgreich sind, mit dem [!DNL Adobe Experience Manager]-Desktop-Programm fehlschlagen. Dies ist gut, da es die korrekte Konfiguration von SSL fördert und die Sicherheit erhöht, kann aber frustrierend sein, wenn das Programm keine Verbindung herstellen kann.

Der empfohlene Ansatz in diesem Fall besteht darin, ein Tool zu verwenden, um das SSL-Zertifikat eines Servers zu analysieren und Probleme zu identifizieren, damit diese korrigiert werden können. Es gibt Websites, die das Zertifikat eines Servers bei der Übermittlung seiner URL überprüfen.

Als vorübergehende Maßnahme ist es möglich, die strikte SSL-Durchsetzung im [!DNL Adobe Experience Manager]-Desktop-Programm zu deaktivieren. Dies ist keine empfohlene langfristige Lösung, da dadurch die Sicherheit verringert wird, indem die Ursache für falsch konfigurierte SSL ausgeblendet wird. So deaktivieren Sie die strikte Durchsetzung:

1. Verwenden Sie den Editor Ihrer Wahl, um die JavaScript-Konfigurationsdatei des Programms zu bearbeiten, die (standardmäßig) an den folgenden Speicherorten (je nach Betriebssystem) zu finden ist:

   Unter macOS: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   Unter Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. Suchen Sie den folgenden Abschnitt in der Datei:

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. Ändern Sie den Abschnitt, indem Sie `"strictSSL": false` wie folgt hinzufügen:

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. Speichern Sie die Datei und starten Sie das [!DNL Adobe Experience Manager]-Desktop-Programm neu.

### Das Programm reagiert nicht {#unresponsive}

In seltenen Fällen reagiert das Programm möglicherweise nicht mehr, zeigt nur einen weißen Bildschirm an oder zeigt einen Fehler am unteren Rand der Benutzeroberfläche an, ohne dass Optionen auf der Benutzeroberfläche vorhanden sind. Versuchen Sie Folgendes in genannter Reihenfolge:

* Klicken Sie mit der rechten Maustaste auf die Programmoberfläche und klicken Sie auf **[!UICONTROL Refresh]**.
* Beenden Sie das Programm und starten Sie es erneut.

Bei beiden Methoden startet das Programm im Stammordner des DAM.

<!--
### Need additional help with [!DNL Experience Manager] desktop app {#additional-help}

Create Jira ticket with the following information:

* Use `DAM - Companion App` as the [!UICONTROL Component].

* Detailed steps to reproduce the issue in [!UICONTROL Description].

* DEBUG level logs that were captured while reproducing the issue.

* Target Experience Manager version.

* Operating system version.

* [!DNL Adobe Experience Manager] desktop app version. To know your app version, see [finding the desktop app version](#know-app-version-v2).
-->

>[!MORELIKETHIS]
>
>* [Bekannte Probleme](release-notes.md#known-issues-v2)
>* [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts)

