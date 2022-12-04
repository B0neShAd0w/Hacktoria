<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: A Strange File
![a_strange_file_cover-600x600](https://user-images.githubusercontent.com/117080369/205494097-10a3e43c-4cba-4ff4-acf8-6226be5ed82e.png)

### Difficulty: Insane

### Mission Briefing:
Greetings Special Agent K. During a raid of our allies in the country of Oman, several computers and server equipment were confiscated.

The authorities of Oman spent the past week analyzing the data that resides on this hardware. However, they were not able to make sense of all the data.

This is where we come in. The Overseer of Hacktoria has agreed to a no-cure no-pay assignment for the government of Oman. If we manage to figure out what the file they’ve sent us means, we take on several additional contracts in the future, at very favorable terms.

A little more information about this file. It was found in a folder named “meeting location”. It had several text files in it, that all had written details about locations and people.

There was one file however, that the Oman authorities were not able to convert to text. This is the file you find below. Please make sense of it and report your findings Special Agent.

As always, Special Agent K. The contract is yours, if you choose to accept.

---

For this contract you will need to use the website https://what3words.com/

The password to open the flagfile consists of (lowercase letters):

country-district-city-areadialcode-what-three-words-business-type

Sample password:

italy-veneto-verona-045-hot-pasta-sauce-paper-mill

---

### Methodology:
The first step is to pull out information from the Mission Briefing that we feel is of importance.
* Oman authorities
* There was one file however, that the Oman authorities were not able to convert to text

This doesn't really give us many clues.

If we open this file with a `Text Editor` we can see a lot of `HEX` code, is there anything else interesting in this file?.

The first 6 characters look like it a file signature!

We can confirm this a number of ways, just have a look at <a href="https://en.wikipedia.org/wiki/List_of_file_signatures">List of file signatures - Wikipedia</a> for `FF D8 FF`

![Screenshot 2022-12-04 134936](https://user-images.githubusercontent.com/117080369/205494363-f784d0e0-5f0c-429e-bb6b-53b608a5d80e.png)

This confirms we are dealing with a malformed `JPG`, let's take a closer look

On closer examination we notice that there is some `white space`, this probably means there is another file embedded within the original.

![Screenshot 2022-12-03 175206](https://user-images.githubusercontent.com/117080369/205494384-a1bc9d1f-60af-4c0b-9a36-0f8fb1c1f782.png)

Let's head over to <a href="https://tomeko.net/online_tools/hex_to_file.php?lang=en">Hex to file (binary)</a> & paste the entirety of the text into the `Hex string` box, give the file a name and click `Convert`.

![Screenshot 2022-12-04 135247](https://user-images.githubusercontent.com/117080369/205494530-ef8064a5-59de-488f-be15-6d7864a5c421.png)

Click OK to the message.

![Screenshot 2022-12-04 135516](https://user-images.githubusercontent.com/117080369/205494648-eaa45288-428a-4163-aa39-775bd22c00cb.png)

Woohoo! we now have an image file showing a location.

![strange-file](https://user-images.githubusercontent.com/117080369/205494663-eeddb34e-7236-4bc5-9668-da0ca6f20ad3.jpg)

Let's see if we can get the 2nd file, for this we will head over to <a href="https://www.aperisolve.com">Aperi'Solve</a> 

Select the image from the previous steps and click `SUBMIT`, once it has finished processing the image, scroll down to the `Foremost` section.

![Screenshot 2022-12-03 180839](https://user-images.githubusercontent.com/117080369/205494696-02550b1f-2aba-4813-a62b-178c91d83823.png)

Click `DOWNLOAD FILES`, once the files have downloaded, extract them and browse the extracted `jpg` folder.

You should now have 2 images, `00000000.jpg` & `00000134.jpg` 

Note: 00000000.jpg is just a duplication of the original file.

Let's examine the images for any clues...

What do we know?
* 00000000.jpg is satellite imagery of an unknown location - not much to use.

![00000000](https://user-images.githubusercontent.com/117080369/205494716-2891a009-fe36-46a5-9f58-e83cb8a06d7e.jpg)

* 00000134.jpg does contain some useful clues
	* Arabic text written on the wall(s)
	* Possibly a disused/closed Gas Station
	* Dry sandy/dusty environment
	* Small overhead Powerlines - probably a remote town/village
	* Water on the ground - possibly a water leak
	* Disused/old car parts
	* Rudimentary pits/trenches - possibly used for car repairs

![Screenshot 2022-12-03 182419](https://user-images.githubusercontent.com/117080369/205494778-4cb416fa-8ed8-476c-a713-72a5773a67b2.png)

I think from the information gathered that we are looking for a disused gas station with a car repair workshop in very close proximity, in an Arabic speaking town/village.

However we do not know if the assumed car repair shop is still in business or not, so how are we going to locate this?

Let's head over to Wikipedia and get a <a href="https://en.wikipedia.org/wiki/List_of_countries_and_territories_where_Arabic_is_an_official_language">List of countries and territories where Arabic is an official language</a> 
1. Algeria
2. Bahrain
3. Chad 
4. Comoros 
5. Djibouti 
6. Egypt 
7. Iraq 
8. Jordan 
9. Kuwait 
10. Lebanon 
11. Libya 
12. Mauritania 
13. Morocco 
14. Oman
15. Palestine 
16. Qatar 
17. Saudi Arabia   
18. Somalia 
19. Sudan 
20. Syria 
21. Tunisia 
22. United Arab Emirates  
23. Yemen 

Um, this highlights how big a task this might be...

After many many hours trying to translate the text in the image using the `Arabic alphabet` and not getting anywhere, I decided to try a different tact.

Let's head over to <a href="https://overpass-turbo.eu/">overpass turbo</a> and enter `Oman` into the search area, zoom out to include as many of the listed countries as possible and enter `amenity=fuel` into the Wizard.

Wow! that is a LOT of `Fuel Stations`.

![Screenshot 2022-12-03 190747](https://user-images.githubusercontent.com/117080369/205494881-cecdb6c0-72e4-4665-b582-50da8094d231.png)

Let's run another <a href="https://overpass-turbo.eu/">overpass turbo</a> query, but this time by entering `shop=car_repair` into the Wizard.

![Screenshot 2022-12-03 190221](https://user-images.githubusercontent.com/117080369/205494901-db2cc996-7c9e-4944-936d-b9221ccbf6c5.png)

This has narrowed the search a little, however we do not really know if we are looking for a `car repair shop` or not, so we could end up wasting hours or even days and not finding our location.

Let's run another <a href="https://overpass-turbo.eu/">overpass turbo</a> query, but this time by entering `amenity=fuel and shop=car_repair` into the Wizard.

![Screenshot 2022-12-03 190856](https://user-images.githubusercontent.com/117080369/205494927-5f2fab2d-1476-44d9-a41a-58dad508c361.png)

Not very many results at all, let's have a look at them in <a href="https://www.google.com/maps/">Google Maps</a> and see if we get lucky.

That is a big fat NO!

At this point I was really struggling to know which direction to head in, So I decided to step away from this contract for a while.

Coming back to this rejuvenated with a couple of new ideas to try out, let's get stuck in.

Something is niggling away at me saying *"the text is important"* - so I decided to use <a href="[Google Translate](https://translate.google.com/)">Google Translate</a> and translate the country names from English to Arabic.

| English | Arabic |
|---|---|
| Algeria | الجزائر |
| Bahrain | البحرين |
| Chad | تشاد |
| Comoros | جزر القمر |
| Djibouti | جيبوتي |
| Egypt | مصر |
| Iraq | العراق |
| Jordan | الأردن |
| Kuwait | الكويت |
| Lebanon | لبنان |
| Libya | ليبيا | 
| Mauritania | موريتانيا |
| Morocco | المغرب |
| Oman | سلطنة عمان |
| Palestine | فلسطين |
| Qatar | دولة قطر |
| Saudi Arabia | المملكة العربية السعودية |
| Somalia | الصومال |
| Sudan | السودان |
| Syria | سوريا |
| Tunisia | تونس |
| United Arab Emirates | الإمارات العربية المتحدة |
| Yemen | اليمن |

Oh, this is interesting...

The translation of `Libya` looks very similar to the text in the our image: 

![Screenshot 2022-12-04 092357](https://user-images.githubusercontent.com/117080369/205495077-467d0df2-dd6d-4630-bdfb-e04c83ba9808.png)







Extract the `flagfile-a-strange-file.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
