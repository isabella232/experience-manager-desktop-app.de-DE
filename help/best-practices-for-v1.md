---
title: Best Practices für das [!DNL Adobe Experience Manager]-Desktop-Programm Version 1.x
description: Wichtige Funktionen und empfohlene Verwendung der  [!DNL Adobe Experience Manager] -Desktop-Programm Version 1.x.
translation-type: ht
source-git-commit: a25c1fa13895ae9eb7268e3e01c83a5f0b9d7d1d
workflow-type: ht
source-wordcount: '1686'
ht-degree: 100%

---


# Best Practices für das AEM-Desktop-Programm, v1.x {#aem-desktop-app-best-practices}

## Überblick {#overview}

Das [!DNL Adobe Experience Manager]-Desktop-Programm verknüpft Ihre Digital Asset Management-Lösung (DAM) mit dem Desktop, damit Sie in der AEM-Web-Benutzeroberfläche verfügbare Dateien direkt auf dem Desktop öffnen können. Wenn Sie ein Asset vom Desktop aus speichern, wird es in den entsprechenden Speicherort in AEM hochgeladen.

Das AEM-Desktop-Programm verhindert auf diese Weise, dass die falschen lokalen Kopien oder die falschen Assets in AEM aktualisiert werden. Der benutzerfreundliche Workflow des Desktop-Programms wird mithilfe der Netzwerkfreigabetechnologie aktiviert, die von Desktop-Betriebssystemen bereitgestellt wird.

Das Desktop-Programm stellt das AEM Assets-Repository als Netzwerkfreigabe auf dem Desktop bereit. Daher sieht es so aus, als handle es sich um lokale Ordner und Dateien. Es wird jedoch nicht empfohlen, Digital Asset Management-Vorgänge direkt über den Desktop in der bereitgestellten Netzwerkfreigabe in Finder oder Explorer durchzuführen. Vielmehr empfiehlt Adobe, dass Sie Vorgänge wie das Kopieren oder Verschieben einer großen Anzahl von Assets über die AEM Assets-Web-Benutzeroberfläche abwickeln.

>[!NOTE]
>
>Vor der Lektüre dieses Dokuments können Sie sich die allgemeinen [Best Practices zur AEM- und Creative Cloud-Integration](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/aem-cc-integration-best-practices.html?lang=de) durchlesen, wenn Sie sich zunächst einen Überblick über dieses Thema verschaffen möchten.

## Architektur des AEM-Desktop-Programms {#aem-desktop-app-architecture}

Das AEM-Desktop-Programm stellt Netzwerkfreigaben über WebDAV (Windows) oder SMB (Mac) bereit. Die bereitgestellte Netzwerkfreigabe liegt ausschließlich lokal vor. Das AEM-Desktop-Programm fängt die Aufrufe (Öffnen, Lesen, Schreiben) ab und bietet zusätzliches lokales Caching. Das Programm übersetzt Remote-Aufrufe an den AEM Assets-Server in optimierte AEM-HTTP-Anforderungen. Die folgende Abbildung zeigt die Architektur des AEM-Desktop-Programms.

![Architektur des AEM-Desktop-Programms](assets/arch_v1.png)

*Abbildung: Architektur des Desktop-Programms*

Das zusätzliche Caching bei Schreibvorgängen führt, wenn eine Datei gespeichert wird, dazu, dass die Datei zunächst lokal gespeichert wird (sodass der Benutzer nicht auf die Netzwerkübertragung warten muss). Dann nach einer vordefinierten Verzögerung (30 Sekunden) die Datei zunächst im Hintergrund in AEM hochgeladen, woraufhin dann das Asset hochgeladen wird. Das AEM-Desktop-Programm verfügt über eine Benutzeroberfläche zum Überwachen des Status von Datei-Uploads im Hintergrund.

## Verwendungsempfehlung für das AEM-Desktop-Programm {#recommended-use-of-aem-desktop-app}

Zu den Hauptfunktionen und -merkmalen des AEM-Desktop-Programms gehören u. a.:

* **Öffnen von Dateien auf dem Desktop über die AEM Assets-Web-Benutzeroberfläche**. Sie können über die Web-Benutzeroberfläche Assets auf dem Desktop (in Finder, Explorer) anzeigen oder ein Asset mithilfe eines Desktop-Programms öffnen.

