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

Let's have a go at decoding the text, it looks like a Base sort of string...

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

Let's work through the location images now.

Location 1:
This one was really easy, a quick reverse image search gave me the location.

![Screenshot 2022-11-30 124121](https://user-images.githubusercontent.com/117080369/204877422-26ac532e-eec7-47f0-b180-7522b9801340.png)

Clicking on the 1st hit gave me the address, search the address in Street View and moving around to the other side of the building gives us confirmation of our location.

![Screenshot 2022-11-30 124002](https://user-images.githubusercontent.com/117080369/204877542-9fecfba8-e4e3-4d00-bad8-388fcc0502e1.png)

Let's make a note of the exact location: 99 Furlong Road, Cairnlea, Victoria, Australia.

Location 2:
This is the easiest as the image gives us a name of a schol, so let's search for `St Martin de Porres parish School, Australia` on <a href="https://www.google.co.uk/maps">Google Maps</a>

![Screenshot 2022-11-30 120459](https://user-images.githubusercontent.com/117080369/204877976-6b415f3e-1345-4bb1-ac9d-de39d5d24f84.png)

Switching to `Street View` we can verify this is the location.

![Screenshot 2022-11-30 120427](https://user-images.githubusercontent.com/117080369/204878104-5385efae-9984-4270-aee2-c68ff323920b.png)

Let's make a note of the exact location: 171 Military Road, Avondale Heights, Victoria, Australia.

Location 4:
This one was fairly easy to locate, we can just about make out the business name `IGA`

Given there are large trucks I made the assumption this was either a warehouse or distribution center.

Let' start by Googling `IGA Distribution Center, Victoria, Australia` if we do not have any luck with a search this narrow we will expand it out.

The first result gives us an address.

![Screenshot 2022-11-30 121220](https://user-images.githubusercontent.com/117080369/204878778-a0c7aa73-8fc5-44a4-9b74-b9ee5e2e3d90.png)

So let's have a look in Street View, with a little bit of moving around we are able to find what we are looking for on the opposite side of the road.

![Screenshot 2022-11-30 122359](https://user-images.githubusercontent.com/117080369/204878900-7382c309-3d07-45c1-9e75-eb02d2fd9910.png)

Let's make a note of the exact location: 52 Fitzgerald Road, Victoria, Australia.

Um interesting, a pattern is emerging, so far 2 of the 8 locations have been in Victoria...













Extract the `flagfile-lost-down-under.zip` with the password from the information gained above to get your contract card.
