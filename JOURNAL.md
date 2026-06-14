# Phoenix — Journal Export

- Exported at: 2026-06-14T18:58:56Z
- Project ID: 1056
- Entries: 32

## Entry 1
- ID: 4875
- Author: AethelVeritas
- Created At: 2025-10-22T09:37:00Z

### Content

I started off by basically just doing a lot of browsing to try and find out what I want to make.
The closest printer I found to what I want to build would be the [Salad Fork](https://github.com/PrintersForAnts/Salad_Fork?tab=readme-ov-file) by [3DPrintersforAnts](https://3dprintersforants.com/). It's basically a shrunk down Voron Trident.
![image.png](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NDM0NiwicHVyIjoiYmxvYl9pZCJ9fQ==--b539d78d0e7b84d2fac9fc696fbf655870e46315/image.png)

I'm definitely using 2020 extrusions instead of the 1515 used here though.

Pandora's Box (also by 3DPforAnts) looked very interesting, and I would love to attempt to build something like that, but having a belted z-xis would be too complicated, so I'll just stick to leadscrews for my first build. Speaking of the z-axis, I was considering of using one motor for all three leadscrews and using a timing belt like the X1C and the [Anicept Vex](https://github.com/invictus-anic3tus/anicept-vex/tree/main?tab=readme-ov-file) use because it's cheaper, but after asking around and looking at other printers I realized that z-tilt is too valuable to sacrifice. Oh and @Renovic on the HC slack provided an extremely helpful explanation comparing the different types of z-axis setups for fixed gantries:

> Motion type
Leadscrew
Sometimes can lead to z wobble
Integrated leadscrew are usually better since some couplers are a bit springy
Usually the simplest option
Look at trident
Belts
You almost always need a gear reduction
using a 60t and 16/20t pulley with 188t belt is common
Some use nema 17 planetary gearboxes but its sometimes expesive and usually has backlash
Highest gear reduction is worm, but thats also somewhat expensive
If its a really small printer(like v0 or slightly larger) you can get away with a 16t pulley or using bmg gears for a reduction
Look at 2.4 z drive or k3 z
Number of z motors/points
Triple Z
Pretty common because 3 points define a plane and allows for bed tramming with 3 motors
You can do 3 leadscrews without 3 seperate motors by using a timing belt to link them together, this is better than controlling a multiple steppers with the same driver
Double Z
Can be worse that triple Z, but its often better for packaging and usually used with linear rods on Z
Single Z
Only really used for small beds, you need to make the bed carriage really stiff for the bed to not bend or bounce

## Entry 2
- ID: 4876
- Author: AethelVeritas
- Created At: 2025-11-03T15:52:00Z

### Content

I mostly did toolhead research. I've decided I'll use the Xol Carriage from the Xol Toolhead, as well as the A4T toolhead, both of which seem really good. I did some research regarding on how to mount the belts to the carriage, and yeah the Archetype clips seem to be the best. For custom toolhead carriages, it's recommend to wrap the belts around some pins, and then make sure 3-4 teeth interlock. Seems to be the most painless way of doing it. I've decided I'm going to use a 20150 axial fan and two 4010 blower fans. That way, if my toolhead sucks (which it probably will), I can reuse the parts to make an A4T or Xol (another reason to use the Xol carriage). I'm also going to use the TZ 2.0 V6 hotend, as it's cheap and decent. I spent a lot of time trying to understand different toolheads and their creator's design choices. But I've now decided, after almost two days of research and browsing that I'll like place the A4T toolhead in the assembly, design the gantry, frame, and everything to that, and then finally make a placeholder/basic toolhead. Toolheads are difficult to make, but can easily be replaced with existing designs. Gantries, frames, and everything else not so much. 

Here are some great resources/references I've found:

https://github.com/Armchair-Heavy-Industries/A4T/tree/main
https://github.com/Armchair-Heavy-Industries/Xol-Toolhead
https://github.com/SartorialGrunt0/Awesome-Toolheads
https://github.com/PrintersForAnts/Voron-Construct

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA4NywicHVyIjoiYmxvYl9pZCJ9fQ==--57a75fe3f7580315bf250902e5311f0d6329881d/image.png)

## Entry 3
- ID: 4877
- Author: AethelVeritas
- Created At: 2025-11-17T22:44:00Z

### Content

So... for the past week or two I've been doing some more research. Scoured Discords, Reddit, and Googled. I can't come up with an idea for doing a new/original idea to make the monolith gantry unique, as I was instructed on the slack. I thought about doing diagonally braced 1515 frame and adapting the monolith to that, then using panels like the monolith zero but with a printed gantry, then 12 mm belts, and then 3030 extrusions, but none made sense/would fit my budget. Turns out 3030s are pointless if you use a bed with a smaller volume than 250 mm, 1515s are pointless for obvious reasons (2020s exist), and using aluminum side panels is obviously ridiculously expensive. I've come to the conclusion that there is no way I can adapt the monolith gantry to be original while still fitting inside the budget and using a 2020 frame. So, I've decided I'll just use the trident and monolith gantries hardware as a reference and build a gantry from scratch without looking at any other ones (as much as possible, that is). That way, I'll have a good learning experience as well as a fail safe: if my gantry does not perform well I can just buy some more parts out of pocket and adapt it to a monolith. Problem solved! ![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTIwMjcsInB1ciI6ImJsb2JfaWQifX0=--4f56af13c5e8f54e3d6b83900780c37a33dbe823/image.png)

The hours I've spent looking at the monolith's cad trying to figure out improvements are ridiculous lol.

## Entry 4
- ID: 4878
- Author: AethelVeritas
- Created At: 2025-11-20T08:23:00Z

### Content

[Something about belt tension too much for not live shaft idlers](https://youtu.be/4XGGuhTlJaw?t=152)


I think I've come up with an idea on how to use a monolith style gantry without directly copying it, but reverse engineering it with purpose in mind, as instructed by @Samliu on Slack! So what I'm think is that I'll move the motors *outside* of the frame, so like just push them back. I'm going to have an electronics backpack, so it won't look ugly or anything. I can also use adjustable sliding motor mounts as the belt tensioners, which is pretty neat, even though I liked the design of the Monolith tensioners. That way, if I ever try to print HT (high temp materials, such as PEEK or Nylon) and I want to make a good chamber, the motors will not heat up! Plus I'd have a little bit more Y space in the gantry, which would be really useful if I want to add a toolchanger mod later on. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTI2MjYsInB1ciI6ImJsb2JfaWQifX0=--68d13dfd7a9019f5eca9b14e3d5913df2bcc09c0/image.png)


Ok I'm scrapping the whole core-xy idea, which is sad, as I've just found a good idea for the gantry. I've done even more research, and I can't make it as good as I want within $400 usd + 100 which I can pay out of pocket, so yeah. As with Tanqish, people in both the Monolith and Ice Cream Factory Discord servers told me it's not really possible: a decent build would be at around $700. So here's what I'll do: I'll try and design an Idex cartesian printer using $400 USD budget. I can reuse a bunch of the extrusions from my Ender 3 V2 Neo, as well as the bed, bed carriage, and worse case scenario, a motor for the z-axis. The key here is that while trying to make a good printer that fits in the budget *I try and use parts that I can reuse in a corexy later*. So for example motors that can be double-sheared, 9mm belts, idlers, and pulleys, a good-ish extruder, a CAN board maybe, good drivers and mainboard, etc. I'll use cheap hotends because I need to get two, but the protxtruder is cheap and should work for both this and a future corexy. That way, once I build this printer and get it working, if I design a corexy I'll have a much higher chance of getting sponsors for it, and it might actually be doable at a following hackclub event. 

New Design Constraints: 
- Use as many reusable parts as possible. I'll reference the Monolith gantry BOM and see if I can use as many of the pulleys and stuff used there in my parts. 
- A few high quality parts are better than more medium-low quality parts. Why? Well because for a bedslinger IDEX I don't mind if I have like good motors but a heavy bed and thus can't reach high accels, because the main feature will be the IDEX. But if I reuse those motors later on in a corexy I'd much rather have them be good. 
- Try to use as many of the parts from the Ender 3 V2 Neo I have without compromising on performance too much. I'm most certainly going to use the existing 4040 Y axis extrusion, as well as the two side 4040s. That way I'll just need like maybe a front 4020 to connect them together + some 4020s or something for the z axis (I might even reuse the existing ones, though I doubt it: depends on where I mount the rails). Actually many designs only use three extrusions for the bottom, so like an H shape. No need to make a square most likely. 
- Decent print speeds, something like 300 mm/s^2 would be great.


I can get two 290 mm and one 350 mm 4040, two 400 mm 4020s, one 330 mm and one 345 mm 2020. Damn 2020s are smaller than I assumed: I thought they were 1515s at first. Ok so I need space for the two toolheads +  the bed. The bed is 235 mm, and the A4T toolhead cowling is about 69, so 235 + 80 (to be safe) x 2...wait hold on I can park the toolheads like over at least part of the bottom 4040s that sustain the Z axis. I'll have to figure out the x-axis first. I'm going to use MGN12H rails for both the gantry as well as most likely both sides of the bed.

[The steppers I'll probably use ](https://www.omc-stepperonline.com/4pcs-nema-17-high-temp-stepper-motor-55ncm-77-93oz-in-55mm-round-shaft-insulation-class-h-180c-4-17hs19-2504s-h-v1)
I'll most likely use a BTT Octopus Pro or something similar. On Ali it's around 85 usd with stepper drivers included. I have to see if I need some for the extruders as well, + CAN and shit.
Protoxtruder would be about $30 a pop. Fans from what I can tell would cost about $25 per toolhead. An BTT EBB 36 board is 15-18. Frame might be $40 USD max including shipping as I only need two longer 2020s and a 4040. 

two skr picos are like 22 per piece

## Entry 5
- ID: 4879
- Author: AethelVeritas
- Created At: 2025-11-23T22:21:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTM3MTMsInB1ciI6ImJsb2JfaWQifX0=--57fb354614d7db695c0934b0df75211d25446023/image.png)

Soo...busy two days. Did a lot of stuff. I did some more research (yes, I'm a perfectionist, I'll research and double-check like crazy), and after some back and forth in the Ice Cream factory Discord, I've decided that I'll do a [Ratrig V-Cast](https://cad.onshape.com/documents/d85f63cb1dd00c47513242ef/w/078df75818db59591633b24e/e/6d79b98fe36ffb8e62f69638) style X gantry. This is after I tried to make a like an offset (relative to the 2020 extrusion) idler tensioner and motor mount. 

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTM3MTYsInB1ciI6ImJsb2JfaWQifX0=--6311d11608d127f083824185ed0b4ed2452b95c1/image.png)


![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTM3MTUsInB1ciI6ImJsb2JfaWQifX0=--63584a9638177a8c47ed15b742a6774bb2e77ad9/image.png)

Thing is that if I did this like this, then because of the extra material needed for the tensioner, the idler and thus the belt paths would be off-center relative to the center of the 2020 extrusion. Wasted several hours on this, but yeah as I said I scrapped this design.

The next several hours were spent iterating on a motor mount inspired by the V-Cast's, but from scratch and improved to support double shear as well as live shaft idlers. Here's a what I came up with (to be refined tomorrow): 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTM3MTcsInB1ciI6ImJsb2JfaWQifX0=--630bc3767399311f5ca328405db62d77d1f7b81c/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTM3MTgsInB1ciI6ImJsb2JfaWQifX0=--ceac3989be539697bb2c2036f4771087a71ea9db/image.png)

