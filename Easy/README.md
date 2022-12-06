# Easy Challenges
Hi! This file will be covering all the Easy challenges in **wiredCTF - bi0s Hardware Recruitment**
Format is **Challenge name - [Category]**

## Dots&Dashes - [WIRELESS]
1. Downloaded the file and opened it on Audacity.
2. Trimmed the part which only had noise.
3. Saved it as a new audio file.
4. Used an online audio morse code decoder.
5. Got the flag.

## chan's favorite - [WIRELESS]
1. Downloaded the file and opened it on Audacity.
2. Could not get anything so tried changing it to Spectogram.
3. Zoomed out and saw Rick Astley.
4. Hence, got the flag.

## ~logic - [HARDWARE]
1. Downloaded the file and saw that it was logic gates.
2. Went in reverse order to get the values of A, B, C, and D.
3. Started the simulation on the link provided.
4. Put in the values of A, B, C, and  D.
5. Got the flag.

## find_thyself - [OSINT]
1. Downloaded the file.
2. Tried to open it and got an error 'Unrecognized image file format'
3. Started the terminal -->  ```file osint_chal.png```
4. Got that it is a webp image type, so changed the extension from .png to .webp
5. Opened the webp image.
6. Searched for that type of socket... didn't get anything :`)
7. Finally searched for the company name mentioned and got the country.

## grep_it - [REVERSING]
1. Downloaded the file.
2. Started the terminal and used cat on the file.
```
cat chall
```
3. Didn't get anything so tried to use strings on it.
```
strings chall
```
4. Got better output, so now tried to use strings with it.
```
strings chall | grep wired
```
5. Got the flag

## D0Z3N_IS_K3Y - [REVERSING]
1. Downloaded the file.
2. Tried to grep wired on it, didn't work
3. Tried to grep flag on it
```
strings corrected_one | grep flag
```
4.  got an encrypted text.
5. used CyberChef to bruteforce decode the text.
6. got the flag.

## Lifetimesettlement - [CRYPTO]
1. After looking at the encrypted text thought that it was binary.
2. Binary decoding didn't work.
3. Used dCode.fr to identify the type of cipher.
4. Found out that it was spoon cipher
5. Searched for online spoon decoding and found a site.
6. Got the flag after decoding.

## da_french_cipher - [CRYPTO]
1. Searched for french ciphers
2. Found vigenere cipher which uses a key. 
3. We got that vowels is the key, so used 'aeiou' as the key.
4. Decoded and got the flag.

#### End of Easy Challenges
