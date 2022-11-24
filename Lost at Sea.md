<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: Lost at Sea
![lost_at_sea_cover-600x600](https://user-images.githubusercontent.com/117080369/203797664-e030da32-fa73-4201-927c-a2713e66f145.png)

### Difficulty: Easy

### Mission Briefing:
Greetings Special Agent K. Yesterday at exactly 22:34 EET we lost contact with our surveillance ship “Narwhal”. A distress signal was sent out, right after this all communication was lost. The Narwhal was operating in the Black Sea, keeping an eye on Russian submarine and aerial activity.

Although she looks like a regular fishing trawler, the Narwhal, built in 2018, was outfitted with state of the art equipment. Housing a crew of 10, including a 4 PAX intervention unit of our best and brightest from the H.M.I.U (Hacktoria Maritime Intervention Unit).

Our allies in the British Royal Navy were kind enough to respond immediately. They were able to retrieve the Narwhals’ distress beacon. This is a device that automatically logs the last ten event, using the many sensors on board. This quick log entry is written to the SD card inside a waterproof tube, outfitted with a flotation device and GPS beacon. After the data is written, the beacon ejects and keeps afloat on the surface.

This prevents any signal delay from external antennas not being fast enough. Now, there’s a catch with this beacon. The log-file is written to an encrypted archive. The password for this log-file is set by the captain and communicated over encrypted channels, changing daily to prevent enemy forces capturing the correct code.

Somehow, the signal was lost right before the captain was able to relay the new password. This is human error, the password would normally be communicated right before being changed. This leaves us with our current situation. We don’t know the password, you’ll have to find a way to unlock the log-file.

This will give us insight into how the Narwhal sunk and allow us to begin the recovery. Given the hostile situation, it’s imperative we find the exact location of the Narwhal.

---

Instructions: Crack the password to open the ship logbook file (flagfile)

---

### Process:
The first step is to pull out imformation from the Mission Briefing that we feel is of importance.
* 22:34
* Narwhal
* Black Sea
* 2018
* H.M.I.U
* Hacktoria Maritime Intervention Unit

We now need to work out what the password could be, given that generally speaking passwords rarely contain space we can exclude a couple of the pieces of information, this leaves us with this:
* 22:34
* Narwhal
* 2018
* H.M.I.U

As we only have 4 possibilites, let's try them one at a time - can it be that easy? umm no!

Okay let's build out a word-list by combining 2 of the words first, if we don't have any luck we can add `-` or up it to 3 words.
* 22:3422:34
* 22:34Narwhal
* 22:342018
* 22:34H.M.I.U
* NarwhalNarwhal
* Narwhal22:34
* Narwhal2018
* NarwhalH.M.I.U
* 20182018
* 201822:34
* 2018Narwhal
* 2018H.M.I.U
* H.M.I.UH.M.I.U
* H.M.I.U22:34
* H.M.I.UNarwhal
* H.M.I.U2018

Doesn't take long for us to find our answer - `Narwhal2018`

Extract the `flagfile-lost-at-sea.zip` with the password from the information gained above to get your contract card.
