# Einleitung

Willkommen bei *The Rust Programming Language*, einer Einführung in Rust.

Rust ist eine Programmiersprache, die Ihnen hilft, schnellere und
zuverlässigere Software zu schreiben. Hohe Ergonomie und niedrige Kontrolle
stehen bei der Gestaltung der Programmiersprache oft im Widerspruch zueinander;
Rust stellt dies auf die Probe. Durch das Abstimmen leistungsstarker
technischer Kapazitäten und einer großartigen Entwicklererfahrung gibt Ihnen
Rust die Möglichkeit, Low-Level-Details (wie z. B. Speicherverbrauch) zu
kontrollieren, ohne den ganzen Aufwand, der traditionell mit einer solchen
Steuerung verbunden ist.

## Für wen ist Rust?

Rost ist für viele Menschen aus verschiedenen Gründen großartig. Lassen Sie uns
einige der wichtigsten Gruppen aufzählen.

### Entwicklerteams

Rust erweist sich als produktives Werkzeug für die Zusammenarbeit zwischen
großen Entwicklerteams mit unterschiedlichen Programmierkenntnissen.
Low-Level-Code ist anfällig für eine Vielzahl von subtilen Fehlern, die in den
meisten anderen Sprachen nur durch umfangreiche Tests und sorgfältige
Codeüberprüfung durch erfahrene Entwickler aufgefangen werden können. In Rust
spielt der Compiler eine Rolle als Gatekeeper, indem er sich weigert, Code mit
solchen Bugs zu kompilieren - einschließlich Concurrency-Bugs. Durch die
Zusammenarbeit mit dem Compiler kann sich das Team mehr auf die Logik des
Programms konzentrieren als auf die Fehlersuche.

Rust bringt auch moderne Entwicklerwerkzeuge in die Welt der
Systemprogrammierung:

* Cargo, der mitgelieferte Dependency Manager und Build-Tool, macht das
  Hinzufügen, Kompilieren und Verwalten von Abhängigkeiten im gesamten
  Rust-Ökosystem schmerzlos und konsistent.
* Rustfmt sorgt für einen einheitlichen, entwicklerübergreifenden
  Programmierstil.
* Der Rust Language Server unterstützt die IDE-Integration für die
  Code-Vervollständigung und Inline-Fehlermeldungen.

Durch den Einsatz dieser und anderer Tools im Rust-Ökosystem können Entwickler
beim Schreiben von Code auf Systemebene produktiv sein.

### Studenten

Rust ist für Studenten und Leute, die sich für Systemkonzepte interessieren.
Viele Menschen haben über Themen wie die Entwicklung von Betriebssystemen
durch Rust gelernt. Die Community beantwortet gerne Fragen von Studenten.
Durch Bemühungen wie dieses Buch wollen die Rust-Teams Systemkonzepte für
mehr Menschen zugänglich machen, insbesondere für diejenigen, die mit dem
Programmieren grade erst anfangen.

### Unternehmen

Rust wird in der Produktion von Hunderten von Unternehmen, großen und
kleinen, für eine Vielzahl von Aufgaben eingesetzt; Kommandozeilen-Tools,
Web-Services, DevOps-Tooling, Embedded-Geräte, Audio-und Video-Analyse und
Transcoding, Krypto-Währungen, Bioinformatik, Suchmaschinen,
Internet-of-things-Anwendungen, maschinelles Lernen, und sogar große Teile
des Firefox-Web-Browsers.

### Open Source Entwickler

Rust ist für Leute, die die Rust Programmiersprache, Community,
Entwicklertools und Bibliotheken erstellen wollen. Wir würden uns freuen,
wenn Sie zur Rust beitragen wollen.

### Menschen, die Geschwindigkeit und Stabilität schätzen

Unter Geschwindigkeit verstehen wir sowohl die Geschwindigkeit der Programme,
die Sie mit Rust erstellen können, als auch die Geschwindigkeit, mit der Sie
sie mit Rust schreiben können. Die Kontrollen des Rust Compilers gewährleisten
Stabilität während Funktionserweiterungen und Refactoring, im Gegensatz zu
brüchigem Legacy-Code in Sprachen ohne diese Prüfungen, die von den Entwicklern
nicht verändert werden können. Durch das Streben nach kostenfreien
Abstraktionen, d.h. Funktionen auf höherer Ebene, die so schnell wie manuell
geschriebener Code kompilieren, versucht Rust, sicheren Code auch zu schnellem
Code zu machen.

