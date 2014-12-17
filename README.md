QueryCSelector
==============

Simple C# implementation for a querySelector JQuery-ish function for XML documents.

```C#
QuerySelector QS = New QuerySelector();
  QS.CreateFromFile("GetMemberResponse.xml");
  //Use Xpath expressions
  QS.Select("vouchersList/voucher/productId").GetElement(2).Text("test");
  Console.WriteLine(QS.Render());
```
#### Methods
`Create` loads the XML string, XElement or XElements object.

`Select` executes an XPath expression to query the document.

`GetElement(i)` gets the QuerySelector object for the i node from a collection of nodes result of a previous selection.

`Length` gets the number of nodes resulting from a selection.

`Text` same as JQuery function.

`Attr` gets or sets attributes.

`Render` ToString method.

#### Additional info
This is just an alpha proof of concept to get simple things done quick (get/set node values and attributes)

Namespaces are ignored