The tolerances for some of the parts such as the bearings and shafts are inspired from the monolith gantry. Also I spent like another hour figuring out how to use Super Derive, which is an amazing Featurescript that's basically the Derived feature but on steroids, allowing you to remove, add, and intersect your derived parts,even several at once. Now what I did was I made kind of like a bearing with tolerances, and then used said feature to subtract it for the top two bearings "holes" of the gray part. This saved me quite some time and sketching. Well technically I lost time because I had to troubleshoot the feature, but now that I know how to use it it's going to save a lot of time, as I'll have to use more of the same bearings and heat inserts in other parts of the printer. Also dang the hours are flying! Can't believe how much time is wasted on searching and finding dimensions as compared to CAD. Over 50 hours already :'(

## Entry 6
- ID: 4880
- Author: AethelVeritas
- Created At: 2025-11-24T16:07:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTQwMjQsInB1ciI6ImJsb2JfaWQifX0=--b088f610d8b763e5a168d9ec8f49fd9d990d1a0d/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTQwMjUsInB1ciI6ImJsb2JfaWQifX0=--760c6a5bf268493480c6d40f72ed2a6113afd6ee/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTQwMjYsInB1ciI6ImJsb2JfaWQifX0=--93512fe75f6fce18f595cd2bcec898dde675a7b8/image.png)

Finished doing the assembly for the x gantry, and refined the motor mounts+ joints a bit more. Took some time because I had to manually import parts, readjust the printed part to fit screws (using 35 mm as the part itself is 31 mm now and the motor + tnut screw holes are about 4mm), and learn how to make better assemblies. I manually imported the screws and bolts only to realize that the standard content library did in fact contain the lengths I was looking for but under ISO section, not DIN. I'm dumb. Also used the "Frame" tool to generate the 2020 extrusion.
Oh and I've also decided to use the my main task app, SuperProductivity, to track how much time I spent on what on the project.  
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTQwMjcsInB1ciI6ImJsb2JfaWQifX0=--21de326d207e6c19ee572583681b8d1dd82c5a4f/image.png)

Should have done this from the start tbh.

## Entry 7
- ID: 4881
- Author: AethelVeritas
- Created At: 2025-11-29T09:45:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3NDksInB1ciI6ImJsb2JfaWQifX0=--5645487c7414e122c938b3395fc9622f7c8de716/image.png)


Soo...this was a lot harder than I expected and took me an abnormal amount of time to design. At first, I thought I could get away with using a tensioner on the bed, similarly to what the lh-stinger does and what Mitsubishi makes does in his Ender 3 upgrade video. This would have simplified the motor mounts, as I would only have to design one and mirror it, a much simpler part at that. But the Lh-stinger uses a custom carbon fiber bed, which brings the weight down from the about 1.8 kg of the original bed to about 700-900 grams, so it can afford a few extra grams for the tensioner on the bed. I cannot afford such a bed, and it's not worth it for my usecase, so yeah motor tensioner it is. The main two projects I derived my inspiration from are [Kevender](https://github.com/kanin2/KevEnder/tree/main) and this [AWD Ender 3 mod](https://github.com/CarnageMarkus/ender-3-pro-awd-y). Even though I kind of liked how AWD Ender 3 mod made use of the pre-tapped screw holes in the standard 350 mm 4040 bed extrusion, the Kevender seemed more well-thought and practical, so most of my inspiration/references were derived from that. Deadlock from the Ice Cream Factory Discord provided me with a great formula regarding how how long do I need to tensioner to tension:
>You want the tensioner to cover at 2% belt length + whatever wiggle room you want for easy installation.
If you're tensioning on an idler or pulley, it's halved since 180° doubles it
So assuming a motor tensioner, 1000 mm belt length and 4 mm leeway you'd get 12 mm

But seeing this has kind of made me worried regarding the toolhead tensioners I'll be using: I don't know if I can fit about 12 mm of tensioner travel in the toolhead without it disturbing the COM and weight too much and besides that I'll also have a longer belt length. I guess I'll cross that hill when I get to it. 

### Nov 26-27
This was basically a failed attempt. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3MzUsInB1ciI6ImJsb2JfaWQifX0=--2a646e52b9b0ee3a6d6f254de14fe65188eb1fdd/image.png)

I think I spent like 6 hours on this in total, and yeah the way I went about it was crappy as hell. My biggest mistake was that I did not make a mental "feature timeline" of sorts before starting, and as a result there were a lot of unnecessary unoptimized features and sketches. From now on, before trying to make a new part (especially if it's inspired/derived from an already existing one) I'll first try and write down or just mentally note how I'll go about it. Things like what will the main sketch contain? How can I make it as parametric as possible? What tolerances might need adjusting, and do I make variables for those to help with said adjusting? In what order will I make the features? Should I use offset for a feature or just use a new sketch that'll be placed on the previous feature and thus relative to it?  Things like that. 


## Nov 27-28
Started a new part. I've decided that I'll reference as much of Kevin's design as possible in order to save time regarding screw positioning and tolerances, but I'll adapt it a bit because I'm using 9mm belts and live shaft idlers, as well as 55mm motor shafts, all of which interfere quite a bit with Kevin's current part. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3MzYsInB1ciI6ImJsb2JfaWQifX0=--01a29be0fb1605fb37a35081e1234ff973cd3925/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3MzgsInB1ciI6ImJsb2JfaWQifX0=--6104f43198ebe67cc9569d13b023e05e972e31fd/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3MzksInB1ciI6ImJsb2JfaWQifX0=--a5b204b8110211bc6f724cc09e66214dbe738843/image.png)

So these are basically my new versions. I made a slot for the longer shaft to pass through, added flanged bearings for double shear even though normal bearings would have probably been easier (so that if need be I can reuse them for monolith later on), used 4 short screws and 2 long external ones instead of 2 short and 2 long like the Kevender used for the sliding motor mount, and added space for a dehubbed 20T 9mm pulley (and double sheared and aligned that, obviously) and yeah. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3NDAsInB1ciI6ImJsb2JfaWQifX0=--99638d2dc6c8b5c4b676acd9a77c03b29084e5e2/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3NDEsInB1ciI6ImJsb2JfaWQifX0=--910c8e5c2acdd53f55797c87c37de56f30ebb0fd/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3NDIsInB1ciI6ImJsb2JfaWQifX0=--618ba6b3652a559754a083cfe25dfb91861d802d/image.png)

I'm a bit worried (look at the last pic) for the bearing to like rub against the white outer part, but if needs be I can adjust that later and either make a small detachable lid of sorts or just embed the bearing deeper in. 

And then obviously I also made a pretty simple back motor mount. ![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTU3NDQsInB1ciI6ImJsb2JfaWQifX0=--8b815b34ef6bf307d8a1c91c5ac3de43e7317ac4/image.png)
And I also started working on the full y-axis assembly. I'm using a subassembly for the front motor mount tensioner, and I'll probably add screws and motors to the back mount as well just for the looks, but besides that all that remains is to add the bed (which is going to be the standard Ender 3 bed with a mount for the two parallel MGN12H rails). 
In total, I think I spent about 10 hours on this. Did like a 3h spree on the night of the 27th, then several hours the next morning, and another 4h on the night of the 28th.

## Entry 8
- ID: 4882
- Author: AethelVeritas
- Created At: 2026-01-02T08:10:00Z

### Content

One of the things I'm worried the most regarding the Z axis is the gantry crashing into the bed if I do belted z. At first, I hoped I could get away with how the LH-Stinger does it: the gear reductiong + cogging toqrue suffice to at least dampen the gantry's fall. With the help from some people in the Ice Cream Factory discord, I realized that it would not be enough:
>For class B insulation hybrid steppers the detent torque is usually around 5% of the holding torque 5% of 400 mNm is 20 nNm 20 mNm × gearing / efficiency ≈ 85 mNm With 20T final pulley (assumed) you get 85 mNm / pitch radius ≈ 13 N 1,3 kg per stepper, while with a safety ratio you'd want at least 3,5 kg per stepper

This clearly wouldn't work for my estimated gantry weight of 4 kg. Did some more research and I found that [Z motor brakes](https://www.formbot3d.com/products/z-motor-brake) are a thing, but they are not cheap.  Someone suggested BMG Z, and Renovic also said that >
>"I'm using creality stock x motors for z with a 4:1 gearing. Your gantry is likely only 300g more from the extra toolhead and axis length, but I have aluminum plates and a 120mm fan mounted to the x axis. So if you use better motors or higher gearing you will likely be fine"

But Ocho and Deadlock said that 10:1 geared would hold about 1.2 kg before drop, and that the best solution is constant force springs. For now I'll try to just make the Z-axis and worry about adding springs later. 

For the belt tensioner, I want the pulley+motor to move about 6mm, using the formula provided by Deadlock mentioned in my previous post. I'm going to be using a 80t pulley and a 188mm belt, like the LH-Stinger.
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NjY4NTgsInB1ciI6ImJsb2JfaWQifX0=--33cdc7b06b798551c54970a9697f20d00e9abdb3/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NjY4NTksInB1ciI6ImJsb2JfaWQifX0=--844a607e9a7385bd21534285b9209431ccb29ebb/image.png)

Ok so here's what I've got so far. Obviously very LH-Stinger inspired (black part is from the latter for comparison)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NjY4NjAsInB1ciI6ImJsb2JfaWQifX0=--afe0ad4cdc81b7ca7f535b4e35b7d797dbb55c70/image.png)

