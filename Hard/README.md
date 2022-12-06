# Hard Challenges
Hi! This file will be covering all the Hard challenges in **wiredCTF - bi0s Hardware Recruitment**
Format is **Challenge name - [Category]**

## circuit_reversing - [OFFLINE HARDWARE]
1. Made the connections given on Tinkercad.
2. Tried several combinations to make the LED glow.
3. Found out the combination and used it on the Offline board present there.
4. Got the flag.

## L3D_Tr4c3R - [OFFLINE HARDWARE]
1. Made the connections and flashed the code to make a pattern.
2. The flag was given to me after the connections were checked.

## da_0n3_wh3r3_u_v1su4l1s3 - [MISC]
1. Opened the code on text editor and made a guess that it was a hex file.
2. Uploaded the file on hexed.it
3. Checked the header and seearched about JFIF headers.
4. Got to know that it was the header of a JPEG file.
5. Changed the extension to .jpg.
6. Got the flag.

## xoring - [REVERSING]
1. Read about XOR function and learned that.
```
x ^ 0 = x
x ^ y = z
x ^ z = y
y ^ z = x
```
2. As the first 5 letters were \x00 = 0
3. I tried to xor it with "wired" and got wired as the result.
4. As the flag is in the format wired{flag} so used 'wired{' for xoring got wiredw as the result.
5. Guessed that it was wired being repeated.
6. Used "wiredwiredwiredwired" for xoring.
7. Got the flag as the result.

#### End of Hard Challenges.
