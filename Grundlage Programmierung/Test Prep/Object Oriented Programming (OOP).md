---
topic: Object Oriented Programming (OOP)
category: OOP
status: in-progress
date_learned: 2025-03-02
tags:
  - OOP
  - Python
  - Basics
  - German
---

- [[#Was ist eine Klasse?]]
- [[#Was ist ein Objekt?]]
- [[#Was ist ein Konstruktor (`___init___`)]]
	- [[#Warum brauchen wir einen Konstruktor?]]
	- [[#❌ Ohne Konstruktor|Beispiel: Ohne Konstruktor]]
	- [[#✅ Mit Konstruktor|Beispiel: Mit Konstruktor]]
- [[#Was ist eine Client-Klasse]]
	- [[#Eine Client-Klasse in Aktion]]
	- [[#Warum kann `Bibliothek` kein `str` akzeptieren, aber `Magazine` schon?]]
- [[#Was ist Vererbung (Inheritance)?]]
	- [[#Warum ist Vererbung nützlich?]]
- [[#Wie hängen Public, Protected und Private mit Vererbung zusammen?]]
	- [[#Public Attribute und Methoden (Standard in Python)|Wie funktioniert Public]]
	- [[#Protected Attribute und Methoden (_protected)|Wie funktioniert Protected (Geschützt)]]
	- [[#Private Attribute und Methoden (__private)|Wie funktioniert Private]]
	- [[#Wie kann man private Attribute trotzdem nutzen? (Getters & Setters)|Getters and Setters]]
	- [[#Fazit - Sichtbarkeit in Klassen (Public, Protected, Private)]]

#### Was ist eine Klasse?

Eine Klasse ist eine Vorlage (Blueprint) für Objekte.

```python
# Klasse
class Buch: # Klasse erstellen
	def __init__ (self, titel): # Konstruktor
		self.titel=titel # Attribute speichern
```

#### Was ist ein Objekt?
Ein Objekt ist eine konkrete Instanz einer Klasse.
Wenn wir eine Klasse verwenden, um ein Objekt zu erstellen, bekommt es echte Werte.

```python
# Klasse
class Buch: # Klasse erstellen
	def __init__ (self, titel): # Kontruktor
		self.titel=titel # Attribute speichern
		
#---------------------------------------------------------#
#---------------------------------------------------------#
# Objekt

# Ein Objekt der Klasse erstellen
mein_buch = Buch("Python Grundlagen") # Objekt mit echtem Titel

print(mein_buch.titel) # Ausgabe: Python Grundlagen
```

1. Die Klasse `Buch` ist eine Vorlage, sie sagt: "Jedes Buch hat einen Titel"
2. `mein_buch = Buch("Python Grundlagen")` erstellt ein Objekt mit dem Titel "Python Grundlagen"
3. Das Attribute `titel` speichert diesen Wert.
4. Jedes Objekt kann eigene Werte haben.

```python
# Klasse
class Buch: # Klasse erstellen
	def __init__ (self, titel): # Kontruktor
		self.titel=titel # Attribute speichern
		
#---------------------------------------------------------#
#---------------------------------------------------------#
# Objekt

# Ein Objekt der Klasse erstellen
mein_buch = Buch("Python Grundlagen") # Objekt mit echtem Titel
dein_buch = Buch("Java Grundlagen") # Zweite Objekt mit Titel

print(dein_buch.titel) # Ausgabe: Java Grundlagen
print(mein_buch.titel) # Ausgabe: Python Grundlagen
```

#### Was ist ein Konstruktor (`___init___`)
Ein Konstruktor ist eine spezielle Methode in einer Klasse.
Er wird automatisch aufgerufen, wenn ein neues Objekt erstellt wird.

##### Warum brauchen wir einen Konstruktor?
- Er gibt dem Object Startwerte.
- Ohne ihn hätten Objekte keine individuellen Eigenschaften.
- Er sorgt dafür, dass das Objekt sofort nutzbar ist.

###### ❌ Ohne Konstruktor

```python
class Buch:
	pass # Keine Attribute oder Methoden

mein_buch = Buch() # Objekt erstellen
mein_buch.titel = "Python Grundlagen" # Manuelle eine Eigeschaft hinzufugen.

print(mein_buch.titel) # Ausgabe: Python Grundlagen

```

Das Objekt hat keine Attribute, bis wir sie manuell setzen.

Wir müssen zuerst `mein_buch = Buch()` aufrufen, um ein Objekt der Klasse `Buch` zu erstellen.
Wenn die Klasse `Buch` keinen Konstruktor hat, können wir danach `mein_buch.titel = "Python Grundlagen"` schreiben, um ein neues Attribut zu erstellen und ihm einen Wert zuzuweisen.
<br>
Das Attribut **existiert nicht von Anfang an**.
Jedes neue `Buch`-Objekt **hätte kein `titel`, bis man es manuell setzt**.

###### ✅ Mit Konstruktor

```python
class Buch:
    def __init__(self, titel):
        self.titel = titel  # Attribut wird direkt gesetzt

mein_buch = Buch("Python Grundlagen")  # Titel direkt beim Erstellen setzen
print(mein_buch.titel)  # Ausgabe: Python Grundlagen

```

Das Objekt hat das Attribut bereits, sobald es erstellt wird, weil der Konstruktor es automatisch setzt.

Wir müssen zuerst `mein_buch = Buch("Python Grundlagen")` aufrufen, um ein Objekt der Klasse `Buch` zu erstellen.  
Da die Klasse `Buch` einen Konstruktor hat, wird `titel` direkt beim Erstellen gesetzt, ohne dass wir es manuell hinzufügen müssen.
<br>
Das Attribut **existiert von Anfang an**.  
Jedes neue `Buch`-Objekt **hat automatisch ein `titel`-Attribut mit dem übergebenen Wert**.

==**Wenn die Klasse `Buch` einen Konstruktor hat, der einen `titel`-Parameter erfordert, müssen wir immer einen Titel angeben, wenn wir ein neues Objekt erstellen.**==

#### Was ist eine Client-Klasse

Eine Client-Klasse ist eine Klasse, die eine andere Klasse nutzt aber ==nicht erbt==.
Sie arbeitet mit einem Objekt einer anderen Klasse.

```python
class Buch:
    def __init__(self, titel):
        self.titel = titel  

class Bibliothek:
	def speichere_buch(self, buch_objekt):
		print(f"Das Buch '{buch_objekt.titel}' wurde gespeichert." )
		
```

`speichere_buch(self, buch_objekt)` nimmt ein Buch Objekt als Argument.
`buch_objekt.titel` liest den Titel des Buchs aus der `Buch` Klasse.

##### Eine Client-Klasse in Aktion

```python
class Buch:
    def __init__(self, titel):
        self.titel = titel 

class Bibliothek:
	def speichere_buch(self, buch_objekt):
		print(f"Das Buch '{buch_objekt.titel}' wurde gespeichert." )

# ------------------------------------------------------- #
# ------------------------------------------------------- #
# Buch-Objekt erstellen
mein_buch = Buch("Python Grundlagen")

# Bibliothek-Objekt erstellen
stadtbibliothek = Bibliothek()

# Buch in die Bibliothek speichern
stadtbibliothek.speichere_buch(mein_buch)
```

1. `mein_buch = Buch("Python Grundlagen")` erstellt ein Buch-Objekt.  
2. `stadtbibliothek = Bibliothek()` erstellt eine Bibliothek.  
3. `stadtbibliothek.speichere_buch(mein_buch)` übergibt das Buch an die Bibliothek.  
4. `buch_objekt.titel` wird ersetzt durch `"Python Grundlagen"`.
<br>
5. Ausgabe:

```cmd
"Das Buch 'Python Grundlagen' wurde gespeichert."
```

##### Warum kann `Bibliothek` kein `str` akzeptieren, aber `Magazine` schon?

Die Klasse ==`Bibliothek` erwartet kein bestimmtes Objekt== wie `Buch`.
Sie erwartet nur ein Objekt mit einem `titel` Attribut, egal welches.

- Ein String (str) hat kein .titel, also gibt es einen Fehler.
- Jede Klasse mit einem .titel-Attribut kann aber funktionieren!

```python
class Buch:
    def __init__(self, titel):
        self.titel = titel  

class Magazine:
    def __init__(self, titel):
        self.titel = titel  

class Bibliothek:
    def speichere_buch(self, buch_objekt):
        print(f"Das Buch '{buch_objekt.titel}' wurde gespeichert.")

# ✅ Funktioniert: Beide Klassen haben .titel
mein_buch = Buch("Python Grundlagen")
mein_magazin = Magazine("Python Mag")

meine_bibliothek = Bibliothek()

meine_bibliothek.speichere_buch(mein_buch) 
# ✅ Ausgabe: Das Buch 'Python Grundlagen' wurde gespeichert.
meine_bibliothek.speichere_buch(mein_magazin)  
# ✅ Ausgabe: Das Buch 'Python Mag' wurde gespeichert.

meine_bibliothek.speichere_buch("Python Grundlagen")
# ❌ Fehler: Ein String hat kein .titel

```


#### Was ist Vererbung (Inheritance)?

Vererbung bedeutet, dass eine Klasse Eigenschaften und Methoden einer anderen Klasse erbt.
Die Elternklasse (Parent-Klasse) stellt die Basis dar, und die Kindklasse (Child-Klasse) erweitert oder verändert diese.

##### Warum ist Vererbung nützlich?
1. Vermeidet doppelten Code – Gemeinsamkeiten werden in der Elternklasse definiert.
2. Die Kindklasse kann eigene Methoden hinzufügen oder bestehende Methoden überschreiben.
3. Neue Klassen können leicht erstellt werden, ohne alles von Grund auf neu schreiben zu müssen.

```python
class Buch:  # Elternklasse (Parent)
    def __init__(self, titel, autor):
        self.titel = titel
        self.autor = autor

    def beschreiben(self):
        print(f"'{self.titel}' von {self.autor}")

# ------------------------------------------------------- #
# ------------------------------------------------------- #

# Kindklasse (Child) erbt von Buch
class Ebook(Buch):
    def __init__(self, titel, autor, dateiformat):
        super().__init__(titel, autor)  # Ruft den Konstruktor der Elternklasse auf
        self.dateiformat = dateiformat  # Neues Attribut
        
    def anzeigen_format(self):
        print(f"Das E-Book '{self.titel}' ist im Format {self.dateiformat}")

# ------------------------------------------------------- #
# ------------------------------------------------------- #

# Ein normales Buch erstellen
mein_buch = Buch("Python Grundlagen", "Max Mustermann")
mein_buch.beschreiben()  
# Ausgabe: 'Python Grundlagen' von Max Mustermann

# Ein E-Book erstellen
mein_ebook = Ebook("Python für Fortgeschrittene", "Anna Beispiel", "PDF")
mein_ebook.beschreiben()  # Geerbte Methode aus 'Buch'
# Ausgabe: 'Python für Fortgeschrittene' von Anna Beispiel
mein_ebook.anzeigen_format()  # Neue Methode aus 'Ebook'
# Ausgabe: Das E-Book 'Python für Fortgeschrittene' ist im Format PDF
```

#### Wie hängen Public, Protected und Private mit Vererbung zusammen?
In der objektorientierten Programmierung (OOP) bestimmen Public, Protected und Private, wie zugänglich Attribute und Methoden innerhalb und außerhalb einer Klasse sind.

🔹 Public (public) → Kann überall genutzt werden (innerhalb und außerhalb der Klasse).<br>
🔹 Protected (_protected) → Sollte nur innerhalb der Klasse und in Unterklassen verwendet werden.<br>
🔹 Private (\__private) → Ist nur innerhalb der Klasse sichtbar.

##### Public Attribute und Methoden (Standard in Python)

In Python sind **alle Attribute und Methoden standardmäßig öffentlich (public)**.  
**Öffentliche Attribute werden von der Kindklasse geerbt und können überall verwendet werden.**

```python
class Buch:
    def __init__(self, titel, autor):
        self.titel = titel  # Öffentliches Attribut
        self.autor = autor  # Öffentliches Attribut

    def beschreiben(self):  # Öffentliche Methode
        print(f"'{self.titel}' von {self.autor}")
        
# ------------------------------------------------------- #
# ------------------------------------------------------- #

class Ebook(Buch):
    def __init__(self, titel, autor, dateiformat):
        super().__init__(titel, autor)
        self.dateiformat = dateiformat  # Öffentliches Attribut

    def anzeigen_format(self):
        print(f"Das E-Book '{self.titel}' ist im Format {self.dateiformat}")
        
# ------------------------------------------------------- #
# ------------------------------------------------------- #

# Alles funktioniert, weil die Attribute public sind
mein_ebook = Ebook("Python für Fortgeschrittene", "Anna Beispiel", "PDF")
print(mein_ebook.titel)  
# Ausgabe: Python für Fortgeschrittene
mein_ebook.beschreiben()  
# Ausgabe: 'Python für Fortgeschrittene' von Anna Beispiel

```

##### Protected Attribute und Methoden (_protected)

Ein **geschütztes (protected) Attribut oder eine Methode** sollte **nur innerhalb der Klasse oder in Unterklassen** genutzt werden.  <br>

Python **erzwingt** diese Regel nicht, aber die **Konvention** ist, dass Attribute mit einem **Unterstrich (`_`)** nicht direkt von außen genutzt werden sollten.

```python
class Buch:
    def __init__(self, titel, autor):
        self._titel = titel  # Geschütztes Attribut
        self._autor = autor  # Geschütztes Attribut

    def beschreiben(self):
        print(f"'{self._titel}' von {self._autor}")
 
# ------------------------------------------------------- #
# ------------------------------------------------------- #

class Ebook(Buch):
    def __init__(self, titel, autor, dateiformat):
        super().__init__(titel, autor)
        self._dateiformat = dateiformat  # Geschütztes Attribut

    def anzeigen_format(self):
        print(f"Das E-Book '{self._titel}' ist im Format {self._dateiformat}")

# ------------------------------------------------------- #
# ------------------------------------------------------- #

# ✅ Funktioniert innerhalb der Klasse
mein_ebook = Ebook("Python für Fortgeschrittene", "Anna Beispiel", "PDF")
mein_ebook.beschreiben()  
# Ausgabe: 'Python für Fortgeschrittene' von Anna Beispiel
mein_ebook.anzeigen_format()  
# Ausgabe: Das E-Book 'Python für Fortgeschrittene' ist im Format PDF

# ⚠️ Direkter Zugriff ist möglich, aber nicht empfohlen
print(mein_ebook._titel)  
# ⚠️ Technisch möglich, aber sollte vermieden werden

```
<br>
1. Subclasses can access `_titel` and `_autor` because they are protected.  <br>
<br>
2. Outside access (e.g., `mein_ebook._titel`) is possible (in python) but discouraged.

##### Private Attribute und Methoden (__private)

Ein privates Attribut oder eine private Methode ist nur innerhalb der Klasse sichtbar. <br>
Sie wird nicht an Kindklassen weitergegeben. <br>
Python erzwingt dies durch Namensänderung (Name Mangling: __attribut → _Klassenname__attribut).

```python
class Buch:
    def __init__(self, titel, autor):
        self.__titel = titel  # Privates Attribut
        self.__autor = autor  # Privates Attribut

    def beschreiben(self):
        print(f"'{self.__titel}' von {self.__autor}")

# ------------------------------------------------------- #
# ------------------------------------------------------- #

class Ebook(Buch):
    def __init__(self, titel, autor, dateiformat):
        super().__init__(titel, autor)
        self.__dateiformat = dateiformat  # Privates Attribut

    def anzeigen_format(self):
        print(f"Das E-Book '{self.__titel}' ist im Format {self.__dateiformat}")  # ❌ FEHLER!

# ------------------------------------------------------- #
# ------------------------------------------------------- #

# ❌ Direkter Zugriff auf private Attribute funktioniert nicht
mein_ebook = Ebook("Python für Fortgeschrittene", "Anna Beispiel", "PDF")
mein_ebook.beschreiben()  # ❌ ERROR!
mein_ebook.anzeigen_format()  # ❌ ERROR!

```

1. `__titel` und `__autor` sind **privat** und können in `Ebook` **nicht genutzt werden**.  <br>
2. `anzeigen_format()` versucht `__titel` zu verwenden, aber es existiert in `Ebook` nicht.

##### Wie kann man private Attribute trotzdem nutzen? (Getters & Setters)

Falls ein privates Attribut **von außen lesbar oder veränderbar sein soll**, nutzt man **Getter und Setter**.

```python
class Buch:
    def __init__(self, titel, autor):
        self.__titel = titel  # Privat
        self.__autor = autor  # Privat

    def get_titel(self):  # Getter-Methode
        return self.__titel

    def set_titel(self, neuer_titel):  # Setter-Methode
        self.__titel = neuer_titel

# ------------------------------------------------------- #
# ------------------------------------------------------- #

# ✅ Objekt erstellen
mein_buch = Buch("Python Grundlagen", "Max Mustermann")

# ❌ Direkter Zugriff funktioniert nicht
# print(mein_buch.__titel)  # ❌ ERROR!

# ✅ Getter-Methode nutzen
print(mein_buch.get_titel())  
# Ausgabe: Python Grundlagen

# ✅ Setter-Methode nutzen
mein_buch.set_titel("Python für Profis")
print(mein_buch.get_titel())  
# Ausgabe: Python für Profis

```

#### Fazit - Sichtbarkeit in Klassen (Public, Protected, Private)
- **Public (`self.titel`)**
  - ✅ Geerbt von Unterklasse
  - ✅ Kann überall genutzt werden
  - **Vererbung**: Wird immer vererbt und ist überall sichtbar.

- **Protected (`self._titel`)**
  - ✅ Geerbt von Unterklasse
  - ⚠️ Sollte nicht außerhalb der Klasse genutzt werden
  - **Vererbung**: Wird vererbt, aber sollte nur in der Klasse oder Unterklassen verwendet werden.

- **Private (`self.__titel`)**
  - ❌ Nicht geerbt von Unterklasse
  - ❌ Kein Zugriff von außerhalb (nur mit Gettern/Settern)
  - **Vererbung**: Wird nicht vererbt, nur in der eigenen Klasse sichtbar.
