---
title: Versionshinweise zur AEM-Desktop-App für Version 1.x
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für AEM Desktop-App Version 1.x.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 850d2c21a796599ed40164e7d6f892967563c16b

---


# Versionshinweise zur AEM-Desktop-App Version 1.x{#aem-desktop-app-release-notes}

## Versionshinweise {#release-information}

| Produkte | Adobe Experience Manager (AEM)-Desktop-App |
|---------------|--------------------------------------------------------------------|
| Version | 1.10 (1.10.0.3 unter Mac und Windows) |
| Typ | Nebenversion |
| Datum | 31. August 2018 |
| Download-URLs | [Mac OS X 64 Bit](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-1.10.0.3.dmg); 32 [Bit](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-1.10.0.3.exe)Windows; 64 Bit [Windows](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-1.10.0.3.exe) |
| Kompatibilität | AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |

>[!NOTE]
>
>Die Cachegrößenbeschränkung wird nicht erzwungen. Beim Starten der Desktop App wird die Cachegröße einmal berechnet und es wird eine Benachrichtigung angezeigt, wenn sich die Größe der vordefinierten Beschränkung nähert.

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites}

AEM Desktop ist mit den folgenden Betriebssystemen kompatibel:

* Mac OS X 10.10 oder höher mit aktuellen Fehlerbehebungen.
* Windows7 und Windows 10 mit den neuesten Service Packs und Fehlerbehebungen.

Adobe empfiehlt dringend, die neueste Version von AEM Desktop zu verwenden, um die neuesten Funktionen mit den neuesten Fehlerkorrekturen und der bestmöglichen Leistung zu nutzen.

Für die Version der AEM Desktop App, die Sie auf Ihrem lokalen Computer installieren möchten, sind eine bestimmte Version von AEM-Server oder zusätzliche serverseitige Komponenten (Service Packs, Hotfixes oder Feature Packs) erforderlich. Stellen Sie sicher, dass der AEM-Server ordnungsgemäß konfiguriert ist, bevor Sie zum ersten Mal eine Verbindung herstellen. Wenn Sie Hilfe benötigen, wenden Sie sich an Ihren AEM-Administrator.