* **Aus- und Einchecken**. Assets können zur Bearbeitung ausgecheckt werden. Für Benutzer sind die Assets dann in AEM Assets als gesperrt markiert. Nach dem Bearbeiten können die Assets dann wieder eingecheckt und damit entsperrt werden.

* **Speichern von Änderungen in Dateien**. Sämtliche Änderungen, die Sie in einer Datei in einer Netzwerkfreigabe speichern, werden automatisch in AEM hochgeladen. Außerdem wird eine neue Version erstellt.

* **Platzieren von verknüpften Assets in anderen Dokumenten**. In Programmen wie Creative Cloud ([!DNL Adobe Photoshop], [!DNL Adobe InDesign] und [!DNL Adobe Illustrator]) können Sie eine externe Datei als Verknüpfung platzieren. Sie können beispielsweise ein Bild in einem InDesign-Dokument platzieren. In diesem Fall können Sie mit der bereitgestellten Netzwerkfreigabe Assets aus AEM zur Platzierung durchsuchen und auswählen. Verknüpfte Dateien können auch in Adobe-fremden Programmen wie MS Office platziert werden.

* **Auflösen von Verweisen in AEM**. Wenn sowohl die platzierte(n) Datei(en) als auch die Hauptdatei mit Verknüpfung in AEM gespeichert sind, können Server-seitige Informationen zu Asset-Verweisen automatisch bereitgestellt werden.

* **Asset-Zugriff über den Desktop**. In der bereitgestellten Netzwerkfreigabe kann über ein Kontextmenü das Dialogfeld [!UICONTROL More Info] mit weiteren Informationen (größere Vorschau, wichtige Metadaten) aufgerufen werden. Außerdem ist es möglich, ein Asset in der AEM-Benutzeroberfläche zu öffnen.

* **Massen-Upload von großen, hierarchischen Ordnern**. Wenn Sie Assets mit der Option „Erstellen“ > „Ordner hochladen“ der AEM-Benutzeroberfläche hochladen, lädt das AEM-Desktop-Programm die ausgewählte Ordnerhierarchie im Hintergrund in AEM hoch. Der Upload-Fortschritt kann über eine dedizierte Benutzeroberfläche im AEM-Desktop-Programm überwacht werden.

## Unsachgemäße Verwendung des AEM-Desktop-Programms {#inappropriate-use-of-aem-desktop-app}

* Setzen Sie das AEM-Desktop-Programm nicht ein, um Assets über den Desktop zu verwalten. Das AEM-Desktop-Programm wurde nicht als Ersatz für Netzlaufwerke entwickelt. Verwenden Sie stattdessen die folgenden Funktionen:

   * AEM Assets-Web-Benutzeroberfläche für Digital Asset Management (Suchen/Freigeben von Assets, Metadaten, Kopieren/Verschieben usw.).

   * [!UICONTROL Folder Upload]-Funktion des AEM-Desktop-Programms für den Uploads von großen, hierarchischen Ordnern.

* Behandeln Sie das AEM-Desktop-Programm nicht als Client zur Desktop-Synchronisierung für AEM Assets. Der Hauptvorteil des AEM-Desktop-Programms besteht hier darin, dass sie einen „virtuellen“ Zugriff auf das gesamte Repository ermöglicht, während Programme zur Desktop-Synchronisierung normalerweise nur die Assets synchronisieren, die dem jeweiligen Benutzer gehören. Das AEM-Desktop-Programm bietet gewisse Caching-Möglichkeiten und Hintergrund-Uploads; dennoch unterscheidet sich die Funktionsweise stark von typischen Synchronisierungsprogrammen wie dem Adobe Creative Cloud-Desktop-Programm oder Microsoft OneDrive.

* Setzen Sie AEM-Desktop-Programm-Netzlaufwerke nicht zum regelmäßigen Speichern von Assets ein. Alle Speichervorgänge werden an AEM Assets übertragen. Daher ist es unpraktisch, intensive Bearbeitungsvorgänge direkt in dem bereitgestellten AEM Assets-Repository durchzuführen. Wird ein Asset direkt im bereitgestellten Repository bearbeitet, wird die Zeitleiste des Assets mit irrelevanten Versionen „vollgestopft“ und der Server wird durch Mehraufwand belastet.

