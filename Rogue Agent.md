<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203551900-f5000c88-af2e-48e6-9acc-7d845113269b.png">

# Contract: Rogue Agent
![cover-rogue-agent-600x600](https://user-images.githubusercontent.com/117080369/203539156-ad62a2da-5bdd-4758-8856-e71cbc6e3adb.jpg)


### Difficulty: Medium

### Mission Briefing:
Greetings Special Agent K. We have a request on our hands from our friends over at the CIA. In September of 2021, one of their operatives went missing in action. Upon further investigation, it was discovered this operative went rogue and started a smuggling business for the Russians. Mostly dealing in complex electronics, which have become difficult to come by for Russians after sanctions began.

The agent we’re looking for is named Valentino Maggi. Born in Brooklyn New York on 18.05.1987. Valentino is one of five sons of the Maggi family, who moved to the United States during World War II. Having grown up a middle class lifestyle, his father a car salesman and mother working as an elementary school teacher. Valentino was recruited into the CIA during his time as a student at Columbia University.

Most of his 10 years in active service were spent as an analyst working out of Langley. Recently though, in August of 2020, Valentino moved to oversees work. Being stationed in Italy as a liaison officer for the Italian foreign intelligence agency “Agenzia Informazioni e Sicurezza Esterna”.

Doing stellar work, right up until the point he went missing. Prompting an extensive investigation into his whereabouts. Documents were eventually found on his computer, recovered using forensics tools to recover deleted files. These indicate a heavy involvement with the Russian underground. Acquiring much needed microelectronics for the Russian government.

And that is where your task begins, Special Agent K. One of the files recovered from Valentino’s computer, is an image with a text file. We believe this to be the current location of Valentino Maggi. Locate the safehouse, so local authorities can raid the premises.

As always, Special Agent K. The contract is yours, if you choose to accept.

---

### Process:
Reading through the mission briefing doesn't really give us anything to go on, so the next step is to look at analyzing the image.

Nothing specific in the image we can really use to identify the location.

* Exiftool - nothing useful
* Aperi'Solve - nothing useful
* Google reverse image search - nothing useful
* Bing reverse image search - nothing useful
* Various other reverse image searches - nothing useful

Nothing of any interest yet.

At this point I am scratching my head a bit. however I am going to make the assumption that because this is a Medium difficulty challenge the `clue` we need must be right in front of us...

Let's head over to CyberChef and select `Open file as input` scanning through the Output, the only thing that stands out a little is the very last line, the very end looks odd. Is that a clue?

æÊäÄÒÂZäÂÖÒÜÂÆZhh\djrljhZdb\`jnphf

Let's copy this into CyberChef and select `Magic` from the Operation menu - nothing of interest.

Let's re-try with `Intensive mode` selected - boom! result...

REDACTED - no spoiler
![Screenshot 2022-11-23 121522](https://user-images.githubusercontent.com/117080369/203544854-9eafd9cf-adf6-4f4a-b72a-de59598f60b2.png)

Extract the `linkfile-rogue-agent.zip` with the password from the `Rotate_right(1,false)` result and visit the `bit.ly` link to get your contract card.