See the [detailed compatibility matrix](#compatibilitymatrix) at the end of this document to evaluate the prerequisites for your setup.

## What's New in AEM desktop app 1.10 {#what-s-new-in-aem-desktop-app}

Die AEM-Desktop-App 1.10 konzentriert sich auf die Verbesserung der Benutzererfahrung bei großen Uploads, Informationen zu Hintergrundvorgängen und optimierte Benutzererfahrung beim Öffnen von Assets mit verknüpften Dateien (z. B. InDesign).

**Lokale Bearbeitung/Auschecken**: Automatische Uploads von Änderungen, die in Assets gespeichert wurden, können im Statusfenster deaktiviert werden. So können Benutzer an Dateien arbeiten, die hierbei vorgenommenen Änderungen speichern und, wenn sie bereit sind, alle Änderungen hochladen.

**Vereinfachtes Asset-Statusfenster**: Das Statusfenster wurde vereinfacht. Die Registerkarte "Uploads"zeigt jetzt sowohl einzelne Assets als auch Ordner-/Massen-Uploads an. Die zuvor vorhandene Registerkarte „Massen-Uploads“ wurde entfernt.

**Anwendungssymbol zur Anzeige von Massen-Uploads**: Das Anwendungssymbol gibt an, dass ein Massen-Upload durchgeführt wird, indem das Overlay „Übertragung“ angezeigt wird.

**Benachrichtigungen für Aktualisierungskonflikte**: Wenn die Anwendung beim Versuch, ein Asset zu aktualisieren, einen Konflikt erkennt, wird eine Benachrichtigung angezeigt, sodass der Benutzer diesen überprüfen kann, ohne das Statusfenster überwachen zu müssen. Wenn die Anwendung startet, sucht sie nach potenziellen Konflikten, damit der Benutzer sie beheben kann.

**Besserer Umgang mit Verbindungsabbrüchen**: Massen-Uploads werden angehalten, wenn die Verbindung unterbrochen wird. Benutzer können sie zu einem späteren Zeitpunkt fortsetzen. Für fehlgeschlagene Uploads einzelner Dateien steht Benutzern die Schaltfläche „Wiederholen“ zur Verfügung.

## Installationsanweisungen {#installation-instructions}

For detailed instructions, see [Install and configure AEM desktop app](install-configure-app-v1.md).

## Verbesserungen in den vorherigen Versionen {#enhancements-in-the-previous-versions}

Diese Version erweitert und ersetzt die früheren Versionen der Experience Manager-Desktop-App, die die folgenden wichtigen Verbesserungen bieten:

* **Version 1.9/1.9.1**: Wiederverwendbare Uploads, verbessertes Statusfenster, Anwendungssymbole, die den Status der Anwendung/Verbindung angeben, Vorab-Abrufen verknüpfter Assets für InDesign-Dateien
* **Version 1.8**: bessere Steuerung der Cachegröße für den Benutzer, verbesserte Anmeldeerfahrung für SAML/SSO unter Windows, Unterstützung von .pac-Netzwerkproxy unter Mac und kundenbezogene Probleme.
* **Version 1.7**: Verbesserte Stabilität und Cache-Logik, bessere Unterstützung für Netzwerk-Proxy und Fähigkeit, interne Dateien nach der Deinstallation zu bereinigen.
* **** Version 1.6: Verbesserungen am Anmeldeprozess für verschiedene AEM-Sicherheitskonfigurationen sowie an der Applikationsstabilität und -leistung.
* **Version 1.5**: Anwendungsstabilität und Resilienz gegen verschiedene Netzwerkprobleme, bessere Supportabilität.
* **Version 1.4**: die Möglichkeit, hierarchische Ordner mit der Fortschrittsüberwachung im Hintergrund hochzuladen.
* **Version 1.3**: Leistungsverbesserungen und Stabilität beim Zugriff auf Dateien und Speichern von Änderungen an AEM, insbesondere von Creative Cloud-Desktop-Anwendungen wie InDesign, Illustrator oder Fotoshop. Diese Version sollte Benutzern ein Desktop-artiges Erlebnis bei der Arbeit mit Dateien bieten und gleichzeitig Übertragungsvorgänge für Netzwerkdaten im Hintergrund durchführen.

### Enhancements available since AEM desktop app 1.9 {#Enhancements-Available-Since-AEM-Desktop-App-19x}

Die Adobe Experience Manager (AEM)-Desktop-App 1.9.1 war eine Patch-Version, mit der einige wichtige Kundenprobleme beim Auschecken von Assets und Kopieren von Dateien von der Netzwerkfreigabe in einen lokalen Ordner behoben wurden.

* Assets, die von einem Benutzer ausgecheckt werden, sollten nicht für Bearbeitungen durch andere Benutzer verfügbar sein (CQ-4246009)
* Unterstützung des Kopierens von einem zugeordneten Ordner in einen lokalen Ordner, wenn sich der Benutzerordner auf einer separaten Laufwerkpartition befindet (CQ-4243978)

Die AEM-Desktop-App 1.9 hat sich auf die Verbesserung der Benutzererfahrung bei großen Uploads, Informationen zu Hintergrundvorgängen und optimierte Erlebnisse beim Öffnen von Assets mit verknüpften Dateien (wie InDesign) konzentriert.

**Uploads**wiederaufnehmen Für Uploads, insbesondere bei großen Dateien, gibt es eine Option, um sie im neuen Fenster "Asset-Status"anzuhalten/fortzusetzen.
**Fenster**"Asset-Status"Ein verbessertes Fensterzum Asset-Status bietet Informationen zu Assets, die folgende Elemente enthalten:
Änderungen

* Zeigt Änderungen an, die sich momentan in der Warteschlange befinden
* Zeigt laufende Upload-Vorgänge an, einschließlich eines Fortschrittsbalkens, der Übertragungsrate, der Dateigesamtgröße und der bislang übertragenen Größe
* Abgeschlossene Uploads werden mit der übertragenen Datenmenge und der Übertragungsrate angezeigt
* Fehlgeschlagene Uploads werden zusammen mit einer Fehlermeldung und Übertragungsinformationen angezeigt, sofern verfügbar
* Für 3-mal fehlgeschlagene Uploads wird eine Fehlermeldung angezeigt
* Für in Konflikt stehende Dateien wird ein Symbol angezeigt, auf das der Benutzer klicken kann. Durch das Klicken auf das Symbol wird ein Dialogfeld mit einer Erklärung und zwei Optionen angezeigt:
   * „Keep Mine“ (Meine behalten): lädt die Datei sofort auf den Server hoch
   * „Overwrite Mine“ (Meine überschreiben): löscht die lokale Datei sofort und lädt eine neue Kopie vom Server herunter

Downloads

* Zeigt aktive Downloads an, einschließlich einer Übertragungsrate und der bislang übertragenen Größe
* Abgeschlossene Downloads werden mit der übertragenen Datenmenge, der Übertragungsrate und einem Symbol angezeigt, über das die Datei per Klick geöffnet wird (nur für einzelne Dateien verfügbar)
* Fehlgeschlagene Downloads werden mit einer Fehlermeldung und Übergangsinformationen angezeigt, sofern verfügbar
* In der Fußzeile werden die Gesamtzahl der heruntergeladenen Dateien und die durchschnittliche Übertragungsrate angezeigt.
* Wenn ein Benutzer mehrere Dateien über die AEM Assets-Webbenutzeroberfläche öffnet oder bearbeitet, werden sie zusammen gruppiert und beispielsweise als „meinasset.jpeg und 4 weitere Datei(en)“ angezeigt
* Beim Herunterladen von InDesign-Dokumenten einschließlich verknüpfter Assets, die in AEM Assets gespeichert sind, lädt die Desktop-App zunächst alle verknüpften Assets herunter, bevor Sie das InDesign-Dokument öffnen und den Download verknüpfter Assets angeben, z. B. (5 von 24)

Massenupload: Das Hochladen großer Ordnerhierarchien über "Erstellen"&gt; "Ordner in AEM-Web-Benutzeroberfläche hochladen"oder Kopieren und Auswählen von "Assets einfügen"im Finder/Explorer im Kontextmenü der Desktop-App löst die Verwendung dieses Dialogfelds aus:

* Zeigt aktive Uploads an, einschließlich eines Fortschrittsbalkens und des Namens der momentan übertragenen Datei
* Aktive Uploads beinhalten ein Symbol, über das der Upload per Klick abgebrochen wird. Die Übertragung endet, nachdem die aktuelle Dateiübertragung abgeschlossen ist
* Fehlgeschlagene Übertragungsprozesse werden mit einer Fehlermeldung angezeigt (nur, wenn die gesamte Übertragung fehlschlägt)
* Wenn die Übertragung einer einzelnen Datei fehlschlägt, wird sie auf der Registerkarte als Fehler angezeigt. Andernfalls werden einzelne Dateien nicht auf der Registerkarte * nur ein Eintrag für den gesamten Upload angezeigt.

**Symbole zur Angabe des Status von Hintergrundoperationen** Das Anwendungssymbol zeigt den Status der Hintergrundvorgänge an, um den Benutzern einen besseren visuellen Hinweis zu geben. Wenn die Anwendung beispielsweise nicht mit AEM verbunden ist, wird das Symbol grau ausgeblendet, wenn ein aktiver Upload erfolgt, wird eine Synchronisierungs-Überlagerung angezeigt usw.

**Vorab-Abrufen von verknüpften Assets**Um die Benutzererfahrung beim Arbeiten mit InDesign-Dokumenten zu verbessern, die in AEM gespeicherte verknüpfte Assets enthalten, versucht die Desktop-App, diese verknüpften Dateien vor dem Herunterladen in den lokalen Cache abzurufen, bevor das InDesign-Dokument geöffnet wird. Somit stehen dem Benutzer die verknüpften Dateien lokal zur Verfügung und er muss beim Zugriff auf diese Dateien in InDesign (im Bereich „Verknüpfungen“) nicht länger warten.
Beachten Sie, dass der Vorab-Abruf nur funktioniert, wenn AEM die Verknüpfungen auf der Serverseite erkennt. Für ein Asset mit erkannten Verknüpfungen wird in der Ansicht „Eigenschaften“ des InDesign-Assets die Liste „Verweise“ aufgeführt.

### Enhancements Available Since AEM desktop app 1.8.x{#enhancements-available-since-aem-desktop-app-18x}

Die AEM-Desktop-App 1.8.1 mit der schnellen Veröffentlichung hat Verbesserungen beim gleichzeitigen Öffnen mehrerer Dateien von der AEM-Benutzeroberfläche bis zur Version 1.8 hinzugefügt (CQ-4237747, CQ-4238780). Verbesserungen in AEM Desktop App 1.8:

* Zwischenspeichern: neue Benutzeroberfläche zum Verwalten des AEM-Cache für Desktop-Apps (CQ-4208690), einschließlich
   * Aktuelle Cachegröße anzeigen
   * Maximale Cachegröße definieren, bevor eine Benachrichtigung gesendet wird
   * Die Cachegröße wird nur beim Start der Desktop-App überprüft und es wird eine Benachrichtigung angezeigt, wenn die konfigurierte Grenze erreicht wird
   * Auf der neuen Benutzeroberfläche ist eine Schaltfläche zum Löschen des Caches verfügbar
* Anmeldung: (Win) Die Anmeldung bei der AEM-Instanz, die für die Verwendung von SAML und SSL konfiguriert wurde, wurde korrigiert (CQ-4216353)
* Netzwerk:
   * Beim Ablauf einer AEM-Sitzung wird der Benutzer entsprechend benachrichtigt und er kann auf die Benachrichtigung klicken, um sich erneut anzumelden (CQ-4202028)
   * (Mac) Fügen Sie Unterstützung für die Verbindung mit AEM über die Pac-Proxykonfiguration hinzu (CQ-4233430)
   * (Win) Beheben von Problemen mit dem Dialogfeld "Erweiterte URL-Anmeldung"(CQ-4236061)
* Fehlerbehebungen:
   * Mehr Asset-Info-Dialogfeld * manchmal war die Aktionsleiste nicht sichtbar (CQ-4208540)
   * (Win) Die Datei kann jetzt synchronisiert werden, nachdem von der Benutzeroberfläche von AEM Assets eine frühere Version wiederhergestellt wurde (CQ-4216411)

### Enhancements Available Since AEM desktop app 1.7{#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabilität:
   * Verbesserte Stabilität bei der Verbindung der AEM-Desktop-App mit einem überladenen AEM-Server (CQ-4224803)
   * Verbesserte Stabilität, wenn viele Dateien angefordert werden (CQ-4224212)
   * Verbesserte Asset-Aktualisierung mit zusätzlicher Prüfung (CQ-4228291)
* Caching:
   * Behobene Festplattenfehler und Probleme beim Öffnen von Dateien in Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717)
   * Verbesserte Zwischenspeicherung zur Vermeidung von Binärdateien mit Größe null (CQ-4216599)
