# QuickMatch
Fast username matcher that compares username list against a combo file and outputs all matching entries.

**Prerequisite**: YOU MUST OWN/DOWNLOAD NODEJS & NOTEPAD++ (not required but highly recommended in case you cannot open the breach file)
You can find the download links here: https://nodejs.org/en/download  and  https://notepad-plus-plus.org/downloads/

**NODEJS:**
Choose the .msi version and leave default options checked.
When you've finished installing it open a Command Prompt window and type "node -v" and then "npm -v".
You should see numbers like v22.18.0 and 10.9.3 and don't worry if they don't match this description here.


**Download and unzip the folder.**
Place your breach file into this folder and rename it to combos.txt this folder will be where you move your SJ usernames.




**Prepare your username list (this is through Notepad++)**
Open collected_usernames.txt from SJ.

Press Ctrl + A to select everything.

Press Ctrl + H.

Set Search Mode to Regular Expression.

In Find What, paste: ^\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z - 

Leave Replace With blank.

Click Replace All.

Copy the cleaned usernames into names.txt then save names.txt.




**To run the checker:**
Open your folder.

Click the address bar at the top.

Type: cmd

Press Enter.

In the Command Prompt window, run: node match_names.js

The script will compare every username in names.txt against every entry in combos.txt.

**You'll see progress messages like:**

Checked 1,000,000 lines...
Checked 2,000,000 lines...

When it's finished, a new file called: **matches.txt** will be created containing all matching entries in the format: **username:password** from the breach file.
