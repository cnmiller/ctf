#Supercow - 40

For this problem,  we are given a untility that prints .cow files. It is located in the /home/daedalus directory along with the files:

* flag.txt
* hint.cow
* secret1.cow
* secret2.cow

Running supercow reveals that we need to give it a cow file as input. Feeding it hint.cow reveals a cute cow picture. Attemping to feed the program flag.txt tells us that the file must end in .cow. 

To solve this, I created symbolic links to supercow and flag.txt. Inorder to bypass the .cow extension check, I named the flag.txt symbolic link flag.cow. 

Feeding flag.cow into the supercow utility reveals the flag (as seen below).

< cows_drive_mooooving_vans >
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||