---
title: '[!DNL Adobe Experience Manager] Versionshinweise zum Desktop-Programm'
description: Versionshinweise, Verbesserungen, neue Funktionen, Kompatibilität und Downloadlinks für das [!DNL Adobe Experience Manager] -Desktop-Programm.
mini-toc-levels: 1
feature: Desktop-App, Versionsinformationen
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
translation-type: tm+mt
source-git-commit: ac533db59b2a5c64243b762f4b77b3148c4f1867
workflow-type: tm+mt
source-wordcount: '1523'
ht-degree: 98%

---

# [!DNL Adobe Experience Manager] Versionshinweise zum Desktop-Programm {#release-notes-v2}

Die Versionshinweise für die neueste Desktop-Programm-Version 2.1 (2.1.2.0) finden Sie unten. Das Veröffentlichungsdatum ist der 26. März 2021. Es handelt sich um eine kleinere Version mit einer Verbesserung.

Die **unterstützten [!DNL Experience Manager]-Versionen** sind:

* [!DNL Experience Manager] as a [!DNL Cloud Service]. Siehe [Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/home.html?lang=de).
* [!DNL Experience Manager] 6.5.0 oder höher, für Adobe Managed Services (AMS) oder On-Premise. Weitere Informationen finden Sie in den [Versionshinweisen zum Service Pack](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=de).
* [!DNL Experience Manager] 6.4.4 oder höher, für Adobe Managed Services (AMS) oder On-Premise. Weitere Informationen finden Sie in den [Versionshinweisen zum Service Pack](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html?lang=de).
* [!DNL Experience Manager] 6.4.0–6.4.3 mit installiertem [Kompatibilitätspaket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support), für Adobe Managed Services (AMS) oder On-Premise.
* [!DNL Experience Manager] 6.3 (mit Kompatibilitätspaket)
* [!DNL Experience Manager] 6.3.3.1 oder höher mit installiertem [Kompatibilitätspaket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support). Das Desktop-Programm wird für [!DNL Experience Manager] 6.3.3.0 oder frühere Versionen nicht unterstützt.

Das [!DNL Adobe Experience Manager]-Desktop-Programm ist für die folgenden **Betriebssysteme** verfügbar:

* macOS X 10.14 oder höher mit aktuellen Fehlerbehebungen. [Mac-Computer mit Apple ](https://support.apple.com/de-de/HT211814) siliconare werden noch nicht unterstützt.
* Windows 10 mit den aktuellen Service Packs und Fehlerbehebungen.

Die **Download-URLs** für die unterstützten Betriebssysteme sind:

| Betriebssystem | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS 64-Bit | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.2.0.dmg) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.2.0.dmg) |
| Windows 64-Bit | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.2.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.2.0.exe) |
| Windows 32-Bit | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.2.0.exe) | [Download-Link](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.2.0.exe) |