* Anmeldung: Ermöglicht die Verbindung mit für spezielle Konfigurationen deaktiviertem strictSSL (z. B. lokal ausgestellte Zertifikate) (CQ-4223949)
* Vernetzung: Verbesserte Unterstützung für die Verbindung über einen Netzwerkproxy (CQ-4223477, CQ-4221280, CQ-4206854)
* Installation und Deinstallation:
   * (Win) Cleaner Deinstallation (CQ-4220906)
   * [Windows 32bit] Installer schlägt bei der Installation von Microsoft .NET Framework v. 4.5 fehl (CQ-4218084)
   * (Mac) Manuelles Skript zum vollständigen Entfernen von Desktop-App-Dateien (CQ-4216489)

>[!NOTE]
>
>Probleme, die beim Laden der AEM-Desktop-App 1.7 als Beta-Version gefunden wurden (die in Version 1.6 nicht vorhanden waren, werden in den Versionshinweisen nicht aufgeführt).

### Enhancements Available Since AEM desktop app 1.6{#Enhancements-Available-Since-AEM-Desktop-App-16}

* Dokumentation: Neue [Best Practices für die App](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-desktop-app-best-practices.html) -Dokumentation der Version 1.x.
* Verbesserter Anmeldeprozess für AEM:
   * Verbessern Sie den SAML-Umgang * Regeln zur Entspannung (CQ-4202781).
   * Zusätzliche Funktion zum Konfigurieren einer separaten Anmelde-URL in den Einstellungen (CQ-4214052, CQ-4214051).
