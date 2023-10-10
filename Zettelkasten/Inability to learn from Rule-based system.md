---
tags:
  - Russel-n-Norvig-chap-3
---
One can say that [[Rule-based system - Expert system]] are good because:
1. They present a *Natural knowledge representation*. Like a person will explain.
2. *Uniform structure*. All of them are in this IF-THEN structure, easily accessed.
3. Clear *separation of knowledge from its processing*. Knowledge base in one side and inference engine on the other.

**THOUGH** we must remember the drawbacks:
1. **Opaque relations between rules**. For this we must rely on extensive and costly documentation
2. **Ineffective search strategy**. If you have a system of 100 rules, the [[Search problem]] to solve this is intractable, since you one have to pass through all the rules checking their conditions every time a new fact appears.
3. **Inability to learn**. A system like this depends on the designer's input, will never evolve to create new rules out of the blue.
