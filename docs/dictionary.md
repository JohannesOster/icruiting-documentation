# Begriffsdefinitionen

## Allgemein

**Tenant:** Die oberste Ordnungsinstanz, welche mehrere Nutzer\*innen zusammenfasst und somit als digitale Repräsentation von einer Organisation, einem Team, etiner Abteilung, etc. dient.

**Stelle:** Eine Offene Position in Ihrere Organisation.

**Anforderungsprofil:** Ein Satz an Kriterien (=Anforderungskriterien) einer Stelle auf welche ein\*eine Bewerber\*in untersucht werden soll.

## Formulare

Ein Formular ist eindeutig einer _Stelle_ zugeordnet und ist aus einer der folgenden drei Kategorien:\
**Formularkategorie:** _Bewerbung_, _Screening_, _Assessment_, _Onboarding_

**Bewerbungs-Formular:** Ein Formular über welches sich Bewerber\*innen für eine Stelle bewerben. Eine _Stelle_ hat genau ein _Bewerbungs-Formular_.\
**Screening-Formular:** Ein Formular über welches Bewertungen zu Bewerbungsunterlagen abgegeben werden. Eine _Stelle_ hat genau ein _Screening-Formular_.\
**Assessment-Formular:** Ein Formular über welches Bewertungen zu Übungungen eines Assessments abgegeben werden. Eine _Stelle_ hat ein oder mehere _Assessment-Formulare_.
**Onboarding-Formular:** Ein Formular über welches Bewertungen zu Übungungen während dem Onboarding abgegeben werden. Eine _Stelle_ hat ein oder mehere _Onboarding-Formulare_.

**Formularfeld:** Ein einzelnes Feld eines Formulars. **Achtung:** Nicht nur Eingabefelder sondern auch statische Felder wie zum Beispiel ein _Section Header_ werden als _Formularfeld_ bezeichnet.

**Formularfeld-Absicht:** Eine aus drei Möglichkeiten der Auswertung: _count distinct_, _aggregate_, _sum up_ \
**count distinct:** In der Auswertung wird gezählt wie oft jeder mögliche Wert vorkommt. (z.B. Ich will diesen\*diese Bewerber\*in besprechen: Ja: 3, Nein: 2)\
**aggregate:** In der Auswertung werden die Werte aller Formulareintragsfelder, welche dieses Formularfeld referenzieren aneinander gereiht. (z.B. Anmerkungen)\
**sum up:** In der Auswertung werden die Werte alle Formulareintragsfelder, welche dieses Formularfeld referenzieren mathematisch ausgewertet berechnet.

## Formulareintrag

**Formulareintrag:** Füllen Sie ein Formular aus und senden es ab, so wird die Zusammenfassung aller Eingabewerte als _Formulareintrag_ bezeichnet.\
**Formulareintragsfeld:** Ein einzelnes Feld aus einem _Formulareintrag_. Ein _Formulareintragsfeld_ ist eindeutig einem _Formularfeld_ zugeordnet.

## Auswertung

Der Zentrale Begriff der Auswertung ist der _Score_. Er tritt auf verschiedenen Ebenen auf und spiegelt entweder eine Summe oder einen Durchschnitt wieder. Um zu erkennen auf was er sich bezieht wird er mit einem entsprechenden Präfix versehen:

### Ranking

**Formulareintrag-Score:** Man betrachte die Felder (=_Formulareintragsfelder_) von einem Formulareintrag und zwar nur die, deren referenziertes _Formularfeld_ die _Formularfeld-Absicht_ "_sum up_" trägt. Berechnet man die Summe der Werten dieser _Formulareintragsfelder_ ensteht der _Formulareintrag-Score_.

**Formular-Score:** Man betrachte alle _Formulareintrag-Score_, welche sich auf ein bestimmtes Formular beziehen. Davon betrachte man nur jene Einträge, die sich auf einen\*eine bestimmten\*bestimmten Bewerber\*in beziehen. Bildet man nun den Durchschnitt aller dieser Einträge erhält man den _Formular-Score_. (="Wie wurde ein\*eine Bewerber\*in durchschnittlich mit einem bestimmten Formular bewertet")

**Formularkategorie-Score:** Man betrachte alle Formulare einer Kategorie (Screening, Assessment) sowie einen\*eine bestimmen\*bestimmte Bewerber\*in. Der Durchschnitt aller _Formular-Scores_ von diesem\*dieser Bewerber\*in wird _Formularkategorie-Score_ genannt. (="Wir wurde ein\*eine Bewerber\*in in einer Kategorie bewertet")

### Bewerber\*innengutachten

Ein Gutachten bezieht sich auf einen\*eine Bewerber\*in sowie eine _Formularkategorie_ und gibt einen Überblick über die allgemeine Bewertung des\*der Bewerber\*in.
Im folgenden werden wichtige Begriffe erläutert:

#### Formularkategorie

**Formularkategorie-Score:** Siehe [Ranking](#ranking)

#### Formular

**Formular-Score:** Siehe [Ranking](#ranking)

**StdDev-Formular-Score:** Man betrachte ein bestimmtes Formular und berechne alle [_Formulareintrags-Scores_](#ranking) für einen\*eine Bewerber\*in. Die Standardabweichung von diesem Datensatz wird _StdDev-Formular-Score_ genannt. (="Wie stark schwanken die Bewertungen in dieser Übung")

#### Formularfeld

**Formularfeld-Score:** Man betrachte die Werte aller _Formulareintragsfelder_ zu einer bestimmten Bewerber\*in sowie zu einem bestimmten Feld. Berechnet man davon den Durchschnitt erhält man den _Formularfeld-Score_. (="Wie wurde dieser\*diese Bewerber\*in bei diesem Feld bewertet")

**StdDev-Formularfeld-Score:** Man betrachte die Werte aller _Formulareintragsfelder_ zu einer bestimmten Bewerber\*in sowie zu einem bestimmten Feld. Berechnet man davon die Standardabweichung erhält man den _StdDev-Formularfeld-Score_. (="Wie stark schwanken die Bewertungen in dieser Frage für diesen\*diese Bewerber\*in")

#### Anforderungskriterien

**Anforderungskriterium-Score:** Man betrachte alle Formularfelder, die auf ein bestimmtes Anforderungskriterium abziehlen und sich auf einen\*eine bestimmeten\*bestimmte Bewerber\*in. Berechnet man nun den Durchschnitt der dazugehörigen _Formulareintragsfeld-Scores_ erhält man den _Anforderungskriterium-Score_. (="Wie wurden ein\*eine Bewerber\*in in diesem Kriterium berwertet")
