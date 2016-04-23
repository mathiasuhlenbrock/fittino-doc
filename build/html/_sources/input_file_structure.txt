Input file structure
====================

The basic structure of a Fittino input file looks like this ::

   <?xml version="1.0" encoding='UTF-8'?>
   <?xml-stylesheet type="text/xsl" href="style/InputFile.xsl"?>

   <InputFile>
     <GlobalOption>Value</GlobalOption>
     ...
     <Model>
       ...
     </Model>
     <Tool>
       ...
     </Tool>
   </InputFile>

The root node (or root element) is ``<InputFile>``. The model of interest, the analysis tool and
several global configuration options, which affect the general behavior of Fittino, are then
specified as first-level sub-nodes. How this is done is explained in detail in the following
sections.
