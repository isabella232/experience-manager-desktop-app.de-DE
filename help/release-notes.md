---
title: Versionshinweise zur AEM Desktop-App
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für die AEM-Desktop-App.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f9c2347f8f17d32479207980fafba058825d986f

---


# AEM desktop app Release Notes {#release-notes-v2}

| Produkte | Adobe Experience Manager (AEM)-Desktop-App |
|---------------|--------------------------------------------------------------------|
| App-Version (Revision) | 2.0 (2.0.0.4) |
| Unterstützte AEM-Versionen | AEM 6.5, AEM 6.4, AEM 6.3 (mit Kompatibilitätspaket) |
| Typ | Hauptversion |
| Veröffentlichungsdatum | 30. August 2019 (Mac), 9. September 2019 (Win) |
| Download-URLs | [MacOS 64-Bit](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.0.4.dmg); [Windows 64-Bit](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.0.4.exe); 32-Bit- [Windows](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.0.4.exe) |

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites-v2}

Die AEM-Desktop-App ist mit den folgenden Betriebssystemen kompatibel:

* Mac OS X 10.10 oder höher mit aktuellen Fehlerbehebungen.
* Windows7 und Windows 10 mit den neuesten Service Packs und Fehlerbehebungen.

Die App kann mit den folgenden AEM-Versionen verwendet werden, unabhängig davon, ob sie lokal oder auf Adobe Managed Services (AMS) bereitgestellt werden:

