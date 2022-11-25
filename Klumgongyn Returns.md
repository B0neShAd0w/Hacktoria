<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Klumgongyn Returns
![klumgongyn-returns-cover-600x600](https://user-images.githubusercontent.com/117080369/204011746-576f7582-5cc2-44cd-8352-0f619c5a5e43.png)

### Difficulty: Medium

### Mission Briefing:
Greetings Special Agent K. We have a very special assignment for you today. You might remember our old friend Klumgongyn. He’s recently turned up again and will be cooperating with us going forward. In what capacity that collaboration is, I cannot say right now.

All I can tell you, that below you’ll find a text written in ancient Klumgon. It’s up to you to translate the text, which will help you uncover the password for your flagfile as well.

Everything else will become clear upon translating the text.

As always. Special Agent K, the contract is yours, if you choose to accept.

---

![image](https://user-images.githubusercontent.com/117080369/204021634-fc0a10b3-5561-413a-9040-0f94d6d1fc02.png)

### Methodology:
The first step is to try and identify some low hanging fruit.
* The most obvious characters are the a `dot` or `comma` or `apostrophe`
* Three letter words with an `apostrophe` are most likely to be `It's` or `I've`
* Sinlge letter words are most likely to be `a` or `I`
* 2 words with 2 letter together are likely to be `it is`

Once we have made a dent in the low hanging fruit, let's move on to the mid hanging fruit.

Common greetings (assuming we are translating to English):
* Hi
* Hey
* Dear
* Hello
* Howdy
* Greetings

Common 6 character words with a 2 consecutive double letters:
* Coffee
* Toffee

Now we have a plan let's start decrypting the text.

It's =
![image](https://user-images.githubusercontent.com/117080369/204021298-8cfcc078-eb18-4eb6-a795-92c4fcdd2f25.png)

I've =
![image](https://user-images.githubusercontent.com/117080369/204021459-a5dbd4d4-5011-4ca4-85fb-496945d22c51.png)

it is =
![image](https://user-images.githubusercontent.com/117080369/204021180-878f5195-4976-46c8-90f9-2c876ffd2519.png)

Just by grabbing the low hanging fruit we are able to make good progress.

![image](https://user-images.githubusercontent.com/117080369/204022345-1b4506e1-11b4-44d4-b6bc-d0754b544f67.png)

Looking at the greeting it seems to have 6 characters, could be a mispelt greeting! however we know it contains an `E` based on our deciphered text so far!

![Screenshot 2022-11-25 161937](https://user-images.githubusercontent.com/117080369/204024331-49ff3ade-e950-4517-bc7f-36cf74ea6b5b.png)

The only greeting with an `E` in that location that could fit is `Hello`, so let's make that assumption for now, we can always change it later if required.

Let's add those characters to our decipher chart.

![image](https://user-images.githubusercontent.com/117080369/204024641-59d350c5-cb58-4cfa-8413-b7459280da0e.png)

Work through the text one line at a time, building up our alphabet as we go.

Klumgon alphabet:

![image](https://user-images.githubusercontent.com/117080369/204028750-3a4cabf9-2201-4ae1-ba5e-2a2e159fbb8c.png)

See the fully deciphered text below.

```
Hello special agent. It’s nice to see you again. Thanks for
saving my life earlier this year, that was quite the
Adventure. Ever since getting off your planet, I’ve missed
this place greatly. Even though your kind can be cruel,
strange and violent, it provides a wonderful home filled
with hope for the future.

It is therefore that I’ve decided to join your planet of
hairless apes. After consulting with the overseer. We have
reached an agreement that I will become your new councel
leader. Meaning there is now a direct link between the
Klumongyn and earthlings. Making both our positions in the
galaxies much stronger. Mostly yours, since we are
absolute lightyears ahead of your steampunk technology
and “micro” chips.

I am also pleased to learn that you are still the top
special agent. This task is designed to identify if you are
truly “the one”. Upon completion, you shall receive the
files to use the ancient Klumgon language. It was written
by Xyntolyr, one of the first elders of our only tribe at
the time.

Our language was founded 105783 years ago! this makes it 
very young in the grand scheme of things, but still quite an
ancient text. Made long before your early hairless space
mice lived in what is now Zimbabwe.

Good luck special agent, it’s an honor working besides you
again.

I would say, live long and prosper. But given your
lifespan…

Live fast and die young!

Password…

j!fqw'eu!itn!vx,cm'qw!re'ir,jl!d
```

Extract the `flagfile-klumgongyn-returns.zip` with the password from the information gained above to get your contract card.