Dies ist keine vollständige Liste aller, die die Rust zu unterstützen hofft,
aber dies sind einige der größten Akteure. Insgesamt ist Rusts größtes Ziel,
Kompromisse einzugehen, die von den Programmierern seit Jahrzehnten akzeptiert
werden, und die Dichotomie zu beseitigen. Sicherheit *und* Produktivität.
Geschwindigkeit *und* Ergonomie. Probieren Sie Rust, und überzeugen Sie sich
selbst.

## Für wen dieses Buch ist

Dieses Buch geht davon aus, dass Sie bereits Software in einer anderen
Programmiersprache geschrieben haben, macht aber keine Annahmen darüber,
welche. Wir haben versucht, das Material für alle zugänglich zu machen, die
aus den verschiedensten Bereichen der Programmierung kommen. Wir vergeuden
nicht viel Zeit damit, darüber zu sprechen, was Programmierung *ist* oder wie
man darüber nachdenkt; jemand, der neu im Programmieren ist, sollte besser
ein Buch lesen, das speziell eine Einführung in die Programmierung bietet.

## Wie man dieses Buch benutzt
Dieses Buch geht im Allgemeinen davon aus, dass Sie es von vorne nach hinten
lesen, das heißt, dass spätere Kapitel auf den Konzepten früherer Kapitel
aufbauen, und frühere Kapitel möglicherweise nicht in Details zu einem Thema
eingehen und das Thema erst in einem späteren Kapitel wieder aufgreifen.

Es gibt zwei Arten von Kapiteln in diesem Buch: Konzeptkapitel und
Projektkapitel. In den Konzeptkapiteln lernen Sie einen Aspekt von Rust
kennen. In den Projektkapiteln werden wir gemeinsam kleine Programme
erstellen und das bisher Gelernte anwenden. Die Kapitel 2, 12 und 20 sind
Projektkapitel, der Rest sind Konzeptkapitel.

Zusätzlich ist Kapitel 2 eine praktische Einführung in Rust als Sprache.
Wir werden Konzepte auf hohem Niveau behandeln und in späteren Kapiteln
detailliert darauf eingehen. Wenn Sie sich sofort die Hände schmutzig machen
wollen, ist Kapitel 2 das Richtige für Sie. für das. Zuerst möchten Sie
vielleicht sogar Kapitel 3 überspringen, in dem es um Rust geht. Funktionen,
die denen anderer Programmiersprachen ähneln, und gehen Sie direkt zu Kapitel
4, um mehr über Rust's Eigentumssystem zu erfahren. Wie auch immer, wenn Sie
ein besonders akribischer Lerner, der es vorzieht, jedes Detail zu lernen
bevor er sich bewegt. auf das nächste, sollten Sie vielleicht Kapitel 2
überspringen und direkt zu Kapitel 3 übergehen, zurück zu Kapitel 2, wenn Sie
an einem Projekt arbeiten möchten, bei dem diese Details.

Zusätzlich ist Kapitel 2 eine praktische Einführung in die Sprache Rust. Wir
werden Konzepte erst auf hohem Niveau, und in späteren Kapiteln werden
zusätzliche Detail einführen. Wenn Sie sich sofort die Hände schmutzig machen
wollen, ist Kapitel 2 das Richtige für Sie. Am Anfang möchten Sie vielleicht
sogar Kapitel 3 überspringen, in dem es um Rust-Features, geht die denen
anderer Programmiersprachen ähneln, und direkt zu Kapitel 4 gehen, um mehr über
Rusts Besitztums-System zu erfahren. Falls Sie aber ein besonders akribischer
Lerner sind, der es vorzieht, jedes Detail zu lernen, bevor er weiter macht,
sollten Sie vielleicht Kapitel 2 überspringen und direkt zu Kapitel 3 gehen,
und dann zurück zu Kapitel 2 kommen, wenn Sie an einem Projekt arbeiten, bei
dem Sie diese Details anwenden möchten.

Kapitel 5 behandelt Strukturen und Methoden, und Kapitel 6 behandelt Enums,
`match`-Ausdrücke und das `if let` Kontrollfluss-Konstrukt. Sie können
Strukturen und Enums benutzen, um benutzerdefinierte Typen in Rust zu erstellen.

