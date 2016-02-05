# Podlove Publisher

## Voraussetzungen

* Du hast ein leeres Wordpress
* Du kannst in deinem Wordpress Plugins installieren
* Du hast schon deine erste Episode aufgenommen
* Grundlegende Wordpress Kenntnisse

## Installation der Plugins

Klicke auf "Plugins" und dann auf "Installieren"

![Plugins installieren](install_plugins.png)

Dann trägst du in die Suche `podlove` ein und installierst die folgenden Plugins:

* Podlove Podcast Publisher
* Shownotes
* Podlove Subscribe Button

Bitte nach der Installation die Plugins noch nicht aktivieren sondern einfach
nur auf "Zurück zur Plugin-Installation" klicken.

![Plugins suchen](search_plugins.png)

![Plugin installieren](install_subscribe_button.png)

Wenn du die Installation abgeschlossen hast, klickst du auf "Installierte Plugins"
um dir die installierten Plugins anzeigen zu lassen.

![Installierte Plugins](installed_plugins_link.png)

Die Liste der installierten Plugins sollte nun etwa so aussehen:

![Installierte Plugins](installed_plugins.png)

Hier können wir nun die Plugins aktivieren. Markiere dazu die 3 Plugins mit einem
Haken. Wähle anschließend aus dem Drop-Down Menü `Aktivieren` aus.

![Plugins aktivieren](activate_plugins.png)

Danach klickst du auf `Übernehmen`.

## Einen Podcast anlegen

### Grundeinstellungen

Wir beginnen mit den `Podcast Settings`. Klicke dazu im Podlove Menü auf der
linken Seite auf den Unterpunkt `Podcast Settings`

![Podlove Settings Menu](podcast_settings_menu.png)

Unter "Description" trägst du alle wichtigen Daten zu deinem Podcast ein.

![Podlove Podcast Description](podcast_settings_description.png)

Nachdem du alles eingetragen hast, klickst du auf `Änderungen übernehmen`.

### Die Media URL

