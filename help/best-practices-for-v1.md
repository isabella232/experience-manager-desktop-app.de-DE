---
title: Best Practices für AEM Desktop-Apps Version 1.x
seo-title: Best Practices für AEM Desktop-Apps Version 1.x
description: Wichtige Funktionen und empfohlene Verwendung der Adobe Experience Manager-Desktop-App Version 1.x
seo-description: Wichtige Funktionen und empfohlene Verwendung der Adobe Experience Manager-Desktop-App Version 1.x
uuid: ba8fbc74-e1ad-4085-a031-ffd317628ba6
contentOwner: Agupta
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 57d5cd78-abce-4ede-a50e-7c161ddb43ae
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 946b853d740444853525e540ff7af1cbc46f9998

---


# Best Practices für AEM Desktop-Apps Version 1.x {#aem-desktop-app-best-practices}

## Überblick {#overview}

Die Adobe Experience Manager (AEM)-Desktop-App verknüpft Ihre Digital Asset Management (DAM)-Lösung mit Ihrem Desktop, damit Sie die in der AEM-Web-Benutzeroberfläche verfügbaren Dateien direkt auf dem Desktop öffnen können. Wenn Sie ein Asset vom Desktop aus speichern, wird es am entsprechenden Speicherort in AEM hochgeladen.

Mit der AEM-Desktop-App können Sie keine falschen lokalen Kopien aktualisieren oder ein falsches Asset in AEM aktualisieren. Der benutzerfreundliche Workflow von Desktop App wird mithilfe der Netzwerkfreigabetechnologie aktiviert, die von Desktop-Betriebssystemen bereitgestellt wird. 

Die Desktop-App bindet das AEM Assets-Repository als Netzwerkfreigabe auf dem Desktop. Daher sieht es so aus, als handle es sich um lokale Ordner und Dateien. Es wird jedoch nicht empfohlen, Digital Asset Management-Vorgänge direkt über den Desktop in der bereitgestellten Netzwerkfreigabe in Finder oder Explorer durchzuführen. Vielmehr empfiehlt Adobe, dass Sie Vorgänge wie das Kopieren oder Verschieben einer großen Anzahl von Assets über die AEM Assets-Webbenutzeroberfläche abwickeln.