I'm using F695 flanged bearings though (because I want to be able to reuse them for the monolith if I ever make one), and I'll be mounting it differently. As you can see, the LH-Stinger uses two holes right beneath the pulley for two M3 x 22 screws, as well as another one right in front of the motor. I'm using obviously different frame, so that's not going to work for me. What I'll do is I'll use one M5 underneath the pulley, for the like Y-axis extrusion, and then another one in front somewhere for the X-axis extrusion. That way it'll be centered but still solid. 

## 26th 
Ok....long time no do nothing. Had some family stuff going on + exams, so I haven't really gotten around to working on it. Let's see if I can somehow speedrun the Z, electronics, toolhead, and BOM in 6 days lol. 

So, if I want to add another screw right beneath/in front of the 80t pulley I'll need to lift the whole thing up a bit, which isn't really convenient, because that'll use more material + longer screws. I've got 50 mms from the extrusion to the start of the Z-rail, and the part is currently 43 mm tall, so I do have some space left but yeah. Why use more material if it it is not necessary. Plus a protruding "tongue" for the screw emerging from underneath the 80t would kind of be a weak point, as it's only connected to the part on one side. Not that it matters much, but why not stick to good design principles for practice at least.

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NjY4NjEsInB1ciI6ImJsb2JfaWQifX0=--ec83157e2bb5be10b8ece4cbfc50ceeb6b38a05e/image.png)

Just realized that using an m5 screw like I intended would result in this abomination, as this slot is much closer to the vertical extrusion than I thought. Might have to just do like a 2-3 M3 screws after all. Anddd an M3 wouldn't fit either. Argghhhhh! I might have to try and like screw it in the vertical extrusion. Not optimal, but yeah.

Oh by the way I got a quote about how much the rails would cost from Brazuka over from the Monolith discord.  
>2x 350 MGN12C - US$25,80 2x 300 MGN12H - US$23,20 1x 400 MGN12C - US$17,60 (2 carriages) around 24 shipping

This if for the in-house BST rails, not even airtacs/hiwin... I'm screwed.

Ran into another problem:![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NjY4NjIsInB1ciI6ImJsb2JfaWQifX0=--e00488e62b84ec528e97cd3ada9c8f24ab58981c/image.png)

When trying to edit the mate that connects the gantry to the rail block, I get a ton of over-defined errors. Onshape mates are weird...I had to redo a large part of the assembly.

## Entry 9
- ID: 4883
- Author: AethelVeritas
- Created At: 2026-01-05T19:50:00Z

### Content

I'm switching direction. Again. It's annoying, and I really wanted to build an IDEX, but with a new law being introduced here that adds a tax for any package shipped from outside of the EU I just can't do it anymore. Even if this wouldn't have existed, I was still pushing limits with the budget. I would have payed at least $150 out of pocket, and just for a cartesian IDEX, especially a first printer design, I don't think I'd be willing to pay $200 (which is what I would have most likely had to pay given an error margin). Instead, I'll try and focus on just a simple Cartesian bed slinger. My Ender 3v2 Neo is still collecting dust, and I'd like to put it to some use. With the IDEX I would have reused some parts from it, such as several extrusions, the PSU and the motors for the Z, and I'd like to use even more parts for this new build. Ahh speaking of, I'll have to come up with a new name now. Orthrus was an amazing name for an IDEX (Orthrus in Greek mythology is Cerberus's two-headed brother by the way), but for just a bedslinger it won't be appropriate. I'll worry about that later. I can reuse all of the CAD and researched parts from the IDEX for this, except the X gantry CAD, obviously. The Z will also probably need some more modifications. I still want to keep trying to use as many reusable parts as possible, with the reference being the Monolith gantry, as before. If I want to build another printer in the future or if this one doesn't work out as I expected there's no point in parts going to waste/buying new ones.

But this time I'm using my damn brain and building a more detailed tentative BOM first. I'll still be using the BTT Octopus Pro, as it's a good mainboard for future builds as well, and most importantly it can run 48v, and I'll definitely be wanting a 48v PSU now. The board + four TMC5160T Pro drivers is about a hundred bucks on Ali. I think I'll use the same motors from steppers-online, as I haven't really seen another decent option that is long enough for double-shear without costing an arm and a leg (LDO Speedy Power HTs I'm looking at you lol). I might use 9 mm belts for the X now, seeing that I don't have to worry about two overlapping belt paths. Still going to stick with the Protoxtruder for obvious reasons (cheap-ish + good), but I'll be using a different hotend hopefully. 

Did some research on the PSU, which seemed really confusing at first. Max amps for the HT 1.8 deg Nema 17 55Ncm is 2.5A, so 48V * 2.5A * 4 motors = 480W. Ok I'm dumb ignore that. After some blindly stumbling across random PSU info on the web I did some digging in the Ice Cream Factory server which payed off, as usual. Deadlock gave [this](https://discord.com/channels/733350014805344377/733350015384420396/1246963470403108864) formula to calculate wattage:
>Estimate (a bit low but a starting point) is P = ((U_induced_RMS × I_RMS) + (I_RMS² × R_coil)) × 2 
>U_induced_RMS you can calculate from speed, current, inductance and steps per rev

But this seems a bit overkill for just a rough estimate, and I don't have the brain power to sit down and do the math right now. So after some more research seems many people use a 200W 48V just fine, including Brazuka (who gave me the rail quotes) from the Monolith Discord. That seems to be for a 2WD monolith gantry though.... Ah dang it I'll deal with it later: I don't need exact numbers for a rough price estimate. For now, I've found some Meanwell PSUs sold by steppers-online, the same place I plan to get my motors from, so I'll save on shipping.

Moving on to the toolhead. Probably should have started with this to be honest. Gonna use a klicky probe (obviously), Protoxtruder 2.0, and I was thinking the Peopoly Lancer Long, until I realized that with shipping that would be about $70. Now I have to find a new hotend. Never mind that the toolhead is on hold again. Probably going to use the Dragon Ace or as Evan suggested on the slack a TZ 2.0 V6 with a Trianglelabs MZE (meltzone extender). But still have to do some more asking around.

I'll have to rework the Z unfortunately, because if I keep the standard frame configuration then the lower motor mounts wouldn't fit under the belts. Fortunately, I don't have to start completely from scratch. The orientation of the pulleys will look roughly like [this](https://www.printables.com/model/932314-belted-ender-by-squirrelf#preview.R1zwE), so basically just flipping the motor mount across the Y axis. This remodeling is a lot easier as I already have experience from the first Z mount attempt. Here I made a version of my last version of the IDEX Z mount so I can always revert to it, then went to the base motor sketch and flipped across the center, and also the whole sketch better and clearer (even though it doesn't look like it haha).

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzQyNTAsInB1ciI6ImJsb2JfaWQifX0=--784b63ce09b826ad8fcdc3bc5934507da5b0cbd9/image.png)

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzQyNTEsInB1ciI6ImJsb2JfaWQifX0=--04c7196b981cb8710bab2e628cc11f4f3210615b/image.png)

Oh and I started tracking what I did again. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzQyNTQsInB1ciI6ImJsb2JfaWQifX0=--b1182ca5e486360c569c274761ff0808a048fd27/image.png)

## Entry 10
- ID: 4884
- Author: AethelVeritas
- Created At: 2026-01-07T22:42:00Z

### Content

My God am I dumb!!! So I've been struggling with like getting the proper angle and mouse position to select what I want to add a mate connector to for so long, and now in frustration I just googled it, and turns out that once like all the white possible mate points appear on the screen you can just hold shift and select which one you want. 

So I've been looking the BOM to see where I could make a compromise or something because I'm like already over-budget with the shipping and all, and I realized that even though AWD X sounds nice, I don't really need it. Like the X gantry has a relatively short belt path and the LH-Stinger goes insanely fast and only uses one motor. The main limiting factor will obviously be the bed, not the X axis. Well a motor is 14 USD, so I guess I'll see. Might just buy a set of 4 to save $7 off of one and just pay that out of pocket.

Started working on the X gantry. So I have a dilemma: I'd  like to use a 9mm belt even though it's overkill as I'd have multiple reusable parts left if I ever dismantle this thing and because a 9mm will obviously be stiffer. But, that would mean I have to run like both 'halves/lines' of the belt underneath the 2020 gantry extrusion, which is not ideal for the COM of the toolhead. So, I guess I'll just settle on doing a AWD 6mm X which will still be overkill but a bit easier to work with. Anyway, the X is not going to be the limiting factor in any case, but rather the heavy bed + carriage of the Y.  I'll still do a toolhead tensioner like the LH-Stinger even though I'm doing IDEX anymore because I really can't think of another good alternative for AWD X: I really don't want to add any weakness by trying to tension one of the motors.

I don't know if I'll do this now, but later on I definitely want to make a shape similar to how the Monolith gantry does it that I can subtract for press fit bearings. I have one for F965 bearings currently, but well it's not very "press fit optimized".  So basically a shape that's the negative of this:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNjcsInB1ciI6ImJsb2JfaWQifX0=--2eb037d9edd252eeb3ccc4aad929b30d07ae5a32/image.png)

12 sided polygon instead of a circle (similar dimensions, obviously), so it works better for press fit. I'll probably just take a part from the Monolith and then boolean and cut up a shape I can then use to remove multiple times from parts I want to add bearings to. 


So after several hours of measuring and designing, this is the very rough part I came up with:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNjgsInB1ciI6ImJsb2JfaWQifX0=--2803bf813355711f9e12e8830289f2e3af3ed6d7/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNjksInB1ciI6ImJsb2JfaWQifX0=--a83493446005692f8c27eadae951725a50521d7d/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNzAsInB1ciI6ImJsb2JfaWQifX0=--36f3deeadb9d95b31385e03258e1404ddf65fe49/image.png)

While this does in fact seem like a rigid and good part, and while I do like the added rigidity given by making the top green part bolt onto the extrusion just like the back grey part, I've just realized that this will actually make me lose quite a bit of X travel, and make the placement of a Klicky or nozzle brush rather impossible. So, I'll have to chop off some of the green part. The back grey part shouldn't interfere with the toolhead if I design it properly, as it should be able to move like in front of it. Arggh. The amount of things/design constraints I discover about only after designing something is hilarious. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNzEsInB1ciI6ImJsb2JfaWQifX0=--376af3f2dc212d3da2861a2cf6d55e912bb138ed/image.png)

Regarding press fit bearings: I don't know if this'll hold up to be honest. Hopefully the tolerances will be tight enough. If not I guess I'll just make it be on outside, but that'll make everything much harder to print. 

