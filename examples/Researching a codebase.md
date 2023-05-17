---
llm: GPT4
data:
  temperature: 0.7
  
description: "Asking GPT4 to look through a text for technical terms and link them to corresponding documentation pages."

---

**User:** In the python library dagster, where is the class that manages the workflow DAG defined?


**Assistant:** In the Dagster library, the class that manages the workflow DAG (directed acyclic graph) is defined in `dagster/core/definitions/graph.py`. The class is called `GraphDefinition`.

---

The actual path is `dagster/_core/definitions/graph_definition.py`, but the name is correct and easily findable with grepping.

---