In Kapitel 7 erfahren Sie mehr über Rusts Modulsystem und die
Privatsphäre-Regeln. zur Organisation Ihres Codes und seiner öffentlichen
Programmierschnittstelle (API). Kapitel 8 bespricht einige gemeinsame
Datenstrukturen, die die Standard-Bibliothek bietet, wie z. B. Vektoren, Strings
und Hash-Maps. Kapitel 9 erforscht Rust's Fehlerbehandlungsphilosophie und
-techniken.

Kapitel 10 behandelt generische Datentypen, Traits und Lifetimes, die Ihnen die
Möglichkeit geben, Code zu definieren, der für mehrere Datentypen gilt. In
Kapitel 11 geht es um das Testen, das auch bei den Sicherheitsgarantien von Rust
noch notwendig ist, um die Logik ihres Programms zu prüfen. In Kapitel 12 bauen
wir unsere eigene Implementierung einer Teilmenge der Funktionalität des
`grep`-Kommandozeilen-Tools, das nach für Text in Dateien sucht. Dazu werden wir
viele der Konzepte verwenden, die wir in die vorigen Kapitel gesehen haben.

Kapitel 13 befasst sich mit Closures und Iteratoren: Eigenschaften von Rust,
die aus funktionalen Programmiersprachen kommen. In Kapitel 14 untersuchen wir
Cargo mehr in Tiefe und sprechen über Best Practices für den Austausch Ihrer
Bibliotheken mit anderen. Kapitel 15 beschreibt die Smart-Pointer, die die
Standardbibliothek bietet, und die Eigenschaften, die ihre Funktionalität
ermöglichen.

In Kapitel 16 werden wir durch verschiedene Modelle der nebenläufigen
Programmierung gehen und darüber sprechen, wie Rust hilft, ohne Furcht mit
mehreren Threads zu programmieren. Kapitel 17 befasst sich mit dem Vergleich von
Rust und Prinzipien objektorientierter Programmierung, die Sie vielleicht kennen.

Kapitel 18 ist eine Referenz über Patterns und Pattern-Matching, die mächtige
Möglichkeiten sind, Ideen in allen Rust-Programmen auszudrücken. Kapitel 19
enthält eine ein Sammelsurium von fortgeschrittenen Themen von Interesse,
einschließlich unsicherem Rust und mehr über Lifetimes, Traits, Datentypen,
Funktionen und Closures.

In Kapitel 20 werden wir ein Projekt durchführen, in dem wir einen Low-Level,
multithreaded Webserver bauen!

Schließlich enthalten einige Anhänge nützliche Informationen über die Sprache
in einem mehr referenzähnlichen Format. Anhang A enthält die Schlüsselwörter
von Rust. Anhang B deckt Rusts Operatoren und Symbole ab. Anhang C enthält
ableitbare Traits die von der Standardbibliothek zur Verfügung gestellt werden.
Anhang D enthält Makros.

Es gibt keinen falschen Weg, dieses Buch zu lesen: Wenn Sie etwas überspringen
wollen, tun Sie es! Möglicherweise müssen Sie dann zu früheren Kapiteln
zurückspringen, wenn es zu verwirrend wird. Lesen Sie so, wie Sie zurechtkommen.

Ein wichtiger Teil des Lernprozesses von Rust ist das Lesens von Fehlermeldungen,
die der Compiler anzeigt: diese leiten Sie zu funktionierendem Code. Daher werden
wir viele Beispiele für Code zeigen, der nicht kompilieren lässt, zusammen mit den
Fehlermeldungen, die der Compiler Ihnen in dieser Situation anzeigt. Seien Sich
sich dessen bewusst, wenn Sie ein zufälliges Beispiel eingeben und ausführen – es
könnte sein, dass es sich nicht kompilieren lässt! Lesen Sie den umgebenden Text,
um zu sehen, ob das Beispiel, das Sie kompilieren wollen, dazu gedacht ist Fehler
zu erzeugen. In den meisten Fällen führen wir Sie später auch zur richtigen
Version des Codes, der nicht kompiliert werden kann.

## Quellen

Die Quelldateien aus denen dieses Buch generiert wird, befinden sich auf [GitHub][book-de].

Die englischsprachigen Originaldateien befinden sich ebenfalls auf [GitHub][book].

[book-de]: https://github.com/zgtm/book/tree/master/second-edition/src
[book]: https://github.com/rust-lang/book/tree/master/second-edition/src