This isn't perfect, but it should do for now. I'll have to add an endstop switch mount and the screws in the assembly later once I get a rough draft of everything. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNzIsInB1ciI6ImJsb2JfaWQifX0=--0f51f01f8545d84da47a75eff9aa93d3daa9a63e/image.png)


Now let's deal with the elephant in the room: the toolhead. Renovic over on the Slack said he got to 30K X accel and 19k Y with v-wheels, AWD X and Y and a LH-Stinger toolhead modifed for the Peopoly Lancer Long hotend. I'll be referencing the LH-Stinger toolhead a lot for general measurements probably, especially for the belt tensioner (that the EVA toolhead series). Als I really like the Xol and A4T, so I might reference some of those too. But firstly I most decide on the hotend I'll use, and then what fans, so 5015, 4010s, or those big square turbos that look insanely cool but eat up a ton of X space (saw [this using them](https://github.com/WV-design/Trinity-toolhead/) in the Monolith Discord and I think it looks so nice and minimal). But as I have my motors shifted a bit downward for a decent belt path it'll interfere with them most likely if I use the turbos. I think they are 3612s.

>PTC heaters are the most cost effective heaters and also the most safe thanks to them increasing in resistance. There are two sub types of PTC heaters we see: Rectangular and circular PTC heaters. Circular PTC heaters are known for breaking over time due to thermal expansion applying pressure on the heaters circular face. Circular heaters are not the correct choice because of this.
>thermistor placement is 1 of the critical choices in hotends. Due to the nature of hotends, there will always be more losses at the bottom of hotends due to part cooling fans blowing at nozzles. Having the thermistor as close as possible to the nozzle reduces the effect/ time it takes for the thermistor to see change in tempature. Software is 1 way that this issue is beingg circumvented to some extent with [https://github.com/KalicoCrew/kalico/pull/333](https://github.com/KalicoCrew/kalico/pull/333 "https://github.com/KalicoCrew/kalico/pull/333") using [https://marlinfw.org/docs/features/model_predictive_control.html](https://marlinfw.org/docs/features/model_predictive_control.html "https://marlinfw.org/docs/features/model_predictive_control.html")

Some info by Burgo that I scrapped from the rather messy hotend info thread in the knowledge-depot of the Ice Cream Factory discord server. After some more digging through the long and tedious messages of multiple Discord servers I have come to the conclusion that I cannot do better than get a Dragon Ace lol. Burgo recommended it, Renovic recommended it, the A4T toolhead setup recommends it, so yeah. $70 USD but such is life. Definitely going for the PT100 version, as I want to be able to print at higher temperatures in the future if I ever reuse the damn thing. Tomorrow I have to deal with fans, but enough for today (yes I know I'm a slow worker, I do a lot of research).
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6NzcyNzMsInB1ciI6ImJsb2JfaWQifX0=--b1ca5efd8a3c27ba836ca4c8a3403becd9c7aeae/image.png)



Never mind that I'm doing more fan research now. https://www.youtube.com/watch?v=mxb71Ndg6tY Found this video, seems useful. According to the latter axial fans (4010s, 4020s) move a high volume of air at high pressure, and the airflow is parallel to the fan axis, while radial fans (5015s) move a low volume of air at high pressure, and the airflow is perpendicular to the fan axis. 4010s are not designed to force air through small ducts, and require a better understanding of fluid dynamics to make them good.  I just asked in the Ice Cream Factory Discord regarding fans, and CarVac shared a bunch of information:
>4010 is for compactness. notice that stinger is a bedslinger and uses that to spread the fans wide so it makes the most of 5015s. there are narrow mouth and widemouth 5015s, the widemouths are often on oem chinese 3d printers. 4020 is similarish to 5015, that's on prusa mk4s and core one. dual 3628 moves high volumes of air, good for fast printing of large objects but it's not as good at point cooling for bridges or tiny objects (speedboating). And ratrig uses a single 4028. The real high performance cooling is done by outsourcing aka cpap.
>CFD is almost completely foor part cooling duct design. Why not simply do test prints? Way faster. And the part geometry under hte nozzle matters, and the Colorful Flow Diagrams don't tell you what cooling is. Also cfd isn't informing you much besides "is the flow going in this general direction", it doesn't know how flow exits the fan nozzle (more on the outside, less on the inside), you and therefore it won't know your blower's pressure/flow curve...it's really not hard to make a solidly functional duct with a little trial and error. Making _the best_ duct for insane printing speeds is another story.But cfd isn't helping at either end: both are highly dependent on trial and error. 
>
>Especially for a bedslinger? that's easy you only have to worry about two things: aim and nozzle area. Smaller nozzles are better with modest (6500 rpm) 5015s because they restrict more, generate more pressure, and convert that pressure into flow velocity but the same nozzle will limit the cooling capacity of a faster (8500+ rpm 5015) fan because above a certain flow speed your cooling doesn't get thaaat much better, while you can benefit from a larger area being cooled with sufficient-velocity air. And aim? aim for just below the hotend nozzle, and not 180° opposed from its paired part cooling duct.

Oh and I'll probably get two 9733 fans in the future and print the LH stinger sheet cooling. Seems it helps a lot, and two fans are like $15-20, but I don't have the time or knowledge to design sheeting cooling now as well.
On a random note I'm thinking of using the drill press (if it still works) to remove more mass from the bed carriage.

## Entry 11
- ID: 4885
- Author: AethelVeritas
- Created At: 2026-01-11T07:00:00Z

### Content

So. Ducts. I'm dead :)) 
Found [this](https://www.youtube.com/watch?v=YijwkQCOBEA). Summary:
- Golden rule: Narrow ducts gradually! Don't narrow a duct by more than 11 degrees.
- Every fan has a tipping point, after which if you narrow the duct more you start loosing pressure instead of gaining it as it chokes the airflow.
- You need to find this ratio: outlet_area/input_area x 100 = final reduction 100%. The you have to do test prints and see (with water or cardboard) at what point does the duct start to choke the airflow.
- The easiest way to start designing a duct is place your start and end sections and then work from that to the middle.
- The duct *must* be as smooth as possible. Try to use big mellow curves, avoid sharp angles/curves.
- Minimize the duct perimeter as much as possible. The perfect duct shape is a circle.
- The shortest possible duct will under-perform compared to a longer duct that has smoother transitions. 
- Don't cut/transition to the final outlet cross-section too soon, as large ducts are more efficient than small ones.
- Aim the airflow so that they just clip the nozzle. The actual airstreams will obviously spread out differently depending on where they intersect with what you are printing, bu this is a good practice. 
- If possible, end the ducts with a short straight or slightly tapered segment instead of placing the nozzle right at the end of a bend, as this helps produce a more well-formed air ject.

Also found this really cool video series from NeedItMakeIt regarding ducts: [this](https://www.youtube.com/watch?v=1pMJQetyA4A) and this [this](https://www.youtube.com/watch?v=jC5yuF9fMp8&list=PLQzIeH3L1tsXJd5ccb0gNgEOIvACHzmi5&index=22) are the two most useful ones.

 As I wrote yesterday, CarVax recommends not using CFD, and same with Colpher (aka James Pray on youtube, whose video I just linked). But, MetricsTonofCooling, whose designs Ocho recommend I look at, said this:
>For me, CFD was necessary in many ways. Tube fill, upper tube air speed, lower tube air speed, nozzle air speed, and most important, air direction of the nozzles. Aiming (angle)of the nozzles themselves won't change air direction much. Most of that work is done preceding the exit orifice. It can be quite challenging to design a duct. Most of which the problem, mostly with high speed, is the dwell time over the part needing to be cooled as well as part of the model that needs to be cooled when the toolhead is not directly over it. I have two types of ducts: UFO-N-Ator and VaLvNaTor. One is a ring with 4 ports aimed at the nozzle, with a doughnut/plenum feeding the orifices. The second is a duct with valves in them, like a car engine, that spray air outside the model and 2 ports that aim at the nozzle. Both ducts work, but I tend to want to use the UFO over the valve duct. The UFO duct is high velocity air and the Valve duct is high volume, low pressure. If you want to get into such a thing, be ready for pain. What you think will work seems to be opposite, so make a crappy one that you don't think will work 1st, LOL. There is no CAD available for VaLvNaToR (.stl only) and .step or .stl for the UFO duct. I believe there is a mistake in the export of the UFO duct listed below. For some reason when exporting, there is a piece missing in the body or blocked, can't remember which, but the .STL's don't have that issue.
[-UfO-N-AtoR- Duct by XrocksaltX](https://www.thingiverse.com/thing:6779529)
[VaLvNaToR V2 VZ 235 duct by XrocksaltX](https://www.thingiverse.com/thing:6313653)

I think I'll use CFD, but the main conclusion I've drawn from all of my duct research would be that it's very important to prototype and test the fans empirically. So I think the best approach would be to deal with all of the other parts first and leave the toolhead for last, as I don't know how much time that will take, and as it's basically the most important assembly of the whole printer I want to do it well. It's better to finish everything else now, and that way I can spend as much time on the toolhead as I want without having to stress about the rest. It's not like I'll be able to design anything good before actually getting the parts and testing anyway. 

New version of the Z motor mounts:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NDEsInB1ciI6ImJsb2JfaWQifX0=--7fd6e117957c00eefe75500f1e3b4afa3bcff699/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NDIsInB1ciI6ImJsb2JfaWQifX0=--f238abbcdec827396c898a217e04ecdd5ba13277/image.png)
Those long horizontal semi-circle indents exist so that I can slot in the M3 screws, as the heads wouldn't fit in otherwise. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NDMsInB1ciI6ImJsb2JfaWQifX0=--19350333fe70bc4d765d4874ab3c50f0ea2e3d39/image.png)


I could have used a longer screw and had the screw head hole smaller and thus higher up (as it wouldn't interfere with the pulley cutout space), but well I'm already using 20mm M3s in this build so why buy another size. I can always change this later on if need be.

## Entry 12
- ID: 4886
- Author: AethelVeritas
- Created At: 2026-01-12T19:09:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NTIsInB1ciI6ImJsb2JfaWQifX0=--3e2e689a385cc63c7409f3ed312e4a263e85e842/image.png)
Currently the idea would be to use some heat inserts and screws to mount a Z belt clamp to the end of the grey part protruding backwards, but I feel like that would not be optimal at all, and most importantly too weak. I was thinking of maybe having that part encase the back of the motor for extra strength or something.

I again asked in the Ice Cream Factory discord for advice, and Ocho responded suggesting using an aluminum motor mount as well as flipping the Z rails to the front of the extrusions and bolting the extrusion directly into the carriage with M3s. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NjcsInB1ciI6ImJsb2JfaWQifX0=--53997b1386bf459b7deb95272a89d3a8e8ed4ed5/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NjgsInB1ciI6ImJsb2JfaWQifX0=--8e86860cc5cea278d5b652a08732843a6a780015/image.png)
Ocho suggested an interesting setup, but doing something like this would mean that I can't run the belt through the bottom slot of the 2020 extrusion like the stinger does it, and that would make things more regarding the X belt path. And also it's a lot more complicated because I have to drill and tap those m3 screw holes as well as a larger slot for the belt. 

Inspired by that, I thought about doing something like this:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NzAsInB1ciI6ImJsb2JfaWQifX0=--c4bc8bc1de3471d6d48d88c4775f3becf80ae25d/image.png)
One end of the belt is secured into that slot and the other end in a similar slot above, and then the like parallel outer half of the belt would be in front, but obviously that be impossible because of the extrusion, which cannot fit between a belt on standard pulleys. 

Another idea is have the blue part run right in the middle of the belt, as the latter being 9mm and the standard pulley pitch indicating that the minimum distance between the parallel halves would be about 10mm if I thin that section out a bit I should have it.
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NzEsInB1ciI6ImJsb2JfaWQifX0=--3bcdb6494c3de20dc38c32b0ac6a863b78d57d4d/image.png)
So roughly something like this:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NzgsInB1ciI6ImJsb2JfaWQifX0=--cb98dfad43f8f43f659667383d761c3732476529/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODA1NzksInB1ciI6ImJsb2JfaWQifX0=--5476835e89b6400cecfa9b5ee6d61d94ffa7514d/image.png)