* Setzen Sie das AEM-Desktop-Programm nicht ein, um große Datenmengen von einer AEM-Instanz zu einer anderen zu migrieren. Informationen zum Planen und Ausführen von Asset-Migrationen finden Sie im [Migrationshandbuch](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html?lang=de). Das AEM-Desktop-Programm ist stattdessen darauf ausgelegt, Assets via [Massen-Upload](use-app-v1.md#bulkupload) erstmalig in [!DNL Adobe Experience Manager] hochzuladen.

## Empfehlungen für ausgewählte Anwendungsfälle {#recommendations-for-selected-use-cases}

### Asset-Zugriff für kreative Benutzer {#access-to-assets-for-creative-users}

Das AEM-Desktop-Programm ermöglicht einen virtuellen Zugriff auf das gesamte DAM-Repository. Dabei kann es sich für kreative Benutzer als schwierig herausstellen, die richtigen Assets zu finden und auf diese über ihren Desktop zuzugreifen. Wenden Sie diese Best Practices an, um diesen Vorgang für kreative Benutzer zu vereinfachen.

* Verwenden Sie die Funktionen zur Zusammenarbeit der Web-Benutzeroberfläche von AEM Assets, um kreativen Benutzern einen direkteren Zugang zu den richtigen Assets zu ermöglichen. Hierzu gehören etwa die Freigabe von Ordnern oder Sammlungen, die Bereitstellung von Smart-Sammlungen (gespeicherten Suchen) oder der Versand von Benachrichtigungen mit Verweisen zu den richtigen Assets. Kreative Benutzer können dann auf ihrem Desktop mithilfe der Desktop-Aktionen der Web-Benutzeroberfläche schnell auf diese Assets zugreifen.

* Legen Sie geeignete Berechtigungen für Assets (Zugriffssteuerung) fest, um die Anzeige des DAM-Repositorys für kreative Benutzer zu vereinfachen, indem Sie im Grunde den Zugriff dieser Benutzer auf die benötigten/interessanten Assets beschränken:

   * Bestimmte Bereiche, die für kreative Benutzer keine Relevanz haben, können den entsprechenden Benutzergruppen verweigert werden, damit sie diesen nicht angezeigt werden, auch nicht auf dem Desktop.

   * Die meisten Assets in DAM liegen in ihrer endgültigen Form vor und sind nicht zur Bearbeitung vorgesehen. Sie sollten daher schreibgeschützt sein, damit sie nicht von kreativen Benutzern geändert werden können.

   * Nur Assets, die geändert/überarbeitet werden müssen, sollten mit Schreibzugriff für kreative Benutzer versehen werden. Manche Unternehmen nutzen AEM-Projekte und die von ihnen erstellten Ordner zum Hosten von Assets, die noch Änderungen unterworfen sind.

### Suchen nach Assets {#searching-assets}

So suchen Sie nach einer Datei, die Sie auf dem Desktop öffnen möchten:

* Suchen Sie mithilfe der AEM Assets-Web-Benutzeroberfläche nach dem Asset. Suchvorgänge in AEM Assets sind nicht nur leistungsstark (Suchfacetten, gespeicherte Suchen), sie bieten darüber hinaus zusätzliche Funktionen zum Auffinden des richtigen Assets. Dazu gehören zusätzliche Filter wie die Suche nach Assets basierend auf dem Status (Genehmigung, Ablauf), Sammlungen, Aufgaben, Benachrichtigungen und Freigeben von Ordnern/Sammlungen für andere Benutzer/Gruppen.

* Wenn Sie das Asset gefunden haben, greifen Sie über die Option „Desktop-Aktionen“ der AEM-Benutzeroberfläche auf das Asset auf dem Desktop zu.

### Aktualisieren von geöffneten Assets mit dem AEM-Desktop-Programm {#updating-assets-opened-using-aem-desktop-app}

Wenn Sie ein Asset direkt in dem Verzeichnis bearbeiten, das AEM Assets einer lokalen Netzwerkfreigabe zugeordnet hat, wird das Asset bei jedem Speichervorgang auf dem Desktop in AEM hochgeladen. Außerdem erstellt AEM eine Version und generiert Wiedergaben.

Gehen Sie wie folgt vor, wenn ein in AEM gespeichertes Asset aktualisiert werden muss:

* Bei **geringfügigen Aktualisierungen**, etwa Anforderungen kleinerer Überarbeitungen im Genehmigungsprozess:

   * Checken Sie die Datei aus und öffnen Sie sie auf dem Desktop.

   * Aktualisieren Sie die Datei.

   * Speichern Sie die aktualisierte Version. Das Asset wird aktualisiert und in der Zeitleiste wird die ursprüngliche Version zum Vergleich angezeigt.

* Bei **umfassenden Aktualisierungen** wie einer Änderungsanforderung, für die ein kleiner kreativer WIP-Zyklus erforderlich ist:

   * Öffnen Sie mithilfe der Option „Anzeigen“ den entsprechenden Ordner auf dem Desktop.

   * Kopieren Sie die Datei in einen WIP-Ordner außerhalb der zugeordneten AEM Assets-Freigabe. (Kopieren Sie die Datei beispielsweise in einen mit dem Adobe Creative Cloud-Desktop-Programm synchronisierten Ordner.)

   * Arbeiten Sie an der Datei und speichern Sie sie zwischendurch. Die Änderungen werden nicht in AEM Assets gespeichert.

   * Wenn Sie die Bearbeitung abgeschlossen haben, verschieben, kopieren oder speichern Sie die von AEM zugeordnete Datei, um sie als neue Version hochzuladen.

## Netzwerkleistung {#network-performance}

Für ein positives Benutzererlebnis mit dem AEM-Desktop-Programm kommt es in erster Linie auf eine gute, stabile Netzwerkverbindung zwischen Benutzer-Desktops und dem AEM-Server an. Außerdem muss der Server für eine gute Leistung abgestimmt sein, insbesondere in Bezug auf das Hochladen und Aktualisieren von Assets. Diese Empfehlungen gelten für Netzwerk-/IT-Teams von Unternehmen.

### Überlegungen zum Netzwerk {#network-considerations}

Die Best Practices für die AEM Assets-Netzwerkkonfiguration finden Sie im Dokument [Überlegungen zum AEM Assets-Netzwerk](https://experienceleague.adobe.com/docs/experience-manager-64/assets/administer/assets-migration-guide.html?lang=de). Folgende Aspekte sind u. a. beim Optimieren des AEM-Desktop-Programm-Erlebnisses für Benutzer nützlich:

* **Ordnungsgemäße Dispatcher-Konfiguration**. Nutzen Sie AEM Dispatcher, um für zusätzliche Sicherheit zu sorgen, und stellen Sie sicher, dass dieser für eine [Verbindung des AEM-Desktop-Programms mit AEM hinter einem Dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher) konfiguriert ist.

* **Brandbreiteneinsparung**. Ziehen Sie unter Mac OS eine Deaktivierung der Symbolvorschau in Finder in Betracht, wenn Sie das bereitgestellte Repository mit Finder durchsuchen. Finder fordert jede einzelne Datei an, um eine Vorschau zu erzeugen, und bewirkt, dass das Desktop-Programm das Asset herunterlädt und lokal im Cache speichert. Jedoch gilt es hierbei zu berücksichtigen, dass sich mit der eingesparten Brandbreite auch das Benutzererlebnis auf dem Desktop verschlechtert. So sollte daher beim Arbeiten mit Repositorys mit großen Assets und/oder begrenzter Brandbreite verfahren werden.

>[!NOTE]
>
>Zum Deaktivieren der Symbolvorschau wählen Sie im Finder-Menü „Ansicht“ den Eintrag „Anzeigeoptionen“ und deaktivieren Sie dann die Option „Symbolvorschau einblenden“. Diese Einstellung bezieht sich nur auf den aktuellen Ordner. Um sie standardmäßig festzulegen, klicken Sie im selben Fenster auf die Schaltfläche „Als Standard verwenden“.

### Optimieren der Serverleistung {#optimizing-server-performance}

Informationen zur Leistungsoptimierung des AEM Assets-Servers finden Sie im [Handbuch zur Optimierung der AEM Assets-Leistung](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html?lang=de). Einige wichtige Aspekte im Zusammenhang mit der Server-Leistung des AEM-Desktop-Programms beziehen sich auf das Optimieren der Workflow-Konfiguration für Asset-Uploads:

* **Leistungsstärkere Asset-Uploads**. Konfigurieren Sie das [AEM-Workflow-Modell „AEM-Asset-Update“ als Übergangs-Workflow](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html?lang=de).

* **Server-Prozessoren für Uploads beschränken**. Stellen Sie sicher, dass der Parameter für parallele Workflow-Aufträge korrekt eingestellt ist, damit bei Uploads nicht die gesamte CPU ausgereizt wird.