* Benutzerfreundlichkeit: Benachrichtigen Sie den Benutzer, wenn das Asset noch für größere Assets heruntergeladen wird (CQ-4216284).
* Netzwerke:
   * DNS-Caching (CQ-4210176).
   * Unterstützung für Verbindung über Proxy unter Windows (CQ-4206854).
* Zwischenspeicherung und Zugriff auf Netzwerkfreigabe in Finder/Explorer:
   * Das Sperrsymbol ist jetzt für ausgecheckte Assets unter Windows 10 (CQ-90957) sichtbar.
   * Ordnerinhalte verschwinden möglicherweise in Network Share (CQ-4209160, CQ-4210180).
   * Fehler beim Hochladen von Dateien aufgrund eines Konflikts, der im Status der Upload-Warteschlange (CQ-4215727) gemeldet wurde.
   * Beim Öffnen mehrerer Dateien aus dem Desktop-App-Ordner in PS werden möglicherweise abgeschnittene oder unvollständige Meldungen angezeigt (CQ-4216276).
* Fehlerbehebungen in Stabilität und Leistung:
   * Verbesserte Leistung beim Durchsuchen von Ordnern mit vielen Assets (CQ-4214933).
   * Die Desktop-App 1.5 kann den Desktop-Computer im Laufe der Zeit verlangsamen (CQ-4209159).
   * Die Funktion zum Anzeigen des Warteschlangenstatus funktioniert nur für den Benutzer, der die App installiert hat (CQ-4212199).
   * (Windows) Stellen Sie sicher, dass das 32-Bit-Installationsprogramm keinen 64-Bit-Code enthält (CQ-4217406).
* Ausgewählte Probleme, die in Beta 1.6 gefunden und behoben wurden:
   * Hohe CPU-Auslastung (CQ-4218070).
   * Drag &amp; Drop-Dateien mit Fehler beim Hochladen auf AEM (CQ-4217006).

### Enhancements Available Since AEM desktop app 1.5{#Enhancements-Available-Since-AEM-Desktop-App-15}

**** Version 1.5.1.5 für Mac OS X: Die Version 1.5.1.5 bietet folgende Vorteile:

* Neue Funktionen und Verbesserungen: Fügen Sie der Finder-Integration die Funktion zum Kopieren/Einfügen hinzu, um eine direkte Übertragung von Desktop zu AEM zu ermöglichen (CQ-4208158)
* Fehlerbehebungen:
   * Problem aufgrund von Fehler 43 behoben, das in einigen Fällen beim Umbenennen von Assets aufgetreten ist (CQ-4207900).
   * Beim Zurückkehren zu einer älteren Version aus der Zeitleiste in AEM wird das Asset im Finder nicht aktualisiert (CQ-4205194)
   * Desktop-App stürzt beim Durchsuchen großer verschachtelter Ordner ab (CQ-4208539)
   * Der Bereitstellungspunkt für die Desktop-App ist jetzt /Volumes/DAM, sodass er für alle Benutzer konsistent ist (CQ-4208159)
   * Beim erstmaligen Platzieren einer Datei in InDesign wird eine Update-Warnung angezeigt (CQ-4207454).