## Entry 13
- ID: 4887
- Author: AethelVeritas
- Created At: 2026-01-17T23:13:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODQ3NzcsInB1ciI6ImJsb2JfaWQifX0=--07103db0a8a7a414f1724eddf30794dff7aacb2c/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODQ3NzgsInB1ciI6ImJsb2JfaWQifX0=--65e15156621df15fe6909520b6d5ceaf1f550f53/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODQ3NzksInB1ciI6ImJsb2JfaWQifX0=--0790732f8ac42190591caef1714693eaa7451456/image.png)
Made the Z motor mount from scratch (for the third time). The belt path is now centered on the center of the out most channel in the vertical 2040 extrusion. I also changed the positioning of the leftmost bearing in order to save space. I'll have to update the super derive remove model to a press fit. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODQ3ODAsInB1ciI6ImJsb2JfaWQifX0=--f40e4092399e081825f621cc1fb8de7aeb73c899/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6ODQ3ODEsInB1ciI6ImJsb2JfaWQifX0=--4deda2609635aa196ed57beb1d43000225b67c6a/image.png)
Also finally designed the Z tensioner. Being dumb, at first I forgot about how I centered the belt path on the outmost channel and so when I made tensioner I centered it on the center of the 2040, so I had to redo it. It's blocky, and unnecessarily large, but for now it'll do. In the future I'll optimize it a bit.

## Entry 14
- ID: 4888
- Author: AethelVeritas
- Created At: 2026-02-24T08:05:00Z

### Content

Long time no see. Took a break from the printer in order to finish up some past projects and because I kind of felt 'blocked'. Back at it now, anyway.

Today was mostly about reworking the Z axis, yet again. So I have 3 versions of the bottom Z drivetrain currently, as shown in the past journals, but V3 still had like a lot of unnecessary space in for the 20T small pulley that's drives the main belt, so I messed around with it for some time until I reduced that so it'd only fit 2 x 1mm shims and the pulley itself, plus a bit of tolerance. I'm really learning a lot from my mistakes every time I do one of these reworks, especially how not-parametric I make my parts sometimes. Anyways here's a before and after.
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjYyLCJwdXIiOiJibG9iX2lkIn19--c274bcd7d93daa2616c802edd072bc6cdb4b1772/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjY0LCJwdXIiOiJibG9iX2lkIn19--ef9e8821d9e6604d7c7e0ac9fce6ce7bb238351e/image.png)
I also finally made the heat insert holes for the top pulley "cage" clamp. I've decided I'll be using the M3 x 5.7 inserts throughout as much as possible of my build, so the holes were made per [this](https://www.prusa3d.com/product/threaded-inserts/) spec. 

Also, I finally figured out belts! Was kind of tedious as I couldn't wrap my ahead around the featurescript but after rummaging through the internet for a bit I figured it out!
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjY1LCJwdXIiOiJibG9iX2lkIn19--7bdd2203b584ef918ae5c5e0507953468f10af8b/image.png)
I'll obviously change the thickness later on but it's finally starting to look more and more like a legitimate printer. Adding belts also helped me notice that my calculations regarding the offset of the top and bottom Z pulleys relative to the vertical extrusion were off:
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjcxLCJwdXIiOiJibG9iX2lkIn19--ad6ed7e643523dcf35d4036cc50589edacfe2b15/image.png)
This I soon fixed, and now it's looking much better. I'm happy with the bottom Z drivetrain, but not with the tensioner, so I'll probably rework that tomorrow. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjczLCJwdXIiOiJibG9iX2lkIn19--c1e6d024db728c313f77dff650e530422d029233/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwMjc0LCJwdXIiOiJibG9iX2lkIn19--a8d54d7ce91b5530cdfe487ffd3a3f8d1948b4cb/image.png)

## Entry 15
- ID: 4889
- Author: AethelVeritas
- Created At: 2026-02-25T07:14:00Z

### Content

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwOTk3LCJwdXIiOiJibG9iX2lkIn19--ea2256038cfa4cb427a3f2e6ac557acc6d38c63e/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwOTk4LCJwdXIiOiJibG9iX2lkIn19--69d11fbfa768db43b6a04c8310705dec6fe678eb/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTEwOTk5LCJwdXIiOiJibG9iX2lkIn19--13bfbe3beb7e35fe55c82679d0b2f2e7964e3a2e/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTExMDAwLCJwdXIiOiJibG9iX2lkIn19--327ed5cb96270a7430c43cd834af7db766bd7855/image.png)
Made a new version of the tensioner, and also added some slots to make it look nice reduce material waste. I'm still a bit unsure about how thick I should make everything though...I mean 6mm is kind of thick for walls that don't have any direct tension applied to them and just act as guides.

## Entry 16
- ID: 4890
- Author: AethelVeritas
- Created At: 2026-02-26T07:45:00Z

### Content

