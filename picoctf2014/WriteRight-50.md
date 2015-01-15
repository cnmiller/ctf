#Write Right - 50

Located in the /home/write_right directory, write_right lets us write to an arbitrary address. Looking at the source code below, we can see that if the secret equals 0x1337beef, the program will open and return the flag. 

```
 if (secret == 0x1337beef){
        printf("Woah! You changed my secret!\n");
        printf("I guess this means you get a flag now...\n");

        f = fopen("flag.txt", "r");
        fgets(key, 32, f);
        fclose(f);
        puts(key);

        exit(0);
    } 
```

This means that we must find the address of secret. To do this, I used gdb and the command "p &secret" which returned the address for the secret variable, 0x804a03c. All that is left to do now is tell write_right to write 0x1337beef to 0x804a03c.

This returns:

```
Value written!
Woah! You changed my secret!
I guess this means you get a flag now...
arbitrary_write_is_always_right
```
