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
## Functions

The allowed functions that can be used in the XML equations are:

<dl>
  <dt>Pi()</dt>
  <dd>Constant value of π (3.14159265358)</dd>
                 
  <dt>Sin(x)</dt>
  <dd>Sine trigonometrical function of x in radians (i.e. Sin(π/2)=1)</dd>
                  
  <dt>Cos(x)</dt>
  <dd>Cosine trigonometrical function of x in radians (i.e. Cos(π/2)=0)</dd>
                
  <dt>Tan(x)</dt>
  <dd>Tangent trigonometrical function of x in radians (i.e. Tan(π)=0)</dd>
                  
  <dt>ASin(x)</dt>
  <dd>Arcsine in radians of x number (i.e. ASin(1)= π/2)</dd>
                  
  <dt>ACos(x)</dt>
  <dd>Arccosine in radians of x number (i.e. ACos(0)= π/2)</dd>
                    
  <dt>ATan(x)</dt>
  <dd>Arctangent in radians of x number (i.e. ATan(0)= π)</dd>
                  
  <dt>ATan2(y,x)</dt>
  <dd>Angle whose tangent is the quotient of two specified numbers (i.e. ATan2(2,1)=1.126)</dd>
                  
  <dt>Abs(x)</dt>
  <dd>Returns the absolute value of x (i.e. Abs(-1)=1)</dd>
                  
  <dt>Sqrt(x)</dt>
  <dd>Returns the square root of x (i.e. Sqrt(4)=2)</dd>
                    
  <dt>Max(x, y)</dt>
  <dd>Returns the maximum value between x and y (i.e. Max(1, 2)=2)</dd>
                   
  <dt>Min(x, y)</dt>
  <dd>Returns the minimum value between x and y (i.e. Min(1, 2)=1)</dd>
                    
  <dt>Pow(x, y)</dt>
  <dd>Returns the value of x to the power of y (xy) (i.e. Pow(2, 2)=4)</dd>
                  
  <dt>Radians(x)</dt>
  <dd>Returns the converted value of x from degrees to radians (i.e. Radians(180)= π)</dd>
                   
  <dt>Degrees(x)</dt>
  <dd>Returns the converted value of x from radians to degrees (i.e. Degrees(π)=180)</dd>
                  
  <dt>Exp(x)</dt>
  <dd>Returns e raised to the power of x (ex) (i.e. Exp(1)= 2.718282)</dd>
                   
  <dt>Log(x)</dt>
  <dd>Returns the natural (base e) logarithm of the specified x (i.e. Log(2)= 0.693147)</dd>
                  
  <dt>Log10(x)</dt>
  <dd>Returns the base 10 logarithm of a specified number (i.e. Log10(100)=2)</dd>
                  
  <dt>Concat(x,y,…)</dt>
  <dd>Returns the concatenated text of all parameters (i.e. Concat('X',1+1)=X2)</dd>
                    
  <dt>IF(c,x,y)</dt>
  <dd>Returns whether x or y depending if the condition c is true or false (i.e. If(1=2,0,1)=1)</dd>
                   
</dl>
