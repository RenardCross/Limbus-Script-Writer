# Limbus-Script-Writer

Version 1.0

Hey there! Thanks for using this tool! I hope you find it useful!

Below are instructions on how the tool operates. There a few things to note first however.

1. This tool assumes you know how dialogue and setup files work and are structured.
If you need a refresher or details you can click on Help and review the guides included.

2. This tool just aids you in creating json files. It does not validate whether a file is
in the correct format or not. There are some guard rails and warnings that try to help you create a properly formatted
file but there is no grantee they work once loaded into Limbus Company.

There is also no preview or testing offered by this tool. You will have to load the files 
into the game to test them.

3. Depending on when you use this tool some of the data loaded in may be out of date.
I have put in a function that will read data from a public data index created by May
however I cannot grantee that the format of the file will always be able to be processed
by this tool or even be avialable. The credits contain a link to May's website which includes links to 
what data is available.


\\\\\\\\\\ Data Loading \\\\\\\\\\

This tool uses a sqlite3 database to store and load data.

There is a pre-loaded database included with this tool. If for whatever reason
you delete the database or it becomes corrupted you will need to redownload the tool to get a new one.

There is currently no manual data loading. The data was based off of a publicly available data index put
together by May. Under File is an option to update (load a fresh database) with data from this index.
If you try to update and see some weird data issues, there is a clear database function under File. Once the database is cleared
try to reload the database.

\\\\\\\\\\ Operation \\\\\\\\\\

Given how files tie together, the script writer assumes you will first make DIALOGUE files
then make SETUP files. You can of course make whatever file you want first but will get some 
warnings.

When making a SETUP file, make sure you SORT THE LIST OF SETUPS before you save out!
Limbus Company requires that the setup nodes are in ascending order by ID in order to work!
If you do not sort before saving the json file then it may not work when loaded in to Limbus Company.

If you need to just update a file you can just load it in and ignore the warnings.

Note that the file is generated based on what is present in the preview window. You can edit whatever you want
in the preview and save that out.

All input boxes take raw input and you can put whatever you want in there. To reiterate, all input boxes can be MANUALLY overwritten 
with whatever values you want. They are pre loaded with data to help make things easier and to help populate your files with valid 
data that Limbus Company will then load. The Script Writer will let you put whatever you want into input boxes however in the event there's 
some data missing or the data is not up to date.

It is important to note again that the Script Writer does NOT validate files

The setup file creation window has a field called "Setup #". This is purely for INTERNAL use and to easily select a setup
you wish to edit. It literally means nothing for the setup file, it's sole purpose is to help you jump to a setup index.

All indexes are ZERO based, that is, they start at 0 and go up. So index 1 is actually index 0 and so on.

When saving out the json files you will have to name them correctly manually.

\\\\\\\\\\ Help/Tooltips \\\\\\\\\\

On the Setup window there are tool tips to help with each section. Simply hover over then "?" icon next
to each section's name.

\\\\\\\\\\ Errors \\\\\\\\\\

While this tool is not designed to validate the JSON files, it does try to help you find issues with your file.

Aside from the warning boxes look out for setup or dialogue with id's of -1. This typically means something
has gone wrong with that block in the JSON file.

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
