---
title: Versionshinweise zur AEM-Desktop-App
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für die AEM-Desktop-App.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ad5337c8e1697d0a37d3020d25802dc1d732f320

---


# Versionshinweise zur AEM-Desktop-App {#release-notes-v2}

| Produkte | Adobe Experience Manager (AEM)-Desktop-App |
|---------------|--------------------------------------------------------------------|
| App-Version (Revision) | 2.0 (2.0.0.4) |
| Unterstützte AEM-Versionen | AEM 6.5, AEM 6.4, AEM 6.3 (mit Kompatibilitätspaket) |
| Typ | Hauptversion |
| Veröffentlichungsdatum | 30. August 2019 (Mac), 9. September 2019 (Win) |
| Download-URLs | [MacOS (64-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.0.4.dmg); [Windows (64-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.0.4.exe); [Windows (32-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.0.4.exe) |

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites-v2}

Die AEM-Desktop-App ist mit den folgenden Betriebssystemen kompatibel:

* Mac OS X 10.10 oder höher mit aktuellen Fehlerbehebungen.
* Windows 7 und Windows 10 mit den neuesten Service Packs und Fehlerbehebungen.

Die App kann mit den folgenden AEM-Versionen verwendet werden, unabhängig davon, ob sie lokal oder auf Adobe Managed Services (AMS) bereitgestellt werden:

* [AEM 6.5.0 ](https://helpx.adobe.com/experience-manager/6-5/release-notes.html) oder höher
* [AEM 6.4.4 ](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) oder höher
* AEM 6.4.0–6.4.3 mit [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* AEM 6.3.3.1 und höher mit [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)
* Für AEM 6.3 sind keine [Service Packs geplant](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html). Adobe empfiehlt die Aktualisierung auf eine spätere AEM-Version.

Für die Version der AEM-Desktop-App, die Sie auf Ihrem lokalen Computer installieren möchten, sind eine bestimmte Server-Version von Adobe Experience Manager oder zusätzliche Server-seitige Komponenten (Service Packs, Hotfixes oder Feature Packs) erforderlich. Wenden Sie sich zwecks Hilfe an Ihren AEM-Administrator.

### Unterstützung verschiedener Asset- und Dateitypen {#support-for-file-types}

Die App unterstützt in AEM gespeicherte Assets, die binäre Dateien für die grundlegenden Vorgänge darstellen. Das Öffnen von Dateien in der nativen Desktop-Applikation hängt von der Betriebssystemverknüpfung bestimmter Dateitypen wie PNG oder JPG mit bestimmten Applikationen wie Mac Preview oder Adobe Photoshop ab.

Einige Dateitypen unterstützen das Platzieren von verknüpften Assets in der Binärdatei. Die App lädt die verknüpften Assets vorab herunter, wenn das Asset im AEM-Repository vorhanden ist, wenn diese Binärdateien mit der Desktop-App geöffnet werden. Derzeit werden folgende Dateitypen unterstützt:

* Adobe InDesign-Dateien (INDD-Format)
* Adobe Illustrator-Dateien (AI-Format)
* Adobe Photoshop-Dateien (PS-Format)

Die Funktion wird den oben genannten Applikationen in Adobe Creative Cloud 2018 und Creative Cloud 2019 unterstützt. Die App verwendet einen heuristischen, Best-Match-Ansatz, um die lokalen Desktop-Pfade verknüpfter Assets URLs auf dem AEM-Server zuzuordnen. Er beruht auf einigen Annahmen:

* Pfade zu platzierten Dateien in der nativen Applikation verwenden einen globalen Desktop-Pfad (platziert von der lokalen Netzwerkfreigabe mit der Option „Anzeigen“)
* Pfade werden von der nativen Applikation im XMP-Datensatz der Datei gespeichert
* AEM hat den XMP-Datensatz mit den Pfaden zum Metadaten-Datensatz des Assets extrahiert.
* Die Pfade können mit Assets in AEM übereinstimmen (d. h. die platzierten Dateien befinden sich auch in AEM unter einem übereinstimmenden Pfad).

## Neue Funktionen und Erweiterungen {#whats-new-added}

Weitere Informationen finden Sie unter [Neue Funktionen in der App](introduction.md#whats-new-v2).

## Installationsanweisungen {#installation-instructions-v2}

Informationen zum Installieren und Konfigurieren der App finden Sie unter [Installieren der AEM-Desktop-App](install-upgrade.md).

Wenn Sie von einer vorherigen AEM-Desktop-App aktualisieren, müssen Sie die folgenden Best Practices für die Umstellung befolgen, die unter [Upgrade von früherer Version](install-upgrade.md#upgrade-from-previous-version) aufgeführt werden.

## Wichtige Hinweise zur Funktionsweise der App {#how-app-works}

Es ist wichtig, die folgenden Informationen zur App und deren Funktionsweise zu verstehen.

* Die App bietet vollständige Kontrolle über Vorgänge, bei denen Asset-Binärdateien vollständig von und nach AEM übertragen werden müssen (Öffnen, Bearbeiten, Hochladen von Assets und Hochladen von Änderungen).
   * Wenn Sie mit dem Asset auf dem Desktop arbeiten möchten, müssen Sie es explizit auf Ihrem Desktop öffnen, bearbeiten oder herunterladen, entweder einzeln, in einem Ordner oder über eine Mehrfachauswahl.
   * Wenn Sie möchten, dass lokale Änderungen an in AEM hochgeladen werden, müssen Sie [!UICONTROL Upload Changes] entweder einzeln oder über eine Mehrfachauswahl auswählen.
   * Die App ist kein „Synchronisierungs-Client“, der Assets auf dem Desktop und in AEM synchron hält.
   * Die App stellt keine Netzwerkfreigabe bereit, die das AEM-Repository als eine virtuelle Ordnerstruktur zuordnet.
* Die Liste der von der App angezeigten Assets basiert auf dem Status des AEM Assets-Repositorys. Dateien, die lokal heruntergeladen und dann in den lokalen Dateien oder im Cache-Ordner umbenannt wurden, werden von der App nicht angezeigt oder verwaltet.
* Wenn die App nicht die erwarteten Ergebnisse anzeigt, klicken Sie in der oberen Leiste auf das Aktualisierungssymbol.
* Die lokale Netzwerkfreigabe, bei Verwendung der Aktion [!UICONTROL Reveal File]. Sie zeigt nur Dateien (und Ordner) an, die lokal verfügbar sind. [!UICONTROL Reveal File] und [!UICONTROL Reveal Folder] lädt Assets vorab herunter, damit die richtigen Assets in der lokalen Netzwerkfreigabe angezeigt werden.
* Die lokale Netzwerkfreigabe SMB (Mac)/WebDAV (Win) wird verwendet, wenn eine Adobe Creative Cloud-Applikation die Asset-Dateien liest, die verknüpft sind/in einer nativen Datei der Creative Cloud-Applikation platziert wurden.

Das folgende Diagramm zeigt den Fluss von Assets und Dateien von der Cloud zum lokalen Dateisystem und umgekehrt, der durch Benutzeraktionen initiiert wird.

![Fluss von Assets vom AEM-Server zu nativen Desktop-Applikationen über die Desktop-App](assets/da20_flow_diagram.png)

## Bekannte Probleme {#known-issues-v2}

**Probleme mit der Benutzeroberfläche:**
* Manchmal kann die Oberfläche der Desktop-App leer sein. Right-click and click [!UICONTROL Refresh] to re-load the application. Nach einer solchen Aktualisierung beginnen Sie am Stammordner des DAM-Repositorys. Aktualisierungen oder Status Ihrer Assets werden beibehalten. <!-- CQ-4270267 -->
* Die Navigation in Ordnern/Suchergebnissen ohne Trackpad oder Mauszeiger ist schwierig. The scroll-bar might not appear with mouse devices without mouse wheel. <!-- CQ-4269947 -->
* In seltenen Fällen wird die Fortschrittsleiste nicht korrekt angezeigt, wenn sich das hochgeladene Asset ändert.
* Nach dem Anwenden und Entfernen des Filters, um alle lokal bearbeiteten Assets zu finden, wechselt die App nicht zu den Suchergebnissen oder der Ordneransicht, mit denen die Benutzer begonnen haben. Die App zeigt den Stammordner des DAM-Repositorys an.
* Wenn Sie eine Verbindung zu einer URL herstellen, bei der kein AEM-Server ausgeführt wird, reagiert der Bildschirm „Verbindung“ manchmal nicht mehr. Beenden Sie die App und starten Sie sie erneut.

**CRUD-Probleme (Erstellen, Lesen, Aktualisieren und Löschen):**
* Die App versucht, Dateien auch mit ungültigen Zeichen hochzuladen, was möglicherweise zu einem Server-seitigen Upload-Fehler führt. <!-- CQ-4273652 -->
* Beim Hochladen von Änderungen zu einem Asset mit Kommentaren werden die Kommentare zusammen mit dem Asset in AEM gespeichert, jedoch nicht als Versionskommentare sichtbar. Dieses Problem wurde in AEM 6.4.5 und AEM 6.5.1 behoben. Adobe empfiehlt dringend, die neuesten Service Packs zu installieren. <!-- CQ-4268990 -->
* Asset-Übertragungen können vom Benutzer nicht abgebrochen werden. Wenn Sie eine unbeabsichtigte große Übertragung ausgelöst haben, beenden Sie die App und starten Sie sie erneut. <!-- CQ-4278940 -->

**Plattformfragen:**
* Unter Windows ändert sich der Status eines Assets unter Umständen sofort nach dem Öffnen in [!UICONTROL Edited Locally], auch wenn Sie es möglicherweise nicht bearbeitet haben. Klicken Sie zur Aktualisierung auf [!UICONTROL Refresh].

>[!MORELIKETHIS]
>
>* [Dokumentation zu AEM 6.5](https://helpx.adobe.com/support/experience-manager/6-5.html)
>* [Dokumentation zu AEM Assets 6.5](https://docs.adobe.com/content/help/en/experience-manager-64/assets/home.html)
>* [Verwenden der AEM-Desktop-App](using.md)
>* [Installieren und Aktualisieren der Desktop-App](install-upgrade.md)
>* [Best Practices und Fehlerbehebung](troubleshoot.md)

