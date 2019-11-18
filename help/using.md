---
title: Verwenden der AEM-Desktop-App
description: Erfahren Sie, wie Sie die Adobe Experience Manager-Desktop-App installieren und verwenden, um mit AEM-Assets direkt von Ihrem Win- oder Mac-Desktop aus zu arbeiten. Machen Sie sich mit Best Practices und Informationen zur Fehlerbehebung vertraut.
uuid: 55057617-89de-43cd-8419-1252a42ab2fb
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 39d7bcad-d7b0-4978-a790-4cb68b8a7d6a
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 850d2c21a796599ed40164e7d6f892967563c16b

---


# Use AEM desktop app {#use-aem-desktop-app-v2}

Verwenden Sie die Adobe Experience Manager (AEM)-Desktop-App, um einfach auf die AEM-Assets auf Ihrem lokalen Desktop zuzugreifen und diese Assets in allen Desktop-Anwendungen zu verwenden. Sie können die Assets in Desktop-Anwendungen öffnen und die Assets lokal bearbeiten. Laden Sie die Änderungen mit Versionskontrolle zurück, um sie für andere Benutzer freizugeben. Sie können auch neue Dateien und Ordnerhierarchien in AEM hochladen, Ordner erstellen und Assets oder Ordner aus AEM löschen.

Die Integration ermöglicht es verschiedenen Rollen in der Organisation, die Assets zentral in AEM Assets zu verwalten und auf die Assets auf dem lokalen Desktop in den nativen Anwendungen unter Windows oder Mac OS zuzugreifen.

Wenn Sie die Anwendung nach dem Abmelden oder zum ersten Mal öffnen, geben Sie die URL Ihres AEM-Servers ein. Klicken Sie auf „Verknüpfen“. Geben Sie Ihre Anmeldeinformationen ein, um die App mit dem Server zu verbinden.

Die Hauptaufgaben, die Sie mit der AEM-Desktop-App ausführen, sind:

![Arbeitsabläufe und Aufgaben, die Sie mit der AEM-Desktop-](assets/do-not-localize/whats-new-desktop-app-v2.png "App ausführen könnenArbeitsabläufe und Aufgaben, die Sie mit der AEM-Desktop-App")ausführen könnenLaden Sie [diese](assets/do-not-localize/aem_desktop_app_usecases_print.pdf) druckfertige PDF-Datei herunter.

## Funktionsweise von Desktop-Apps {#how-app-works2}

