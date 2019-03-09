---
layout: post
title: 'XML Schema Object Model (SOM) Parser for Delphi'
category: programming
tags: [delphi]
---

I'm working on a new project and have a need to parse XML Schemas found inside WSDL documents.  After a few google searches I discovered the concept of a Schema Object Model (SOM).  The <a href="http://www.xml.com/pub/a/2002/12/04/som.html">.NET Framework has a SOM parser</a> as does <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/xmlsdk/html/85b447ee-70d0-4456-9ad7-70b4e2d1f3fa.asp">MSXML</a>.  There's also a <a href="https://xsom.dev.java.net/">SOM parser for Java</a> as well.  Because I'm writing a Win32 application, I started learning <a href="http://www.informit.com/articles/article.asp?p=31360&amp;seqNum=1">the ins and outs of MSXML's SOM parser</a>.  As a learned more I did additional google searches and discovered Delphi has its own SOM parser.<br /><br />Interfaces such as <i>IXmlSchemaDoc</i> and functions such as <i>LoadXMLSchema</i> and <i>LoadXMLSchemaStr</i> are undocumented but the source can be found in <i>source\win32\xml\XMLSchema.pas</i>.  There is also <a href="http://codecentral.borland.com/Item.aspx?id=21870">sample code for parsing an XML Schema</a> available BDN.  With the aid of the sample code I was able to get my sample project working.  <br /><br />And in case you are wondering, the VCL library has a component called <i>TXMLSchemaDoc</i> that wraps Delphi's SOM parser into a handy component.  You will not find it in the tool pallet though.  For what it is worth, I found working with the interface (<i>IXmlSchemaDoc</i>) easy and I have not tried the <i>TXMLSchemaDoc</i> component.