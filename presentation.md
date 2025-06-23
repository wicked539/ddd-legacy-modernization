# Legacy-Modernisierung mit DDD und Event-Storming

# Übersicht
* Motivation
  * Definition Legacy-Software
  * Warum DDD?
  * Stakeholder überzeugen
* Big-Picture-Event-Storming
  * Einführung Event-Storming
  * Durchführung Workshops
* Umsetzung
  * Strategie
  * Pitfalls

# Motivation - Warum DDD für Legacy-Modernisierung?
## Legacy-Software
* Gewachsene Software-Systeme sind oft Big Balls of Mud und (wenn überhaupt) technisch geschnitten
* In den 00er-Jahren entstandene Software:
  * Lastenheft, Pflichtenheft, Architekt im Elfenbeinturm, UML, Wasserfall
  * technischer Schnitt (Server-Team, DB-Entwickler, Web-Team)
  * Proprietäre Technologien, große Datenbanken (inkl. Logik), Vertikale Skalierung
* Schlechte Wartbarkeit:
  * ...durch starren Entwicklungsprozess, der kaum Feedback zulässt
  * ...durch technische System-Schnitte, da Features immer Änderungen in mehreren Schichten / Teams bedingen
* Fachexperten und Entwickler wechseln, mehr und mehr Lösungen werden an der Architektur vorbei gebaut
* Wartbarkeit nimmt weiter ab
* Big Ball of Mud entsteht
## Warum DDD?
* Oftmals keine Original-Entwickler _und_ keine Fachexperten mehr da
  * Fachlichkeit _und_ Code wird von Menschen maintained, die bei der Entstehung nicht dabei waren
* Gemeinsames Domain-Wissen und Ziel-Architektur notwendig!
## Management überzeugen
* Weniger Wartungsaufwand
* Schnellere Feature-Entwicklung
* Moderner Technik-Stack besser verkäuflich
* Klare Domänen-Schnitte ermöglichen...
  * fundierte Make-or-Buy-Entscheidungen
  * gezielten Resourcen-Einsatz am Kern der Wertschöpfungskette
## Entwickler überzeugen
* Technische Schulden abbauen
* Legacy-Tech-Stack loswerden
* Kollaboratives Software-Design sorgt für...
  * _unfassbar viel_ mehr Spaß, Software zu entwickeln, wenn Entwicklung und Fachbereich das gleiche Verständis von der Domain haben
  * keinen Frust beim rumwursteln in Alt-Code, den keiner kapiert
## Fachexperten überzeugen
* Herausfordernd, aber essentiel
* Fachexperten lernen...
  * wie moderne Software-Entwicklung funkiontiert
  * wie sie unmittelbar Einfluss auf das entstehende Software-System nehmen können
 
# Big Picture Event Storming
## Domain Driven Design
* Fachlichkeit soll Treiber von Software-Design und Architektur sein
* Create collaboration of software experts and domain experts
* Domain-Driven Design is an approach to the development of complex software in which we:
  * Focus on the core domain.
  * Explore models in a creative collaboration of domain practitioners and software practitioners.
  * Speak a ubiquitous language within an explicitly bounded context.
## Event Storming
* Leichtgewichtige Methode zum Modellieren von Geschäftsprozessen
* Sehr inklusiv: Menschen aus allen Bereichen der Organisation können gemeinsam einen ersten Entwurf für die Architektur eines Software-Systems gestalten
* Bonus: Auch sehr gut geeignet, um ein gemeinsames Verständnis der Abläufe in einem bestehenden System (oder auch Geschäftsprozess!) zu erarbeiten
* Lebende Dokumentation, die nie fertig ist: muss agil und iterativ enstehen!
## Vorbereitung Workshop-Serie
### Teilnehmer
* Optimal ca. 10-15 Personen
* Idealerweise mindestens 50% Fachexperten!
### Zeitplanung
* 5 Halbtages-Sessions für große Software-Systeme
* Mehrere Tage Pause zwischen den Sessions!
* Möglichst alle Termine im Vorfeld planen
### Location
* Mindestens 5m, besser 10m breite Wand
* Notfalls Whiteboards zusammenstellen
### Material
* Großem Rolle Plotterpapier als modeling canvas
* Super Sticky Post-Its (Viel Orange, Pink, Blau, Grün, ...)
* Stabilo Pen 68 (schwarz)
* Krepp-Band
## Erste Session
* Ankommen & kurze (!) Einführung in die Methode
* Chaotic Exploration
* Duplikate auflösen
  * Vokabular festlegen
  * Domain-Objekten definieren