>[!NOTE]
>
>Windows 7 wird nicht mehr unterstützt. Nähere Informationen finden Sie im [Artikel über das Ende der Unterstützung von Windows 7](https://support.microsoft.com/de-de/help/4057281/windows-7-support-ended-on-january-14-2020).

<!-- The version of the app you plan to install on your local machine requires a specific [!DNL Adobe Experience Manager] server version/additional server-side components (service packs, hot fixes, or feature packs). Contact your [!DNL Experience Manager] administrator for help.
-->

## Unterstützung verschiedener Asset- und Dateitypen {#support-for-file-types}

Das Programm unterstützt in [!DNL Experience Manager] gespeicherte Assets, die Binärdateien für die grundlegenden Vorgänge darstellen. Das Öffnen von Dateien im nativen Desktop-Programm hängt von der Betriebssystemverknüpfung bestimmter Dateitypen wie PNG oder JPG mit bestimmten Programmen wie Mac Preview oder Adobe Photoshop ab.

Einige Dateitypen unterstützen das Platzieren von verknüpften Assets in der Binärdatei. Das Programm lädt die verknüpften Assets vorab herunter, falls das Asset im [!DNL Experience Manager]-Repository vorhanden ist, wenn diese Binärdateien mit dem Desktop-Programm geöffnet werden. Derzeit werden folgende Dateitypen unterstützt:

* [!DNL Adobe InDesign]-Dateien (INDD-Format)
* [!DNL Adobe Illustrator]-Dateien (AI-Format)
* [!DNL Adobe Photoshop]-Dateien (PS-Format)

Diese Funktion wird in den Versionen [!DNL Adobe Creative Cloud] 2018 und [!DNL Adobe Creative Cloud] 2019 des oben genannten Programms unterstützt. Das Programm verwendet einen heuristischen Best-Match-Ansatz, um die lokalen Desktop-Pfade verknüpfter Assets URLs auf dem [!DNL Experience Manager]-Server zuzuordnen. Dieser Ansatz beruht auf den folgenden Annahmen:

* Pfade zu platzierten Dateien im nativen Programm verwenden einen globalen Desktop-Pfad (platziert von der lokalen Netzwerkfreigabe mit der Option [!UICONTROL Reveal]).

* Pfade werden vom nativen Programm im XMP-Datensatz der Datei gespeichert.

* [!DNL Experience Manager] hat den XMP-Datensatz mit den Pfaden zum Metadaten-Datensatz des Assets extrahiert.

* Die Pfade können mit Assets in [!DNL Experience Manager] übereinstimmen, das heißt, die platzierten Dateien befinden sich auch in [!DNL Experience Manager] unter einem übereinstimmenden Pfad.

## Neue Funktionen, Verbesserungen und Fehlerbehebungen {#what-is-new}

Weitere Informationen finden Sie unter [Neue Funktionen in Version 2.0](introduction.md#whats-new-v2).

**Aktualisierung in der Programmversion 2.1.2.0**

* Dem Hauptmenü des Programms wurde eine neue Option [!UICONTROL Clear Cookies] hinzugefügt. Sie hilft bei möglichen Anmeldeproblemen, z. B. beim Wechsel der Verbindung von einem Server zu einem anderen. Siehe [Löschen von Cookies vor dem Verbinden](/help/troubleshoot.md#cannot-login-cookies-issue).

**Aktualisierung in der Programmversion 2.1.1.0**

* Mit einer erweiterten Einstellung kann das Programm das Programmverhalten der Version 1.10 beim Hochladen von Ordnern emulieren. In Version 1.10 berücksichtigen die im Repository erstellten Knotennamen die Leerzeichen und die Groß-/Kleinschreibung der vom Benutzer angegebenen Ordnernamen. Das Standardverhalten von Version 2.1 bleibt weiterhin erhalten, d. h. mehrere Leerzeichen in Ordnernamen werden durch einen Bindestrich im Repository-Knotennamen ersetzt und die Knotennamen werden in Kleinbuchstaben umgewandelt. Weitere Informationen finden Sie in den [Programmvoreinstellungen](/help/install-upgrade.md#set-preferences).

**Aktualisierung in der Programmversion 2.1.0.0**

* Um Assets hochzuladen, können Benutzer die Dateien oder Ordner jetzt direkt aus dem Windows Explorer oder Mac Finder auf die Benutzeroberfläche des Programms ziehen. Dies funktioniert zusätzlich zu der im Programm bereits verfügbaren Upload-Option. <!-- CQ-4309527 -->

**Aktualisierung in der Programmversion 2.0.3**

Folgender Fehler wurde in der aktuellen Version behoben:

* Das Anmeldeproblem für Programmbenutzer unter Windows, die versuchen, auf das DAM-Repository unter [!DNL Adobe Experience Manager] 6.5.5.0 zuzugreifen, wurde behoben.

**Aktualisierungen in der Programmversion 2.0.2**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Die Einstellung für die Upload-Beschleunigung ist jetzt verfügbar, um die Upload-Leistung zu steigern. Wenn diese Einstellung aktiviert ist, verwendet das Programm mehr lokale CPU-Threads und ist ressourcenintensiver, um schnellere Uploads durchzuführen.

* Das Hochladen von Assets funktioniert jetzt, wenn Dateinamen oder Pfade bestimmte GB18030-Zeichen enthalten. <!-- CQ-4283494 -->

* Die Option „Nach Relevanz sortieren“ ist verfügbar, nachdem in den Suchergebnissen zu einem anderen Sortiertyp gewechselt wurde. <!-- CQ-4286874 -->

* Im Desktop-Programm werden jetzt Unterordner aufgeführt, ohne dass dafür eine Aktualisierung erforderlich ist. <!-- CQ-4285711 -->

* (Windows) Ein seltener Fehler mit einer nicht verwendbaren Programm-Oberfläche auf einigen Windows-Computern wurde behoben. Benutzer können nicht auf die Programm-Oberfläche klicken, da sie verzerrt angezeigt wird und der Klickbereich der Oberflächenelemente seitlich „verschoben“ ist. <!-- CQ-4280785 -->

**Aktualisierungen in der Programmversion 2.0.1**

Die folgenden Fehlerbehebungen und Aktualisierungen sind verfügbar:

* Option zum Konfigurieren des Verzeichnisses `%Temp%` entsprechend dem Pfad `%APPDATA%`. <!-- CQ-4282665 -->

* Benutzer können sich über die Okta-SAML-Authentifizierung bei der [!DNL Experience Manager]-Autoreninstanz anmelden. <!-- CQ-4278134 -->

## Installationsanweisungen {#installation-instructions-v2}

Informationen zum Installieren und Konfigurieren des Programms finden Sie unter [Installieren des [!DNL Experience Manager] -Desktop-Programms](install-upgrade.md).

Wenn Sie von einer vorherigen Version des [!DNL Experience Manager]-Desktop-Programms aktualisieren, müssen Sie die folgenden Best Practices für die Umstellung befolgen, die unter [Upgrade von früherer Version](install-upgrade.md#upgrade-from-previous-version) aufgeführt werden.

## Wichtige Hinweise zur Funktionsweise des Programms {#how-app-works}

Es ist wichtig, die folgenden Informationen zum Programm und dessen Funktionsweise zu verstehen.

* Das Programm bietet vollständige Kontrolle über Vorgänge, bei denen Asset-Binärdateien vollständig von und nach [!DNL Experience Manager] übertragen werden müssen (Öffnen, Bearbeiten, Hochladen von Assets und Hochladen von Änderungen).

   * Wenn Sie mit dem Asset auf dem Desktop arbeiten möchten, müssen Sie es explizit auf Ihrem Desktop öffnen, bearbeiten oder herunterladen, entweder einzeln, in einem Ordner oder über eine Mehrfachauswahl.

   * Wenn Sie möchten, dass lokale Änderungen an Assets nach [!DNL Experience Manager] hochgeladen werden, müssen Sie [!UICONTROL Upload Changes] entweder einzeln oder über eine Mehrfachauswahl auswählen.

   * Das Programm ist kein Synchronisierungs-Client, der Assets auf dem Desktop und in [!DNL Experience Manager] synchronisiert.

   * Das Programm stellt keine Netzwerkfreigabe bereit, die das [!DNL Experience Manager]-Repository als eine virtuelle Ordnerstruktur zuordnet.

* Die Liste der vom Programm angezeigten Assets basiert auf dem Status des Assets-Repositorys. Dateien, die lokal heruntergeladen und dann in den lokalen Dateien oder im Cache-Ordner umbenannt wurden, werden vom Programm nicht angezeigt oder verwaltet.

* Wenn das Programm nicht die erwarteten Ergebnisse anzeigt, klicken Sie in der oberen Leiste auf das Aktualisierungssymbol.

* Die lokale Netzwerkfreigabe, bei Verwendung der Aktion [!UICONTROL Reveal File]. Sie zeigt nur Dateien (und Ordner) an, die lokal verfügbar sind. [!UICONTROL Reveal File] und [!UICONTROL Reveal Folder] lädt Assets vorab herunter, damit die richtigen Assets in der lokalen Netzwerkfreigabe angezeigt werden.

* Die lokale Netzwerkfreigabe SMB (Mac)/WebDAV (Win) wird verwendet, wenn ein Adobe Creative Cloud-Programm die Asset-Dateien liest, die verknüpft sind/in einer nativen Datei des Creative Cloud-Programms platziert wurden.

Das folgende Diagramm zeigt den Fluss von Assets und Dateien von der Cloud zum lokalen Dateisystem und umgekehrt, der durch Benutzeraktionen initiiert wird.

![Fluss von Assets vom [!DNL Experience Manager]-Server zu nativen Desktop-Programmen über das Desktop-Programm](assets/da20_flow_diagram.png)

## Bekannte Probleme {#known-issues-v2}

**Probleme mit der Benutzeroberfläche:**

* Manchmal ist die Oberfläche des Desktop-Programms plötzlich leer. Klicken Sie mit der rechten Maustaste und klicken Sie auf [!UICONTROL Refresh], um das Programm erneut zu laden. Nach einer solchen Aktualisierung beginnen Sie im Stammverzeichnis des DAM-Repositorys. Aktualisierungen oder Status Ihrer Assets werden beibehalten. <!-- CQ-4270267 -->

* Schwierigkeiten beim Navigieren in Ordnern/Suchergebnissen ohne Trackpad oder Mauszeiger. Die Bildlaufleiste wird bei Mausgeräten ohne Mausrad möglicherweise nicht angezeigt. <!-- CQ-4269947 -->

* In seltenen Fällen wird die Fortschrittsleiste nicht korrekt angezeigt, wenn sich das hochgeladene Asset ändert.

* Nach dem Anwenden und Entfernen des Filters, um alle lokal bearbeiteten Assets zu finden, wechselt das Programm nicht zu den Suchergebnissen oder der Ordneransicht, mit denen die Benutzer begonnen haben. Das Programm zeigt den Stammordner des DAM-Repositorys an.

* Wenn Sie eine Verbindung zu einer URL herstellen, bei der kein [!DNL Experience Manager]-Server ausgeführt wird, reagiert der Bildschirm „Verbindung“ manchmal nicht mehr. Beenden Sie das Programm und starten Sie es erneut.

**CRUD-Probleme (Erstellen, Lesen, Aktualisieren und Löschen):**

* Das Programm versucht, Dateien auch mit ungültigen Zeichen hochzuladen, was möglicherweise zu einem Server-seitigen Upload-Fehler führt. <!-- CQ-4273652 -->

* Beim Hochladen von Änderungen an einem Asset mit Kommentaren werden die Kommentare mit dem Asset in [!DNL Experience Manager] gespeichert, sind jedoch nicht als Versionskommentare sichtbar. Dieses Problem wurde in [!DNL Experience Manager] 6.4.5. und [!DNL Experience Manager] 6.5.1. behoben. Adobe empfiehlt dringend, die neuesten Service Packs zu installieren. <!-- CQ-4268990 -->

* Asset-Übertragungen können vom Benutzer nicht abgebrochen werden. Wenn Sie eine unbeabsichtigte große Übertragung ausgelöst haben, beenden Sie das Programm und starten Sie es erneut. <!-- CQ-4278940 -->

**Plattformfragen:**

* Unter Windows ändert sich der Status eines Assets unter Umständen sofort nach dem Öffnen in [!UICONTROL Edited Locally], auch wenn Sie es möglicherweise nicht bearbeitet haben. Klicken Sie zur Aktualisierung auf [!UICONTROL Refresh].

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=de)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] Dokumentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=de)
>* [Verwenden des [!DNL Experience Manager] -Desktop-Programms](using.md)
>* [Installieren und Aktualisieren des Desktop-Programms](install-upgrade.md)
>* [Best Practices und Tipps zur Fehlerbehebung](troubleshoot.md)

