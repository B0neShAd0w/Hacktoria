<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Infectious File
![cover-infesctious-file-600x600](https://user-images.githubusercontent.com/117080369/208292208-429b0b61-b4ec-4033-a6e3-10c53017ec04.png)

#### Difficulty: Medium

### **$\textcolor{Rhodamine}{Prologue:}$**
Jamal sat in the dimly lit basement of his parents’ house, hunched over his computer. He was a hacker, and he was writing some of the most advanced malware the world had ever seen.

He had always been fascinated by computers and technology, and had spent years learning everything he could about hacking and coding. And now, finally, he was putting all of that knowledge to use.

As he worked, Jamal’s fingers moved across the keyboard with lightning speed. He was completely focused, completely immersed in his work. He was in a zone, and nothing could distract him.

He knew that what he was doing was illegal, and that there were serious consequences if he was caught. But he didn’t care. He was driven by a desire to push the boundaries, to see just how far he could go.

Finally, after hours of intense work, the malware was complete. Jamal sat back in his chair and let out a sigh of relief. It had been a long and difficult process, but it had all been worth it.

Now it was time to send the malware to his boss, Mr Reaper. Mr Reaper was the leader of a group of hackers known as the Shadow Syndicate, and Jamal was one of their top operatives.

Jamal carefully packaged the malware and sent it off to Mr Reaper, along with a detailed report on how it worked. He knew that Mr Reaper would be pleased with his work, and he couldn’t wait to see what the Shadow Syndicate would do with it.

A few days later, Jamal received a message from Mr Reaper. “Excellent work, Jamal,” it read. “The malware is even more advanced than I had hoped. We’ll put it to good use. Keep up the good work.”

Jamal couldn’t help but feel a sense of pride and accomplishment. He had done something that few others would have the courage to do, and he knew that he had made a real difference.

From that day on, Jamal continued to work for the Shadow Syndicate, using his skills and knowledge to help them achieve their goals. And though he knew that it was dangerous work, he couldn’t help but feel a sense of excitement and purpose. This was where he belonged, and he knew that he would always be remembered as one of the greatest hackers of all time.

### $\textcolor{Rhodamine}{Briefing:}$

Greetings Special Agent K. We have received intelligence that a hacker group known as the Shadow Syndicate has been developing very advanced malware. This group has been responsible for a number of high-profile cyber attacks in the past, and we believe they are planning to launch another one soon.

Your mission is to examine one of the samples of their malware that we have obtained. We believe that it contains clues about their plans and capabilities, and we need you to find out as much as you can about it.

You will be working with a team of experts to analyze the sample and extract any useful information. We need you to be thorough and detail-oriented, as every piece of information could be crucial in stopping the Shadow Syndicate.

It’s imperative to figure out exactly what they are capable of and discover their intentions based on the malware sample. We are counting on you to help us take down this dangerous group and prevent them from causing any more harm.

Pay extra attention on this one, as you are working with a live malware sample.

As always, Special Agent K. The Contract is yours, if you choose to accept.

---

> __Warning__ The “infectious file” is a REAL MALWARE SAMPLE. Download at your own risk. Advice to use a Virtual Machine for interacting with the file. Hacktoria is not responsible for any consequences of your own actions.

---

### Methodology:
First thing I will be doing is creating a `Sandbox VM` for this contract, to be honest I do not want to be playing around with live Malware samples (bad experience from days gone by - however that is another story!).

> __Note__ Due to the dangers associated with this I will be breaking away from the norm and doing this entirely isolated within the VM, with no network access.

Okay let's download an ISO for our VM, I choose to use <a href="https://www.parrotsec.org/download/">Parrot Architect Edition</a>, why? because I like Parrot OS and this edition is just a bare bones image.

![Screenshot 2022-12-18 075647](https://user-images.githubusercontent.com/117080369/208293047-5de3457c-e97a-4de4-8aa7-31f6db71b42d.png)

Once the ISO has downloaded and the `Checksums` have been verified open Virtualbox and click `New` on the main menu.

Enter a `Name:`, `Folder:` path to save the VM to & the `ISO Image:` location, then click `Next`

![Screenshot 2022-12-18 080021](https://user-images.githubusercontent.com/117080369/208293097-ddb1ae29-9245-4a39-9421-666a5b70ac1f.png)

At the `Create Virtual Machine` wizard enter the amount of `Base Memory:` and `Processors:` required, then click `Next`

![Screenshot 2022-12-18 080422](https://user-images.githubusercontent.com/117080369/208293154-42fc87cb-570f-48a7-966d-fd6cf7d95612.png)

Enter the `Disk Size:` required and click `Next`.

![Screenshot 2022-12-18 080546](https://user-images.githubusercontent.com/117080369/208293244-19a71ed7-708e-4451-8515-480742ff02a1.png)

At the `Summary` page review the summary and click `Finish`

![Screenshot 2022-12-18 080651](https://user-images.githubusercontent.com/117080369/208293536-bdff1d3b-a0a4-410f-9d32-eba6fea4a632.png)

Now the VM has been created there a few important steps to fulfil before we can start using it for Malware Analysis.

Click `Settings` from the main Menu.

![Screenshot 2022-12-18 080800](https://user-images.githubusercontent.com/117080369/208293415-a356a228-6cc7-4b13-9581-0c38089868f6.png)

From the Side Menu select `General` then select the `Basic` tab, change the `Version` to `Debian (64-bit)`

![Screenshot 2022-12-18 080930](https://user-images.githubusercontent.com/117080369/208293633-662ca23d-5d8a-45d5-a4ae-40c25246ab8f.png)

Click the `Advanced` tab and make sure that `Shared Clipboard:` and ` Drag'n'Drop:` are `Disabled`

![Screenshot 2022-12-18 081026](https://user-images.githubusercontent.com/117080369/208293701-a7ff2b8a-fd51-40c2-aa4e-e21c9eca9a7b.png)

From the Side menu select `System` and then select the `Processor` tab, make sure `Extended Features: > Enable PAE/NX` is not selected.

![Screenshot 2022-12-18 081418](https://user-images.githubusercontent.com/117080369/208293855-fb25a04c-e9a0-4da2-8edb-ceec6743e884.png)

Click the `Acceleration` tab, make sure `Paravirtualization Interface:` is set to `None`.

![Screenshot 2022-12-18 081559](https://user-images.githubusercontent.com/117080369/208293872-b66016e7-76d8-42b4-8f97-77b6e22013a0.png)

From the Side menu select `Display` then the `Screen` tab, change the `Video Memory:` to `128 MB`

![Screenshot 2022-12-18 085051](https://user-images.githubusercontent.com/117080369/208293978-d052e4e9-0a01-4d52-b0df-e436deaa9354.png)

From the Side menu select `Audio` make sure `Enable Audio` is not selected.

![Screenshot 2022-12-18 081834](https://user-images.githubusercontent.com/117080369/208294116-4b13b757-b73a-41cb-ab9c-1a53cf9239be.png)

From the Side menu select `Network` and then select the `Adapter 1` tab, set `Attached to:` to `Bridged Adapter`

> __Note__ We will be changing this once we have the required updates/tools and files.

![Screenshot 2022-12-18 085651](https://user-images.githubusercontent.com/117080369/208294183-febd8fd9-ec8f-47a4-9a8c-35362693412e.png)

From the Side menu select `Shared Folders` and confirm non have been set, and click `OK`

![Screenshot 2022-12-18 082159](https://user-images.githubusercontent.com/117080369/208294603-f75c0185-c469-4f30-b14b-8cbe713ac02c.png)

Now run `sudo apt update && sudo parrot-upgrade` to ensure the OS is fully patched.

Install any tools that are required (for this contract we only require the Strings tool), which is already installed.

> __Warning__ Do not install `Virtualbox Tools` on the VM.

Now everything is patched, tools installed and the Malware sample downloaded we are going to drop the network from the VM.

Shutdown the VM 

Let's take an export of this VM, so we have a disposable VM for situations just like this.

Right click on the VM and select `Export to OCI...`, enter the following settings and click `Next`

![Screenshot 2022-12-18 091818](https://user-images.githubusercontent.com/117080369/208295185-10b0e2bc-358e-40f5-8c9c-981adbf01db7.png)

Once the export has finsihed we are ready to start analyising the Malware Sample.

Let's isolate this VM from any network, click `Settings`

From the Side menu select `Network` and then select the `Adapter 1` tab, set `Attached to:` to `Not attached`

![Screenshot 2022-12-18 110811](https://user-images.githubusercontent.com/117080369/208295017-dab3c235-ec76-4020-9253-6fd632844b25.png)

> __Warning__
> This is your final warning, anything you do from here on out is on your head!, I cannot be help responsible for any damage caused. - if you are unsure DO NOT PROCEED.

If you are sure read on...

Are you sure?.

Okay then...

Open a terminal and enter the following command:
```bash
strings <PATH TO FILE/MALWARE SAMPLE>
```

Read through the very long output and look for anything that really stands out, `Th3p@$$4th3Fl@g` looks a little different to everything else, let's try that on our flag file.

![woohoo-homer-simpson](https://user-images.githubusercontent.com/117080369/208295750-f84ba8de-3ffd-4880-abe2-fc272da32c37.gif)

Extract the `flagfile-infectious-file.zip` with the password from the information gained above to get your contract card.


BoΠeShΔdϴw³