* Enforcing the timeline
* Happy Path zuerst modelieren
* Hotspots
  * Am Ende der Session festlegen, wer das Thema zur Klärung mitnimmt 
## Zweite session
* Happy Path nochmals von Anfang bis Ende erzählen
* External Systems
* Commands & Actors
* Pivotal Events
* Kandidaten für Bounded Contexts
  * Events aus dem Unhappy Path ebenfalls zuordnen!
## Dritte Session
* Kandidaten für Bounded Contexts in Kleingruppen schärfen
* Edge-Cases integrieren
* Kommunikationsbeziehungen zwischen Bounded Contexts betrachten
* Context Canvases ausfüllen
## Vierte Session
* Context Canvases abschliessen
  * Detaillierte Beschreibungen der einzelnen Bounded Contexts
* Context Map finalisieren
## Fünfte Session
* Bei Bedarf: Restarbeiten vom Big Picture Event Storming
* Umsetzungs-Strategie erarbeiten

# Umsetzung
## Leitplanken
* Grundlegende Architekturmuster
* Technologie-Empfehlungen
* Design-Level-Event-Storming-Sessions für Software-Design einzelner Bounded Contexts
  * Ein halber Tag reicht in der Regel aus
* Architecture Decision Records
## Proof of Concept
* Kleiner Ausschnitt der Context Map (2-3 Bounded Contexts) als PoC umsetzen
* Nicht zu komplex, aber auch nicht trivial!
## Umsetzungs-Strategie
* Big-Bang-Neuentwicklung
* Iterative Ablösung
## Core Domain Chart
* Bounded Contexts bewerten 
* Roadmap für die Umsetzung
  * Reihenfolge abhängig von Strategie:
    * MVP für auslieferbares Gesamtsystem _oder_
    * Risiko-Minimierung bei schrittweiser Ablösung
## Iterative Ablösung
* Anti-Corruption-Layer/Adapter-Ring um neue Services herum bauen
* Frühzeitig und kontinuierlich in Produktion ausliefern
## Team-Zusammenstellung / Skalierung
* Empfehlung: 50% Entwickler aus Alt-System, 50% Experten für neuen Technik-Stack
* Langsam skalieren, max. ein neues Team pro Quartal
* Outsourcing (mindestens von Core Domain) vermeiden

# Pitfalls
## Zu viele Entwickler / zu wenige Fachexperten im Event-Storming
* "Internen Projektleiter" finden, der gut in der Organisation vernetzt ist
* 1-2 Fachexperten können ausreichen, wenn sie als Multiplikator agieren
## "Modellieren wir jetzt das Alt-System oder etwas Neues?"
* Wir modellieren zunächst (noch) garkein System, sondern erschaffen ein gemeinsames Verständnis für unsere Geschäftsprozesse!
* Möglichst von Technik lösen
## Outsourcing
* Saubere Bounded Context-Beschreibungen können Manager verleiten, diese als komplette Arbeitspakete extern zu vergeben
* Standard-Software für Generic Domain ist völlig in Ordnung
* Wenn externe Entwicklungs-Teams eingesetzt werden: Zusammenarbeit an Supporting Domain erproben
* Zur Not: Laufen lassen. Wahrscheinlich merkt das Management nach ein paar Monaten, dass die Idee nicht besonders gut war.
