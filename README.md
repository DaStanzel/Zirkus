# Übung

Als Softwareentwickler betreuen Sie den Zirkus GNIE. Dieser möchte ein umfangreiches Softwaresystem zur Verwaltung der Aufführungen des Zirkus

Erstellen Sie eine JEE-Anwendung mit REST-Endpoints und JPA-Persistierung mit folgenden Tabellen:

- Show: Datum und Uhrzeit des Beginns der Show, Titel der Show (zB Abendvorstellung)
- Program: Show, Act
- Act 
- ActMember: name zB "Lustiger Lukas", "Wendiger Walter"
- Actor (Künstler, erbt von ActMember)
- Animal (Tier, erbt von ActMember)

Eine Aufführung (Show) findet an gewissen Tagen statt. 
Program ist die n:m - Auflösung zwischen Show und Act.
Bei jeder Show gibt es sogenannte Acts (zB Löwenbändiger, Trapezvorführung, Clown, Elefantenshow usw.)
Jeder Act hat einen oder mehrere Künstler und keine, eine oder mehrere Tiere.

Ein Act weiß, welche Members er hat, Jeder Member kann nur in einem Act mitmachen und weiß in welchem Act er mitmacht.

## Aufgabenstellung:

a. Erstellen Sie die Entitäten und Fassaden für JPA. Wählen Sie notwendige Attribute, aber nicht zu viele.

b. Befüllen Sie das System mit Daten

c. Erstellen Sie eine REST-Endpoint mit 

  - allen Shows und dem dazugehörigen Acts `zirkus/rs/show`
  - Erstellen von Shows (Zuordnung von Acts zu Shows mit der Entität Program) `zirkus/rs/show`
  - Ändern von Act `zirkus/rs/act`
  - Löschen aller ActMember mit Namen "Lustiger Lukas": `zirkus/rs/act/member?name="Lustiger Lukas"`
  
  
  __Sie können mit dem Programm "Postman" Ihre REST-Endpoints testen. Ergänzen Sie den Progammcode der Endpoints mit den korrekten URL und (falls notwendig) dem jeweiligen Body__
    
d. Generieren Sie ein Klassendiagramm und speichern sie es als CLD.png in das root Ihres Projektes

e. Generieren Sie ein Entity-Relationship-Diagram und speichern sie es als ERD.png in das root Ihres Projektes

f. ZUSATZPUNKTE: Testen Sie mit JUnit, ob die CRUD-Funktionalität für eine bidirektionale Beziehung korrekt funktioniert