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

#### ⚠️ Disclaimer: Due to the length of this writeup I am NOT including the dead ends and rabbit holes I encountered on my way to complete this contract, only the steps required to solve this incredibly fun contract.

#### *Note: Do not overlook the obvious - avoid Rabbit Holes...*


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







### Step 04:


### Step 05:


### Step 06:


### Step 07:


### Step 08:


### Step 09:


### Step 10:


# WIP

Extract the `flagfile-rabbit-hole.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
