Why XML?
========

The XML format has been chosen because it is widely used in software configuration and many reliable
parsers are readily available. In XML, configuration items can be nested infinitely, so that options
can be easily extended. In addition, it is possible to exactly define the structure of an XML
document for a specific application, which means the content can be validated. In this way, the
validation provides invaluable help, especially for the less experienced user, to prevent
configuration errors at the earliest possible stage. The corresponding XML Schema Definition files
(XSD) can be found in the ``input/definitions/`` directory. For simplicity, in Fittino input files
only sub-nodes (and no attributes) are allowed to specify configuration options.

Complex XML files, on the other hand, are considered to be tedious to read and write. As a
countermeasure, Fittino comes with a set of dedicated style definitions, which allow the user to
look at well-arranged configuration options with a web browser. The corresponding XML Stylesheet
Language files (XSL) can be found in the ``input/style/`` directory. For the future, however, it
might be worthwhile to also consider alternative input file formats for Fittino, e.g. the rather
recent JavaScript Object Notation (JSON), which, despite being less powerful than XML, provides all
the aforementioned features and is well readable and writable at the same time.
