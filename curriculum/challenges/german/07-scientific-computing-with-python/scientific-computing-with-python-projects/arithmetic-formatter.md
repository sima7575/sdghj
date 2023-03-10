---
id: 5e44412c903586ffb414c94c
title: Arithmetischer Formatierer
challengeType: 10
forumTopicId: 462359
dashedName: arithmetic-formatter
---

# --description--

Du wirst <a href="https://replit.com/github/freeCodeCamp/boilerplate-arithmetic-formatter" target="_blank" rel="noopener noreferrer nofollow">mit unserem Replit-Startercode an diesem Projekt arbeiten</a>.

-   Start by importing the project on Replit.
-   Next, you will see a `.replit` window.
-   Select `Use run command` and click the `Done` button.


# --instructions--

Schüler der Grundschule stellen oft arithmetische Probleme vertikal auf, um sie leichter lösen zu können. Zum Beispiel wird "235 + 52" zu:

```py
  235
+  52
-----
```

Erstelle eine Funktion, die eine Liste von Strings mit artihmetischen Problem empfängt und die angeordneten Probleme vertikal und nebeneinander zurückgibt. Optional sollte die Funktion ein zweites Argument verwenden. Wenn das zweite Argument auf `True` gesetzt ist, sollten die Antworten gezeigt werden.

## Beispiel

Function-Call:

```py
arithmetic_arranger(["32 + 698", "3801 - 2", "45 + 43", "123 + 49"])
```

Output:

```py
   32      3801      45      123
+ 698    -    2    + 43    +  49
-----    ------    ----    -----
```

Function-Call:

```py
arithmetic_arranger(["32 + 8", "1 - 3801", "9999 + 9999", "523 - 49"], True)
```

Output:

```py
  32         1      9999      523
+  8    - 3801    + 9999    -  49
----    ------    ------    -----
  40     -3800     19998      474
```

## Regeln

Die Funktion gibt die korrekte Konvertierung zurück, wenn die übergebenen Probleme richtig formatiert sind. Andernfalls **gibt** er einen **String** zurück, der einen für den Benutzer aussagekräftigen Fehler beschreibt.


- Situations that will return an error:
  - If there are **too many problems** supplied to the function. The limit is **five**, anything more will return: `Error: Too many problems.`
  - The appropriate operators the function will accept are **addition** and **subtraction**. Multiplication and division will return an error. Other operators not mentioned in this bullet point will not need to be tested. The error returned will be: `Error: Operator must be '+' or '-'.`
  - Each number (operand) should only contain digits. Otherwise, the function will return: `Error: Numbers must only contain digits.`
  - Each operand (aka number on each side of the operator) has a max of four digits in width. Otherwise, the error string returned will be: `Error: Numbers cannot be more than four digits.`
- If the user supplied the correct format of problems, the conversion you return will follow these rules:
  - There should be a single space between the operator and the longest of the two operands, the operator will be on the same line as the second operand, both operands will be in the same order as provided (the first will be the top one and the second will be the bottom).
  - Numbers should be right-aligned.
  - There should be four spaces between each problem.
  - There should be dashes at the bottom of each problem. The dashes should run along the entire length of each problem individually. (The example above shows what this should look like.)

## Entwicklung

Schreibe deinen Code in `arithmetic_arranger.py`. Für die Entwicklung kannst du `main.py` verwenden, um die `arithmetic_arranger()` Funktion zu testen. Klicke den "Run"-Button und `main.py` wird ausgeführt.

## Testen

Die Unit-Tests für dieses Projekt sind in `test_module.py`. Wir haben die Tests von `test_module.py` zu `main.py` bereits für dich importiert. Die Tests werden automatisch ausgeführt, wenn du auf den "Run"-Button klickst. Alternativ können die Tests auch ausgeführt werden, indem du `pytest` in die Konsole eingibst.

## Absenden

Kopiere die URL deines Projekts und sende sie an freeCodeCamp.

# --hints--

Es sollte ein arithmetisches Problem korrekt formatieren und alle Tests bestehen.

```js

```

# --solutions--

```js
/**
  Backend challenges don't need solutions,
  because they would need to be tested against a full working project.
  Please check our contributing guidelines to learn more.
*/
```
