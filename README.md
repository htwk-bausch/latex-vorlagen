# Vorlagen für studentische Arbeiten

In diesem Repo finden Sie Vorlagen zur Erstellung von Dokumenten in LaTeX. Folgende Vorlagen stehen zur Auswahl:

- `report/report.tex`: Vorlage für Belegarbeiten und Projektdokumentationen
- `thesis/thesis.tex`: Vorlage für eine Abschlussarbeit (Bachelor- oder Masterarbeit) (@ToDo)

Im Ordner `common/` befinden sich Dateien, die gemeinsam genutzt werden sowohl für `report.tex` als auch `thesis.tex`. Die Datei `htwk.sty` enthält alle Zusatzpakete sowie die entpsrechenden Einstellungen der Pakete. Somit bleibt die Hauptdatei übersichtlich.

### Minted und Pygments
Zur Formatierung von Quellcode wurde die `minted`-Umgebung (https://ctan.org/pkg/minted) eingebunden. Zur Formatierung von Quellcode benötigt `minted` das Programm Pygments (https://pygments.org), welches sich mit `pip` installieren lässt:

```bash
pip3 install pygments

# Additional styles (github, monokai_light, railscasts)
git clone git://github.com/thecodechef/pygments-style-extras.git
cd pygments-style-extras
python setup.py install
```
Für die Konvertierung von LaTeX in ein PDF ist bei der Verwendung von `minted` zusätzlich noch die Option `-shell-escape` notwendig:
```bash
pdflatex -shell-escape report.tex
```

### Weiterentwicklung und Fehler
Diese Vorlagen dienen als Basis, die Sie selbstverständlich gerne erweitern oder ändern können.

Finden Sie Fehler oder haben Sie nützliche Ergänzungen, von denen alle profitieren, können Sie mir gerne die überarbeitete Vorlage als neues Template zur Verfügung stellen. Ich würde mich freuen.