Last journal post was for yesterday. I've slept on it and realized that my idea was dumb. Adding slots does not reduce waste in this case: it just makes the part have more perimeters in the slicer, which only increases both print time and material waste. Also, I should optimize it's length given the belt tensioning formula Deadlock gave me a while back (the one I alsu used for the Y axis. Now that I added a Z belt to the assembly two days ago I can make a pretty decent estimate of how long the belt will be, which in my case is 375 mm from top to bottom (so the actual belt length would be doubled in real life, but that doesn't matter for the calculation). 379(+ 4 mm wiggle room) * 0.02 gives 7.58, and I'll just round that up to 8 mm. So I should be able to tension 8 mm. Tensioner block is 25 mm tall, so 34 mm slot height. Wait no I can't have the tensioner just hanging out. Add 7 mm to that. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTExMDY4LCJwdXIiOiJibG9iX2lkIn19--2254049b285532cf5b3fe91bd3fc8e7f76fd520d/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTExMDY5LCJwdXIiOiJibG9iX2lkIn19--252de753fa00dab2100eeb48153e1eee1b5c8c24/image.png)
Ok this is what I'm going with for now. In the future I might remove the screw on the side as well as one of two top screws that hold the top X extrusion to the Z axis and then just use a longer similar screw to directly bolt tensioner through the top X and into the Z extrusion. Should be stronger, but I'll see. 

I've also decided to drop the 48v dream. TMC5160 Pros are prone to blowing/overheating as I recently learned in the Monolith discord, and I'd have to get 4x TMC5160 Plus, which would be like a fifth of the whole budget, $80. And I just realized that belts are actually more expensive than I thought, so yeah no can do 48v. Plus I talked to Renovic and also watched some older videos of Kevin's Kevender while it was still on 24v and they can hit like pretty decent accels and speeds even with 24v. Nothing like the 700 mm/s speed or 1000k accels that LH stinger can, but well then again my Q1 Pro usually prints at like 300 mm/s and it still seems really fast for me. I'll just focus on a good 24V base build, one that I can either upgrade to 48V in the future or reuse the parts for a 48V corexy. We'll see. I have to stop trying to overachieve...a bird in hand is worth two in the bush, and I really have to finish the damn printer already.

At this point I should make a more detailed rough BOM. 
https://docs.google.com/spreadsheets/d/19SDQH5rKj-VOt543ikEq3R2ylwxd--UoErljUox35hg/edit?usp=sharing

So, according to the Ice Cream Factory's Discord:
- Trianglelabs is the cheapest decent option for belts, and I can also get pulleys from there
- According to deadlock, for live idlers: "g6 is preferred here, h6 is still good but will require more work as clearance goes down to 0), and press fit on the housing (M7, N7)."
- Raindew bearings, make sure they are 2RS
https://docs.google.com/spreadsheets/d/19SDQH5rKj-VOt543ikEq3R2ylwxd--UoErljUox35hg/edit?gid=0#gid=0

Here's what I've got so far, and I still need a 340mm 2040 extrusion, lube for the rails, T-nuts, screws, 80T pulleys + timing belts (x 2). I've pretty much scrapped JLCMC because it turns out that shipping from there costs like $34, which is crazy. I also still need a Klicky probe, fans for the hotend + the motherboard, wires+crimps, and also brackets for the Y 4040, as I'll be shifting in front.

## Entry 17
- ID: 4891
- Author: AethelVeritas
- Created At: 2026-03-10T06:09:00Z

### Content

Ok I'm making the toolhead for #rework, can't fit in the budget. Brazuka gave me an updated quotation for the rails, which would be 87 (4x 300mm Z1 and 1 x 300 Z2) + 24 shipping, and then I just realized I actually can't use only my 350w psu cause the bed draws like 240W max and the Dragon hotend like 90-115W if I don't go for the volcano option. I really don't want to buy another 24v PSU for nothing, so I guess 48v it is. I'll just buy some TCM5160 Pros and it is what it is. I've got crimps and wires for everything I think, so I just need to get some wire sleeves as well as maybe a buck convertor.

Ahhh scratch that. Been racking my head with electronics and how'd I'd deal with them for the past 5 hours (not going to add that though because I didn't really journal it). Ok so I've decided that I'll let electronics be for the moment. I'll build an ebox for a either stasis or rework (I found some really cheap 3-4mm plexiglass and I want to make this really good looking transparent sides ebox), and I'll buy the 5160 drivers with that grant, and the PSU as well. I'll just focus on refining and making what I've designed so far better and just hope the reviewers see the amount of work I've put into this. Man I hate compromises! 

![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTE4ODA3LCJwdXIiOiJibG9iX2lkIn19--449f20853a0dea083159a627d5dc12ca92a014d4/image.png)
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTE4ODA4LCJwdXIiOiJibG9iX2lkIn19--6d0096a2a333d9cca3e4d1f77ae8396bc1c950e0/image.png)
Made some rail endstops, mock plexiglass panels, and also messed around with an octopus pro and pi 3b+ to see if I can fit them on the bottom. Octopus is too long to put like parallel to the base with the ethernet ports like in the front, so the only way I'd be able to make it fit would be to rotate it 90 degrees and place in the center, and then like direct everything else from the Pi, whose ports would be accessible. Honestly this sounds feasible enough so I might actually do that. 
But then again, did some more ebox research, and turns out that doing that without something like LH's breakbeat board isn't that hard either. In fact, in his build log, the latter uses some of those blank pcbs and some JSTs in order to improvise one https://github.com/lhndo/LH-Stinger/wiki/Build-Log#wiring. ![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTE4ODEyLCJwdXIiOiJibG9iX2lkIn19--6b6bc8cb0e31e7bdd163a113f1c46bc573b4b58a/image.png)
Zwirbel from the Stinger Discord recommended that I get some of these connectors if I plan to do so. And I'd need longer wires obviously, but I don't think that's gonna be a problem. ![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTE4ODExLCJwdXIiOiJibG9iX2lkIn19--99f60ea61271cdb93d9d31050db5df22237445d7/image.png)

## Entry 18
- ID: 4892
- Author: AethelVeritas
- Created At: 2026-03-11T07:51:00Z

### Content

Polished up the readme, assigned some new colors, changed the name, and mainly just finished the BOM. LH's [Stinger BOM](https://docs.google.com/spreadsheets/d/1s8ulLfThmbuy1G_40MvkXXL2oVx9PZhvpAY9hMxqYbg/edit?gid=1441455036#gid=1441455036) was very useful, as it contains links to reputable sources. 
![image](https://blueprint.hackclub.com/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTE5MzgzLCJwdXIiOiJibG9iX2lkIn19--9f7f66ec59513e5930d45002c76542c77bd64a4c/image.png)

## Entry 19
- ID: 726
- Author: AethelVeritas
- Created At: 2026-03-30T17:56:31Z

### Content

So last time I took tackled the ebox idea, I ditched in favor of mounting two psus of the same size on the back of the Z extrusions. Now I'm going for ebox, thanks to extra possible funding. What I'm getting at is that I don't need my 48V PSU to be the same size as the 350w 24v I'm getting off of the Ender. Never mind that, 350w it is. It's cheap ($20), and it should suffice for a CoreXY. Why are drivers so expensive :((. Gonna have to shell out $86 on 48v drivers. Turns out 5160T Plus have better cooling and thus are less prone to frying as compared to the slightly cheaper ($18 less) 5160T Pros. Mounting them is going to be interesting though.

Spent some time finding some accurate models for the pi, drivers, and octopus pro and then imported them into Onshape. Messed around with them in an assembly to get a rough idea of how I want to position them.


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY0OCwicHVyIjoiYmxvYl9pZCJ9fQ==--66fb300d1f9f2b1eb587ae2ecf44685ec021f8bd/image.png)

I think I'll be going with something like this, with the drivers on the bottom. Yes this will make the ebox wider, but it's still pretty compact (probably <15cm with the walls included) and this also allows me to do an interesting lid idea I had. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY0OSwicHVyIjoiYmxvYl9pZCJ9fQ==--b543634a0d7fb6e62ff74b1b1c7fed7648c54d44/image.png)
I want to make the slanted part have a small acrylic window, and add fans to the bottom vertical part for cooling. Also, I was thinking of maybe using some alu hollow rods for the frame, as they are pretty cheap, would look cool and would maybe give my structure some more stability. We'll see. Oh and I also spent some time making a mount for the octopus pro (obviously not finished yet). 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY1MCwicHVyIjoiYmxvYl9pZCJ9fQ==--b656d770bddb74148f709b4f0ddfc19300796c4c/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/f7e4fa06-7d14-4743-97c6-4d976468209f/video.mp4

## Entry 20
- ID: 1050
- Author: AethelVeritas
- Created At: 2026-04-03T17:53:52Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMCwicHVyIjoiYmxvYl9pZCJ9fQ==--b273e9aa0e933e30ac2c48a6d843918709b150ca/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMiwicHVyIjoiYmxvYl9pZCJ9fQ==--958c997563c1825ab6c81364da24ba8ce08f65c2/image.png)


So messed around some more in CAD, and this is what I think I'll go with. I can have the 6025 fans on the top on the outside to save space, stacking two TMC5160 Plus drivers allows me to save space lengthwise, and I'll add some cutouts in the bottom to improve air circulation. Still very cramped though unfortunately. I left 5 mm space between the PSUs, hopefully that'll be enough. 

Ok talked to LH and someone else in the LH stinger discord, and turns out my idea of stacking them isn't that great. Turns out that most of the heat from the drivers dissipates on the bottom, not the top where you usually see the heatsink. Seemingly, BTT has a history of not placing their heatsinks correctly. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyNCwicHVyIjoiYmxvYl9pZCJ9fQ==--c50d922bdd8409341b4a9c0dad51fd5dc21ec838/image.png)

Ocho from the Ice Cream Factory Discord suggested I rotate them vertically, and this seemed like the best option, but after some more back and forth I've come to the conclusion that it'd be too cramped, and that I'd have to make the Ebox too big to get proper cooling. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyNSwicHVyIjoiYmxvYl9pZCJ9fQ==--a5aaf9bfb26b92d8ceb85bf27445ea35663ee90e/image.png)

Seems I'd want about 20mm between the PSUs for instance, and 20-35mm between the drivers and mainboard for wiring. After much messing around with positioning and research, I think I'll have to give up the Ebox idea. I just can't get good cooling without making a humongous box, which besides not being printable for anyone with an ender who might want to use it in the future, would also consume a tremendous amount of filament. It's sad really: I had this great idea of a good looking box with transparent plexiglass cutouts and all, but it is what it is. Ocho reminded me that I don't actually need a new PSU like I initially calculated the last time I considered giving up 48v for now, because I can just get a 15-20 dollar AC bed heater and wire it directly to the power socket basically, meaning that I don't have the bed draining 230W from my 350W PSU. 

Yes I'll be sacrificing a lot of speed, but honestly I don't really want a very fast (500mm/s) bedslinger...not that efficient and not that interesting honestly. I'll still be able to hit good speeds (like 300/400mm/s), which is more than enough, due to my AWD setup. And honestly I've kind of got burnout from this project: it was meant to be a quick printer so I can get parts to build a good one, a corexy. I've sunk too much time in a bedslinger. Time to wrap it up and actually build the thing. 

### Recording Links

- https://lookout.hackclub.com/api/media/fb5e4a1a-39d1-4671-bb90-40f25136ad30/video.mp4

## Entry 21
- ID: 1557
- Author: AethelVeritas
- Created At: 2026-04-09T08:30:32Z

### Content

More research. AC might not be feasible after all because it's dangerous. I need to ground the frame, have a GFCI outlet, etc. And all of that stuff adds up. The whole point of going with the AC bed heater was to minimize cost. But if it's gonna cost like $100 dollars for something like that then I'd prefer to just get 5160s and a 48v for that sum, as I can reuse those later  and I'll get more speed. 
However, I think it'd be wise to make an updated version of my whole BOM first. Better get it over with it now and make sure I don't design something for nothing. 

So basically all I've done today is getting started on the BOM and thinking more about what items I could reduce/get a different part to optimize cost.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzQxMywicHVyIjoiYmxvYl9pZCJ9fQ==--c64779a771d9c11dd545f0fb6201d507afb92d27/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/e082c6bd-16ad-4b2f-b8c8-f379e4956d57/video.mp4

## Entry 22
- ID: 1679
- Author: AethelVeritas
- Created At: 2026-04-10T19:14:37Z

### Content

I think I'll have to return (once again) to the Ebox idea. Can't think of any other way, and as I previously mentioned AC seems too dangerous, especially with a moving bed. Also, I'm almost certain that I won't be able to get a filament sponsorship from Polymaker, as May and several who are building printers for #infill were rejected (and those were good unique projects). This is unfortunate, as I was kind of "relying" on that for filament. So now I'll have to somehow squeeze one-two rolls of PET-CF/ABS/ASA in the budget. I'm getting uncomfortably close the $600 mark, and I still don't have a hotend.

Found a 500x500 4mm plexiglass/hobbyglas sheet for 9 USD at a local hardware store. Transparent as well as black/color options, and rated up to 75C. A quick search shows that motherboards+drivers shouldn't usually exceeed 45-55C (I am not certain how accurate this estimate is though). I think I'll use this for panels if I can find a good way to cut it. I've got a router, so I guess I could use that for cutting slots for ventilation, but it seems this more brittle then acrylic, so I am not certain how well that would work. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzQxNiwicHVyIjoiYmxvYl9pZCJ9fQ==--f5ad4c030ee887b5b05cca94cfcd0de2931bf1f9/image.png)
All my panels would fit easily though. 

For reinforcing the frame, since I'll be using plexiglass panels instead of 3D printing everything I was thinking of using alu pipes, as they are really cheap, I can source them locally, and I've used them before for a telescope mount. They're like $2-3 for 1000mm x 8mm x 1mm (thickness). Thing is I'll have to consume more material to make panel mounts. Not that that is a great problem by any means, but it makes mounting components and stuff harder. Now the other alternative I've been considering is just getting some alu extrusions. I found a listing on Aliexpress for 4 x 330mm 2020s for about $25. The one 2020 I had in my BOM previously that I was planning on using for the gantry is $9 for reference. Thing is, I'd have to get that as well as the gantry one, and I'm not sure if the price is worth it. Like $25 for an ebox frame? Seems a bit overkill. I guess I'll figure the layout first and then worry about the frame.

