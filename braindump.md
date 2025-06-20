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

# motivation
## warum ddd für legacy-modernisierung? 
### gewachsene software-systeme sind oft big ball of mud und (wenn überhaupt) technisch geschnitten
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
### oftmals keine original-entwickler _und_ keine fachexperten mehr da
#### fachlichkeit _und_ code wird von menschen maintained, die bei der entstehung nicht dabei waren
### gemeinsames domain-wissen und ziel-architektur notwendig!
## management überzeugen
### TODO
## entwickler überzeugen
### TOOD

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
## erste session
### domain events
### duplicates
### enforcing the timeline
* hotspots
* definition von domain-objekten
## zweite session
### happy path
* external systems
### pivotal events
## dritte session
### kandiaten für bounded contexts in kleingruppen schärfen
### edge-cases integrieren
## vierte session
### context canvases ausfüllen
### kommunikationsbeziehungen herausarbeiten
## fünfte session
### context map finalisieren
### umsetzungsstrategie

# umsetzung
## poc, kleiner ausschnitt der context map (2-3 contexts) umsetzen
## core domain chart!
## strategie
### komplette neuentwicklung vs. schrittweise ablösung altsystem

# pitfalls
## zu viele entwickler / zu wenige fachexperten im eventstorming
## "modelieren wir jetzt das alt-system oder etwas neues?"
## zu gute context-beschreibungen -> management freut sich und versucht near-shoring