Hinweis zu Linkwarnungen: Creative Cloud-Anwendungen (z. B. InDesign) erstellen einen "Schnappschuss"der letzten Änderung des Elements zum Zeitpunkt seiner Platzierung. Ändert sich dieses Datum zu einem späteren Zeitpunkt, meldet die Adobe Creative Cloud-App, dass die Links veraltet sind. Dies wird auf unterschiedliche Weise gemeldet:

* Wenn die Adobe Creative Cloud-App gestartet wird, wird ein Dialogfeld angezeigt, in dem der Benutzer darüber informiert wird, dass die verknüpften Assets veraltet sind, und der Benutzer aufgefordert, Maßnahmen zu ergreifen.
* Wenn die Adobe Creative Cloud-App bereits ausgeführt wird, wird ein gelbes Dreieckswarnsymbol für das verknüpfte Asset angezeigt.

Dies gilt gleichermaßen für Assets auf lokalen Festplatten und Assets in einem von AEM Desktop bereitgestellten Verzeichnis, mit folgenden Ausnahmen:

* Wenn ein platziertes Asset von einem anderen Benutzer geändert wird, erscheint das Warnsymbol beim ersten Mal, wenn andere Benutzer ein Dokument mit dem platzierten Asset öffnen. Dies geschieht nur, wenn das platzierte Asset bereits lokal zwischengespeichert wurde..
* Wenn ein Benutzer ein platziertes Asset über den gemounteten Ordner des AEM-Desktops ändert und dann den lokalen Cache löscht, wird das platzierte Asset als veraltet gemeldet.

Diese beiden Fälle treten erwartungsgemäß ein. Sie sind auf die „Delayed Sync“-Architektur von AEM Desktop zurückzuführen.

**** Version 1.5.0.x für Mac OS X und Windows: Diese Version der AEM-Desktop-App bietet die folgenden Vorteile:

* Bessere Stabilität und Widerstandsfähigkeit gegen Netzwerkprobleme
   * stabilere Zuordnung von AEM Assets-Ordnern (CQ-103276, CQ-4204669, CQ-4203957)
   * Besseres Handling zwischengespeicherter Dateien (CQ-4204336, CQ-4206263)
   * Verbesserte Handhabung beim Herunterladen/Hochladen großer Dateien mit einer Größe von mehr als 2 GB (CQ-4206438)
   * Behebung von Fehler 36 beim Verschieben oder Umbenennen einer großen Anzahl von Dateien im Finder (CQ-4204640)
* Optimierungen in der Netzwerkkommunikation mit AEM Server (CQ-4204974, CQ-100903)
* Verbesserte Zuverlässigkeit beim Öffnen, Platzieren und Speichern von AEM-Assets in Creative Cloud-Apps (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980)
* Verbesserte Unterstützung: Option zum Löschen des Cache (CQ-4202541), einfacher Zugriff auf Protokolle (CQ-4202340, CQ-4204673)
* Weitere Fehlerbehebungen:
   * Bessere Unterstützung für Assets und Ordner mit japanischen Zeichen in den Einstellungen für Name/Nicht-Englisch (CQ-4195433, CQ-4205793, CQ-4199446)
   * Besseres Handling der Anmeldung mit SSL (CQ-4200217)
   * Zuverlässigere Freigabebereitstellung (CQ-4200793)
   * Verschiedene Verbesserungen der Stabilität (CQ-4207539, CQ-4200378)
   * Besseres Handling von AEM Assets-URL in den Einstellungen (CQ-97388)

### Enhancements Available Since AEM desktop app 1.4{#Enhancements-Available-Since-AEM-Desktop-App-14}

* Vereinfachter Upload hierarchischer Ordner über die neue Aktion „Erstellen“ &gt; „Ordner hochladen“ in der Touch-optimierten Benutzeroberfläche
   * Aktion initiiert einen Vorgang zum Hochladen von Ordnern, der von der Desktop-App ausgeführt wird
   * Die Desktop App durchläuft die jeweilige Ordnerhierarchie auf dem Desktop im Hintergrund und lädt die Dateien in AEM Assets hoch.
   * Der Benutzer kann den Fortschritt im neuen Fenster für den Upload-Warteschlangen-Status mithilfe des Fortschrittsbalkens für nicht abgeschlossene Vorgänge überwachen.
   * Der Status der Upload-Warteschlange bietet außerdem bessere Informationen zur Fehlerbehebung (z. B. keine Verbindung zum Server).
