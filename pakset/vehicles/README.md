# How to Vehicle in Pak192.Comic

Small documentation on how to use the sub-folders.
We're very aware that this convention is not on full affect on everything yet, but that's work in progress.


## What's there to be defined in the .dat file?

We start with

> obj=vehicle

as first line. That's a no brainer and in every dat-file of a vehicle.

> name=Track_Passenger_Train_1999_Doppelstockwagen

After that, we define the name of the vehicle. For that, read further into the naming of vehicles in the following paragraphs.

> intro_year=1999

> intro_month=6

Is next. Please use the year of the introduction of the vehicle to service. This is not about when the vehicle is build, but rather on the date it can be put into service from the company purcheasing it.

> runningcost=1034

> cost=11376338

Honestly, we don't need this right now. These values will be generated by the github-action.

> weight=58

This is the operating weight without the load.

> speed=160

Fastest operating speed in service.

> payload=150

The definition of this is work in progress. Just put in something that seems to fit in the game.

> freight=Passagiere

In case you're lost witht hese, check out the goods.dat file in the buildings/industry folder. It lists all the kinds of goods we have in the game.

> length=12

Visual length of the vehicle. The vehicle will have a size of its length times 6px in S, W, N, E, 4px in NW and SE, and 8px in NE and SW.

> waytype=narrowgauge_track 

Waytype of the vehicle. Mind that �narrowgauge_track� and �track� are swapped in this pakset.

> loading_time=10340

Loading time for a full load in milliseconds. Honestly, we don't need this right now. This value will be generated by the github-action.

> constraint[prev][0]=any

Constraints are a complicated construct. For startes, put in `constraint[prev][0]=any` in case your vehicle shouldn't be put in front, and do not put in anything in case it shall be put in front.

> EmptyImage[W,N,E,S,SE,NE,NW,SW]=image/Passenger_Train_1999_Double_Deck.3.<$0>

Image definitions; please look them up by now; they're to be added to this by a later point of time.

## Name of the vehicle

The name of the vehicles builds from the following aspects, linked by underscores:

- The type of way. It's okay to use "Narrowgauge" instead of "Narrowgauge_Track"
- The type of vehicle
- The transported good
- The year of introduction
- Optional: a known name of the vehicle to help identifying it
- In case there are multiple vehicles with the same name, add an additional counter

Examples:

> Narrowgauge_Car_Agriculture_1935

> Narrowgauge_Passenger_Train_2015_Komet_1

> Track_Car_Piece_Goods_1986_Hbbills_305

> Track_Lokomotive_2003_BR189

## Name and position of the .dat file

All .dat files are positioned in the main vehicles/waytype folder.
The .dat file has the same name as the vehicle, except there being no way in front, as that's a given.
You can merge multiple vehicles in the same .dat file, but only if the .dat file name is leagal and holds true for all the vehicles in the file.
Examples for good names of .dat files:

> Passenger_Train_1990_Dostos.dat

> Lokomotive_1993_OBB1014.dat

Examples for bad names of .dat files:

> Tram_Leipzig.dat

> vt17.dat

## Name and position of the .png files

The .png file shares either the name of the vehicle or the dat file.
In case of latter, all vehicles of that .dat file shall be includet.
All images are hosted in a sub folder called "image".
Examples of good .png file references:

> ./image/Lokomotive_2003_BR189.png

> ./image/Electric_1999_ICE3.png

Examples of bad .png file references:

> ./image/BR_120_101.png

> ./DB_FV/Electric_1999_ICE3.png

> Electric_1999_ICE3.png
