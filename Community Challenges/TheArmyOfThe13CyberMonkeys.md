## 24/7 Community Driven Challenges - only on the Discord Server.

## Challenge: ThƩ Δrmɏ ϴf thƩ 13 Cyβer MoΠkƩys

![TheArmyOfThe13Cyb3rM0nkey5](https://user-images.githubusercontent.com/117080369/208705547-1d23bbfd-256f-4053-a179-fb44974ad29c.gif)

### Steps to create (reverse order):

Using Google Earth / Maps I located a remote area with only a couple of Street View "Photo Spheres", The idea behind this was to make it Non-Contentious.

I settled on the location shown below:

As you can see from the location that there is only 1 "Photo Sphere" anywhere near.

![Screenshot 2022-12-20 154135](https://user-images.githubusercontent.com/117080369/208706713-20eb190d-4f2e-4318-9f69-16f3d9a38319.png)

Dropping the golden "Peg Person" in gives us a view of a realistic area.

![Screenshot 2022-12-20 154302](https://user-images.githubusercontent.com/117080369/208707346-23db1773-55e0-407a-bf08-b34291ab62ec.png)

Now we make a note of the actual coordinates.

![Screenshot 2022-12-20 154648](https://user-images.githubusercontent.com/117080369/208707933-ae3dcc19-942a-41e0-a184-4289483b07d4.png)

Paste them into what3words to get the challenge answer.

![Screenshot 2022-12-20 155905](https://user-images.githubusercontent.com/117080369/208710630-ed0a5fbc-6ff6-47b5-8533-059c06c4824e.png)

Now we have the final answer it is time to work our way back to the start.

At this point I create a text file with a story containing the answers (cryptic):
```
Meet me at the nearest Photo Sphere to avoid detection, I fear we are being closely monitored...
Make sure you are not followed; this mission is too important to fail!

Shopping List:
------------------
3 Hijabs
3 Gauge Electrical Wire 
Exactly .03 kilograms of used Coffee grounds
6 AA Batteries

40 Lbs of Plain Flour
Exactly .283 meters of Duct Tape

---------------------------------------------------------------------------------------------------------------------------------

Once you have collected everything from the list put it together, as it will be required immediately for the next step.

What 3 words can help us avoid detection?
```

1. meet me at the nearest `Photo Sphere`
2. `3` Hijabs
3. `3` Gauhge Electrical Wire
4. Exactly `.03` kilograms of used Coffee grounds
5. `6` AA Batteries
6. `40` Lbs of Plain Flour
7. Exactly `.283` meters of Duct Tape

Putting it all together (33.036,40.283) as stated in the story will give us coordinates close to our Google Maps `Photo Sphere` 

![Screenshot 2022-12-20 160919](https://user-images.githubusercontent.com/117080369/208712886-2b2106f1-3220-4a95-a327-9ec751eb55c8.png)

Next we will encode the story with the `Vigenere Cipher` using a `KEY` which we will write to a file also.

![Screenshot 2022-12-20 161400](https://user-images.githubusercontent.com/117080369/208713794-c1f7650c-1150-4754-8cbb-6d55dff6de3a.png)

Next we will encode the Vigenere Cipher `KEY` in `Base62` and write it to a file.

![Screenshot 2022-12-20 163848](https://user-images.githubusercontent.com/117080369/208719027-a9bca26a-39a7-4c44-8390-97da366fa164.png)

Now we have our `KEY` and `Story` file encoded we need to add them to a `ZIP` file and embed them in the `GIF`

> __Note__ The file name for the `Story File` is "shopping-list-put-items-together" encoded with the `Rail Fence Cipher` - this was a Rabbit Hole!

I am doing this from Windows, but it can be done just as easily in Linux / MacOS etc.

Run the following command in a `Command Prompt` 

Breakdown of the command: `image.gif` is the original file, `1.zip` is the ZIP file containing the encoded files and `TheArmyOfThe13Cyb3rM0nkey5.gif` is the output "new" GIF file.

```cmd
copy /b image.gif + 1.zip TheArmyOfThe13Cyb3rM0nkey5.gif
```

That is it, the challenge to prepared, the only thing left to do it test it.

### Steps to solve::

Run the `GIF` in binwalk.

```bash
binwalk TheArmyOfThe13Cyb3rM0nkey5.gif
```
We can see `binwalk` shows us that there is a ZIP file embedded.

![Screenshot 2022-12-20 163143](https://user-images.githubusercontent.com/117080369/208717611-d734837b-7065-4ab3-9dda-fbda01c37425.png)

Next we will extract the ZIP file, run the following command.

```bash
binwalk -e TheArmyOfThe13Cyb3rM0nkey5.gif
```
Now we have the extracted files we can decode them.

Decoding file `1` from `Base62` gives us:

> This is important: nuwqLNgZGDkBplGDVOLt

Decoding file `sopn-itptiestgtehpigls-u-tm-oehr` with `Vigenere Decode` using `nuwqLNgZGDkBplGDVOLt` as the `KEY` from file `1`gives us:

```
Meet me at the nearest Photo Sphere to avoid detection, I fear we are being closely monitored...
Make sure you are not followed; this mission is too important to fail!

Shopping List:
------------------
3 Hijabs
3 Gauge Electrical Wire 
Exactly .03 kilograms of used Coffee grounds
6 AA Batteries

40 Lbs of Plain Flour
Exactly .283 meters of Duct Tape

---------------------------------------------------------------------------------------------------------------------------------

Once you have collected everything from the list put it together, as it will be required immediately for the next step.

What 3 words can help us avoid detection?
```

What we need to complete the challenge:
* 33.036
* 40.283

Put these together gives us `33.036,40.283` coordinates.

Also: "Meet me at the nearest `Photo Sphere` to avoid detection" and "`What 3 words` can help us avoid detection?"

If we put those coordinates into Google Maps and activate `Street View` we get this: 

![Screenshot 2022-12-20 164856](https://user-images.githubusercontent.com/117080369/208721653-2fa75801-533f-4d42-adef-a7facc063823.png)

All that we need to do now is drop our "Pegman" onto the `Photo Sphere` and grab the coordinates.

![Screenshot 2022-12-20 165330](https://user-images.githubusercontent.com/117080369/208722227-6cd6f60f-7fd5-4bb5-a6d9-f39dc0227a93.png)

Paste the coordinates into what3words to get the answer.

![Screenshot 2022-12-20 165538](https://user-images.githubusercontent.com/117080369/208722623-965dcafc-f80c-4ccb-8ccb-753e5cae80d7.png)


BoΠeShΔdϴw³
