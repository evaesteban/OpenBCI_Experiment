# OpenBCI_Experiment

Welcome to the OpenBCI Puppies and Kittens Experiment designed by Fan Li.

During this experiment, you will watch a video containing images of puppies and kittens, and press a button every time you see a puppy in the image.

Below are the instructions on how to do it. The full information on this experiment can be found on [Fan Li's Repository](https://github.com/Fan1117/Puppies_and_Kittens/).

## Equipment Required

1. Headwear, which can be:

- [Ultracortex Mark IV Headset](https://shop.openbci.com/products/ultracortex-mark-iv) with copper cables. 
- [Gold Cup Electrodes](https://shop.openbci.com/collections/frontpage/products/openbci-gold-cup-electrodes?variant=9056028163) with [Ten20 Paste](https://shop.openbci.com/collections/frontpage/products/ten20-conductive-paste-2oz-jars?variant=31373533198).
- [EEG Electrode Cap Kit](https://docs.openbci.com/docs/04AddOns/01-Headwear/ElectrodeCap) with [Electrode Cap Gel](https://shop.openbci.com/collections/frontpage/products/electrodegel?variant=28056992776264) and [Touch Proof Adapter](https://shop.openbci.com/collections/frontpage/products/touch-proof-electrode-cable-adapter?variant=31007211715).
2. [Cyton Board](https://shop.openbci.com/collections/frontpage/products/cyton-biosensing-board-8-channel?variant=38958638542)
2. [OpenBCI GUI](https://github.com/OpenBCI/OpenBCI_GUI/releases/tag/v5.0.0)
3. External Button Breadboard:

- [1x Breadboard](https://www.amazon.com/DEYUE-breadboard-Set-Prototype-Board/dp/B07LFD4LT6/ref=sr_1_5?dchild=1&keywords=breadboard&qid=1591125068&sr=8-5)
- [1x Photoresistor](https://www.amazon.com/DEYUE-breadboard-Set-Prototype-Board/dp/B07LFD4LT6/ref=sr_1_5?dchild=1&keywords=breadboard&qid=1591125068&sr=8-5)
- [1x 220 ohm resistor](https://www.amazon.com/EDGELEC-Resistor-Tolerance-Multiple-Resistance/dp/B07QK9ZBVZ/ref=sr_1_1_sspa?crid=S5FLXTR7YG6L&dchild=1&keywords=resistor+220+ohm&qid=1591125607&s=industrial&sprefix=resistor+220+%2Cindustrial%2C146&sr=1-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExWlRVVTM3QzRBWEE4JmVuY3J5cHRlZElkPUEwOTMyNDM3Q1JIM0gwUlc5UzJYJmVuY3J5cHRlZEFkSWQ9QTAwNzUwODkxSDRDS0ZQVTlJWVpKJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==)
- [5x Jumper cables male to male (8 inch)](https://www.amazon.com/GenBasic-Solderless-Dupont-Compatible-Breadboard-Prototyping/dp/B077N9X7Y3/ref=sr_1_2?dchild=1&keywords=Male%2Bto%2Bmale%2BJumpers&qid=1591126744&sr=8-2&th=1)
- Either [2x Jumper cables female to male (8 inch)](https://www.amazon.com/GenBasic-Solderless-Dupont-Compatible-Breadboard-Prototyping/dp/B077N5RLHN/ref=sr_1_1_sspa?dchild=1&keywords=Male%2Bto%2BFemale%2BJumpers&qid=1591126392&sr=8-1-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEzTEtKREtGMTZSNTA0JmVuY3J5cHRlZElkPUEwMjExMDE0Q0dYOEZCUFlKRFZMJmVuY3J5cHRlZEFkSWQ9QTA0NDYyMjMyMTk5WlhCMEg0MzFRJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ&th=1)  for connection to photoresistor or [2x Jumper cables male to male (8 inch)](https://www.amazon.com/GenBasic-Solderless-Dupont-Compatible-Breadboard-Prototyping/dp/B077N9X7Y3/ref=sr_1_2?dchild=1&keywords=Male%2Bto%2Bmale%2BJumpers&qid=1591126744&sr=8-2&th=1) if we can solder the cable with photoresistor.

## Step 1: Headwear, Board and Software Setup

First, connect the headwear to yourself and to the Cyton board, and read from it using the GUI. If you are using the Ultracortex, follow [this tutorial](https://docs.openbci.com/docs/04AddOns/01-Headwear/MarkIV). If you're using the gold cup electrodes, follow [this guide](https://docs.openbci.com/docs/01GettingStarted/02-Biosensing-Setups/EEGSetup) to learn how to connect each electrode, and connect them in the positions you'd like to measure EEG from. A good guide to the 8 positions commonly used can be found in the Ultracortex tutorial. If you're using an electrode cap, follow [this tutorial](https://docs.openbci.com/docs/04AddOns/01-Headwear/ElectrodeCap) to connect it.

## Step 2: External Button Setup

Using the components listed above, assemble the external button on the breadboard as shown in the pictures below.

![](Full_Breadboard.jpeg)
![](Breadboard.jpeg)

Next, connect the breadboard to the Cyton board as shown in the picture below. Place the breadboard beside your computer such that the photocell points to the lower left corner of your screen, which is where the video trigger will be located.

![](connect.jpg)

## Step 4: Run Experiment

Download [this video](video.mp4). Once you're ready to start, press ```Start Data Stream``` in the GUI,open the video, and make it Full-Screen. Every time a puppy appears in the video, press the button. The video is around 3 minutes long. You're now ready to press play!

## Step 5: Retrieve Data

Once you've finished watching the video, press ```Stop Data Stream```. In your /Documents/OpenBCI_GUI/Recordings folder you should find the recorded data for that session. 

## Step 6: Process Data

In [this file], you'll find sample code to read, plot, and analyze the recorded data. 

## Step 7: Create your Own Experiment

Once you understand how to conduct an experiment, you can modify [this Python script](ExternalTriggerCreator_quick.py) to make your own video. The current code reads the images stored in the ```Images``` folder, shuffles them, and creates a video with 4 different sessions. Each session displays the images at a different rate. Each image has an embedded trigger and is separated from the others by a fixation cross.
