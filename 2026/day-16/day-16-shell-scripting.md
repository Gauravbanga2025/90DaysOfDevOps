**Task 1 
**

# Created File hello.sh under scripts folder
1. vim hello.sh
   shell script content 
  ** #!/bin/bash
    << comments
    Shell Scripting Basics
    comments
    echo "Hello, Devops!"**
   
   # change the permission of the file with chmod +x hello.sh then execute it by ./hello.sh
   # and if you remove the shebang from the top then no change happened, shell script executed successfully

2. # Created File variables.sh
   file content
   #!/bin/bash
    name="Gaurav"
    role="DevOps Engineer"
    
    echo "Hello, I am $name and I am working as a $role;"

   # If we print the statement with variable in double quotes (echo "") then the variables value executes successfully
   # If we print the statement with variables in single quotes (echo "") then the variables value prints as a simple text ($name stays $name)

3. # Created greet.sh file
   file content
   #!/bin/bash
    echo "Enter Your Name"
    read Name
    echo "Enter Your Favourite Tool"
    read Tool
    echo "Which Tool You Have to Install"
    read InstallTool
    echo "Hello $Name My Favourite Tool is $Tool, Installing $InstallTool..."
    sudo apt install $InstallTool  -y

4. ## Create check_number.sh file
    file content
   #!/bin/bash
  echo "Enter one Number"
  read number
    if (( $(echo "$number > 0" | bc -l) )); then
           echo "Positive Number"
   elif (( $(echo "$number == 0" | bc -l) )); then
           echo "Number is Zero"
   else
           echo "Number is Negative"
   fi
   # Note:- bc -l finds the integer expression like any decimal value 28.5 etc

   ## Created file_check.sh file
     file content
   #!/bin/bash
      read -p "Enter File Name: " fileName
      
      if [ -f "$fileName" ]; then
              echo "file exists."
      
      elif [ -d "$fileName" ]; then
              echo "directory exists."
      else
              echo "File or Directory Does Not Exist"
      
      fi
   # Note: This Script Find both File & Directory

5. 


   
