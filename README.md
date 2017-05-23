<h1>Welcome to WikiBarbell</h1>
Welcome to the wiki where you'll find all the information that you'll need to use your devices, learn tips and tricks, and contribute to the community. 

== OpenBarbell Manuals ==

<p>Dive right in to the [[V2.0|OpenBarbell V2.0 Manual]] </p>

<span class="plainlinks">[{{fullurl:V2.0}} <p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/10/IMG_7664.jpg" width="600" height="360"></p>]</span>

<p>[[V1.0|OpenBarbell V1.0 Manual]] </p>

<span class="plainlinks">[{{fullurl:V1.0}} <p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/02/20160201_183650.jpg" width="600" height="338"></p>]</span>

<p>[[V0.25|OpenBarbell V0.25 Manual]] </p>

<span class="plainlinks">[{{fullurl:V0.25}} <p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2015/08/email_image.jpg" width="600" height="291"></p>]</span>

== Getting started ==

Consult the [//meta.wikimedia.org/wiki/Help:Contents User's Guide] for information on using the wiki software.

<h1> OpenBarbell V2 </h1>
<p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/10/IMG_7664.jpg" width="960" height="540"></p>

<h1> Under Construction </h1>
<h2> What does OpenBarbell V2 Do? </h2>
[[#toc|Back to Table of Contents]]

OpenBarbell V2 is a low barrier-to-entry Velocity Based Training device. It enables lifters to track the velocity of barbell (or otherwise) exercises to they can do velocity based autoregulation training. This data has been used for decades by high level athletes and has yet to trickle down to the average lifter because of a perceived lack in demand. We disagree with that perspective and are dedicated to supplying athletes in strength sports with the same level of technology that athletes in other sports enjoy.

Each Rev 2 device measures average velocity that has been validated against the best technology in velocity tracking. It also has the ability to display peak velocity, which has been greatly improved in comparison to OpenBarbell V1 and other tether-based velocity measurement systems. It also measures the duration of each lift in seconds, the total range of motion of each lift, and the spot at which you achieve your peak velocity (in %), time between sets, and with the new OpenBarbell App, the potential for much more. With successive firmware and software updates, OpenBarbell will earn more and more features that we will include in this live document.

<h2> Frequently Asked Questions </h2>
[[#toc|Back to Table of Contents]]

<h3>Basic Info</h3>
<blockquote>
<strong>How much does OpenBarbell V2 cost?</strong>

We are trying our best to keep the price low enough to allow the amateur lifter to enjoy the benefits of Velocity Based Training. At the same time, we're balancing unit costs and the amount of time spent on our part designing and assembling small batches of these units. That being said, we are offering OpenBarbell V2 for sale at $249, plus $9.99 for our new Roller Hook (our velcro strap is included). Overall, an order of magnitude less expensive than comparable devices.

<strong>When will OpenBarbell V2 be released?</strong>

OpenBarbell V2 was released for pre-order on our webstore in August 2016. They sold out in under two weeks, raising over $70,000 for the manufacture of the devices and future VBT tool development. A small number of OBV2's will be made available on RogueFitness.com mid-October, with more to follow.

<strong>Does my device have a warranty?</strong>

The Squats and Science OpenBarbell V2 is unlike most consumer devices available for purchase. It was made by a couple engineers who were fed up with the lack of accessibility for advanced training tools and decided to solve the problem themselves. That meant making something that works quickly and at low cost. Although we would love to continue to support our devices as long as you own them, we will only be making these in small batches and therefore unable to replace parts, dedicate a service team or absorb the costs of return shipping. We will however support each and every device when it arrives on your doorstep, and if there are any issues you can ship it back to us to be repaired or we will give you a full refund.

OpenBarbell V2, like the name suggests, is also open source and Arduino compatible. Normal warranties prevent users from hacking their devices, but we encourage it. We do not wish to preclude you from modifying your device and we hope you have the ingenuity to create functionality that the community can take advantage of. We cannot guarantee your hacks will not break OpenBarbell, but if we find upon repair that issues arose via hackery we will have limited ability to repair your device free of charge.

<strong>What does OpenBarbell V2 do?</strong>

Very simply, OpenBarbell V2 measures the position and velocity of an object in one dimension. This capability allows a lifter to utilize VBT (Velocity Based Training) to autoregulate their exercise routine. Autoregulation is a fancy way of saying you use the most current information about how strong you are to determine what you do at the gym that day. This type of training has been shown to be incredibly effective at both executing long term training goals and planning maximum effort attempts in the same day.

<strong>How do you use OpenBarbell V2?</strong>

Coming soon!
</blockquote>
<h3>Technical Questions</h3>
<blockquote>
<strong>I'm getting funky battery readings, is that alright?</strong>

OpenBarbell V2 is made primarily by two engineers. In order to get these devices out in a reasonable amount of time, we decided against doing in-house battery conditioning. What that means is your OpenBarbell needs to learn its battery over the course of the first few charge and discharge cycles. We highly recommend you charge it until full as soon as you get it, and let it discharge until 2-3% without letting it die. You'll notice it has much more consistent battery readings, and will appear to last much longer.

<strong>What are OpenBarbell V2s dimensions?</strong>

80mm (width) x 100mm (height) - Approximately.

<strong>What's under the hood?</strong>

OpenBarbell V2 is powered by a Nordic nRF51 series ultra low power SOC. This system is a combination of a 2.4 GHZ Bluetooth transceiver and a low power 32 bit ARM Cortex -M0 core. This package is mounted onto a board developed by RF Digital called the RFduino, which is Arduino compatible and FCC Module Certified for use in consumer electronics.

<strong>What are the maximum and minimum velocities?</strong>

The following are theoretical numbers from our experimentation. We will likely do further investigation and will post them here.

''Maximum'':

The maximum velocity can be answered in a few different ways. If you wanted to know what the fastest barbell lift is that it can track, the answer is ALL OF THEM! In our testing we haven't been able to approach a skipped reading or measurement with any barbell lift, no matter how strong our subject is an how light the weight is. We can be relatively sure of this because, our velocity code runs in what's called an 'interrupt', which checks the encoder at a rate close to the clock speed (16 MHz, or 16 million times per second). The bottle neck is how fast it can crunch the numbers after the interrupt occurs, and by comparing how many times we get in the interrupt vs. how many times we crunch the numbers, we can tell when reps are missed.

If you want to know how fast you can pull the string out of the device, first I would say please don't do anything you would regret, then I would say we have pulled the string as fast as 5.71 m/s average velocity and 12.62 m/s peak velocity. The fastest lifts I've ever seen are hovering around 2 m/s average velocity. The bottleneck would likely be the mounting point of the spring and the axle, so if you were to attach it to a bottle rocket or an SR-71 Blackbird that's where we're guessing it would fail first. We've tried and failed to do it with any of our humane means.

''Minimum'':

The minimum is a little more straightforward, although a bit mathematically involved. Let's pretend we're coaching the worlds smallest lifter. His bench ROM is incredibly short and he has been training for decades, carefully refining his technique becoming the worlds slowest lifter.

Our hardware calculates velocity approximately every 2.8 mm. Velocity being distance over time, the smallest possible distance you can travel would lead to the slowest possible velocity. Coincidentally, our tiniest lifter in the world has a bench ROM of 2.8 mm.

Our ARM Cortex M-0 processor has a time-based interrupt that is constantly counting upwards in microseconds (millionths of a second). Because of the limitations of a 32 bit unsigned long variable, the number rolls over every 70 minutes and starts counting from 0 again. Since the odds of you starting and ending a rep at that exact time are incredibly slim, we did not write code to fix that fringe case. That means the maximum time we can do one rep would be about 70 minutes. That happens to be the longest attempt our World's tiniest lifter has ever accomplished.

A little bit of math later and we've calculated that the tiniest lifter in the World has maxed out our device at an astonishing 0.0000006667 m/s. That is roughly the equivalent of traveling the distance of one wavelength of red light every second.

<strong>How accurate is OpenBarbell V2?</strong>

There are two metrics that are important when talking about the quality of data you get from OpenBarbell. Those are accuracy, and precision. Accuracy is how close our readings are to real-world velocities, which we discern from lab grade velocity measurement devices. Although accuracy is very important, we often get the argument that precision is even more valuable. A precise device would produce readings that are always consistent with each other, allowing you to compare lifts to those done in the past and future, which is vital for autoregulation.

OpenBarbell V2 is both very precise and incredibly accurate. We have preliminary results from measurements made against the Tendo device, OptoTrak optical position sensing device, precision micrometers and super-high accuracy industrial encoders. Our readings show that we have the capability to reproduce real-world velocities very consistently, with R-values above 0.999 and accuracy hovering around 98-99%. Don't take our word for it. Dr. Mike Zourdos at Florida Atlantic University is currently conducting a validation study on the device with the results to be published later this year, or early next year. We will also publish official results of our own test soon as well.

<strong>How long does OpenBarbell V2 last on a charge?</strong>

With our real-world testing, we are currently estimating that, using your device's energy economically, it can be trained with every day and last about a month. We upgraded the battery from 1000 mAh to 1600 mAh to accomodate bluetooth interation with our mobile app, and expect an even better usable duration. The lifetime of the battery should be great as well, since that is dictated by number of charge cycles and there can be as little as 10 a year!

Please keep in mind, personal use can vary. If you tend to leave your device on between workouts you can kill the battery in a matter of days. If you turn it off between sets it will last much, much longer.

<strong>What's the maximum displacement?</strong>

The maximum string displacement is under 9 ft. In real world scenarios, that means a lifter about 6'6 can do an overhead press with a close grip and only have a few inches to spare. If you're very tall, tread with overhead work carefully in the beginning. If you're doing presses you can mount the device higher off the ground. If you're doing Olympic Lifting you can mount it on a few extra plates until it's just below the bar, and be careful not to run off the platform. If you have a habit of doing that, we will be developing a magnetic attachment that will release if pulled too far. Check our store for that in the future!

<strong>How much resistance does this add to the bar?</strong>

OpenBarbell V2 adds up to 1/3 lb to the bar. That is when pulling hard at close to the extent of the string length. This is consistent with other draw-string based devices.

<strong>How does my device work?</strong>

Coming soon!

<strong>My device is acting weird while plugged in. Is it broken?</strong>

It's perfectly fine! OpenBarbell is chock full of peripherals so we needed to use pins for multiple purposes. Two pins that are grounded while the MicroUSB are plugged in are vital for the devices functionality.

We understand this may be inconvenient, but we've designed it to charge fast and last long, so hopefully it won't be so bad!
</blockquote>
<h3>Servicing and Repair</h3>
<blockquote>
<strong>EDIT What happens if a part breaks or malfunctions?</strong>

If your item breaks or is in need of a specific part, you have a couple of choices. OpenBarbell is totally open from head to toe so from day one you have the ability to modify, improve, or fix your own device. Search the forum or write a post and we will instruct you on the best course of action. If it turns out we have the ability to supply a spare part or can fix it ourselves, you can send the unit to us and we will fix it at no cost (but we cannot cover the shipping). Since the device is also totally open source, we hope others who may be more technically inclined can pitch in to help others in case of VBT emergencies.

<strong>EDIT What happens if my string breaks?</strong>

OpenBarbell is made with a very durable half millimeter Kevlar string. It has been tested for almost a year in these devices with very little signs of wear. That being said, we know somebody out there will put the string through the gauntlet so we installed a few fallback solutions.

A common area of wear for the string is at the top where it rubs on the bar. If you see it getting precariously thin, you can cut it off and tie the bar clip lower. There are a few extra turns of string on the spool, so you can unfurl a turn or so and you won't lose any string travel. There will be a tutorial for this soon!

If you need to restring the device, the entire center assembly comes off and you'll have access to the spool. A tutorial will be available for this as well.

<strong>Are my magnets supposed to spin in place?</strong>

Don't worry, nothing is wrong with your unit. In our effort to allow easy disassembly, we used screws at the bottom that do not have nylon locking nuts. They'll stay put, but over time they will move around by a fraction of a turn. This doesn't impact the units ability to maintain its magnetic attachment to a ferrous base object. We encourage owners NOT to tighten these bolts, as you can over-tighten them and cause the top part to break.

<strong>EDIT How resilient is OpenBarbell V2?</strong>

We hope you've noticed how sturdy OpenBarbell feels, but we hope you also know that this device is hand made by the Squats & Science team and isn't your ordinary consumer device. It was built to be kept in your gym bag and will last as long as you keep good care of it. Think of OpenBarbell as a fine hand made sports car.  It's beautiful, high performance and rock solid but you probably shouldn't go off-roading with it.

<strong>EDIT Why is my spindle wobbly, and is that OK?</strong>

We evaluated several manufacturing techniques for OpenBarbell. The laser cutter turned out to be our best bet for a high accuracy low cost device. The problem with laser cutters is the optics create a conical beam for cutting, not the super straight laser beam people imagine.

Laser beam cutting edge.
This causes the edge of some parts to be a little crooked, and moving parts to be a little wobbly. We evaluated this fact when deciding to use laser cutting for our manufacturing and it doesn't effect the accuracy or consistency of our device in any way. For more information about how our device works, see the "How does the device work" question.
</blockquote>
<h3>Hacking your device</h3>
<blockquote>
<strong>EDIT How do I hack my device?</strong>

<nowiki>** DISCLAIMER: WE DO NOT RECOMMEND YOU TAKE APART YOUR DEVICE **</nowiki>

We're glad you asked! OpenBarbell V2 is Arduino compatible, has a totally open source design and a completely open source app (if it's not released, we're working on it!). That means there are a ton of ways you can tinker with your device! The best place to start is the [http://squatsandscience.com/wikibarbell/index.php?title=V0.25#Instructions V0.25 Instructions], which will show you how the meat of an OpenBarbell is made.

If you're looking to hack the firmware head over to the [https://github.com/RFduino/RFduino/blob/master/README.md RFduino Readme on GitHub] to get started. You can play with the velocity detection algorithm, send more robust velocity data to the app, display all kinds of information to the screen, program visual cues at certain points of the lift, create a visual metronome for tempo squats, the opportunities are endless!

If you're looking to hack the app, which is where we think the most exciting features can be implemented, check back here soon for more information as we are deep into development as we speak. If you think you can help the team we'd love to hear from you, send us an email at contact@squatsandscience.com.

<strong>Does this stuff void my warranty?</strong>

<nowiki>** DISCLAIMER: WE DO NOT RECOMMEND YOU TAKE APART YOUR DEVICE **</nowiki>

Remember, OpenBarbell V2 doesn't have a standard warranty. It comes with very limited support (outlined above) and a 14 day return policy. That being said, I can split this answer into two sections.

<strong>Hardware:</strong>

If you decide to modify the hardware and break something, we will do our best to make you replacement parts (at close to cost) but we cannot guarantee you parts or fix your device for you for free. We build the device to last, but we can't compensate for your possible lack of DIY skills. If you NEED to hack the hardware or manufacture your own replacement parts, our housing and PCB CAD files are all available via our [https://github.com/seminolemuscle GitHub page]. The V2.0 and V1.0 units share the same PCB.

<strong>Firmware & Electronics:</strong>

Again, we aren't sure how good your hobby electronics skills are, so we can't guarantee our board can make it through bouts with your soldering iron. Upgrading your battery, adding LED's, installing a buzzer are all things that we would not be able to support if it were to go wrong. The same goes for firmware, if you are clever enough you can probably find a way to burn out your PCB via firmware change. We will however support any upgrade to official Squats & Science firmware updates. If you verify that your issue was caused directly because of a firmware update we will do our best to correct the situation.

<strong>EDIT FOR NEW LINKS How do I update my firmware?</strong>

Updating firmware is a little involved, and not for the faint of heart. If you're familiar with Arduino and can navigate a breadboard it isn't too bad. It requires the following parts:



One OpenBarbell V2

[https://www.sparkfun.com/products/10031 One MicroUSB Breakout Board]

[http://www.rfduino.com/product/rfd22121-usb-shield-for-rfduino/ One RFduino USB Shield] (or other FTDI board)

[https://www.sparkfun.com/products/12002 One Breadboard]

[https://www.sparkfun.com/products/12794 Jumper Wires]


<ol>
<li>Follow the guide [https://github.com/RFduino/RFduino here] (scroll down) to both install the Arduino IDE (if you haven't already) and RFduino compatibility.</li>
<li>Grab the latest firmware from our [https://github.com/seminolemuscle/V1.0 GitHub].
<li>Download the [http://squatsandscience.com/wp-content/uploads/2015/07/OpenBarbell-Libraries-1.zip OpenBarbell V2 required libraries] and paste them into your Arduino libraries folder.
<li>Use Git to clone or [https://github.com/fullerth/Filters/archive/bb959e7.zip unzip a copy] of the [https://github.com/fullerth/Filters Filters Library] into your Arduino libraries folder.
<li>Put together your breadboard
<ol>
<li>Wire the MicroUSB breakout to the RFduino USB Shield in the following configuration (MicroUSB Breakout --> RFduino USB Shield) ([http://squatsandscience.com/wp-content/uploads/2015/07/RFduino-USB-Shield-schematic.png see the RFduino USB Shield schematic here])
<ol>
<li>D+ --> GPIO0</li>
<li>D- -->GPIO1</li>
<li>ID --> RESET</li>
<li>GND --> GND</li>
<li>VCC --> +3V</li>
</ol>
<li>Plug the RFduino MicroUSB Shield into your computer, go into the Arduino IDE and navigate to Tools --> Board and choose "RFduino", and select your COM port (you may need trial and error to pick the correct one).</li>
<li>Plug the MicroUSB Breakout into your OpenBarbell.</li>
</ol>
<li>Upload code!</li>
</ol>
</blockquote>

<h2> Getting Started </h2>
[[#toc|Back to Table of Contents]]

<h3>EDIT Whats in the box...</h3>
1. One official Squats &amp; Science OpenBarbell V2 unit

<img src="http://squatsandscience.com/wp-content/uploads/2015/07/OpenBarbell_V1_Announce_dark.png" height="169" width="300"> 

<img src="" height="" width="X"> 

2. One MicroUSB cable for charging ONLY (you can pair it with your cellphone charger)

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_112948.jpg" height="169" width="300"> 


3. A thank you letter from us, including the unit number of your specific device.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_113506.jpg" height="169" width="300"> 

4. One lanyard for mounting onto the bar

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_112929.jpg" height="169" width="300"> 

5. The hopes and dreams of two guys who just want you to be a better you.
<h3>What next...</h3>
<ol>
	<li>Read our care instructions! It's imperative that you treat your OpenBarbell the way you'd like it to treat you. There's information about safe OpenBarbell placement during your workout, transporting your device, battery management, device maintenance, etc.</li>
	<li>Using your device:
<ul>
	<li>Using your device is simple. As you can see in the instruction card included with the device, all you need to do is turn it on, anchor it to a plate or rack, attach it to the bar, and lift!</li>
</ul>
</li>
</ol>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/final-final-instructions.png" height="418" width="512"> 

<h3>Begin Set...</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7487.jpg" height="203" width="300"> 

On the begin set screen, you can see the rep number you're on in the top left (it will always be Rep#: 1 on the Begin Set screen), the time since your last rep in the top middle, and the percentage of battery remaining in the top right. This is called the System Tray and will almost always be present for your device.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7488.jpg" height="195" width="300"> 

After you complete your first rep, you'll default to the Power Mode (more on that in a second). The power mode displays the System Tray at the top, Average Velocity for that rep nice an big in the center, Peak Velocity at the bottom left and Range of Motion of the rep on the bottom right. As you can see, the rest timer at the top center resets after each rep is performed.
<h3>Olympic Mode</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7492.jpg" height="175" width="300"> 

If you'd like to switch to a different data set more suited towards Olympic Weightlifting, press and hold one of the buttons for three seconds to switch over.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7490.jpg" height="176" width="300"> 

As you can see in this mode, Peak Velocity is displayed prominently in the center of the screen, with the duration of the lift at the bottom left, and the spot at which you achieved your peak velocity for that lift in the bottom right. You can switch from Power Mode to Olympic Mode by holding either button for three seconds, and it will display the same rep data during each mode, for a total of five metrics for each lift.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7493.jpg" height="177" width="300"> 

Holding down a button for three more seconds returns you to Power Mode.
<h3>Invert Mode</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7494.jpg" height="180" width="300"> 

Holding down both buttons for three seconds will send you into Invert Mode. Invert Mode is used if you would like to mount your device up-side down above your exercise implement. This essentially tells the device to pay attention to the opposite direction, since while inverted we care about the velocity coming <em>towards </em>the device, instead of away. <a href="http://squatsandscience.com/wikibarbell/openbarbell-wiki/openbarbell-v1-0/care-instructions/">PLEASE READ OUR CARE INSTRUCTIONS BEFORE USING YOUR DEVICE WHILE INVERTED</a>.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7496.jpg" height="171" width="300"> 

Invert mode displays the same data as non-inverted mode, but you can now accomplish reps with the device above you.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7497.jpg" height="177" width="300"> 

Another three second hold turns off Invert Mode.
<h3>Deleting Past Set</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7489.jpg" height="181" width="300"> 

Tapping the right button until you reach the end of your set will display the 'Delete Past Set' screen. If you chose to tap the right button once more, you will remove all previous rep data from device memory. Tapping the left button will preserve your rep data.

<h2> Interacting with the Device </h2>
[[#toc|Back to Table of Contents]]

On the hardware side, OpenBarbell V2 has two input buttons that you can use to toggle between reps, reset rep memory, wake the screen, switch between Power Mode and Olympic Mode, and invert the device. It also has a power switch for (obviously) turning on and off power supply, a MicroUSB port for charging and uploading firmware, an OLED display for displaying device functionality to the user, and a string/string hook for measuring barbell velocity.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/Input.png" height="576" width="1024"> 


&nbsp;

See screen shots of the UI in the [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Getting_Started Getting Started] section.

&nbsp;

<h2> Interpreting the LEDs </h2>
[[#toc|Back to Table of Contents]]

At rest, the green LED indicates the device is on, will blink every 2 seconds to catch your attention if it is inadvertently left on. The purpose of this LED can be modified by playing with our Arduino Code - https://github.com/seminolemuscle/V0.24 - for whatever you'd like.


<img src="http://squatsandscience.com/wp-content/uploads/2016/04/Me0Bnbu-Imgur.gif"> 


The red LED indicates the battery is being charged. When the LED turns off that means your battery is fully charged. If the LED is showing a less bright red than usual, don't worry. That's a bug with the LiPo battery charging chip and can usually be fixed by unplugging your device and plugging it back in. The red LED cannot be changed via firmware as it is connected directly to the LiPo charging chip and not the RFduino microcontroller.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_103906.jpg" height="401" width="712"> 


<h2> Battery Life and Charging </h2>
[[#toc|Back to Table of Contents]]

The Squats and Science OpenBarbell V2 is equipped with a 1600 mAh battery. Let's put that in perspective.

&nbsp;

FitBit Flex: 50 mAh

iPod Nano: 220 mAh

Moto 360 Smartwatch: 300 mAh

iPhone 6S: 1715 mAh

&nbsp;

We wanted to make sure you didn't have to worry about charging another device every day. In preliminary testing we've operated the OpenBarbell V2 for the equivalent of weeks of training sessions, theoretically much more if battery is conserved by shutting the device off between sets. With a standard phone charger, the device can charge from nearly empty to 40%+ in minutes, and can charge completely within about two hours. We are currently testing our battery capacity in terms of actual reps completed and will publish our findings here when they're available.

&nbsp;

<strong>Battery Study Findings:</strong>

The following are results we've found when using a device that has had the battery conditioned (charged and discharged) several times, giving us more consistent results. Each test has been a traditional workout session consisting of about 50-60 total reps over the course of 1.5-2 hours, without a Bluetooth connection and keeping the device on between sets. The results vary depending on the current state of battery charge.

&nbsp;

BATTERY LEVEL/BATTERY DRAIN

93%/10%

86%/11%

54%/6%

31%/2%

13%/7%

&nbsp;

As you can see, there is a general trend where the lower the current battery level is at the beginning of the workout, the longer it seems to last. We're estimating on average a lifter can get 10 uses per month if used in the conditions stated above.

&nbsp;

<strong>Battery Care</strong>

Battery care is essential for any consumer electronics device. We recommend you let your battery experience nearly a full range of its capacity every charging cycle. Let it discharge down to less than 5% and charge it until it is full, rinse and repeat. Try very hard not to let your battery die, as it can impact longevity and the function of its internal circuitry. You can feel free to use your cellphone charger for this device, and we have tested it with chargers that go up to 2.0A supply current (it will charge faster with chargers that have greater supply current).

&nbsp;

If your battery is giving you fluctuating readings, or rapidly reducing after it is unplugged do not worry. The batter fuel gauge chip has a learning period until it figures out your batteries habits, and it can sometimes be tricked by different chargers. It seems there is about a 3 charge cycle learning period until you can get consistent, predictable readings. Even then, there may be sudden drops in readings or it may not drop much at all during the same usage period.

&nbsp;

We've added a blinking LED light to indicate when the device is left on. If you see this blinking light and you intend for your device to be off, it is an indication that you should turn off your device. Although OpenBarbell V2 lasts quite a while, it can discharge a significant amount overnight as it consumes most of its current at rest.

&nbsp;

<h2> Care Instructions </h2>
[[#toc|Back to Table of Contents]]

It's imperative that you care dearly for your brand new Squats &amp; Science OpenBarbell V2. Your new velocity measuring device is not indestructible, in fact there are several ways you can destroy your brand new strength tool during your workout. Here's our attempt at a comprehensive list of ways you can do just that.

<strong>EDIT Dropping weight on your device</strong>

It's very possible to drop a barbell or other implement on your OpenBarbell since it can be located directly below your exercise equipment of choice. OpenBarbell was not designed to live through this event and will surely break into quite a few pieces if this were to happen. To avoid this tragic occurrence, try to place OpenBarbell in a spot under your implement that is not in immediate crushing danger. For a barbell, do not place the unit below the weights themselves, rather to the side where there will be clearance in the case where it is dropped. Please also make sure to keep the device as close to the same position every time you use it, preferably with the string completely vertical (but not directly under the weights!).

&nbsp;
<h3><strong>Crushing the string hook/cutting the kevlar string</strong></h3>
In our tests we were able to both break the nylon string hook as well as cut the kevlar string by pinching it between sharp knurling and a metal rack hook. To ameliorate this occurrence, we shipped each unit with a fabric lanyard that can be looped around the bar and hooked onto the device. This way, the string can still be mounted inside the barbell collar for barbell exercise so it does not need to be repeatedly removed between weight changes. If you do not like this mounting configuration and would rather mount it directly onto the bar without the lanyard, we recommend you do so outside of the weights to reduce the chance of wear and tear due to knurling and contact between the bar and rack.
<h3><strong>Transporting OpenBarbell V2</strong></h3>
OpenBarbell V2 is meant to live in your gym bag, but it isn't a pair of squat shoes or wrist wraps. It should be kept away from heavy items like metal belt clips or wooden shoe soles, and should not be dropped onto the ground from any height without cushioning. A simple solution would be to put it in a side pocket of the gym bag that does not extend to the bottom of the bag, keep it in a dedicated draw string bag inside your gym bag, keep it inside a (dry) knee sleeve, or even toss it in a dedicated sock or coozie.
<h3><strong>Battery maintenance</strong></h3>
Make sure to see our [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Battery_Life_and_Charging Battery Life and Charging] section of the user manual. To summarize, we recommend not using a MicroUSB charger above 2.0 A supply current. We also do not recommend fully discharging your device, or leaving it on the charger for very elongated periods of time. To condition your battery, make sure to fully charge your device each time and discharge down to about 5% before recharging. Keep OpenBarbell away from temperatures above 110 degrees F or below 32 degrees F for extended periods of time.
<h3><strong>EDIT Assembly/Disassembly</strong></h3>
OpenBarbell V2 was designed to be fully serviceable. We understand parts in the device might need care every once in a while, but we cannot guarantee that skills of our customers in assembling and disassembling their device. That is why we cannot support any problems that occur due to our customers fixing their device themselves. Any issues found upon receipt of the device can be fixed by us for free within 14 days of the product arriving at your doorstep. If any disassembly is required after that, please contact us and we will work out an amicable solution to your repair needs.
<h3><strong>EDIT Safe magnetic mounting of OpenBarbell V2</strong></h3>
It is possible to damage OpenBarbell if it is carelessly mounted onto a hard ferromagnetic surface (a metal plate or rack). We recommend gently placing the device down to reduce the odds of a stress fracture in the acrylic housing.

If mounting the device in invert mode, it is very important to make sure it has a very secure mounting spot for all four magnets, and that it is not being pulled by the string at an odd angle as to introduce a lateral force that can remove one side of the device from its mounting position. Unless that is achievable, we do not recommend inverting your device.
<h3><strong>Caring for the Housing</strong></h3>
The exterior and many of the internal parts of the device are made from a cast Acrylic - also known as Plexiglass, Lucite and Acylite. With proper care this device should be able to last for years to come, however acrylic is susceptible to scratches and abrasions as well as damage from some chemicals.

Most of the superficial dirt and grime that the OpenBarbell will pick up can be wiped away with a mild solution of soap, water and a rag. This device is by no means water-proof but will withstand a very lightly damp rag (just stay away from the buttons, usb, and switch!). If you want to do some heavier cleaning then we have to take some precautions. The best way to clean cast Acrylic is with products specifically designed for cleaning cast Acrylic such as Novus No. 1 or Brillianize. <strong>It is important to NEVER use cleaning solutions with Ammonia (such as Windex or Formula 409), gasoline, denatured alcohol (paint thinner), carbon tetrachloride, or acetone!</strong> All of these product will cause the Acrylic to Craze with minute cracks.

<h2>EDIT FOR NEW LINKS Loading Code </h2>
[[#toc|Back to Table of Contents]]

The purpose of this brief tutorial is to demonstrate how to upload code to an OpenBarbell V2 unit made at home, or modified by an owner. Before we begin, please read our [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Warranty Warranty]

&nbsp;

To load code on your device you need a few things:
<ol>
	<li>Female to male USB cord</li>
	<li>[http://www.rfduino.com/product/rfd22121-usb-shield-for-rfduino/ RFduino USB Breakout Board] ([http://forum.rfduino.com/index.php?topic=75.0  or another FTDI Breakout Board]</li>
	<li>[https://www.sparkfun.com/products/10031 MicroUSB Breakout Board] (or you can find one online that requires no soldering)</li>
	<li>Breadboard</li>
	<li>Female to male breadboard jumper wires</li>
</ol>
&nbsp;

Essentially what we're doing is connecting the RFduino on your device to an FTDI breakout board. We routed the appropriate pins to the spare microUSB pins on the board for easy access, but don’t go plugging it into your computer. We need to get those pins hooked up to your FTDI board to convert it to a language your computer can understand. You need 5 pins to program an RFduino, GND, VCC, TX, RX, and RESET. TX and RX are hooked up to pins GPIO0/1 so they are routed to USB pins D+ and D-. The most convenient way to access these pins is to split a USB cord, but most USB cords do not utilize the ID pin and therefore do not have a 5th wire. If you do not have a 5 pin microUSB cable, you need a microUSB breakout board to have access to these pins. See the schematic below for reference.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/GPIO_to_USB2.png" height="632" width="476"> 

VUSB above is the vertical USB port on the top of OpenBarbell. This will match with the labeled pins on the microUSB breakout board. Those pins need to be routed to the same pins on the RFduino USB Shield.

&nbsp;

Once that is set up, you should head over to the [https://github.com/RFduino/RFduino Getting Started page of the Rfduino Github]. That will walk you through downloading and setting up an RFduino compatible version of the Arduino IDE. You can run a default RFduino example to blink the OpenBarbell LED on pin 2. If you can get that to work, you're ready to download our code and libraries. Several of them are slightly modified to fit our exact needs, or to fix a few issues we found along the way. [http://squatsandscience.com/wp-content/uploads/2016/03/OpenBarbell-Libraries-Modified.zip You can find the modified libraries here]. Place them alongside your other Arduino libraries in your installation folder.

&nbsp;

Last but not least, grab our firmware off of GitHub and upload it onto your device. [https://github.com/seminolemuscle/V1.0/blob/BlueToothFloatingPt/Arduino%20Code/OpenBarbellV1.0/OpenBarbellV1.0.ino Our latest revision can be found here].

&nbsp;

We'll be writing a more detailed calibration method in the near future, but for now the following should suffice. If you're re-loading firmware onto a device you purchased, contact us for your tic length, we will give you a very accurate number you can use in your code for your specific device.

&nbsp;
<ol>
	<li>Place a caliper above your device (MINIMUM 12 inch caliper, the longer it is the more accurate your calibration will be) and have the string follow the caliper precisely. Do this several times around the maximum caliper displacement and record the ROM from the device, and the displacement from the caliper.</li>
	<li>We set the default tic length (string displacement between encoder readings) at 2.667 mm. Take each ROM you recorded and divide it by the tic length, then round to the nearest whole number. This represents the number of encoder readings.</li>
	<li>Next, divide each caliper displacement by the corresponding number of encoder readings. This will give you a new tic length. Average each of your recorded tic lengths (since you did the measurement several times) and this will be your new ticLength variable on line 56 of our code.</li>
	<li></li>
</ol>
That's it! Go lift some weights, and make sure to sign up for [http://squatsandscience.com/velocity_tracking/ Squats &amp; Science Velocity Tracking] so we can help you optimize your training!

<h2>EDIT FOR NEW PROTOCOL Bluetooth Communication</h2>
[[#toc|Back to Table of Contents]]

What really unlocks some great potential with the OpenBarbell V2 is the ability to take the information off the unit for use online or in an app and to set configurable values. In order to accomplish this the device utilizes BLE (Bluetooth Low Energy) to talk with a paired phone.

&nbsp;

<hr />

&nbsp;
<h3>(OpenBarbell --&gt; Phone)</h3>
By default the device will transmit limited information to a paired phone at the end of a rep. All of the information calculated on the device will be sent but the raw times between the encoder ticks will be compressed. The limitation imposed on this transmission is the amount of time necessary to send the requested data and the battery drain resulting from continuously broadcasting via bluetooth. In order to ensure we do not miss a rep and/or to ensure that we are not transmitting at the start of a rep we have kept default transmissions to a minimum.

The following is a breakdown of how the data is transmitted to the phone in the order that the phone receives it
<h4>-1234</h4>
<blockquote>This is a unique number sequence that will signify to the app (and to the person looking at the data) that the rep has begun. Data transmission is then held until the rep is complete.</blockquote>
<h4>Rep #</h4>
<blockquote>Once the rep is complete there will be a string of data coming to the phone. The first piece of data coming is the "Rep #" - this number corresponds to the "Rep #" displayed on the unit.</blockquote>
<h4>Avg Velocity</h4>
<blockquote>This is the average velocity during the rep as calculated on the device.</blockquote>
<h4>ROM (Range of Motion)</h4>
<blockquote>This is the distance traveled, in mm, through the rep</blockquote>
<h4>Peak Velocity</h4>
<blockquote>This is the peak instantaneous velocity during the rep as calculated on the device.</blockquote>
<h4>Peak Velocity Location</h4>
<blockquote>This is the location, expressed as a percentage, at which the peak velocity occurred. For example, if the peak velocity location was "63%" with a ROM of "1000 mm" then the peak velocity location occurred at 63% of 1000 mm or 630 mm into the rep.</blockquote>
<h4>-9999 (Start compression data)</h4>
<blockquote>This is a unique number sequence to signify that the "Compression Data" transmission will now begin</blockquote>
<h4># of ticks counted</h4>
<blockquote>As discussed above, by default, only a sample of the total lift will be sent over to the phone to conserve transmission time and battery life. The "# of ticks counted" corresponds to the frequency at which we log the data to be sent.

For example, if this said "5" then that would mean every 5th tick of the encoder we would save the value - as in...

<span style="color: #ff6600;">Tick #1 - Not Saved, Tick #2 - Not Saved, Tick #3 - Not Saved, Tick #4 - Not Saved,</span> <span style="color: #99cc00;">Tick #5 - Saved,</span>  <span style="color: #ff6600;">Tick #6 - Not Saved, Tick #7 - Not Saved, Tick #8 - Not Saved, Tick #9 - Not Saved,</span> <span style="color: #99cc00;">Tick #10 - Saved, <span style="color: #ff6600;">Tick #11 - Not Saved, Tick #12 - Not Saved, Tick #13 - Not Saved, Tick #14 - Not Saved,</span> <span style="color: #99cc00;">Tick #15 - Saved,</span></span> <span style="color: #99cc00;"><span style="color: #ff6600;">Tick #16 - Not Saved, Tick #17 - Not Saved, Tick #18 - Not Saved, Tick #19 - Not Saved,</span> Tick #20 - Saved, </span>etc....

Then when the values are sent over they are sent in order that they were saved. So for the above example of "5 ticks" the string of compressed data would be .... Tick #5, Tick #10, Tick #15, Tick #20, Tick #25, etc...

In order to the get the compression ratio, divide one by the "# of ticks counted". So, continuing with our above example of 5, the compression ratio would be 1/"# of ticks counted" or 1/5 ticks would be counted or a net result in 20% of the available data being sent.</blockquote>

<h4>Precision of Compressed Values</h4>
<blockquote>Another way we compress the data being sent is to utilize all the available size in the data types being sent to the device.

For example,  say we wanted to send two DTs worth of information to the device. DT1 has a value of "100 ms" while DT2 has a value of "140 ms". We could send the first DT, DT1, followed by the second DT, DT2 - that would look something like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">DT1</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2: <span style="color: #ff6600;">DT2</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
This would be fine and it would work for such a short string but when we start having to send over many hundreds of values it can really slow things down. We can save on transmission time by compressing both DTs into one message...here's the underlying principle...

The data type that BLE uses to send its data is called a Floating Point Number - [https://en.wikipedia.org/wiki/Single-precision_floating-point_format Here's a good write up on Floating Point Numbers from Wikipedia]. In it's simplest embodiment, the floating point number can represent a value with 8 locations for digits where we can choose to put the decimal place wherever we would like within/outside those 8 locations. See the picture below for an explanation...

&nbsp;

<p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/03/FloatingPointExplanation-1.png" height="596" width="600"></p>


As you can see above, this data type can be used to represent very large numbers (1,075,270) as well as very small numbers (.34375). However, we should also notice that regardless of the value of the number (i.e. 100 or 1,075,270), all 8 positions of the data type will be utilized regardless if there is meaningful information in those positions. One way to think about this is by placing leading zeros in front of the values. For example, 100 is represented as 00000100 and 1,075,270 is represented as 01,075,270. Thus, a value of 100 and 1,075,270 have the same size in terms of the amount of data being sent over bluetooth. So this brings us to how we might utilize this information to compress the data via bluetooth.

If we go back to our original example of DT1 and DT2 (100 ms and 140 ms, respectively) now we know that it will actually look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">00000100</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2: <span style="color: #ff6600;">00000140</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
Let's combine both of those numbers into one number by dividing the second number by 10,000 (to shift the decimal places over 4 values) and add it to the first. Now we'll have DT1+DT2/10,000 = 100 + 140/10,000 = 100 + .0140 = 100.0140. And voila, we've turned two numbers into one number and we can easily separate them as well. Let's see what his new transmission might look like...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0100.0140</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
Just for one more example, lets compress the following string of numbers and send them over... 123, 52, 5124, 62, 462, 688, 123, 2, 4123,6252 ... if we apply the same compression above to these values then we would get the following message...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0123.0052</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">5124.0062</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 3: <span style="color: #ff6600;">0462.0688</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 4 : <span style="color: #ff6600;">0123.0002</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 5: <span style="color: #ff6600;">4123.6252</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
FANTASTIC! We did it, right?! Yeah, of course we did! So we've been talking a lot about "compression" but we still haven't touched on what the "Precision of Compressed Values" is...for that we have to did just a little bit deeper to understand.

One of the main things measured on the device is the amount of time in microseconds between "ticks" of the encoder. Yeah, microseconds, as in there are 1 million of them per second. As you can imagine that number gets very large very fast - this number can actually get up to 4,294,967,296 which is ~4.3 trillion microseconds or about ~4,294 seconds or ~72 minutes.

For a realistic scenario, let's say the average speed of a 1 meter ROM lift is .75 m/s. Some simple math tells us that the time of the lift is about 1.33 seconds [(1 meter)/(.75 meter/second)=~1.33 seconds]. We can do some more math to calculate how many ticks occurred during that lift since we know there are roughly 2.667 mm/tick to figure out there was roughly 374 ticks [1 meter = 1000 mm --&gt; (1000 mm)/(2.667 mm/tick)= ~374 ticks]. If we take the amount of time for the lift, 1.33 seconds, and divide by the number of ticks, 374, we will get to an average length of time between the ticks of, (1.33 seconds)/(374 ticks)=.00355615 seconds/tick or (if we multiply by 1,000,000 microseconds/second) about ~3556 microseconds/tick. Now that we know the average dt between ticks lets pick some numbers around that average for a sample transmission - Let's say 3550, 4267, 3000, 3687

If we apply the above compression the data transmission would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">3550.4267</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">3000.3687</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
This all seems great until we consider what might happen for a lift with an average velocity of .25 m/s with a 1 meter ROM. If we do the same math as above we find  (1 meter)/(.25 meter/second)=4 seconds --&gt; (4 seconds)/(374 ticks)= ~.01069519 seconds/tick or roughly 10,695 microseconds/tick. Now let's pick some numbers around this average time - Let's say 11,212, 10501, 9,632, 10729. However, there's a problem. Now that we have 5 digit numbers, we wouldn't be able to fit it into the above compression method as there are only 8 placeholders for digits and two 5 digit numbers would require 10 placeholders. What to do? Well, we can finally get to the whole purpose of this section,  the "precision of the compressed value".

While these 10 digits of precision are necessary for the device to do its job correctly (as in the number of digits in 4,294,967,296), we may be perfectly fine in shaving the last digit of precision - as in the difference to us of 525,967,283 microseconds vs 525,967,280 microseconds is not very much - we're literally talking about a rounding error there of 3 microseconds or .000003 seconds. For this reason the device will, by default, divide all of the DTs (time between ticks) by "10" (the default "precision of the compressed value") before sending them over. So if we take the above example numbers for the .25 m/s lift - 11212, 10501, 9632, 10727 -and divide them by 10 (and round to the nearest integer) we get values that we can fit into our compression scheme - 1121, 1050, 963, 1073 - Thus the transmission for the .25 m/s lift would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">1121.1050</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">0963.1073</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
If we now apply this principle of "precision of the compressed value" to the .75 m/s lift we see that it would actually be sent over like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0355.0427</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">0300.0369</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
So what's the trade off here? In order to, by default, allow some of the slowest lifts to fit into the compression method we have to round the last digit of the time. This means that for very fast lifts, with very small DTs, we lose some precision. But the good thing is that if you want that last digit of precision, you can have it, just set the "precision of the compressed value" to 1 and the full microsecond number will come over. In any scenario there exists the possibility of generating a number with over 4 digits, even after you apply the "precision of the compressed value" divider - in that case the number is sent over by itself.

So, for one final example - if we want to send the following values... 1963, 1938, 19381, 39103, 739173, 9381, 1912...the transmission would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">1963.1938</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">00019381</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 3 : <span style="color: #ff6600;">0039103</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 4 : <span style="color: #ff6600;">00739173</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 5 : <span style="color: #ff6600;">9381.1912</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
</blockquote>
<h4>-<span class="match">9876</span></h4>
<blockquote>This is a unique number sequence to signify that the "Compressed Bulk Data" transmission will now begin</blockquote>
<h4>**"COMPRESSED" BULK DATA**</h4>
<blockquote>This is the compressed bulk data - this will be a snapshot of some or all of the DTs between ticks - see [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Precision_of_Compressed_Values Precision of Compressed Values] for more details. Although this is written as "11." this section could be anywhere from 1 message long to hundreds if not 1000+ messages depending on the settings of the user.</blockquote>
<h4>-6789</h4>
<blockquote>This is a unique number sequence to signify that the "Compressed Bulk Data" transmission has completed</blockquote>
<h4>Battery charge</h4>
<blockquote>This will send the battery charge of the device to the phone to keep tabs on the device.</blockquote>

<hr />

<h3>(Phone --&gt; OpenBarbell)</h3>
<span style="color: #ff0000;">Note - All transmissions to the OpenBarbell must be done in HEX format - since we don't normally think in base16 here's a helpful site to convert DECIMAL notation (base10 - what you would interact with on a daily basis) into the proper format (HEX) to send http://www.binaryhexconverter.com/decimal-to-hex-converter

<hr />

<h4>Minimum Rep Threshold (01 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">01</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = The "minimum rep threshold", in mm, in HEX notation</span>

<span style="color: #008000;">Explanation: </span>The minimum rep threshold is the minimum distance, in mm, that will be counted as a valid ROM.

<span style="color: #ff6600;">Range:</span> <span style="color: #800080;">XX</span> can range from 00 (0 mm) to FF (255 mm)

<span style="color: #ff00ff;">Default Value:</span> 150 mm

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "0 mm" which will count any ROM as a valid rep as any rep will have a ROM greater than 0 mm</li>
</ul>
</li>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">64</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; 100 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "100 mm" which will not allow any rep with a ROM less than 100 mm to be counted as a valid rep</li>
</ul>
</li>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">C8</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(C8 in Hex = 200 in Decimal ==&gt; 200 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "200 mm" which will not allow any rep with a ROM less than 200 mm to be counted as a valid rep</li>
</ul>
</li>
</ul>

<hr />

<h4>Power/Olympic Mode Select (02 XX)</h4>
<span style="color: #993300;">Interaction: </span> <span style="color: #ff0000;">02</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = "Mode Select" in HEX notation</span>

<span style="color: #008000;">Explanation: </span>Use this function to switch between Power Mode and Olympic Mode. In order to switch between the two modes the full range of 00 to FF is divided into two sections.

<span style="color: #993300;"><span style="color: #ff6600;">Range:</span></span>
<blockquote>Power Mode - <span style="color: #800080;">XX</span> can range from 00 (0) to 09 (9)

Olympic Mode - <span style="color: #800080;">XX</span> can range from 0A (10) to FF (255)</blockquote>
<span style="color: #ff00ff;">Default Value:</span> n/a

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Power/Olympic Mode Select)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; Power Mode)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC) which falls in the range of 0-9, thus we have selected Power Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">07</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(07 in Hex = 7 in Decimal ==&gt; Power Mode)</span>
<ul>
	<li>In this example we sent over a value of 07 (HEX) or 7 (DEC) which falls in the range of 0-9, thus we have selected Power Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">0A</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; Olympic Mode)</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC) which falls in the range of 10-255, thus we have selected Olympic Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">AC</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(AC in Hex = 172 in Decimal ==&gt; Olympic Mode)</span>
<ul>
	<li>In this example we sent over a value of AC (HEX) or 172 (DEC) which falls in the range of 10-255, thus we have selected Olympic Mode</li>
</ul>
</li>
</ul>

<hr />

<h4>Low Pass Filter Frequency (04 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">04</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = Low Pass "Filter Frequency", in hertz, in HEX notation</span>

<span style="color: #008000;">Explanation: </span>In order to work with some of the mechanical properties of the device it is necessary to apply a low pass filter for accurate peak velocity values. Read more about this filter here: http://playground.arduino.cc/Code/Filters

<span style="color: #ff6600;">Range:</span> <span style="color: #800080;">XX</span> can range from 00 (0 hz) to FF (255 hz)

<span style="color: #ff00ff;">Default Value:</span> 10 hz

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Low Pass Filter Frequency)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 hz)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC), this will set the filter frequency to 0 hz</li>
</ul>
</li>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">0A</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Low Pass Filter Frequency)</span> <span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; 10 hz (default value))</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC), this will set the filter frequency to 10 hz (the default value)</li>
</ul>
</li>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">AC</span> =&gt; <span style="color: #ff0000;">(Low Pass Filter Frequency)</span> <span style="color: #800080;">(AC in Hex = 172 in Decimal ==&gt; 172 hz)</span>
<ul>
	<li>In this example we sent over a value of AC (HEX) or 172 (DEC), this will set the filter frequency to 172 hz</li>
</ul>
</li>
</ul>

<hr />

<h4>Compressed Transmission Settings (08 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">08</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = is a value in HEX notation that can either change the precision of the compressed values or the compression ratio
</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">In order to compress the data coming from the OpenBarbell there are two compression schemes. The first is to send only a certain ratio of the collected data (as in one out of every 5 or one out of every 10 pieces of data collected) while the second is round the values to one decimal place and remove the trailing zero (as in "12237" rounds to "12240" and is sent over as "1224"... this reduces the overall size of the data being sent over). When setting the RATIO the value sent is put over 1 (as in the ratio becomes 1/XX). When setting the PRECISION there are only two settings - rounding or full precision. Sending <span style="color: #ff0000;">08</span> <span style="color: #993366;">FE</span> will allow the rounding of the sent values to 1 decimal place while sending <span style="color: #008000;"><span style="color: #000000;"><span style="color: #ff0000;">08</span> <span style="color: #993366;">FF</span></span></span> will force full precision values to be sent. See the section above entitled [[Precision of Compressed Values]] for more detail.

<span style="color: #ff6600;">Range: </span>

<span style="color: #800080;">XX</span> can range from 01 (1) to FD (253) to change the <strong>RATIO OF SENT VALUES</strong>

<span style="color: #800080;">XX</span> can either be FE (254) or FF (255) to change the <strong>PRECISION OF THE VALUES</strong>

<span style="color: #ff00ff;">Default Value:</span>

<strong>RATIO</strong> of sent values: <strong>5</strong> (This results in 1/5 of the values collected being sent)

<strong>PRECISION</strong> of sent values: <strong>FE</strong> (Rounded)

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">01</span> =&gt;<span style="color: #ff0000;"> (Compressed Transmission Setting) </span><span style="color: #800080;">(01 in Hex = 1 in Decimal ==&gt; Ratio of 1/1)</span>
<ul>
	<li>In this example we sent over a value of 01 (HEX) or 1 (DEC). Because 1 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 1 in this case will make the ratio 1/<strong>1</strong>, or will force all values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">05</span> =&gt; <span style="color: #800080;"><span style="color: #ff0000;">(Compressed Transmission Setting) </span>(05 in Hex = 5 in Decimal ==&gt; Ratio of 1/5 (default value))</span>
<ul>
	<li>In this example we sent over a value of 05 (HEX) or 5 (DEC). Because 5 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 5 in this case will make the ratio 1/<strong>5</strong>, or will only allow one out of every <strong>five</strong> values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; Ratio of 1/100)</span>
<ul>
	<li>In this example we sent over a value of 64 (HEX) or 100 (DEC). Because 100 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 100 in this case will make the ratio 1/<strong>100</strong>, or will only allow one out of every <strong>hundred</strong> values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">FE</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(FE in Hex = 254 in Decimal ==&gt; Rounded Values)</span>
<ul>
	<li>In this example we sent over a value of FE (HEX) or 254 (DEC). Because 254 (DEC) is in the range of 254 to 255, this value will adjust the <strong>PRECISION</strong> of sent values. A value of 254 in this case will send over the default precision where the values will be rounded to the tens place and the trailing zero removed.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">FF</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(FF in Hex = 255 in Decimal ==&gt; Full Precision)</span>
<ul>
	<li>In this example we sent over a value of FF (HEX) or 255 (DEC). Because 255 (DEC) is in the range of 254 to 255, this value will adjust the <strong>PRECISION</strong> of sent values. A value of 255 in this case will send over the full precision of the collected values with no rounding.</li>
</ul>
</li>
</ul>

<hr />

<h4> OLED Back Light Timeout (10 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">10</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = "OLED Back Light Timeout", in seconds, in HEX notation</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">The OLED screen on the device is back lit to aid in viewing the display. This adjustment allows one to modify the time that the screen stays on before timing out. </span></span>

<span style="color: #ff6600;">Range: </span><span style="color: #800080;">XX</span> can range from 00 (0 seconds) to FF (255 seconds)

<span style="color: #ff00ff;">Default Value:</span> 10 seconds

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (OLED Back Light Timeout)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 Seconds)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC), this will set the back light timer to 0 seconds which will effectively mean that they screen no longer turns on - This may be helpful to conserve battery life when Bluetooth is being used.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(</span><span style="color: #ff0000;">OLED Back Light Timeout) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; 10 Seconds (default value))</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC), this will set the back light timer to 10 seconds (the default value)</li>
</ul>
</li>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(</span><span style="color: #ff0000;">OLED Back Light Timeout)</span> <span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; 100 Seconds)</span>
<ul>
	<li>In this example we sent over a value of 64 (HEX) or 100 (DEC), this will set the back light timer to 100 seconds (or 1 minute and 40 seconds)</li>
</ul>
</li>
</ul>

<hr />

<h4> Status Check (40 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">40</span> <span style="color: #800080;">XX</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">Regardless of the value of XX, this will initiate a status check that can be called at any time to check several important values including a verification of set values from some of the other commands from the phone to the OpenBarbell. The readout from this status check should read as follows:</span></span>
<blockquote>
<ol>
	<li>Ratio of Values Sent</li>
	<li>Precision of Values Sent</li>
	<li>Slowest Instantaneous Velocity</li>
	<li>OLED Back Light Timeout</li>
	<li>Minimum Rep Threshold</li>
	<li>Tic Length</li>
	<li>Battery Charge</li>
	<li>Unit Number</li>
</ol>
</blockquote>
<span style="color: #ff6600;">Range: </span><span style="color: #800080;">XX</span> can range from 00 to FF

<span style="color: #ff00ff;">Default Value:</span> n/a

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Status Check)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
</ul>

<hr />

<h4> Slowest Instantaneous Velocity</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">80</span> <span style="color: #800080;">YY<span style="color: #000000;"> where</span> YY is a code with reference table below
</span>

<span style="color: #008000;">Explanation: </span>The slowest instantaneous velocity is set by the maximum allowable time (in microseconds) between "ticks" of the encoder. The slowest instantaneous velocity can be set any where from ~6.15E-08 m/s to ~.003 m/s or you can disable this filter (and all any instantaneous velocity) by sending a value of FF. See below for more information.

<span style="color: #ff6600;">Range: </span><span style="color: #800080;">YY</span> can range from 00 (6.15371E-08 m/s) to FF (0 m/s)

<span style="color: #ff00ff;">Default Value:<span style="color: #000000;"> .01 m/s</span></span>

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Slowest Instantaneous Velocity)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 6.15371E-08 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 6.15371E-07 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 0.001218435 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">FF</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(FF in Hex = 255 in Decimal)</span>
<ul>
	<li>See below for more information. A value of FF will disable this filter and allow any instantaneous velocity.</li>
</ul>
</li>
</ul>
<strong>Further Explanation</strong>

In version 1.08 the default for the slowest instantaneous velocity is ~0.01 m/s however you can make that much, much slower (any where from ~6.15E-08 m/s to ~.003 m/s). Refer to the table below to see the corresponding number to send to get the desired slowest instantaneous velocity. Keep in mind that the chart below displays values in DECIMAL notation however all values MUST BE SENT IN HEXADECIMAL notation.

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/SlowestInstVelocityFull.jpg" height="498" width="732"> 

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/SlowestInstVelocityLower.jpg" height="498" width="732"> 

<h5> Full Table </h5>
For a full table of values to send to the device for a given velocity see [[SlowestInstVelocity Table]]

<h2> Setup At The Gym </h2>
[[#toc|Back to Table of Contents]]

<h2> Warranty </h2>
[[#toc|Back to Table of Contents]]

The Squats and Science OpenBarbell V2 is unlike most consumer devices available for purchase. It was made by a couple engineers who were fed up with the lack of accessibility for advanced training tools and decided to solve the problem themselves. That meant making something that works quickly and at low cost. Although we would love to continue to support our devices as long as you own them, we will only be making these in small batches and therefore unable to replace parts, dedicate a service team or absorb the costs of return shipping. We will stand by our product up to 14 days after receipt of the device, after which you can contact us for further support inquiries.

OpenBarbell V2, like the name suggests, is also totally open source and Arduino compatible. Normal warranties prevent users from hacking their devices, but we encourage it. We do not wish to preclude you from modifying your device and we hope you have the ingenuity to create functionality that the community can take advantage of. We cannot however fix issues that arise from the modification or alteration of OpenBarbell, and we are not liable for repairs for said issues.

<h2>EDIT Issue List </h2>
[[#toc|Back to Table of Contents]]

This is an evolving known bug list that will likely increase over the next few weeks and month. We cannot find or fix every issue in our firmware and hardware before it's sent out, but we did our best to make sure they were all identified and the serious issues were addressed.
<h3>Peak velocity does not give accurate readings above 2.0 m/s</h3>
<ul>
	<li>Each displacement reading is put through a filter to reduce erroneous values due to encoder imbalances, indoor lighting effecting our optical sensors, inconsistent spring tension, string slack, etc. This filter helps us eliminate bad values but also dampens our good values. If you achieve a maximum instantaneous velocity above 2.0 m/s the display will read "MAX". We understand this limitation for very fast lifts, including Olympic lifts like the snatch and clean &amp; jerk, and we are working hard to introduce a high accuracy mode in the phone app to be released in Spring of 2016.</li>
</ul>
<h3>OpenBarbell does not function as expected when plugged into power</h3>
<ul>
	<li>In order to keep this device as open source as possible we wanted to make sure that you can reprogram the device at will - in order to do this we had to "share" some of the functionality across different hardware. For this reason the USB is not only used to charge the device but also allows reprogramming over FTDI via a USB MicroB Plug Breakout board. For reasons we'd love to discuss with you in depth if you'd like, the USB connection interferes with the button presses. While it is a minor inconvenience we think the ability to hack the device makes up for it!</li>
</ul>
<h3>Switching between Power and Olympic modes can show a 0.00 velocity rep</h3>
<ul>
	<li>This is because the displayed rep is changed after two seconds in order to refresh the screen, so it doesn't appear to be stuck on the 'Power' or 'Olympic' mode. Fixing this bug would have required the introduction of a more sophisticated state machine to run our display, which would have elongated our release schedule. This bug does not effect performance.</li>
</ul>
<h3>Invert mode can be inhibited by slightly misaligned top screws</h3>
<ul>
	<li>Our optical encoders require a precise position to read tics accurately. When assembled, our devices were tested to work recording tics from a position on the floor, and some units needed to be re-calibrated to work in both directions. If these screws loosen over time it might cause this same issue to arise again.</li>
</ul>
<h3>Kevlar knot can come untied from the string hook</h3>
<ul>
	<li>This happens on rare occasions and was remedied by re-affixing each unit to the string hook. If the string comes undone and pulls back into the device, the spindle could un-spin from the spring and lose retractability. If this happens please contact us.</li>
</ul>
<h3>Magnets may be loose and spin in place</h3>
<ul>
	<li>If this is the case for your unit, please do not try to tighten them. Their spinning does not inhibit their ability to magnetically adhere to a surface, and tightening them could interfere with internal component alignment. This issue does not impact performance.</li>
</ul>

<h3>First Timestamp Bug</h3>
<ul>
        <li>A variable named tic_timestamp_last doesn't get cleared between reps when using OpenBarbell V1.0 release code. This causes the very first time measurement of a rep to be huge, but the effect of that is very minimal since it gets filtered out by our low pass filter.</li>
</ul>
<h3>Time Waiting Bug</h3>
<ul>
        <li>We have a function called 'time waiting' that removes velocity readings below a customizable threshold (.01 m/s by default). This is useful because a lift might end very smoothly without changing direction, which is what we use to indicate a rep has finished. We then remove the amount of time spent at the end of your rep. The OpenBarbell V1.0 release code does not also remove the amount of displacement during that time. This usually only accounts for about 3mm of ROM.</li>
</ul>
<h3>0.0 Velocity Bug</h3>
<ul>
        <li>In testing we have very rarely recorded velocities of 0.0 randomly after a long period of use. This has yet to be repeated so we are having a hard time locating the bug. More info will be added here when it's available. </li>
</ul>

<h2> Limitations </h2>
[[#toc|Back to Table of Contents]]

<strong>Limitations:</strong>

There are none! Just kidding, of course there are limitations. OpenBarbell V2 was built to be a low barrier to entry device so people can start taking advantage of velocity based training principles. While we wish we could implement all of the features we have in mind, it wouldn't be feasible for this device. Here are a few things we can't do.

&nbsp;

<strong>Bar Path</strong>

OpenBarbell V2 cannot measure bar path. At the most basic level, it measures the velocity vector of a single point in space in one dimension. As much as we'd like to do some engineering wizardry, there is just no way to figure out where your bar is in space only by pulling out a string. This doesn't mean we can't tell you anything about your form. Our range of motion measurements tell you a lot about your consistency and which reps were higher, lower, tighter and better set-up. Our peak velocity height reading can tell you where you're achieving your fastest speed and you can measure how that changes over time. We think these metrics will be very valuable to your training in the place of absolute bar position.

&nbsp;

<strong>Peak Velocity Over 2 m/s on the Device</strong>

In order to lower costs and make hand assembly in the USA feasible we needed to invent our own optical quadrature encoder. There are companies who focus on that aspect alone for decades and they make wonderful systems. Ours is definitely adequate for its purpose, but there are a few drawbacks. The readings fluctuate a little from one to another, which are averaged out very well with our average velocity calculations. Peak velocity however extracts one reading that is the very fastest, so erroneous spikes can cause a wildly inaccurate reading. To fix this, we put whats called a one pole low pass digital filter on our incoming measurements and this allowed us great accuracy below 1.5 m/s, good accuracy up to 2.0 m/s, and less than consistent peak velocities above that. We made a decision that rather than show you readings we aren't confident about, we will instead display 'MAX' to the screen. A peak velocity above 2.0 m/s is rare in powerlifting so we don't think this will be much of an issue, but Olympic Weightlifting can reach those speeds often. That's why we're implementing much more effective filtering in our upcoming app and a new high precision mode that can unlock some more accuracy from your device.

&nbsp;

<strong>Device Placement</strong>

OpenBarbell V2 must be placed directly below where the bar will be moving in order to achieve accurate and repeatable results. Any angle away from vertical that the string is pulled from the device will reduce the speed your device will read. You don't need to do anything special, just make sure the device is approximately where you expect to be at the end of a walk out, unrack, or break the ground on a deadlift.

&nbsp;

<strong>Bluetooth Transmission</strong>

When our app is launched, it will transmit data in bulk to your device. Since OpenBarbell V2 utilizes the very low power Bluetooth 4.0 LE, our transmission rates cause a delay in the speed at which you can complete reps. To circumvent this issue, we have a high speed mode that sends about 1/5th of the bulk data to your device along with all of the OpenBarbell measurements you see on the OLED screen. What this means is in this mode, your app will be able to do simple graphs and math on your data as well as display the same info on your OpenBarbell screen, but it will not be able to do some more complicated features by default. That's why we've implemented High Precision Mode, where you get every single reading the device captures but it takes anywhere from 1 to 4 seconds to send it all to your device. This mode allows us to do much higher peak velocity readings (see out 2.0 m/s cap above), as well as very high resolution graphing and other features. This will be an option on the app that will activate this mode in the future.

<h2> BOM </h2>
[[#toc|Back to Table of Contents]]
{| class = "wikitable"													
|	Item Number	||	Part Number	||	Description	||	Material	||	Vendor	||	Link	||	QTY.
|-													
|	1	||	Tube Base	||	Exterior Bottom of Unit	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	2	||	Countersunk Magnet	||	3/8" od x 1/8" thick with countersunk hole for #4 screw	||	NdFeB, Grade N42	||	K&J Magnetics, Inc.	||	http://www.kjmagnetics.com/proddetail.asp?prod=R622CS-S&cat=173	||	4
|-													
|	3	||	CircBase	||	Base of inner tower	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	4	||	91772A151	||	Pan Head Phillips Machine Screw - 6-32 Thread, 3/4" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772A151	||	4
|-													
|	5	||	Battery_Top	||	Battery Cover	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	6	||	BearingHolder	||	Bearing Walls	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	2
|-													
|	7	||	608_Bearing	||	Abec 9 - Size 608 Bearings	||	Titanium/Stainless Steel	||	Amazon	||	http://www.amazon.com/Titanium-Stainless-Sporting-Skateboard-Bearings/dp/B00IZ7LBLW/ref=sr_1_11?ie=UTF8&qid=1460066714&sr=8-11&keywords=608+bearing+abec+9	||	2
|-													
|	8	||	Axle	||	Spring/Spindle Axle	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	9	||	SpringSpool	||	Tape Measure Spring Spool	||	Injection Molded Plastic	||	Custom Component	||	n/a	||	1
|-													
|	10	||	Spindle_Wall	||	Spindle Wall without Slots for IR encoder	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	11	||	Spindle_Insert_String	||	Spindle Core with Cutout for String	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	12	||	Spindle_Insert	||	Spindle Core	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	13	||	Spindle_Encoder_Wall	||	Spindle Wall with Slots for IR encoder	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	14	||	91772A114	||	Pan Head Phillips Machine Screw - 4-40 Thread, 7/8" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772A114	||	2
|-													
|	15	||	91831A005	||	Nylon-Insert Locknut - 4-40 Thread Size, 1/4" Wide, 9/64" High	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91831a005/=11vss2j	||	10
|-													
|	16	||	Top_Bearing_Connect	||	Bearing Wall Bridge	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	17	||	Top_Mount	||	PCB Mount	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	18	||	91772A110	||	Pan Head Phillips Machine Screw - 4-40 Thread, 1/2" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772a110/=11vst2z	||	8
|-													
|	19	||	PCB_Lenoff	||	Assembled PCB	||	FR4 PCB	||	Custom Component	||	n/a	||	1
|-													
|	20	||	Tube	||	Exterior Tube	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	21	||	Top_Wings	||	Connection between Tube, PCB and Top Cover	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	22	||	Top_Cover	||	Top Cover to protect PCB	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	23	||	97975A115	||	Thread Forming Screw for Brittle Plastic - Pan Head, 4-24 Thread, 1/2" Length	||	410 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#97975a115/=11vstf4	||	4
|-													
|	24	||	91831A007	||	Nylon-Insert Locknut - 6-32 Thread Size, 5/16" Wide, 11/64" High	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91831a007/=11vstwk	||	4
|-													
|	25	||	Switch_Cover	||	Power Switch Cap	||	PLA Plastic	||	Custom Component	||	n/a	||	1
|-													
|	26	||	Battery	||	1000 mAh	||	Polymer Lithium Ion Battery	||	Sparkfun	||	https://www.sparkfun.com/products/339	||	1
|}													


<h2> FCC Notification </h2>
[[#toc|Back to Table of Contents]]

<h3>What is this section even for?</h3>
This section is a heads up to you, the users, and for our friends over at the FCC. The FCC has a monumental task of monitoring and managing a common resource that we all need, the electromagnetic spectrum. In order to make sure that everyone plays nicely in this area, a series of tests and certifications are necessary to ensure that our device won't negatively impact any other device. Below is some information pertinent to those tests as well as some guidelines if unexpected interference occurs.

&nbsp;
<h3>FCC Notification</h3>
Contains FCC ID: UYI25

This device complies with Part 15 of the FCC Rules. Operation is subject to the following two conditions"

(1) This device may not cause harmful interference and

(2) This device must accept any interference received, including interference that may cause undesired operation.

&nbsp;
<h3>More in-depth...</h3>
This equipment has been tested and found to comply with the limits for a class B digital device, pursuant to part 15 of the FCC Rules. These limits are designed to provide reasonable protection against harmful interference in a residential installation. This equipment generates, uses and can radiate radio frequency energy and if not installed and used in accordance with the instructions, may cause harmful interference to radio communications. However, there is no guarantee that interference will not occur in a particular installation. If this equipment does cause harmful interference to radio or television reception, which can be determined by turning the equipment off and on, the user is encouraged to try to correct the interference by one or more of the following measures:

&nbsp;

* Reorient or relocate the receiving antenna.

* Increase the separation between the equipment and receiver.

* Connect the equipment into an outlet on a circuit different from that to which the receiver is connected.

* Consult the dealer or an experienced radio/TV technician for help.

&nbsp;

In order to maintain compliance with FCC regulations, shielded cables must be used with this equipment. Operation with non-approved equipment or unshielded cables is likely to result in interference to radio and TV reception. The user is cautioned that changes and modifications made to the equipment without the approval of manufacturer could void the user's authority to operate this equipment.

<h2>EDIT OpenBarbell V2 Specs </h2>
[[#toc|Back to Table of Contents]]

OpenBarbell V2 is powered by a Nordic nRF51 series ultra low power SOC. This system is a combination of a 2.4 GHZ Bluetooth transceiver and a low power 32 bit ARM Cortex -M0 core. This package is mounted onto a board developed by RF Digital called the RFduino, which is Arduino compatible and FCC Module Certified for use in consumer electronics.

&nbsp;

MORE COMING SOON.

<h2> What we can do with Velocity Data </h2>
[[#toc|Back to Table of Contents]]

We're working hard on this - Come back soon!


<h1> OpenBarbell V1 </h1>

<p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/02/20160201_183650.jpg" width="960" height="540"></p>

<h2> What does the OpenBarbell Do? </h2>
[[#toc|Back to Table of Contents]]

OpenBarbell is a low barrier-to-entry Velocity Based Training device. It enables lifters to track the velocity of barbell (or otherwise) exercises to they can do velocity based autoregulation. This data has been used for decades by high level athletes and has yet to trickle down to the average lifter because of a perceived lack in demand. We disagree with that perspective and are dedicated to supplying athletes in strength sports with the same level of technology that athletes in other sports enjoy.

Each Rev 1 device measures average velocity that has been validated against the best technology in velocity tracking. It also has the ability to display peak velocity, but that data has not yet (at this date) been validated. It also measures the duration of each lift in seconds, the total range of motion of each lift, and the spot at which you achieve your peak velocity (in %). With successive firmware and software updates, OpenBarbell will earn more and more features that we will include in this live document.

<h2> Frequently Asked Questions </h2>
[[#toc|Back to Table of Contents]]

<h3>Basic Info</h3>
<blockquote>
<strong>How much does OpenBarbell cost?</strong>

We are trying our best to keep the price low enough to allow the amateur lifter to enjoy the benefits of Velocity Based Training. At the same time, we're balancing unit costs and the amount of time spent on our part designing and assembling small batches of these units. That being said, we are offering OpenBarbell for sale at $199, an order of magnitude less expensive than comparable devices.

<strong>When will OpenBarbell be released?</strong>

OpenBarbell will be released on our webstore on Sunday, February 21st at 8:00 PM Eastern! They will go fast, so we recommend you keep an eye on the OpenBarbell countdown here and on the home page.

<strong>Does my device have a warranty?</strong>

The Squats and Science OpenBarbell is unlike most consumer devices available for purchase. It was made by a couple engineers who were fed up with the lack of accessibility for advanced training tools and decided to solve the problem themselves. That meant making something that works quickly and at low cost. Although we would love to continue to support our devices as long as you own them, we will only be making these in small batches and therefore unable to replace parts, dedicate a service team or absorb the costs of return shipping. We will however support each and every device when it arrives on your doorstep, and if there are any issues you can ship it back to us to be repaired or we will give you a full refund.

OpenBarbell, like the name suggests, is also totally open source and Arduino compatible. Normal warranties prevent users from hacking their devices, but we encourage it. We do not wish to preclude you from modifying your device and we hope you have the ingenuity to create functionality that the community can take advantage of.

That being said, we do plan on helping our owners wherever we can. Any questions you have about your device can (or may already) be answered in the [http://squatsandscience.com/forums/forum/openbarbell-buildlog/owners/ Owners forum]. If the forum doesn't help and you're feeling frustrated you can also send an email to the dedicated account rep1support@squatsandscience.com. This service will never expire and as long as we have fingers (and money to pay for hosting) we will be replying to your forum posts.

<strong>What does OpenBarbell do?</strong>

Very simply, OpenBarbell measures the position and velocity of an object in one dimension. This capability allows a lifter to utilize VBT (Velocity Based Training) to autoregulate their exercise routine. Autoregulation is a fancy way of saying you use the most current information about how strong you are to determine what you do at the gym that day. This type of training has been shown to be incredibly effective at both executing long term training goals and planning maximum effort attempts in the same day.

<strong>How do you use OpenBarbell?</strong>

Coming soon!
</blockquote>
<h3>Technical Questions</h3>
<blockquote>
<strong>I'm getting funky battery readings, is that alright?</strong>

OpenBarbell is made primarily by two engineers. In order to get these devices out in a reasonable amount of time, we decided against doing in-house battery conditioning. What that means is your OpenBarbell needs to learn its battery over the course of the first few charge and discharge cycles. We highly recommend you charge it until full as soon as you get it, and let it discharge until 2-3% without letting it die. You'll notice it has much more consistent battery readings, and will appear to last much longer.

<strong>What are OpenBarbells dimensions?</strong>

80mm (width) x 90mm (height) - Approximately.

<strong>What's under the hood?</strong>

OpenBarbell is powered by a Nordic nRF51 series ultra low power SOC. This system is a combination of a 2.4 GHZ Bluetooth transceiver and a low power 32 bit ARM Cortex -M0 core. This package is mounted onto a board developed by RF Digital called the RFduino, which is Arduino compatible and FCC Module Certified for use in consumer electronics.

<strong>What are the maximum and minimum velocities?</strong>

The following are theoretical numbers from our experimentation. We will likely do further investigation and will post them here.

''Maximum'':

The maximum velocity can be answered in a few different ways. If you wanted to know what the fastest barbell lift is that it can track, the answer is ALL OF THEM! In our testing we haven't been able to approach a skipped reading or measurement with any barbell lift, no matter how strong our subject is an how light the weight is. We can be relatively sure of this because, our velocity code runs in what's called an 'interrupt', which checks the encoder at a rate close to the clock speed (16 MHz, or 16 million times per second). The bottle neck is how fast it can crunch the numbers after the interrupt occurs, and by comparing how many times we get in the interrupt vs. how many times we crunch the numbers, we can tell when reps are missed.

If you want to know how fast you can pull the string out of the device, first I would say please don't do anything you would regret, then I would say we have pulled the string as fast as 5.71 m/s average velocity and 12.62 m/s peak velocity. The fastest lifts I've ever seen are hovering around 2 m/s average velocity. The bottleneck would likely be the mounting point of the spring and the axle, so if you were to attach it to a bottle rocket or an SR-71 Blackbird that's where we're guessing it would fail first. We've tried and failed to do it with any of our humane means.

''Minimum'':

The minimum is a little more straightforward, although a bit mathematically involved. Let's pretend we're coaching the worlds smallest lifter. His bench ROM is incredibly short and he has been training for decades, carefully refining his technique becoming the worlds slowest lifter.

Our hardware calculates velocity approximately every 2.8 mm. Velocity being distance over time, the smallest possible distance you can travel would lead to the slowest possible velocity. Coincidentally, our tiniest lifter in the world has a bench ROM of 2.8 mm.

Our ARM Cortex M-0 processor has a time-based interrupt that is constantly counting upwards in microseconds (millionths of a second). Because of the limitations of a 32 bit unsigned long variable, the number rolls over every 70 minutes and starts counting from 0 again. Since the odds of you starting and ending a rep at that exact time are incredibly slim, we did not write code to fix that fringe case. That means the maximum time we can do one rep would be about 70 minutes. That happens to be the longest attempt our World's tiniest lifter has ever accomplished.

A little bit of math later and we've calculated that the tiniest lifter in the World has maxed out our device at an astonishing 0.0000006667 m/s. That is roughly the equivalent of traveling the distance of one wavelength of red light every second.

<strong>How accurate is OpenBarbell?</strong>

There are two metrics that are important when talking about the quality of data you get from OpenBarbell. Those are accuracy, and precision. Accuracy is how close our readings are to real-world velocities, which we discern from lab grade velocity measurement devices. Although accuracy is very important, we often get the argument that precision is even more valuable. A precise device would produce readings that are always consistent with each other, allowing you to compare lifts to those done in the past and future, which is vital for autoregulation.

OpenBarbell is both very precise and incredibly accurate. We have preliminary results from measurements made against the Tendo device, OptoTrak optical position sensing device, precision micrometers and super-high accuracy industrial encoders. Our readings show that we have the capability to reproduce real-world velocities very consistently, with R-values above 0.999 and accuracy hovering around 98-99%. Don't take our word for it. Dr. Mike Zourdos at Florida Atlantic University is currently conducting a validation study on the device with the results to be published later this year, or early next year. We will also publish official results of our own test soon as well.

<strong>How long does OpenBarbell last on a charge?</strong>

With our real-world testing, we are currently estimating that, using your device's energy economically, it can be trained with every day and last about a month. With a normal training schedule it could last even longer than that. The lifetime of the battery should be great as well, since that is dictated by number of charge cycles and there can be as little as 10 a year!

Please keep in mind, personal use can vary. If you tend to leave your device on between workouts you can kill the battery in a matter of days. If you turn it off between sets it will last much, much longer.

<strong>What's the maximum displacement?</strong>

The maximum string displacement is under 9 ft. In real world scenarios, that means a lifter about 6'6 can do an overhead press with a close grip and only have a few inches to spare. If you're very tall, tread with overhead work carefully in the beginning. If you're doing presses you can mount the device higher off the ground. If you're doing Olympic Lifting you can mount it on a few extra plates until it's just below the bar, and be careful not to run off the platform. If you have a habit of doing that, we will be developing a magnetic attachment that will release if pulled too far. Check our store for that in the future!

<strong>How much resistance does this add to the bar?</strong>

OpenBarbell adds up to 1/3 lb to the bar. That is when pulling hard at close to the extent of the string length. This is consistent with other draw-string based devices.

<strong>How does my device work?</strong>

Coming soon!

<strong>My device is acting weird while plugged in. Is it broken?</strong>

It's perfectly fine! OpenBarbell is chock full of peripherals so we needed to use pins for multiple purposes. Two pins that are grounded while the MicroUSB are plugged in are vital for the devices functionality.

We understand this may be inconvenient, but we've designed it to charge fast and last long, so hopefully it won't be so bad!
</blockquote>
<h3>Servicing and Repair</h3>
<blockquote>
<strong>What happens if a part breaks or malfunctions?</strong>

If your item breaks or is in need of a specific part, you have a couple of choices. OpenBarbell is totally open from head to toe so from day one you have the ability to modify, improve, or fix your own device. Search the forum or write a post and we will instruct you on the best course of action. If it turns out we have the ability to supply a spare part or can fix it ourselves, you can send the unit to us and we will fix it at no cost (but we cannot cover the shipping). Since the device is also totally open source, we hope others who may be more technically inclined can pitch in to help others in case of VBT emergencies.

<strong>What happens if my string breaks?</strong>

OpenBarbell is made with a very durable half millimeter Kevlar string. It has been tested for almost a year in these devices with very little signs of wear. That being said, we know somebody out there will put the string through the gauntlet so we installed a few fallback solutions.

A common area of wear for the string is at the top where it rubs on the bar. If you see it getting precariously thin, you can cut it off and tie the bar clip lower. There are a few extra turns of string on the spool, so you can unfurl a turn or so and you won't lose any string travel. There will be a tutorial for this soon!

If you need to restring the device, the entire center assembly comes off and you'll have access to the spool. A tutorial will be available for this as well.

<strong>Are my magnets supposed to spin in place?</strong>

Don't worry, nothing is wrong with your unit. In our effort to allow easy disassembly, we used screws at the bottom that do not have nylon locking nuts. They'll stay put, but over time they will move around by a fraction of a turn. This doesn't impact the units ability to maintain its magnetic attachment to a ferrous base object. We encourage owners NOT to tighten these bolts, as you can over-tighten them and cause the top part to break.

<strong>How resilient is OpenBarbell?</strong>

We hope you've noticed how sturdy OpenBarbell feels, but we hope you also know that this device is hand made by the Squats & Science team and isn't your ordinary consumer device. It was built to be kept in your gym bag and will last as long as you keep good care of it. Think of OpenBarbell as a fine hand made sports car.  It's beautiful, high performance and rock solid but you probably shouldn't go off-roading with it.

<strong>Why is my spindle wobbly, and is that OK?</strong>

We evaluated several manufacturing techniques for OpenBarbell. The laser cutter turned out to be our best bet for a high accuracy low cost device. The problem with laser cutters is the optics create a conical beam for cutting, not the super straight laser beam people imagine.

Laser beam cutting edge.
This causes the edge of some parts to be a little crooked, and moving parts to be a little wobbly. We evaluated this fact when deciding to use laser cutting for our manufacturing and it doesn't effect the accuracy or consistency of our device in any way. For more information about how our device works, see the "How does the device work" question.
</blockquote>
<h3>Hacking your device</h3>
<blockquote>
<strong>How do I hack my device?</strong>

<nowiki>** DISCLAIMER: WE DO NOT RECOMMEND YOU TAKE APART YOUR DEVICE **</nowiki>

We're glad you asked! OpenBarbell is Arduino compatible, has a totally open source design and a completely open source app (if it's not released, we're working on it!). That means there are a ton of ways you can tinker with your device! The best place to start is the [http://squatsandscience.com/wikibarbell/index.php?title=V0.25#Instructions V0.25 Instructions], which will show you how the meat of an OpenBarbell is made.

If you're looking to hack the firmware head over to the [https://github.com/RFduino/RFduino/blob/master/README.md RFduino Readme on GitHub] to get started. You can play with the velocity detection algorithm, send more robust velocity data to the app, display all kinds of information to the screen, program visual cues at certain points of the lift, create a visual metronome for tempo squats, the opportunities are endless!

If you're looking to hack the app, which is where we think the most exciting features can be implemented, check back here soon for more information as we are deep into development as we speak. If you think you can help the team we'd love to hear from you, send us an email at contact@squatsandscience.com.

<strong>Does this stuff void my warranty?</strong>

<nowiki>** DISCLAIMER: WE DO NOT RECOMMEND YOU TAKE APART YOUR DEVICE **</nowiki>

Remember, OpenBarbell doesn't have a standard warranty. It comes with very limited support (outlined above) and a 14 day return policy. That being said, I can split this answer into two sections.

<strong>Hardware:</strong>

If you decide to modify the hardware and break something, we will do our best to make you replacement parts (at close to cost) but we cannot guarantee you parts or fix your device for you for free. We build the device to last, but we can't compensate for your possible lack of DIY skills. If you NEED to hack the hardware or manufacture your own replacement parts, our housing and PCB CAD files are all available via our GitHub page.

<strong>Firmware & Electronics:</strong>

Again, we aren't sure how good your hobby electronics skills are, so we can't guarantee our board can make it through bouts with your soldering iron. Upgrading your battery, adding LED's, installing a buzzer are all things that we would not be able to support if it were to go wrong. The same goes for firmware, if you are clever enough you can probably find a way to burn out your PCB via firmware change. We will however support any upgrade to official Squats & Science firmware updates. If you verify that your issue was caused directly because of a firmware update we will do our best to correct the situation.

<strong>How do I update my firmware?</strong>

Updating firmware is a little involved, and not for the faint of heart. If you're familiar with Arduino and can navigate a breadboard it isn't too bad. It requires the following parts:



One OpenBarbell

[https://www.sparkfun.com/products/10031 One MicroUSB Breakout Board]

[http://www.rfduino.com/product/rfd22121-usb-shield-for-rfduino/ One RFduino USB Shield] (or other FTDI board)

[https://www.sparkfun.com/products/12002 One Breadboard]

[https://www.sparkfun.com/products/12794 Jumper Wires]


<ol>
<li>Follow the guide [https://github.com/RFduino/RFduino here] (scroll down) to both install the Arduino IDE (if you haven't already) and RFduino compatibility.</li>
<li>Grab the latest firmware from our [https://github.com/seminolemuscle/V1.0 GitHub].
<li>Download the [http://squatsandscience.com/wp-content/uploads/2015/07/OpenBarbell-Libraries-1.zip OpenBarbell required libraries] and paste them into your Arduino libraries folder.
<li>Put together your breadboard
<ol>
<li>Wire the MicroUSB breakout to the RFduino USB Shield in the following configuration (MicroUSB Breakout --> RFduino USB Shield) ([http://squatsandscience.com/wp-content/uploads/2015/07/RFduino-USB-Shield-schematic.png see the RFduino USB Shield schematic here])
<ol>
<li>D+ --> GPIO0</li>
<li>D- -->GPIO1</li>
<li>ID --> RESET</li>
<li>GND --> GND</li>
<li>VCC --> +3V</li>
</ol>
<li>Plug the RFduino MicroUSB Shield into your computer, go into the Arduino IDE and navigate to Tools --> Board and choose "RFduino", and select your COM port (you may need trial and error to pick the correct one).</li>
<li>Plug the MicroUSB Breakout into your OpenBarbell.</li>
</ol>
<li>Upload code!</li>
</ol>
</blockquote>

<h2> Getting Started </h2>
[[#toc|Back to Table of Contents]]

<h3>Whats in the box...</h3>
1. One official Squats &amp; Science OpenBarbell unit

<img src="http://squatsandscience.com/wp-content/uploads/2015/07/OpenBarbell_V1_Announce_dark.png" height="169" width="300"> 

<img src="" height="" width="X"> 

2. One MicroUSB cable for charging ONLY (you can pair it with your cellphone charger)

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_112948.jpg" height="169" width="300"> 


3. A thank you letter from us, including the unit number of your specific device.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_113506.jpg" height="169" width="300"> 

4. One lanyard for mounting onto the bar

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_112929.jpg" height="169" width="300"> 

5. The hopes and dreams of two guys who just want you to be a better you.
<h3>What next...</h3>
<ol>
	<li>Read our care instructions! It's imperative that you treat your OpenBarbell the way you'd like it to treat you. There's information about safe OpenBarbell placement during your workout, transporting your device, battery management, device maintenance, etc.</li>
	<li>Using your device:
<ul>
	<li>Using your device is simple. As you can see in the instruction card included with the device, all you need to do is turn it on, anchor it to a plate or rack, attach it to the bar, and lift!</li>
</ul>
</li>
</ol>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/final-final-instructions.png" height="418" width="512"> 

<h3>Begin Set...</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7487.jpg" height="203" width="300"> 

On the begin set screen, you can see the rep number you're on in the top left (it will always be Rep#: 1 on the Begin Set screen), the time since your last rep in the top middle, and the percentage of battery remaining in the top right. This is called the System Tray and will almost always be present for your device.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7488.jpg" height="195" width="300"> 

After you complete your first rep, you'll default to the Power Mode (more on that in a second). The power mode displays the System Tray at the top, Average Velocity for that rep nice an big in the center, Peak Velocity at the bottom left and Range of Motion of the rep on the bottom right. As you can see, the rest timer at the top center resets after each rep is performed.
<h3>Olympic Mode</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7492.jpg" height="175" width="300"> 

If you'd like to switch to a different data set more suited towards Olympic Weightlifting, press and hold one of the buttons for three seconds to switch over.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7490.jpg" height="176" width="300"> 

As you can see in this mode, Peak Velocity is displayed prominently in the center of the screen, with the duration of the lift at the bottom left, and the spot at which you achieved your peak velocity for that lift in the bottom right. You can switch from Power Mode to Olympic Mode by holding either button for three seconds, and it will display the same rep data during each mode, for a total of five metrics for each lift.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7493.jpg" height="177" width="300"> 

Holding down a button for three more seconds returns you to Power Mode.
<h3>Invert Mode</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7494.jpg" height="180" width="300"> 

Holding down both buttons for three seconds will send you into Invert Mode. Invert Mode is used if you would like to mount your device up-side down above your exercise implement. This essentially tells the device to pay attention to the opposite direction, since while inverted we care about the velocity coming <em>towards </em>the device, instead of away. <a href="http://squatsandscience.com/wikibarbell/openbarbell-wiki/openbarbell-v1-0/care-instructions/">PLEASE READ OUR CARE INSTRUCTIONS BEFORE USING YOUR DEVICE WHILE INVERTED</a>.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7496.jpg" height="171" width="300"> 

Invert mode displays the same data as non-inverted mode, but you can now accomplish reps with the device above you.

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7497.jpg" height="177" width="300"> 

Another three second hold turns off Invert Mode.
<h3>Deleting Past Set</h3>
<img src="http://squatsandscience.com/wp-content/uploads/2016/03/IMG_7489.jpg" height="181" width="300"> 

Tapping the right button until you reach the end of your set will display the 'Delete Past Set' screen. If you chose to tap the right button once more, you will remove all previous rep data from device memory. Tapping the left button will preserve your rep data.

<h2> Interacting with the Device </h2>
[[#toc|Back to Table of Contents]]

On the hardware side, OpenBarbell has two input buttons that you can use to toggle between reps, reset rep memory, wake the screen, switch between Power Mode and Olympic Mode, and invert the device. It also has a power switch for (obviously) turning on and off power supply, a MicroUSB port for charging and uploading firmware, an OLED display for displaying device functionality to the user, and a string/string hook for measuring barbell velocity.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/Input.png" height="576" width="1024"> 


&nbsp;

See screen shots of the UI in the [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Getting_Started Getting Started] section.

&nbsp;

<h2> Interpreting the LEDs </h2>
[[#toc|Back to Table of Contents]]

At rest, the green LED indicates the device is on, will blink every 2 seconds to catch your attention if it is inadvertently left on. The purpose of this LED can be modified by playing with our Arduino Code - https://github.com/seminolemuscle/V0.24 - for whatever you'd like.


<img src="http://squatsandscience.com/wp-content/uploads/2016/04/Me0Bnbu-Imgur.gif"> 


The red LED indicates the battery is being charged. When the LED turns off that means your battery is fully charged. If the LED is showing a less bright red than usual, don't worry. That's a bug with the LiPo battery charging chip and can usually be fixed by unplugging your device and plugging it back in. The red LED cannot be changed via firmware as it is connected directly to the LiPo charging chip and not the RFduino microcontroller.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/03/20160303_103906.jpg" height="401" width="712"> 


<h2> Battery Life and Charging </h2>
[[#toc|Back to Table of Contents]]

The Squats and Science OpenBarbell is equipped with a 1000 mAh battery. Let's put that in perspective.

&nbsp;

FitBit Flex: 50 mAh

iPod Nano: 220 mAh

Moto 360 Smartwatch: 300 mAh

iPhone 6S: 1715 mAh

&nbsp;

We wanted to make sure you didn't have to worry about charging another device every day. In preliminary testing we've operated the OpenBarbell for the equivalent of weeks of training sessions, theoretically much more if battery is conserved by shutting the device off between sets. With a standard phone charger, the device can charge from nearly empty to 40%+ in minutes, and can charge completely within about two hours. We are currently testing our battery capacity in terms of actual reps completed and will publish our findings here when they're available.

&nbsp;

<strong>Battery Study Findings:</strong>

The following are results we've found when using a device that has had the battery conditioned (charged and discharged) several times, giving us more consistent results. Each test has been a traditional workout session consisting of about 50-60 total reps over the course of 1.5-2 hours, without a Bluetooth connection and keeping the device on between sets. The results vary depending on the current state of battery charge.

&nbsp;

BATTERY LEVEL/BATTERY DRAIN

93%/10%

86%/11%

54%/6%

31%/2%

13%/7%

&nbsp;

As you can see, there is a general trend where the lower the current battery level is at the beginning of the workout, the longer it seems to last. We're estimating on average a lifter can get 10 uses per month if used in the conditions stated above.

&nbsp;

<strong>Battery Care</strong>

Battery care is essential for any consumer electronics device. We recommend you let your battery experience nearly a full range of its capacity every charging cycle. Let it discharge down to less than 5% and charge it until it is full, rinse and repeat. Try very hard not to let your battery die, as it can impact longevity and the function of its internal circuitry. You can feel free to use your cellphone charger for this device, and we have tested it with chargers that go up to 2.0A supply current (it will charge faster with chargers that have greater supply current).

&nbsp;

If your battery is giving you fluctuating readings, or rapidly reducing after it is unplugged do not worry. The batter fuel gauge chip has a learning period until it figures out your batteries habits, and it can sometimes be tricked by different chargers. It seems there is about a 3 charge cycle learning period until you can get consistent, predictable readings. Even then, there may be sudden drops in readings or it may not drop much at all during the same usage period.

&nbsp;

We've added a blinking LED light to indicate when the device is left on. If you see this blinking light and you intend for your device to be off, it is an indication that you should turn off your device. Although OpenBarbell lasts quite a while, it can discharge a significant amount overnight as it consumes most of its current at rest.

&nbsp;

<h2> Care Instructions </h2>
[[#toc|Back to Table of Contents]]

It's imperative that you care dearly for your brand new Squats &amp; Science OpenBarbell. Your new velocity measuring device is not indestructible, in fact there are several ways you can destroy your brand new strength tool during your workout. Here's our attempt at a comprehensive list of ways you can do just that.

<strong>Dropping weight on your device</strong>

It's very possible to drop a barbell or other implement on your OpenBarbell since it can be located directly below your exercise equipment of choice. OpenBarbell was not designed to live through this event and will surely break into quite a few pieces if this were to happen. To avoid this tragic occurrence, try to place OpenBarbell in a spot under your implement that is not in immediate crushing danger. For a barbell, do not place the unit below the weights themselves, rather to the side where there will be clearance in the case where it is dropped. Please also make sure to keep the device as close to the same position every time you use it, preferably with the string completely vertical (but not directly under the weights!).

&nbsp;
<h3><strong>Crushing the string hook/cutting the kevlar string</strong></h3>
In our tests we were able to both break the nylon string hook as well as cut the kevlar string by pinching it between sharp knurling and a metal rack hook. To ameliorate this occurrence, [https://www.domainracer.com/cheap-web-hosting.php best cheap web hosting] we shipped each unit with a fabric lanyard that can be looped around the bar and hooked onto the device. This way, the string can still be mounted inside the barbell collar for barbell exercise so it does not need to be repeatedly removed between weight changes. If you do not like this mounting configuration and would rather mount it directly onto the bar without the lanyard, we recommend you do so outside of the weights to reduce the chance of wear and tear due to knurling and contact between the bar and rack.
<h3><strong>Transporting OpenBarbell</strong></h3>
OpenBarbell is meant to live in your gym bag, but it isn't a pair of squat shoes or wrist wraps. It should be kept away from heavy items like metal belt clips or wooden shoe soles, and should not be dropped onto the ground from any height without cushioning. A simple solution would be to put it in a side pocket of the gym bag that does not extend to the bottom of the bag, keep it in a dedicated draw string bag inside your gym bag, keep it inside a (dry) knee sleeve, or even toss it in a dedicated sock or coozie.
<h3><strong>Battery maintenance</strong></h3>
Make sure to see our [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Battery_Life_and_Charging Battery Life and Charging] section of the user manual. To summarize, we recommend not using a MicroUSB charger above 2.0 A supply current. We also do not recommend fully discharging your device, or leaving it on the charger for very elongated periods of time. To condition your battery, make sure to fully charge your device each time and discharge down to about 5% before recharging. Keep OpenBarbell away from temperatures above 110 degrees F or below 32 degrees F for extended periods of time.
<h3><strong>Assembly/Disassembly</strong></h3>
OpenBarbell was designed to be fully serviceable. We understand parts in the device might need care every once in a while, but we cannot guarantee that skills of our customers in assembling and disassembling their device. That is why we cannot support any problems that occur due to our customers fixing their device themselves. Any issues found upon receipt of the device can be fixed by us for free within 14 days of the product arriving at your doorstep. If any disassembly is required after that, please contact us and we will work out an amicable solution to your repair needs.
<h3><strong>Safe magnetic mounting of OpenBarbell</strong></h3>
It is possible to damage OpenBarbell if it is carelessly mounted onto a hard ferromagnetic surface (a metal plate or rack). We recommend gently placing the device down to reduce the odds of a stress fracture in the acrylic housing.

If mounting the device in invert mode, it is very important to make sure it has a very secure mounting spot for all four magnets, and that it is not being pulled by the string at an odd angle as to introduce a lateral force that can remove one side of the device from its mounting position. Unless that is achievable, we do not recommend inverting your device.
<h3><strong>Caring for the Housing</strong></h3>
The exterior and many of the internal parts of the device are made from a cast Acrylic - also known as Plexiglass, Lucite and Acylite. With proper care this device should be able to last for years to come, [https://www.domainracer.com/reseller-hosting.php unlimited reseller hosting] however acrylic is susceptible to scratches and abrasions as well as damage from some chemicals.

Most of the superficial dirt and grime that the OpenBarbell will pick up can be wiped away with a mild solution of soap, water and a rag. This device is by no means water-proof but will withstand a very lightly damp rag (just stay away from the buttons, usb, and switch!). If you want to do some heavier cleaning then we have to take some precautions. The best way to clean cast Acrylic is with products specifically designed for cleaning cast Acrylic such as Novus No. 1 or Brillianize. <strong>It is important to NEVER use cleaning solutions with Ammonia (such as Windex or Formula 409), gasoline, denatured alcohol (paint thinner), carbon tetrachloride, or acetone!</strong> All of these product will cause the Acrylic to Craze with minute cracks.

<h2> Loading Code </h2>
[[#toc|Back to Table of Contents]]

The purpose of this brief tutorial is to demonstrate how to upload code to an OpenBarbell unit made at home, or modified by an owner. Before we begin, please read our [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Warranty Warranty]

&nbsp;

To load code on your device you need a few things:
<ol>
	<li>Female to male USB cord</li>
	<li>[http://www.rfduino.com/product/rfd22121-usb-shield-for-rfduino/ RFduino USB Breakout Board] ([http://forum.rfduino.com/index.php?topic=75.0  or another FTDI Breakout Board]</li>
	<li>[https://www.sparkfun.com/products/10031 MicroUSB Breakout Board] (or you can find one online that requires no soldering)</li>
	<li>Breadboard</li>
	<li>Female to male breadboard jumper wires</li>
</ol>
&nbsp;

Essentially what we're doing is connecting the RFduino on your device to an FTDI breakout board. We routed the appropriate pins to the spare microUSB pins on the board for easy access, but don’t go plugging it into your computer. We need to get those pins hooked up to your FTDI board to convert it to a language your computer can understand. You need 5 pins to program an RFduino, GND, VCC, TX, RX, and RESET. TX and RX are hooked up to pins GPIO0/1 so they are routed to USB pins D+ and D-. The most convenient way to access these pins is to split a USB cord, but most USB cords do not utilize the ID pin and therefore do not have a 5th wire. If you do not have a 5 pin microUSB cable, you need a microUSB breakout board to have access to these pins. See the schematic below for reference.

&nbsp;

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/GPIO_to_USB2.png" height="632" width="476"> 

VUSB above is the vertical USB port on the top of OpenBarbell. This will match with the labeled pins on the microUSB breakout board. Those pins need to be routed to the same pins on the RFduino USB Shield.

&nbsp;

Once that is set up, you should head over to the [https://github.com/RFduino/RFduino Getting Started page of the Rfduino Github]. That will walk you through downloading and setting up an RFduino compatible version of the Arduino IDE. You can run a default RFduino example to blink the OpenBarbell LED on pin 2. If you can get that to work, you're ready to download our code and libraries. Several of them are slightly modified to fit our exact needs, or to fix a few issues we found along the way. [http://squatsandscience.com/wp-content/uploads/2016/03/OpenBarbell-Libraries-Modified.zip You can find the modified libraries here]. Place them alongside your other Arduino libraries in your installation folder.

&nbsp;

Last but not least, grab our firmware off of GitHub and upload it onto your device. [https://github.com/seminolemuscle/V1.0/blob/BlueToothFloatingPt/Arduino%20Code/OpenBarbellV1.0/OpenBarbellV1.0.ino Our latest revision can be found here].

&nbsp;

We'll be writing a more detailed calibration method in the near future, but for now the following should suffice. If you're re-loading firmware onto a device you purchased, contact us for your tic length, we will give you a very accurate number you can use in your code for your specific device.

&nbsp;
<ol>
	<li>Place a caliper above your device (MINIMUM 12 inch caliper, the longer it is the more accurate your calibration will be) and have the string follow the caliper precisely. Do this several times around the maximum caliper displacement and record the ROM from the device, and the displacement from the caliper.</li>
	<li>We set the default tic length (string displacement between encoder readings) at 2.667 mm. Take each ROM you recorded and divide it by the tic length, then round to the nearest whole number. This represents the number of encoder readings.</li>
	<li>Next, divide each caliper displacement by the corresponding number of encoder readings. This will give you a new tic length. Average each of your recorded tic lengths (since you did the measurement several times) and this will be your new ticLength variable on line 56 of our code.</li>
	<li></li>
</ol>
That's it! Go lift some weights, and make sure to sign up for [http://squatsandscience.com/velocity_tracking/ Squats &amp; Science Velocity Tracking] so we can help you optimize your training!

<h2>Bluetooth Communication</h2>
[[#toc|Back to Table of Contents]]

What really unlocks some great potential with the OpenBarbell is the ability to take the information off the unit for use online or in an app and to set configurable values. In order to accomplish this the device utilizes BLE (Bluetooth Low Energy) to talk with a paired phone.

&nbsp;

<hr />

&nbsp;
<h3>(OpenBarbell --&gt; Phone)</h3>
By default the device will transmit limited information to a paired phone at the end of a rep. All of the information calculated on the device will be sent but the raw times between the encoder ticks will be compressed. The limitation imposed on this transmission is the amount of time necessary to send the requested data and the battery drain resulting from continuously broadcasting via bluetooth. In order to ensure we do not miss a rep and/or to ensure that we are not transmitting at the start of a rep we have kept default transmissions to a minimum.

The following is a breakdown of how the data is transmitted to the phone in the order that the phone receives it
<h4>-1234</h4>
<blockquote>This is a unique number sequence that will signify to the app (and to the person looking at the data) that the rep has begun. Data transmission is then held until the rep is complete.</blockquote>
<h4>Rep #</h4>
<blockquote>Once the rep is complete there will be a string of data coming to the phone. The first piece of data coming is the "Rep #" - this number corresponds to the "Rep #" displayed on the unit.</blockquote>
<h4>Avg Velocity</h4>
<blockquote>This is the average velocity during the rep as calculated on the device.</blockquote>
<h4>ROM (Range of Motion)</h4>
<blockquote>This is the distance traveled, in mm, through the rep</blockquote>
<h4>Peak Velocity</h4>
<blockquote>This is the peak instantaneous velocity during the rep as calculated on the device.</blockquote>
<h4>Peak Velocity Location</h4>
<blockquote>This is the location, expressed as a percentage, at which the peak velocity occurred. For example, if the peak velocity location was "63%" with a ROM of "1000 mm" then the peak velocity location occurred at 63% of 1000 mm or 630 mm into the rep.</blockquote>
<h4>-9999 (Start compression data)</h4>
<blockquote>This is a unique number sequence to signify that the "Compression Data" transmission will now begin</blockquote>
<h4># of ticks counted</h4>
<blockquote>As discussed above, by default, only a sample of the total lift will be sent over to the phone to conserve transmission time and battery life. The "# of ticks counted" corresponds to the frequency at which we log the data to be sent.

For example, if this said "5" then that would mean every 5th tick of the encoder we would save the value - as in...

<span style="color: #ff6600;">Tick #1 - Not Saved, Tick #2 - Not Saved, Tick #3 - Not Saved, Tick #4 - Not Saved,</span> <span style="color: #99cc00;">Tick #5 - Saved,</span>  <span style="color: #ff6600;">Tick #6 - Not Saved, Tick #7 - Not Saved, Tick #8 - Not Saved, Tick #9 - Not Saved,</span> <span style="color: #99cc00;">Tick #10 - Saved, <span style="color: #ff6600;">Tick #11 - Not Saved, Tick #12 - Not Saved, Tick #13 - Not Saved, Tick #14 - Not Saved,</span> <span style="color: #99cc00;">Tick #15 - Saved,</span></span> <span style="color: #99cc00;"><span style="color: #ff6600;">Tick #16 - Not Saved, Tick #17 - Not Saved, Tick #18 - Not Saved, Tick #19 - Not Saved,</span> Tick #20 - Saved, </span>etc....

Then when the values are sent over they are sent in order that they were saved. So for the above example of "5 ticks" the string of compressed data would be .... Tick #5, Tick #10, Tick #15, Tick #20, Tick #25, etc...

In order to the get the compression ratio, divide one by the "# of ticks counted". So, continuing with our above example of 5, the compression ratio would be 1/"# of ticks counted" or 1/5 ticks would be counted or a net result in 20% of the available data being sent.</blockquote>

<h4>Precision of Compressed Values</h4>
<blockquote>Another way we compress the data being sent is to utilize all the available size in the data types being sent to the device.

For example,  say we wanted to send two DTs worth of information to the device. DT1 has a value of "100 ms" while DT2 has a value of "140 ms". We could send the first DT, DT1, followed by the second DT, DT2 - that would look something like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">DT1</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2: <span style="color: #ff6600;">DT2</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
This would be fine and it would work for such a short string but when we start having to send over many hundreds of values it can really slow things down. We can save on transmission time by compressing both DTs into one message...here's the underlying principle...

The data type that BLE uses to send its data is called a Floating Point Number - [https://en.wikipedia.org/wiki/Single-precision_floating-point_format Here's a good write up on Floating Point Numbers from Wikipedia]. In it's simplest embodiment, the floating point number can represent a value with 8 locations for digits where we can choose to put the decimal place wherever we would like within/outside those 8 locations. See the picture below for an explanation...

&nbsp;

<p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2016/03/FloatingPointExplanation-1.png" height="596" width="600"></p>


As you can see above, this data type can be used to represent very large numbers (1,075,270) as well as very small numbers (.34375). However, we should also notice that regardless of the value of the number (i.e. 100 or 1,075,270), all 8 positions of the data type will be utilized regardless if there is meaningful information in those positions. One way to think about this is by placing leading zeros in front of the values. For example, 100 is represented as 00000100 and 1,075,270 is represented as 01,075,270. Thus, a value of 100 and 1,075,270 have the same size in terms of the amount of data being sent over bluetooth. So this brings us to how we might utilize this information to compress the data via bluetooth.

If we go back to our original example of DT1 and DT2 (100 ms and 140 ms, respectively) now we know that it will actually look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">00000100</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2: <span style="color: #ff6600;">00000140</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
Let's combine both of those numbers into one number by dividing the second number by 10,000 (to shift the decimal places over 4 values) and add it to the first. Now we'll have DT1+DT2/10,000 = 100 + 140/10,000 = 100 + .0140 = 100.0140. And voila, we've turned two numbers into one number and we can easily separate them as well. Let's see what his new transmission might look like...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0100.0140</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
Just for one more example, lets compress the following string of numbers and send them over... 123, 52, 5124, 62, 462, 688, 123, 2, 4123,6252 ... if we apply the same compression above to these values then we would get the following message...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0123.0052</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">5124.0062</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 3: <span style="color: #ff6600;">0462.0688</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 4 : <span style="color: #ff6600;">0123.0002</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 5: <span style="color: #ff6600;">4123.6252</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
FANTASTIC! We did it, right?! Yeah, of course we did! So we've been talking a lot about "compression" but we still haven't touched on what the "Precision of Compressed Values" is...for that we have to did just a little bit deeper to understand.

One of the main things measured on the device is the amount of time in microseconds between "ticks" of the encoder. Yeah, microseconds, as in there are 1 million of them per second. As you can imagine that number gets very large very fast - this number can actually get up to 4,294,967,296 which is ~4.3 trillion microseconds or about ~4,294 seconds or ~72 minutes.

For a realistic scenario, let's say the average speed of a 1 meter ROM lift is .75 m/s. Some simple math tells us that the time of the lift is about 1.33 seconds [(1 meter)/(.75 meter/second)=~1.33 seconds]. We can do some more math to calculate how many ticks occurred during that lift since we know there are roughly 2.667 mm/tick to figure out there was roughly 374 ticks [1 meter = 1000 mm --&gt; (1000 mm)/(2.667 mm/tick)= ~374 ticks]. If we take the amount of time for the lift, 1.33 seconds, and divide by the number of ticks, 374, we will get to an average length of time between the ticks of, (1.33 seconds)/(374 ticks)=.00355615 seconds/tick or (if we multiply by 1,000,000 microseconds/second) about ~3556 microseconds/tick. Now that we know the average dt between ticks lets pick some numbers around that average for a sample transmission - Let's say 3550, 4267, 3000, 3687

If we apply the above compression the data transmission would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">3550.4267</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">3000.3687</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
This all seems great until we consider what might happen for a lift with an average velocity of .25 m/s with a 1 meter ROM. If we do the same math as above we find  (1 meter)/(.25 meter/second)=4 seconds --&gt; (4 seconds)/(374 ticks)= ~.01069519 seconds/tick or roughly 10,695 microseconds/tick. Now let's pick some numbers around this average time - Let's say 11,212, 10501, 9,632, 10729. However, there's a problem. Now that we have 5 digit numbers, we wouldn't be able to fit it into the above compression method as there are only 8 placeholders for digits and two 5 digit numbers would require 10 placeholders. What to do? Well, we can finally get to the whole purpose of this section,  the "precision of the compressed value".

While these 10 digits of precision are necessary for the device to do its job correctly (as in the number of digits in 4,294,967,296), we may be perfectly fine in shaving the last digit of precision - as in the difference to us of 525,967,283 microseconds vs 525,967,280 microseconds is not very much - we're literally talking about a rounding error there of 3 microseconds or .000003 seconds. For this reason the device will, by default, divide all of the DTs (time between ticks) by "10" (the default "precision of the compressed value") before sending them over. So if we take the above example numbers for the .25 m/s lift - 11212, 10501, 9632, 10727 -and divide them by 10 (and round to the nearest integer) we get values that we can fit into our compression scheme - 1121, 1050, 963, 1073 - Thus the transmission for the .25 m/s lift would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">1121.1050</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">0963.1073</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
If we now apply this principle of "precision of the compressed value" to the .75 m/s lift we see that it would actually be sent over like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">0355.0427</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">0300.0369</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
So what's the trade off here? In order to, by default, allow some of the slowest lifts to fit into the compression method we have to round the last digit of the time. This means that for very fast lifts, with very small DTs, we lose some precision. But the good thing is that if you want that last digit of precision, you can have it, just set the "precision of the compressed value" to 1 and the full microsecond number will come over. In any scenario there exists the possibility of generating a number with over 4 digits, even after you apply the "precision of the compressed value" divider - in that case the number is sent over by itself.

So, for one final example - if we want to send the following values... 1963, 1938, 19381, 39103, 739173, 9381, 1912...the transmission would look like this...
<p style="text-align: center;"><strong><span style="color: #99cc00;">***START TRANSMISSION***</span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 1 : <span style="color: #ff6600;">1963.1938</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 2 : <span style="color: #ff6600;">00019381</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 3 : <span style="color: #ff6600;">0039103</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 4 : <span style="color: #ff6600;">00739173</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #ffcc00;">MESSAGE 5 : <span style="color: #ff6600;">9381.1912</span></span></strong></p>
<p style="text-align: center;"><strong><span style="color: #99cc00;">***END TRANSMISSION***</span></strong></p>
</blockquote>
<h4>-<span class="match">9876</span></h4>
<blockquote>This is a unique number sequence to signify that the "Compressed Bulk Data" transmission will now begin</blockquote>
<h4>**"COMPRESSED" BULK DATA**</h4>
<blockquote>This is the compressed bulk data - this will be a snapshot of some or all of the DTs between ticks - see [http://squatsandscience.com/wikibarbell/index.php?title=V1.0#Precision_of_Compressed_Values Precision of Compressed Values] for more details. Although this is written as "11." this section could be anywhere from 1 message long to hundreds if not 1000+ messages depending on the settings of the user.</blockquote>
<h4>-6789</h4>
<blockquote>This is a unique number sequence to signify that the "Compressed Bulk Data" transmission has completed</blockquote>
<h4>Battery charge</h4>
<blockquote>This will send the battery charge of the device to the phone to keep tabs on the device.</blockquote>

<hr />

<h3>(Phone --&gt; OpenBarbell)</h3>
<span style="color: #ff0000;">Note - All transmissions to the OpenBarbell must be done in HEX format - since we don't normally think in base16 here's a helpful site to convert DECIMAL notation (base10 - what you would interact with on a daily basis) into the proper format (HEX) to send http://www.binaryhexconverter.com/decimal-to-hex-converter

<hr />

<h4>Minimum Rep Threshold (01 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">01</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = The "minimum rep threshold", in mm, in HEX notation</span>

<span style="color: #008000;">Explanation: </span>The minimum rep threshold is the minimum distance, in mm, that will be counted as a valid ROM.

<span style="color: #ff6600;">Range:</span> <span style="color: #800080;">XX</span> can range from 00 (0 mm) to FF (255 mm)

<span style="color: #ff00ff;">Default Value:</span> 150 mm

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "0 mm" which will count any ROM as a valid rep as any rep will have a ROM greater than 0 mm</li>
</ul>
</li>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">64</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; 100 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "100 mm" which will not allow any rep with a ROM less than 100 mm to be counted as a valid rep</li>
</ul>
</li>
	<li><span style="color: #ff0000;">01</span> <span style="color: #993366;">C8</span> =&gt;<span style="color: #ff0000;"> (Minimum Rep Threshold)</span> <span style="color: #800080;">(C8 in Hex = 200 in Decimal ==&gt; 200 mm)</span>
<ul>
	<li>In this example we have set the Minimum Rep Threshold to "200 mm" which will not allow any rep with a ROM less than 200 mm to be counted as a valid rep</li>
</ul>
</li>
</ul>

<hr />

<h4>Power/Olympic Mode Select (02 XX)</h4>
<span style="color: #993300;">Interaction: </span> <span style="color: #ff0000;">02</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = "Mode Select" in HEX notation</span>

<span style="color: #008000;">Explanation: </span>Use this function to switch between Power Mode and Olympic Mode. In order to switch between the two modes the full range of 00 to FF is divided into two sections.

<span style="color: #993300;"><span style="color: #ff6600;">Range:</span></span>
<blockquote>Power Mode - <span style="color: #800080;">XX</span> can range from 00 (0) to 09 (9)

Olympic Mode - <span style="color: #800080;">XX</span> can range from 0A (10) to FF (255)</blockquote>
<span style="color: #ff00ff;">Default Value:</span> n/a

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Power/Olympic Mode Select)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; Power Mode)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC) which falls in the range of 0-9, thus we have selected Power Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">07</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(07 in Hex = 7 in Decimal ==&gt; Power Mode)</span>
<ul>
	<li>In this example we sent over a value of 07 (HEX) or 7 (DEC) which falls in the range of 0-9, thus we have selected Power Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">0A</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; Olympic Mode)</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC) which falls in the range of 10-255, thus we have selected Olympic Mode</li>
</ul>
</li>
	<li><span style="color: #ff0000;">02</span> <span style="color: #993366;">AC</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Power/Olympic Mode Select)</span> <span style="color: #800080;">(AC in Hex = 172 in Decimal ==&gt; Olympic Mode)</span>
<ul>
	<li>In this example we sent over a value of AC (HEX) or 172 (DEC) which falls in the range of 10-255, thus we have selected Olympic Mode</li>
</ul>
</li>
</ul>

<hr />

<h4>Low Pass Filter Frequency (04 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">04</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = Low Pass "Filter Frequency", in hertz, in HEX notation</span>

<span style="color: #008000;">Explanation: </span>In order to work with some of the mechanical properties of the device it is necessary to apply a low pass filter for accurate peak velocity values. Read more about this filter here: http://playground.arduino.cc/Code/Filters

<span style="color: #ff6600;">Range:</span> <span style="color: #800080;">XX</span> can range from 00 (0 hz) to FF (255 hz)

<span style="color: #ff00ff;">Default Value:</span> 10 hz

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Low Pass Filter Frequency)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 hz)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC), this will set the filter frequency to 0 hz</li>
</ul>
</li>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">0A</span> =&gt;<span style="color: #ff0000;"> </span><span style="color: #ff0000;">(Low Pass Filter Frequency)</span> <span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; 10 hz (default value))</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC), this will set the filter frequency to 10 hz (the default value)</li>
</ul>
</li>
	<li><span style="color: #ff0000;">04</span> <span style="color: #993366;">AC</span> =&gt; <span style="color: #ff0000;">(Low Pass Filter Frequency)</span> <span style="color: #800080;">(AC in Hex = 172 in Decimal ==&gt; 172 hz)</span>
<ul>
	<li>In this example we sent over a value of AC (HEX) or 172 (DEC), this will set the filter frequency to 172 hz</li>
</ul>
</li>
</ul>

<hr />

<h4>Compressed Transmission Settings (08 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">08</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = is a value in HEX notation that can either change the precision of the compressed values or the compression ratio
</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">In order to compress the data coming from the OpenBarbell there are two compression schemes. The first is to send only a certain ratio of the collected data (as in one out of every 5 or one out of every 10 pieces of data collected) while the second is round the values to one decimal place and remove the trailing zero (as in "12237" rounds to "12240" and is sent over as "1224"... this reduces the overall size of the data being sent over). When setting the RATIO the value sent is put over 1 (as in the ratio becomes 1/XX). When setting the PRECISION there are only two settings - rounding or full precision. Sending <span style="color: #ff0000;">08</span> <span style="color: #993366;">FE</span> will allow the rounding of the sent values to 1 decimal place while sending <span style="color: #008000;"><span style="color: #000000;"><span style="color: #ff0000;">08</span> <span style="color: #993366;">FF</span></span></span> will force full precision values to be sent. See the section above entitled [[Precision of Compressed Values]] for more detail.

<span style="color: #ff6600;">Range: </span>

<span style="color: #800080;">XX</span> can range from 01 (1) to FD (253) to change the <strong>RATIO OF SENT VALUES</strong>

<span style="color: #800080;">XX</span> can either be FE (254) or FF (255) to change the <strong>PRECISION OF THE VALUES</strong>

<span style="color: #ff00ff;">Default Value:</span>

<strong>RATIO</strong> of sent values: <strong>5</strong> (This results in 1/5 of the values collected being sent)

<strong>PRECISION</strong> of sent values: <strong>FE</strong> (Rounded)

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">01</span> =&gt;<span style="color: #ff0000;"> (Compressed Transmission Setting) </span><span style="color: #800080;">(01 in Hex = 1 in Decimal ==&gt; Ratio of 1/1)</span>
<ul>
	<li>In this example we sent over a value of 01 (HEX) or 1 (DEC). Because 1 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 1 in this case will make the ratio 1/<strong>1</strong>, or will force all values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">05</span> =&gt; <span style="color: #800080;"><span style="color: #ff0000;">(Compressed Transmission Setting) </span>(05 in Hex = 5 in Decimal ==&gt; Ratio of 1/5 (default value))</span>
<ul>
	<li>In this example we sent over a value of 05 (HEX) or 5 (DEC). Because 5 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 5 in this case will make the ratio 1/<strong>5</strong>, or will only allow one out of every <strong>five</strong> values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; Ratio of 1/100)</span>
<ul>
	<li>In this example we sent over a value of 64 (HEX) or 100 (DEC). Because 100 (DEC) is in the range of 1 to 253, this value will adjust the <strong>RATIO</strong> of sent values. A value of 100 in this case will make the ratio 1/<strong>100</strong>, or will only allow one out of every <strong>hundred</strong> values to be sent via Bluetooth.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">FE</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(FE in Hex = 254 in Decimal ==&gt; Rounded Values)</span>
<ul>
	<li>In this example we sent over a value of FE (HEX) or 254 (DEC). Because 254 (DEC) is in the range of 254 to 255, this value will adjust the <strong>PRECISION</strong> of sent values. A value of 254 in this case will send over the default precision where the values will be rounded to the tens place and the trailing zero removed.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">08</span> <span style="color: #993366;">FF</span> =&gt; <span style="color: #ff0000;">(Compressed Transmission Setting) </span><span style="color: #800080;">(FF in Hex = 255 in Decimal ==&gt; Full Precision)</span>
<ul>
	<li>In this example we sent over a value of FF (HEX) or 255 (DEC). Because 255 (DEC) is in the range of 254 to 255, this value will adjust the <strong>PRECISION</strong> of sent values. A value of 255 in this case will send over the full precision of the collected values with no rounding.</li>
</ul>
</li>
</ul>

<hr />

<h4> OLED Back Light Timeout (10 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">10</span> <span style="color: #800080;">XX</span> where <span style="color: #800080;">XX = "OLED Back Light Timeout", in seconds, in HEX notation</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">The OLED screen on the device is back lit to aid in viewing the display. This adjustment allows one to modify the time that the screen stays on before timing out. </span></span>

<span style="color: #ff6600;">Range: </span><span style="color: #800080;">XX</span> can range from 00 (0 seconds) to FF (255 seconds)

<span style="color: #ff00ff;">Default Value:</span> 10 seconds

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (OLED Back Light Timeout)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal ==&gt; 0 Seconds)</span>
<ul>
	<li>In this example we sent over a value of 00 (HEX) or 0 (DEC), this will set the back light timer to 0 seconds which will effectively mean that they screen no longer turns on - This may be helpful to conserve battery life when Bluetooth is being used.</li>
</ul>
</li>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(</span><span style="color: #ff0000;">OLED Back Light Timeout) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal ==&gt; 10 Seconds (default value))</span>
<ul>
	<li>In this example we sent over a value of 0A (HEX) or 10 (DEC), this will set the back light timer to 10 seconds (the default value)</li>
</ul>
</li>
	<li><span style="color: #ff0000;">10</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(</span><span style="color: #ff0000;">OLED Back Light Timeout)</span> <span style="color: #800080;">(64 in Hex = 100 in Decimal ==&gt; 100 Seconds)</span>
<ul>
	<li>In this example we sent over a value of 64 (HEX) or 100 (DEC), this will set the back light timer to 100 seconds (or 1 minute and 40 seconds)</li>
</ul>
</li>
</ul>

<hr />

<h4> Status Check (40 XX)</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">40</span> <span style="color: #800080;">XX</span>

<span style="color: #008000;">Explanation: <span style="color: #000000;">Regardless of the value of XX, this will initiate a status check that can be called at any time to check several important values including a verification of set values from some of the other commands from the phone to the OpenBarbell. The readout from this status check should read as follows:</span></span>
<blockquote>
<ol>
	<li>Ratio of Values Sent</li>
	<li>Precision of Values Sent</li>
	<li>Slowest Instantaneous Velocity</li>
	<li>OLED Back Light Timeout</li>
	<li>Minimum Rep Threshold</li>
	<li>Tic Length</li>
	<li>Battery Charge</li>
	<li>Unit Number</li>
</ol>
</blockquote>
<span style="color: #ff6600;">Range: </span><span style="color: #800080;">XX</span> can range from 00 to FF

<span style="color: #ff00ff;">Default Value:</span> n/a

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Status Check)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
	<li><span style="color: #ff0000;">40</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal)</span>
<ul>
	<li>In this case the status messages will be read back</li>
</ul>
</li>
</ul>

<hr />

<h4> Slowest Instantaneous Velocity</h4>
<span style="color: #993300;">Interaction: </span><span style="color: #ff0000;">80</span> <span style="color: #800080;">YY<span style="color: #000000;"> where</span> YY is a code with reference table below
</span>

<span style="color: #008000;">Explanation: </span>The slowest instantaneous velocity is set by the maximum allowable time (in microseconds) between "ticks" of the encoder. The slowest instantaneous velocity can be set any where from ~6.15E-08 m/s to ~.003 m/s or you can disable this filter (and all any instantaneous velocity) by sending a value of FF. See below for more information.

<span style="color: #ff6600;">Range: </span><span style="color: #800080;">YY</span> can range from 00 (6.15371E-08 m/s) to FF (0 m/s)

<span style="color: #ff00ff;">Default Value:<span style="color: #000000;"> .01 m/s</span></span>

<span style="color: #0000ff;">Example Transmissions: </span>
<ul>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">00</span> =&gt;<span style="color: #ff0000;"> (Slowest Instantaneous Velocity)</span> <span style="color: #800080;">(00 in Hex = 0 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 6.15371E-08 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">0A</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(0A in Hex = 10 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 6.15371E-07 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">64</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(64 in Hex = 100 in Decimal)</span>
<ul>
	<li>See below for more information. The slowest instantaneous velocity will be set to 0.001218435 m/s</li>
</ul>
</li>
	<li><span style="color: #ff0000;">80</span> <span style="color: #993366;">FF</span> =&gt; <span style="color: #ff0000;">(Status Check) </span><span style="color: #800080;">(FF in Hex = 255 in Decimal)</span>
<ul>
	<li>See below for more information. A value of FF will disable this filter and allow any instantaneous velocity.</li>
</ul>
</li>
</ul>
<strong>Further Explanation</strong>

In version 1.08 the default for the slowest instantaneous velocity is ~0.01 m/s however you can make that much, much slower (any where from ~6.15E-08 m/s to ~.003 m/s). Refer to the table below to see the corresponding number to send to get the desired slowest instantaneous velocity. Keep in mind that the chart below displays values in DECIMAL notation however all values MUST BE SENT IN HEXADECIMAL notation.

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/SlowestInstVelocityFull.jpg" height="498" width="732"> 

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/SlowestInstVelocityLower.jpg" height="498" width="732"> 

<h5> Full Table </h5>
For a full table of values to send to the device for a given velocity see [[SlowestInstVelocity Table]]

<h2> Setup At The Gym </h2>
[[#toc|Back to Table of Contents]]

<h2> Warranty </h2>
[[#toc|Back to Table of Contents]]

The Squats and Science OpenBarbell is unlike most consumer devices available for purchase. It was made by a couple engineers who were fed up with the lack of accessibility for advanced training tools and decided to solve the problem themselves. That meant making something that works quickly and at low cost. Although we would love to continue to support our devices as long as you own them, we will only be making these in small batches and therefore unable to replace parts, dedicate a service team or absorb the costs of return shipping. We will stand by our product up to 14 days after receipt of the device, after which you can contact us for further support inquiries.

OpenBarbell, like the name suggests, is also totally open source and Arduino compatible. Normal warranties prevent users from hacking their devices, but we encourage it. We do not wish to preclude you from modifying your device and we hope you have the ingenuity to create functionality that the community can take advantage of. We cannot however fix issues that arise from the modification or alteration of OpenBarbell, and we are not liable for repairs for said issues.

That being said, we do plan on helping our owners wherever we can. Any questions you have about your device can (or may already) be answered in the [http://squatsandscience.com/forums/forum/openbarbell-buildlog/owners/ OpenBarbell Owners Forum] . If the forum doesn’t help and you’re feeling frustrated you can also send an email to the dedicated account rep1support@squatsandscience.com. This service will never expire and as long as we have fingers (and money to pay for hosting) we will be replying to your forum posts.

<h2> Issue List </h2>
[[#toc|Back to Table of Contents]]

This is an evolving known bug list that will likely increase over the next few weeks and month. We cannot find or fix every issue in our firmware and hardware before it's sent out, but we did our best to make sure they were all identified and the serious issues were addressed.
<h3>Peak velocity does not give accurate readings above 2.0 m/s</h3>
<ul>
	<li>Each displacement reading is put through a filter to reduce erroneous values due to encoder imbalances, indoor lighting effecting our optical sensors, inconsistent spring tension, string slack, etc. This filter helps us eliminate bad values but also dampens our good values. If you achieve a maximum instantaneous velocity above 2.0 m/s the display will read "MAX". We understand this limitation for very fast lifts, including Olympic lifts like the snatch and clean &amp; jerk, and we are working hard to introduce a high accuracy mode in the phone app to be released in Spring of 2016.</li>
</ul>
<h3>OpenBarbell does not function as expected when plugged into power</h3>
<ul>
	<li>In order to keep this device as open source as possible we wanted to make sure that you can reprogram the device at will - in order to do this we had to "share" some of the functionality across different hardware. For this reason the USB is not only used to charge the device but also allows reprogramming over FTDI via a USB MicroB Plug Breakout board. For reasons we'd love to discuss with you in depth if you'd like, the USB connection interferes with the button presses. While it is a minor inconvenience we think the ability to hack the device makes up for it!</li>
</ul>
<h3>Switching between Power and Olympic modes can show a 0.00 velocity rep</h3>
<ul>
	<li>This is because the displayed rep is changed after two seconds in order to refresh the screen, so it doesn't appear to be stuck on the 'Power' or 'Olympic' mode. Fixing this bug would have required the introduction of a more sophisticated state machine to run our display, which would have elongated our release schedule. This bug does not effect performance.</li>
</ul>
<h3>Invert mode can be inhibited by slightly misaligned top screws</h3>
<ul>
	<li>Our optical encoders require a precise position to read tics accurately. When assembled, our devices were tested to work recording tics from a position on the floor, and some units needed to be re-calibrated to work in both directions. If these screws loosen over time it might cause this same issue to arise again.</li>
</ul>
<h3>Kevlar knot can come untied from the string hook</h3>
<ul>
	<li>This happens on rare occasions and was remedied by re-affixing each unit to the string hook. If the string comes undone and pulls back into the device, the spindle could un-spin from the spring and lose retractability. If this happens please contact us.</li>
</ul>
<h3>Magnets may be loose and spin in place</h3>
<ul>
	<li>If this is the case for your unit, please do not try to tighten them. Their spinning does not inhibit their ability to magnetically adhere to a surface, and tightening them could interfere with internal component alignment. This issue does not impact performance.</li>
</ul>

<h3>First Timestamp Bug</h3>
<ul>
        <li>A variable named tic_timestamp_last doesn't get cleared between reps when using OpenBarbell V1.0 release code. This causes the very first time measurement of a rep to be huge, but the effect of that is very minimal since it gets filtered out by our low pass filter.</li>
</ul>
<h3>Time Waiting Bug</h3>
<ul>
        <li>We have a function called 'time waiting' that removes velocity readings below a customizable threshold (.01 m/s by default). This is useful because a lift might end very smoothly without changing direction, which is what we use to indicate a rep has finished. We then remove the amount of time spent at the end of your rep. The OpenBarbell V1.0 release code does not also remove the amount of displacement during that time. This usually only accounts for about 3mm of ROM.</li>
</ul>
<h3>0.0 Velocity Bug</h3>
<ul>
        <li>In testing we have very rarely recorded velocities of 0.0 randomly after a long period of use. This has yet to be repeated so we are having a hard time locating the bug. More info will be added here when it's available. </li>
</ul>

<h2> Limitations </h2>
[[#toc|Back to Table of Contents]]

<strong>Limitations:</strong>

There are none! Just kidding, of course there are limitations. OpenBarbell was built to be a low barrier to entry device so people can start taking advantage of velocity based training principles. While we wish we could implement all of the features we have in mind, it wouldn't be feasible for this device. Here are a few things we can't do.

&nbsp;

<strong>Bar Path</strong>

OpenBarbell cannot measure bar path. At the most basic level, it measures the velocity vector of a single point in space in one dimension. As much as we'd like to do some engineering wizardry, there is just no way to figure out where your bar is in space only by pulling out a string. This doesn't mean we can't tell you anything about your form. Our range of motion measurements tell you a lot about your consistency and which reps were higher, lower, tighter and better set-up. Our peak velocity height reading can tell you where you're achieving your fastest speed and you can measure how that changes over time. We think these metrics will be very valuable to your training in the place of absolute bar position.

&nbsp;

<strong>Peak Velocity Over 2 m/s on the Device</strong>

In order to lower costs and make hand assembly in the USA feasible we needed to invent our own optical quadrature encoder. There are companies who focus on that aspect alone for decades and they make wonderful systems. Ours is definitely adequate for its purpose, but there are a few drawbacks. The readings fluctuate a little from one to another, which are averaged out very well with our average velocity calculations. Peak velocity however extracts one reading that is the very fastest, so erroneous spikes can cause a wildly inaccurate reading. To fix this, we put whats called a one pole low pass digital filter on our incoming measurements and this allowed us great accuracy below 1.5 m/s, good accuracy up to 2.0 m/s, and less than consistent peak velocities above that. We made a decision that rather than show you readings we aren't confident about, we will instead display 'MAX' to the screen. A peak velocity above 2.0 m/s is rare in powerlifting so we don't think this will be much of an issue, but Olympic Weightlifting can reach those speeds often. That's why we're implementing much more effective filtering in our upcoming app and a new high precision mode that can unlock some more accuracy from your device.

&nbsp;

<strong>Device Placement</strong>

OpenBarbell must be placed directly below where the bar will be moving in order to achieve accurate and repeatable results. Any angle away from vertical that the string is pulled from the device will reduce the speed your device will read. You don't need to do anything special, just make sure the device is approximately where you expect to be at the end of a walk out, unrack, or break the ground on a deadlift.

&nbsp;

<strong>Bluetooth Transmission</strong>

When our app is launched, it will transmit data in bulk to your device. Since OpenBarbell utilizes the very low power Bluetooth 4.0 LE, our transmission rates cause a delay in the speed at which you can complete reps. To circumvent this issue, we have a high speed mode that sends about 1/5th of the bulk data to your device along with all of the OpenBarbell measurements you see on the OLED screen. What this means is in this mode, your app will be able to do simple graphs and math on your data as well as display the same info on your OpenBarbell screen, but it will not be able to do some more complicated features by default. That's why we've implemented High Precision Mode, where you get every single reading the device captures but it takes anywhere from 1 to 4 seconds to send it all to your device. This mode allows us to do much higher peak velocity readings (see out 2.0 m/s cap above), as well as very high resolution graphing and other features. This will be an option on the app that will activate this mode in the future.

<h2> BOM </h2>
[[#toc|Back to Table of Contents]]
{| class = "wikitable"													
|	Item Number	||	Part Number	||	Description	||	Material	||	Vendor	||	Link	||	QTY.
|-													
|	1	||	Tube Base	||	Exterior Bottom of Unit	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	2	||	Countersunk Magnet	||	3/8" od x 1/8" thick with countersunk hole for #4 screw	||	NdFeB, Grade N42	||	K&J Magnetics, Inc.	||	http://www.kjmagnetics.com/proddetail.asp?prod=R622CS-S&cat=173	||	4
|-													
|	3	||	CircBase	||	Base of inner tower	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	4	||	91772A151	||	Pan Head Phillips Machine Screw - 6-32 Thread, 3/4" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772A151	||	4
|-													
|	5	||	Battery_Top	||	Battery Cover	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	6	||	BearingHolder	||	Bearing Walls	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	2
|-													
|	7	||	608_Bearing	||	Abec 9 - Size 608 Bearings	||	Titanium/Stainless Steel	||	Amazon	||	http://www.amazon.com/Titanium-Stainless-Sporting-Skateboard-Bearings/dp/B00IZ7LBLW/ref=sr_1_11?ie=UTF8&qid=1460066714&sr=8-11&keywords=608+bearing+abec+9	||	2
|-													
|	8	||	Axle	||	Spring/Spindle Axle	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	9	||	SpringSpool	||	Tape Measure Spring Spool	||	Injection Molded Plastic	||	Custom Component	||	n/a	||	1
|-													
|	10	||	Spindle_Wall	||	Spindle Wall without Slots for IR encoder	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	11	||	Spindle_Insert_String	||	Spindle Core with Cutout for String	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	12	||	Spindle_Insert	||	Spindle Core	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	13	||	Spindle_Encoder_Wall	||	Spindle Wall with Slots for IR encoder	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	14	||	91772A114	||	Pan Head Phillips Machine Screw - 4-40 Thread, 7/8" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772A114	||	2
|-													
|	15	||	91831A005	||	Nylon-Insert Locknut - 4-40 Thread Size, 1/4" Wide, 9/64" High	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91831a005/=11vss2j	||	10
|-													
|	16	||	Top_Bearing_Connect	||	Bearing Wall Bridge	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	17	||	Top_Mount	||	PCB Mount	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	18	||	91772A110	||	Pan Head Phillips Machine Screw - 4-40 Thread, 1/2" Length	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91772a110/=11vst2z	||	8
|-													
|	19	||	PCB_Lenoff	||	Assembled PCB	||	FR4 PCB	||	Custom Component	||	n/a	||	1
|-													
|	20	||	Tube	||	Exterior Tube	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	21	||	Top_Wings	||	Connection between Tube, PCB and Top Cover	||	1/4" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	22	||	Top_Cover	||	Top Cover to protect PCB	||	1/8" Cast Acrylic	||	Custom Component	||	n/a	||	1
|-													
|	23	||	97975A115	||	Thread Forming Screw for Brittle Plastic - Pan Head, 4-24 Thread, 1/2" Length	||	410 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#97975a115/=11vstf4	||	4
|-													
|	24	||	91831A007	||	Nylon-Insert Locknut - 6-32 Thread Size, 5/16" Wide, 11/64" High	||	18-8 Stainless Steel	||	McMaster-Carr	||	http://www.mcmaster.com/mv1459975500/#91831a007/=11vstwk	||	4
|-													
|	25	||	Switch_Cover	||	Power Switch Cap	||	PLA Plastic	||	Custom Component	||	n/a	||	1
|-													
|	26	||	Battery	||	1000 mAh	||	Polymer Lithium Ion Battery	||	Sparkfun	||	https://www.sparkfun.com/products/339	||	1
|}													


<h2> FCC Notification </h2>
[[#toc|Back to Table of Contents]]

<h3>What is this section even for?</h3>
This section is a heads up to you, the users, and for our friends over at the FCC. The FCC has a monumental task of monitoring and managing a common resource that we all need, the electromagnetic spectrum. In order to make sure that everyone plays nicely in this area, a series of tests and certifications are necessary to ensure that our device won't negatively impact any other device. Below is some information pertinent to those tests as well as some guidelines if unexpected interference occurs.

&nbsp;
<h3>FCC Notification</h3>
Contains FCC ID: UYI25

This device complies with Part 15 of the FCC Rules. Operation is subject to the following two conditions"

(1) This device may not cause harmful interference and

(2) This device must accept any interference received, including interference that may cause undesired operation.

&nbsp;
<h3>More in-depth...</h3>
This equipment has been tested and found to comply with the limits for a class B digital device, pursuant to part 15 of the FCC Rules. These limits are designed to provide reasonable protection against harmful interference in a residential installation. This equipment generates, uses and can radiate radio frequency energy and if not installed and used in accordance with the instructions, may cause harmful interference to radio communications. However, there is no guarantee that interference will not occur in a particular installation. If this equipment does cause harmful interference to radio or television reception, which can be determined by turning the equipment off and on, the user is encouraged to try to correct the interference by one or more of the following measures:

&nbsp;

* Reorient or relocate the receiving antenna.

* Increase the separation between the equipment and receiver.

* Connect the equipment into an outlet on a circuit different from that to which the receiver is connected.

* Consult the dealer or an experienced radio/TV technician for help.

&nbsp;

In order to maintain compliance with FCC regulations, shielded cables must be used with this equipment. Operation with non-approved equipment or unshielded cables is likely to result in interference to radio and TV reception. The user is cautioned that changes and modifications made to the equipment without the approval of manufacturer could void the user's authority to operate this equipment.

<h2> OpenBarbell V1.0 Specs </h2>
[[#toc|Back to Table of Contents]]

OpenBarbell is powered by a Nordic nRF51 series ultra low power SOC. This system is a combination of a 2.4 GHZ Bluetooth transceiver and a low power 32 bit ARM Cortex -M0 core. This package is mounted onto a board developed by RF Digital called the RFduino, which is Arduino compatible and FCC Module Certified for use in consumer electronics.

&nbsp;

MORE COMING SOON.

<h2> What we can do with Velocity Data </h2>
[[#toc|Back to Table of Contents]]

We're working hard on this - Come back soon!



<h1> OpenBarbell V0.25 </h1>

<p style="text-align: center;"><img src="http://squatsandscience.com/wp-content/uploads/2015/08/email_image.jpg" width="600" height="291"> </p>

Here you'll find all the info that requires version control for OpenBarbell version 0.25. V0.25 was developed in the Fall of 2015 and shipped to Dr. Mike Zourdos in December 2015. The device was made for that purpose as well as to make a more friendly open source alternative to V0.24. It is the fourth version of OpenBarbell, following the first prototype dubbed ‘Mystery Shoebox’, the second prototype which is the original 3D printed OpenBarbell unit, and V0.24 which is the first open sourced design.

<h2>Feature List</h2>
<ul>
	<li>Sub-3mm accuracy with custom 3D printed encoder wheel</li>
	<li>Quadrature encoder for directional output</li>
	<li>Average velocity output accurate to 2 units of precision (validated against Tendo Unit)</li>
	<li>Stores up to 39 reps locally</li>
	<li>2 buttons for toggling between reps and UI input</li>
	<li>OLED screen</li>
	<li>Rechargeable Lithium Polymer battery (lasts several weeks on a charge)
<ul>
	<li>charges from 3% to 40% in minutes</li>
</ul>
</li>
	<li>Also compatible with disposable battery power source</li>
	<li>Bluetooth capable</li>
	<li>Compatible with OpenBarbell phone app to be released in the Spring</li>
	<li>10 ft. Kevlar string</li>
	<li>3D printed enclosure</li>
	<li>12 ft. spring steel reel</li>
</ul>

<h2> Parts List </h2>

The following links below are active as of 1/24/2016. They are the lowest cost sources that we have found in our efforts to this point. If better resources are found feel free to edit this Wiki. Our goal will be to have most of these parts for sale in the squatsandscience.com web store.
<ul>
	<li>PCB Components (See BOM - http://squatsandscience.com/wp-content/uploads/2016/01/OpenBarbell_V0p25_BOM.xls):
<ul>
	<li>http://www.digikey.com/short/3cjzr4 - Components available via DigiKey (click for DigiKey cart)
<ul>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757357&amp;uq=635871091745723126 - 1 x LED RED DIFFUSED 0805 SMD (NOT NEEDED FOR DISPOSABLE BATTERY BUILD)</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757358&amp;uq=635871091745733126 - 1 x DIODE SCHOTTKY 20V 1A SOD123</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757354&amp;uq=635871091745733126 - 3 x CAP TANT 10UF 6.3V 20% 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757350&amp;uq=635871091745743126 - 1 x LED GREEN CLEAR 0805 SMD</li>
	<li>http://www.digikey.com/product-detail/en/T520B686M006ATE025/399-5231-1-ND/1830043 - 1 x CAP TANT POLY 68UF 6.3V 1411</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757349&amp;uq=635871091745753126 - 1 x CAP CER 10000PF 50V X7R 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757352&amp;uq=635871091745753126 - 1 x CAP CER 1UF 16V X7R 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757348&amp;uq=635871091745753126 - 1 x CONN HEADER PH SIDE 2POS 2MM SMD (NOT NEEDED FOR DISPOSABLE BATTERY BUILD)</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757351&amp;uq=635871091745763126 - 1 x RES SMD 4.7K OHM 1% 1/8W 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757347&amp;uq=635871091745763126 - 1 x RES SMD 1K OHM 5% 1/8W 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757345&amp;uq=635871091745773126 - 1 x RES SMD 590 OHM 1% 1/8W 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757344&amp;uq=635871091745773126" target="_blank">2 x RES SMD 100 OHM 1% 1/8W 0805</a> <span style="color: #ff0000;">(ONLY ONE NEEDED FOR DISPOSABLE BATTERY BUILD)</span></li>
	<li>http://www.digikey.com/product-detail/en/MCP73831T-2DCI%2FOT/MCP73831T-2DCI%2FOTCT-ND/1979804 - 1 x IC CONTROLLR LI-ION 4.2V SOT23-5</a> <span style="color: #ff0000;">(NOT NEEDED FOR DISPOSABLE BATTERY BUILD)</span></li>
	<li>http://www.digikey.com/product-search/en?vendor=0&amp;keywords=576-1259-1-ND - 1 x IC REG LDO 3.3V 0.15A SOT23-5</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757342&amp;uq=635871091745783126 - 1 x CAP CER 0.1UF 50V X7R 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757341&amp;uq=635871091745783126 - 1 x RFDUINO BLE 4.0 SMT MODULE</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757338&amp;uq=635871091745793126 - 1 x FIXED IND 47UH 720MA 370 MOHM</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=186757336&amp;uq=635871091745793126">1 x IC REG BOOST 5V 0.13A 5TSOP</li>
	<li>http://www.digikey.com/product-detail/en/C0805C475K9PACTU/399-3134-1-ND/551639 - 2 x CAP CER 4.7UF 6.3V X5R 0805</li>
	<li>http://www.digikey.com/product-detail/en/08055A102JAT2A/478-1328-1-ND/564360 - 1 x CAP CER 1000PF 50V NP0 0805</li>
	<li>http://www.digikey.com/product-detail/en/RC0805FR-072KL/311-2.00KCRCT-ND/730611 - 1 x RES SMD 2K OHM 1% 1/8W 0805</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=187430306&amp;uq=635881208933649085 - 1 x C&amp;K Components  AYZ0102AGRLC</li>
	<li>http://www.digikey.com/scripts/DkSearch/dksus.dll?Detail&amp;itemSeq=187430057&amp;uq=635881215589011586 - 1 x MICRO USB, 2.0 TYPE B, RECEPTACLE, TH</li>
	<li>http://www.digikey.com/product-search/en?keywords=480-1966-ND - 1 x EMITTER IR 880NM 50MA RADIAL</li>
	<li>http://www.digikey.com/product-search/en?keywords=HLC2705 - 1 x SENSOR LOGIC OUT OPTIC SIDE VIEW</li>
</ul>
</li>
	<li>Components currently not in stock on DigiKey (available elsewhere)
<ul>
	<li>http://www.digikey.com/product-search/en?keywords=MAX17043G%2BU - 1 x Battery Management MAX17043G+U</a> <span style="color: #ff0000;">(NOT NEEDED FOR DISPOSABLE BATTERY BUILD)</span></li>
	<li>http://www.digikey.com/product-detail/en/95C06F3GWT/95C06F3GWT-ND/2681049">1 x SWITCH TACTILE SPST-NO 0.05A 12V</li>
	<li>http://www.banggood.com/5Pcs-0_96-Inch-4Pin-White-IIC-I2C-OLED-Display-Module-For-Arduino-p-971295.html">1 x 0.96 Inch 4Pin BLUE IIC I2C OLED Display Module</li>
</ul>
</li>
</ul>
</li>
	<li><span class="component-number">1</span> <span class="component-x">×</span> <span class="component-content">6-12 ft Tape Measure t<span class="component-description">o extract spring steel for retracting mechanism</span></span>
<ul>
	<li>Wal-Mart has a 12 ft. tape measure for $1 that has very low string tension when used in the OpenBarbell.</li>
</ul>
</li>
	<li><span class="component-number">1</span> <span class="component-x">×</span> <span class="component-content">Enclosure <span class="component-description">Currently 3D printable</span></span>
<ul>
	<li>As of the date of this Wiki, the enclosure needs to be 3D printed by each OpenBarbell maker. See instructions for other options to acquire 3D parts.</li>
</ul>
</li>
	<li>https://www.sparkfun.com/products/10718 - 1 x 400 mAh LiPo battery (CAN BE REPLACED WITH 9V BATTERY)</li>
	<li>http://www.ebay.com/itm/FREE-SHIPPING-200ft-100lbs-Braided-Kevlar-Line-String-for-Fishing-Kite-/280894228405?pt=LH_DefaultDomain_0&amp;hash=item416699c7b5 - 6-12ft Kevlar String</li>
	<li>http://www.ebay.com/itm/PRECISION-BEARINGS-PACK-OF-8-ABEC-7-FITS-4-SKATEBOARD-LONGBOARD-WHEELS-/331558540987 - 2 Metal Bearings</li>
</ul>
You will also need the following:
<ul>
	<li>Solder</li>
	<li>Soldering Iron</li>
	<li>SMD reflow station for MAX17043G+U (if you're skilled in soldering, you do not need this)</li>
	<li>Hot glue gun</li>
	<li>Superglue</li>
	<li>Hot air gun (not required, used for heat shrink tubing)</li>
	<li>3D printer &amp; 3D printer filament (unless acquiring 3D parts elsewhere)</li>
	<li>Pliers (to install spring)</li>
	<li>Razer blades (to clean up prints)</li>
</ul>

<h2> Instructions </h2>
<img src="http://squatsandscience.com/wp-content/uploads/2016/04/AWMc7tk-Imgur.gif">


<ol>
	<li>Read the top level Wiki titled “Build Your Own OpenBarbell” for a list of things you need to get done before you start this version-specific instruction. Once those items are completed, move on to step 2.</li>
	<li>By now you should have all of the source files needed to complete an OpenBarbell unit from scratch. V0.25 is packed with a lot more content than previous versions, including a set of Eagle CAD files, a detailed PCB bill of materials with a Digikey Cart - http://www.digikey.com/short/3cjzr4, and a reference designator file to describe what part goes where on the PCB. When you're ready to build, check out our YouTube tutorial that takes you through a full build of a V0.25 prototype. It's recommended when assembling the 3D printed device to have the Solidworks assembly in front of you. If you don't have Solidworks then have no fear, the tutorial will guide you - https://www.youtube.com/embed/qytn7cA2MjQ.

&nbsp;

</div></li>
	<li>A total of 19 parts need to be printed (one of which is optional), you can find the list below. All of these parts can be printed without support material. Unless specified, the parts below can be printed at 0.3mm layer size. We recommend printing your own parts, but if need be you can use services like <a href="https://www.3dhubs.com/3dprint#" target="_blank">3DHubs </a> and Shapeways - http://www.shapeways.com/. See step 4 for a description of how to install the spring.
<ul>
	<li>Axel (0.2mm)</li>
	<li>Battery Compartment</li>
	<li>Compartment bottom (0.2mm)</li>
	<li>Dowel x 4 (0.2mm)</li>
	<li>Housing</li>
	<li>Pillar Base</li>
	<li>Pillar Lock Flange</li>
	<li>Pillar Lock</li>
	<li>Pillar</li>
	<li>Pillar Balance</li>
	<li>Screen Mount (optional) (0.2mm)</li>
	<li>Spindle Encoder (0.1mm, or the smallest possible layer size for your 3D printer)</li>
	<li>Spindle Housing</li>
	<li>Spring Mount Thin (or Spring Mount Wide, depending on your spring width)</li>
	<li>String Guard</li>
	<li>String Hook
<ul>
	<li>The reason you need to print 21 files instead of 1 like you see in 3D printing videos is because this device pushes the limits of the 3D printer. Parts like the Spindle Encoder need to be very precise so they need to be printed in a precise manner. Other parts tend to warp if printed together, so they are separated. Support material has been completely avoided to reduce plastic burs.</li>
</ul>
</li>
</ul>
</li>
	<li>Check out our tutorial for a visual walk through of the Spring Mount installation (https://youtu.be/qytn7cA2MjQ?t=8m38s). The Spring Mount was designed to be slightly larger than the average spring enclosure in a 6-12 ft. tape measure, so it could be possible to grab the spring out of the tape measure and transplant it to the Spring Mount without it unraveling. If it does unravel, the spring MUST be wound in reverse direction or it will not provide retraction for your OpenBarbell unit. Care must also be taken to install the spring in the correct orientation. V0.25 was built so the string is pulled from the right of the encoder (if you are facing the screen). If the string is pulled from the left of the encoder (because the spring was installed incorrectly) you can just change the direction bit in the code and it will work, but you will not have the string guard to keep the string from getting caught in the spindle.
<ol>
	<li>Changing the direction bit: This is useful if the OpenBarbell happens to be reading the downward velocity instead of the upward velocity. That should only happen if you have installed either the spring or the string in the wrong direction. All you need to do is change which input value the code thinks is UP.  That code can be found on line 175:
<ul>
	<li>goingUpward = digitalRead(3);</li>
	<li>change to: goingUpward = !digitalRead(3);</li>
</ul>
</li>
</ol>
</li>
	<li>The electronics for V0.25 are the biggest differentiator between it and V0.24. If you don't have experience doing SMD soldering you can still use the previous schematic from V0.24 and it will work on this version, just keep in mind there is less space in the battery compartment for the electronics in V0.25. The old version is not compatible with a single cell 3.7V lithium polymer battery, so to fit in the smaller enclosure a 9V battery and a 5V regulator (compatible with 9V input) is recommended. Here, we'll outline all of your choices for obtaining your own OpenBarbell PCB.
<ol>
	<li>Making it yourself - This is a two layer PCB so you would need to use a DIY method that allows copper on both sides as well as VIAS. These methods exist - http://www.instructables.com/id/Two-sided-PCB-using-toner-method/?ALLSTEPS - but they are tricky. Option two may be a better bet for most people.</li>
	<li>Buying small batches - There are a few great resources out there for small batch PCB manufacturing. OSHPark - https://oshpark.com/ - and DirtyPCBs - http://dirtypcbs.com/ - are a couple that we've used before and like. In fact, here's our shared project on OSHPark - https://oshpark.com/shared_projects/IcWd7Sc6. If you're not in a rush, you can get a handful of boards for about 5 bucks a piece or less. If you do this and end up with extra boards please feel free to post in the For Sale/Wanted forum - http://squatsandscience.com/forums/forum/openbarbell-buildlog/general-questions/for-salewanted/ - that you have spares. If you aren't confident in your PCB purchasing skills, head down to option 3.</li>
	<li>Buy one from us - http://squatsandscience.com/product/openbarbell-v0-25-pcb/. We have extras from our prototyping batch that worked like a charm (we didn't have to change anything but the silkscreen) so we're tossing them in the online store at cost. We paid a little more than the price you can get from OSHPark (we needed them in a particular way, and FAST) but they're guaranteed to work and you'll be supporting the cause.</li>
</ol>
</li>
	<li>Once you get yourself a PCB and buy everything on our above mentioned Digikey Cart - http://www.digikey.com/short/3cjzr4 you're ready to assemble the electronics (keep in mind, if you're looking for a budget version of the OpenBarbell you can have the same VBT functionality without a lithium ion battery, lithium ion charger, and lithium ion fuel gauge and save about $7). If you're skilled with a soldering iron you can do everything with just that. If you're kind of OK with one but not the greatest, you'll need to find a local makerspace that has a surface mount station or some kind of hot air reflow machine - https://youtu.be/qytn7cA2MjQ?t=21m9s - (the MAX17043 has small pads, although they have a little bit of exposed pad that can be soldered by hand in a pinch, we've done it a couple times). For your convenience, we put together a reference designator file - http://squatsandscience.com/wp-content/uploads/2016/01/OpenBarbell_Order_V0p25_11_7_2016.pdf - that matches up with part numbers and descriptions on our BOM - http://squatsandscience.com/wp-content/uploads/2016/01/OpenBarbell_V0p25_BOM.xls. We recommend starting from the top and crossing out each item on the BOM until the board is done.
	
	<img src="http://squatsandscience.com/wp-content/uploads/2016/01/IMG_3175.jpg" height="683" width="1024">
	
	<li>Head up one level in this Wiki and you'll find the OpenBarbell V0.25 parts list. We've put together a list of links where you can find yourself everything you need that can't be made at home. We did our best to source everything in the US and reduce the number of stores you need to visit to complete the build. If you know of any improvements or found a better source, go ahead and post it in the Where to Find Parts Forum - http://squatsandscience.com/forums/forum/openbarbell-buildlog/general-questions/where-to-find-parts/</li>
	<li>At this point, you've collected all 19 requisite OpenBarbell parts, bought a bunch of miscellaneous dubiously related items, acquired a PCB and assembled all components, and are staring at a pile of anabolic potential. If you haven't already, now is when you should head over to the Tubes and watch our OpenBarbell V0.25 tutorial - https://www.youtube.com/watch?v=qytn7cA2MjQ.
<ol>
	<img src="http://squatsandscience.com/wp-content/uploads/2016/04/ypWufQC-Imgur.gif">
</ol>
</li>

<h2> Uploading Code </h2>
	<li>Back already? That must mean you have a fully assembled OpenBarbell ready to upload code. To do so, you need to connect the RFduino on your device to an FTDI breakout board - http://forum.rfduino.com/index.php?topic=75.0. RFduino sells a USB shield that does just that - http://www.rfduino.com/product/rfd22121-usb-shield-for-rfduino/, or you can use anything you have lying around. We routed the appropriate pins to the spare microUSB pins on the board for easy access, but don't go plugging it into your computer. We need to get those pins hooked up to your FTDI board. You need 5 pins to program an RFduino, GND, VCC, TX, RX, and RESET. TX and RX are hooked up to pins GPIO0/1 so they are routed to USB pins D+ and D-. The most convenient way to access these pins is to split a USB cord, but most USB cords do not utilize the ID pin and therefore do not have a 5th wire. If you do not have a 5 pin microUSB cable, you need a microUSB breakout board to have access to these pins. Sparkfun has a great one for $4 - https://www.sparkfun.com/products/10031. See the schematic below for reference.
<ol>

<img src="http://squatsandscience.com/wp-content/uploads/2016/01/GPIO_to_USB2.png" width="476" height="632">

</ol>
</li>
	<li>Now that we're hooked up to the computer we can go ahead and load code. You should have been to our Github by now, but if not you can download the release code here - https://github.com/seminolemuscle/V0.25/tree/master/OpenBarbell_12_29_2015. Make sure you download all of the libraries used for the code, and double check that you're downloading the ARM version of the libraries and not the AVR version (if you download Adafruit_SSD1306 and not Adafruit_SSD1306<strong>ms</strong>.h you'll get a delay.h issue). You can find the libraries here - http://squatsandscience.com/wp-content/uploads/2016/01/OpenBarbell-Libraries.zip, but please download fresh versions as these are not live.</li>
	<li>Libraries are up to date? Great, you should be able to load code and start playing with your device. Velocity is a great unit of measurement when consistent, but it's even better when accurate. That's why we recommend everybody to calibrate their own unit against a VBT device whenever possible. We've been able to verify accuracy on our end by comparing it to several gold standard velocity measurement devices, but there could be a few things that fudge that calibration between our build and yours. If you do get that chance, the fix is pretty simple. Go into the code and play with line 64. It represents the space of the gaps in the encoder in micrometers. You adjust that up if your device is reading slow, and down if it's reading fast.
<ol>
	<li><span class="pl-k">long</span> ticLength = <span class="pl-c1">2950</span></li>
</ol>
</li>
	<li>If you're here, you're pretty much set! Check back soon for updates on the open source phone app that's currently in development and what you can do to hack that as well. Please do us a solid and head to the forum and document your build. Others will be happy to see it and it will undoubtedly help them on their very own OpenBarbell build.</li>