So...cooling. Found a message in the Monolith Discord by Vex saying that external drivers do not really need cooling. Also while browsing I noticed that a lot of builds (including Brazuka's) don't actively cool the mainboard. Interesting. Maybe I'll just add a large PC fan for airflow since my Ebox is smaller than a Trident's electronic bay for example. Why do I have to overthink literally everything. This perfectionism is going to be the ruin of me.

Hopped on a huddle with Renovic and some other people later on in the day, and decided that the 3mm plexi panels should be enough. Also talked to LH who said he used a 4020 noctua blowing on the PSU fan in order to make sure it doesn't overheat in the summer (because the octopus pro covers part of it. 












### Recording Links

- https://lookout.hackclub.com/api/media/80a5dd69-92e4-4a9b-8f17-06549a28e744/video.mp4

## Entry 23
- ID: 1695
- Author: AethelVeritas
- Created At: 2026-04-10T21:27:11Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzY1OCwicHVyIjoiYmxvYl9pZCJ9fQ==--2c2c82cb9f043bffb50b1a473900b91ee4c6fa9c/image.png)
Made a rough mount for the drivers. Also did a bit more research on how flimsy those 3mm panels are. From what I've found, they appear to be PVC, and not very flexible but definitely not rigid. I'm still debating whether I should go with 4mm transparent plexiglass or use those 3mm PVC ones. 4mm seems more rigid and solid, but cutting and post processing might make it look worse. I think if I can cut it at my local library I'll go with the plexiglass. To be honest a mostly transparent ebox with maybe some cool leds inside would look pretty darn sick. Also researched fans a bit again. I might add a 120mm fan one end to help circulate the air, but I don't think I'll add any other fans besides that. Asked in the monolith discord and most people don't use active cooling for their 5160 plus drivers, only for stepsticks. So I guess the like $15 difference between the stepstick and these externals is now worth it, because besides getting better quality I'm also "saving" on the fans. 

### Recording Links

- https://lookout.hackclub.com/api/media/3d24d85b-8ba4-4b45-b696-592677f41106/video.mp4

## Entry 24
- ID: 2221
- Author: AethelVeritas
- Created At: 2026-04-14T18:49:45Z

### Content

One of the reviews on that 4mm plexiglass I was looking at said it was really easy to bend with a little bit of heat....what if instead of cutting like the angled front cover I bend it. Scope creep is real haha. 

After some more CAD, here's the rough idea. 


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDY4MiwicHVyIjoiYmxvYl9pZCJ9fQ==--1b4052b3013708bdcb8c17a9c0df74d421f994e8/image.png)

Now my initially idea was that I'd have braces such as the red part all along the frame, to compensate for the fact that I can't print the frame in one piece.


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDY4MywicHVyIjoiYmxvYl9pZCJ9fQ==--324d45ab187a6fa040fa99e66802f829e72de003/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDY4NCwicHVyIjoiYmxvYl9pZCJ9fQ==--f098107224998c4d07e211ef713815562068fb46/image.png)

I was planning to drive M3/M2 screws through the outside frame and the panel and into heat inserts/nuts secured in these braces. But now I realized that firstly it would consume both material and space for not that much of an addition to rigidity. I kind of keep forgetting that this is actually a really small box, and hence the rigidity of the panels will be pretty dang high, especially if I go with 4mm panels. Now, my outer frame will actually be thick enough that I can put the heat inserts in the frame from the _inside_, and screw the screws from the inside, thus completely hiding them. 

I'm also debating how I'll split the frame. I could split it directly in half, like this:
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDY4NSwicHVyIjoiYmxvYl9pZCJ9fQ==--3fb5effe4855c5195bccf7f3743e716a3808ae11/image.png)

But the issue is that I'll lose some rigidity on the longest side. I guess the panels could compensate for that, but I'm not sure. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDY5NywicHVyIjoiYmxvYl9pZCJ9fQ==--a1b69ab4a4f0dd2be5bfb75b48f83cb435f9b6ff/image.png)


Well this is how it's looking so far. Not bad in my opinion. I've started adding the holes in the panels and the frame for the heat inserts and screws, but that's gonna take some time. Very tedious unfortunately. I really hope I won't have to rework this. 


### Recording Links

- https://lookout.hackclub.com/api/media/80767ab6-3c3b-4414-a494-b438d9c049d6/video.mp4
- https://lookout.hackclub.com/api/media/239cd98c-8f8d-4a27-a1d4-2de468122cfb/video.mp4

## Entry 25
- ID: 4893
- Author: AethelVeritas
- Created At: 2026-05-02T05:16:20Z

### Content

Project transferred from Blueprint! Duration Transferred: 132.0h

## Entry 26
- ID: 8022
- Author: AethelVeritas
- Created At: 2026-05-19T19:15:27Z

### Content

Worked on the ebox again...man I hate this thing. Why do I have to over-complicate everything. Anyways I made screws holes to attach the panels to the frame, and it was one of the most tedious things I've done in quite some time. I think I'll stick with black 3mm panels for the sides back, and bottom, and then just use 4mm clear plexiglass for the front. Honestly should have just made everything except the front cover printable...would have saved a lot of screws and post processing. Well anyways hopefully this'll reduce material cost by a bit, even though it's only like $10-20. I'll derive the panels (which now have screw holes) in another part studio, cutout the centers, and then use those as cut and drill guides for the plexiglass. Cut some yesterday for another project using the same technique and it worked quite well. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTc1MzEsInB1ciI6ImJsb2JfaWQifX0=--2c78d3ca876ed499125674f0dcf89839a61fc14f/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTc1MzIsInB1ciI6ImJsb2JfaWQifX0=--54d0d917ae7dfc89fef5da6deead16f02c2f798d/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/66992d0c-a727-4ef4-b635-bd78e4f1ab3b/video.mp4
- https://lookout.hackclub.com/api/media/5ce17cff-c9dc-42fe-8e92-643b7abe586d/video.mp4

## Entry 27
- ID: 8513
- Author: AethelVeritas
- Created At: 2026-05-22T18:16:46Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MjAsInB1ciI6ImJsb2JfaWQifX0=--41f0a82372c7ab718371c43614ab01f3e6103fea/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MjEsInB1ciI6ImJsb2JfaWQifX0=--132aacbb6af2af8d5be76cf9798ef03f4ea1e80a/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MjMsInB1ciI6ImJsb2JfaWQifX0=--97b9899c5237f0a488ce6dfc0f0cbd02c19bb18e/image.png)
So first of all, I've added magnet holes for the door. While for the door frame I'll just be gluing them in, as you can see in the last pic, for the frame I've also managed to make them slot in. Hopefully the 0.8 mm of plastic will be enough to keep them from popping out but at the same time not weaken their strength. 

Then I moved on to the hinges:
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MjcsInB1ciI6ImJsb2JfaWQifX0=--11de6fef81031ccfe657d159c70d3f498f3cea9f/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MjksInB1ciI6ImJsb2JfaWQifX0=--947e407f9c5b93eedc1cd86e881efaa203ed9598/image.png)

As you can see, I've used the LH stinger's Ebox hinges as my main reference, and I've only changed the dimensions slightly for my use case. A piece of filament or wire will go in the small "pin hole". 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzAsInB1ciI6ImJsb2JfaWQifX0=--7e157364404b2cd84423a06570964ca36a394cc4/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzEsInB1ciI6ImJsb2JfaWQifX0=--6491b4b4d81482fdc54c62c85395828d7dc872bb/image.png)
Then I finally started making the main assembly. I've decided I'll only use clear plexiglass for the door, as it has a tendency to gather a lot of oil and marks. I'll use 3mm polycarbonate for the rest of the walls. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzIsInB1ciI6ImJsb2JfaWQifX0=--caded82d993d8f146457fe6f25fcee7bb52bb911/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzMsInB1ciI6ImJsb2JfaWQifX0=--ee98761871d82fb1a71e3498e7c9bb0ae730fb28/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzQsInB1ciI6ImJsb2JfaWQifX0=--107470de50b089a409e4182684195f51cd71d671/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg2MzUsInB1ciI6ImJsb2JfaWQifX0=--b85d316c86903a15ad2b610eca75874698faf879/image.png)
Also, I modifed the psu mount I had created earlier to also hold the raspi 3, and added some cable channels on top near the mainboard as well. These are from the LH Stinger, with just the logo removed. I'll have to make a logo and add it somewhere on the ebox once I finish renders and the BOM and everything. I still have to make its feet (I want to use the same kind of rubber feet as I'll use for the Y-axis, to save money) and holes/an inlet or outlet of sorts to let the cables pass in, as well as a mount for the power inlet and switch. I'll be drilling holes in the walls for ventilation, which is another reason for avoiding the plexiglass for all walls, as it being transparent kind of makes the hole burrs more nagging to the eye.. 

### Recording Links

- https://lookout.hackclub.com/api/media/513a9f47-bd40-4e23-955a-99457558040d/video.mp4
- https://lookout.hackclub.com/api/media/cb79d077-c574-4f93-89b5-27c0ce9ff9cb/video.mp4

## Entry 28
- ID: 8876
- Author: AethelVeritas
- Created At: 2026-05-24T14:39:35Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTk2MTgsInB1ciI6ImJsb2JfaWQifX0=--b65af0ae8378cb293e0ddb2a3c7d43e1500ce132/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTk2MTksInB1ciI6ImJsb2JfaWQifX0=--85821d8ef190648652a555f5948b9463e72402c0/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTk2MjAsInB1ciI6ImJsb2JfaWQifX0=--48356a202493251d046fef43f1e047c3b72d572d/image.png)
Made the power inlet/cable outlet mount today. A bit overkill, and bit complicated, but I also made an inner piece because since I'll be cutting the panels by hand with a drill and a small saw I can't really cut complex shapes precisely, so they'll be rough, and since that area will be clearly visible through the door I thought I should make it look nice. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTk2MjQsInB1ciI6ImJsb2JfaWQifX0=--c98ec5db90bda9a682d5d87d09b0237f29384889/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTk2MjUsInB1ciI6ImJsb2JfaWQifX0=--2562efaa141eb1d4ae5b6cfd292298e6cfd40c54/image.png)
Also spent some time adding finishing touches such as all the screws and the "clamps" for the driver mounts. I still have to deal with ventilation, which is going to be an immense pain. The amount of time I'll waste drilling holes in those panels will be insane. Also, I'm kind of worried, as I've now realized that the distance between the edges of the panels and the holes is like 1.7 mm or something like that...not good. I'll fix that later I guess. 

### Recording Links

- https://lookout.hackclub.com/api/media/5a5297f3-a69c-422c-a182-8976489d47f0/video.mp4

