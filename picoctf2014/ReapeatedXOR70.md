#Repeated XOR - 70

To solve this problem, I used a handy little tool called xortool  https://github.com/hellman/xortool. xortool performs XOR analysis by guessing the key length based on a count of equal characters and guesses the key based on a knowledge of the most frequent characters. The code below shows the xortool command I used, as well as the output.

'''
$ xortool -x /Users/chase/Desktop/encrypted.txt -b
The most probable key lengths:
   1:   6.5%
   7:   25.5%
  14:   18.0%
  17:   3.9%
  21:   13.0%
  28:   9.9%
  35:   7.6%
  42:   6.2%
  49:   5.1%
  56:   4.2%
Key-length can be 7*n
256 possible key(s) of length 7:
K>\x97\xe2< \xd8
J?\x96\xe3=!\xd9
I<\x95\xe0>"\xda
H=\x94\xe1?#\xdb
O:\x93\xe68$\xdc
...
Found 58 plaintexts with 95.0%+ printable characters
See files filename-key.csv, filename-char_used-perc_printable.csv

'''

Looking through the output files, all of them except 32.out were binary files. Below is the contents of 32.out.

'''
your flag is: 1b72210a293170905ae740686d3d7f72313c523a

Most German messages decrypted at Bletchey were produced by one or another version of the Enigma cipher machine, but an important minority were produced by the even more complicated twelve-rotor Lorenz SZ42 on-line teleprinter cipher machine.

Five weeks before the outbreak of war, in Warsaw, Poland's Cipher Bureau revealed its achievements in breaking Enigma to astonished French and British personnel. The British used the Poles' information and techniques, and the Enigma clone sent to them in August 1939, which greatly increased their (previously very limited) success in decrypting Enigma messages.

The bombe was an electromechanical device whose function was to discover some of the daily settings of the Enigma machines on the various German military networks. Its pioneering design was developed by Alan Turing (with an important contribution from Gordon Welchman) and the machine was engineered by Harold 'Doc' Keen of the British Tabulating Machine Company. Each machine was about 7 feet (2.1 m) high and wide, 2 feet (0.61 m) deep and weighed about a ton.

At its peak, GC&CS was reading approximately 4000 messages per day. As a hedge against enemy attack most bombes were dispersed to installations at Adstock and Wavendon (both later supplanted by installations at Stanmore and Eastcote) and Gayhurst.
'''