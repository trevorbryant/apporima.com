---
layout: post
title: "Writeup for H@cktivityCon CTF"
author: "trevor"
categories: blog
tags: [blog]
---

These are the writeups for the challenges that I created for the 2020 [H@cktivityCon](https://www.hackerone.com/hacktivitycon) CTF by HackerOne.

## Spy vs Spy
Spy vs Spy is a simple challenge. Use `stegsolve` to see the flag on Red, Green, or Blue Plane 0.
![flag_spyvsspy.png](/assets/img/flag_spyvsspy.png "Spy vs Spy")

## Cold War
Cold war hides the flag using whitespace steganography. Use `stegsnow` without password to retrieve the flag.
![flag_coldwar.png](/assets/img/flag_coldwar.png "Cold War")

## Chess Cheater
Chess Cheater is a morse code challenge. Using [this](https://morsecode.world/international/decoder/audio-decoder-adaptive.html) site, the non-standard format flag can be retrieved.
![flag_chesscheater.png](/assets/img/flag_chesscheater.png "Chess Cheater")

## Busted
Busted is a password-protected challenge. The password is in the comment field of the image header. Use `steghide` to retrieve the flag.
![flag_busted.png](/assets/img/flag_busted.png "Busted!")

## Contracted
Contracted is a braille-focused challenge that embeds a file within the host file. There are two versions of braille: uncontracted, and contracted. Use `stegpy` to retrieve the hidden file. Translate using uncontracted braille to retrieve the flag `flag{touch_read_write}`.
![flag_contracted.png](/assets/img/flag_contracted.png "Contracted")

## Fan Theory
This challenge uses the [book cipher](https://en.wikipedia.org/wiki/Book_cipher) to select characters based on its positioning provided by the key followed by a rotation of 10 (rot10). The intent of the challenge is to go back and forth from steps one and two. This challenge was not able to be scripted, and was not well received because of that. The scrambled flag is `vbqw{feiyjyluduwqjylusetui}` and the flag is `flag{positivenegativecodes}`.

## Unsubscribe
Unsubscribe uses the technique of discreetly hiding short message in spam. Using [spammimic](https://www.spammimic.com/decode.cgi), we are able to encode or decode the messages.
![flag_unsubscribe.png](/assets/img/flag_unsubscribe.png "Unsubscribe")

## Substitute Face
Substitute Face uses the emoji cypher followed by a substitution to hide the flag. There are two ways to solve this challenge. The easier way is to decode the emojis using the [Emoji Cypher](https://emoji-cypher.netlify.app/) solution, or by converting the emojis to unicode to extract the hex strings (last two characters), and using the subtitution key `ctlbxysgjpqiwhueaovdmfknzr` to retrieve the flag.

```code
1. 👳👯👸👣👤🐡🐠👺👵👭🐠👢👪👢🐠👪👤🐡🐠👹👩👣👳👻👷👵👲👪👩👩👣👟👬👵👢👸👷👵👰👪👽

2. 
U+D83DU+DC73 U+D83DU+DC6F U+D83DU+DC78 U+D83DU+DC63 U+D83DU+DC64 U+D83DU+DC21 U+D83DU+DC20 U+D83DU+DC7A U+D83DU+DC75 U+D83DU+DC6D U+D83DU+DC20 U+D83DU+DC62 U+D83DU+DC6A U+D83DU+DC62 U+D83DU+DC20 U+D83DU+DC6A U+D83DU+DC64 U+D83DU+DC21 U+D83DU+DC20 U+D83DU+DC79 U+D83DU+DC69 U+D83DU+DC63 U+D83DU+DC73 U+D83DU+DC7B U+D83DU+DC77 U+D83DU+DC75 U+D83DU+DC72 U+D83DU+DC6A U+D83DU+DC69 U+D83DU+DC69 U+D83DU+DC63 U+D83DU+DC5F U+D83DU+DC6C U+D83DU+DC75 U+D83DU+DC62 U+D83DU+DC78 U+D83DU+DC77 U+D83DU+DC75 U+D83DU+DC70 U+D83DU+DC6A U+D83DU+DC7D

3.
73 6F 78 63 64 21 20 7A 75 6D 20 62 6A 62 20 6A 64 21 20 79 69 63 73 7B 77 75 72 6A 69 69 63 5F 6C 75 62 78 77 75 70 6A 7D

4.
soxcd! zum bjb jd! yics{wurjiic_lubxwupj}

5.
FLAG{MOZILLA_CODEMOJI}
```

## World Hotspots
World Hotspots provides the MAC address `9C:EF:D5:FB:9F:F0`. As indicated by the challenge title, the flag can be found using [Wigle.net](https://wigle.net/search#detailSearch?netid=9c%3Aef%3Ad5%3Afb%3A9f%3Af0). Now you know my neighborhood.
![flag_worldhotspots.png](/assets/img/flag_worldhotspots.png "World Hotspots")
