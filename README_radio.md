- Use soundconvrter to generate .ogg file and put at Pi_Radio_Server/store/ folder
- mp3 file name space 
- remove space of filename
- $ sudo apt install rename
-  do the directories first 
- find . -name "* *" -type d | rename 's/ /_/g'
-  do the files then 
-  find . -name "* *" -type f | rename 's/ /_/g'


                 