* Neue Aktion „Bearbeiten“ in der Touch-optimierten Benutzeroberfläche, die Vorgänge zum Auschecken und Öffnen kombiniert
* Optimierte Gruppierung von Desktop-bezogenen Aktionen in der Touch-optimierten Benutzeroberfläche (AEM 6.3)
* Verbesserte Kompatibilität mit den neuesten Betriebssystemversionen
* Fehlerbehebungen für von Kunden gemeldete Probleme

### Enhancements Available Since AEM desktop app 1.3{#Enhancements-Available-Since-AEM-Desktop-App-13}

* Höhere Effizienz. Netzwerkvorgänge werden schneller abgeschlossen und die Wartezeiten für Benutzer werden verkürzt.
* Verbesserte Finder-Integration, die für mehr Stabilität sorgt und den Zugriff auf Funktionen wie Miniaturansichten ermöglicht.
* Verbesserungen hinsichtlich der Zwischenspeicherung und Leistung.
* Bessere Unterstützung für das direkte Speichern aus Desktop-Applikationen (PS, ID, AI usw.).
* Verbesserte Integration mit Mac OS (Protokoll für lokale Netzwerklaufwerke geändert, statt WebDAV zuverlässigeres SMB1)..
* Die Desktop-App stellt eine Verbindung mit dem AEM-Server mithilfe des nativen Protokolls HTTP RESTful her.
* Die Dateien werden zunächst lokal gespeichert und nach einer festgelegten Zeit (30 Sek.) im Hintergrund wieder in AEM hochgeladen. Dadurch wird das Speichern von Dateien beschleunigt.
* Besseres Handling von Desktop-Applikationen, die Zwischenvorgänge zum Speichern von Dateien verwenden (partielles Speichern und temporäre Dateien). Dadurch können in der AEM Assets-Timeline korrekte Versions- und Asset-Upload-Informationen angezeigt werden.
* Dialogfeld zur Nachverfolgung des Status von im Hintergrund ausgeführten Upload-Aufgaben.

## Liste der Änderungen {#list-of-changes}

### Mount point on Mac {#mount-point-on-mac}

Mit Einführung von MacOS 10.12 (Sierra) hat Apple die Berechtigungen für den Ordner „/Volumes“ stärker eingeschränkt, der für die Bereitstellung von Netzwerklaufwerken und Geräten verwendet wird. Für das Erstellen eines neuen Bereitstellungspunkts waren Administratorrechte erforderlich. Dieses Problem wurde mit Einführung von MacOS 10.12.5 behoben.

Da die AEM-Desktop-App für Benutzer ausgeführt werden sollte, die keine Administratorrechte auf dem lokalen Computer haben, wurde der Bereitstellungspunkt für das AEM Assets-Repository in 1.4 und 1.5 in einen DAM-Unterordner im lokalen Ordner des Benutzers unter MacOS geändert (CQ-104183).

Da für den Ordner „/Volumes“ keine Administratorrechte mehr erforderlich sind, wurde diese Änderung mit Version 1.5.1 rückgängig gemacht. Dieses ermöglicht es zudem, InDesign-Dokumente mit platzierten AEM-Assets unter MacOS-Benutzern freizugeben.

### Protocol change (since v1.3) {#protocol-change-since}

* Mac OS X:
   * Das Protokoll für lokale Netzwerklaufwerke für die OS X-Desktop-Integration wurde von WebDAV in SMB1 geändert.
   * Das mit der Desktop-App bereitgestellte AEM-Repository wird als "smb"-Netzwerklaufwerk im Finder anstatt als WebDAV-Laufwerk angezeigt.
* Windows:
   * Das Protokoll für das lokale Netzwerklaufwerk für Windows-Desktop-Integrationen bleibt bestehen. AEM wird als WebDAV-Freigabe bereitgestellt.
* Für beide Plattformen (Windows und Mac):
   * Das Protokoll zum Zugriff auf/Download von Assets und zum Hochladen von Änderungen in AEM wurde in das AEM-native Protokoll geändert, bei dem es sich um ein HTTP-basiertes RESTful-Protokoll handelt. Es bietet eine bessere Kontrolle über Netzwerkvorgänge und eine bessere Kompatibilität mit der Netzwerkinfrastruktur.

>[!NOTE]
>
>Unter Mac OS X führt die Änderung des Protokolls des lokalen Netzwerklaufwerks von WebDAV in SMB1 zu einem anderen lokalen Pfad zu demselben Asset im Repository. Dies kann sich auf Links zu Dateien auswirken, die über den Befehl "Platzieren"in Adobe Creative Cloud-Anwendungen platziert wurden. Weitere Informationen finden Sie unter [Verwenden der AEM Desktop-App](use-app-v1.md) .

### Dateiverarbeitung (seit 1.3) {#file-handling-since}

