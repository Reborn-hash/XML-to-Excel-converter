# XML to Excel Converter

The following utility I created out of necessity for the ability to do data validations of incoming XML files. I researched solutions before development, however, did not find anything to cope with complex XML files exhibiting changing column names and varying depth. The solution I developed is essentially a plug and play solution which only needs an input xml path to work.


- The converter uses the library xml.etree.ElementTree to source the root and tags of the file, and then iterates over the data adding each to a dictionary which is then sent to a pandas dataframe.
- The function iterate uses recursion to find the maximum depth of the XML file.
- The resulting dataframe can then be exported to an excel file, fully representing the data from the XML file.