## Entry 29
- ID: 9165
- Author: AethelVeritas
- Created At: 2026-05-25T18:03:30Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDIsInB1ciI6ImJsb2JfaWQifX0=--6de306d72d3fd85f770a0a21c21b505f2520a44f/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDMsInB1ciI6ImJsb2JfaWQifX0=--30663ca6f741de1d7a6f965f0c3d9aa003dfff7e/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDQsInB1ciI6ImJsb2JfaWQifX0=--5df2b9ff3cdbd84ff8a81e662a60e0970fee9d78/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDUsInB1ciI6ImJsb2JfaWQifX0=--5beeb933965b233e63c0f2672b0bb9fdee87f46a/image.png)
Ventilation! Finally. This didn't turn out as detailed as I'd initially hoped, because I'm running out of time. Hopefully it'll be enough. I'm thinking that worse case scenario I can just open the door when printing. Using a 6040 fan that will hopefully draw the air from the above the drivers (which I think will be letting off the most heat), allowing new cool air to flow in through beneath the holes beneath the drivers and on the left side of the ebox. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDcsInB1ciI6ImJsb2JfaWQifX0=--7410bca7a7ce8ed3019202c5d2fa01526733172c/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDgsInB1ciI6ImJsb2JfaWQifX0=--f5fe375af328a3c07c568c26fa0bdb6cfd64c160/image.png)
I also made a new modified version of the gantry in order to give the custom toolhead I designed (Aeolus) more X travel. I think the whole gantry looks even cooler now honestly
. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMDksInB1ciI6ImJsb2JfaWQifX0=--011cbc557fcd596d592d63e1b710c874908988eb/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAzMTAsInB1ciI6ImJsb2JfaWQifX0=--eae0d1b001048a2f859aa02a308578fcef09625b/image.png)
I also made a dock for the quickdraw probe, based on the LH Stinger's dock. As you can probably tell, I'll be losing some X print space because the bed is too big and the gantry too small for the current toolhead to have space to get lower than the bed in the Z to attach to the probe. 

On a side note, I've been thinking of renaming the whole project "Revenant". A revenant is someone who returns after a long time, usually from the dead, so I guess this would still kind of fit the theme I'm trying to go with here: a "reborn" Ender. But we'll see. I kind of like the current color scheme. 


### Recording Links

- https://lookout.hackclub.com/api/media/580312b1-8756-4319-8427-3feff466f974/video.mp4
- https://lookout.hackclub.com/api/media/87b42c9e-3e14-4fbd-91a2-0d2a52f2ddc7/video.mp4

## Entry 30
- ID: 9447
- Author: AethelVeritas
- Created At: 2026-05-26T19:02:44Z

### Content

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5ODIsInB1ciI6ImJsb2JfaWQifX0=--13af0f7713b224544199d05f2696a96a8c0bf7a3/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5ODMsInB1ciI6ImJsb2JfaWQifX0=--5f9dba006622b365f796a276466fade94b629733/image.png)
Started off with these logos I found on the web as inspo. I especially liked the last one, but I want to keep the geometry simple. Messed around with some logo generators for like about an hour, and this is the one I eventually settled on:
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5ODQsInB1ciI6ImJsb2JfaWQifX0=--751ac0d15569b83cf8a1013231c10637ba01ccf4/image.png)
Made a bitmap in inkscape, exported it as svg, converted it to dxf, and then I added to the CAD.  Made these 4040 endcaps with the logo on them....I'll use a lot of z-hop to print two different colors on the base layer. Also made a larger phoenix that I'll glue to the back of the ebox. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5ODUsInB1ciI6ImJsb2JfaWQifX0=--ad43a46be89b45f7f4f2a6e4ee1d37a2a5c40177/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5ODYsInB1ciI6ImJsb2JfaWQifX0=--70f10f0caf2b348aa9cd9b271cfa49661ba83d25/image.png)
The rest of the time was spent just adding different missing screws in the assembly and working on the BOM. 

Stuff I have left to do:
- Finish BOM. 
- Polish up README writing.
- Generate/make some pics/drawings for the main pics. 



### Recording Links

- https://lookout.hackclub.com/api/media/64f2eeed-c9ef-452d-90c6-6257922ca035/video.mp4
- https://lookout.hackclub.com/api/media/e0f8519f-be4e-44a1-8307-6fe0b647673f/video.mp4

## Entry 31
- ID: 10232
- Author: AethelVeritas
- Created At: 2026-05-29T19:42:46Z

### Content

Worked on the BOM. I hate this part honestly...very tedious and so many little things that can go wrong. Not much I can journal about that, but some things I learned are:

1. Add every part to a final assembly, and use as much standard content as possible. I use Onshape, and it can generate a BOM of an assembly, which is very helpful. Using as much standard content as possible ensures Onshape also displays names+dimensions of screws, nuts, washers, etc. 
2. After making a final assembly, open the generated BOM and try to see if you can't reduce different instances by using the same kind of screw for example. Let's say I need 20 M3 x 6mm screws, and then use 4 M3 x 8mm screws for some other part. If I can modify the latter to use 6mm screws, I might have just saved $4, which is about the minimum price for a bunch of screws off of Ali. 
3. If you can't reduce different instances as mentioned above, check local stores' websites. If a find a screw I only need 4 of for several cents at my local hardware store then I don't need to order it. Double check though, because it's really annoying when all your parts arrive only for you to realize you can't source X part locally as you thought. Waiting another several weeks for stuff from Aliexpress to arrive is not fun. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMxOTQsInB1ciI6ImJsb2JfaWQifX0=--0ce9dec6d71b66c847ce04539f9542fc48d09a7a/image.png)
Here's a pic of how I've structured my BOM. One thing which rather confused me was quantity. Like if need 4 fasteners, but they only come in a 10 pack for $5, then do I add another column to the BOM saying the quantity and then list the price for a pack of 10? Wouldn't that be confusing as I'd think I have to buy 4 packs of 10? So for now I've just "ignored" quantity. I've specified the number of pieces  in the title, and then listed the final price for all pieces. There's probably a better way to do this, but for a hobbyist level this should be fine. I've looked at other BOMs from other hackclubbers who are more skilled in the art of 3D printing and they seem to be doing the same. 
Oh and also I must say that [LH Stinger BOM](https://docs.google.com/spreadsheets/d/19SDQH5rKj-VOt543ikEq3R2ylwxd--UoErljUox35hg/edit?gid=0#gid=0)
was huge help for referencing reliable sellers of screws and the like. 

Another issue I faced was sourcing filament. I really wanted to get good ASA, since I can't use PET-CF (can't anneal it). The problem is most brands were either expensive or didn't have a decent fiery orange. I looked at Extrudr, Polymaker, 3DJake, Sunlu, and many others. In the end, after scouring some Discord servers I settled on Torofil from toro3d for the black and then just sourcing some orange locally, either Polymaker Polylite or Devil Design ASA. I really wanted to get torofil because it's pretty highly recommended on the Monolith Discord, and it's maker/owner of toro3d is pretty active there. And of course because one spool of black ASA costs only 19 euros on his website right now, which is like Elegoo levels of cheap.

Moving on to the biggest thorn in my side: rendering. At first, I tried Blender. Wasted like an hour on that before giving up: I knew there was no way my Intel iGPU could handle a 1.3 GB .obj file, but thought I'd try anyway, as I didn't really see any other way. My laptop felt like it was about to explode when Blender crashed. I also considered making a drawing style main readme pic like I did for the  [Aeolus](https://github.com/AethelVeritas/Aeolus), but unfortunately my laptop again couldn't handle it. Onshape was slow and laggy when trying to load views in the drawing, the lines were too choppy/large to properly show off all the detail, and I also didn't want to spend half a day learning how to use the drawing workspace properly just to get some mild looking pics. Fortunately, Raygen reminded me on the HC Slack that Onshape has a free 6 month trial for professionals, which also grants access to the built-in renderer. So I made a new account, claimed the trial, and started to mess around with said renderer, which is honestly awesome. Pretty intuitive, nice UI, and not too laggy. The problem is I don't really know what I'm doing, and I'm also a perfectionist. I don't know why I want pro level renders...many quality 3DP projects have almost stock renders. I think I might be focusing too much on this point..this isn't something that I intend to commercialize, like the LH stinger for example. Anyways, an annoying thing I learnt is that if you use composite parts in an assembly, you then can't assign appearances to individual parts, only to faces. This is really frustrating because now my motors are pretty much stuck with the default/auto appearances, which look like shit. But oh well, lesson learned. Oh and also something I wanted to do is use the github dark theme background color as my background color, so that the render would blend in with the background of the readme. Seems to have worked out pretty well....anyway here are some random renders.



![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMTEsInB1ciI6ImJsb2JfaWQifX0=--a4dd178581465343eed4777b11b00a9d150974e5/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMTIsInB1ciI6ImJsb2JfaWQifX0=--ad34adb5d91f506f9d50355115569d1746bf36c9/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMTMsInB1ciI6ImJsb2JfaWQifX0=--8677a619c6f67aa333efbfc992947e0e12f731a2/image.png)
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMyMTQsInB1ciI6ImJsb2JfaWQifX0=--e39ffea7320afc30b504c71bcfa542d015fb3456/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/fb0c7484-fd64-464c-a21f-4fd26ecbb88e/video.mp4
- https://lookout.hackclub.com/api/media/f36aa8f8-c1c5-4730-a882-70274208454c/video.mp4
- https://lookout.hackclub.com/api/media/97e499c7-b17a-406d-8926-9329ce2ddfb3/video.mp4

## Entry 32
- ID: 10867
- Author: AethelVeritas
- Created At: 2026-06-01T10:30:37Z

### Content

Not much to say. This was mostly polishing up stuff, making a rough firmware file, ebox wiring diagram, and the zine. I forgot how much I hated making these kind of posters honestly....I am just not good at art of any kind. Actually, I'm just as good as I need to be to tell that what I'm doing does not in fact look good haha. So yeah, made the zine, made some more renders and finished up the readme. 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ3OTAsInB1ciI6ImJsb2JfaWQifX0=--ba35a60da5c2900e39c3ff368a0514a380671c85/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/72323eed-ef79-446a-8280-71ada5dd8172/video.mp4
- https://lookout.hackclub.com/api/media/10f4bcd8-23c3-45b2-9d93-af3e1e9e1264/video.mp4
- https://lookout.hackclub.com/api/media/c8aabee5-d1ce-4ecf-ad80-59d94d0ee90d/video.mp4
- https://lookout.hackclub.com/api/media/c55da64b-201d-4f46-9132-15f5e37acf2d/video.mp4
