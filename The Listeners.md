![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# The Listeners
![the-listeners-cover-image-600x600](https://user-images.githubusercontent.com/117080369/204564489-03244eb9-d8b4-4931-ad2f-487bac1f344a.png)

### $\color{magenta}{DIFFICULTY}$
${\color{gray}EASY\ |\ MEDIUM\ |\color{white}\ HARD\ \color{gray}|\ INSANE}$

$~$
---

### $\color{magenta}{PROLOGUE}$
Jaque was in the middle of a meeting at his office when he received a phone call that would change his life forever.

The caller, a man with a rough voice, informed Jaque that his boat had been attacked while sailing off the coast of Spain. Jaque’s wife and daughter, who had been on board the yacht at the time, were nowhere to be found.

Panicked and afraid, Jaque rushed out of the meeting and headed straight to the marina where his yacht was docked. When he arrived, he saw that the boat was badly damaged and there was no sign of his wife or daughter.

Jaque immediately contacted the authorities and begged for their help in finding his loved ones. The search for his wife and daughter became the top priority for the French coast guard, and Jaque vowed to do whatever it took to bring them home safely.

Days turned into weeks, and still there was no sign of Jaque’s wife and daughter. Jaque was devastated, but he refused to give up hope. He spent every waking moment searching for any clues or leads that could help him find his family.

Finally, after nearly a month of searching, Jaque received the news he had been praying for. His wife and daughter had been found, alive and well, on a small island off the coast of Africa. They had been rescued by a group of fishermen and were now safe and sound.

$~$

### $\color{magenta}{BRIEFING}$
Good day Special Agent K, glad you could make it. One of our oldest clients, a wealthy French businessman, is requesting we find a location where a conversation between two of his rivals will take place. These two have been after our clients’ fortune for a long time, endlessly scheming to end his business endeavors. After their recent attempt to sink one of our clients’ boats off the coast of Spain, while his wife and daughter were on board, our client has had enough.

The plan is to uncover the location of their meeting and have one of our Field Agents plant a listening device. This will record the meeting and lead to the valuable information our client is looking for. Using this information our client plans to take down the businesses of both rivals.

After their businesses are destroyed, we will be called upon again to fully end their existence. Something that, given the high profile of these men, wil make Hacktoria a hefty amount of money. As well as some very good standing with the French elite.

There is a catch to this however. We don’t know where this meeting will take place. Our client was able to intercept an image of the meeting location, which will take place 3 days from now at noon. Besides this photo, we know these rivals share a common interest in luxurious lifestyles along the coastlines of Western and Southern Europe.

Using this information and the intercepted image below, it is your task to figure out exactly where this meeting will take place. Our Field Agent closest to this region will take over from there.

As always. Special Agent K, the contract is yours, if you choose to accept.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$
Use your findings to generate the password that will unlock the “flagfile”, which in turn leads to your Contract Card.

The pattern will be as follows (make sure to add a dash between every word).:

country-zipcode-fullstreet-name-number

<a href="https://hacktoria.com/wp-content/contracts/flags/flagfile-the-listeners.zip">Download Flagfile</a>

<a href="https://hacktoria.com/wp-content/uploads/2022/08/the-listeners.jpg">Download Full Size Image</a>

$~$

---

### $\color{magenta}{METHODOLOGY}$
The first step is to pull out imformation from the Mission Briefing that we feel is of importance.
* French businessman
* off the coast of Spain
* luxurious lifestyles
* coastlines of Western and Southern Europe

After examining the supplied image, 2 elements jump out at me:
* Mirror
* House design/style

Uploading the image to <a href="https://lens.google.com/">Google Lens</a> and cropping on the `mirror` reveals these Traffic Mirrors are located in France.

![Screenshot 2022-11-29 145747](https://user-images.githubusercontent.com/117080369/204566153-574640e8-2b76-49e7-b461-95508cc704fc.png)

We can do more investigation about these mirrors to confirm our findings.

This type of mirror seems to be a `TM-F French Premium traffic mirror`

![Screenshot 2022-11-29 151536](https://user-images.githubusercontent.com/117080369/204568124-1f8b54d5-45e2-498a-86db-1228456c190d.png)

With this in mind let's have a think about luxury areas of Southern/Western France - a few places spring to mind.
* Nice
* Cannes
* Monaco
* Saint-Tropez

Let's try and match the house style/design to the locations and try to mind a match.

After a fair bit of Googling and reading about the architecture of each area, the only one that seems to match is `Monaco`

Okay, we now have an area to focus in on, however that is still quite a large task, can we narrow it down further?

Let's head over to <a href="https://overpass-turbo.eu/">overpass turbo</a> and enter `Monaco` into the search area and enter `highway"="traffic_mirror"` into the Wizard.

![image](https://user-images.githubusercontent.com/117080369/204573385-3b9b6b64-1e72-463e-a19d-12701618e09a.png)

Unfortunately this does not show any `Traffic Mirrors` in Monaco, oh well it was worth a shot!

I think this means we are going to have to just have a look around Monaco in the hope we spot something...

Let's head over to <a href="https://earth.google.com/web/">Google Earth</a> and search for Monaco.

Let the map roate in `3D` until the orientation roughly matches the supplied image.

![image](https://user-images.githubusercontent.com/117080369/204575268-d9c88eed-8cdf-48c3-936b-0d054df99b3f.png)

If we look at the supplied image we can see that the house has an angled wall and isn's square, this should help narrow down our search.

![Screenshot 2022-11-29 121007-1](https://user-images.githubusercontent.com/117080369/204576217-cd6ec638-e5f6-4335-8d66-97a636d0e4ca.png)

Let's zoom in and have a look at the buildings and try to match the shape.

After a short time i think we have found a match!

![Screenshot 2022-11-29 155627](https://user-images.githubusercontent.com/117080369/204578948-db436069-509a-4d61-9579-d3bd234922d1.png)

Let's have a closer look and see what's what.

I am pretty sure we have a match, although not an exact like for like image, it's definitely close enough to be confident this is the location.

![image](https://user-images.githubusercontent.com/117080369/204579335-c0ab7646-d3c5-4abd-91cf-047acd7aca42.png)

Now all that is left to do is gather the information for the passowrd.

We just need to find the Zipcode, let's just Google `post code Boulevard de Belgique, Monaco`

With the information gathered above, let's compose the password.

`Monaco-98000-Boulevard-de-Belgique-32`

Extract the `flagfile-the-listeners.zip` with the password from the information gained above to get your contract card.

$~$

📌 BoΠeShΔdϴw³