Bevor Sie mit der Anwendung beginnen, sollten Sie wissen, [wie die App funktioniert](release-notes.md#how-app-works). Machen Sie sich auch mit den folgenden Begriffen vertraut:

* **[!UICONTROL Desktop Actions]**: In der Assets-Weboberfläche können Sie in einem Browser die Asset-Speicherorte erkunden oder das Asset auschecken und zur Bearbeitung in Ihrer nativen Desktop-Anwendung öffnen. Diese Aktionen sind über die Weboberfläche verfügbar und verwenden die Funktionalität der Desktop-App. Erfahren Sie, [wie Sie Desktop-Aktionen](using.md#desktopactions-v2)aktivieren.

* Dateistatus **[!UICONTROL Cloud Only]**: Solche Assets werden nicht auf den lokalen Computer heruntergeladen und stehen nur auf dem AEM-Server zur Verfügung.

* Dateistatus **[!UICONTROL Available locally]**: Die Assets werden wie bisher heruntergeladen und stehen auf dem lokalen Computer zur Verfügung. Die Assets werden nicht geändert.

* Dateistatus **[!UICONTROL Edited locally]**: Diese Assets werden lokal geändert und die Änderungen bleiben beim Hochladen auf den AEM-Server erhalten. Nach dem Hochladen ändert sich der Status in [!UICONTROL Available locally]. Siehe [Bearbeiten von Assets](using.md#edit-assets-upload-updated-assets).

* Dateistatus **[!UICONTROL Editing conflict]**: Wenn Sie und andere Benutzer ein Asset gleichzeitig ändern, zeigt die App an, dass ein Bearbeitungskonflikt aufgetreten ist. Die App bietet außerdem Optionen zum Beibehalten oder Verwerfen Ihrer Änderungen. Erfahren Sie, [wie Sie Bearbeitungskonflikte](using.md#adv-workflow-collaborate-avoid-conflicts)vermeiden können.

* Dateistatus **[!UICONTROL Modified remotely]**: Die App gibt an, ob ein heruntergeladenes Asset auf dem AEM-Server geändert wurde. Die App bietet auch die Möglichkeit, die neueste Version herunterzuladen und Ihre lokale Kopie zu aktualisieren. Erfahren Sie, [wie Sie Bearbeitungskonflikte](using.md#adv-workflow-collaborate-avoid-conflicts)vermeiden können.

* **Checkout**: Wenn Sie eine Datei bearbeiten oder eine Datei bearbeiten möchten, können Sie den Status zum Auschecken wechseln. Es wird ein Sperrsymbol für das Asset in der App und der AEM-Weboberfläche hinzugefügt. Das Symbol Sperren zeigt anderen Benutzern an, dass sie dasselbe Asset nicht gleichzeitig bearbeiten müssen, da es zu einem Bearbeitungskonflikt führt.

* **Check-in**: Markieren Sie das Asset als sicher, damit andere Benutzer es bearbeiten können, ohne dass ein Bearbeitungskonflikt entsteht. Wenn Sie Ihre Änderungen hochladen, wird das Sperrsymbol automatisch entfernt. Durch das Umschalten des Eincheckstatus wird auch das Schloss-Symbol entfernt. Es wird jedoch empfohlen, nicht manuell einzuchecken, ohne die Änderungen hochzuladen. Wenn Sie Ihre Änderungen verwerfen, können Sie den Check-in manuell aktivieren.

* **[!UICONTROL Open]** Aktion: Öffnen Sie einfach das Asset, um es in der nativen Anwendung anzuzeigen. Es wird nicht empfohlen, das Asset mit dieser Aktion zu bearbeiten, da das Asset nicht ausgecheckt wird und andere Benutzer Änderungen vornehmen können, die zu Bearbeitungskonflikten führen.

* **[!UICONTROL Edit]** Aktion: Verwenden Sie die Aktion, um das Bild zu ändern. Durch Klicken auf [!UICONTROL Edit] "Aktion"wird das Asset automatisch ausgecheckt und ein Sperrsymbol für das Asset hinzugefügt. Wenn Sie nach dem Klicken auf Bearbeiten das Asset nicht bearbeiten möchten, klicken Sie auf [!UICONTROL Toggle check-in]. Verwenden Sie zum Löschen, Umbenennen oder Verschieben von Assets in der AEM DAM-Ordnerhierarchie die AEM-Weboberflächenaktionen und nicht die Bearbeitungsaktion.

* **[!UICONTROL Download]** Aktion: Laden Sie das Asset auf Ihren lokalen Computer herunter. Sie können die Assets jetzt herunterladen und später bearbeiten. offline arbeiten und die Änderungen später hochladen. Assets werden in einen Cache-Ordner auf Ihrem Dateisystem heruntergeladen.

* **[!UICONTROL Reveal File]** oder **[!UICONTROL Reveal Folder]** Aktion: Während die Assets in einen lokalen Cache-Ordner heruntergeladen werden, imitiert die App ein lokales Netzwerklaufwerk und stellt für jedes Asset einen lokalen Pfad bereit. Um diesen Pfad zu kennen, verwenden Sie die entsprechende Einblendeoption in der App. Zum Platzieren von Assets in der Creative Cloud-Anwendung ist eine Anzeigeaktion erforderlich. Siehe [Platzieren von Assets](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** Aktion: Um das Asset in der AEM-Weboberfläche anzuzeigen, öffnen Sie es im Web. Sie können weitere Arbeitsabläufe über die AEM-Oberfläche auslösen, z. B. das Aktualisieren von Metadaten oder die Asset-Erkennung.

* **[!UICONTROL Delete]** Aktion: Löschen Sie das Asset aus dem AEM DAM-Repository. Durch die Aktion wird die Originalkopie des Assets auf dem AEM-Server gelöscht. Wenn Sie nur Änderungen am lokalen Asset verwerfen möchten, lesen Sie [Änderungen](using.md#edit-assets-upload-updated-assets)verwerfen.

* **[!UICONTROL Upload Changes]**: Die Desktop-App lädt das aktualisierte Asset nur hoch, wenn Sie es explizit auf den AEM-Server hochladen. Wenn Sie Ihre Änderungen speichern, werden diese nur auf Ihrem lokalen Computer gespeichert. Beim Hochladen wird das Asset automatisch eingecheckt und das Sperrsymbol entfernt. Siehe [Bearbeiten von Assets](using.md#edit-assets-upload-updated-assets).

## Aktivieren von Desktop-Aktionen in der AEM-Webbenutzeroberfläche {#desktopactions-v2}

In der Benutzeroberfläche "Assets"in einem Browser können Sie die Asset-Speicherorte erkunden oder das Asset auschecken und zur Bearbeitung in Ihrer Desktop-Anwendung öffnen. These options are called [!UICONTROL Desktop Actions] and are not enabled by default. Gehen Sie zur Aktivierung wie folgt vor.

1. In the Assets console, click/tap the **[!UICONTROL User]** icon from the toolbar.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL My Preferences]** , um das **[!UICONTROL Preferences]** Dialogfeld anzuzeigen.
1. Wählen Sie im Dialogfeld "Benutzereinstellungen" **[!UICONTROL Show Desktop Actions For Assets]**. Klicken/Tippen **[!UICONTROL Accept]**.

   ![„Desktop-Aktionen für Assets anzeigen“ aktivieren, um Desktop-Aktionen zu ermöglichen](assets/chlimage_1-3.png)

   Aktivieren [!UICONTROL Show Desktop Actions For Assets] von Desktop-Aktionen

## Durchsuchen, Suchen und Anzeigen einer Vorschau von Assets {#browse-search-preview-assets}

Sie können die im AEM-Repository verfügbaren Assets innerhalb der Desktop-Anwendung durchsuchen, suchen und in der Vorschau anzeigen. Versuchen Sie Folgendes in der App:

1. Navigieren Sie zu einem Ordner und sehen Sie einige grundlegende Informationen zu den im Ordner verfügbaren Assets sowie kleine Miniaturen aller Assets.

   ![DAM-Dateien und -](assets/browse_folder_da2.png "Ordner durchsuchenDAM-Dateien und -Ordner durchsuchen")

1. Um weitere Informationen und eine größere Miniaturansicht eines einzelnen Assets anzuzeigen, klicken Sie auf den Dateinamen.

   ![Anzeigen einer größeren Vorschau eines Assets und](assets/large_preview_actions_da2.png "weiterer AktionenAnzeigen einer größeren Vorschau eines Assets und größerer Aktionen")

1. Klicken Sie auf **[!UICONTROL Open]** oder **[!UICONTROL Edit]** , um die Datei lokal herunterzuladen und sie in der nativen Anwendung anzuzeigen oder zu bearbeiten.
1. Suchen Sie mithilfe von Suchbegriffen nach einem zugehörigen Asset im AEM-Repository. Verwenden Sie `?` und `*` als Platzhalter. Diese Platzhalter ersetzen ein einzelnes oder mehrere Zeichen. Filtern und sortieren Sie die Ergebnisse nach Bedarf.

   ![Beispielsuche mit](assets/search_wildcard_da2.png "einem Sternchen-PlatzhalterBeispielsuche mit einem Sternchen-Platzhalter")

   ![Eine weitere Beispielsuche mit](assets/search_wildcard2_da2.png "Platzhalter mit SternchenEine weitere Beispielsuche mit unterschiedlicher Platzierung des Sternchen-Platzhalters")

>[!NOTE]
>
>Die App zeigt die Assets an, indem sie die Suchkriterien über mehrere Metadatenfelder hinweg und nicht nur den Titel oder Dateinamen des Assets abgleichen.

## Herunterladen von Assets {#download-assets}

Sie können die Assets auf Ihr lokales Dateisystem herunterladen. Die App ruft die Assets vom AEM-Server ab und speichert dieselbe Kopie auf Ihrem lokalen Dateisystem.

Klicken Sie für Optionen auf das Symbol![ ](assets/do-not-localize/more2_da2.png)Mehr Optionen und dann auf das Symbol ![Herunterladen](assets/do-not-localize/download_cloud_da2.png) zum Herunterladen.

![Download-Option für ein](assets/download_option_da2.png "AssetDownload-Option für ein Asset")

>[!NOTE]
>
>Beim Herunterladen oder Hochladen einer oder mehrerer Dateien deaktiviert die Anwendung die Aktionen für Assets und Ordner. Die Aktionen sind verfügbar, wenn der Download oder Upload abgeschlossen ist.

Das Herunterladen mehrerer Assets kann zu einer schlechten Leistung führen, wenn die Warteschlangengröße groß ist oder wenn ein Netzwerkproblem vorliegt. Außerdem können Sie unwissentlich viele Assets zum Herunterladen in eine Warteschlange stellen, wenn Sie einen Ordner herunterladen. Um lange Wartezeiten zu vermeiden, beschränkt die App die Anzahl der Assets, die in einem Schritt heruntergeladen wurden. Informationen zum Konfigurieren finden Sie unter Voreinstellungen [festlegen](install-upgrade.md#set-preferences). Selbst unterhalb dieser Grenze kann die App manchmal nach einer Bestätigung suchen, bevor ein anscheinend großer Ordner heruntergeladen wird.

![App bestätigt Herunterladen relativ vieler](assets/download_confirmation_da2.png "AssetsApp bestätigt Herunterladen relativ vieler Assets")

Wenn Ordner ausgewählt und heruntergeladen werden, lädt die Anwendung nur Assets herunter, die direkt in den Ordnern in AEM gespeichert sind. Assets werden nicht automatisch aus Unterordnern heruntergeladen.

## Öffnen von Assets auf Ihrem Desktop {#openondesktop-v2}

Sie können die Remote-Assets zur Ansicht in der nativen Anwendung öffnen. Die Assets werden in einen lokalen Ordner heruntergeladen und in der mit dem Dateiformat verknüpften nativen Anwendung gestartet. Sie können die native Anwendung ändern, um bestimmte Dateitypen (Erweiterungen) in Ihrem Mac oder Windows zu öffnen.

Klicken Sie **[!UICONTROL Open]** im Asset-Menü auf . Das Asset wird lokal heruntergeladen und in der nativen Anwendung geöffnet. Überprüfen Sie den Downloadstatus und die Übertragungsgeschwindigkeit großer Assets in der Statusleiste.
<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")

-->

>[!NOTE]
>
>Wenn die erwarteten Änderungen nicht in der App übernommen werden, klicken Sie auf das Symbol ![Aktualisieren oder klicken Sie mit der rechten Maustaste auf das Symbol](assets/do-not-localize/refresh.png) Aktualisieren und dann auf **[!UICONTROL Refresh]**. Die Aktionen sind nicht verfügbar, während größere Downloads oder Uploads ausgeführt werden.

Um den lokalen Download-Ordner eines Assets zu öffnen, klicken Sie auf das Symbol![ " ](assets/do-not-localize/more2_da2.png)Mehr Aktionen"und dann auf "Aktion ![zum Anzeigen des Symbols](assets/do-not-localize/reveal_action2_da2.png) " **[!UICONTROL Reveal File]** .

## Verwenden oder Platzieren von Assets in nativen Dokumenten {#place-assets-in-native-documents}

In einigen Fällen, z. B. beim Platzieren eines Assets in einem nativen Dokument, greifen Sie in Windows Explorer oder Mac Finder auf eine Datei zu. Um zum Speicherort der lokal heruntergeladenen Datei im Dateisystem zu gelangen, verwenden Sie die Option ![Symbol](assets/do-not-localize/reveal_action2_da2.png) anzeigen **[!UICONTROL Reveal File]** .

![Aktion "Datei anzeigen"für eine](assets/revealfile_action_da2.png "AssetAktion "Datei anzeigen"für ein Asset")

Klicken Sie auf **[!UICONTROL Reveal File]** oder **[!UICONTROL Reveal Folder]** in einem Ordner, um den Windows Explorer oder den Mac Finder mit der auf Ihrem lokalen Computer vorab ausgewählten Datei- oder Ordnerauswahl zu öffnen. Die Option ist nützlich, um z. B. die AEM-Dateien in den nativen Anwendungen zu platzieren, die das Platzieren oder Verknüpfen lokaler Dateien unterstützen. Informationen zum Platzieren von Dateien in Adobe InDesign finden Sie unter [Platzieren von Grafiken](https://helpx.adobe.com/indesign/using/placing-graphics.html).

Die **[!UICONTROL Reveal File]** Aktion öffnet eine lokale Netzwerkfreigabe, die nur die lokal verfügbaren Assets anzeigt, d. h. Assets, die mit der App veröffentlicht, heruntergeladen oder geöffnet/bearbeitet wurden. Die lokale Netzwerkfreigabe lädt keine Änderungen in AEM hoch. Verwenden Sie zum Hochladen der Änderungen explizit **[!UICONTROL Upload Changes]** oder **[!UICONTROL Upload]** Aktionen in der App.

>[!NOTE]
>
>Zur Abwärtskompatibilität mit der AEM-Desktop-App v1.x werden die angezeigten Dateien von einer lokalen Netzwerkfreigabe bereitgestellt, wobei nur lokal verfügbare Dateien verfügbar sind. Die Desktop-Pfade der angezeigten Dateien sind mit den Pfaden identisch, die von app v1.x erstellt werden.

>[!CAUTION]
>
>Verwenden Sie keine **[!UICONTROL Reveal File]** Option, um Assets in nativen Anwendungen zu bearbeiten. Verwenden Sie stattdessen die **[!UICONTROL Edit]** Aktionen. Weitere Informationen finden Sie unter [Erweiterter Workflow: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten](#adv-workflow-collaborate-avoid-conflicts).

## Bearbeiten von Assets und Hochladen aktualisierter Assets zu AEM {#edit-assets-upload-updated-assets}

Öffnen Sie Assets zur Bearbeitung, wenn Sie Änderungen vornehmen und die aktualisierten Assets auf den AEM-Server hochladen möchten. Um Konflikte mit Bearbeitungen anderer Benutzer zu vermeiden, verwenden Sie die App, um eine Bearbeitungssitzung zu starten. Bevor Sie mit der Bearbeitung beginnen, stellen Sie sicher, dass das Asset kein Sperrsymbol enthält, d. h., dass ein anderer Benutzer das Asset nicht bearbeitet.

Um ein Asset zu bearbeiten, suchen Sie nach dem Asset oder navigieren Sie zum Speicherort des Assets. Klicken Sie auf das Symbol ![Mehr](assets/do-not-localize/more2_da2.png) und dann auf **[!UICONTROL Edit]**.

Verwenden Sie **[!UICONTROL Toggle Check-out]** zum Sperren des Assets, um Konflikte mit Bearbeitungen anderer Benutzer in beiden folgenden Situationen zu vermeiden:

* Sie haben begonnen, ein Asset zu bearbeiten, ohne es vorher auszuchecken (indem Sie es einfach öffnen).
* Sie möchten demnächst mit der Bearbeitung eines Assets beginnen und möchten nicht, dass andere Benutzer es bearbeiten.

Nachdem Sie die Änderungen vorgenommen haben, zeigt die App den **[!UICONTROL Edited Locally]** Status der geänderten Assets an. Alle in den Assets gespeicherten Änderungen sind nur lokal verfügbar, bis Sie die Änderungen in AEM hochladen. Um einzelne Assets oder einige Assets einzeln hochzuladen, klicken Sie in den Optionen für ein Asset **[!UICONTROL Upload Changes]** auf . Es wird eine Version des Assets in AEM erstellt. Über die Weboberfläche von AEM Assets können Sie den Asset-Verlauf in der [Zeitleiste anzeigen](https://helpx.adobe.com/experience-manager/6-5/assets/using/activity-stream.html).

![Option zum Hochladen von Änderungen in der AppOption zum](assets/upload_changes_single1_da2.png "Hochladen von Änderungen in der App")

![Option zum Hochladen von Änderungen beim Anzeigen einer großen Vorschau eines](assets/upload_changes_single2_da2.png "AssetsÄndern Sie beim Hochladen einer großen Vorschau eines Assets")

Bewährte Verfahren zur gemeinsamen Bearbeitung finden Sie unter [Erweiterter Workflow: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten](#adv-workflow-collaborate-avoid-conflicts).

In den folgenden Fällen sollten Sie Ihre Änderungen und Änderungen am lokalen Asset verwerfen. Click **[!UICONTROL Discard Changes]**.

* Wenn Sie Ihre lokalen Änderungen nicht in AEM speichern möchten.
* Nehmen Sie Änderungen am ursprünglichen Asset vor, nachdem Sie einige Änderungen gespeichert haben.
* Beenden Sie die Bearbeitung des Assets, da es nicht mehr benötigt wird.

Schalten Sie ggf. den Checkout um. Das aktualisierte Asset wird aus dem lokalen Cache-Ordner entfernt und erneut heruntergeladen, wenn Sie es bearbeiten oder öffnen.

## Hochladen und Hinzufügen neuer Assets zu AEM {#upload-and-add-new-assets-to-aem}

Benutzer können dem DAM-Repository neue Assets hinzufügen. Sie können z. B. ein Agenturfotograf oder -auftragnehmer sein, der eine große Anzahl von Fotos aus einem Fotoshot zum AEM-Repository hinzufügen möchte. Um AEM neue Inhalte hinzuzufügen, klicken Sie auf das Symbol "In Cloud ![hochladen"](assets/do-not-localize/upload_to_cloud_da2.png) in der oberen Leiste der App. Navigieren Sie zu den Asset-Dateien im lokalen Dateisystem und klicken Sie auf **[!UICONTROL Select]**. Die App startet das Hochladen des Assets und zeigt am unteren Rand eine Fortschrittsleiste an, wenn das Hochladen des Assets länger dauert. Verwenden Sie beim Erstellen oder Hochladen von Ordnern keine Leerzeichen und ungültige Zeichen. Eine Liste der Zeichen finden Sie unter Ordner [erstellen in AEM Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders).

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

Sie können Ordner oder einzelne Dateien aus Ihrem lokalen Dateisystem hochladen. Die Hierarchie eines Ordners wird beim Hochladen beibehalten. Bevor Sie Assets stapelweise hochladen, lesen Sie [Massenhochladen](#bulk-upload-assets).

Um die Liste der in einer bestimmten Sitzung übertragenen Assets anzuzeigen, klicken Sie auf **[!UICONTROL View]** &gt; **[!UICONTROL Assets transfers]**. Mit der Liste können Sie die Dateiübertragungen der aktuellen Sitzung anzeigen und schnell überprüfen.

![Liste der übertragenen Assets in einer bestimmten](assets/assets_transfered_da2.png "SitzungListe der übertragenen Assets in einer bestimmten Sitzung")

>[!NOTE]
>
>Die Übertragungsliste ist nicht beständig und steht nicht zur Verfügung, wenn Sie die App verlassen und erneut öffnen.

>[!NOTE]
>
>Wenn die Dateien nicht hochgeladen werden können und Sie eine Verbindung zu AEM 6.5.1 oder einer späteren Bereitstellung herstellen, finden Sie weitere Informationen zur [Fehlerbehebung](troubleshoot.md#upload-fails).

## Arbeiten mit mehreren Assets {#work-with-multiple-assets}

Benutzer können problemlos mit mehreren Assets arbeiten und diese verwalten, indem sie beispielsweise alle Bearbeitungen in einem Schritt hochladen oder verschachtelte Ordner mit wenigen Klicks hochladen.

### Große Ordner durchsuchen {#browse-large-folders}

Wenn Sie mit Ordnern arbeiten, die viele Assets enthalten, führen Sie einen Bildlauf durch, um weitere Assets anzuzeigen. Um mit der Tastatur zu blättern, drücken Sie einige Male die Tabulatortaste, um das Asset oben auszuwählen. Beachten Sie, dass das hervorgehobene Asset bekannt ist, wann es ausgewählt ist. Verwenden Sie jetzt die Nach-unten-Taste, um durch die Liste der Assets zu navigieren.

### Schnellaktionen für ausgewählte Assets {#quick-actions-for-selected-assets}

Klicken Sie auf die Miniaturansicht einiger Assets, um die Assets auszuwählen. Um alle Assets auszuwählen, aktivieren Sie das Kontrollkästchen in der oberen Leiste der App. Die Aktionen, die für alle ausgewählten Assets gemeinsam gelten, werden in einer Symbolleiste am unteren Rand der App angezeigt.

![Die Symbolleiste am unteren Rand zeigt Aktionen an, die für die ausgewählten](assets/actions_bottom_toolbar1_da2.png "Assets relevant sindDie Symbolleiste am unteren Rand zeigt allgemeine Aktionen für die ausgewählten Assets")

![Keine Aktionen in der Symbolleiste, wenn keine gemeinsamen Aktionen für die](assets/actions_bottom_toolbar2_da2.png "AuswahlKeine Aktionen in der Symbolleiste, wenn keine gemeinsamen Aktionen für die Auswahl")

Die in der Symbolleiste unten verfügbaren Aktionen hängen vom Status der ausgewählten Dateien ab. Wenn Sie beispielsweise nur **[!UICONTROL Edited Locally]** Dateien auswählen, wird das Symbol **[!UICONTROL Upload Changes]** angezeigt. Wenn Sie eine Mischung aus **[!UICONTROL Edited locally]** und **[!UICONTROL Cloud only]** wählen, steht die **[!UICONTROL Upload Changes]** Aktion nicht zur Verfügung.

### Alle bearbeiteten Bilder suchen {#find-all-edited-images}

Die Anwendung bietet eine Ansicht mit der Bezeichnung **[!UICONTROL Edited locally]**, mit der Sie schnell auf alle Dateien zugreifen können, die Sie lokal heruntergeladen haben (über [!UICONTROL Open] oder [!UICONTROL Edit] Aktionen) und die dann geändert wurden. Mit der App können Sie alle lokal bearbeiteten Assets auswählen und die Änderungen mit wenigen Klicks hochladen. In dieser Ansicht werden auch die lokal bearbeiteten Assets angezeigt, die einen Bearbeitungskonflikt haben.

![Filtern, um alle lokal bearbeiteten](assets/edited_locally_filter_da2.png "Assets anzuzeigenFiltern, um alle lokal bearbeiteten Assets anzuzeigen, z. B. beim Massen-Upload von Bearbeitungen")

### Massenupload von Assets {#bulk-upload-assets}

Benutzer oder Organisationen, wie Fotografen oder Kreativagenturen, können in Szenarien zahlreiche lokale Assets erstellen, z. B. Fotoaufnahmen, Retuschieren oder Auswahl aus einem größeren Set, das außerhalb von AEM erstellt wird. Sie können diese großen lokalen Ordner direkt von der Desktop-App in AEM Assets hochladen. Die Ordnerhierarchien bleiben erhalten, und alle verschachtelten Unterordner und eingeschlossenen Assets werden hochgeladen. Die hochgeladenen Assets stehen auch anderen Benutzern desselben Servers sofort zur Verfügung. Assets werden im Hintergrund hochgeladen, sodass der Vorgang nicht an eine Webbrowser-Sitzung gebunden ist.

![Massen-Upload mehrerer lokaler Ordner von Ihrem Desktop in](assets/upload_local_folders_da2.png "AEMBulk Hochladen mehrerer lokaler Ordner von Ihrem Desktop in AEM")

Wenn die erwarteten Änderungen nach dem Hochladen nicht in der App übernommen werden, klicken Sie auf das Symbol " ![Aktualisieren"](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>Verwenden Sie keine Upload-Funktion, um Assets über zwei AEM-Bereitstellungen zu migrieren. Siehe stattdessen auch [Migrationshandbuch](https://helpx.adobe.com/experience-manager/6-5/assets/using/assets-migration-guide.html).

### Liste der übertragenen Vermögenswerte {#list-of-transferred-assets}

Informationen zum Anzeigen der Liste der in einer bestimmten Sitzung übertragenen Assets finden Sie unter [Hochladen von Assets zu AEM](#upload-and-add-new-assets-to-aem).

## Erweiterter Arbeitsablauf: von der AEM Assets-Weboberfläche starten {#adv-workflow-start-from-aem-ui}

Starten Sie bei Bedarf Ihren Workflow über die AEM Assets-Weboberfläche. Die Desktop-App wird mit AEM integriert, um sie bei Bedarf mit Desktop-Aktionen zu übernehmen.

Ein besonderes Beispiel für den Start des Workflows über die Weboberfläche ist die Asset-Suche. Die Omniture Suchleiste in der Benutzeroberfläche "Assets"bietet eine umfassende und erweiterte Sucherfahrung. Möglicherweise möchten Sie zuerst ein gewünschtes Asset im Web suchen und dann den Workflow in der App starten, indem Sie [!UICONTROL Desktop Actions]es verwenden. Einige Beispielfälle umfassen das Filtern von Suchergebnissen mithilfe von Facetten, das Auffinden eines bestimmten von Adobe Stock lizenzierten Assets oder eine von Ihrem Unternehmen implementierte Anpassung, die eine bessere Erkennung über die Weboberfläche ermöglicht.

Die Funktionalität der Desktop-App wird verwendet, wenn Sie die folgenden Aktionen auf der Assets-Weboberfläche durchführen:

* Die [!UICONTROL Desktop Actions] , die [!UICONTROL Open], [!UICONTROL Edit]und [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] oder [!UICONTROL check-in]

Beispielsweise sind die Aktionen auf der Weboberfläche, die für ein Asset verfügbar sind, das in der App ausgecheckt wurde, [!UICONTROL Open], [!UICONTROL Reveal]und [!UICONTROL Check-in].

![Desktop-Aktionen in der AEM-](assets/assets_web_actions_da2.png "WeboberflächeDesktop-Aktionen in der AEM-Weboberfläche")

>[!NOTE]
>
>Der Browser fordert Sie möglicherweise auf, den Start von Adobe Experience Manager Desktop zuzulassen. Um eine unterbrechungsfreie Übertragung vom Browser auf die App zu erhalten, aktivieren Sie das entsprechende Kontrollkästchen, damit die App immer übernommen werden kann.

Folgende Informationen oder Arbeitsabläufe können Sie nicht über die Weboberfläche finden. Verwenden Sie die Desktop-App, da die Weboberfläche lokale Änderungen nicht verfolgt und sich Folgendes nicht bewusst ist:

* Dateien lokal bearbeitet.
* Dateien, die einen Bearbeitungskonflikt haben und diese lösen können.
* Laden Sie lokale Änderungen in AEM hoch.
* Verschiedene Status der lokal verfügbaren Dateien.

Im Gegenteil, Sie können das Asset in der Web-Oberfläche von der Desktop-App aus mit der **[!UICONTROL Open In Web]** Aktion öffnen.

## Erweiterter Arbeitsablauf: Zusammenarbeit an denselben Dateien und Vermeidung von Bearbeitungskonflikten {#adv-workflow-collaborate-avoid-conflicts}

In kollaborativen Umgebungen arbeiten mehrere Benutzer möglicherweise mit demselben Satz von Assets, die zu Versionskonflikten führen können. Um Konflikte zu vermeiden, befolgen Sie folgende bewährte Verfahren:

* Bearbeiten Sie keine Assets, indem Sie auf [!UICONTROL Open]. Bearbeiten Sie die lokal heruntergeladenen Assets nicht, indem Sie sie aus Ihrem Dateisystemordner öffnen. Andere Benutzer wissen nicht, dass das Asset gerade bearbeitet wird.
* Um ein Asset zu bearbeiten, klicken Sie immer auf [!UICONTROL Edit]. Dadurch wird das Asset in der nativen Anwendung geöffnet und dem Asset ein Sperrsymbol hinzugefügt, sodass die anderen Benutzer wissen, dass das Asset bearbeitet wird.
* Klicken Sie auf [!UICONTROL Toggle Check-in] , wenn Sie versehentlich mit der Bearbeitung beginnen, ohne auf [!UICONTROL Edit]. Dadurch wird dem Asset ein Sperrsymbol hinzugefügt. Wenn Sie ein Asset später bearbeiten möchten, es aber nicht bearbeiten möchten, klicken Sie auf , um es zu sperren [!UICONTROL Toggle Check-in] .
* Bevor Sie ein Asset bearbeiten, stellen Sie sicher, dass es von anderen Benutzern nicht bearbeitet wird. Suchen Sie nach dem Sperrsymbol für das Asset.
* Laden Sie nach Abschluss der Änderungen alle Änderungen hoch und checken Sie das Asset ein.

![Status der Bearbeitung von](assets/edits_conflicts_status_da2.png "KonfliktenStatus der Bearbeitung von Konflikten")

Wenn ein lokal heruntergeladenes Asset auf dem AEM-Server aktualisiert wird, zeigt die App einen **[!UICONTROL Modified remotely]** Status an. Sie können entweder Ihre lokale Kopie entfernen oder Ihre lokale Kopie aktualisieren, indem Sie auf [!UICONTROL Remove] bzw. [!UICONTROL Update] klicken. Über Links im Dialogfeld können Sie beide Versionen des Assets anzeigen.

![Optionen zum Beheben des Konflikts, wenn das Asset remote](assets/modified_remotely_dialog_da2.png "modifiziert wirdOptionen zum Beheben des Konflikts beim Remote-Ändern des Assets")

Wenn ein lokal bearbeitetes Asset auch ohne Ihr Wissen auf dem Server aktualisiert wird, zeigt die App einen **[!UICONTROL Editing Conflict]** Status an. Sie können einen Satz der Änderungen beibehalten - entweder Ihre Updates beibehalten (klicken **[!UICONTROL Keep Mine]**) und die Bearbeitung des anderen Benutzers löschen oder die Updates des anderen Benutzers respektieren und Ihre löschen (**[!UICONTROL Overwrite Mine]**).

![Optionen zum Auflösen eines](assets/editing_conflict_dialog_da2.png "BearbeitungskonfliktsOptionen zum Beheben eines Bearbeitungskonflikts")

## Erweiterter Arbeitsablauf: Platzieren und Verknüpfen von Assets in der InDesign-Datei {#adv-workflow-place-assets-indesign}

Wenn Sie mit der AEM-Desktop-App Dateien mit verknüpften Assets öffnen, werden die Assets vorab heruntergeladen und in den nativen Anwendungen abgelegt. Damit dieser Workflow funktioniert, muss Ihre native Anwendung das Platzieren von Links zu lokalen Assets unterstützen und AEM muss die Auflösung dieser Links in den Binärdateien zu serverseitigen Verweisen unterstützen.

Die AEM-Desktop-App unterstützt diesen Workflow mit einigen ausgewählten Adobe Creative Cloud-Desktop-Anwendungen und Dateiformaten - Adobe InDesign, Adobe Illustrator und Adobe Fotoshop. Mit dem Arbeitsablauf können Sie effizient mit den unterstützten Creative Cloud-Dateien arbeiten. Wenn Benutzer A also einige Assets in eine InDesign-Datei platziert und sie in AEM prüft, werden die Assets in der InDesign-Datei von Benutzer B angezeigt, auch wenn die Assets nicht Teil der Datei sind. Die Assets werden lokal auf den Computer des Benutzers B heruntergeladen.

>[!NOTE]
>
>Die Desktop-App kann jedem Laufwerk unter Windows zugeordnet werden. Ändern Sie jedoch nicht den Standardbuchstaben des Laufwerks, wenn Sie einen sanften Vorgang durchführen möchten. Wenn Benutzer derselben Organisation unterschiedliche Laufwerksbuchstaben verwenden, können sie die von anderen platzierten Assets nicht sehen. Die platzierten Assets werden nicht abgerufen, wenn sich der Pfad ändert. Die platzierten Assets bleiben weiterhin in der Binärdatei (z. B. INDD) und werden nicht entfernt.

Informationen zu den Einschränkungen dieses Workflows finden Sie in den [Systemanforderungen und unterstützten Versionen](release-notes.md#system-requirements-and-prerequisites-v2).

Gehen Sie wie folgt vor, um diesen Workflow mit einem Bild-Asset und InDesign auszuprobieren:

1. Halten Sie eine INDD-Datei mit platzierten Assets in AEM praktisch bereit. Informationen zum Erstellen einer solchen INDD-Datei finden Sie unter [Platzierung von Grafiken](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. Von der Desktop-App aus **[!UICONTROL Edit]** die INDD-Datei mit den platzierten Assets in AEM.
1. Die App lädt sowohl die InDesign-Datei als auch die verknüpften Assets herunter. Wenn InDesign das Dokument öffnet, werden die Verknüpfungen aufgelöst, Assets werden heruntergeladen und die Assets werden im InDesign-Dokument angezeigt.
1. Wenn Sie eine neue Grafik in die InDesign-Datei einfügen möchten, verwenden Sie die **[!UICONTROL Reveal File]** Aktion für das Asset. Die Aktion lädt das Asset lokal herunter und öffnet den Speicherort für die lokale Netzwerkfreigabe in Windows Explorer oder Mac Finder.
1. Platzieren Sie das angezeigte Asset im InDesign-Dokument. Dadurch wird eine Verknüpfung im Dokument erstellt.
1. Nachdem Sie die Änderungen im InDesign-Dokument abgeschlossen haben, speichern Sie es und laden Sie es mit der Desktop-App auf AEM hoch.

## Erweiterter Arbeitsablauf: Assets lokal herunterladen {#adv-workflow-download-assets-locally}

Die App lädt die Assets vom AEM-Server in vielen Szenarien lokal auf Ihr Dateisystem herunter. Die Downloads verbrauchen Bandbreite und Speicherplatz. Wenn Sie die Szenarien kennen, können Sie die Wartezeit optimieren, bis die Downloads abgeschlossen sind.

Sie laden die Assets von der App auf Abruf herunter. Siehe [Herunterladen von Assets](#download-assets).

Wenn Sie mit der [!UICONTROL Open] Aktion ein Asset in einer nativen Desktop-Anwendung öffnen, wird das Asset lokal heruntergeladen, wenn es nicht bereits lokal verfügbar ist. Siehe [Öffnen von Assets](#openondesktop-v2).

Wenn Sie den Speicherort eines Assets oder Ordners in der App anzeigen, wird das Asset oder der Ordner zunächst lokal heruntergeladen und dann auf Ihrem Computer in der lokalen Netzwerkfreigabe geöffnet. Siehe [Öffnen von Assets](#openondesktop-v2).

Wenn Sie die [!UICONTROL Edit] Aktion zum Bearbeiten eines Assets in einer nativen Desktopanwendung verwenden, wird das Asset lokal heruntergeladen, wenn es nicht bereits lokal verfügbar ist. Siehe [Bearbeiten von Assets und Hochladen aktualisierter Assets in AEM](#edit-assets-upload-updated-assets).

Wenn die App installiert ist und darf, werden die Aktionen ausgeführt, wenn Sie sie über [!UICONTROL Desktop Actions] die AEM-Weboberfläche verwenden. Die App lädt das Asset zuerst herunter und schließt dann die Aktion ab.