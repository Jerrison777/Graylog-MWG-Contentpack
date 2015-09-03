# Graylog-MWG-Contentpack
Collecting Syslog Ouput from McAfee Web Gateway 7.5
Collecting output from MWG.
Get your MWG to export logs like this (do NITRO/SIEM): https://community.mcafee.com/docs/DOC-5206
and  adjust the output in two ways: I erased the first and second field (first was just the appliance name, second was date).

You do need to import some grok-patterns beforehand in Graylog and make a new "input" in order to use the grok-extractor.
Importing the grok patterns is fairly straight forward: copy and paste "grok-patterns" from here http://grokdebug.herokuapp.com/patterns to a text file
and import that text-file into Graylogs "import pattern file" button.