* Ordner werden nach einer festgelegten Verzögerung (derzeit 30 Sek.) automatisch aktualisiert.
* Dateien, die von anderen Benutzern ausgecheckt wurden, sind als schreibgeschützt markiert.
* Die Dateien werden in zwei Phasen an einem Netzwerkspeicherort gespeichert, der über die Desktop-App gemountet wird.
* In der ersten Phase wird eine Datei lokal gespeichert. Auf diese Weise muss der Benutzer, der die Datei speichert, nicht warten, bis die Datei vollständig in AEM übertragen wurde, und kann seine Arbeit fortsetzen, sobald die Datei gespeichert wurde.
* In der zweiten Phase lädt die Desktop-App eine aktualisierte Datei nach einer vordefinierten Verzögerung (z. B. 30 s) auf den AEM-Server hoch. Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option **Status der Dateisynchronisierung im Hintergrund anzeigen**, um den Status des Upload-Vorgangs anzuzeigen.

## Wichtige Hinweise {#important-notices}

**Ordner-Upload.** Es empfiehlt sich, die neue Funktion zum Hochladen von Ordnern zu verwenden, um größere hierarchisch strukturierte Ordner in AEM hochzuladen, anstatt eine Kopie zu verwenden/sie per Drag-and-Drop in ein bereitgestelltes AEM-Repository von der Finder-/Explorer-Ebene zu ziehen. Wenn Sie die Funktion zum Hochladen von Ordnern verwenden, kommuniziert die Desktop-App direkt mit AEM und hat somit eine viel bessere Kontrolle über den gesamten Prozess.

**AEM-Sitzung aktivieren.** Die AEM-Desktop-App hängt von einer Sitzung ab, die auf dem AEM Assets-Server geöffnet ist, um den ordnungsgemäßen Betrieb sicherzustellen. Für Benutzer, die jeden Tag mit einer Desktop-App arbeiten, wird empfohlen, die Bereitstellung von AEM Assets am Ende des Tages aufzuheben, um die Abmeldung zu erzwingen, und dann morgens "AEM Assets hochladen", um sicherzustellen, dass sie angemeldet sind und die Netzwerkfreigabe betriebsbereit ist.

**Symbolvorschau im Finder deaktivieren.** Um große Ordner mit dem Finder reibungslos zu durchsuchen, insbesondere bei einer schlechten Netzwerkverbindung, sollten Sie sicherstellen, dass sowohl die Symbol- als auch die Symbolvorschau-Ansicht deaktiviert ist. Andernfalls lädt der Finder jedes Asset in einen Ordner herunter, um eine kleine Vorschau zu erzeugen, was die Leistung beeinträchtigen und die Bandbreitenauslastung erhöhen kann (CQ-4219779).

* Navigieren Sie im Finder zum freigegebenen AEM Assets-Netzwerkordner.
* Klicken Sie mit der rechten Maustaste auf den DAM-Bereitstellungspunkt.
* Wählen Sie die Option zum Anzeigen der Ansichtsoptionen aus.
* Deaktivieren Sie das Kontrollkästchen „Symbolvorschau anzeigen“.
* Klicken Sie auf „Als Standard verwenden“.

**Cache beim Verbinden mit einem neuen AEM-Server leeren.** Wenn die Desktop-App eine Verbindung zu einem anderen AEM-Server mit derselben URL herstellt, wird der Cache nicht automatisch geleert. Leeren Sie den Cache manuell, um eine ordnungsgemäße Funktionsweise sicherzustellen. Beachten Sie, dass dies üblicherweise bei Tests auftritt, wenn AEM-Installationen ersetzt werden können, während sie unter derselben URL ausgeführt werden (CQ-4216982).

**CA-signierte SSL-Zertifikate verwenden.** Beachten Sie, dass die AEM-Desktop-App bei der Verbindung mit AEM über eine sichere HTTPS-Verbindung keine selbst signierten SSL-Zertifikate unterstützt. Für derartige Verbindungen ist ein CA-signiertes Zertifikat auf dem Server erforderlich. (CQ-87941)

## Bekannte Probleme {#known-issues}

* Allgemein:
   * Server URLs are required to point to the server without a path (e.g. `http://server`, `https://server`, `http://server:port`, or `https://server:port`). Andere Kontextpfade und Unterordner als /content/dam werden nicht unterstützt (CQ-89343, CQ-87272)
* Dateinamen/Lokalisierung:
   * Datei- und Ordnernamen mit reservierten Zeichen werden nicht ordnungsgemäß verarbeitet. Verwenden Sie unbedingt Datei- und Ordnernamen, die AEM-Anforderungen entsprechen (CQ-93361, CQ-93308, CQ-89276, CQ-4217183)
   * Einige Anwendungen wie Adobe Illustrator erstellen möglicherweise Dateien mit Namen, die in AEM nicht unterstützt werden. Hinzufügen einer Datei `Converted` nach dem Konvertieren, wodurch das Hochladen verhindert wird (CQ-4216985)
   * Assets mit internationalen Namen erscheinen und verschwinden möglicherweise alle paar Sekunden.
