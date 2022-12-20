## 24/7 Community Driven Challenges - only on the Discord Server.

Challenge: ThƩ Δrmɏ ϴf thƩ 13 Cyβer MoΠkƩys

![TheArmyOfThe13Cyb3rM0nkey5](https://user-images.githubusercontent.com/117080369/208705547-1d23bbfd-256f-4053-a179-fb44974ad29c.gif)

Creator: BoΠeShΔdϴw³

### Steps to create (reverse order):

Using Google Earth / Maps I located a remote area with only a couple of Street View "Photo Spheres", The idea behind this was to make it Non-Contentious.

I settled on here:

As you can see from the location that there is only 1 "Photo Sphere" anywhere near.

![Screenshot 2022-12-20 154135](https://user-images.githubusercontent.com/117080369/208706713-20eb190d-4f2e-4318-9f69-16f3d9a38319.png)

Dropping the golden "Peg Person" in gives us a realistic area.

![Screenshot 2022-12-20 154302](https://user-images.githubusercontent.com/117080369/208707346-23db1773-55e0-407a-bf08-b34291ab62ec.png)

Now we make a note of the actual coordinates.

![Screenshot 2022-12-20 154648](https://user-images.githubusercontent.com/117080369/208707933-ae3dcc19-942a-41e0-a184-4289483b07d4.png)

Paste them into what3words to get the final answer.

![Screenshot 2022-12-20 155905](https://user-images.githubusercontent.com/117080369/208710630-ed0a5fbc-6ff6-47b5-8533-059c06c4824e.png)

Now we have the final answer it is time to work our way back to the start.

At this point a create a text file with a story containing the answers:
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

1. nearest `Photo Sphere`
2. `3` Hijabs
3. `3` Gauhge Electrical Wire
4. Exactly `.03` kilograms of used Coffee grounds
5. `6` AA Batteries
6. `40` Lbs of Plain Flour
7. Exactly `.283` meters of Duct Tape

Putting it all together (33.036,40.283) as stated in the story will give us coordinates close to our Google Maps `Photo Sphere` 

![Screenshot 2022-12-20 160919](https://user-images.githubusercontent.com/117080369/208712886-2b2106f1-3220-4a95-a327-9ec751eb55c8.png)

Next we will encode the story with the Vignere Cipher using a `KEY` and write it to a file.

![Screenshot 2022-12-20 161400](https://user-images.githubusercontent.com/117080369/208713794-c1f7650c-1150-4754-8cbb-6d55dff6de3a.png)

Next we will encode the Vigenere Cipher `KEY` with Base62 and write it to a file.

![Screenshot 2022-12-20 161731](https://user-images.githubusercontent.com/117080369/208714424-42b221e7-136f-46f0-b900-3fdd72c4258f.png)

Now we have our `KEY` and `Story` file encoded we need to add them to a `ZIP` file and embed them in the `GIF`

> __Note__ The file name for the `Story File` is "shopping-list-put-items-together" encoded with the `Rail Fence Cipher` - this was a Rabbit Hole!

I am doing this from Windows, but it can be done just as easily in Linux / MacOS etc.

Run the following command in a `Command Prompt` 

Breakdown of the command: `image.gif` is the original file, `1.zip` is the ZIP file containing the encoded files and `TheArmyOfThe13Cyb3rM0nkey5.gif` is the output "new" GIF file.

```cmd
copy /b image.gif + 1.zip haha.gif
```

That is it, the challenge to prepared, only thing left to do it test it.

### Steps to solve:

Run the `GIF` in binwalk.

```bash
binwalk TheArmyOfThe13Cyb3rM0nkey5.gif
```

