---
llm: GPT4
data:
  temperature: 0.7
  
description: "Looking up the Bureau of Labor Statistics OES codes for a set of occupations"

---

OES (Occupational Employment Statistics) codes can be used to look up data for a given profession. For example, the code for "Software Developer" is 15-1252 and leads to [this page](https://www.bls.gov/oes/current/oes151252.htm).

The below use-case did not use code formatting blocks; I added them in to get proper newlines in markdown.

---

**System:** give me data in the following format:

Civil Engineer: oes172051

**User:** Complete the BLS OES table:

```
Civil Engineer: oes172051
Mechanical Engineer: 
Chemical Engineer:
Electrical Enigneer:
Industrial Engineer:
```

**Assistant:**

```
Civil Engineer: oes172051
Mechanical Engineer: oes172141
Chemical Engineer: oes172041
Electrical Engineer: oes172071
Industrial Engineer: oes172112
```
All of the 


**User:**

Continue the table.

**Assistant:**

```
Aerospace Engineer: oes172011
Biomedical Engineer: oes172031
Computer Hardware Engineer: oes172061
Environmental Engineer: oes172081
Materials Engineer: oes172131
Nuclear Engineer: oes172161
Software Engineer: oes151132
Structural Engineer: oes172181
```

---

All of these were correct with the exception of "Software Engineer" and "Structural Engineer", neither of which are BLS occupations. Interestingly 15-1132 [*used to be*](https://web.archive.org/web/20200309184536/https://www.bls.gov/oes/current/oes_stru.htm) the code for "software developers" but it was changed after GPT's training cutoff.

