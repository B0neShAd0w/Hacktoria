![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# A Christmas Conspiracy
![gigachad-evil-elf-600x600](https://user-images.githubusercontent.com/117080369/210732986-abc33d46-332a-4182-92fd-57c8053f3fe8.png)

$~$
---

### $\color{magenta}{COLLAB\ INFO}$
Welcome, to this collaboration Contract between <a href="https://twitter.com/infosecunited">Infosec United</a> and Hacktoria. We hope you have a wonderful Christmas and a lot of fun solving this Contract.

If you would like to collaborate with Hacktoria on making your own contract, reach out to the Overseer role in our Discord community. We’re always open to hearing new ideas, don’t be shy!

$~$

### $\color{magenta}{PROLOGUE}$
Snowy and Billy were two elves who worked in Santa’s factory on the North Pole. They had both been there for as long as they could remember, and while they enjoyed the work, they were starting to feel burnt out.

“I can’t take it anymore,” Snowy said as they walked home from the factory one evening. “The long hours, the constant pressure, it’s all just too much. We deserve better than this.”

Billy nodded in agreement. “I know what you mean,” he said. “I’m starting to feel like we’re nothing more than slaves, working ourselves to the bone just to make Santa happy.”

The two elves walked in silence for a moment, each lost in thought. Finally, Snowy spoke up.

“We have to do something about it,” he said. “We can’t just keep going on like this.”

Billy raised an eyebrow. “What do you mean?” he asked.

“I mean, we have to get rid of Santa,” Snowy said. “We have to kill him.”

Billy’s eyes widened in shock. “Are you serious?” he asked. “We can’t just go around killing people!”

“I know it’s a drastic measure,” Snowy said. “But think about it. If we get rid of Santa, we’ll be free. No more long hours, no more pressure. We can live our lives however we want.”

Billy thought about it for a moment. It was true that he was fed up with the way things were, but he wasn’t sure if murder was the answer.

“I don’t know,” he said. “It seems like a pretty risky move. What if we get caught?”

Snowy shrugged. “We won’t get caught if we do it right,” he said. “We could hire a hitman to do the job for us. They could take care of everything and make it look like an accident.”

Billy wasn’t sure what to think. On one hand, the idea of being free from Santa’s tyranny was tempting. On the other hand, he wasn’t sure if he was ready to take such a drastic step.

In the end, the two elves decided to sleep on it and think about it some more. They knew that whatever they decided, it was a decision that would change their lives forever.

$~$

### $\color{magenta}{BRIEFING}$
Greetings, Special Agent S. We have an extremely urgent matter on our hands. As you may know, Hacktoria has an Alien counsel member, we track Sasquatches all over the planet, fight Vampires and we regularly visit other planets. If all of that wasn’t bananas enough, wait until you hear about today’s assignment.

Currently in one of our safehouses, deep in the northern forests of Finnish Lapland, Santaclaus is hiding out under the protection of several of our B.T.R.U. (Borderless Tactical Response Unit) agents. The night before Christmas, the old man received intel from one of his Elves that there’s a murder being plotted against him.

For his safety, we’ve used Agent T’s likeliness to the big man to play as a double. He’s currently taken Santaclaus his place and it dropping packages across the world. Meanwhile, we are tasked with figuring out what the plan is to kill Santaclaus. Set up a trap and catch the killers as they try to execute their plan.

The head of the conspiracy is an elf named Snowy, one of Santa’s hardest working elves for years now. Snowy went rogue and conspired with several elves to hire a hitman to kill Santa.

Below you find intercepted WhatsApp messages and a picture of Snowy. Thanks to the poorly made backdoors by Zuckerberg his “security engineers”, our friends at the NSA were able to give us access quickly. US president Joe Biden personally signed off on us using the backdoor. As he forgot to send Santa the list of presents he wants, as well as the milk and cookies in the Whitehouse, he needs to be on good terms with the old man. Otherwise his kids will hate him for ruining Christmas.

As you see, this has the highest priority. We need everyone to stop working on World War 3 in Europe, the food crisis, China and North Korea. All eyes are on saving Santa from his burned out sweatshop elves.

As always, Special Agent S. The contract is yours, if you choose to accept.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$
Submit your answer to the <a href="https://twitter.com/infosecunited">Infosec United Twitter</a> account via Direct Message.

If your message does not come through, reach out to “Joey the Same” in the Hacktoria Discord server.

![Untitled](https://user-images.githubusercontent.com/117080369/210734269-869bcd83-976d-44b3-a985-69aa81e732c6.png)

$~$

---

### $\color{magenta}{METHODOLOGY}$
Reading through the Prologue and Briefing doesn't really give us to go on, however there is an encoded string in one of the captured messages:
`ZTGIS://YHW.XJGPOHX.EZM/MUD/FB/1R9NFPMZ4MN2EDU4V6W82/S?DF=0&JDKRR=V1DFD4OLLWMC6JJATXO9FGY9G`

This looks suspiciously like some sort of polyalphabetic substitution cipher.

Let's head over to <a href="https://gchq.github.io/CyberChef/">CyberChef</a> and have a crack at decoding it.

When a polyalphabetic substitution cipher is used my go to cipher is the Vigenere cipher, this seems to be a favourite amonst CTF's.

Paste the code into the Input pane and select `vigenere decode` from the Operations menu.

![image](https://user-images.githubusercontent.com/117080369/210737562-c86a5413-b8bc-433b-a2c1-cc0b06180f40.png)

Currently we do not have the required `Key` and there is no hint of what this could be from the Briefing etc. however not all is lost!\
As we can see from the format of the string it looks very much like a URL.

So let's try `https` as the key, as we can see this now gives us the actual key - `SANTA`.

![Screenshot 2023-01-05 084409](https://user-images.githubusercontent.com/117080369/210738393-cc6e3de0-8ee2-4e5a-b8b9-ca6057b4e1d5.png)

Let's change the key to `santa`, unfortunately this isn't the full key required.

![image](https://user-images.githubusercontent.com/117080369/210739074-9e74ce4c-3223-47b1-8581-ccc016d19e7a.png)

We can assume the start of the address is `www`, so let's enter that as the key, we can see that we now have more of the key - `CLA`

![Screenshot 2023-01-05 085013](https://user-images.githubusercontent.com/117080369/210739543-2442f640-f861-499d-b73f-0eee06b58758.png)

So for the key we now have `SANTACLA`, it doesn't take much to work out the full key from here.

![Screenshot 2023-01-05 085511](https://user-images.githubusercontent.com/117080369/210740480-58869efa-3d77-4d2a-b9c5-df9648ea2b7e.png)

A general rule of thumb is URL's start in lowercase, so let's convert this to lowercase, select `To Lower case` from the operations menu.

![Screenshot 2023-01-05 085841](https://user-images.githubusercontent.com/117080369/210741079-3cba7427-6e3f-434a-bf1b-2943d3d25d6b.png)

Heading over to the link we can see we have material to sift through.

![image](https://user-images.githubusercontent.com/117080369/210741563-1ae87e5c-4275-4915-8db7-5a784f1954e3.png)

We find a couple of interesting files in the `Plan to kill santa` directory.

### 1. "Plan to fuck him up.txt"

>Step 1:
>
>Go to this location -61.978900, -58.028966
>
>Step 2:
>
>Talk with the "G" to invite santa there.
>
>Step 3:
>
>Go to this location -62.291162, -59.098073
>
>Step 4:
>
>Buy poison and hot chocolate.
>
>Step 5:
>
>Get santa on the location of the picture on the folder.
>
>Step 6:
>
>Give  santa the hot chocolate.
>
>Step 7:
>
>Watch santa die slowly.
>
>Step 8:
>
>Dance, and then. kill miss clause.
>
>Step 9:
>
>Get rich with the tourist attraction on the north pole.
>
>Step 10:
>
>Open a strip club.

### 2. "Screenshot (229).png"

![y67ksXEo](https://user-images.githubusercontent.com/117080369/210743172-c7d8ad79-4258-4022-8c2c-3787ad83b7ba.png)

Let's do as the "Plan to kill santa.txt" tells us.

Searching for the location coordinates from step 1 in Google Maps takes us to `King George Island, Antarctica`

![image](https://user-images.githubusercontent.com/117080369/210743988-15c2ea45-c80e-4caa-810a-950366f42bb4.png)

Searching for the location coordinates from step 3 in Google Maps takes us to `Nelson Island, Antarctica`

![image](https://user-images.githubusercontent.com/117080369/210744442-c4448295-5281-42d3-bfed-e0f932271648.png)

Step 5 tells us to "Get santa on the location of the picture on the folder."

There are only a few locations between those 2 locations we looked at.
* Machu Picchu Base
* Carlini Base
* King Sejong Station
* Base Presidente Eduardo Frei Montalva 

Visiting each of those locations reveals the answer.

![image](https://user-images.githubusercontent.com/117080369/210746920-62b51ef3-7a8b-4f3b-a4e6-a40b4083f7d6.png)

All that is left to do is Submit our answer to the <a href="https://twitter.com/infosecunited">Infosec United Twitter</a> account via Direct Message.

$~$

📌 BoΠeShΔdϴw³
