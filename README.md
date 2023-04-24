# Stolpersteine - Filme gegen das Vergessen
# Unterseite: Ein weißer Fleck

Dies ist das Repository für die [Website](https://stolpersteine.medienkomm.uni-halle.de) des Projekts **Stolpersteine - Filme gegen das Vergessen**. Die Website ist mit _Bootstrap_ gebaut und wird mit _Git_ verwaltet. Diese Abgabe bezieht sich auf die Unterseite "ein weißer fleck.html", die als Vorschlag für die Unterseiten der weiteren Filme der Stolperstein-Reihe gelten soll. 

Die Anlehnung an das gemeinsam erarbeitete Design auf Basis des Bootstrap-Themes "Grayscale" wurde hier mit Farben aus dem Design-Team angereichert und dem favorisierten Favicon der Studierenden (Entworfen von Hannah). Die Website wurde für responsiv angelegt und ist damit auf mobile Darstellung optimiert.

Die nachfolgende **Dokumentation** soll folgenden Generationen bei der Pflege und Weiterentwicklung der Website helfen.

Um die Website zu verwenden, laden Sie einfach die Dateien in einen Webserver und navigieren Sie zu index.html. Die Website ist responsiv und sollte auf verschiedenen Geräten gut funktionieren.
Technologien

Die Website wurde mit HTML, CSS und JavaScript erstellt. Es wurden auch Bootstrap und Font Awesome verwendet, um das Design und einige Funktionalitäten zu implementieren. Das Video wurde auf YouTube hochgeladen und dann in die Website eingebettet.
Autoren

Zum Einfügen neuer Inhalte: 

# neuer Titel:

einfügen im <!-- Masthead-->
<div class="text-center">
  <h1 class="mx-auto mt-10 mb-60" >HIER TITEL IN VERSALIEN EINFÜGEN</h1>  
  <h2 class="mx-auto mt-20">hier Autor*innen: von ... und ....</h2> 
  <h2 class="mx-auto">Erscheinungsjahr | DAUER in Min.</h2> 
</div>


# Eingebettetes Video

einfügen in <!-- Einbettung -->
<div class="row align-items-start">
  <div class="col-md-6 col-12">
      <div class="youtube-video-container">
        <iframe width="560" height="315" src="HIER YOUTUBE EMBED-LINK EINFÜGEN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
   </div>
        <div class="col-md-6 col-12">
           <h4> HIER BESCHREIBUNG AUS STOLPERSTEIN-PAPER (oder YT-Video).</h4>
         </div>
    </div>

----

## Schnellstart

Der Schnellstart soll es dir unmittelbar ermöglichen an der Website zu arbeiten.

1. Installiere dafür Bootstarp auf deinem Rechner entsprechend eines der [folgenden Guides](hhttps://getbootstrap.com/). (Möglicherweise musst du zunächst die Vorraussetzungen entsprechend des Guides installieren.)

2. Klone das git-Repository mit Hilfe von Git:

```bash
git clone https://
```

3. Starte die lokale Entwicklungsumgebung:

```bash
bundle exec xxxxx serve
```

----

## Was ist eigentlich ... ?

### Was ist Bootstrap?

Die Website ist mit Hilfe von [Bootstrap](https://getbootstrap.com/), einem Static-Site-Generator, gebaut. Das lässt sich ungefähr so vorstellen, wie ein _Brotbackautomat_, auch wenn ich noch nie einen benutzt habe. Du gibst verschiedene Zutaten hinein, nimmst Einstellungen vor, drückst Start und am Ende hast du ein fertiges Brot. Entsprechend erstellt Bootstrap auf Basis verschiedener Einzelteile und (Markdown-)Dokumente eine entsprechende Ordnerstruktur mit HTML-, CSS- und JS-Dateien. Fertig ist die Website.

### Was ist Git?

Git ist ein digitales Versionierungssystem, was es ermöglicht zu mehrt dezentral in einem Ordner zu arbeiten, ohne sich ständig Dateien mit Versions- oder Datumsnummern hin und her zu schicken.

- Wie kann ich die Website bearbeiten?
Es gibt einen übergreifenden Punkt, an dem der aktuelle Stand gespeichert wird. Diesen ziehst du dir zu Beginn deiner Arbeit herunter. (git clone ...) Jetzt kannst du den Stand lokal bearbeiten, parallel zu einem:einer Kommiliton:in. 
- Wie füge ich Änderungen hinzu?

#### Arbeitsverzeichnis erstmalig herunterladen

```bash
git clone https://github.com/adiphon
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


Diese Website wurde von Mathis Schneider erstellt.