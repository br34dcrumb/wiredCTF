# Medium Challenges
Hi! This file will be covering all the Medium challenges in **wiredCTF - bi0s Hardware Recruitment**
Format is **Challenge name - [Category]**

## WiFi_Hacking-1 - [WIRELESS]
1. Downloaded the file and searched for .cap extension files
2. Found that it was a capture file which can be opened on WireShark.
3. Went through the file in WireShark and found some messages being sent in 4 part.
4. Searched about EAPOL.
5. Found a David Bombal video on how to crack WiFi Passwords.
6. Went through the video and got to know about wordlist attacks.
7. Downloaded the wordlist 'rockyou.txt'
8. 
```
aircrack-ng dump_c8d020f8-aa4b-43ec-b761-b9fee3f328fb.cap-01.pcap -w /usr/share/wordlists/Hob0Rules/wordlists/rockyou.txt
```
9. Got the flag in the process.

## I2C_F0R_LYF - [OFFLINE HARDWARE]
1. Searched how to connect two arduino boards for I2C communication.
2. Connected the SDA and SCL pins of both the boards.
3. Connected the 5V pins of both the arduinos.
4. Connected the SDA and SCL of the master to CH0 and CH1 of the logic analyser.
5. Started Salae Logic Analyser and got the message.
6. Decrypted it using I2C 8bit analyser.

## uPy_flag - [OFFLINE HARDWARE]
1. Searched about micropython code extraction from ESP8266.
2. Found about esptool.py and how to extract python code using it.
```
esptool.py -p PORT -b 115200 read_flash 0 0x400000 flash.bin
```
3. Did not work, I don't know why
4. Started to find other tools which worked in a similar way.
5. Got ESPlorer tool.
6. Connected the board and connected to it on baud rate 115200.
7. Sent the command 
```
print(flag)
```
8. Got the flag.

#### End of Medium Challenges