>[!NOTE]
>
>Vor der Lektüre dieses Dokuments können Sie sich die allgemeinen [Best Practices zur AEM- und Creative Cloud-Integration](https://docs.adobe.com/content/help/en/experience-manager-64/assets/administer/aem-cc-integration-best-practices.html) durchlesen, wenn Sie sich zunächst einen Überblick über dieses Thema verschaffen möchten.

## AEM desktop app architecture {#aem-desktop-app-architecture}

Die AEM-Desktop-App verwendet WebDAV- (Windows) oder SMB- (Mac) Netzwerkfreigabe, um Netzwerkfreigabe bereitzustellen. Die bereitgestellte Netzwerkfreigabe liegt ausschließlich lokal vor. Die AEM-Desktop-App fängt die Aufrufe ab (Öffnen, Lesen, Schreiben) und bietet zusätzliche lokale Zwischenspeicherung. Die Applikation übersetzt Remote-Aufrufe an den AEM Assets-Server in optimierte AEM-HTTP-Anforderungen. Das folgende Diagramm zeigt die Architektur der AEM-Desktop-App.

![AEM Desktop-App-Architektur](assets/chlimage_1.png)

Das zusätzliche Caching bei Schreibvorgängen führt, wenn eine Datei gespeichert wird, dazu, dass die Datei zunächst lokal gespeichert wird (sodass der Benutzer nicht auf die Netzwerkübertragung warten muss). Dann nach einer vordefinierten Verzögerung (30 Sek.) wird zunächst die Datei im Hintergrund in AEM hochgeladen, dann auch das Asset. Die AEM-Desktop-App bietet eine Benutzeroberfläche zum Überwachen des Status von Hintergrunddatei-Uploads.

## Recommended use of AEM desktop app {#recommended-use-of-aem-desktop-app}

Die wichtigsten Funktionen der AEM-Desktop-App sind:

* Öffnen von Dateien aus der AEM Assets Web UI auf dem Desktop: Über die Web-Benutzeroberfläche können Sie Assets auf dem Desktop (im Finder, Explorer) anzeigen oder ein Asset mit einer Desktop-Anwendung öffnen.
* Aus- und Einchecken: Assets können zur Bearbeitung ausgecheckt werden. Für Benutzer sind die Assets dann in AEM Assets als gesperrt markiert. Nach dem Bearbeiten können die Assets dann wieder eingecheckt und damit entsperrt werden.
* Speichern von Änderungen in Dateien: Sämtliche Änderungen, die Sie in einer Datei in einer Netzwerkfreigabe speichern, werden automatisch in AEM hochgeladen. Außerdem wird eine neue Version erstellt.
* Verknüpfte Assets in anderen Dokumenten platzieren: In Anwendungen wie Creative Cloud (PS, ID, AI usw.) können Sie eine externe Datei als Link platzieren (beispielsweise können Sie ein Bild in einem InDesign-Dokument platzieren). In diesem Fall können Sie mit der Freigabe-Bereitstellung im Netzwerk Assets aus AEM zur Platzierung durchsuchen und auswählen. Verknüpfte Dateien können auch in Adobe-fremde Applikation wie MS Office platziert werden.
* Referenzauflösung in AEM: Wenn sowohl die platzierte(n) Datei(en) als auch die Hauptdatei(en) mit Link(en) in AEM gespeichert sind, können serverseitige Informationen zu den Asset-Verweisen automatisch bereitgestellt werden.
* Zugriff auf das Asset vom Desktop aus: In der gemounteten Netzwerkfreigabe bietet ein Kontextmenü ein Dialogfeld mit mehr Informationen (größere Vorschau, wichtige Metadaten) und die Möglichkeit, ein Asset in der AEM-Benutzeroberfläche zu öffnen.
* Große, hierarchische Ordner stapelweise hochladen: Wenn Sie die Option "Erstellen"&gt; "Ordner hochladen"in der AEM-Benutzeroberfläche verwenden, um Assets hochzuladen, lädt die AEM-Desktop-App die ausgewählte Ordnerhierarchie in AEM im Hintergrund hoch. Der Uploadfortschritt kann über eine dedizierte AEM Desktop App-Benutzeroberfläche überwacht werden.

## Inappropriate use of AEM desktop app {#inappropriate-use-of-aem-desktop-app}

* Verwenden Sie keine AEM-Desktop-App, um Assets vom Desktop zu verwalten. Die AEM-Desktop-App wurde nicht als Ersatz für Netzwerklaufwerke erstellt. Verwenden Sie stattdessen die folgenden Funktionen:
   * AEM Assets-Web-Benutzeroberfläche für die Verwaltung digitaler Assets (Suchen/Freigeben von Assets, Metadaten, Kopieren/Verschieben usw.)
   * AEM Desktop-App-Ordner hochladen, um große, hierarchische Ordner hochzuladen

* AEM Desktop-App nicht als "Desktop-Synchronisierungs"-Client für AEM Assets behandeln. Der Hauptvorteil der AEM-Desktop-App besteht darin, dass sie "virtuellen"Zugriff auf das gesamte Repository bietet und Desktop-Synchronisierungsanwendungen in der Regel nur Elemente eines Benutzers synchronisieren. Die AEM-Desktop-App bietet eine gewisse Stufe der Zwischenspeicherung und des Hochladevorgangs im Hintergrund. Es funktioniert weiterhin ganz anders als bei herkömmlichen Synchronisierungsanwendungen wie Adobe Creative Cloud-Desktop-App oder Microsoft OneDrive.
* Verwenden Sie keine AEM Desktop-App-Netzwerklaufwerke, um Assets häufig zu speichern. Alle Speichervorgänge werden an AEM Assets übertragen. Daher ist es unpraktisch, intensive Bearbeitungsvorgänge direkt in dem bereitgestellten AEM Assets-Repository durchzuführen. Wird ein Asset direkt im bereitgestellten Repository bearbeitet, wird die Zeitleiste des Assets mit irrelevanten Versionen „vollgestopft“ und der Server wird durch Mehraufwand belastet.
* Verwenden Sie keine AEM-Desktop-App für die Migration großer Datenmengen von einer AEM-Instanz in eine andere. Informationen zum Planen und Ausführen von Asset-Migrationen finden Sie im [Migrationshandbuch](https://helpx.adobe.com/experience-manager/6-4/assets/using/assets-migration-guide.html). In contrast, desktop app [supports bulk uploading](use-app-v1.md#bulkupload) large number of assets for the first time in AEM.

## Empfehlungen für ausgewählte Anwendungsbeispiele {#recommendations-for-selected-use-cases}

### Asset-Zugriff für kreative Benutzer {#access-to-assets-for-creative-users}

Die AEM-Desktop-App bietet virtuellen Zugriff auf das gesamte DAM-Repository - und es kann für kreative Benutzer auf dem Desktop schwierig sein, die richtigen Assets auf ihrem Desktop zu finden und darauf zuzugreifen. Wenden Sie diese Best Practices an, um diesen Vorgang für kreative Benutzer zu vereinfachen.

* Setzen Sie Collaboration-Funktionen in der AEM Assets-Webbenutzeroberfläche ein, um kreativen Benutzern einen direkteren Zugang zu den richtigen Assets zu ermöglichen. Hierzu gehören etwa die Freigabe von Ordnern oder Sammlungen, die Bereitstellung von Smart-Sammlungen (gespeicherten Suchen) oder der Versand von Benachrichtigungen mit Verweisen zu den richtigen Assets. Kreative Benutzer können dann auf ihrem Desktop mithilfe der Desktop-Aktionen der Webbenutzeroberfläche schnell auf diese Assets zugreifen.
* Legen Sie geeignete Berechtigungen für Assets (Zugriffssteuerung) fest, um die Anzeige des DAM-Repositorys für kreative Benutzer zu vereinfachen, indem Sie im Grunde den Zugriff dieser Benutzer auf die benötigten/interessanten Assets beschränken:

   * Bestimmte Bereiche, die für kreative Benutzer keine Relevanz haben, können den entsprechenden Benutzergruppen verweigert werden, damit sie diesen nicht angezeigt werden, auch nicht auf dem Desktop.
   * Die meisten Assets in DAM liegen in ihrer endgültigen Form vor und sind nicht zur Bearbeitung vorgesehen. Sie sollten daher schreibgeschützt werden, damit sie nicht von kreativen Benutzern geändert werden können.
   * Nur Assets, die geändert/überarbeitet werden müssen, sollten mit Schreibzugriff für kreative Benutzer versehen werden. Manche Unternehmen nutzen AEM-Projekte und die von ihnen erstellten Ordner zum Hosten von Assets, die noch Änderungen unterworfen sind.

### Suchen nach Assets {#searching-assets}

So suchen Sie nach einer Datei, die Sie auf dem Desktop öffnen möchten:

* Suchen Sie mithilfe der AEM Assets-Webbenutzeroberfläche nach dem Asset. Suchvorgänge  ist die Suche in AEM Assets leistungsstark (Suchfacetten, gespeicherte Suchen), bietet sie auch zusätzliche Funktionen, um das richtige Asset zu finden. Dazu gehören zusätzliche Filter wie die Suche nach Assets basierend auf dem Status (Genehmigung, Ablauf), Sammlungen, Aufgaben, Benachrichtigungen und Freigeben von Ordnern/Sammlungen für andere Benutzer/Gruppen.
* Wenn Sie das Asset gefunden haben, greifen Sie über die Option „Desktop-Aktionen“ der AEM-Benutzeroberfläche auf das Asset auf dem  Desktop .

### Updating assets opened using AEM desktop app {#updating-assets-opened-using-aem-desktop-app}

Wenn Sie ein Asset direkt in dem Verzeichnis bearbeiten, das AEM Assets einer lokalen Netzwerkfreigabe zugeordnet hat, wird das Asset bei jedem Speichervorgang auf dem Desktop in AEM hochgeladen. Außerdem erstellt AEM eine Version und generiert Wiedergaben.

Gehen Sie wie folgt vor, wenn ein in AEM gespeichertes Asset aktualisiert werden muss:

* For **minor updates**, such as minor retouching requests in the approval process:

   * Checken Sie die Datei aus und öffnen Sie sie auf dem Desktop.
   * Aktualisieren Sie die Datei.
   * Speichern Sie die aktualisierte Version. Das Asset wird aktualisiert und in der Zeitleiste wird die ursprüngliche Version zum Vergleich angezeigt.

* For **major updates**, such as a change request that requires a small creative WIP cycle:

   * Öffnen Sie mithilfe der Option „Anzeigen“ den entsprechenden Ordner auf dem Desktop.
   * Kopieren Sie die Datei in einen WIP-Ordner außerhalb der zugeordneten AEM Assets-Freigabe (kopieren Sie die Datei beispielsweise in einen mit der Adobe Creative Cloud-Desktop-App synchronisierten Ordner)
   * Arbeiten Sie an der Datei und speichern Sie sie zwischendurch. Die Änderungen werden nicht in AEM Assets gespeichert.
   * Wenn Sie die Bearbeitung abgeschlossen haben, verschieben, kopieren oder speichern Sie die von AEM zugeordnete Datei, um sie als neue Version hochzuladen.

## Netzwerkleistung {#network-performance}

Die optimale Benutzerfreundlichkeit bei der Verwendung der AEM-Desktop-App hängt in hohem Maße von einer guten und stabilen Netzwerkverbindung zwischen Desktop-Computern und AEM-Server sowie vom Server ab, der für eine gute Leistung optimiert ist, insbesondere beim Hochladen und Aktualisieren von Assets. Diese Empfehlungen gelten für Netzwerk-/IT-Teams von Unternehmen.

### Netzwerkhinweise {#network-considerations}

Die Best Practices für die AEM Assets-Netzwerkkonfiguration finden Sie im Dokument [Überlegungen zum AEM Assets-Netzwerk](https://helpx.adobe.com/experience-manager/6-4/assets/using/assets-network-considerations.html). Zu den wichtigen Aspekten, die zur Optimierung der AEM-Desktop-App für die Benutzer beitragen, zählen:

* **** Verwenden Sie ordnungsgemäß konfigurierten Dispatcher: Verwenden Sie AEM Dispatcher für zusätzliche Sicherheit und stellen Sie sicher, dass er für die Verbindung mit AEM [AEM Desktop-Apps mit einem Dispatcher konfiguriert ist](https://helpx.adobe.com/experience-manager/desktop-app/aem-desktop-app.html#ConnectingtoAEMBehindaDispatcher)

* **Brandbreiteneinsparung:** Ziehen Sie unter Mac eine Deaktivierung der Symbolvorschau in Finder in Betracht, wenn Sie das bereitgestellte Repository mit Finder durchsuchen. Finder fordert jede einzelne Datei an, um eine Vorschau zu erzeugen, und bewirkt, dass die AEM Desktop App das Asset herunterlädt und lokal im Cache speichert. Jedoch gilt es hierbei zu berücksichtigen, dass sich mit der eingesparten Brandbreite auch das Benutzererlebnis auf dem Desktop verschlechtert. So sollte daher beim Arbeiten mit Repositorys mit großen Assets und/oder begrenzter Brandbreite verfahren werden.

**** Hinweis: Um die Symbolvorschau zu deaktivieren, wählen Sie im Finder die Option "Anzeigeoptionen"und deaktivieren Sie dann die Option "Symbolvorschau anzeigen". Diese Einstellung bezieht sich nur auf den aktuellen Ordner. Um sie standardmäßig festzulegen, klicken Sie im selben Fenster auf die Schaltfläche „Als Standard verwenden“.

### Optimieren der Serverleistung {#optimizing-server-performance}

Informationen zur Leistungsoptimierung des AEM Assets-Servers finden Sie im [Handbuch zur AEM Assets-Leistungsoptimierung](https://helpx.adobe.com/in/experience-manager/6-4/assets/using/performance-tuning-guidelines.html). Bei einigen der wichtigen Aspekte der Serverleistung für AEM Desktop-Apps geht es um die Optimierung der Workflow-Konfiguration, sodass sie beim Hochladen von Assets gut funktioniert:

* **** Leistungsfähigeres Hochladen von Assets: Konfigurieren Sie das Workflow-Modell für die [AEM Asset-Aktualisierung so, dass es vorübergehend](https://helpx.adobe.com/experience-manager/6-4/assets/using/performance-tuning-guidelines.html#Workflows)ist.

* **** Serverprozessoren für Uploads beschränken: Stellen Sie sicher, dass der Parameter für parallele Arbeitsablaufaufträge korrekt eingestellt ist, damit bei Uploads nicht die gesamte CPU ausgefüllt wird.