Unter `Media` trägst du die URL ein, unter der deine Podcasts hochgeladen werden.
Wenn du [Podseed](https://podseed.org/) benutzt, lautet diese `http://cdn.podseed.org/deinpodcast/`
beziehungsweise `https://cdn.podseed.org/deinpodcast` solltest du deine Seite mit HTTPS ausliefern.

![Podlove Media URL](podcast_mediaurl.png)

Auch hier bestätigst du deine Änderungen mit `Änderungen übernehmen`.

### Lizenz

Unter `License` kannst du nun eine Lizenz für deinen Podcast anlegen.
Die [Creative Commons Webseite](https://creativecommons.org/choose/) kann dir bei
der Auswahl deiner Lizenz helfen.

![Podlove License](podcast_license.png)

`Änderungen übernehmen` und weiter gehts!

### Formate hinzufügen

In den `Episode Assets` sind die Formate definiert, in denen deine Podcasts
ausgeliefert werden. Du brauchst mindestens eines davon.

Zum Anlegen eines Formates klickst du auf `Episode Assets` im `Podlove` Menü auf
der linken Seite.

![Podlove Episode Assets](podlove_episode_assets.png)

Zum Hinzufügen eines Formates klickst du auf `Add new`

![Asset Add New](asset_add_new.png)

Wähle als "Asset Type" `audio` für ein Audioformat aus. Als "File Format" nimmst du
`MP3 Audio (mp3)`

![Episode Assets MP3](episode_assets_mp3.png)

Speichere nun deine Änderungen mit `Änderungen übernehmen`.

Dieses kannst du anschließend mit allen Audioformaten wiederholen die du deinen
Hörern anbieten willst.

![Assets complete](asset_complete.png)

### Feeds hinzufügen

Ganz wichtig: Feeds. Du solltest für jedes Format in dem dein Podcast veröffentlicht
wird einen Feed anbieten.

Damit sind wir am nächsten Menüpunkt des `Podlove` Menüs angelangt: `Podcast Feeds`

![Podcast Feeds](podcast_feeds.png)

Um einen Feed hinzuzufügen klickst du auf `Add new`.

![Feeds Add New](feeds_add_new.png)

Bei "Episode Media File" wählst du nun dein vorhin angelegtes Format aus, wahrscheinlich
`MP3 Audio`. Als "Feed Name" solltest du auch das Audio Format angeben.

Durch anhaken von "Append Feed Name to Podcast Title" wird automatisch dein Podcast-Name
in den Feed-Titel eingefügt.

Bei "Slug" solltest du den URL Part für den Feed eintragen, meistens reicht `mp3`.

"Discoverable" sorgt dafür, daß der Feed in den Meta-Tags deiner Webseite verlinkt wird.

Durch das Auswählen von "Include HTML Content" werden auch die Shownotes in deinem
Feed sichtbar und können so von Podcast Clients wie [Podcat](http://www.podc.at) angezeigt werden.

Das ganze sollte dann etwa so aussehen:

![Podcast Feed Details](podcast_feed.png)

Wieder die `Änderungen übernehmen` und das ganze für alle in den Assets angelegten Formaten wiederholen.

## Shownotes einbinden

Die [Shownotes](http://shownot.es) erlauben Hörern und Podcastern bei Livesendungen
oder nachträglich Sendungsnotizen mit Zeitstempeln zu erstellen.

### Shownotes Plugin konfigurieren

Zuerst mußt du das Shownotes Plugin konfigurieren. Klicke dazu auf `Einstellungen`
und dann auf `Shownotes`

![Shownotes Settings](shownotes_settings.png)

Dort änderst du den "Tag Mode" auf `use all items except items with the following tags`

![Shownotes Tag Mode](shownotes_tag_mode.png)

Danach speicherst du deine Änderungen mit `Änderungen übernehmen`

### Shownotes in Podlove Template einbinden

Damit die Shownotes auch unter jedem Podcast eingebettet werden, kannst du jetzt
das Standard Podlove Template anpassen.

Dazu klickst du jetzt im `Podlove` Menü auf `Templates`

![Podlove Templates](podlove_templates.png)

Im "default" Template fügst du eine neue Zeile mit dem Inhalt `[shownotes]` hinter
dem letzten `{% endif %}` ein. Damit werden jetzt deine Shownotes unter dem Mediaplayer
angezeigt.

![Shownotes in Podlove Template](podlove_template_with_shownotes.png)

**Wichtig**: Jede Änderung in dem Template muß mit dem `Save` Knopf rechts oben
gespeichert werden. Erst danach kann man die Änderungen übernehmen.

Normalerweise werden Mediaplayer, Downloadbuttons und Shownotes über deinem zur
Episode verfassten Text angezeigt. Möchtest du das ändern und deinen Text dem
Mediaplayer voranstellen mußt du die Templateeinbindung so ändern, daß das "default"
Template unten eingefügt wird.

Dazu wählst du bei "Insert at top" `Don't insert automatically`aus und bei
"Insert at bottom" `default`

![Template Bottom](template_bottom.png)

Wie immer die Änderungen mit `Änderungen übernehmen` übernehmen.
(_Hast du vorher dein Template gespeichert?_)

## Podlove Subscribe Button einbinden

Podlove bietet einen "Abonnieren" Button für verschiedene Clients. Diesen kannst
du komfortabel in der Widgetleiste von Wordpress einbinden.

Klicke hierzu auf "Design" und dann auf das `Widgets` Menü.

![Design Widgets](design_widgets.png)

Jetzt kannst du den "Podcast Subscribe Button" in die Widget-Leiste ziehen und
einen Stil auswählen.

![Subscribe button](subscribe_button.png)

Nur noch `Speichern` und der Subscribe Button wird in deiner Seitenleiste angezeigt.

## Die erste Episode

Bist du soweit? Dann kannst du jetzt deine erste Episode veröffentlichen.

_Zuerst mußt du deine Mediendateien hochladen._

Klicke auf "Episodes" und dann auf `Add new`.

![New Episode](episodes_add_new.png)

Du fängst am besten mit dem "Podcast Episode" Feld an. Trage als erstes den Dateinamen
der Episode in das Feld "Episode Media File Slug" ein. Danach sollten die Formate
in den Media Files auftauchen.

![Episode Media Slug](episode_media_slug.png)

Anschließend kannst du die Metadaten der Podcast Episode eintragen.

![Episode Meta Data](episode_meta.png)

Ganz unten kannst du die Shownotes im OSF Format einfügen. Das OSF Format wird
[hier](https://github.com/shownotesArchive/OSF-in-a-Nutshell/blob/master/OSF-in-a-Nutshell.de.md)
erklärt.

Jetzt noch den Titel der Episode ergänzen und ein paar einleitende Worte schreiben.

![Episode Text](episode_text.png)

Alles erledigt? Dann kannst du auf `Veröffentlichen` klicken und deine erste
Podcastfolge veröffentlichen.

## Dokumentenlizenz
Dieses Dokument steht unter [Creative Commons BY-NC-SA 4.0](http://creativecommons.org/licenses/by-nc-sa/4.0/)

2016-02-06 Falk Stern <falk@fourecks.de> [https://podseed.org](https://podseed.org)
