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
source-git-commit: 381e586077c7db63dd57a468b1c6abc60c63e34e
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 70%

---


# Fehlerbehebung für das Adobe Experience Manager-Desktop-Programm {#troubleshoot-v2}

Das Adobe Experience Manager-Desktop-Programm (AEM) stellt eine Verbindung zum Digital Asset Management-Repository (DAM) einer Remote-Bereitstellung von Experience Manager her. Das Programm ruft Repository-Informationen und Suchergebnisse auf Ihrem Computer ab, lädt Dateien und Ordner herunter und lädt sie hoch und bietet Funktionen zum Verwalten von Konflikten mit der Benutzeroberfläche von AEM Assets.

Lesen Sie weiter, um Fehler im Programm zu beheben, lernen Sie die Best Practices kennen und erfahren Sie mehr über Einschränkungen.

## Best Practices {#best-practices-to-prevent-troubles}

Befolgen Sie die folgenden Best Practices, um einige häufige Probleme und die Fehlerbehebung zu vermeiden.

* **So funktioniert das Desktop-Programm**: Bevor Sie mit der Verwendung des Programms beginnen, sollten Sie sich kurz mit ihrer Funktionsweise vertraut machen. Erfahren Sie mehr über Verknüpfung zwischen der Web-Oberfläche von Experience Manager und dem Desktop-Programm, Repository-Zuordnung, Asset-Zwischenspeicherung, lokales Speichern und Hochladen im Hintergrund. Machen Sie sich mit der [Funktionsweise](release-notes.md#how-app-works) vertraut:

* **Vermeiden Sie nicht unterstützte Zeichen in Ordnernamen**: Verwenden Sie beim Erstellen oder Hochladen von Ordnern keine Leerzeichen und ungültige Zeichen. Eine Liste der Zeichen finden Sie unter [Erstellen von Ordnern in Experience Manager Assets](https://docs.adobe.com/content/help/de-DE/experience-manager-65/assets/managing/managing-assets-touch-ui.html#Creatingfolders). In einigen Adobe Experience Manager-Anwendungsfällen können durch nicht unterstützte Zeichen im Ordnernamen Probleme auftreten.

* **Best Practices zur Vermeidung von Konflikten**: Um mögliche Konflikte bei der Zusammenarbeit mit mehreren Assets zu vermeiden, lesen Sie [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Verwenden Sie den Ordner-Upload für große, hierarchische Ordner**: Verwenden Sie anstelle der Assets-Web-Oberfläche oder anderer Methoden das Experience Manager-Desktop-Programm, um große Ordner hochzuladen. Das Programm lädt die Assets mit Protokollierung und Überwachung im Hintergrund hoch. Siehe [Massen-Upload von Assets](using.md#bulk-upload-assets).

* **Verwenden Sie die neueste Version**: Verwenden Sie die neueste Programmversion und prüfen Sie immer, ob die Kompatibilität gewährleistet ist, bevor Sie eine neue Programmversion installieren oder bevor Sie auf eine neuere Adobe Experience Manager-Version aktualisieren. Siehe [Versionshinweise](release-notes.md).

* **Verwenden Sie denselben Laufwerksbuchstaben**: Verwenden Sie in der gesamten Organisation denselben Laufwerksbuchstaben für Adobe Experience Manager DAM. Damit von anderen Benutzern platzierte Assets angezeigt werden können, müssen die Pfade identisch sein. Mit demselben Laufwerksbuchstaben wird ein konstanter Pfad zu DAM-Assets sichergestellt. Die Assets bleiben platziert und werden auch dann nicht entfernt, wenn verschiedene Laufwerksbuchstaben von verschiedenen Benutzern verwendet werden.

* **Beachten Sie das Netzwerk**: Die Netzwerkleistung ist von entscheidender Bedeutung für die Leistung des Experience Manager-Desktop-Programms. Wenn die Reaktion auf Dateiübertragungen oder Massenvorgänge verlangsamt ist, deaktivieren Sie die Funktionen oder Applikationen, die zu viel Netzwerkverkehr führen können.

* **Vom Desktop-Programm nicht unterstützte Anwendungsfälle**: Verwenden Sie das Programm nicht für die Asset-Migration (diese muss gründlich geplant werden und erfordert andere Tools), anspruchsvolle DAM-Operationen (z. B. Verschieben großer Ordner, Uploads großer Dateien, Suchen von Dateien anhand erweiterter Metadaten-Suchen) oder als Synchronisierungs-Client (Design- und Nutzungsmuster unterscheiden sich von In-Sync-Clients wie Microsoft OneDrive oder Adobe Creative Cloud-Desktop-Synchronisierung).

* **Timeout**: Das Desktop-Programm weist derzeit keinen konfigurierbaren Timeout-Wert auf, um die Verbindung zwischen dem Experience Manager-Server und dem Programm nach einem bestimmten Zeitintervall zu trennen. Wenn beim Hochladen großer Assets nach einiger Zeit ein Verbindungs-Timeout eintritt, versucht das Programm, das Asset einige Male hochzuladen, indem es den Timeout-Wert für den Upload erhöht. Es gibt keine empfohlene Vorgehensweise, um die Standardeinstellungen für den Timeout zu ändern.

## Fehlerbehebung {#troubleshooting-prep}

Um Probleme mit dem Desktop-Programm zu beheben, beachten Sie die folgenden Informationen. Außerdem werden Sie darauf vorbereitet, die Probleme besser an die Adobe-Kundenunterstützung zu übermitteln, wenn Sie sich für den Support entscheiden.

### Aktivieren des Debugging-Modus {#enable-debug-mode}

Zur Fehlerbehebung können Sie den Debug-Modus aktivieren und weitere Informationen in den Protokollen abrufen.

>[!NOTE]
>
>Gültige Protokollebenen sind DEBUG, INFO, WARN oder FEHLER. Die Ausführlichkeit der Protokolle ist im DEBUG am höchsten und im FEHLER am niedrigsten.

So verwenden Sie die App im Debug-Modus unter Mac:

1. Öffnen Sie ein Terminalfenster oder eine Eingabeaufforderung.

1. Starten Sie die [!DNL Experience Manager] Desktop-App, indem Sie den folgenden Befehl ausführen:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

So aktivieren Sie den Debug-Modus unter Windows:

1. Öffnen Sie ein Befehlsfenster.

1. Starten Sie die [!DNL Experience Manager] Desktop-App, indem Sie den folgenden Befehl ausführen:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### Speicherort der Protokolldateien {#check-log-files-v2}

[!DNL Experience Manager] Die Desktop-App speichert ihre Protokolldateien je nach Betriebssystem an den folgenden Speicherorten:

Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Unter Mac OS: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

Wenn beim Hochladen vieler Assets einige Dateien nicht hochgeladen werden können, finden Sie in der Datei `backend.log` Informationen zu den fehlgeschlagenen Uploads.

>[!NOTE]
>
>Wenn Sie bei einer Supportanfrage oder einem Ticket mit der Kundenunterstützung der Adobe arbeiten, können Sie gebeten werden, die Protokolldateien freizugeben, damit das Kundendienstteam das Problem besser verstehen kann. Archivieren Sie den gesamten Ordner `Logs` und geben Sie ihn für Ihre Kontaktperson bei der Kundenunterstützung frei.

### Löschen des Cache {#clear-cache-v2}

Beim Löschen des Caches von handelt es sich um eine vorläufige Aufgabe zur Fehlerbehebung, durch die verschiedene Probleme mit dem AEM-Desktop-Programm gelöst werden können. Löschen Sie den Cache in den Programm-Voreinstellungen. Siehe [Festlegen von Voreinstellungen](install-upgrade.md#set-preferences). Der Standardspeicherort des Cache-Ordners ist:

* Unter Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Unter Mac OS: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Das Verzeichnis kann sich jedoch in Abhängigkeit vom konfigurierten AEM-Endpunkt des AEM-Desktop-Programms ändern. Der Wert ist eine codierte Version der Ziel-URL. Wenn das Ziel des Programms beispielsweise `http://localhost:4502` ist, lautet der Verzeichnisname `http%3A%2F%2Flocalhost%3A4502%2F`. Um den Cache zu leeren, löschen Sie den entsprechenden Ordner. Ein weiterer Grund, den Cache zu leeren, besteht darin, Speicherplatz freizugeben, wenn Sie wenig Speicherplatz auf der Festplatte haben.

>[!CAUTION]
>
>Wenn Sie den AEM-Desktop-Cache löschen, gehen dabei nicht mit AEM synchronisierte Änderungen lokaler Assets unwiderruflich verloren.

### Ermitteln der AEM-Desktop-Programm-Version {#know-app-version-v2}

Klicken Sie auf das ![Programmmenü](assets/do-not-localize/more_options_da2.png), um das Menü des Programms zu öffnen, und klicken Sie auf **[!UICONTROL Help]** > **[!UICONTROL About]**.

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

## [!DNL Experience Manager] Verbindungsprobleme mit Desktop-Apps {#connection-issues}

### SAML-Anmeldeauthentifizierung funktioniert nicht {#da-connection-issue-with-saml-aem}

Wenn die [!DNL Experience Manager] Desktop-App keine Verbindung zu Ihrer SSO-aktivierten [!DNL Adobe Experience Manager] Instanz (SAML) herstellt, lesen Sie diesen Abschnitt, um eine Fehlerbehebung durchzuführen. SSO-Prozesse sind vielfältig, manchmal komplex, und das Design der Anwendung bietet das Beste, um diese Arten von Verbindungen aufzunehmen. Einige Setups erfordern jedoch eine zusätzliche Fehlerbehebung.

Manchmal leitet der SAML-Prozess nicht zum ursprünglich angeforderten Pfad zurück, oder die endgültige Umleitung erfolgt zu einem Host, der sich von dem unterscheidet, was in der [!DNL Adobe Experience Manager] Desktop-App konfiguriert wurde. So überprüfen Sie, ob dies nicht der Fall ist:

1. Öffnen Sie einen Webbrowser.

1. Geben Sie die URL `<AEM host>/content/dam.json` in die Adressleiste ein.

   Ersetzen Sie `<AEM host>` dies beispielsweise durch die Zielgruppe- [!DNL Adobe Experience Manager] Instanz `http://localhost:4502/content/dam.json`.

1. Log in to the [!DNL Adobe Experience Manager] instance.

1. Wenn die Anmeldung abgeschlossen ist, sehen Sie sich die aktuelle Adresse des Browsers in der Adressleiste an. Er sollte exakt mit der URL übereinstimmen, die ursprünglich eingegeben wurde.

1. Überprüfen Sie außerdem, ob alle zuvor `/content/dam.json` festgelegten Werte mit dem in den Einstellungen der [!DNL Adobe Experience Manager] Desktop-App konfigurierten [!DNL Adobe Experience Manager] Wert für die Zielgruppe übereinstimmen.

**Der SAML-Anmeldeprozess funktioniert gemäß den oben genannten Schritten korrekt, aber die Benutzer können sich trotzdem nicht anmelden**

Das Fenster innerhalb der [!DNL Adobe Experience Manager] Desktop-App, in dem der Anmeldevorgang angezeigt wird, ist lediglich ein Webbrowser, in dem die Webbenutzeroberfläche [!DNL Adobe Experience Manager] der Instanz der Zielgruppe angezeigt wird:

* Die Mac-Version verwendet eine [WebView](https://developer.apple.com/documentation/webkit/webview).

* Die Windows-Version verwendet Chromium-basiertes [CefSharp](https://cefsharp.github.io/).

Stellen Sie sicher, dass der SAML-Prozess diese Browser unterstützt.

Zur weiteren Fehlerbehebung können die exakten URLs, die der Browser zu laden versucht, Ansicht werden. So sehen Sie diese Informationen:

1. Befolgen Sie die Anweisungen zum Starten der Anwendung im [Debug-Modus](#enable-debug-mode).

1. Reproduzieren Sie den Anmeldeversuch.

1. Navigieren Sie zum [Protokollverzeichnis](#check-log-files-v2) der Anwendung

1. Für Windows:

   1. Öffnen Sie &quot;aembegleitonlog.txt&quot;.

   1. Suchen Sie nach Meldungen, die mit &quot;Login-Browser-Adresse geändert zu&quot;beginnen. Diese Einträge enthalten auch die URL, die die Anwendung geladen hat.

   Mac:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`, wobei das **n** durch die Nummern ersetzt wird, die im neuesten Dateinamen stehen.

   1. Suchen Sie nach Meldungen, die mit &quot;loaded frame&quot;beginnen. Diese Einträge enthalten auch die URL, die die Anwendung geladen hat.


Wenn Sie sich die URL-Sequenz ansehen, die geladen wird, können Sie die Fehlerbehebung am SAML-Ende durchführen, um festzustellen, was falsch ist.

### Problem bei SSL-Konfiguration {#ssl-config-v2}

Die Bibliotheken, die das AEM-Desktop-Programm zur HTTP-Kommunikation nutzt, setzen auf strikte SSL-Durchsetzung. Mitunter kann zwar über einen Browser eine Verbindung erfolgreich hergestellt werden, aber nicht über das AEM-Desktop-Programm. Installieren Sie für eine ordnungsgemäße SSL-Konfiguration das fehlende Zwischenzertifikat in Apache. Siehe [How to install an Intermediate CA cert in Apache](https://access.redhat.com/solutions/43575) (nur auf Englisch verfügbar).

## Das Programm reagiert nicht {#unresponsive}

In seltenen Fällen reagiert das Programm möglicherweise nicht mehr, zeigt nur einen weißen Bildschirm an oder zeigt einen Fehler am unteren Rand der Benutzeroberfläche an, ohne dass Optionen auf der Benutzeroberfläche vorhanden sind. Versuchen Sie Folgendes in genannter Reihenfolge:

* Klicken Sie mit der rechten Maustaste auf die Programmoberfläche und klicken Sie auf **[!UICONTROL Refresh]**.
* Beenden Sie das Programm und starten Sie es erneut.

Bei beiden Methoden startet das Programm im Stammordner des DAM.

>[!MORELIKETHIS]
>
>* [Bekannte Probleme](release-notes.md#known-issues-v2)
>* [Vermeiden von Bearbeitungskonflikten](using.md#adv-workflow-collaborate-avoid-conflicts)

