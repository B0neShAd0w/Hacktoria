<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Rabbit Hole
![rabbit-hole-cover-600x600](https://user-images.githubusercontent.com/117080369/207818904-a312292c-011c-4027-8971-7f05e0321245.png)

### Difficulty: Insane

### Mission Briefing:
Greetings Special Agent K. Today we have a special Contract. At the time of writing, 06.12.2022 at 19:48 EET, Hacktoria is now one year old. The first ever Monthly Capture the Flag event was announced roughly one year ago, between 06 and 15.12.2021. Meaning this was the week that the idea for “Story Driven OSINT Capture the Flag Exercises” was born.

To thank everyone who’s been a part of this journey and celebrate the birthday of Hacktoria, I present you with the “Rabbit Hole” Contract. The name stems from the OSINT term “Rabbit Hole”, where the investigator chases after suspected leads and clues, not knowing if or where they will end. Or… If they’re even real.

This Contract will take you through almost all disciplines covered in Hacktoria events and Contracts so far, with the inclusion of some new concepts as well. Only limited by the exclusion of steps that would be too fragile to stay online permanently. For example, the art gallery in the Mona Lisa Heist, would be too unpredictable for a permanent Contract. As a guideline, I can say this Contract is comprised of 10 steps in total. Various steps will hint to where you are, using the step number in filenames.

With the first step for this Contract, I present you the first ever complete archived screenshot of the Hacktoria website. Made on 15.12.2021 at 14:04:04. I hope you enjoy this Contract, and all those to come in the future. Thank you for being part of this.

As always, Special Agent K. The Contract is yours, if you choose to accept.

---

Password instruction flagfile:

Species from step 03
Social handle from step 06
Username from step 08
Country and Streetname from step 10
Example password:

galeocerdo-cuvier-dodgy_malaka08-logmein-germany-hamburger-d-strasse

---

#### ⚠️ *Due to the length of this writeup I am NOT including the dead ends and rabbit holes I encountered on my way to complete this contract, only the steps required to solve this incredibly fun and difficult contract.*

##### *Note: Do not overlook the obvious - avoid Rabbit Holes...* 🐰


### Step 01:
We are supplied an image of an archived screenshot with very little else to go on.

![step-01-rabbit-hole](https://user-images.githubusercontent.com/117080369/207823141-1872b9ab-0e0d-48cf-b89b-68e31c4f5740.jpg)

Looking through the image very carefully we can see some text at the very bottom of the page that points us to a Step 02 file.

![Screenshot 2022-12-15 094259](https://user-images.githubusercontent.com/117080369/207826386-8d42d824-f0fc-4e28-b080-3da2deff198d.png)

Let's go ahead and download the file: hacktoria.com/wp-content/contracts/items/rabbithole/dmehuf/step2.zip

### Step 02:
After extracting the the file we are presented with a files contains 3 pieces on encoded/encrypted text.

>```(9:=6 :? 2 D6?D6 6249 >@C?:?8 >2C<D E96 368:??:?8 @7 Q2 ?6H 52JQ J6E[ 2D E9:D =2DE J62C 92D D@F?565 E96 562E9 <?6== @7 2? 6C2 5:D2DEC@FD E@ E96 H6=72C6 2?5 92AA:?6DD @7 >2?<:?5 :? >2?J H2JD[ D@ E96 }6H *62C ;FDE 52H?:?8 AC@>:D6D 2? 6A@49 @7 F?A2C2==6=65 6?=:89E6?>6?E 2?5 @AA@CEF?:EJ 7@C >2?<:?5 E@ C64@FA 9:D =@DD6D DF776C65 E9C@F89 :8?@C2?46[ @C H:==7F= 2?5 56=:36C2E6 DF3DE:EFE:@? @7 >2?VD 32D6 56D:C6D 2?5 56DECF4E:G6 H:== 7@C E96 s:G:?6 (:== 2?5 !6C764E !=2? @7 v@5[ 9:D rC62E@CP (62C:=J 5C:G6]8@@8=6]4@> 92G6 E96 52JD 5C28865 3J[ H9:=6 A=@ED 2?5 4@F?E6C A=@ED 4@>A=:42E65 2?5 >F=E:A=:65 >2?VD F?D@=G23=6 AC@3=6>D] (6 92G6 H2E4965 H:E9 2 9@CC@C :>A@DD:3=6 E@ C6AC6DD[ >2?VD :?67764EF2= 2EE6>AED E@ 6IEC:42E6 9:>D6=7 7C@> E96 EC62496C@FD BF:4<D2?5D @7 5646AE:G6 Q28C66>6?EDQ 2446AE65 :? 2AA2C6?E 8@@5 72:E9[ @?=J E@ 36 CFE9=6DD=J EC2>A=65 F?56C 7@@E H96? E96:C 6G:= AFCA@D6 92D 366? 249:6G65]```

Let's head over to <a href="https://www.dcode.fr/cipher-identifier">dCode cipher identifier</a> and paste in the text and hit the Analyze button.

Results show a high probability of being a `ROT-47` cipher 

![Screenshot 2022-12-15 100605](https://user-images.githubusercontent.com/117080369/207831396-5a798260-2831-488e-aa81-85319a334604.png)

Let's decode with `ROT-47` and see what we get.

Oh, that is interesting, there is part of a URL, we are on to something here...

![Screenshot 2022-12-15 101003](https://user-images.githubusercontent.com/117080369/207832193-3020c37b-3915-41ed-a49a-27fb2070bb9e.png)

Let's move on to the 2nd piece of text.

>```V2h5IGRvIHdlIHNheSB0aGUgdGlkZSBoYXMgbm93IHR1cm5lZD8gQmVjYXVzZSBhbGwgbWFua2luZCBlbnNsYXZlZCBvciBzdGlsbCBjYXBhYmxlIG9mIHJlY292ZXJpbmcgdGhlaXIgbG9zdCBoZXJpdGFnZSBvZiBmcmVlZG9tIGJlZ2luIHRvIHNlZSBmb3IgdGhlbXNlbHZlcyB0aGUgZW5vcm1pdHkgb2YgdGhlaXIgZm9sbHkgaW4gdHJhbnNncmVzc2luZyBsYXdzIGFsbC1wb3dlcmZ1bCB0byBwcm9tb3RlIHRoZWlyIHBlcnNvbmFsIHByb2dyZXNzIGFuZCBjb25zZXF1ZW50IHBvc3Nlc3Npb24gb2YgYWxsIHRoZXkgbW9zdCBlYXJuZXN0bHkgbmVlZCBhbmQgZGVzaXJlISBXaGVuIHdpbGwgTWFuIGNlYXNlIGhpcyByaWRpY3Vsb3VzIGF0dGVtcHRzIHRvIG9ic3RydWN0IHRoZSBvcmRlcmx5IHByb2Nlc3NlcyBvZiBwcm9ncmVzc2l2ZSBkZXZlbG9wbWVudCBhcyBzZXQgaW4gbW90aW9uIGF0IHRoZSBjb21tZW5jZW1lbnQgb2YgaGlzIHNvam91cm4gb24gdGhlIHBsYW5ldCBTaGFuPyBUaGUgYW5zd2VyIGlzIGFic3VyZGx5IHNpbXBsZSEgL2RyaXZlL2ZvbGRlcnMgV2hlbiBoZSBhY2tub3dsZWRnZXMgdG8gaGltc2VsZiB0aGF0IGhpcyBwdW55IGJyYWluIGFuZCB1bnJ1bHkgaW1wdWxzZXMgY29uc3RpdHV0ZSBubyByZWxpYWJsZSBndWlkZSB0byB0aGUgYWNxdWlzaXRpb24gb2YgdGhvc2UgdGFuZ2libGUgYW5kIGludGFuZ2libGUgYXNzZXRzIHdpdGhvdXQgd2hpY2ggaGUgY2Fubm90IGhvcGUgdG8gZXNjYXBlIGEgbW9zdCB0ZXJyaWZ5aW5nIGZhdGUhIE1pZ2h0IHdlLCB3aG9tIHlvdSBoYXZlIG5hbWVkICJTcGFjZSBNZW4sIiBzaGFyZSB3aXRoIHlvdSB0aGUgYWN0dWFsLCBwcm92YWJsZSBmYWN0cyB3ZSBoYXZlIGJlZW4gYWJsZSB0byBkaXNjb3ZlciBieSBleHBlcmltZW50IGFuZCBleHBlcmllbmNlIGluIHRha2luZyBwcmVjaXNlbHkgdGhlIG9wcG9zaXRlIGNvdXJzZSBvZiBhY3Rpb24gdG8gdGhhdCBmb2xsb3dlZCBieSB0aGUgbWFqb3JpdHkgb2YgZWFydGggZHdlbGxlcnM/```

Head back to <a href="https://www.dcode.fr/cipher-identifier">dCode cipher identifier</a> and paste in the 2nd piece text and hit the Analyze button.

Results show a high probability of being a `Base64` coding

![Screenshot 2022-12-15 101525](https://user-images.githubusercontent.com/117080369/207833308-14f55ef1-ad39-4659-a525-a310b9061b45.png)

Let's decode with `Base64` and see what we get.

Agian, there is another part of a URL.

![Screenshot 2022-12-15 101953](https://user-images.githubusercontent.com/117080369/207834245-6b1ebbaf-d2fe-4b10-b6d5-d57f184e17b2.png)

Let's move on to the 3rd piece of text.

>```IFRGOIDPNBTSA2TVNZTSAZ3VOJSXEIDVNZUXEIDPOJZGCIDBNB5HEZLCNBTCAZLOMZ2SA3THM5ZHUY3HMYQHU3TROIQG63BAOZQXA3TIM53GE2DGEBXXE6LWOJUXEZLGEB3GCICROZUXMYLSEBLGCZ3SPF4XM5DSMFYHELBAJJ3GM4LCPIQG4YLREBIGK4TOM53GS4RAKZQXI4TBNB3GO3BAM5RCA3TZOZ2GCIDHOVZHMZJAPF3GS4TGEBVHMZ3VEBTXK5TGEBTGQY3FOJ5HEIDHMV3GQ6TJOZSW4Z3SEBXWQZZAM5RCA2TVNZTSA3TJNZ3HSPZALJXGC6DWMFYSA5TBEB2HEYLSMVXHSIDKMJUHS4JAOVXGS4RAMFRGC4RAMJZSAZ3VOJ5CCICHOVZHMZJAONXGO4RAOZTCA3TZPEQGOYTCEBVHE6LZEB4GCYTKMEQGOYRANRRGQIJAIZ2W46LZEBVHEIDGOVXGK4RAM52W4ZZAONXGO4R7EBAUEIJAKZTSA5TGEBRGQZJANZUWE2TSOEQHMYLHOJQWO5TCMEQGOYRANZYGI2DOOZQWOIDMMJUCA2TWM52SAZ3VOIQGK4TGNB4WOZRAMJXWO3TWMFZHCIDHOVSWE2DUOUQGO5LSEBYGEYLGOZTGO4TBM4QG4YLREBRXEZLGOZTGO4TBM4QGQZTSEB3GCIDOEBYGEYLGM5SWQ4DHOZUXEIDKNZWCAYTTEBTXK4RANFZGK3BAONRGK4DSMYQGYYTIEB2W42LSEBUGM4TREBTWEIDROJTGOZLCNQQHE2LSMVWGO5LWMF2CA5DCMJYSA3TBOEQG64TONBTXM43IPEQG4YLREBQWE2RAOZQWM3TBOJ4WYIDDPFXGCIDHMIQHE6TDPFRGYIDHMIQHAYT2PJ3GOIDGNB3HA5TROIQGEYJANYQHI6LCN5XHSIDGOBXHS4RBEBBGQZJAOVRHU4TGEBXGK4RAN5UHM6LHEBTWEIDDMVRGS5TROIQHAYT2ONRGKZ3GEBSGQ5THOIQG64TMMJQXCIDMMJUGKIDRMVZG46TGEBRHGIDZNBVWQZLMEBUGC3THM5XHMYLON54XEIJAI52XE5TFEBYG4ZLSEB3GMIDOEBYXE6LWOR2WOLBAONRGKIDHOVZGK4RAOZTCAYLCEBYWK2DRORZGK3BBEBJGCZ3SMVTW45TBOZQXIIDUNBZGMZ3GEB3GMIDFMJXW64TREBRHGIDOPF4SA5THMYQGGZLCN54XE6TGEBTG42LSEBTXK4RAMN4XE3TGNBSXEIDCOMQHC4TJOZTHMYLUEBZWK4TGOUQGG6LOMFTCA43CMUQGO5LSOZSSA4TBO5RGY6TSMFTS4IBIKYQHU5TUOVTSA3TROEQGO5LSNQQHEYLHOJSSA5TBM5RCA3TZPEQGM2DQOUQGG6LOMFTCA2TWM52SA3LSMZTSCKJAF4YU4T3VKBGTCTTZIR4GUMRQGB4UQQ3VPFPVELLSNBEVKS3IKV2FESRAJZ4XSIDCNBSSA4TRNBYG4Z3WMJQW46JAONXHA5TZOZTXM4TGEBXGK4RAOJQWO5TFOJ4WYIDTMVZHELBANZQXCIDGMIQGS3TFOZZHCIDOMVZCAZ3VOIQG6ZLOMFYHK4TGEBRHGIDGM5UHC3BANZQXCIDDMVXHAZ3WOBXHSIDOMNRXS5TQNZTXMYTBEBTXK3THEBQWEIDGM5UHC4TBM4QHK3TGEBZGS4TFEBZW45TZOJYSAZ3CEBZXMYLREBRWK4TQOZTHE6LMEBTXK4RAM5WGG4RAMJZSA5TBMZTWK2DQM53GEYJAN5ZGMZZAMZUHMZ3SOEQGOYRAOV3GMIDDNZSWO5TQNB4W4ZJAN5ZGCZZANZQXCIDON53HS5THNQXCAQ3FOZTGEYLGFQQGK4TTMJSXUIDGOB2WEYTZMYWCA5TBMZTXMZ3IM5ZGMIDTMJSSAZ3VOIQHMYLGNZQXEIBINRZGMLBAOJUXEYJAOVRGMY3WM5XHSZRJEBXGK4RANBQXQYLCNJQS4ICHOVZGYIDKMJUHS4JAN5ZCA2DBMJYHA2DDOZZHCLRAKVXGS4RAM52XEZTSEBXGC4JAOZQWC2D2OJSW433ZOIQGEZ3VOJSSAITKMJQXC4TFMYRCA4DCPJZCA3TPMJUGOIDHOVSWE2DUOUQGMYT2OIQGMYTFM4QGE4ZAPJXHI5TQH4QE63BAMFRCA6TSNZQWMIJAJJZCA5LONFZCA2TCMV4HE4JAM52XE6RAMJUGOIJAJJ2XEZLSEBYXM4JANJZCA5DSM4QGE2DFEB3GCZTHMVUHAZ3WMJQWMPZAKNSWE6RAM52XEIDGOJ4XGZTOPJZCARTCNBSXA4RANJ2XM4DVEB3GMIDONFXHM6LON54XEIDHMIQGYYTIFYQFMIDKOZ4XSIDHOJ4XSIDMMJUCA6TCMVZCAZTVMJUHS4JANRRGQIDQNZSXEIDHMIQHQYLCNIXA====```

Head back to <a href="https://www.dcode.fr/cipher-identifier">dCode cipher identifier</a> and paste in the 3rd piece text and hit the Analyze button.

Results show a high probability of being a `Base32` coding

![Screenshot 2022-12-15 102205](https://user-images.githubusercontent.com/117080369/207834699-d910798e-9c61-4169-bfae-bf3cd5219758.png)

Let's decode with `Base32` and see what we get.

![Screenshot 2022-12-15 102352](https://user-images.githubusercontent.com/117080369/207835185-e6328cc7-402a-418f-afdf-3d7e10116755.png)

Um, okay. seems we have some more work to do.

Let's copy the result and run it through the Cipher Identifier again.

Results show a high probability of being a `ROT-13` coding

![Screenshot 2022-12-15 102714](https://user-images.githubusercontent.com/117080369/207835984-f3f75768-f903-4290-92a0-765a94d83a9d.png)

Let's decode with `ROT-13` and see what we get.

![Screenshot 2022-12-15 102934](https://user-images.githubusercontent.com/117080369/207836380-76e8fa4f-e678-4687-9a85-17617a5e0597.png)

Agian, there is another part of a URL.

Putting those parts together gives us: drive.google.com/drive/folders/1ABhCZ1AlQkw200lUPhl_E-euVHXuHgEW

Let's go and see what goodies we get.

![Screenshot 2022-12-15 103441](https://user-images.githubusercontent.com/117080369/207837381-7ad2c39a-e0da-4149-9ad1-62436046e744.png)

### Step 03:

Ah, we need a password for the zip file, at least the picture of a Shark 🦈 gives us a clue.

After a quick Google Lens search tells us this is a `Reef Shark` of some sort. 

![Screenshot 2022-12-15 104033](https://user-images.githubusercontent.com/117080369/207838682-1088c2ae-ef55-42ec-a6f0-08088b3afc23.png)

From the image I can't quite make out the exact make of the shark 🦈

A quick Google Search for "rofficial names for sharks" leads us to <a href="https://www.floridamuseum.ufl.edu/discover-fish/sharks/species-profiles/">Shark species profiles identifier</a>

Entering `reef shark` into the search, gives us 4 possibilities.

![Screenshot 2022-12-15 105037](https://user-images.githubusercontent.com/117080369/207840828-fb8af880-2b11-4196-bdd4-d50b42198fa8.png)

After trying the options we find find our password: `carcharhinus-perezi` - make a note of this as it is needed for the final password.

### Step 04:

Let's load our capture file into Wireshark and start analysing it for clues.

First thing to do is sort the `Protocol` column by name, this allows us to see if there are any nuggets we can find quickly.

Scanning through the output we see a lot of interesting looking `FTP-DATA` enteries.

![Screenshot 2022-12-15 123244](https://user-images.githubusercontent.com/117080369/207860358-96e041ea-3ca9-4077-b4c4-962faddde4af.png)

Right click and select `Follow > TCP Stream` 

![Screenshot 2022-12-15 123748](https://user-images.githubusercontent.com/117080369/207861107-f4211c82-8250-45d9-9f22-6a74b5715dd3.png)

Under `Show data as` select `RAW`

![Screenshot 2022-12-15 123845](https://user-images.githubusercontent.com/117080369/207861334-1a02622d-a3df-4e20-a84f-f98f1f8a6337.png)


Click `Save as...`

![Screenshot 2022-12-15 123845](https://user-images.githubusercontent.com/117080369/207861626-f9f08853-bb2d-4e6a-bc03-b143b917153f.png)

Give the file a name (dont forget the .zip extension) and save it.

### Step 05:

After extracting the file from the previous step we are presented with a picture of a location.

![image-step-05-fkgvdgfdmw](https://user-images.githubusercontent.com/117080369/207862328-ef0bbfa8-d8e0-449d-a1f2-a585ee4daa2e.jpg)

Um, not much in this image to go on, so let's head over to <a href="https://www.aperisolve.com/">Aperi'Solve</a> and analze the image.

Bingo! we can see there is a hidden file embedded.

![Screenshot 2022-12-15 124905](https://user-images.githubusercontent.com/117080369/207863327-c2061d58-5ef1-4314-9ece-c986994f1fad.png)

Let's `DOWNLOAD FILES` and have a closer look.

The extracted steghide file contains a text file with a cryptic message:

>```We hear the former head of Hackoria / Tiberian Order's HUMINT team likes to post on social media.```

### Step 06:

From the information gained in the previous step it seems we need to go on the hunt for an former member of the team.

Lead's head over to the <a href="https://archive.org/">Wayback Machine</a> and run a search for `hactoria.com`

![Screenshot 2022-12-15 125936](https://user-images.githubusercontent.com/117080369/207865271-6f64e495-d8a3-4c33-a472-75f715a4d397.png)

Select the `Snapshot` related to `1st FEB 2022`

![Screenshot 2022-12-15 130217](https://user-images.githubusercontent.com/117080369/207865834-59898b35-8a5d-48d0-98b8-a64b1d12a0e2.png)

Looking through the archived page we find refernece to `Julia Sharpe - team leader for the HUMINT teams`

![Screenshot 2022-12-15 130506](https://user-images.githubusercontent.com/117080369/207866460-8c66e0dc-a8ba-40f6-84c2-e51565d69806.png)

Let's head over to <a href="https://twitter.com/">Twitter</a> and run a people search for `Julia Sharpe`

The one that immediately jumps out is `julia_sharpe007` becuase of the encoded text in their bio and 007 on appended to their handle - make a note of this as it is needed for the final password.

![Screenshot 2022-12-15 131613](https://user-images.githubusercontent.com/117080369/207868936-d1179ec8-c807-4722-ab1a-93e4112b19ea.png)

Taking a closer look at Julia's account confirms this is the account we are looking for due to the mention of `Special Agent K` 🐰 - The rabbit is a dead give away.

Let's grab the text:

>```NB2HI4DTHIXS62DBMNVXI33SNFQS4Y3PNUXXO4BNMNXW45DFNZ2C6Y3PNZ2HEYLDORZS62LUMVWXGL3SMFRGE2LUNBXWYZJPNJTWI53WNVZWYZRPORXW63DTFVZXIZLQFUYDOLLGM5XGW43RNJVXCLT2NFYA====```

Let's head over to <a href="https://www.dcode.fr/cipher-identifier">dCode cipher identifier</a> and paste in the text and hit the Analyze button.

Results show a high probability of being a `Base32` coding

![Screenshot 2022-12-15 133030](https://user-images.githubusercontent.com/117080369/207871614-13966c85-9c9d-4019-b292-6e42b427e215.png)

Let's decode with `Base32` and see what we get.

![Screenshot 2022-12-15 133240](https://user-images.githubusercontent.com/117080369/207872093-3167c894-6deb-4a3c-b5a7-968bdb8a2853.png)

Look's like we have a location for a zip file: https://hacktoria.com/wp-content/contracts/items/rabbithole/jgdwvmslf/tools-step-07-fgnksqjkq.zip

### Step 07:

Upon xtracting the zip file from the previous step we are presented with a bunch of python scripts. 

![Screenshot 2022-12-15 133916](https://user-images.githubusercontent.com/117080369/207873320-ce48dee9-cd86-457d-8459-7d46b5658541.png)

Let's go ahead open each of them in a text editor and read through the code for any clues.

Boom! We find an interesting entry in the `reverseShell.py` script, look's like another file location:.

![Screenshot 2022-12-15 134113](https://user-images.githubusercontent.com/117080369/207873810-86c0549d-8c4d-46e9-a475-4d7f50ebb3e1.png)

Let's go and check it out: https://drive.google.com/drive/folders/1NhNYUalh1knesoJyD4EV5ikfHscYIKkQ

![Screenshot 2022-12-15 134454](https://user-images.githubusercontent.com/117080369/207874589-8796a7f8-0a9b-4ed2-add9-0d9fd4f581fd.png)

### Step 08:

⚠️ *Configuring Virtualbox is out of scope for this write-up.*

Let's go ahead and download the `OVA` file and `password-hint` files.

Once the files have downloaded, import the OVA into Virtualbox, depending how you have your Virtualbox configured you may need to adjust the virtual machine network settings.

Fireup the VM, we can see that we are presented with a login screen but do not have the credentials.

![Screenshot 2022-12-15 140057](https://user-images.githubusercontent.com/117080369/207880121-8d085c92-2b1f-4c36-8495-9b0dc3aa1fbe.png)

Remember there was addintional file named `password-hint`, let's see what that gives us: 
>The one I always use ending in 123 and starting with a capital P..

Interesting, assumptions on what this could be can be made, however given I do not know what `the one I always use` is, we will generate our own password list.

To generate a password list I am going to be using `Parrot OS` but any Linux (or MacOS) will do, although it can be done in Windows with PowerShell etc. it isn't as user friendly a process.

We will need to install the `rockyou.txt` password file for this, so if you don't have it go ahaead and run `sudo apt update && sudo apt install wordlists`

Next you need to extract the `rockyou.txt` file, run `sudo gzip -d /usr/share/wordlists/rockyou.txt.gz`

With that done we can now generate our `password.txt` file.

Run `cat /usr/share/wordlists/rockyou.txt | grep -e '^P' | grep -e '[1][2][3]$' >> passwords.txt`

Basically what the above command is doing is outputting all enteries in the rockyou.txt file that start with an uppercase `P` and end in `123` to a new file called `passwords.txt`

Next we need a `users.txt` list, a quick Google search for `top 10 most common usernames linux` leads us <a href="https://yurisk.info/2010/06/04/top-10-usernames-used-in-ssh-brute-force/">here</a>

Let's create a `users.txt` file with the below usernames.

As we can see the hostname on the login screen we will add that, as it is very common in CTF's to use the hostname as the username.

```
zayed
mysql
info
postgres
guest	
nagios
user
oracle
admin
test
root
```

Now let's get stuck in and get access to this system. 👻

We have a number of methods available to us to gain access to this VM.

**Method 1 - Hydra:**
First we need the IP address of the target system.

Run `netdiscover` to list active IP address on the subnet - change the subnet range in the command to suit your environment.

```bash
sudo netdiscover -r 10.10.2.0/24 
```

We now have the IP address of our target system.

![Screenshot 2022-12-15 150938](https://user-images.githubusercontent.com/117080369/207896234-f0621480-79da-4283-90c0-f67c74510a83.png)

Next we will run `Nmap` to see if there are any open ports we can abuse.

```bash
nmap -sC -sV 10.0.2.5
```
Our `Nmap` scan confirms SSH is open - although there is no guarentee it is configured.

![Screenshot 2022-12-15 151346](https://user-images.githubusercontent.com/117080369/207897284-b969fb20-c749-4f74-9af7-d153b9d465fa.png)

Let's see if we can bruteforce our way in via SSH.

```bash
hydra -F -L ~/.users.txt -P ~/passwords.txt -vV 10.0.2.5 ssh -t 4
```

After a very short time Hydra gets a hit!

![Screenshot 2022-12-15 151908](https://user-images.githubusercontent.com/117080369/207898427-712cecb0-9c78-453e-9787-f13060811087.png)

**Method 2 - Metasploit:**
Launch `Metasploit` by running the command below.

```bash
msfconsole -q
```

Select the `SSH_Login Scanner`

```bash
use auxiliary/scanner/ssh/ssh_login
```

Next we need to see what options are required, run the command below.

```bash
show options
```
![Screenshot 2022-12-15 153420](https://user-images.githubusercontent.com/117080369/207902136-f7b2a223-cdfb-4d5a-8bb8-9c504a4098b5.png)

We need to set `RHOSTS`, `PASS_FILE`, `USER_FILE`, `STOP_ON_SUCCESS` & `VERBOSE` options, run the commands below.

```bash
set verbose true

set stop_on_success true

set rhosts 10.0.2.5

set pass_file /home/boneshadow/passwords.txt

set user_file /home/boneshadow/users.txt
```

Run `show options` to confirm you have set the required options.

![Screenshot 2022-12-15 154028](https://user-images.githubusercontent.com/117080369/207903662-bf5ceb0a-a991-4b15-999c-18558f09f45c.png)

Only thing left to do now is to run the module.

```bash
run
```

After a very short time Metasploit gets a hit!

![Screenshot 2022-12-15 154308](https://user-images.githubusercontent.com/117080369/207904493-6719cafb-c219-4bc1-8f0d-6240cdd224bd.png)

**Method 3 - Manual:**

Make an assumption about the password and just try each combination manually until you maybe get lucky.

Now we have gained the credentials let's SSH to the box.

```bash
ssh zayed@10.0.2.5
```
Now we need to have a snoop around for a nugget of information.

Let's have a poke around the user's home directory showing hidden files etc.

```bash
ls -lah
```

The last file that was updated is `.bash_history` - for anyone that does CTF's always look through this file.

![Screenshot 2022-12-15 155221](https://user-images.githubusercontent.com/117080369/207906573-653674e3-478f-41a9-b590-c89481ced5ce.png)

Let's see what the user have been up to - note: the command is not misspelt, `tac` is an alias for `cat`, sometimes in CTF's `cat` command is blocked.

```bash
tac .bash_history
```

We can see that a file has been created before the box was shutdown.

![Screenshot 2022-12-15 155644](https://user-images.githubusercontent.com/117080369/207907592-63b2f3b6-f9d6-40e3-a1b1-d76ded95a797.png)

Let's see what that file is all about.

```bash
ls -lah /media

tac /media/.vboxm
```

Look's like we have a link to another zip file.

![Screenshot 2022-12-15 160144](https://user-images.githubusercontent.com/117080369/207908795-c8c2db7f-4ecf-4e4c-be49-27f9519996a3.png)

Let's go ahead and download the zip file: https://hacktoria.com/wp-content/contracts/items/rabbithole/bfgiunfummjh/image-step-09-sdffwacff.zip

### Step 09:

After extracting the file from the previous step we are presented with a image of the ancient Klumgon language and a file with a name.

![step-09-image-457395345345](https://user-images.githubusercontent.com/117080369/207910181-4f65d902-8a67-4494-a91f-f69c44541b61.jpg)

If you are not familiar with decoding Klumgon check out my write-up for <a href="https://github.com/B0neShAd0w/Hacktoria/blob/main/Klumgongyn%20Returns.md">Klumgongyn Returns</a>, otherwise below is the decoded text.

>A VERSE ABOUT OUR SUBJECT…
>THE KING’S VOICE WAKED THE
>SILENT HOST WHO SLEPT BESIDE
>THE WILD SEA-COAST, AND BADE
>THE SONG OF SPEAK AND SWORD
>OVER THE BATTLE PLAIN BE HEARD.
>WHERE HEROES’ SHIELDS THE
>LOUDEST RANG, WHERE LOUDEST
>WAS THE SWORD-BLADE’S CLANG, BY
>THE SEA-SHORE AT KORMT SOUND,
>HE FELLED GUTHORM TO THE
>GROUND.
>
>AND GUTHORM’S BROTHERS TOO,
>WHO KNOW SO SKILFULLY TO
>BEND THE BOW, THE CONQUERING
>HAND MUST ALSO FEEL OF HIM, GOD
>OF THE BRIGHT STEEL, ~ THE SUN-
>GOD, WHOSE BRIGHT RAYS, THAT
>DART FLAME-LIKE, ARE SWORDS
>THAT PIERCE THE HEART.
>WELL I REMEMBER HOW THE KING
>HIM, THE BATTLE’S LIFE AND
>SPRING, O’ER THE WIDE OCEAN
>CLEARED AWAY EIRIK’S BRAVE
>SONS. THEY DURST NOT STAY, BUT
>ROUND THEIR SHIPS’ SIDES HUNG
>THEIR SHIELDS AND FLED ACROSS
>THE BLUE SEA-FIELDS

Although decoding the text doesn't give us anything useful it is an intersting read.

Let's head over to <a href="https://www.aperisolve.com/">Aperi'Solve</a> and analze the image.

We can see that there is some encoded text under the Strings section.

![Screenshot 2022-12-15 162216](https://user-images.githubusercontent.com/117080369/207913843-7baf2185-898f-4e87-9272-88ea8c62799a.png)

Let's head over to <a href="https://www.dcode.fr/cipher-identifier">dCode cipher identifier</a> and paste in the text and hit the Analyze button.

Results show a high probability of being a `Base32` cipher 

![Screenshot 2022-12-15 162451](https://user-images.githubusercontent.com/117080369/207914418-e0f62a9b-896a-4b9d-98bd-4710bbb5ffd4.png)

Let's decode with `Base32` and see what we get.

It seems we have a location for our last step. 

![Screenshot 2022-12-15 162905](https://user-images.githubusercontent.com/117080369/207915529-480189b9-39de-40e0-a7a1-2d9e2b704b73.png)

Let's go ahead and download the file: https://hacktoria.com/wp-content/contracts/items/rabbithole/dhglwerm/gj234853jsef435.zip

### Step 10:

Extracting the zip file from the previous step with the name in the `name` file.

We are presented with an image of a location, let's identify any data points that can help us geolocate it.

We can see a building with a name on it `Mariscos E Mas`, boats that look grounded and interesting pavement/road.

![image-final-step-](https://user-images.githubusercontent.com/117080369/207917444-35818942-efef-4089-94da-8eec9488b19a.jpg)

Let's head over to Google Maps and zoom out as far as possible.

Enter `"mariscos e mas"` into the search. 

Google Maps tries to search `mariscos e mas` instead, so make sure to select `mariscos e mas`

![Screenshot 2022-12-15 170130](https://user-images.githubusercontent.com/117080369/207922516-13871715-91f3-49cd-8a23-64221bd82fbb.png)

We don't get that many hit's

![Screenshot 2022-12-15 165741](https://user-images.githubusercontent.com/117080369/207921612-a9ef446c-b4eb-43f6-ba2a-8c1b151d504d.png)

Above results didn't help with locating the place in the image, however it has narrowed down the search to Mexico but given `Mariscos and Mas` translates from Spanish as Seafood and More, as they speak Spanish in Mexico I am confident this is the best place to start our search.








Extract the `flagfile-rabbit-hole.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