* [AEM 6.5.0](https://helpx.adobe.com/experience-manager/6-5/release-notes.html) oder höher
* [AEM 6.4.4](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) oder höher
* AEM 6.4.0 - 6.4.3 mit [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* AEM 6.3.3.1 und höher mit [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* Für AEM 6.3 sind keine [Service Packs geplant](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html). Adobe empfiehlt die Aktualisierung auf eine spätere AEM-Version.

Die Version der App, die Sie auf Ihrem lokalen Computer installieren möchten, erfordert eine bestimmte Adobe Experience Manager-Serverversion/zusätzliche serverseitige Komponenten (Service Packs, Hotfixes oder Feature Packs). Wenden Sie sich zwecks Hilfe an Ihren AEM-Administrator.

### Unterstützung verschiedener Asset- und Dateitypen {#support-for-file-types}

Die Anwendung unterstützt in AEM gespeicherte Assets, die binäre Dateien für die grundlegenden Vorgänge darstellen. Das Öffnen von Dateien in der nativen Desktop-Anwendung hängt von der Betriebssystemverknüpfung bestimmter Dateitypen wie PNG oder JPG mit bestimmten Anwendungen wie Mac Preview oder Adobe Fotoshop ab.

Einige Dateitypen unterstützen das Platzieren von verknüpften Elementen in der Binärdatei. Die Anwendung lädt die verknüpften Assets vorab herunter, wenn das Asset im AEM-Repository vorhanden ist, wenn diese Binärdateien mit der Desktop-App geöffnet werden. Derzeit werden folgende Dateitypen unterstützt:

* Adobe InDesign-Dateien (INDD-Format)
* Adobe Illustrator-Dateien (AI-Format)
* Adobe Fotoshop-Dateien (PS-Format)

Die Funktion wird von Adobe Creative Cloud 2018 und Creative Cloud 2019-Versionen der oben genannten Anwendung unterstützt. Die App verwendet einen heuristischen, am besten übereinstimmenden Ansatz, um die lokalen Desktop-Pfade verknüpfter Assets URLs auf dem AEM-Server zuzuordnen. Er beruht auf einigen Annahmen:

* Pfade zu platzierten Dateien in der nativen Anwendung verwenden einen globalen Desktop-Pfad (platziert von der lokalen Netzwerkfreigabe mit der Option "Anzeigen")
* Pfade werden von der nativen App im XMP-Datensatz der Datei gespeichert
* AEM hat den XMP-Datensatz mit den Pfaden zum Metadaten-Datensatz des Assets extrahiert
* Die Pfade können mit Assets in AEM übereinstimmen (d. h. die platzierten Dateien befinden sich auch in AEM unter einem übereinstimmenden Pfad)

## Neue Funktionen und Erweiterungen {#whats-new-added}

Weitere Informationen finden Sie unter [Neue Funktionen in der App](introduction.md#whats-new-v2).

## Installationsanweisungen {#installation-instructions-v2}

Informationen zum Installieren und Konfigurieren der App finden Sie unter AEM Desktop-App [installieren](install-upgrade.md).

Wenn Sie von einer vorherigen AEM-Desktop-App aktualisieren, müssen Sie die folgenden Best Practices für die Umstellung befolgen, die beim [Upgrade von einer früheren Version](install-upgrade.md#upgrade-from-previous-version)aufgeführt werden.

## Wichtige Hinweise zur Funktionsweise der App {#how-app-works}

Es ist wichtig, die folgenden Informationen zur Anwendung und deren Funktionsweise zu verstehen.

* Die Anwendung bietet vollständige Kontrolle über Vorgänge, bei denen Asset-Binärdateien vollständig von und nach AEM übertragen werden müssen (Öffnen, Bearbeiten, Hochladen von Änderungen und Hochladen von Assets).
   * Wenn Sie mit dem Asset auf dem Desktop arbeiten möchten, müssen Sie es explizit auf Ihrem Desktop öffnen, bearbeiten oder herunterladen, entweder einzeln, in einem Ordner oder über eine Mehrfachauswahl.
   * Wenn Sie lokale Änderungen an Assets erhalten möchten, die auf AEM hochgeladen wurden, müssen Sie diese entweder einzeln oder über eine Mehrfachauswahl auswählen [!UICONTROL Upload Changes].
   * Die Anwendung ist kein "Synchronisierungs-Client", der Assets über den Desktop und AEM synchronisiert.
   * Die Anwendung stellt keine Netzwerkfreigabe bereit, die das AEM-Repository als eine virtuelle Ordnerstruktur zuordnet.
* Die Liste der von der Anwendung angezeigten Elemente basiert auf dem Status des AEM Assets-Repositorys. Dateien, die lokal heruntergeladen und dann in den lokalen Dateien oder im Cache-Ordner umbenannt wurden, werden von der Anwendung nicht angezeigt oder verwaltet.
* Wenn die App nicht die erwarteten Ergebnisse anzeigt, klicken Sie in der oberen Leiste auf das Aktualisierungssymbol.
* Die lokale Netzwerkfreigabe (bei Verwendung der [!UICONTROL Reveal File] Aktion) zeigt nur Dateien (und Ordner) an, die lokal verfügbar sind. [!UICONTROL Reveal File] und [!UICONTROL Reveal Folder] lädt Assets vorab herunter, damit die richtigen Assets im lokalen Netzwerkfreigabe angezeigt werden.
* SMB (Mac)/WebDAV (Win) wird lokale Netzwerkfreigabe verwendet, wenn eine Adobe Creative Cloud-App die Asset-Dateien liest, die verknüpft sind/in einer nativen Datei der Creative Cloud-App platziert wurden.

Das folgende Diagramm zeigt den Fluss von Assets und Dateien von der Cloud zum lokalen Dateisystem und umgekehrt, wie durch Benutzeraktionen initiiert.

![Fluss von Assets vom AEM-Server zu nativen Desktop-Apps über die Desktop-App](assets/da20_flow_diagram.png)

## Bekannte Probleme {#known-issues-v2}

**Probleme mit der Benutzeroberfläche:**
* Manchmal wird die Oberfläche der Desktop-App leer. Klicken Sie mit der rechten Maustaste und klicken Sie auf [!UICONTROL Refresh] , um die Anwendung erneut zu laden. Durch eine solche Aktualisierung wird der Status der App zurückgesetzt und Sie beginnen im Startbildschirm im Stammverzeichnis des DAM-Repositorys. <!-- CQ-4270267 -->
* Schwierigkeiten beim Navigieren in Ordnern/Suchergebnissen ohne Trackpad oder Mausrad. Die Bildlaufleiste wird möglicherweise nicht mit Mausgeräten ohne Mausrad angezeigt. <!-- CQ-4269947 -->
* In seltenen Fällen wird die Fortschrittsleiste nicht korrekt angezeigt, wenn sich das hochgeladene Asset ändert.
* Nach dem Anwenden und Entfernen des Filters, um alle lokal bearbeiteten Assets zu finden, gelangt die App nicht zu den Suchergebnissen oder der Ordneransicht, mit denen die Benutzer begonnen haben. Die App zeigt den Stammordner des DAM-Repositorys an.
* Wenn Sie eine Verbindung zu einer URL herstellen, bei der kein AEM-Server ausgeführt wird, reagiert der Bildschirm "Verbindung"manchmal nicht mehr. Beenden Sie die Anwendung und starten Sie sie erneut.

**CRUD-Probleme (Erstellen, Lesen, Aktualisieren und Löschen):**
* Die Anwendung versucht, Dateien auch mit ungültigen Zeichen hochzuladen, was möglicherweise zu einem serverseitigen Upload-Fehler führt. <!-- CQ-4273652 -->
* Beim Hochladen von Änderungen zu einem Asset mit Kommentaren werden die Kommentare mit dem Asset in AEM gespeichert, sind jedoch nicht als Versionskommentare sichtbar (Lösung in AEM 6.4.5, 6.5.1). <!-- CQ-4268990 -->
* Asset-Übertragungen können vom Benutzer nicht abgebrochen werden. Wenn Sie eine unbeabsichtigte große Übertragung ausgelöst haben, beenden Sie die Anwendung und starten Sie sie erneut. <!-- CQ-4278940 -->

**Plattformfragen:**
* Unter Windows ändert sich der Status eines Assets unter Umständen sofort nach dem Öffnen in [!UICONTROL Edited Locally] , auch wenn Sie ihn möglicherweise nicht bearbeitet haben. Klicken Sie [!UICONTROL Refresh] zur Aktualisierung auf .

>[!MORELIKETHIS]
>
>* [Dokumentation zu AEM 6.5](https://helpx.adobe.com/support/experience-manager/6-5.html)
>* [Dokumentation zu AEM Assets 6.5](https://docs.adobe.com/content/help/en/experience-manager-64/assets/home.html)
>* [Verwenden der AEM-Desktop-App](using.md)
>* [Installieren und Aktualisieren der Desktop-App](install-upgrade.md)
>* [Best Practices und Tipps zur Fehlerbehebung](troubleshoot.md)

