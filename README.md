### silly-cipher
A command line encoder-decoder

Written by Chris Wilson



new cli usage -
``````
silly-cipher <path/to/dictionary> <inputfile[.txt.enc]> <key[number]>

e.g $ silly-cipher charChar.txt example.txt 50

will encode example.txt outputting example.txt.enc using the dictionary from charChar.txt and an offset of 50

$ silly-cipher charChar.txt example.txt.enc 50 will decode the coded file and output example.txt

the key must be a positive integer

``````
- The program will auto-detect if the given dictionary substitutes all numeric or alphanumeric

- Program will encode or decode depending on the fileName extension (.txt 2nd argument will encode, .txt.enc 2nd argument will decode)

-  A dictionary must consist of exactly 97 character substitutions

- The dictionary  must contain ***all*** of the following characters for substitution
 
abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!@£$%^&*()-_=+[]{};:'"\|,.<>/?`~§±1234567890

- The dictionary e.g.(charChar.txt) must have ***exactly*** 97 lines each following the following format:- character,(space)[integer or character]

- integers must be in the range 0-99

- all substitutions must be unique

example encoding .txt files can be found here [charChar.txt](https://gist.github.com/Chris-Mark-Wilson/e065bcb072c38a2105c8c38859253667) and here [charNum.txt](https://gist.github.com/Chris-Mark-Wilson/fb140f2312119b1aa59b9a29a4240536)
