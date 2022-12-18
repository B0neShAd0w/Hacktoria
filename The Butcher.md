<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: The Butcher
![the-butcher-cover-600x600](https://user-images.githubusercontent.com/117080369/203931080-d927f0e0-6968-4c04-8e74-0e353572798c.png)

#### Difficulty: Easy

### **$\textcolor{Rhodamine}{Prologue:}$**
It was just another ordinary day in Berlin, until the German police received a tip about a suspicious apartment in the city. They had no idea what they were going to find, but they knew that they had to be prepared for the worst.

As they arrived at the apartment building, the police noticed that the windows were all covered with black curtains, and there were no signs of life inside. They knew that this was a bad sign, and they braced themselves for what was to come.

With guns drawn, the police burst into the apartment, ready to take down any threats that might be waiting for them. But as they searched the rooms, they found nothing but an empty, rundown space.

It wasn’t until they reached the bedroom that they found something unusual. Tucked away in a corner was a computer, with various sets of knives scattered around it.

The police knew immediately that they had stumbled upon something significant. They carefully gathered up the knives and the computer, and took them back to the station for further analysis.

As they began to go through the computer’s files, the police were shocked to discover that they had finally found the apartment of the serial killer they had been searching for. For years, this mysterious figure had been terrorizing the city, leaving a trail of bodies in his wake.

The police were elated at the discovery, knowing that they were one step closer to bringing the killer to justice. They poured over the evidence, piecing together the clues and trying to track down the killer’s whereabouts.

### **$\textcolor{Rhodamine}{Briefing:}$**
Greetings, Special Agent K. As you might have heard in the news over the past few months. The city of Berlin in Germany is being plagued by a serial killer, nicknamed “The Butcher”.

As the name implies, this individual butchers his victims and disposes their body parts all over the city. Autopsy reports conclude that the weapon for disposal is most likely a meat cleaver.

The total body count currently sits at 18 people, mostly women and younger men. All victims were traveling alone at night, mostly through quiet areas, when they were last seen.

Fortunately, yesterday the German police raided an apartment in the city center of Berlin. Neighbors had complained about a stale, metal like smell coming from the apartment. Upon closer inspection, the police found large quantities of plastic sheets, blood traces of several victims and an assortment of meat cleavers.

Since the apartment was rented out to an individual who had used a fake ID, the police has hit a dead end in trying to find the killer. They did however retrieve several files from a personal laptop, including a large, encrypted archive.

In the same location as the archive was stored, a file named “password” was found. However, this just contained a bunch of HEX values. We need you to make sense of this file, perhaps it leads to the password for the archive.

As always, Special Agent K. The contract is yours, if you choose to accept.

---

### Methodology:
Reading through the mission briefing it mentions a file named "password", let's download the file and have a look at what we are dealing with.

The beginning of the code looks like it is a file signature!, we can confirm this a number of ways, just have a look at <a href="https://en.wikipedia.org/wiki/List_of_file_signatures">List of file signatures - Wikipedia</a> for `49 44 33`

![image](https://user-images.githubusercontent.com/117080369/203943992-47c2e2a1-e0f8-4abe-8fad-5fd3e19217bf.png)

Alternatively we can head over to <a href="https://gchq.github.io/CyberChef/">CyberChef</a> 
* Copy the code into the `Input` pane
* From the Operations menu select `From Hex` 

![Screenshot 2022-11-25 092425](https://user-images.githubusercontent.com/117080369/203946107-5ae33b10-43c2-416e-a46f-8b9be421acdd.png)

*   Without clearing anything, select `Detect File Type` from the Operations menu - this confirms the file type is an MP3

![Screenshot 2022-11-25 092543](https://user-images.githubusercontent.com/117080369/203946457-e5298169-8793-47df-8264-5d2c6f610892.png)

In the Output pane, click `Save output to file`, then at the `Please enter a filename:` dialog change the extension from`.dat` to `.mp3` and click **OK** to download the file.

![Screenshot 2022-11-25 092806](https://user-images.githubusercontent.com/117080369/203946967-9f43fac5-8e39-4056-8bbf-36ca1d5121df.png)


Play the file in a media player like VLC to hear the password.

Extract the `flagfile-the-butcher.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
