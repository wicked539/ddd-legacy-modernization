# motivation
## warum ddd für legacy-modernisierung? 
### gewachsene software-systeme sind entweder big ball of mud und (wenn überhaupt) technisch geschnitten
* In den 00er-Jahren entstandene Software:
** Pflichtenheft, Lastenheft, Architekt im Elfenbeinturm, UML, Wasserfall, technischer Schnitt (Server-Team, DB-Entwickler, Web-Team)
### oftmals keine original-entwickler _und_ keine fachexperten mehr da
#### fachlichkeit _und_ code wird von menschen maintained, die bei der entstehung nicht dabei waren
### gemeinsames domain-wissen und ziel-architektur notwendig!
## management überzeugen
### TODO
## entwickler überzeugen
### TOOD

# big picture event storming
## einführung methode
## vorbereitung
### zielgruppe motivieren, optimale personenanzahl, geeignete location
## erste session
### domain events
### duplicates
### enforcing the timeline
## zweite session
### happy path
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
