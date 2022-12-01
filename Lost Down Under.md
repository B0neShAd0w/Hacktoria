<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Lost Down Under
![lost-down-under-cover-600x600](https://user-images.githubusercontent.com/117080369/204875717-bc98bf32-764a-4f0d-9bcf-96743e214ec6.png)

### Difficulty: Insane

### Mission Briefing:
Greetings Special Agent K. We need your assistance in an urgent matter. Our client, the Australian Secret Intelligence Agency, ASIS for short, has requested our help to uncover a terrorist organization.

This group, who’s name is yet to be uncovered, has shown intent on bombing several locations around Australia. Their origins are confirmed to be domestic, with money coming in from Chinese non-government actors.

Several hours ago, one of our Red Teams was able to breach one of the terrorist groups’ email accounts. There was a single email, containing a cryptic looking text and a total of seven images.

We need you to figure out what these seven images and text mean. Are they connected? Is this a rabbit hole? With our current information, we have reason to believe these images are directly related to the suspected plans for bombings.

The answer from the text and images leads to the password for unlocking the flagfile. Which contains your contract card.

As always. Special Agent K, the contract is yours, if you choose to accept.

---

### Methodology:
The first step is to pull out imformation from the Mission Briefing that we feel is of importance.
* Australian Secret Intelligence Agency
* cryptic looking text

```
GEYTMIBRGE2CAOJXEAYTCMBAGEYTKIBRGA4SAMJQGUQDCMJVEAYTCNJAGEYDKIBRGEYSAMJRGAQDGMRAGEYTAIBRGE3SAMJQHEQDSOBAGEYDCIBRGE2CAMZSEA2TEIBVGMQDKNRAGU3SANJUEA2TEIBVG4QDKNRAGUYSAMZSEAYTCMBAGEYDCIBRGAYSAMJQGAQDCMJVEAZTEIBRGA4SAMJRG4QDCMBYEAYTCNRAGEYDKIBRGEZCAMJQHAQDCMBVEA4TSIBZG4QDCMJWEAYTANJAGEYTCIBRGEYCAMZSEAYTCOJAGEYDKIBRGE3CAMJQGQQDGMRAGEYTMIBRGA2CAMJQGEQDGMRAGEYDGIBRGAYSAMJRGEQDCMBYEAYTCMJAHE4SAOJXEAYTCNRAGEYDKIBRGEYSAMJRGAQDGMRAHE3SAMJRGAQDCMJVEAYTCOJAGEYDCIBRGE2CAMZSEAYTCNRAGEYTCIBTGIQDCMJXEAYTCMBAGEYDQIBRGEYSAOJZEAYTANZAGMZCAMJRGYQDCMBUEAYTAMJAGMZCAMJQGIQDCMBVEAYTAOBAGEYDCIBUGYQDGMRAHE3SAMJQGAQDCMBQEAZTEIBRGE3CAMJQGQQDCMBREAZTEIBRGAZCAMJQGUQDCMJUEAYTCNJAGEYTMIBTGIQDCMJWEAYTANBAGEYTIIBRGAYSAMJQGEQDGMRAGEYDQIBRGAYSAMJRGYQDCMJWEAYTAMJAGEYTIIBRGE2SAMZSEAYTCMJAGEYDEIBTGIQDSNZAGEYDQIBRGA4CAMZSEAYTCNJAGEYTMIBRGE2CAMJQGEQDCMBREAYTCNRAGEYTAIBZG4QDCMBZEAYTAMJAGEYTKIBTGIQDCMBVEAYTCMBAGMZCAMJRGEQDCMJUEAYTAMBAGEYDCIBRGE2CAMZSEA4TOIBRGE3CAMZSEAYTCNRAGEYDIIBRGAYSAMZSEAYTAMJAGEYTAIBRGAYCAMZSEAYTCMJAGEYDEIBTGIQDCMJWEAYTANBAGEYDCIBTGIQDCMJQEAYTCNZAGEYDSIBZHAQDCMBREAYTCNBAGEYTKIBUGYQDGMRAGEYTSIBRGAYSAMZSEAYTCOJAGEYDKIBRGA4CAMJQHAQDGMRAGEYTKIBRGE3CAOJXEAYTCNBAGEYTMIBTGIQDCMJREAYTCMRAGEYDCIBRGE2CAOJXEAYTCNRAGEYDKIBRGEYSAMJRGAQDGMRAGEYDOIBZG4QDCMJQEAYTAMZAHE3SAMJRGQQDCMJREAYTCMJAGMZCAMJRGEQDCMJQEA4TSIBRGAYSAMZSEA4TOIBRGA4CAMJQHAQDGMRAHE4CAMJRGEQDCMBZEA4TQIBRGE2SAMZSEA4TOIBRGE2CAMJQGEQDGMRAGEYDKIBRGEYCAMZSEAYTCMRAGEYDQIBZG4QDSOJAGEYDCIBUGY======
```

Let's have a go at decoding the text, it looks like a `Base` sort of string...

Let's head over to <a href="https://www.dcode.fr/cipher-identifier">Cipher Identifier</a> and paste in the text and hit the Analyze button.

We can see from the output that there are a few to try...
* Base32
* Substitution Cipher
* Shift Cipher
* Homophonic Cipher
* Multiplicative Cipher

Running `Base32` decoder on the text gives us a new coded output.

```
116 114 97 110 115 109 105 115 115 105 111 110 32 110 117 109 98 101 114 32 52 53 56 57 54 52 57 56 51 32 110 101 101 100 115 32 109 117 108 116 105 112 108 105 99 97 116 105 111 110 32 119 105 116 104 32 116 104 101 32 103 101 111 108 111 99 97 116 105 111 110 32 97 110 115 119 101 114 32 116 111 32 117 110 108 111 99 107 32 116 104 101 32 102 105 108 101 46 32 97 100 100 32 116 104 101 32 102 105 114 115 116 32 116 104 114 101 101 32 108 101 116 116 101 114 115 32 111 102 32 97 108 108 32 115 116 114 101 101 116 110 97 109 101 115 32 105 110 32 111 114 100 101 114 32 97 116 32 116 104 101 32 101 110 100 32 111 102 32 116 104 101 32 110 117 109 98 101 114 115 46 32 119 101 32 119 105 108 108 32 115 116 97 114 116 32 111 112 101 114 97 116 105 111 110 32 107 97 110 103 97 114 111 111 32 111 110 99 101 32 97 108 108 32 98 111 109 98 115 32 97 114 101 32 105 110 32 112 108 97 99 101 46
```

Running through  <a href="https://www.dcode.fr/cipher-identifier">Cipher Identifier</a> again gives a new list of possibilities to try.
* ASCII Code
* Circular Bit Shift
* EBCDIC Encoding
* RC4 Cipher
* Base64 Coding
* Base32 Encoding
* Substitution Cipher
* Shift Cipher
* Hexadecimal (Base 16)
* Homophonic Cipher
* XOR Cipher
* Huffman Coding
* LZW Compression
* Base32
* Multiplicative Cipher

Running `ASCII Code` decoder on the text gives us a result.

```
transmission number 458964983 needs multiplication with the geolocation answer to unlock the file. add the first three letters of all streetnames in order at the end of the numbers. we will start operation kangaroo once all bombs are in place.
```

Important information:
* 458964983 needs multiplication with the geolocation answer
* add the first three letters of all streetnames in order at the end of the numbers

**NOTE: I didn't do the locations in order, I worked through based on difficulty.**

Let's work through the location images now.

*Location 1:*

This one was really easy, a quick reverse image search gave me the location.

![Screenshot 2022-11-30 124121](https://user-images.githubusercontent.com/117080369/204877422-26ac532e-eec7-47f0-b180-7522b9801340.png)

Clicking on the 1st hit gave me the address, search the address in `Street View` and moving around to the other side of the building gives us confirmation of our location.

![Screenshot 2022-11-30 124002](https://user-images.githubusercontent.com/117080369/204877542-9fecfba8-e4e3-4d00-bad8-388fcc0502e1.png)

Let's make a note of the exact location: 99 Furlong Road, Cairnlea, Victoria, Australia.

*Location 2:*

This one was really easy also as the image gives us a name of a school, so let's search for `St Martin de Porres parish School, Australia` on <a href="https://www.google.co.uk/maps">Google Maps</a>

![Screenshot 2022-11-30 120459](https://user-images.githubusercontent.com/117080369/204877976-6b415f3e-1345-4bb1-ac9d-de39d5d24f84.png)

Switching to `Street View` we can verify this is the location.

![Screenshot 2022-11-30 120427](https://user-images.githubusercontent.com/117080369/204878104-5385efae-9984-4270-aee2-c68ff323920b.png)

Let's make a note of the exact location: 171 Military Road, Avondale Heights, Victoria, Australia.

*Location 4:*

This one was fairly easy to locate, we can just about make out the business name `IGA`

Given there are large trucks, I made the assumption this was either a warehouse or distribution center.

Let's start by Googling `IGA Distribution Center, Victoria, Australia` if we do not have any luck with a search this narrow we will expand it out.

The first result gives us an address.

![Screenshot 2022-11-30 121220](https://user-images.githubusercontent.com/117080369/204878778-a0c7aa73-8fc5-44a4-9b74-b9ee5e2e3d90.png)

So let's have a look in `Street View`, with a little bit of moving around we are able to find what we are looking for on the opposite side of the road.

![Screenshot 2022-11-30 122359](https://user-images.githubusercontent.com/117080369/204878900-7382c309-3d07-45c1-9e75-eb02d2fd9910.png)

Let's make a note of the exact location: 52 Fitzgerald Road, Victoria, Australia.

Um interesting, a pattern is emerging, so far 3 of the 8 locations are in Victoria...

*Location 3:*

We can make out the sign with `Vinnies` on it, let's Google `Vinnies, Australia`

![Screenshot 2022-11-30 130120](https://user-images.githubusercontent.com/117080369/204879160-c3624a20-1c20-4cc8-aee7-5f81ddf433ca.png)

Let's view More Locations and zoom in a bit on the `Melbourne area`.

![Screenshot 2022-11-30 130634](https://user-images.githubusercontent.com/117080369/204879286-06b4a39e-176e-4740-a659-685812333a3c.png)

Let's enter each one into `Street View` and try to find a match, we know that the supplied image contaings `Traffic Lights`, so any that don't have any traffic lights nearby can be skipped, after working through most of the list we find a match - Vinnies Sunshine

![Screenshot 2022-11-30 125414](https://user-images.githubusercontent.com/117080369/204879559-b96a85cf-6e62-43fd-907b-3d6e8b4b23a6.png)

Let's make a note of the exact location: 45 Dickson Street , Sunshine, Victoria, Australia.

*Location 5:*

Let's run a reverse image search, scrolling through the results we can see a house that matches the exact style, however it has a wall and not a fench, this is definately worth further investigation though.

![Screenshot 2022-11-30 150126](https://user-images.githubusercontent.com/117080369/204880074-202be04c-582e-42ca-86d5-ea0f4e686651.png)

Boom!, look's like we have a match.

![Screenshot 2022-11-30 150438](https://user-images.githubusercontent.com/117080369/204880123-ff8a4d98-4b52-4908-8f3a-716e3e48cfa8.png)

Let's make a note of the exact location: 20 Buckley Street, Essendon, Victoria, Australia.

*Location 7:*

Let's do some reverse image searching on the `Street Art/Graffiti`, the first hit has what looks like a close match to the supplied image.

![Screenshot 2022-11-30 141756](https://user-images.githubusercontent.com/117080369/204880702-0a616b3e-bfea-450c-b67c-5c8ff6e6cdd3.png)

looking at the page we see the illustrator `Tonia Composto` has tagged a location.

![Screenshot 2022-12-01 074941](https://user-images.githubusercontent.com/117080369/204996115-ba4baade-e7a7-4239-8a17-804a063d6010.png)

Looking through their page we find this:

![Screenshot 2022-12-01 075206](https://user-images.githubusercontent.com/117080369/204996497-d99f5ceb-1de7-44bb-8061-4d0ffe1831a3.png)

Let's start searching around `Thornbury` for a match, maybe we get lucky, however this might be a time consuming task, Thornbury is quite big...

![Screenshot 2022-11-30 142506](https://user-images.githubusercontent.com/117080369/204880809-d731b188-a2ad-42a2-a462-5af6ae45c7ef.png)

Let's drop into `Street View` right on top of Thornbury and have a look around.

Umm this looks interesting, we can see a Green sign with a building of a similar shape, just like the supplied image, although it is a different color. 

![Screenshot 2022-11-30 142718](https://user-images.githubusercontent.com/117080369/204881051-5f76b039-62be-4eca-babe-e0d5117bbc5d.png)

Let's have a closer look...

Oh, as we move up the building changes colour, boom! we have a match, that was a stroke of luck.

![Screenshot 2022-11-30 140724](https://user-images.githubusercontent.com/117080369/204881122-c8be28e0-514a-4f56-b755-a7aaa2869176.png)

Let's make a note of the exact location: 1 Normanby Avenue, Thornbury, Victoria, Australia.

At this point I am struggling to find the locations of images 6 & 8.

I have no luck with reverse image searches, overpass turbo queries or Google Dorking, sigh!

Let's review what information we have gathered so far, the decoded text mentions that we have to `multiply 458964983 with the geolocation answer`, this must mean we are looking for a number from something.

Marking out the locations on a map sets off a light bulb moment.

![Screenshot 2022-11-30 164409](https://user-images.githubusercontent.com/117080369/204881373-eace5194-2417-4837-a31e-7329cb4a5aa8.png)

So we have a `7` so far with two locations left to locate, this leads me to think that the options left would point to these rough locations, as with only 2 remaining locations I am going to make an assumption the numbers can only be a 0 drawn like a square, a pair of 1's, a 2 drawn like a Z or 1 7, however given that they seems to follow a sequence, I have made the assumption the search area would be based on 2 area's, if this this doesn't work we can re-evaluate and expannd our search:

![Screenshot 2022-11-30 164409-1](https://user-images.githubusercontent.com/117080369/204881533-8f5ac603-48bf-43f7-bdca-d234611c1f4d.png)

With this new information to hand let's try and locate the last 2 locations.

*Location 6:*

In `Google Maps` zooming in on the new search area reveals this isn't a huge area to search, so what do we know about the area?
* Looks like a Dual Carriageway
* With a grass central reservation

So let's zoom in more on our search area to see if we can match this criteria, seems to be only 6 roads that match this criteria, 2 of these are Routes, so I think we can skip those for now.
* Route 30
* Route 33
* Williamstown Rd
* Graham St
* Prohasky St
* Cook St

Let's have a look around via `Street View`, after a while we hit the jackpot.

![Screenshot 2022-11-30 173605](https://user-images.githubusercontent.com/117080369/204881692-92104be7-c506-41b6-9c4b-6ea3fb978bf2.png)

Let's make a note of the exact location: 314 Williamstown Road, Port Melbourne, Victoria, Australia.

*Location 8:*

We can just about make out a house number, could be either 307, 507 or 807.

Each of the houses has a different style roof, one looks like it has solar panel(s), and one has a Red and White awning type thing.

Lets try <a href="[overpass turbo (overpass-turbo.eu)](https://overpass-turbo.eu/)">overpass turbo</a> for all houses in `Richmond, Victoria` numbered `307`, if no luck we will move on to `507` then `807`.

Running the wizard and using `addr:housenumber=307` returns a handful of locations, lets view them in `Google Earth` to see if any match.

Unfortunately this did not bear any fruit - it seems that a lot of the houses havn't been `tagged`, sigh!

Okay Plan B, lets search for `Richmond, Victoria` in `Google Earth` and see if we can spot the Red and White awning style thing.

Luckily `Google Earth` displays house numbers also, so hopefully we can get lucky...

It doesn't take too long to find as we only need to looks for numbers 307, 507 & 807

![Screenshot 2022-11-30 175130](https://user-images.githubusercontent.com/117080369/204881945-aacbb596-7bf5-4528-b776-f9ca97c6cae5.png)

Lets drop into `Street View` to confirm our findings...

![Screenshot 2022-11-30 175446](https://user-images.githubusercontent.com/117080369/204881999-618cfe9a-4cf2-476b-81c3-71f601a1109d.png)

Let's make a note of the exact location: 311 Lennox Street, Richmond, Victoria, Australia.

Now we can update our location pins to get our information for the password.

![Screenshot 2022-11-30 164409-2](https://user-images.githubusercontent.com/117080369/204882128-3c50ee6d-c414-45d6-a5f5-b5e157bbd343.png)

Let's build up our password:
* Transmission number = 458964983
* Location 1 street = fur
* Location 2 street = mil
* Location 3 street = dic
* Location 4 street = fit
* Location 5 street = buc
* Location 6 street = wil
* Location 7 street = nor
* Location 8 street = len
* Geolocation number: 711

Extract the `flagfile-lost-down-under.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
