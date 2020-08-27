---
title: Versionshinweise zum Adobe Experience Manager-Desktop-Programm
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für das Adobe Experience Manager-Desktop-Programm.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 91de08ba317de97a1d1900dc2351efcb4d6cf95f
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 94%

---


# Versionshinweise zum Adobe Experience Manager-Desktop-Programm {#release-notes-v2}

| Produkte | Adobe Experience Manager-Desktop-Programm |
|--- |--- |
| Programm-Version (Revision) | 2.0 (2.0.3.2) |
| Unterstützte AEM-Versionen | AEM as a Cloud Service; AEM 6.5; AEM 6.4; AEM 6.3 (mit Kompatibilitätspaket) |
| Typ | Nebenversion |
| Veröffentlichungsdatum | 27. August 2020 (Mac und Win) |
| Download-URLs | [macOS (64-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.3.2.dmg); [Windows (64-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.3.2.exe); [Windows (32-Bit)](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.3.2.exe) |

## Systemanforderungen und Voraussetzungen {#system-requirements-and-prerequisites-v2}

Das Adobe Experience Manager-Desktop-Programm ist mit den folgenden Betriebssystemen kompatibel:

* Mac OS X 10.14 oder höher mit aktuellen Fehlerbehebungen.

* Windows 10 mit den neuesten Service Packs und Fehlerbehebungen.

>[!NOTE]
>
>Windows 7 wird nicht mehr vom Anbieter unterstützt (https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020).

Das Programm funktioniert mit den folgenden Experience Manager-Versionen, unabhängig davon, ob sie als Cloud Service, auf Adobe Managed Services (AMS) oder on-Premise bereitgestellt werden:

* [Experience Manager as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/release-notes/home.html).

* [Experience Manager 6.5.0](https://docs.adobe.com/content/help/de-DE/experience-manager-65/release-notes/release-notes.html) oder höher.

* [Experience Manager 6.4.4](https://docs.adobe.com/content/help/de-DE/experience-manager-64/release-notes/release-notes.html) oder höher.

* Experience Manager 6.4.0 bis 6.4.3 mit [Kompatibilitätspaket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support).

>[!NOTE]
>
>Die Unterstützung des Desktop-Programms für Experience Manager 6.3 ist veraltet. Adobe empfiehlt ein Upgrade auf eine neuere und unterstützte Adobe Experience Manager-Version.
>Experience Manager 6.3.3.1 oder höher funktioniert mit dem Desktop-Programm, nachdem das [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) installiert wurde. Für Experience Manager 6.3 ist kein solches Paket verfügbar, da keine [Service Packs geplant](https://helpx.adobe.com/de/experience-manager/maintenance-releases-roadmap.html) sind.

Für die Version des Programms, die Sie auf Ihrem lokalen Computer installieren möchten, sind eine bestimmte Server-Version von Adobe Experience Manager oder zusätzliche Server-seitige Komponenten (Service Packs, Hotfixes oder Feature Packs) erforderlich. Wenden Sie sich an Ihren Adobe Experience Manager-Administrator, um Hilfe zu erhalten.

### Unterstützung verschiedener Asset- und Dateitypen {#support-for-file-types}

Das Programm unterstützt in Adobe Experience Manager gespeicherte Assets, die Binärdateien für die grundlegenden Vorgänge darstellen. Das Öffnen von Dateien in der nativen Desktop-Applikation hängt von der Betriebssystemverknüpfung bestimmter Dateitypen wie PNG oder JPG mit bestimmten Applikationen wie Mac Preview oder Adobe Photoshop ab.

Einige Dateitypen unterstützen das Platzieren von verknüpften Assets in der Binärdatei. Das Programm lädt die verknüpften Assets vorab herunter, sofern das Asset im Experience Manager-Repository vorhanden ist, wenn diese Binärdateien mit dem Desktop-Programm geöffnet werden. Derzeit werden folgende Dateitypen unterstützt:

* [!DNL Adobe InDesign]-Dateien (INDD-Format)
* [!DNL Adobe Illustrator]-Dateien (AI-Format)
* [!DNL Adobe Photoshop]-Dateien (PS-Format)

Die Funktion wird in den Adobe Creative Cloud-Versionen 2018 und 2019 der oben genannten Programme unterstützt. Das Programm verwendet einen heuristischen, Best-Match-Ansatz, um die lokalen Desktop-Pfade verknüpfter Assets URLs auf dem Experience Manager-Server zuzuordnen. Dieser Ansatz beruht auf den folgenden Annahmen:

* Pfade zu platzierten Dateien in der nativen Applikation verwenden einen globalen Desktop-Pfad (platziert von der lokalen Netzwerkfreigabe mit der Option [!UICONTROL Reveal]).

* Pfade werden von der nativen Applikation im XMP-Datensatz der Datei gespeichert.

* Experience Manager hat den XMP-Datensatz mit den Pfaden zum Metadaten-Datensatz des Assets extrahiert.

* Die Pfade können mit Assets in Experience Manager übereinstimmen (d. h. die platzierten Dateien befinden sich auch in Experience Manager unter einem übereinstimmenden Pfad).

## Neue Funktionen und Erweiterungen {#whats-new-added}

Weitere Informationen finden Sie unter [Neue Funktionen in v2.0](introduction.md#whats-new-v2).

**Aktualisierungen in der Programmversion 2.0.3**

Der in der aktuellen Version behobene Fehler lautet:

* Korrektur des Anmeldeproblems, das Windows-Benutzern auftrat, die versuchten, mithilfe der App auf das DAM-Repository in der [!DNL Adobe Experience Manager] 6.5.5.0-Instanz zuzugreifen.

**Aktualisierungen in der Programmversion 2.0.2**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Verbesserung der Upload-Leistung durch Erhöhung der Upload-Beschleunigung in [!UICONTROL Preferences]. Wenn diese Einstellung aktiviert ist, verwendet die App mehr lokale CPU-Threads und ist ressourcenintensiver.

* Problem mit Asset-Uploads behoben, wenn Dateinamen oder Pfade bestimmte GB18030-Zeichen enthalten. <!-- CQ-4283494 -->

* Die Option „Nach Relevanz sortieren“ ist verfügbar, nachdem in den Suchergebnissen zu einem anderen Sortiertyp gewechselt wurde. <!-- CQ-4286874 -->

* Im Desktop-Programm werden jetzt Unterordner aufgeführt, ohne dass dafür eine Aktualisierung erforderlich ist. <!-- CQ-4285711 -->

* (Windows) Ein seltener Fehler mit einer nicht verwendbaren Programm-Oberfläche auf einigen Windows-Computern wurde behoben. Benutzer können nicht auf die Programm-Oberfläche klicken, da sie verzerrt angezeigt wird und der Klickbereich der Oberflächenelemente seitlich „verschoben“ ist. <!-- CQ-4280785 -->

**Aktualisierungen in der Programmversion 2.0.1**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Option zum Konfigurieren des Verzeichnisses `%Temp%` entsprechend dem Pfad `%APPDATA%`. <!-- CQ-4282665 -->

* Benutzer können sich über die Okta-SAML-Authentifizierung bei der AEM-Autorenistanz anmelden. <!-- CQ-4278134 -->

## Installationsanweisungen {#installation-instructions-v2}

Informationen zum Installieren und Konfigurieren des Programms finden Sie unter [Installieren des Adobe Experience Manager-Desktop-Programms](install-upgrade.md).

Wenn Sie von einer vorherigen Version des Experience Manager-Desktop-Programms aktualisieren, müssen Sie die folgenden Best Practices für die Umstellung befolgen, die unter [Upgrade von früherer Version](install-upgrade.md#upgrade-from-previous-version) aufgeführt sind.

## Wichtige Hinweise zur Funktionsweise des Programms{#how-app-works}

Es ist wichtig, die folgenden Informationen zum Programm und dessen Funktionsweise zu verstehen.

* Das Programm bietet vollständige Kontrolle über Vorgänge, bei denen Asset-Binärdateien vollständig von und nach AEM übertragen werden müssen (Öffnen, Bearbeiten, Hochladen von Assets und Hochladen von Änderungen).

   * Wenn Sie mit dem Asset auf dem Desktop arbeiten möchten, müssen Sie es explizit auf Ihrem Desktop öffnen, bearbeiten oder herunterladen, entweder einzeln, in einem Ordner oder über eine Mehrfachauswahl.

   * Wenn Sie möchten, dass lokale Änderungen an in AEM hochgeladen werden, müssen Sie [!UICONTROL Upload Changes] entweder einzeln oder über eine Mehrfachauswahl auswählen.

   * Das Programm ist kein „Synchronisierungs-Client“, der Assets auf dem Desktop und in AEM synchron hält.

   * Das Programm stellt keine Netzwerkfreigabe bereit, die das AEM-Repository als eine virtuelle Ordnerstruktur zuordnet.

* Die Liste der vom Programm angezeigten Assets basiert auf dem Status des AEM Assets-Repositorys. Dateien, die lokal heruntergeladen und dann in den lokalen Dateien oder im Cache-Ordner umbenannt wurden, werden vom Programm nicht angezeigt oder verwaltet.

* Wenn das Programm nicht die erwarteten Ergebnisse anzeigt, klicken Sie in der oberen Leiste auf das Aktualisierungssymbol.

* Die lokale Netzwerkfreigabe, bei Verwendung der Aktion [!UICONTROL Reveal File]. Sie zeigt nur Dateien (und Ordner) an, die lokal verfügbar sind. [!UICONTROL Reveal File] und [!UICONTROL Reveal Folder] lädt Assets vorab herunter, damit die richtigen Assets in der lokalen Netzwerkfreigabe angezeigt werden.

* Die lokale Netzwerkfreigabe SMB (Mac)/WebDAV (Win) wird verwendet, wenn eine Adobe Creative Cloud-Applikation die Asset-Dateien liest, die verknüpft sind/in einer nativen Datei der Creative Cloud-Applikation platziert wurden.

Das folgende Diagramm zeigt den Fluss von Assets und Dateien von der Cloud zum lokalen Dateisystem und umgekehrt, der durch Benutzeraktionen initiiert wird.

![Fluss von Assets vom AEM-Server zu nativen Desktop-Applikationen über das Desktop-Programm](assets/da20_flow_diagram.png)

## Bekannte Probleme {#known-issues-v2}

**Probleme mit der Benutzeroberfläche:**

* Manchmal ist die Oberfläche des Desktop-Programms plötzlich leer. Klicken Sie mit der rechten Maustaste und klicken Sie auf [!UICONTROL Refresh], um das Programm erneut zu laden. Nach einer solchen Aktualisierung beginnen Sie im Stammverzeichnis des DAM-Repositorys. Aktualisierungen oder Status Ihrer Assets werden beibehalten. <!-- CQ-4270267 -->

* Schwierigkeiten beim Navigieren in Ordnern/Suchergebnissen ohne Trackpad oder Mauszeiger. Die Bildlaufleiste wird bei Mausgeräten ohne Mausrad möglicherweise nicht angezeigt. <!-- CQ-4269947 -->

* In seltenen Fällen wird die Fortschrittsleiste nicht korrekt angezeigt, wenn sich das hochgeladene Asset ändert.

* Nach dem Anwenden und Entfernen des Filters, um alle lokal bearbeiteten Assets zu finden, wechselt das Programm nicht zu den Suchergebnissen oder der Ordneransicht, mit denen die Benutzer begonnen haben. Das Programm zeigt den Stammordner des DAM-Repositorys an.

* Wenn Sie eine Verbindung zu einer URL herstellen, bei der kein AEM-Server ausgeführt wird, reagiert der Bildschirm „Verbindung“ manchmal nicht mehr. Beenden Sie das Programm und starten Sie es erneut.

**CRUD-Probleme (Erstellen, Lesen, Aktualisieren und Löschen):**

* Das Programm versucht, Dateien auch mit ungültigen Zeichen hochzuladen, was möglicherweise zu einem Server-seitigen Upload-Fehler führt. <!-- CQ-4273652 -->

* Beim Hochladen von Änderungen an einem Asset mit Kommentaren werden die Kommentare mit dem Asset in AEM gespeichert, sind jedoch nicht als Versionskommentare sichtbar. Dieses Problem wurde in AEM 6.4.5 und AEM 6.5.1 behoben. Adobe empfiehlt dringend, die neuesten Service Packs zu installieren. <!-- CQ-4268990 -->

* Asset-Übertragungen können vom Benutzer nicht abgebrochen werden. Wenn Sie eine unbeabsichtigte große Übertragung ausgelöst haben, beenden Sie das Programm und starten Sie es erneut. <!-- CQ-4278940 -->

**Plattformfragen:**

* Unter Windows ändert sich der Status eines Assets unter Umständen sofort nach dem Öffnen in [!UICONTROL Edited Locally], auch wenn Sie es möglicherweise nicht bearbeitet haben. Klicken Sie zur Aktualisierung auf [!UICONTROL Refresh].

>[!MORELIKETHIS]
>
>* [Dokumentation zu AEM as a Cloud Service](https://docs.adobe.com/content/help/de-DE/experience-manager-cloud-service/landing/home.translate.html)
>* [Dokumentation zu AEM as a Cloud Service Assets](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/home.html)
>* [Verwenden des Adobe Experience Manager-Desktop-Programms](using.md)
>* [Installieren und Aktualisieren des Desktop-Programms](install-upgrade.md)
>* [Best Practices und Tipps zur Fehlerbehebung](troubleshoot.md)

