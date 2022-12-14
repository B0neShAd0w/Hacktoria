![hacktorie-pixel-cyberpunk](https://user-images.githubusercontent.com/117080369/210135718-2b467f21-bc81-438c-b856-2ceb3f8b4375.png)

# Lost at Sea
![lost_at_sea_cover-600x600](https://user-images.githubusercontent.com/117080369/203797664-e030da32-fa73-4201-927c-a2713e66f145.png)

### $\color{magenta}{DIFFICULTY}$
${\color{white}EASY\ \color{gray}|\ MEDIUM\ |\ HARD\ |\ INSANE}$

$~$
---

### $\color{magenta}{PROLOGUE}$
The Narwhal was a ship like no other. Outfitted with the most advanced electronic warfare equipment known to man, it was capable of intercepting and decoding even the most encrypted communications. But to the outside world, the Narwhal was just another ordinary fishing trawler, making its way through the choppy waters of the Black Sea.

On this particular mission, the Narwhal was tasked with monitoring a Russian ship that was suspected of transporting illegal weapons. Captain Marcus and his crew were experts at blending in and going unnoticed, and they had spent the past week trailing the Russian ship at a safe distance.

As they worked, the crew of the Narwhal couldn’t help but marvel at the sheer sophistication of their vessel. From its state-of-the-art radar system to its advanced communication tools, the Narwhal was a true marvel of modern technology.

But as they neared the Russian ship, the crew began to pick up some strange signals. It was clear that the Russians were using some kind of advanced jamming technology to try and block their communications.

Captain Marcus knew that this was their moment to strike. He ordered his crew to activate the Narwhal’s electronic warfare systems, and within minutes, they had successfully decrypted the Russian ship’s communications.

As they read through the intercepted messages, the crew of the Narwhal couldn’t believe what they were seeing. The Russian ship was indeed transporting illegal weapons, and they had enough evidence to bring down the entire operation.

The Narwhal quickly reported their findings back to headquarters, and within hours, the Russian ship was apprehended by authorities. It was a triumphant moment for Captain Marcus and his crew, who knew that their mission had made a real difference in the world.

$~$

### $\color{magenta}{BRIEFING}$
Greetings Special Agent K. Yesterday at exactly 22:34 EET we lost contact with our surveillance ship “Narwhal”. A distress signal was sent out, right after this all communication was lost. The Narwhal was operating in the Black Sea, keeping an eye on Russian submarine and aerial activity.

Although she looks like a regular fishing trawler, the Narwhal, built in 2018, was outfitted with state of the art equipment. Housing a crew of 10, including a 4 PAX intervention unit of our best and brightest from the H.M.I.U (Hacktoria Maritime Intervention Unit).

Our allies in the British Royal Navy were kind enough to respond immediately. They were able to retrieve the Narwhals’ distress beacon. This is a device that automatically logs the last ten event, using the many sensors on board. This quick log entry is written to the SD card inside a waterproof tube, outfitted with a flotation device and GPS beacon. After the data is written, the beacon ejects and keeps afloat on the surface.

This prevents any signal delay from external antennas not being fast enough. Now, there’s a catch with this beacon. The log-file is written to an encrypted archive. The password for this log-file is set by the captain and communicated over encrypted channels, changing daily to prevent enemy forces capturing the correct code.

Somehow, the signal was lost right before the captain was able to relay the new password. This is human error, the password would normally be communicated right before being changed. This leaves us with our current situation. We don’t know the password, you’ll have to find a way to unlock the log-file.

This will give us insight into how the Narwhal sunk and allow us to begin the recovery. Given the hostile situation, it’s imperative we find the exact location of the Narwhal.

$~$
---

### $\color{magenta}{MATERIALS\ AND\ ANSWER\ INSTRUCTION}$
Instructions: Crack the password to open the ship logbook file (flagfile)

<a href="https://hacktoria.com/wp-content/contracts/flags/flagfile-lost-at-sea.zip">Download Flagfile</a>

$~$

---

### $\color{magenta}{METHODOLOGY}$
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

Okay let's build out a word-list by combining 2 of the words first, if we don't have any luck we can add `-` or up it to 3/5 words etc.
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

$~$

📌 BoΠeShΔdϴw³
