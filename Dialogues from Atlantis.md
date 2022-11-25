<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Dialogues from Atlantis
![dialogues-from-atlantis-cover-600x600](https://user-images.githubusercontent.com/117080369/203964216-1717baa0-b94f-4494-b535-aeb3cc2fa1fc.png)

### Difficulty: Easy

### Mission Briefing:
Greetings, Special Agent K. One of our clients, a wealthy art collector from Monaco, is requesting we help her find a recorded dialogue between Critias, Hermocrates, Timaeus and Soscrates.

In her quest to unravel the mysteries regarding the ancient city of Atlantis, our client wishes to gather all evidence possible as to where the location of the lost city truly is. Getting stuck a fair bit into her endeavors, she has reached out to Hacktoria to decipher a piece of text.

Our client believes this text to be of vital importance to prove the existence of Atlantis as a city. Whether it will lead directly to the discovery of the city is doubtful. Nonetheless, it’s of great importance to unravel it’s meaning.

I trust your ability to deal with ciphers and ancient dialogues in this matter. You find the text below. In the end, this will lead to another Contract Card if you manage to complete this assignment.

As always. Special Agent K, the contract is yours, if you choose to accept.

---

The link you find is the password for your flagfile (updated 23.11.2022)

---

### Methodology:
The mission briefing mentions trusting our ability to deal with ciphers and ancient dialogues, this is a big clue.

Let's see if we can decode the text.

First thing we notice is that it looks like HEX, let's run that through <a href="https://gchq.github.io/CyberChef/">CyberChef</a>
* Copy the code into the `Input` pane
* From the Operations menu select `From Hex`

![image](https://user-images.githubusercontent.com/117080369/203968062-e4a5d425-7144-47f5-b885-4921a12f150b.png)


We can see from the output that we have some more work to do in order to decode this text...

Let's head over to <a href="https://www.dcode.fr/cipher-identifier">Cipher Identifier</a> and paste in a portion of the text and hit the Analyze button.

![Screenshot 2022-11-25 105956](https://user-images.githubusercontent.com/117080369/203970354-722ccc0d-79eb-4f0c-86b3-33ab16c6f8c7.png)

We can see from the output that there are a few to try...

So let's group these, we will start with the low hanging fruit ciphers - no options required.
* ROT-47 Cipher
* UUencode

Followed by mid hanging fruit ciphers (small amount of options), if the low hanging fruit ins't successful.
* Base91 Encoding
* Substitution Cipher	
* Homophonic Cipher
* ASCII Shift Cipher

Followed by high hanging fruit ciphers (lots amount of options), if the mid hanging fruit ins't successful.
* ASCII85 Encoding
* Shift Cipher

Running ROT-47 decoder on the example text gives us a new coded output.

![Screenshot 2022-11-25 113224](https://user-images.githubusercontent.com/117080369/203976854-45f3d615-dbcd-4353-a046-30c7481d3f54.png)

Let's analyze the output again...

![Screenshot 2022-11-25 113600](https://user-images.githubusercontent.com/117080369/203977535-dddd8721-e7c4-48aa-9ccf-33cb39e031d7.png)

Let's work through the list to see what we get...
Looks like we hot the jackpot with the first one on the list - Base64.

![Screenshot 2022-11-25 114016](https://user-images.githubusercontent.com/117080369/203978245-a34e27bc-035f-4066-88a7-2be03a5d30f5.png)

Boom! we now have our decoding sequence - `Hex - ROT-47 - Base64`

We can either decode the entirety of the text using the <a href="https://www.dcode.fr/cipher-identifier">Cipher Identifier</a> site or <a href="https://gchq.github.io/CyberChef/">CyberChef</a>

With the entirety text loaded, add `From Hex`, `ROT47` and `From Base64` from the Operations menu.

![image](https://user-images.githubusercontent.com/117080369/203979633-e69f95e4-54c3-415a-8657-b64011a6748e.png)

Save the Output to a file to make it easy to read through if you wish, let's see what the decoded message has to say...

Reading through the text we notice something strange - this doesn't fit with the style of writing.

![image](https://user-images.githubusercontent.com/117080369/203982021-675703a8-48c7-464c-aea0-de8f533ca26b.png)

Reading on a bit further we find some more odd text.

![image](https://user-images.githubusercontent.com/117080369/203981082-a2a317fd-bec8-4967-b1c8-4af466a35501.png)

Putting this together gives us the password: `https://bit.ly/3Dq6rGW`

Extract the `flagfile-intergalactic-warfare.zip` with the password from the information gained above to get your contract card.