* Einchecken/Auschecken:
   * Ein von einem Benutzer ausgechecktes Asset kann nicht für einen anderen Benutzer geöffnet werden, entweder durch Öffnen über die Touch-Benutzeroberfläche oder direkt auf dem Desktop. Einige Applikationen melden möglicherweise, dass das Asset gesperrt oder beschädigt ist bzw. nicht reagiert, wenn versucht wird, das Asset zu öffnen. (CQ-4199234)
   * Das gleichzeitige Ändern von Dateien durch mehrere Benutzer kann dazu führen, dass einige Änderungen verloren gehen. Als Problemumgehung können Sie die Funktion zum  Checkin-/Checkout-Funktion, um zu verhindern, dass mehrere Benutzer dieselbe Datei ändern (CQ-97035)
   * Bestimmte Applikationen unterstützen die Schreibschutzkennzeichnung nicht ordnungsgemäß. Dies ermöglicht es Benutzern, eine Datei zu speichern, die von einem anderen Benutzer ausgecheckt wurde. Die geänderte Datei wird erst dann übertragen, wenn der andere Benutzer die Datei wieder eincheckt. Beide Änderungen sind in AEM als verschiedene Versionen des Assets verfügbar (CQ-89551, CQ-87572, CQ-89615)
   * Der Ausgecheckt- und der Schreibschutzstatus werden unabhängig voneinander im Finder gemeldet. Dies führt zur Anzeige von zwei Schlosssymbolen, wenn ein Benutzer ein Asset auscheckt (CQ-89507).
* Finder-Integration:
   * Beim Ziehen/Ablegen großer Dateien kann es vorkommen, dass der Finder eine Zeitüberschreitung durchläuft, während Dateien im Hintergrund übertragen werden. This results in an `Error - 36`. Als Problemumgehung können Sie das Asset erneut per Drag-and-Drop ziehen oder öffnen (CQ-4219628).
   * Das manuelle erneute Laden von Ordnern funktioniert nicht immer. Problemumgehung:  30 s warten, bis der Ordner automatisch aktualisiert wird. (CQ-97389)
   * Weitere Asset-Informationen... ist auf Auswahl einzelner Dateien beschränkt (CQ-89542, CQ-87656)
   * Die Option „In AEM Assets öffnen“ ist auf die Auswahl einzelner Dateien und Ordner begrenzt (CQ-83382).
   * Fehler beim Umbenennen von Assets, die keine Erweiterung aufweisen (CQ-4218971).
* Funktion zum Kopieren/Einfügen: Einfügen ist verfügbar, wenn kein Asset in die Zwischenablage kopiert wurde
* Windows:
   * Dateien mit alternativen Datenströmen (ADS) werden nur in NTFS-Dateisystemen vollständig unterstützt. Das Kopieren solcher Dateien in die von der Desktop-App bereitgestellte WebDAV-Freigabe führt zu einem Warndialogfeld, das den Benutzer warnt, dass die Datei Eigenschaften aufweist, die nicht in den neuen Speicherort kopiert werden können. Dies ist normalerweise korrekt, da die Eigenschaften nur für eine bestimmte Anwendung auf dem Desktop des Benutzers relevant sind und nichts mit dem tatsächlichen Dateiinhalt zu tun haben (CQ-103770) (Win)
   * Die Desktop-App unter Windows muss von dem Benutzer installiert werden, der sie verwenden wird (CQ-4216389) (win)
   * Die App kann abstürzen, wenn Sie bei einem fehlgeschlagenen Upload auf die Schaltfläche "Wiederholen"klicken, nachdem der Batch-Upload nach der Trennung der Verbindung fortgesetzt wurde (CQ-4251884) (Win)

## Hilfreiche Ressourcen {#helpful-resources}

* [Dokumentation zu AEM](https://helpx.adobe.com/support/experience-manager/6-4.html)
* [Verwenden der AEM Desktop-App Version 1.x](use-app-v1.md)
* [Best Practices für AEM Desktop-Apps Version 1.x](best-practices-for-v1.md)

## Kompatibilitätsmatrix und Voraussetzungen {#compatibilitymatrix}

Die AEM-Desktop-App funktioniert mit verschiedenen Versionen von AEM. Informationen zu den unterstützten Versionen finden Sie in der Kompatibilitätsmatrix.

| Version | Revision | Veröffentlichungsdatum | Kompatibilität |
|---------|------------------------|--------------|-------------------------------------------------------------|
| 1.10 | 1.10.0.3 (Mac und Win) | 31.08.2018 | AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.9 | 1.9.1.1 (Mac und Win) | 21.06.2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.8 | 1.8.1.0 (Mac und Win) | 28.03.2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.7 | 1.7.0.3 (Mac und Win) | 10. Januar 2018 |  AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
