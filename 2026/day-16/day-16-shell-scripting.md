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
   

   
