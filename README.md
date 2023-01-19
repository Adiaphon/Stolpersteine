# M.A. Multimedia und Autorschaft

Dies ist das Repository für die [Website](https://mmautor.net/?ref=https://github.com/soerenengels/mmautor.net) des Master-Studiengangs **Multimedia und Autorschaft**. Die Website ist mit _Jekyll_ gebaut und wird mit _Git_ verwaltet.

Die nachfolgende **Dokumentation** soll folgenden Generationen bei der Pflege und Weiterentwicklung der Website des Studiengangs Multimedia & Autorschaft helfen.

----

## Schnellstart

Der Schnellstart soll es dir unmittelbar ermöglichen an der Website zu arbeiten.

1. Installiere dafür Jekyll auf deinem Rechner entsprechend eines der [folgenden Guides](https://jekyllrb.com/docs/installation/). (Möglicherweise musst du zunächst die Vorraussetzungen entsprechend des Guides installieren.)

2. Klone das git-Repository mit Hilfe von Git:

```bash
git clone https://github.com/soerenengels/mmautor.net.git
```

3. Starte die lokale Entwicklungsumgebung:

```bash
bundle exec jekyll serve
```

----

## Was ist eigentlich ... ?

### Was ist Jekyll?

Die Website ist mit Hilfe von [Jekyll](https://jekyllrb.com/), einem Static-Site-Generator, gebaut. Das lässt sich ungefähr so vorstellen, wie ein _Brotbackautomat_, auch wenn ich noch nie einen benutzt habe. Du gibst verschiedene Zutaten hinein, nimmst Einstellungen vor, drückst Start und am Ende hast du ein fertiges Brot. Entsprechend erstellt _Jekyll_ auf Basis verschiedener Einzelteile und (Markdown-)Dokumente eine entsprechende Ordnerstruktur mit HTML-, CSS- und JS-Dateien. Fertig ist die Website.

### Was ist Git?

Git ist ein digitales Versionierungssystem, was es ermöglicht zu mehrt dezentral in einem Ordner zu arbeiten, ohne sich ständig Dateien mit Versions- oder Datumsnummern hin und her zu schicken.

- Wie kann ich die Website bearbeiten?
Es gibt einen übergreifenden Punkt, an dem der aktuelle Stand gespeichert wird. Diesen ziehst du dir zu Beginn deiner Arbeit herunter. (git clone ...) Jetzt kannst du den Stand lokal bearbeiten, parallel zu einem:einer Kommiliton:in. 
- Wie füge ich Änderungen hinzu?

#### Arbeitsverzeichnis erstmalig herunterladen

```bash
git clone https://github.com/soerenengels/mmautor.net.git
```

#### Arbeitsverzeichnis updaten

```bash
git pull
```

#### Arbeitsverzeichnis hochladen

```bash
git add .
git pull
git commit -m "Textnachricht, die die Veränderungen beschreibt"
git push
```

### Was ist Markdown?

Markdown ist eine Auszeichnungssprache, ähnlich wie HTML nur simpler und text-bezogener. Hier findest du einen [kurzen Guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) und ein [kurzes Tutorial](https://www.markdowntutorial.com/).

----

## Einrichten

1. Installiere Jekyll auf deinem Rechner entsprechend eines der [folgenden Guides](https://jekyllrb.com/docs/installation/).
2. Klone das git-Repository mit Hilfe von ``` git clone https://github.com/soerenengels/mmautor.net.git ```
3. Starte

## Struktur

Das Repository bzw. der Ordner mit den Dateien für die Website hat eine Struktur, die sich teilweise aus Vorgaben _Jekylls_ heraus ergeben, teilweise selbst gewählt sind. Der nachfolgende Abschnitt soll die Struktur erklären.

## _data

Im Ordner *_data* liegen Daten(-strukturen), die möglicherweise auf mehreren Unterseiten wiederverwendet werden können. Zum Zeitpunkt der Erstellung der vorliegenden Dokumentation (Frühjahr 2021) ist der Ordner wiefolgt angelegt:

- _/instructors/_  
ist akuell ein leerer Ordner, der zukünftig für Daten zu Mitarbeitenden des Studiengangs denkbar wäre.
- _/students/_  
ist der Ordner, an dem die Daten zu den Studierenden gesammelt werden. Jeder Jahrgang erhält eine Datei, die nach dem Eintrittsjahr benannt ist (YYYY.yml). Die Struktur der Datei wir an späterer Stelle erläutert.
Insbesondere die Über-uns- und die Alumni-Seite greifen auf diese Daten zurück.
- */advisory_board.yml*  
Hier sind alle Daten zum Advisory Board enthalten. Aktuell greift die Über-uns-Seite darauf zurück.
- cooperations.yml  
Hier sind alle Daten zu medialen, akademischen oder strategischen Kooperationspartner:innen enthalten.
- social.yml  
Hier sind alle Daten zu Social-Media-Accounts des _MMA_ enthalten.

Wichtig ist, dass die Struktur (der Einrückungen) in _.yml_-Dateien eingehalten wird.

### advisory_board.yml

In der Datei *advisory_board.yml* ist das Advisory Board schmatisch abgebildet. 

Jede Organisation beginnt mit einem Bindestrich. Die dazugehörigen Daten (_organization_, _url_, _image_ und _member_) werden eingerückt. Der Punkt _member_ hat wieder mit Bindestrich eingrückte Unterpunkte für die entsprechende(n) Person(en).

Der Punkt _image_ verweist auf den _/assets/images/_-Ordner, welcher dem angegeben Pfad vorangestellt wird. Es bietet sich ein transparentes Logo als _.png_-Datei an.

```yaml
- organization: Name der Organisation
  url: https://www.url-der-organisation.de/
  image: advisory-board/name-der-organisation.png
  member:
    - name: Titel & Name der stellvertretenden Person
    - name: Titel & Name der stellvertretenden Person
```

Die Daten des Advisory Boards sind aktuell auf der Über-uns-Seite eingebettet.

### cooperations.yml

In der Datei _cooperations.yml_ werden Kooperationspartner:innen festgehalten.

```yaml
partner:
- name: Name des Unternehmens
  image: cooperations/aussagekraftiger-name.jpg # Pfad zur Bilddatei im assets/images/-Ordner
  url: https://www.mmautor.de/ # Url zur jeweiligen Website
- ...
```

Die Daten der Kooperationspartner:innen sind aktuell auf der Über-uns-Seite eingebettet.

### social.yml

In der Datei _social.yml_ werden Verweise zu Social-Media-Seiten festgehalten. Sie dienen auch als Grundlage für die Social-Media-Icons im _header_-Bereich der Seite.

Jeder Verweis auf einen Social-Media-Account beginnt mit einem Bindestrich und einem _slug_ (z.B. "twitter"). Darunter folgen entsprechend eingerückt die dazugehörigen Daten (_name_, _handle_, _url_, _icon_ und _hidden_).

```yaml
- tiktok:
  name: TikTok
  handle: "@mmautor"
  url: https://website.com
  icon: icon-name.png
  hidden: true
- ...
```

### students/YYYY.yml

In der Datei _YYYY.yml_ werden alle Studierenden festgehalten. Ein Jahrgang beginnt einmalig mit der Immatrikulations-Jahreszahl als _key_. Für jede:n Student:in wir ein Objekt mit Hilfe eines Bindestriches angelegt. Eingerückt ist verpflichtend der _key_ **name**.

Optional können weitere Merkmale angegeben werden. Unter dem _key_ **image** wird ein Pfad innerhalb des _assets/images/_-Ordner angegeben. 

Unter dem _key_ **references** können Links zu Portfolios, Projekten oder Social-Media-Accounts angegeben werden. Für jede Seite Bedarf es eines eigenen Objektes mit Hilfe eines Bindestriches. Obligatorisch bei Angaben zu Referenzen sind die _keys_ **handle** und **url**.

```yaml
year: "2019"
description: "Der Jahrgang 2019 hatte die Schwerpunkte Recherche & Diversität."
students:
- name: Vorname Nachname
  image: students/2021/vorname-nachname.png
  references:
    - website:
      url: https://website.de/
      handle: "Website"
    - instagram:
      url: https://www.instagram.com/name/
      handle: Instagram
- ...
```

## _includes

Der Ordner *_includes* enthält Bestandteile, auf die Layouts zurückgreifen können. Sie können auf verschiedenen Unterseiten wiederverwendet werden. Möchtest du einen spezifischen Teil der Website ändern, z.B. für die Suchmaschinenoptimierung oder die Fußzeile, so kannst du das zentral an einer Stelle tun. Der Ordner enthält aktuell folgende Dateien:

- _header.html_  
beinhaltet den Kopfbereich der Website mit Logo, Sprachsiwtcher und (mobiles Burgermenü-Icon).
- _navigation.html_  
beinhaltet das Menü mit allen Menüpunkten und wird von _header.html_ abgerufen
- _footer.html_  
beinhaltet den Fußbereich der Website mit Links u.a. zu Datenschutz und Impressum.
- _head.html_  
beinhaltet den `<head>`-Bereich der html-Dokumente
- _head-seo.html_  
beinhaltet die Grundlagen für Metadaten zur Suchmaschinenoptimierung und wird von _head.html_ abgerufen.

## _layouts

Der Ordner *_layouts* enthält verschiedene Layout-/Template-Dateien, die mit den Inhaltsdokumenten durch einen Eintrag im _Frontmatter_ verknüpft sind. Die Angabe

```yaml
---
layout: home
---
```

in der Datei _./index.md_ gibt an, dass dieser Inhalt mit der Layout-Datei home.html verknüft werden soll.
Da fast jede Seite eine eigene Collage aufweist, hat nahezu jede Seite eine eigene Layout-Datei im *_layouts*-Ordner.

Es gibt drei Seiten, die etwas aus der Logik herausstechen. Das sind folgende Dateien:

- _base.html_  
Hierbei handelt es sich um ein generelles Grundgerüst aller Seiten, auf das alle anderen Layouts zurückgreifen.
- _default.html_  
Sofern kein anderes _layout:_ im FrontMatter angegeben ist, wird auf das _default_-Layout zurückgegriffen.
- _project.html_  
Hiebei handelt es sich um das Layout der Projektseiten des Showrooms. Sie zeigen keine Collagen im Teaser-Bereich, sondern das jeweilige Projektbild.

### Collagen

Die Collagen sind _image_-Elemente mittels _svg_-Element kombiniert und von einem _figure_-Element mit der Klasse _collage_ umgeben.  

Die _svg_-Viewbox ist mit 1200x1200 Punkten bezeichnet. Im _defs > style_-Bereich sind Gestaltungsanweisungen für _:hover_-Effekte angegeben.

Darunter werden die einzelnen Elemente der Collage entweder mit reinen _image_-Elementen (für statische Bilder ohne Verweise) oder mit zusätzlich umgebenen _a_-Elementen (für dynamische Bilder mit _:hover_-Effekt) ausgezeichnet.

Die x- und y-Koordinaten werden jeweils von der oberen linken Ecke aus betrachtet.

## _site

Beim ersten Herunterladen, ist dieser Ordner noch nicht vorhanden, denn der Ordner *_site* entsteht erst im Rahmen des _build_-Prozesses von Jekyll. Um die Website aus den verschiedenen Einzelteilen zusammenzusetzen, musst du _Jekyll_ sagen, dass die Website gebaut werden soll.

```bash
bundle exec jekyll build
```

Dieser Ordner ist es auch, der nach dem _build_-Prozess als zip-Ordner an den zuständigen technischen Mitarbeiter des Instituts geht, damit dieser ihn dann auf den entsprechenden Uniserver hochladen kann.

## assets/

In diesem Ordner werden Bilder, Stylesheets und Skripte hinterlegt.

### images/

Struktur des images-Ordner. Verweis auf *_config.yml* **imageurl:**

### css/

Die CSS-Datei _style.css_ ist für die Gestaltung der Website zuständig.

### js/

Allgemeine Bemerkungen

#### script.js

Menü

#### showroom.js

showroom.js-Bemerkungen

#### splide.min.js

Für das Karussel wurde [Splide.js](https://splidejs.com/) ([Github](https://github.com/Splidejs/splide)) verwendet.

## _posts/

In diesem Ordner liegen die Projekte. Beim Anlegen von Projekten sollte auf die Komprimierung der Projektbilder geachtet werden.

## Englischsprachige Übersetzung

In dem Ordner _en/_ liegen die Dateien für die englischsprachige Übersetzung der Website. Fügst du eine deutschsprachige Seite hinzu oder änderst du sie, mache dir Gedanken machen, ob diese Änderung auch auf der englischsprachigen Seite reflektiert werden sollte.

## Nutzungsszenarien

Wir haben uns verschiedene Szenarien überlegt, wie du zukünftig die Seite womöglich bearbeiten möchtest.

### Ich möchte einen neuen Jahrgang hinzufügen.

Um einen neuen Jahrgang hinzuzufügen, musst du im Ordner */_data/students/* eine neue yml-Datei mit dem entsprechenden Namen anlegen (z.B. _2021.yml_).

Füge nun Einträge entsprechend der Struktur (siehe oben) hinzu oder kopiere einen bestehenden Jahrgang und passe die Felder entsprechend an.

Bilder des neuen Jahrgangs können (mit der entsprechenden Angabe) theoretisch überall liegen, folgen aber idealerweise der bestehenden Ordnerstruktur und kommen in */assets/images/students/* und dann einen Ordner mit der entsprechenden Jahreszahl.
_data/students.yml

### Ich möchte einen neuen Social-Media-Account hinzufügen.

_TikTok_ ist im Mainstream angekommen und der MMA möchte auch darauf stattfinden? Dann verändere die Datei */_data/social.yml* entsprechend.

### Neue Hauptseite anlegen

/*

### Neue:n Projektpartner:in hinzufügen

_data/cooperations.yml
assets/images/cooperations/
Bildoptimierung: Größenverhältnis, Komprimierung (z.B. mit ImageOptim)

### Ich möchte ändern, welches Projekt im Showroom hervorgehoben wird.

Alle Projekte (bzw. deren deutschsprachige Beschreibung) liegen im Ordner */_posts/*. Wenn sie im _Frontmatter_ der jeweiligen Datei mit "highlight: true" gekennzeichnet sind, werden sie im Teaserbereich des Showcase in der Slideshow angezeigt.

Das Bild.
Die Logline.

### Ein:e Student:in möchte ein Portfolio, ein Projekt oder einen Social-Media-Account zum Alumniverzeichnis hinzufügen

_data/students.yml

### Ich möchte Informationen, die die Bewerbung betreffen, ändern.

Die entsprechende Datei dafür ist _/bewerbung.md_.

### _config.yml

----

## Zusatzinfos

### .htaccess

Was ist die .htaccess-Datei? Die .htaccess-Datei liegt auf dem Webserver und lässt sich wie eine Rufumleitung oder ein Nachsendeantrag verstehen. Änderst du deine Telefonnummer oder deine Adresse möchtest du in der Regel weiterhin erreichbar sein. Dafür erstellst eine Rufumleitung, die den Anruf auf deine alte Nummer an deine neue Nummer weiterleitet.

Auf die Website übertragen, brauchst du eine _Rufumleitung_, wenn Seiten umziehen (also sich ihre URL ändert). Man spricht von einer 301-Weiterleitung, wenn eine Seite dauerhaft umgezogen ist. Sie sorgt dafür, dass Nutzer:innen bei einer Änderung der URL-Struktur nicht ins Leere geleitet werden, sondern weiterhin zu ihrem Ziel finden.

Da der Jahrgang 2019-2021 nicht nur visuell, sondern auch inhaltlich und konzeptionell die MMA-Website bearbeitet hat, waren auch Weiterleitungen zumindest von den relevantesten Links nötig, auf die von externen Seiten verwiesen wurde. Diese finden sich u.a. in der _.htaccess_-Datei

### 404.html

Hin und wieder kommt es mal zu Fehlern. Beispielsweise, wenn sich ein:e Nutzer:in in der Adresszeile vertippt hat oder sich ein Fehler in einen Link eingeschlichen hat. Es lassen sich einfach nicht alle Fehler ausschließen. Daher benötigt es eine Fehlerseite. Man spricht von einer 404-Fehlerseite, da eine nicht gefundene Seite mit dem Fehlercode 404 beschrieben wird.

Die Fehlerseite der MMA-Website findet sich im Hauptverzeichnis als _/404.md_. Sie wird auch in der _.htaccess_-Datei referenziert.

### Favicon

Ein Favicon ist eine simple Grafik, für gewöhnlich das Logo. Sie wird z.B. als Tab-Icon im Browser angezeigt oder als Kachel beim Speichern der Website auf dem Homescreen. Daher wird diese Grafik in vielen verschiedenen Formaten benötigt, da viele Geräte oder Systeme eigene Anforderungen daran richten.

Für die MMA-Seite haben wir die entsprechenden Icons mit Hilfe von [Real Favicon Generator](https://realfavicongenerator.net/) erstellt. Das Tool erstellt einerseits einen Ordner mit Grafikdateien und andererseits die entsprechenden _meta_-Tags für den _head_-Bereich im _HTML_-Code.

Die Grafikdateien haben wir aktuell in das Hautpverzeichnis gelegt. Perspektivisch ließe sich auch ein Bereich im _/assets/images/_-Ordner vorstellen. Den _HTML_-Code haben wir in die Datei */_include/head.html* kopiert. Dadurch wird er auf allen Unterseiten verfügbar

### .gitignore

Die Date _.gitignore_ dient _Git_ dazu, bestimmte Seiten oder Ordner aus der Versionierung auszuschließen. Aktuell werden vorallem Cache-Dateien und der *_site*-Ordner ausgeschlossen, da diese für die Versionierung überflüssig sind.

### robots.txt

Die Datei _robots.txt_ gibt Suchmaschinen bzw. deren Programmen, die das Web durchsuchen an, welche Teile der Website sie indexieren sollen/dürfen und welche nicht.

Aktuell ist für die MMA-Website hier keine besondere Angabe gemacht. Es wird lediglich auf die Sitemap verwiesen.

### sitemap.xml

Eine Sitemap ist eine Form der Darstellung der Webseitenstruktur. Sie ist insbesondere für Suchmaschinen da, um die Website besser _crawlen_ zu können. Sie wird automatisch von dem Plugin [jekyll-sitemap]() beim _build_-Prozess generiert, welches bei der bundle-Installation mit installiert wird. Daher ist sie nur im *_site*-Ordner zu finden.

### Gemfile

Die Datei _Gemfile_ (als auch Gemfile.lock) gehören zu _Jekyll_ bzw. _Ruby_, der Sprache, in der _Jekyll_ geschrieben ist. Sie gibt an, welche _Jekyll_-Version verwendet werden soll und beinhaltet Verweise auf die installierten Plugins.

## To Do

### perspektivisch
- Sitemap an englischsprachige Seiten anpassen
