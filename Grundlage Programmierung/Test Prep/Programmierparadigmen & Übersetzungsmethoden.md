---
topic: Programmierparadigmen & Übersetzungsmethoden
category: Fundamentals
status: in-progress
date_learned: 2025-03-02
tags:
  - Programming
  - Basics
---

### Programmierparadigmen & Übersetzungsmethoden  

#### Programmierparadigma: Imperative Programmierung  
Das **imperative Programmierparadigma** beschreibt Programme als eine **Reihenfolge von Befehlen**, die genau vorschreiben, **wie** etwas gemacht werden soll.  

- Der Name kommt aus dem Lateinischen „imperare“ („anordnen“, „befehlen“).  
- Programme bestehen aus **Schritten**, die nacheinander ausgeführt werden.  
- Beispiel: **Strukturierte Programmierung** (z. B. **Pascal**).  

---

#### Programmierparadigma: Deklarative Programmierung  
Im **deklarativen Programmierparadigma** gibt man an, **was** das gewünschte Ergebnis ist, aber nicht den exakten Lösungsweg.  

- Man beschreibt das Ziel, **nicht den Ablauf**.  
- Wird oft für **Datenverarbeitung und mathematische Berechnungen** genutzt.  
- **Beispiele:**  
  - **Funktionale Programmierung** (z. B. **Lisp, Haskell**)  
  - **Logische Programmierung** (z. B. **Prolog**)  
  - **Mengenbasierte Abfragesprachen** (z. B. **SQL**)  

---

#### Programmierparadigma: Objektorientierte Programmierung  
- Programme werden in **Objekte** unterteilt, die **Daten und Funktionen** enthalten.  
- Erlaubt eine **modulare und wiederverwendbare Struktur**.  
- Wird oft in modernen Sprachen wie **Java, C++, Python** verwendet.  

---

### Interpreter vs. Compiler  

####  Interpreter-Sprachen  
- Der Quellcode bleibt **im Textformat** und wird **bei der Ausführung** Schritt für Schritt **interpretiert**.  
- Langsamer als Compiler, aber einfacher zu testen.  
- **Beispiele:** Python, JavaScript.  

####  Compiler-Sprachen  
- Der Quellcode wird **vor der Ausführung** in eine **binäre, computerlesbare Form** übersetzt.  
- Programme starten schneller, benötigen aber vorher eine **Kompilierung**.  
- **Beispiele:** C, C++.  

####  Java / C#: Mischform  
- Java und C# nutzen eine **Zwischenform**: Der Quellcode wird zuerst in **Bytecode** übersetzt und dann zur Laufzeit von einer **virtuellen Maschine (JVM oder .NET VM)** interpretiert.  
- Dadurch sind sie **plattformunabhängig** und laufen auf vielen Systemen.  

---

### 💡 Zusammenfassung  
- **Imperative Programmierung** gibt Befehle Schritt für Schritt vor.  
- **Deklarative Programmierung** beschreibt das Ziel, nicht den Ablauf.  
- **Objektorientierte Programmierung** nutzt Objekte und ist modular.  
- **Interpreter-Sprachen** führen Code direkt aus, **Compiler-Sprachen** übersetzen ihn vorher.  
- **Java & C# sind eine Mischung aus beiden Ansätzen** und nutzen Bytecode.  
