# Graylog-MWG-Contentpack
Collecting Syslog Ouput from McAfee Web Gateway 7.5
Collecting output from MWG.
Get your MWG to export logs like this (do NITRO/SIEM): https://community.mcafee.com/docs/DOC-5206
and  adjust the output in two ways: I erased the first and second field (first was just the appliance name, second was date).
Looks like this in MWG:
![](https://cloud.githubusercontent.com/assets/13982849/9652240/e043e724-5219-11e5-9bd2-ea5be904b2b0.JPG) 

You do need to import some grok-patterns beforehand in Graylog and make a new "input" in order to use the grok-extractor.
Importing the grok patterns is fairly straight forward: copy and paste "grok-patterns" from here http://grokdebug.herokuapp.com/patterns to a text file and import that text-file into Graylogs "import pattern file" button.
You´ll get indexed logs from the MWG like this:

![](https://cloud.githubusercontent.com/assets/13982849/9652239/e0365e42-5219-11e5-815d-e02e78df0ce5.PNG) 

Now, import the content pack and you should get an input, stream and dashboard you can adjust to your liking. One thing of note: I used a dedicated syslog port (50014).
