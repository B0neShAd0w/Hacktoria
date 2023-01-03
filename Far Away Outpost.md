![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# Far Away Outpost
![far-away-outpost-cover-600x600](https://user-images.githubusercontent.com/117080369/204478206-d9583b8b-4ddb-46cd-9528-6d54e72b47f4.png)

### $\color{magenta}{DIFFICULTY}$
${\color{gray}EASY\ |\ MEDIUM\ |\color{white}\ HARD\ \color{gray}|\ INSANE}$

$~$
---

### $\color{magenta}{PROLOGUE}$
It was a hot and humid day in the Kenyan forest, and the team of forest rangers were on high alert. They had received a tip that a man named Zayed was attempting to smuggle illegal zebra hides out of the country, and they were determined to catch him in the act.

As they patrolled the winding dirt roads, they spotted a Rangerover coming towards them. It was driven by a man who looked a lot like the one in the photo they had been given.

The rangers signaled for the vehicle to stop, and as it came to a halt, they surrounded it, guns drawn. The driver, a rugged-looking man with a thick beard, glared at them with cold eyes.

“Step out of the vehicle,” one of the rangers ordered.

The man hesitated for a moment, and then slowly climbed out of the car. As he did, the rangers noticed a suspicious bulge under his jacket. They quickly searched him and found a package containing several zebra hides.

Zayed was arrested on the spot and taken back to the ranger station, where he was booked and charged with illegal wildlife smuggling.

$~$

### $\color{magenta}{BRIEFING}$
Greetings Special Agent K. I hope you’re in the mood for hunting down some poachers. We have a contract from the Kenyan government to track down an animal smuggling and poaching operation.

This group uses various humanitarian organizations as fronts for their poaching operations. Often pretending to be building civilian infrastructure to obscure their activities.

In their latest attempts to stay undetected, the group started to present themselves as construction workers. Traveling to remote villages and outposts to supposedly install water tanks and wells. Unsuspecting locals would let them go about their business, as they used this cover to poach wild animals.

Last week, the Kenyan authorities were able to apprehend one of their members. They were able to extract a few pieces of information from his cellphone. Unfortunately, the young man hung himself that same night. Making further questioning somewhat troublesome.

You’ll find the information we have below. Your mission is simple, find the location of the current poacher outpost.

As always. Special Agent K, the contract is yours, if you choose to accept.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$

<a href="https://hacktoria.com/wp-content/contracts/flags/flagfile-far-away-outpost.zip">Download Flagfile</a>

<a href="https://hacktoria.com/wp-content/uploads/2022/09/far-away-outpost-1.jpg">Download Image One Full Size</a>

<a href="https://hacktoria.com/wp-content/uploads/2022/09/far-away-outpost-2.jpg">Download Image Two Full Size</a>

$~$

---

### $\color{magenta}{METHODOLOGY}$
The first step is to pull out imformation from the Mission Briefing that we feel is of importance.
* Kenyan government
* uses various humanitarian organizations as fronts for their poaching operations
* present themselves as construction workers
* remote villages and outposts
* install water tanks and wells

As always when images are supplied I will run some analysis on the images, metadata and reverse image searches etc., however this didn't bear any fruit unfortunately.

At this point I thought with the information above some Google Dorking might point me to some useful locations to analysis more, however after spending a fair bit of time on this and getting nowhere I scrapped that idea.

At this point a started to research Keyna and found <a href="https://www.citypopulation.de/en/kenya/admin/">Kenyan Provinces and Counties</a>.

The next step was to view each `County` in `3D` on <a href="https://earth.google.com/web/">Google Earth</a> to see if any areas matched the sort of terrain in the images supplied - dusty/sandy looking area, with Peak(s) in very close proximity.

This provided me with a pretty large list to sift through, sigh!

Next step was to work through the new list of towns/villages that match the criteria and adding them to a new list for further analysis.

Using <a href="https://overpass-turbo.eu/">overpass turbo</a>, I entered each result into the Search Area and zoomed the view out so that the really small townships show and then run the query below, we can exclude any peaks that are NOT near a road.

This now gives a smaller list to work with.

```
[out:json][timeout:25];
// gather results
(
  node[natural=peak]({{bbox}})
      (if:t["ele"] > 1000.0); 
);
out; 

// print results
out body;
>;
out skel qt;
```

*Note: If I didn't get lucky, I would have changed the elevation in the query.*

Grab the coordinates for each of the Peaks and enter into Google Earth and view in `3D` to see if we get a hit.

![image](https://user-images.githubusercontent.com/117080369/204509021-c948677b-4001-4ab7-9309-f50e0925327f.png)

Eventually - this looked interesting, similar shape, similar buildings, there is a road near the peak, definately worth looking into...

![Screenshot 2022-11-29 095255](https://user-images.githubusercontent.com/117080369/204497246-68e4ecd0-fb57-412c-9613-1f67e0cd9953.png)

Zooming in and having a better look confirms this could be the location we are looking for.

![image](https://user-images.githubusercontent.com/117080369/204510079-c30dd9d8-614a-4752-9e0c-1aaa066f0c23.png)

Let's switch to `Street View` and make sure.

![image](https://user-images.githubusercontent.com/117080369/204510500-2752e81a-d72c-481b-86f9-aea548f9067b.png)

Boom! we have now confirmed the location, let's grab the information to get our contract card.

Switching back to overpass turbo and zooming in, we are able to gather the required information.

![Screenshot 2022-11-29 105431](https://user-images.githubusercontent.com/117080369/204511386-d88a4e97-6c0e-469a-9d96-c9db6ed77ee4.png)

Extract the `flagfile-far-away-outpost.zip` with the password from the information gained above to get your contract card.

$~$

📌 BoΠeShΔdϴw³
