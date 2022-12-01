<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Kanonniers
![kanonniers-cover-600x600](https://user-images.githubusercontent.com/117080369/205070112-88dbd378-7d7e-4af7-beb2-6632a30966a6.png)

### Difficulty: Insane

### Mission Briefing:
Greetings, Special Agent K. We are on the hunt for operatives of a competing organization. We believe them to be the continuation of a rival Order “The Golden Creed”, who we eradicated mid 18th century. Somehow the family running the Order managed to reorganize and fund new endeavors. Flying under the radar for several years, they now have a foothold in many European countries.

Unfortunately for them, they’ve chosen to cross paths with some of our bigger clients in several of these countries. Most recently, the Dutch intelligence agency AIVD, started investigating them after being linked to a human trafficking ring. All beginning with the Syrian refugee crisis a few years back.

What made this Order fly under the radar for many years, is their total aversion for the digital world. Barely dipping their toes in web 1.0, The Golden Creed uses mostly analog means of communication. Making them infinitely harder to track.

Our friends at the AIVD however once observed a member of The Golden Creed insert a package into an opening of a monument. Upon closer inspection, it turned out to be instructions for a hit being placed by a client of The Golden Creed.

This leads us to your objective. Last week, an operative of The Golden Creed was arrested by Dutch police. Carrying a picture with him of an old cannon. Given their tendency to hide information in historical objects, we believe this particular cannon is a location of interest. Possibly holding information, or being frequently used to pass information.

Our client has asked us to locate the cannon. Use the image below to find the location of the cannon.

As always. Special Agent K, the contract is yours, if you choose to accept.

---

Use your findings to generate the password that will unlock the “flagfile”, which in turn leads to your Contract Card. For this you will need the service: https://what3words.com/

---

### Methodology:
The first step is to pull out imformation from the Mission Briefing that we feel is of importance.
* Dutch intelligence agency
* monument
* cannon

Given the above information pertains to the Dutch Intelligence Services I think we should start our search in the `Netherlands`.

Upon eaxmaning the supplied image we have a couple of very useful keys to go on.
* Old cannon on stone base
* Some kind of waterway, could be river or canal etc.
* A few buildings dotted around fileds

Let's head over to <a href="https://overpass-turbo.eu/">overpass turbo</a> and run a search for historic cannons in the Neterlands.

Running the wizard and using the tag `historic=cannon in Netherlands` returns a handful of locations.

![image](https://user-images.githubusercontent.com/117080369/205074392-e420ed03-f51c-402b-a042-1d1001c03c9b.png)

We can skip any of these that are not near a waterway or near a very big body of water, this narrows the search down a little further.

Zooming in a little pick the ones that match our criteria, and grab the coordinates.

![Screenshot 2022-12-01 141257](https://user-images.githubusercontent.com/117080369/205074913-9092543e-a3be-4df1-b2e6-bff6e589fa3a.png)

Looking up the coordinates in <a href="https://earth.google.com/">Google Earth</a> we can have a quick look around to see if we are in the correct area or not.

![image](https://user-images.githubusercontent.com/117080369/205075775-1cfcac83-1306-4e58-9504-8c6342790c88.png)

Dropping into `Street View` to get a better look...

![image](https://user-images.githubusercontent.com/117080369/205077432-317f9235-0de8-4009-aaee-2141a5701cd0.png)

Nope, not a match, not even close...

Let's work our way through them.

Soon we find one that looks promising...

![image](https://user-images.githubusercontent.com/117080369/205076951-b50f4406-2faf-4976-a652-f2cf829ffebd.png)

Extract the `flagfile-kanonniers.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
