<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: The Archive
![cover-the-archive-600x600](https://user-images.githubusercontent.com/117080369/208250839-09efe280-cb3f-4d20-8057-fa16a9d518ba.png)

### Difficulty: Hard

### Mission Briefing:
Greetings Special Agent K. As you might know, the end of the year is always signified with a massive uptick in cyber attacks. Particularly DDoS and Ransomware attacks are commonplace during this time of the year. It’s also the time of the year for agencies worldwide, to crack down on the criminal enterprises destroying the downtime of IT personnel everywhere.

Our good friends over at the FBI have done just that. Yesterday morning around 0400 UTC they were able to seize a warehouse full of C2 servers, crypto miners and an entire scam call-center rolled int one.

During this bust, several laptops of key individuals were confiscated. There was however one laptop of which the owner was able to wipe the disk, right as the raid was happening. The FBI was able to recover most of the files, but is left puzzled at several of them.

You might already feel this one coming. One of these archives was sent our way to be investigated. Find out what you can about the file inside the archive. It seems to have been damaged beyond the point of recovery, but the FBI has hopes our best and brightest can uncover something.

As always, Special Agent K. The contract is yours, if you choose to accept.

---

The password starts with “flag-“

MD5 Checksum for The Archive: 2625ae7c180080e580551347831362d7

---

### Methodology:
On this occasion the mission briefing doesn't really contain any pearls of wisdom for us to go on.

All we have is the downloaded `Archive zip file`

Upon extracting the `Archive` we are presented with an odd file named `psvoxkwo8mm`, with no file extension.

Open the file in a text editor, and search <a href="https://en.wikipedia.org/wiki/List_of_file_signatures">here</a> for the first 6 characters, this tells us the file should be a `.webp` file.

![Screenshot 2022-12-17 161653](https://user-images.githubusercontent.com/117080369/208251348-457958ce-0c9e-43e6-847b-f7ebe61b4871.png)

Let's go ahead and convert this file to the correct format, head over to <a href="https://tomeko.net/online_tools/hex_to_file.php?lang=en">tomeko.net</a>

Paste in the `HEX` from the file, enter a file name to save as and click `Convert`

![Screenshot 2022-12-17 162608](https://user-images.githubusercontent.com/117080369/208251688-9e37e865-dffd-485c-b251-c655fd4c78d8.png)

We are now presented with a lovely image of Rick Astley.

![myfile](https://user-images.githubusercontent.com/117080369/208251756-08552f80-f29d-4a9a-88e3-dbba8326cbe2.png)

### ⚠️ WARNING: At this point I went off way down the rabbit hole...

![rabbit-hole-alice-in-wonderland](https://user-images.githubusercontent.com/117080369/208251928-f65973f5-9616-468c-9bd9-031340f8d774.gif)

After spending the evening with Rick and stalking him on YouTube and everywhere else I had a reverse image search result for, I moved onto a different avenue, to be honest at this point I really couldn't cope with anymore Rickrolling...

![rick-astley-never-gonna-give-you-up](https://user-images.githubusercontent.com/117080369/208252123-b4b8b0c1-7ac2-4f9a-8aa3-dfe4c62561c6.gif)

That just can't be un-seen!

After trying every Steganography tool known to human kind (and other kind) I exhausted that avenue of investigation, re-think and re-group time...

Okay let's get brutal, from the Mission Briefing it mentioned that the password starts with `flag-`, I created a custom Rockyou.txt file prefixed with `flag-` and tried to brute-force the flag file with both `Fcrackzip` & `John` without any success, to be honest I wasn't really expecting to.

Let's try a bunch of passwords manually based on the information we found while stalking Rick, just in-case we get lucky.

![depositphotos_54225809_s-2015](https://user-images.githubusercontent.com/117080369/208252373-93c61673-49a1-4061-921f-01b5cc67b148.jpg)

At this point I decided to give up for the night, as this wasn't going anywhere.

New day, fresh start and fueled with numerous double Espresso's it is time to crack this bit%! wide open.

![maxresdefault](https://user-images.githubusercontent.com/117080369/208252684-8cba3dc9-ed0a-4680-9272-2855f62eb93e.jpg)

Yeah! that went well..

After yet more road blocks, the assumption was made that the key has to be the / or in the odd file before it is converted.

Eventually we stumble upon a promising lead after decoding the name of the file.

After analyzing the the file name `psvoxkwo8mm` in <a href="https://www.dcode.fr/cipher-identifier">Cipher Identifier</a> we find that the `Affine Cipher` returns a human readable string (although this doesnt' really mean much, currently).

![Screenshot 2022-12-17 170146](https://user-images.githubusercontent.com/117080369/208253161-f0313dc6-9be4-4509-91ff-84981f1a17dc.png)

After looking through the other possible ciphers from the results, we see that again we have a human readable string from the `Disk/Wheel Cipher`, same word, just with a different character, we must be on to something here...

![Screenshot 2022-12-17 170459](https://user-images.githubusercontent.com/117080369/208253155-5326ae0a-4372-46d8-b738-1478052f745c.png)

Okay let's see if this really does mean anything.

Why don't we try a manual shift and see if anything interesting happens.

Running the `Unicode Shift Cipher` with a `Shift` of `10` gives us another interesting result, is this a URL?

![Screenshot 2022-12-17 154723](https://user-images.githubusercontent.com/117080369/208253295-968261c8-607c-49d0-a9a6-63139eb60372.png)

Smashing `https://filename.cc` into a browser downloads a zip file.

Within this downloaded zip is a file named `password-the-archive` containing the password for the flagfile.

![giphy](https://user-images.githubusercontent.com/117080369/208253533-6820b9f6-a3e2-4948-a955-67ccf32a3ac4.gif)

Extract the `flagfile-the-archive.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
