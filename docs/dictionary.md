# Begriffsdefinitionen

## Allgemein

**Tenant:** Die oberste Ordnungsinstanz, welche mehrere Nutzer\*innen zusammenfasst und somit als digitale Repräsentation von einer Organisation, einem Team, etiner Abteilung, etc. dient.

**Stelle:** Eine Offene Position in Ihrere Organisation.

**Anforderungsprofil:** Ein Satz an Kriterien (=Anforderungskriterien) einer Stelle auf welche ein\*eine Kanditat\*in untersucht werden soll.

## Formulare

Ein Formular ist eindeutig einer _Stelle_ zugeordnet und ist aus einer der folgenden drei Kategorien:\
**Formularkategorie:** _Bewerbung_, _Screening_, _Assessment_

**Bewerbungsformular:** Ein Formular über welches sich Kandidat\*innen für eine Stelle bewerben. Eine _Stelle_ hat genau ein _Bewerbungsformular_.\
**Screeningformular:** Ein Formular über welches Bewertungen zu Bewerbungsunterlagen abgegeben werden. Eine _Stelle_ hat genau ein _Screeningformular_.\
**Assessmentformular:** Ein Formular über welches Bewertungen zu Übungungen eines Assessment Centers abgegeben werden. Eine _Stelle_ hat ein oder mehere _Assessmentformulare_.

**Formularfeld:** Ein einzelnes Feld eines Formulars. **Achtung:** Nicht nur Eingabefelder sondern auch statische Felder wie zum Beispiel ein _Section Header_ werden als _Formularfeld_ bezeichnet.

**Formulareintrag:** Füllen Sie ein Formular aus und senden es ab, so wird die Zusammenfassung aller Eingabewerte als _Formulareintrag_ bezeichnet.\
**Formulareintragsfeld:** Ein einzelnes Feld aus einem _Formulareintrag_. Ein _Formulareintragsfeld_ ist eindeutig einem _Formularfeld_ zugeordnet.

**Formularfeld-Absicht:** Eine aus drei Möglichkeiten der Auswertung: _count distinct_, _aggregate_, _sum up_\
**count distinct:** In der Auswertung wird gezählt wie oft jeder mögliche Wert vorkommt. (z.B. Ich will diesen\*diese Kandidat\*in besprechen)\
**aggregate:** In der Auswertung werden die Werte aller Formulareintragsfelder, welche dieses Formularfeld referenzieren aneinander gereiht. (z.B. Anmerkungen)\
**sum up:** In der Auswertung werden die Werte alle Formulareintragsfelder, welche dieses Formularfeld referenzieren summiert und/oder deren Durchschnitt berechnet.

### Auswertung

Der Zentrale Begriff der Auswertung ist der _Score_. Er tritt auf verschiedenen Ebenen auf und spiegelt entweder eine Summe oder einen Durchschnitt wieder. Um zu erkennen auf was er sich bezieht wird er mit einem entsprechenden Präfix versehen:

**Formulareintrag-Score:** Man betrachte die Felder (=_Formulareintragsfelder_) von einem Formulareintrag und zwar nur die, deren referenziertes _Formularfeld_ die _Formularfeld-Absicht_ "_sum up_" trägt. Berechnet man die Summe der Werten dieser _Formulareintragsfelder_ ensteht der _Formulareintrag-Score_.

**Formular-Score:** Man betrachte alle _Formulareintrag-Score_, welche sich auf ein bestimmtes Formular beziehen. Davon betrachte man nur jene Einträge, die sich auf einen\*eine bestimmten\*bestimmten Kandidat\*in beziehen. Bildet man nun den Durchschnitt aller dieser Einträge erhält man den _Formular-Score_. (="Wie wurde ein\*eine Kandidat\*in durchschnittlich mit einem bestimmten Formular bewertet")

**Average-Formular-Score:** Man betrachte ein bestimmtes Formular und berechne den _Formular-Score_ für alle Kanditat\*innen. Der Durchschnitt dieser _Forumlar-Scores_ wird _Average-Formular-Score_. (="Wie wurden Kandidat\*innen durschnittlich mit diesem Formular bewertet.")

**Formularkategorie-Score:** Man Betrachte alle Formulare einer Kategorie (Screening, Assessment) sowie einen\*eine bestimmen\*bestimmte Kandidat\*in. Der Durchschnitt aller _Formular-Scores_ von diesem\*dieser Kandidat\*in wird _Formularkategorie-Score_ genannt. (="Wir wurde ein\*eine Kandida\*in in einer Kategorie bewertet)
