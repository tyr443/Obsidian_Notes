---
topic: Datentypen
category: Fundamentals
status: in-progress
date_learned: 2025-03-02
tags:
  - Python
  - Basics
  - Data_Types
  - German
---

# Übersicht der wichtigsten primitiven Datentypen in Java

### Was sind Datentypen?  
Jede Programmiersprache arbeitet mit **Daten** – Zahlen, Texte, Wahr/Falsch-Werte usw.  
Ein **Datentyp** sagt dem Computer, **was für eine Art von Wert gespeichert wird** und **wie viel Speicher er braucht**.

### Primitive Datentypen

| **Typ**   | **Speicher** | **Beschreibung** | **Beispiele** |
|----------|-------------|------------------|--------------|
| `bool`   | 1 Bit       | `true` oder `false` | `true`, `false` |
| `char`   | 16 Bit      | Unicode-Zeichen (UTF-16) | `'A'`, `'9'`, `'€'` |
| `byte`   | 8 Bit       | Zahl `-128` bis `127` | `100`, `-50` |
| `short`  | 16 Bit      | Zahl `-32k` bis `32k` | `32000`, `-150` |
| `int`    | 32 Bit      | Zahl `-2Mrd` bis `2Mrd` | `42`, `-100` |
| `long`   | 64 Bit      | Große Zahl | `123456789012345L` |
| `float`  | 32 Bit      | Fließkommazahl | `3.14f`, `-0.5f` |
| `double` | 64 Bit      | Präzisere Fließkommazahl | `3.14159` |


#### Hinweise:

**Einfache Genauigkeit (`float`)**: Speichert Fließkommazahlen mit **32 Bit**, hat aber eine **begrenzte Präzision** (~7 Dezimalstellen).  <br>
**Doppelte Genauigkeit (`double`)**: Speichert Fließkommazahlen mit **64 Bit** und bietet eine **höhere Präzision** (~15 Dezimalstellen).

#### Fazit

- **Primitive Datentypen sind effizient und haben feste Speichergrößen**, was die Leistung optimiert.  
- **Speicherverbrauch hängt von der richtigen Wahl des Datentyps ab**.  

---

### Zusammengesetzte Datentypen: `str` und Listen/Tuples

Zusammengesetzte Datentypen bestehen aus mehreren Werten und bieten mehr Möglichkeiten als einfache Zahlen oder Zeichen.

| **Datentyp**  | **Speicherplatz** | **Beschreibung** | **Beispielwerte** |
|--------------|----------------|------------------|----------------|
| `str` (String) | Variabel | Ein Text, kann nicht geändert werden | `"Hallo"`, `"Python"` |
| `list` (Liste) | Variabel | Eine veränderbare Liste mit verschiedenen Werten | `[1, "Text", 3.5]` |
| `tuple` (Tupel) | Variabel | Eine Liste, die nicht geändert werden kann | `(1, 2, 3)`, `("X", "Y")` |
| `array` (aus `array`-Modul) | Variabel | Eine Liste mit Werten des gleichen Typs | `array('i', [1, 2, 3])` |

#### Hinweise: 
- **`str` kann nicht verändert werden** → Eine Änderung erzeugt ein **neues Objekt**.  
- **`list` kann geändert werden** → Man kann Werte hinzufügen oder entfernen.  
- **`tuple` ist wie eine `list`, aber kann nicht verändert werden**.  
- **`array` ist wie eine `list`, aber speichert nur einen Typ von Werten (z. B. nur Zahlen)**.  


==Datentypen können in verschiedenen Programmiersprachen unterschiedlich viel Speicherplatz brauchen, weil jede Sprache eigene Regeln für die Speicherung und Verarbeitung von Daten hat.==