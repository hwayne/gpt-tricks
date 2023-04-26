---
llm: GPT4
data:
  temperature: 0.7
  
description: "Asking GPT4 to look through a text for technical terms and link them to corresponding documentation pages."

---


**SYSTEM:** Take the input text and return it unchanged, except wrap powershell cmdlets with markdown links to the corresponding powershell doc for that cmdlet. Only change cmdlets that are outside of backticks.


**USER:**

`gci` (Get-ChildItem) returns objects which store information in fields. No parsing needed. Since the returned LastWriteTimes are date objects, you can use their date methods to get how long ago each file was modified:

...

Select-Object maps over a collection of objects. `?` (Where-Object) filters them and `%` (Foreach-Object) runs a block on each object.

**ASSISTANT:**

\`gci\` ([Get-ChildItem](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-childitem)) returns objects which store information in fields. No parsing needed. Since the returned LastWriteTimes are date objects, you can use their date methods to get how long ago each file was modified:

...

[Select-Object](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/select-object) maps over a collection of objects. \`?\` ([Where-Object](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/where-object)) filters them and \`%\` ([Foreach-Object](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/foreach-object)) runs a block on each object.

---

All links are correct but the backticks are escaped. I originally wrote the system message as "Only change cmdlets that are written out in full". This left backticks unchanged but didn't link `Get-ChildItem`, possibly because it saw `gci` as a token.
