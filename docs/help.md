# Structure Wizard Template Schema

This section documents the XML schema used for Structure Wizard template files.

## XML Basics

This document describes the syntax to create a XML Template file, that could be used as an input for the Structural Template Wizard.

![Annotated description of basic XML structure](image/XML%20Structural%20Diagram.svg "Basic XML structure")

**Note:** It is recommended that you use an XML-aware editor when creating and editing XML files. Microsoft's [Visual Studio Code](https://code.visualstudio.com/) with the [XML Language Support extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml) from Red Hat is a free and easy-to-use example.

### Reserved Markup Characters

Some special characters are not allowed in XML code (known as reserved markup characters). In order to utilize these in attribute or element values, you must utilize the following character escape sequences:

| Name | Symbol | Escape Sequence |
| ---- | ------ | --------------- |
| Double quote | " | `&quot;` or `&#34;` |
| Single quote (apostrophe) | ' | `&apos;` or `&#39;` |
| Lesser than |  < | `&lt;` or `&#60;` |
| Greater than | > | `&gt;` or `&#62;` |
| Ampersand | & | `&amp;` or `&#38;` |

For example, to write a condition "A < 5", you need to use:
```xml
<If Condition="a&lt;5" />
```
