![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# Follow the Black Rabbit
![BoeShdw3_Follow_the_black_rabbit_through_the_internet_600x600](https://user-images.githubusercontent.com/117080369/210749514-0ace8f3d-f6af-41b1-96d0-7c843aafaa33.png)

$~$
---

### $\color{magenta}{COLLAB\ INFO}$
This Collaboration Contract was made by our community member “Mr.Midnight”.
https://twitter.com/MrMidnight53

If you would like to collaborate with Hacktoria on making your own contract, reach out to the Overseer role in our Discord community. We’re always open to hearing new ideas, don’t be shy!

$~$

### $\color{magenta}{PROLOGUE}$
Last week sunday:

James layes on his bed after an exhausting day of school and a long coding session. His heart pounding like crazy. He cant fall asleep even tho its 1 in the morning. What happened to him today, was just too exciting for him not to constantly think about it. He stood up, grabbed his laptop from the desk in the hope that writing it down, will finally granting him some sleep:

diary.txt:

>Dear diary,
>
>Today is the craziest day ever. I just cant stop thinking about it. It might be the best thing happened to me since the bunny-high started.
>
>First school started off normally. The bunny-chemistry lesson however wanted us to do a presentation about “what chemicals are inside a carrot and why carrots are the >best food for our species”.
>
>I first thought that it was a stupid presentation like always but this time, we are suppost to work in groups of 2. The teacher calls our name in pairs and we are >suppost to work together. Surprisingly I was pared with the prettiest bunny in class: “Jessica”. I had a crush on her since the beginning of the school. I cant belive >that I can work along with her.
>
>This is my only chance to get her to like me…
>
>I red somewhere that there is a coffee recipe that makes someone like you…
>
>Maby ill give that a try…

Today is james birthday (Saturday). He wished for the “magic” coffee beans that he needed for the magic coffee.

Since his parents are very rich, they bought him the 1000$ coffee beans he wished for.

$~$

### $\color{magenta}{BRIEFING}$
Greetings, Special Agent X.. James called us yesterday at 9am, asking us to find out who stole his precious coffee beans. Apparently the day after he got the beans, he told his friends about it and now its missing.

We’ve located his school and found out the names and class-photo of his friends.

Your mission is to recover the stolen coffee beans, return it to james and find out who stole the precious coffee beans. Youll find further information in the folder that comes with this contract.

As always, Special Agent X. Our allies and the agency depend on you.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$
password sample for flagfile: name-of-coffee-beans-name-of-thief

sample password: midnight-og-coffee-beans-jimmy

<a href="https://hacktoria.com/wp-content/contracts/flags/flagfile-follow-the-black-rabbit.zip">Download the Flagfile</a>

<a href="https://hacktoria.com/wp-content/contracts/items/start-information-black-rabbit-2.zip">Download the starting information ZIP</a>

$~$

---

### $\color{magenta}{METHODOLOGY}$
> __Note__ There are many rabbit holes in this challenge, I am only covering the steps required to solve the challenge.

The first thing to do is extract the `start-information-black-rabbit-2.zip` file and run the `tree -a` command to see what we are dealing with.

![Screenshot 2023-01-04 100701](https://user-images.githubusercontent.com/117080369/210543415-1d4b6567-1dc6-4a78-a90f-a0e71f489311.png)

Let's start looking through the files for clues...

The first clue is provided in the `Information/suspects/unknown-note` file.

>PpppmmmfmmfmPppffpPfpmfmPppffpPfpmfmPppffpMmmmfmPppffpPpmmfmPpm2MppmfmPpmppmFfmmfmPpmppmFfmmfmPpppmmPfpmfmPppffpMffmfmPpppmmpmpmfmPppffpFfmmfmPpppmmFmfmfmPpmppmFmfmfm>PpppmmmmfmfmPppppmFfmmfmPppppmFfmmfmPpppmmmmfmfmPppppmPpmmfmPpppmmFmfmfmPpmppmFmfmfmPpppmmPpmmfmPppppmFfmmfmPppppmPfpmfmPpmppmFfmmfmPpppmmFfmmfmPpppmmpmpmfmPppppmPpmm>fmPpppmmFmfmfmPpmppmFfmmfmPpppmmPfpmfmPpmppmFfmmfmPpmffpMppmfmPppFmpmfmmfmPpmppmPfpmfmPppppmMppmfmPppMfmPfpmfmPppFmpmmfmfmPppffpmmfmfmPppFmpmmfmfmPppMpmMppmfmPppFmpPp>mmfmPpmffppmpmfmPppffpmmfmfmPppFmpPpmmfmPpmppmPfpmfmPppppmMffmfmPppMpmmmfmfmPpppmmFmfmfmPppMpmFfmmfmPppffpPfpmfmPpppmmmmfmfmPppffpPfpmfmPpmffpPfpmfmPpmffpPpmmfmPppFmp>MmmmfmPppMfmMffmfmPppppmFmfmfmPppMfmMffmfmPpp2MppmfmPpppmmMppmfmPppFmpPpmmfmPppFmpmfmmfmPppMpmMffmfmPppFmpPfpmfmPpmppmFfmmfmPppffpFfmmfmPpppmmpmpmfmPpppmmFmfmfmPppffp>mmfmfmPpm2FfmmfmPppffpFmfmfmPppffpPpmmfmPppffpMmmmfmPpm2PfpmfmPppffpPpmmfmPpppmmmfmmfmPpppmmMppmfmPppffpMffmfmPpppmmFmfmfmPppFppFfmmfmPppppmPpmmfmPpppmmpmpmfmPppppmFm>fmfmPppppmMff

Let's use <a href="https://www.dcode.fr/cipher-identifier">dCode Cipher Identifier</a> to make some sense of this.

![7912ee50df9e7d9358b02a1acfe10c2d](https://user-images.githubusercontent.com/117080369/210548199-35d74462-7736-4d7f-a1a1-74d760890f38.gif)

* Decode from `Kenny Language (Southpark)`
* Decode from `Base64 Encoding`
* Decode from `Ascii Code`

The decoded result is: https://drive.google.com/file/d/1X-jMWwWAS9wS-kGeFtgt43PKnKzaSXBT/view?usp=share_link

Having a look at the Google Drive reveals information about a Job Application for `Jeff`:

>FULL NAME: Jeff anderson\
>DATE: 30.July.2022\
>ADDRESS: 69th Bunny-lane UK\
>EMAIL: Jeffaldersonthebunny@bunnymail.com\
>POSTION APPLIED FOR: IT-security-manager\
>SSN: 1421.3425.2348\
>DESIRED PAY: 6900$ the month\
>EMPLOYMENT DESIRE: FULL-TIME
>\
>\
>HIGH SCHOOL: BUNNYHIGH-UK\
>CITY/STATE: UK/BUNNY-LANE\
>GRADUATE: YES\
>\
>COLLEGE: BUNNY-COL-UK\
>CITY/STATE: UK/COLLEGE-STREET56\
>GRATUATE: YES

The second clue is provided in the `Information/unknown-backup/etc/P455WORD` file.

>name-of-structure-contry-city\
>\
>use password for vault

We can deduce from this information that we are looking for an image of a location, let's have a look around for one.

The third clue is from the `Information/unknown-backup/root/password.png` image file.

![password](https://user-images.githubusercontent.com/117080369/210553024-9102d70f-9952-4ea5-9e59-6d4673763f12.png)

A quick Google Reverse Image search reveals that the location in the image is The Cologne Cathedral in Cologne, Germany.

With this information we can extract the `Information/unknown-backup/home/UNTITLED/vault.zip` with the password `cologne-cathedral-germany-cologne`

The extracted archive provides us with 2 files, 1 image containing an email address and a cryptic message.

![black-bunny-organization-card](https://user-images.githubusercontent.com/117080369/210554727-53966de3-00ea-4c58-99ee-d7a3018e1227.jpeg)

And a secret file, with the message:

>Black rabbit, so sleek and so sly,\
>With fur as dark as the starless night sky.\
>Your long ears twitch and your nose twitches too,\
>As you hop and bound through the dew-covered dew.\
>\
>Your eyes are bright and your paws are quick,\
>You dart and you weave through the grass so thick.\
>Your movements are graceful, your spirit is free,\
>You are the embodiment of wild and carefree.\
>\
>You are the keeper of secrets and mystery,\
>A creature of magic and history.\
>You are a symbol of strength and resilience,\
>A reminder to always embrace our difference.\
>\
>So here's to you, black rabbit, so wild and so true,\
>May you always be free to roam and do what you do.\
>\
>\
>\
>secret: blackrabbits4life-operation-coffee

Let's email `blackbunnyhideout@gmail.com` with the secret: `blackrabbits4life-operation-coffee` and see what happens!

Almost instantly an email is received back with the following information and a satellite image.

>G00d afternoon, to retrieve the coffe beans you have deposited, please proof that you are ****** by answering the following question:\
>\
>The-coordinates is the password for the beans in this vault: https://drive.google.com/file/d/158EIYAW1IJvYfNkFxUA92yeBGVN_jPbF/view?usp=sharing

![gmail](https://user-images.githubusercontent.com/117080369/210557277-3ef997be-8bcc-4ff0-a996-897a85e6b99d.png)

Let's download the vault from the Google Drive.

The clue for the vault password mentions that `The-coordinates is the password for the beans in this vault`

Reviewing the meatdata of the image will give us the coordinates for the image location.

However this is NOT the password, we need to read the message carefully and take it literally! `The-coordinates is the password`

Extract the beans.zip with `The-coordinates` as the password.

Reviewing the beans.bag file provides with another clue:

>California Gold coffee-beans\
>\
>Best magic coffee beans in the world

Now we have all the information required to unlock the flagfile (remember back to the job application we found?:
* california-gold-coffee-beans
* jeff

Extract the `flagfile-follow-the-black-rabbit.zip` with the password from the information gained above to get your contract card.

$~$

📌 BoΠeShΔdϴw³
