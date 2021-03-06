# convert-textra-db-to-xml
Export from textra database to XML format compatible with 'SMS Backup and Restore'

Textra => SMS Backup and Restore => Android Stock - conversion script
 
2015 Ben Jones / octopod.org

http://github.com/textra-to-sms-backup-and-restore-conversion-script
 
A very rough script. Inefficient and cobbled together. But did the job of a one-off conversion from a Textra database, to SMS backup and restore XML format, which allowed me to import the messages back into the android messages database.
 
Perhaps some issues remain - out of 13k messages I had about 10 fail to import and a couple of conversations show 'loading mms' every time I open them. I don't know if it was the conversion or if they were bad in the original. But those results were good enough for me.
 
Instructions:
- Clone this repo or download convert.groovy
- Change the variables 'pathToTextraData' to a path to your backup directory with Textra's 'data' folder
- Change the variable 'myMobileNumber' to be your mobile number with + prefix
- Install Groovy from http://www.groovy-lang.org/download.html
- Run the export to read your textra data and produce an XML file (i.e. `groovy convert.groovy`)
- Copy XML file onto your device
- Install 'SMS Backup and Restore' on the device from the play store
- Use 'SMS Backup and Restore' to load the file and import the messages
 
Thanks to
- Textra - http://www.textra.me/
- SMS Backup and Restore - http://android.riteshsahu.com/apps/sms-backup-restore
 
Both great apps. It was my ignorance with backups which left me with only a Textra database and not a stock messaging database.

Tested on Textra version 2.5, SMS Backup and Restore version 7.42, and messaging database  from a Samsung S6 5.0 stock firmware.

Possible issues:
- This was tested on a mac. Linux should work OK too. For Windows, you might need to edit the paths to the files but it might work.
