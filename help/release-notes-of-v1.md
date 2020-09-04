---
title: Versionshinweise für das AEM-Desktop-Programm, Version 1.x
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für das AEM-Desktop-Programm, Version 1.x.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: 9de9d086be4c0eccda7a60bd3dcbe68735394fad
workflow-type: ht
source-wordcount: '3869'
ht-degree: 100%

---


# Versionshinweise für das AEM-Desktop-Programm, Version 1.x {#aem-desktop-app-release-notes}

Für das AEM-Desktop-Programm v1.x sind die folgenden Download-Links und AEM-Kompatibilitätsinformationen verfügbar:

| Produkte | Adobe Experience Manager (AEM)-Desktop-Programm |
|--- |--- |
| Version | 1.10 (1.10.0.6 unter Mac und 1.10.0.3 unter Windows) |
| Typ | Nebenversion |
| Datum | 1.10.0.6 (Mac): 15. April 2020; 1.10.0.3 (Win): 31. August 2018 |
| Download-URLs | [Mac OS X (64 Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-1.10.0.6.dmg); [Windows (32 Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-1.10.0.3.exe); [Windows (64 Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-1.10.0.3.exe) |
| Kompatibilität | AEM 6.5.x; AEM 6.4.x; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |

>[!NOTE]
>
>Die Cachegrößenbeschränkung wird nicht erzwungen. Beim Starten des Desktop-Programms wird die Cachegröße einmal berechnet und es wird eine Benachrichtigung angezeigt, wenn sich die Größe der vordefinierten Beschränkung nähert.

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites}

Das [!DNL Adobe Experience Manager]-Desktop-Programm ist mit den folgenden Betriebssystemen kompatibel:

* Mac OS X 10.10 oder höher mit aktuellen Fehlerbehebungen.

* Windows 10 mit den aktuellsten Service Packs und Fehlerbehebungen.

>[!NOTE]
>
>Windows 7 wird vom Anbieter nicht mehr unterstützt (https://support.microsoft.com/de-de/help/4057281/windows-7-support-ended-on-january-14-2020).

Adobe empfiehlt dringend, die neueste Version des AEM-Desktop-Programms zu verwenden, um die neuesten Funktionen mit den neuesten Fehlerkorrekturen und der bestmöglichen Leistung zu nutzen.

Für die Version des AEM-Desktop-Programms, die Sie auf Ihrem lokalen Computer installieren möchten, sind eine bestimmte Version von AEM-Server oder zusätzliche serverseitige Komponenten (Service Packs, Hotfixes oder Feature Packs) erforderlich. Stellen Sie sicher, dass der AEM-Server ordnungsgemäß konfiguriert ist, bevor Sie zum ersten Mal eine Verbindung herstellen. Wenn Sie Hilfe benötigen, wenden Sie sich an Ihren AEM-Administrator.

Lesen Sie die Informationen in der [detaillierten Kompatibilitätsmatrix](#compatibilitymatrix) am Ende dieses Dokuments, um die Voraussetzungen für Ihr Setup zu prüfen.

## Neue Funktionen im AEM-Desktop-Programm 1.10 {#what-s-new-in-aem-desktop-app}

Das AEM-Desktop-Programm 1.10 konzentriert sich auf die Verbesserung des Benutzererlebnisses rund um den Upload großer Dateien, Informationen über Hintergrundvorgänge sowie ein optimiertes Erlebnis beim Öffnen von Assets mit verlinkten Dateien (wie InDesign).

>[!NOTE]
>
>Wenn Sie macOS 10.15.4 oder höher verwenden, verwenden Sie mindestens Version 1.10.0.6 des Programms. Diese Patch-Version erfüllt die [Apple-Benachrichtigungsanforderungen](https://developer.apple.com/news/?id=04102019a).

**Lokales Bearbeiten/Auschecken**: Automatische Uploads gespeicherter Asset-Änderungen, die im Statusfenster deaktiviert werden können. So können Benutzer an Dateien arbeiten, die hierbei vorgenommenen Änderungen speichern und, wenn sie bereit sind, alle Änderungen hochladen.

**Vereinfachtes Asset-Statusfenster**. Das Statusfenster wurde vereinfacht. Auf der Registerkarte [!UICONTROL Uploads] werden jetzt sowohl einzelne Assets als auch Ordner- oder Massen-Uploads angezeigt. Die zuvor vorhandene Registerkarte „Massen-Uploads“ wurde entfernt.

**Programmsymbol zur Anzeige von Massen-Uploads**. Das Programmsymbol zeigt anhand der Überlagerung „Transfer“ (Übertragung) an, dass ein Massen-Upload durchgeführt wird, indem die Überlagerung angezeigt wird.

**Benachrichtigungen bezüglich Aktualisierungskonflikten**. Wenn das Programm beim Aktualisieren eines Assets einen Konflikt feststellt, wird eine Benachrichtigung angezeigt, damit der Benutzer den Fall untersuchen kann, ohne das Statusfenster im Blick behalten zu müssen. Wenn die Anwendung startet, sucht sie nach potenziellen Konflikten, damit der Benutzer sie beheben kann.

**Besserer Umgang mit Verbindungsabbrüchen**. Massen-Uploads werden angehalten, wenn die Verbindung unterbrochen wird. Benutzer können sie zu einem späteren Zeitpunkt fortsetzen. Für fehlgeschlagene Uploads einzelner Dateien steht Benutzern die Schaltfläche „Retry“ (Wiederholen) zur Verfügung.

## Installationsanweisungen {#installation-instructions}

Detaillierte Anweisungen finden Sie unter [Installieren und Konfigurieren des AEM-Desktop-Programms](install-configure-app-v1.md).

## Verbesserungen in den vorherigen Versionen {#enhancements-in-the-previous-versions}

Diese Version erweitert und ersetzt die Vorgängerversionen des Experience Manager-Desktop-Programms, die die folgenden wesentlichen Verbesserungen boten:

* **Version 1.9/1.9.1**: fortsetzbare Uploads, verbessertes Statusfenster, Programmsymbole, die den Status des Programms/der Verbindung angeben, Vorab-Abruf verknüpfter Assets für InDesign-Dateien.

* **Version 1.8**: bessere Steuerung der Cache-Größe für den Benutzer, verbesserte Anmeldung für SAML/SSO unter Windows, Unterstützung des .pac-Netzwerk-Proxys auf Mac-Computern und Behebung der von Kunden gemeldeten Probleme.

* **Version 1.7.**: Verbesserungen der Stabilität und Caching-Logik, bessere Unterstützung für Netzwerk-Proxys und Möglichkeit, interne Dateien nach der Deinstallation zu bereinigen

* **Version 1.6**: Verbesserungen am Anmeldeprozess für verschiedene AEM-Sicherheitskonfigurationen sowie an der Stabilität und Leistung des Programms.

* **Version 1.5**: Programm-Stabilität und Ausfallsicherheit bei verschiedenen Netzwerkproblemen, bessere Unterstützungsmöglichkeiten.

* **Version 1.4**: Möglichkeit, hierarchische Ordner im Hintergrund mit der Fortschrittsüberwachung hochzuladen.

* **Version 1.3**: verbesserte Leistung und Stabilität beim Zugriff auf Dateien und Speichern von Änderungen in AEM, insbesondere aus Creative Cloud-Desktop-Applikationen wie InDesign, Illustrator oder Photoshop. Diese Version sollte Benutzern ein Desktop-artiges Erlebnis bei der Arbeit mit Dateien bieten und gleichzeitig Übertragungsvorgänge für Netzwerkdaten im Hintergrund durchführen.

### Seit Einführung des AEM-Desktop-Programms 1.9 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-19x}

Beim Adobe Experience Manager (AEM)-Desktop-Programm 1.9.1 handelte es sich um eine Patch-Version, mit der einige wichtige Kundenprobleme im Hinblick auf das Auschecken von Assets und Kopieren von Dateien aus einer Netzwerkfreigabe in ein lokales Verzeichnis behoben wurden.

* Assets, die von einem Benutzer ausgecheckt werden, sollten nicht für Bearbeitungen durch andere Benutzer verfügbar sein (CQ-4246009)

* Unterstützung des Kopierens von einem zugeordneten Ordner in einen lokalen Ordner, wenn sich der Benutzerordner auf einer separaten Laufwerkpartition befindet (CQ-4243978)

Das AEM-Desktop-Programm 1.9 konzentrierte sich auf die Verbesserung des Benutzererlebnisses rund um den Upload großer Dateien, Informationen über Hintergrundvorgänge sowie ein optimiertes Erlebnis beim Öffnen von Assets mit verlinkten Dateien (wie InDesign).

**Fortsetzbare Uploads**
Für Upload-Vorgänge – insbesondere für große Dateien – ist im neuen Fenster „Asset-Status“ eine Option zum Anhalten/Fortsetzen verfügbar.

**Fenster mit verbesserter Einsicht in Asset-Status**
Das Fenster zum Asset-Status bietet folgende Informationen zu Assets.

[!UICONTROL Changes]

* Zeigt Änderungen an, die sich momentan in der Warteschlange befinden.

* Zeigt laufende Upload-Vorgänge an, einschließlich eines Fortschrittsbalkens, der Übertragungsrate, der Dateigesamtgröße und der bislang übertragenen Größe.

* Abgeschlossene Uploads werden mit der übertragenen Datenmenge und der Übertragungsrate angezeigt.

* Fehlgeschlagene Uploads werden zusammen mit einer Fehlermeldung und Übertragungsinformationen angezeigt, sofern verfügbar.

* Für 3-mal fehlgeschlagene Uploads wird eine Fehlermeldung angezeigt.

* Für in Konflikt stehende Dateien wird ein Symbol angezeigt, auf das der Benutzer klicken kann. Durch das Klicken auf das Symbol wird ein Dialogfeld mit einer Erklärung und zwei Optionen angezeigt:

   * [!UICONTROL Keep Mine] lädt die Datei sofort auf den Server hoch

   * [!UICONTROL Overwrite Mine] löscht die lokale Datei sofort und lädt eine neue Kopie vom Server herunter

[!UICONTROL Downloads]

* Zeigt aktive Downloads an, einschließlich einer Übertragungsrate und der bislang übertragenen Größe.

* Abgeschlossene Downloads werden mit der übertragenen Datenmenge, der Übertragungsrate und einem Symbol angezeigt, über das die Datei per Klick geöffnet wird (nur für einzelne Dateien verfügbar).

* Fehlgeschlagene Downloads werden mit einer Fehlermeldung und Übertragungsinformationen angezeigt, sofern verfügbar.

* In der Fußzeile werden die Gesamtzahl der heruntergeladenen Dateien und die durchschnittliche Übertragungsrate angezeigt.

* Bei Verwendung der Web-Benutzeroberfläche von Experience Manager Assets, um mehrere Dateien zu öffnen, werden diese gruppiert. Beispiel: meinasset.jpeg und 4 weitere Dateien.

* Beim Herunterladen von InDesign-Dokumenten mit verknüpften Assets, die in AEM Assets gespeichert sind, lädt das Desktop-Programm zunächst alle verknüpften Assets herunter, bevor das [!UICONTROL Adobe InDesign]-Dokument geöffnet und der Download verknüpfter Assets angezeigt wird. Beispiel: 5 von 24.

[!UICONTROL Bulk Uploads]

Durch das Hochladen von umfangreichen Ordnerhierarchien über [!UICONTROL Create] > [!UICONTROL Upload Folder] in der AEM-Web-Benutzeroberfläche oder durch das Kopieren und Auswählen von „Paste Assets“ (Assets einfügen) in Finder/Explorer wird im Kontextmenü des Desktop-Programms die Verwendung dieses Dialogfelds ausgelöst.

* Zeigt aktive Uploads an, einschließlich eines Fortschrittsbalkens und des Namens der momentan übertragenen Datei.

* Aktive Uploads beinhalten ein Symbol, über das der Upload per Klick abgebrochen wird. Die Übertragung endet, nachdem die aktuelle Dateiübertragung abgeschlossen ist.

* Fehlgeschlagene Übertragungsprozesse werden mit einer Fehlermeldung angezeigt (nur, wenn die gesamte Übertragung fehlschlägt).

* Wenn die Übertragung einer einzelnen Datei fehlschlägt, wird sie auf der Registerkarte als Fehler angezeigt. Andernfalls werden einzelne Dateien nicht auf der Registerkarte angezeigt, sondern lediglich ein einzelner Eintrag für den gesamten Upload.

**Symbole für den Status von Hintergrundvorgängen**

Das Programmsymbol gibt den Status von Hintergrundvorgängen an, um bessere visuelle Hinweise für die Benutzer bereitzustellen. Wenn das Programm beispielsweise nicht mit AEM verbunden ist, ist das Symbol ausgegraut. Im Falle eines aktiven Uploads wird eine Synchronisierungsüberlagerung angezeigt usw.

**Vorab-Abruf verknüpfter Assets**

Zur Verbesserung des Benutzererlebnisses beim Arbeiten mit InDesign-Dokumenten, die in AEM gespeicherte verknüpfte Assets beinhalten, versucht das Desktop-Programm, diese verknüpften Dateien vorab in den lokalen Cache zu verschieben, bevor das InDesign-Dokument heruntergeladen und geöffnet wird. Somit stehen dem Benutzer die verknüpften Dateien lokal zur Verfügung und er muss beim Zugriff auf diese Dateien in InDesign (im Bereich „Verknüpfungen“) nicht länger warten.
Beachten Sie, dass der Vorab-Abruf nur funktioniert, wenn AEM die Verknüpfungen auf der Server-Seite erkennt. Für ein Asset mit erkannten Verknüpfungen wird in der Ansicht „Eigenschaften“ des InDesign-Assets die Liste „Verweise“ aufgeführt.

### Seit Einführung von AEM-Desktop-Programm 1.8 verfügbare Verbesserungen {#enhancements-available-since-aem-desktop-app-18x}

In der Folgeversion 1.8.1 des AEM-Desktop-Programms wurden Verbesserungen hinsichtlich des gleichzeitigen Öffnens mehrerer Dateien über die AEM-Benutzeroberfläche gegenüber der Version 1.8 hinzugefügt (CQ-4237747, CQ-4238780). Verbesserungen im AEM-Desktop-Programm 1.8:

* Caching: Neue Benutzeroberfläche zum Verwalten des Caches des AEM-Desktop-Programms (CQ-4208690), einschließlich folgender Funktionen:

   * Aktuelle Cachegröße anzeigen

   * Maximale Cache-Größe definieren, bevor eine Benachrichtigung gesendet wird

   * Die Cache-Größe wird nur beim Start des Desktop-Programms überprüft. Beim Erreichen der konfigurierten Beschränkung wird eine Meldung angezeigt.

   * Die neue Benutzeroberfläche bietet eine Schaltfläche zum Löschen des Caches.

* Anmelden: (Win) Anmeldung bei der AEM-Instanz so korrigiert, dass SAML und SSL verwendet werden (CQ-4216353)

* Netzwerk:

   * Beim Ablauf einer AEM-Sitzung wird der Benutzer entsprechend benachrichtigt und er kann auf die Benachrichtigung klicken, um sich erneut anzumelden (CQ-4202028).

   * (Mac) Neue Unterstützung zum Verbinden mit AEM über eine .pac-Proxy-Konfiguration (CQ-4233430).

   * (Windows) Behebung von Problemen mit dem Dialogfeld „Advanced“ > „Login URL“ (Erweitert > Anmelde-URL) (CQ-4236061).

* Fehlerbehebungen:

   * Dialogfeld „More Assets Info“ (Weitere Asset-Informationen): mitunter war die Aktionsleiste nicht sichtbar (CQ-4208540).

   * (Windows) Dateien können nun synchronisiert werden, nachdem sie in der AEM Assets-Benutzeroberfläche auf eine ältere Version zurückgesetzt wurden (CQ-4216411).

### Seit Einführung von AEM-Desktop-Programm 1.7 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabilität:

   * Verbesserte Stabilität, wenn das AEM-Desktop-Programm eine Verbindung zu einem überlasteten AEM-Server herstellt (CQ-4224803).

   * Verbesserte Stabilität, wenn viele Dateien angefordert werden (CQ-4224212).

   * Verbesserte Asset-Aktualisierung mit zusätzlicher Prüfung (CQ-4228291).

* Caching:

   * Behobene Festplattenfehler und Probleme beim Öffnen von Dateien in Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717).

   * Verbesserte Zwischenspeicherung zur Vermeidung von Binärdateien mit Größe null (CQ-4216599).

* Anmeldung: Ermöglichung der Verbindungsherstellung mit deaktiviertem strictSSL für spezielle Konfigurationen (z. B. lokal ausgestellte Zertifikate) (CQ-4223949).

* Netzwerke: Verbesserte Unterstützung für die Verbindung über Netzwerk-Proxy (CQ-4223477, CQ-4221280, CQ-4206854).

* Installation und Deinstallation:

   * (Win) Gründlichere Deinstallation (CQ-4220906).

   * [Windows (32 Bit)] Installationsprogramm schlägt beim Versuch zur Installation von Microsoft.NET Framework Version 4.5 zu fehl  (CQ-4218084).

   * (Mac) Skript zur manuellen Ausführung für das vollständige Entfernen von Desktop-Programm-Dateien (CQ-4216489).

>[!NOTE]
>
>In der Beta-Version des AEM-Desktop-Programms 1.7 festgestellte Probleme (die in Version 1.6 nicht vorhanden waren) werden in den Versionshinweisen nicht aufgeführt.

### Seit Einführung von AEM-Desktop-Programm 1.6 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-16}

* Dokumentation: Neue Dokumentation [Best Practices für das Programm, v1.x](https://helpx.adobe.com/de/experience-manager/6-3/assets/using/aem-desktop-app-best-practices.html).

* Verbesserter Anmeldeprozess für AEM:

   * Verbessertes SAML-Handling – Relax-Regeln (CQ-4202781).

   * Zusätzliche Funktion zum Konfigurieren einer separaten Anmelde-URL in den Einstellungen (CQ-4214052, CQ-4214051).

* Benachrichtigung für Benutzer beim Herunterladen größerer Assets über nicht abgeschlossenen Asset-Download (CQ-4216284).

* Netzwerke:

   * DNS-Caching (CQ-4210176).

   * Unterstützung für Verbindung über Proxy unter Windows (CQ-4206854).

* Zwischenspeicherung und Zugriff auf Netzwerkfreigabe in Finder/Explorer:

   * Schlosssymbol wird nun für ausgecheckte Assets unter Windows 10 angezeigt (CQ-90957).

   * Ordnerinhalte in Netzwerkfreigaben verschwinden oder erscheinen möglicherweise wieder (CQ-4209160, CQ-4210180).

   * Fehler beim Datei-Upload aufgrund eines Konflikts, der im Bericht zum Upload-Warteschlangen-Status gemeldet ist (CQ-4215727).

   * Beim Öffnen mehrerer Dateien über den Ordner für das Desktop-Programm in PS werden möglicherweise Fehlermeldungen zu abgeschnittenen oder unvollständigen Dateien angezeigt (CQ-4216276).

* Verbesserungen an Stabilität und Performance:

   * Verbesserte Leistung beim Durchsuchen von Ordnern mit vielen Assets (CQ-4214933).

   * Das Desktop-Programm 1.5 kann Desktop-Computer mit der Zeit verlangsamen (CQ-4209159).

   * Die Funktion zum Anzeigen des Warteschlangenstatus funktioniert nur für den Benutzer, der das Programm installiert hat (CQ-4212199).

   * (Windows) Vergewissern Sie sich, dass das 32-Bit-Installationsprogramm keinen 64-Bit-Code enthält (CQ-4217406).

* Ausgewählte Probleme, die in Beta 1.6 gefunden und behoben wurden:

   * Hohe CPU-Auslastung (CQ-4218070).

   * Ziehen von Dateien per Drag-and-Drop führt zu Fehler beim Hochladen in AEM (CQ-4217006).

### Seit Einführung von AEM-Desktop-Programm 1.5 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-15}

**Version 1.5.1.5 für Mac OS X:** Die Version 1.5.1.5 bietet folgende Vorteile:

* Neue Funktionen und Erweiterungen: Zusätzliche Funktionen zum Kopieren/Einfügen für die Finder-Integration, um die direkte Übertragung vom Desktop zu AEM zu ermöglichen (CQ-4208158)..

* Fehlerbehebungen:

   * Problem aufgrund von Fehler 43 behoben, das in einigen Fällen beim Umbenennen von Assets aufgetreten ist (CQ-4207900)..

   * Beim Zurücksetzen auf eine ältere Version aus der Timeline aktualisiert AEM das Asset nicht in Finder (CQ-4205194).

   * Das Desktop-Programm stürzt beim Durchsuchen großer verschachtelter Verzeichnisse ab (CQ-4208539).

   * Der Desktop-Programm-Bereitstellungspunkt ist nun „/Volumes/DAM“ und damit für alle Benutzer einheitlich (CQ-4208159).

   * Beim erstmaligen Platzieren einer Datei in InDesign wird eine Warnung bezüglich der Aktualisierung angezeigt (CQ-4207454).

Hinweis zu Link-Warnungen: Creative Cloud-Applikationen (z. B. InDesign) erstellen einen „Schnappschuss“ der letzten Änderung des Elements zum Zeitpunkt seiner Platzierung. Ändert sich dieses Datum zu einem späteren Zeitpunkt, meldet die Adobe Creative Cloud-Applikation, dass die Links veraltet sind. Dies wird auf unterschiedliche Weise gemeldet:

* Wenn die Adobe Creative Cloud-Applikation gestartet wird, erscheint ein Dialogfeld, um den Benutzer darüber zu informieren, dass die verknüpften Assets veraltet sind, und den Benutzer aufzufordern, Maßnahmen zu ergreifen.

* Wenn die Adobe Creative Cloud-Applikation bereits ausgeführt wird, erscheint ein gelbes Warnsymbol am verknüpften Asset.

Dies gilt gleichermaßen für Assets auf lokalen Festplatten und Assets in einem von AEM Desktop bereitgestellten Verzeichnis, mit folgenden Ausnahmen:

* Wenn ein platziertes Asset von einem anderen Benutzer geändert wird, erscheint das Warnsymbol beim ersten Mal, wenn andere Benutzer ein Dokument mit dem platzierten Asset öffnen. Dies geschieht nur, wenn das platzierte Asset bereits lokal zwischengespeichert wurde..

* Wenn Benutzer ein platziertes Asset über das von AEM Desktop bereitgestellte Verzeichnis ändern und dann ihren lokalen Cache löschen, wird das platzierte Asset als veraltet gemeldet.

Diese beiden Fälle treten erwartungsgemäß ein. Sie sind auf die „Delayed Sync“-Architektur von AEM Desktop zurückzuführen.

**Version 1.5.0.x für Mac OS X und Windows:** Diese Version des AEM-Desktop-Programms bietet die folgenden Vorteile:

* Bessere Stabilität und Ausfallsicherheit bei verschiedenen Netzwerkproblemen.

   * Zuverlässigere Zuordnung von AEM Assets-Ordnern (CQ-103276, CQ-4204669, CQ-4203957).

   * Verbesserte Handhabung zwischengespeicherter Dateien (CQ-4204336, CQ-4206263).

   * Verbesserte Handhabung von Downloads/Uploads von Dateien mit einer Größe von mehr als 2 GB (CQ-4206438).

   * Behebung von Fehler 36 beim Verschieben oder Umbenennen einer großen Anzahl von Dateien in Finder (CQ-4204640).

* Optimierung der Netzwerkkommunikation mit dem AEM-Server (CQ-4204974, CQ-100903).

* Verbesserte Zuverlässigkeit beim Öffnen, Platzieren und Speichern von AEM-Assets in Creative Cloud-Programmen (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980).

* Verbesserte Unterstützungsmöglichkeit: Option zum Leeren des Cache (CQ-4202541), einfacher Zugriff auf Protokolle (CQ-4202340, CQ-4204673).

* Weitere Fehlerbehebungen:
   * Verbesserte Unterstützung für Assets und Ordner, die japanische Zeichen im Namen enthalten oder nicht-englische Spracheinstellungen aufweisen (CQ-4195433, CQ-4205793, CQ-4199446).

   * Verbesserte Handhabung der Anmeldung mit SSL (CQ-4200217).

   * Zuverlässigere Freigabebereitstellung (CQ-4200793).

   * Diverse Verbesserungen hinsichtlich der Stabilität (CQ-4207539, CQ-4200378).

   * Verbesserte Handhabung der AEM Assets-URL in den Voreinstellungen (CQ-97388).

### Seit Einführung von AEM-Desktop-Programm 1.4 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-14}

* Vereinfachter Upload hierarchischer Ordner über die neue Aktion „Erstellen“ > „Ordner hochladen“ in der Touch-optimierten Benutzeroberfläche.
   * Die Aktion löst einen Ordner-Upload-Vorgang aus, der vom Desktop-Programm ausgeführt wird.
   * Das Desktop-Programm durchläuft die jeweilige Ordnerhierarchie auf dem Desktop im Hintergrund und lädt die Dateien in AEM Assets hoch.
   * Der Benutzer kann den Fortschritt im neuen Fenster für den Upload-Warteschlangen-Status mithilfe des Fortschrittsbalkens für nicht abgeschlossene Vorgänge überwachen.
   * Der Upload-Warteschlangen-Status bietet außerdem bessere Informationen zur Fehlerbehebung (z. B. dass keine Verbindung zum Server besteht).
* Neue Aktion „Bearbeiten“ in der Touch-optimierten Benutzeroberfläche, die Vorgänge zum Auschecken und Öffnen kombiniert
* Optimierte Gruppierung von Desktop-bezogenen Aktionen in der Touch-optimierten Benutzeroberfläche (AEM 6.3)
* Verbesserte Kompatibilität mit den neuesten Betriebssystemversionen
* Fehlerbehebungen für von Kunden gemeldete Probleme

### Seit Einführung des AEM-Desktop-Programms 1.3 verfügbare Verbesserungen {#Enhancements-Available-Since-AEM-Desktop-App-13}

* Höhere Effizienz. Netzwerkvorgänge werden schneller abgeschlossen und die Wartezeiten für Benutzer werden verkürzt.
* Verbesserte Finder-Integration, die für mehr Stabilität sorgt und den Zugriff auf Funktionen wie Miniaturansichten ermöglicht.
* Verbesserungen hinsichtlich der Zwischenspeicherung und Leistung.
* Bessere Unterstützung für das direkte Speichern aus Desktop-Applikationen (PS, ID, AI usw.).
* Verbesserte Integration mit Mac OS (Protokoll für lokale Netzwerklaufwerke geändert, statt WebDAV zuverlässigeres SMB1)..
* Das Desktop-Programm stellt eine Verbindung zum AEM-Server mithilfe des AEM-nativen HTTP RESTful-Protokolls her.
* Die Dateien werden zunächst lokal gespeichert und nach einer festgelegten Zeit (30 Sek.) im Hintergrund wieder in AEM hochgeladen. Dadurch wird das Speichern von Dateien beschleunigt.
* Besseres Handling von Desktop-Applikationen, die Zwischenvorgänge zum Speichern von Dateien verwenden (partielles Speichern und temporäre Dateien). Dadurch können in der AEM Assets-Timeline korrekte Versions- und Asset-Upload-Informationen angezeigt werden.
* Dialogfeld zur Nachverfolgung des Status von im Hintergrund ausgeführten Upload-Aufgaben.

## Liste der Änderungen   {#list-of-changes}

### Bereitstellungspunkt für Mac {#mount-point-on-mac}

Mit Einführung von MacOS 10.12 (Sierra) hat Apple die Berechtigungen für den Ordner „/Volumes“ stärker eingeschränkt, der für die Bereitstellung von Netzwerklaufwerken und Geräten verwendet wird. Für das Erstellen eines neuen Bereitstellungspunkts waren Administratorrechte erforderlich. Dieses Problem wurde mit Einführung von MacOS 10.12.5 behoben.

Da das AEM-Desktop-Programm für Benutzer ohne Administratorrechte auf lokalen Computern ausgeführt werden sollte, wurde der Bereitstellungspunkt für AEM Assets-Repositorys in Version 1.4 und 1.5 in einen DAM-Unterordner im lokalen Ordner des Benutzers unter macOS geändert (CQ-104183).

Da für den Ordner „/Volumes“ keine Administratorrechte mehr erforderlich sind, wurde diese Änderung mit Version 1.5.1 rückgängig gemacht. Dies ermöglicht es zudem, InDesign-Dokumente mit platzierten AEM-Assets zwischen macOS-Benutzern freizugeben.

### Protokolländerung (seit Version 1.3) {#protocol-change-since}

* Mac OS X:
   * Das Protokoll für lokale Netzwerklaufwerke für die OS X-Desktop-Integration wurde von WebDAV in SMB1 geändert.
   * Das mit dem Desktop-Programm bereitgestellte AEM-Repository wird in Finder als „smb“-Netzwerklaufwerk anstatt als WebDAV-Laufwerk angezeigt.
* Windows:
   * Das Protokoll für lokale Netzwerklaufwerke für die Windows-Desktop-Integration wird beibehalten; AEM wird als WebDAV-Freigabe bereitgestellt.
* Für beide Plattformen (Windows und Mac):
   * Das Protokoll zum Zugriff auf/Download von Assets und zum Hochladen von Änderungen in AEM wurde in das AEM-native Protokoll geändert, bei dem es sich um ein HTTP-basiertes RESTful-Protokoll handelt. Es bietet eine bessere Kontrolle über Netzwerkvorgänge und eine bessere Kompatibilität mit der Netzwerkinfrastruktur.

>[!NOTE]
>
>Unter Mac OS X: Die Änderung des Protokolls für lokale Netzwerklaufwerke von WebDAV in SMB1 führt zu einem anderen lokalen Pfad für dasselbe Asset im Repository. Dies kann sich auf Verknüpfungen zu Dateien auswirken, die in Adobe Creative Cloud-Applikationen über den Befehl „Platzieren“ platziert werden. Weitere Informationen finden Sie unter [Verwenden des AEM-Desktop-Programms](use-app-v1.md).

### Dateiverarbeitung (seit 1.3) {#file-handling-since}

* Ordner werden nach einer festgelegten Verzögerung (derzeit 30 Sek.) automatisch aktualisiert.
* Dateien, die von anderen Benutzern ausgecheckt wurden, sind als schreibgeschützt markiert.
* Die Dateien werden in zwei Phasen auf einem Netzwerklaufwerk gespeichert, das über das Desktop-Programm bereitgestellt wird.
* In der ersten Phase wird eine Datei lokal gespeichert. Auf diese Weise muss der Benutzer, der die Datei speichert, nicht warten, bis die Datei vollständig in AEM übertragen wurde, und kann seine Arbeit fortsetzen, sobald die Datei gespeichert wurde.
* In der zweiten Phase lädt das Desktop-Programm die aktualisierte Datei nach einer festgelegten Verzögerung auf den AEM-Server hoch (z. B. 30 Sek.). Dieser Vorgang erfolgt im Hintergrund. Verwenden Sie die Option **Status der Dateisynchronisierung im Hintergrund anzeigen**, um den Status des Upload-Vorgangs anzuzeigen.

## Wichtige Hinweise {#important-notices}

**Ordner-Upload.** Es empfiehlt sich, die neue Funktion zum Hochladen von Ordnern zu verwenden, um größere hierarchisch strukturierte Ordner in AEM hochzuladen, anstatt eine Kopie zu verwenden/sie per Drag-and-Drop in ein bereitgestelltes AEM-Repository von der Finder-/Explorer-Ebene zu ziehen. Bei Verwendung der Funktion für den Ordner-Upload kommuniziert das Desktop-Programm direkt mit AEM und bietet so eine sehr viel bessere Kontrolle über den Gesamtprozess.

**AEM-Sitzung aktivieren.** Das AEM-Desktop-Programm erfordert für ordnungsgemäße Funktion eine aktive Sitzung auf dem AEM Assets-Server. Für Benutzer, die täglich mit dem Desktop-Programm arbeiten, empfiehlt es sich, die Bereitstellung von AEM Assets abends aufzuheben, um das Abmelden zu erzwingen, und AEM Assets dann morgens wieder bereitzustellen, um sicherzugehen, dass sie angemeldet sind und die Netzwerkfreigabe betriebsbereit ist.

**Symbolvorschau im Finder deaktivieren.** Um große Ordner mit dem Finder reibungslos zu durchsuchen, insbesondere bei einer schlechten Netzwerkverbindung, sollten Sie sicherstellen, dass sowohl die Symbol- als auch die Symbolvorschau-Ansicht deaktiviert ist. Andernfalls lädt Finder jedes Asset in einen Ordner herunter, um eine kleine Vorschau zu erzeugen, was die Leistung beeinträchtigen und die Bandbreitenauslastung erhöhen kann (CQ-4219779).

* Navigieren Sie im Finder zum freigegebenen AEM Assets-Netzwerkordner.
* Klicken Sie mit der rechten Maustaste auf den DAM-Bereitstellungspunkt.
* Wählen Sie die Option zum Anzeigen der Ansichtsoptionen aus.
* Deaktivieren Sie das Kontrollkästchen „Symbolvorschau anzeigen“.
* Klicken Sie auf „Als Standard verwenden“.

**Cache beim Verbinden mit einem neuen AEM-Server leeren.** Wenn das Desktop-Programm eine Verbindung zu einem anderen AEM-Server mit derselben URL herstellt, wird der Cache nicht automatisch gelöscht. Leeren Sie den Cache manuell, um eine ordnungsgemäße Funktionsweise sicherzustellen. Beachten Sie, dass dies üblicherweise bei Tests auftritt, wenn AEM-Installationen ersetzt werden können, während sie unter derselben URL ausgeführt werden (CQ-4216982).

**CA-signierte SSL-Zertifikate verwenden.** Beachten Sie, dass das AEM-Desktop-Programm beim Herstellen einer sicheren HTTPS-Verbindung zu AEM keine selbstsignierten SSL-Zertifikate unterstützt. Für derartige Verbindungen ist ein CA-signiertes Zertifikat auf dem Server erforderlich. (CQ-87941)

## Bekannte Probleme   {#known-issues}

* Allgemein:
   * Es werden Server-URLs benötigt, um ohne Pfad auf den Server zu verweisen (z. B. `http://server`, `https://server`, `http://server:port` oder `https://server:port`). Außer „/content/dam“ werden keine anderen Kontextpfade und Unterordner unterstützt (CQ-89343, CQ-87272).
* Dateinamen/Lokalisierung:
   * Datei- und Ordnernamen mit reservierten Zeichen werden nicht ordnungsgemäß verarbeitet. Stellen Sie sicher, dass Sie Datei- und Ordnernamen verwenden, die den Anforderungen entsprechen (CQ-93361, CQ-93308, CQ-89276, CQ-4217183).
   * Einige Applikationen wie Adobe Illustrator erstellen möglicherweise Dateien mit Namen, die in AEM nicht unterstützt werden. Ein Beispiel ist das Hinzufügen von `Converted` nach dem Konvertieren, wodurch das Hochladen verhindert wird (CQ-4216985)
   * Assets mit internationalen Namen erscheinen und verschwinden möglicherweise alle paar Sekunden.
* Funktionen für das Ein- und Auschecken:
   * Ein von einem Benutzer ausgechecktes Asset kann nicht von einem anderen Benutzer geöffnet werden, weder über die Aktion „Öffnen“ in der Touch-optimierten Benutzeroberfläche noch direkt auf dem Desktop. Einige Applikationen melden möglicherweise, dass das Asset gesperrt oder beschädigt ist bzw. nicht reagiert, wenn versucht wird, das Asset zu öffnen. (CQ-4199234)
   * Das gleichzeitige Ändern von Dateien durch mehrere Benutzer kann dazu führen, dass einige Änderungen verloren gehen. Als Abhilfe können Sie die Funktion zum      Einchecken/Auschecken verwenden, um zu verhindern, dass mehrere Benutzer Änderungen an derselben Datei vornehmen (CQ-97035).
   * Bestimmte Applikationen unterstützen die Schreibschutzkennzeichnung nicht ordnungsgemäß. Dies ermöglicht es Benutzern, eine Datei zu speichern, die von einem anderen Benutzer ausgecheckt wurde. Die geänderte Datei wird erst dann übertragen, wenn der andere Benutzer die Datei wieder eincheckt. Die Änderungen der beiden Benutzer werden in AEM in zwei verschiedenen Versionen des Assets gespeichert (CQ-89551, CQ-87572, CQ-89615).
   * Der Ausgecheckt- und der Schreibschutzstatus werden unabhängig voneinander im Finder gemeldet. Dies führt zur Anzeige von zwei Schlosssymbolen, wenn ein Benutzer ein Asset auscheckt (CQ-89507).
* Finder-Integration:
   * Beim Ziehen großer Dateien per Drag-and-Drop kann es in Finder während der Übertragung großer Dateien im Hintergrund zu einer Zeitüberschreitung kommen. Das Ergebnis ist ein `Error - 36`. Als Problemumgehung können Sie das Asset erneut per Drag-and-Drop ziehen oder öffnen (CQ-4219628).
   * Das manuelle erneute Laden von Ordnern funktioniert nicht immer. Problemumgehung: Warten Sie 30 Sekunden, bis der Ordner automatisch aktualisiert wird. (CQ-97389)
   * Die Angaben unter „Weitere Asset-Informationen“ sind auf die Auswahl einer einzigen Datei begrenzt (CQ-89542, CQ-87656).
   * Die Option „In AEM Assets öffnen“ ist auf die Auswahl einzelner Dateien und Ordner begrenzt (CQ-83382).
   * Fehler beim Umbenennen von Assets, die keine Erweiterung aufweisen (CQ-4218971).
* Funktion zum Kopieren/EinfügenDie Option zum Einfügen wird angezeigt, obwohl kein Asset in die Zwischenablage kopiert wurde.
* Windows:
   * Dateien mit alternativen Datenströmen (ADS) werden nur in NTFS-Dateisystemen vollständig unterstützt. Das Kopieren derartiger Dateien auf die vom Desktop-Programm bereitgestellte WebDAV-Freigabe führt zur Anzeige einer Warnung, die den Benutzer darauf hinweist, dass die Datei Eigenschaften aufweist, die nicht an den neuen Speicherort kopiert werden können. Das ist normalerweise unproblematisch, da die Eigenschaften nur für eine bestimmte Applikation auf dem Desktop des Benutzers relevant sind und nichts mit dem eigentlichen Dateiinhalt zu tun haben (CQ-103770). (Win)
   * Unter Windows muss das Desktop-Programm von dem Benutzer installiert werden, der sie verwenden wird (CQ-4216389). (Win)
   * Das Programm kann abstürzen, wenn Benutzer unter bestimmten Umständen (nach Fortsetzen des Massen-Uploads nach einem Verbindungsabbruch) auf die Schaltfläche „Wiederholen“ für einen fehlgeschlagenen Upload klicken (CQ-4251884). (Win)

## Hilfreiche Ressourcen {#helpful-resources}

* [Dokumentation zu AEM](https://helpx.adobe.com/de/support/experience-manager/6-4.html)
* [Verwenden des AEM-Desktop-Programms, v1.x](use-app-v1.md)
* [Best Practices für das AEM-Desktop-Programm, v1.x](best-practices-for-v1.md)

## Kompatibilitätsmatrix und Voraussetzungen {#compatibilitymatrix}

Das AEM-Desktop-Programm ist mit verschiedenen AEM-Versionen kompatibel. Informationen zu den unterstützten Versionen finden Sie in der Kompatibilitätsmatrix.

| Version | Revision | Veröffentlichungsdatum | Kompatibilität |
|--- |--- |--- |--- |
| 1.10 | 1.10.0.3 (Mac und Win) | 31.08.2018 | AEM 6.5; AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.9 | 1.9.1.1 (Mac und Win) | 21.06.2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.8 | 1.8.1.0 (Mac und Win) | 28.03.2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
| 1.7 | 1.7.0.3 (Mac und Win) | 10.01.2018 | AEM 6.3 SP1; AEM 6.2 SP1 CFP2+; AEM 6.1 SP2 CFP7+ |
