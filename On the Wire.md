<img width="600" alt="hacktoria-llw" src="https://user-images.githubusercontent.com/117080369/203552008-2d0e0a07-1815-485b-8f3f-ae7ed7258af8.png">

# Contract: On the Wire
![on-the-wire-cover-600x600](https://user-images.githubusercontent.com/117080369/204089579-690a2968-bd82-45b8-87b2-bc5093741877.png)

### Difficulty: Medium

### Mission Briefing:
Greetings Special Agent K. One of our field agents in Malaysia managed to physically breach the office of a corrupt politician. Doubling as a mole for a Chinese criminal enterprise, mostly smuggling endangered animals. In this case their evil business involves shark fin trade and other exotic food items.

During the breach, our agent successfully obtained several pieces of information on the organization. Currently this does not include their name, as they only communicate using anonymous messages and codenames.

We hope that the information, which includes pictures, floorplans, data dumps and packet captures. Will lead to a more complete picture of this organization. We know that the Malaysian government will be exceptionally happy to get this criminal enterprise out of its borders.

All data has been divided over several agents. Your segment for this contract is the analysis of a packet capture file. Figure out what is being communicated and find the message that matters. This message will lead to your Contract Card.

As always. Special Agent K, the contract is yours, if you choose to accept.

---

The second link you are directed to via the packet capture, is the password for the flagfile. (updated at 23.11.2022)

---

### Methodology:
Our task as specified in the mission briefing is to analysis a packet capture file.

We have a couple of options here, we could use an online tool like <a href="https://apackets.com/">A-Packets Online pcap file analyzer</a> or a tool like Wireshark.

My personal preference is to use Wireshark.

Let's fire up Wireshark and load the Capture file to see what is what...

After the Capture file loads we can see there is a LOT of data to sift through, 37723 lines of a "needle in a haystack", we need to make this a little easier to deal with.

![image](https://user-images.githubusercontent.com/117080369/204091791-97339f55-9ac1-4a11-966e-507aa326af69.png)

Let's start breaking this down to make it slightly more manageable. first let's set an `HTTP filter`

![image](https://user-images.githubusercontent.com/117080369/204092108-3b1b15f5-737f-43e8-bc24-6b9313b64150.png)

Now let's export this to a `CSV` file as this should make it eaiser to sift through.

To export to CSV: Select `File > Export Packet Dissections > As CSV...` give the file a name and click `Save`

Let's repeat but this time with a `DNS filter` set.

![image](https://user-images.githubusercontent.com/117080369/204092343-0610d247-578e-4c16-9580-e1908a7245b8.png)

Now we have 2 CSV files we can analyze.

Looking through the `http,csv` file nothing really jumps out that would be worth investigating further.

Let's move onto the `dns.csv` file...

Umm, interesting, there is a reference to `Pastebin` - this is often used to upload various nefarious files.

![Screenshot 2022-11-26 140316](https://user-images.githubusercontent.com/117080369/204092719-48a92132-0ac3-429d-bd07-04257c9d5682.png)

Let's see where that **Pastebin URL** takes us...

![Screenshot 2022-11-26 141142](https://user-images.githubusercontent.com/117080369/204093116-e2e3e9e6-a71d-4016-aa40-4c28981d7803.png)

Extract the `flagfile-on-the-wire.zip` with the password from the information gained above to get your contract card.
