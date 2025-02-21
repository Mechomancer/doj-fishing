# Fishing script for QB

| If you are intested in recieving github updates join the community on **[Discord](https://discord.gg/NVsaunpesE)**! |
|----|

**[Source](https://github.com/Kuzkay/esx_AdvancedFishing)**

**[Inspiration](https://github.com/sven20202020/qb-fishing)**

# About
- Optimized / Now works with new QBCore
- Fish anywhere besides Pools most rivers and such
- Random loot pool Check Config.lua
- 3 diffrent skillbars to choose from
- Utilizes qb-target,qb-menu,& text ui <ehh not so much Most moved to qb-notify, still working on this.>
- Uses Raycast to find water now <real Water> Will be adding some functions later on for freshwater rivers and such for just
	Bass, Trout, Salmon and possibly Catfish.
	
# Info
- **[Rent](https://streamable.com/bymhyv)** a fishing boat
- **[Return](https://streamable.com/ns3qeb)** boat for small refund
- **[Fish](https://streamable.com/ca7wo7)** spawn once caught
- **[Sell](https://streamable.com/5c8nm0)** regular fish easily & exotics no so much 
- **[Purchase](https://i.imgur.com/LIj0Rs8.png)** fishing gear to start your trip 
- **[Store](https://i.imgur.com/eeQrnD0.png)** fish you have caught
- **[Inventory Tooltip](https://i.imgur.com/vnpIb2b.png)** will display species, weight & type
 
- Catch & Sell 13 diffrent items (5 fish, 4 exotic, 2 Trash, 2 Rewards)
- Chance to find a **[Tackle Box](https://streamable.com/4e1kte)** left over from another fisherman when purchasing a boat
- ***Tackle Box*** contains a **[Pearls Seafood Card](https://i.imgur.com/xFEmoLt.png)** required to sell exotic fish
- Chance to catch a ***Small Loot Box*** & ***Treasure Chest*** while fishing
- **[Small Loot Box](https://streamable.com/4ff2ht)** contains a **[Corroded Key](https://i.imgur.com/Pyg81vH.png)** that is needed to open a **[Treasure Chest](https://i.imgur.com/dIKE1rw.png)**

I needed a Decent fishing Script and DOJWUN had a pretty good one, only problem was it didn't work with the new QBCore, So i did a little tinkering
Got some changes for the new Core, Added the raycast to find water, and fixed the HASITEM and Item control to Server side like it should be
Also moved the Images together named correctly to the images folder <they are 100 x 100 BTW>

Plan to add Freshwater poly checks with Freshwater fish as well later but i've tested it and it's working pretty good. If your still running Old Core
I don't think this version will work for ya, But if you are this one is spot on. Thanks DOJWUN!!

PLEASE LET ME KNOW IF YOUR HAVING ISSUES I WOULD LIKE TO MAKE SURE THIS STAYS UP TO DATE!!


# Dependencies
**[textUi](https://github.com/dojwun/textUi)** Will move away from this completely later.

**[qb-menu](https://github.com/qbcore-framework/qb-menu)**


**[qb-target](https://github.com/BerkieBb/berkie-target)**


**[progressBars](https://drive.google.com/drive/folders/1uuxtWibJIZYx2yDY_7y4mnl5AbqDpSqt?usp=sharing)**

### Skillbars

**[reload-skillbar](https://github.com/Utinax/reload-skillbar)**

**[np-skillbar](https://drive.google.com/drive/folders/17xznaEcn5rmP0aOKL5XIj6SIfqQVB8iH?usp=sharing)**

**[qb-skillbar](https://github.com/qbcore-framework/qb-skillbar)**


# images
All images are now in the IMAGES FOLDER - Simply Copy them all and Paste them into your qb-inventory/html/images folder
This was done for simplicity sake by MechoMancer.


# Required
- qb-core/shared/items.lua info
```
	-- Regular Fish
	['stingray'] 			     	 = {['name'] = 'stingray', 				    ['label'] = 'Stingray',            		['weight'] = 2500,      ['type'] = 'item',      ['image'] = 'stingray.png',         	['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Stingray'},
	['flounder'] 			     	 = {['name'] = 'flounder', 				    ['label'] = 'Flounder',            		['weight'] = 2500,      ['type'] = 'item',      ['image'] = 'flounder.png',         	['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Flounder'},
	['codfish'] 			     	 = {['name'] = 'codfish', 				    ['label'] = 'Cod',            			['weight'] = 2500,      ['type'] = 'item',      ['image'] = 'codfish.png',         		['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Cod'},
	['mackerel'] 			     	 = {['name'] = 'mackerel', 				    ['label'] = 'Mackerel',            		['weight'] = 2500,      ['type'] = 'item',      ['image'] = 'mackerel.png',         	['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Mackerel'},
	['bass'] 			 		 	 = {['name'] = 'bass', 						['label'] = 'Bass',                     ['weight'] = 1250,      ['type'] = 'item',      ['image'] = 'bass.png',                 ['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'A normal fish Tatses pretty good!'},
	
	-- Trash Items
	['fishingtin'] 			 	 	 = {['name'] = 'fishingtin', 				['label'] = 'Fishing Tin', 				['weight'] = 2500, 		['type'] = 'item', 		['image'] = 'fishingtin.png', 			['unique'] = false,    ['useable'] = false, 	['shouldClose'] = false,	 ['combinable'] = nil,   ['description'] = 'Fishing Tin'},	
	['fishingboot'] 			 	 = {['name'] = 'fishingboot', 				['label'] = 'Fishing Boot', 			['weight'] = 2500, 		['type'] = 'item', 		['image'] = 'fishingboot.png', 			['unique'] = false,    ['useable'] = false, 	['shouldClose'] = false,	 ['combinable'] = nil,   ['description'] = 'Fishing Boot'},	
	
	-- Exotic Fish
	['killerwhale'] 			 	 = {['name'] = 'killerwhale', 				['label'] = 'Whale', 					['weight'] = 15000, 	['type'] = 'item', 		['image'] = 'killerwhale.png', 			['unique'] = true, 	   ['useable'] = false, 	['shouldClose'] = false,	 ['combinable'] = nil,   ['description'] = 'Killer Whale'},	
	['dolphin'] 			     	 = {['name'] = 'dolphin', 					['label'] = 'Dolphin',          		['weight'] = 5000,      ['type'] = 'item',      ['image'] = 'dolphin.png',       		['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Dolphin'},
	['sharkhammer'] 			     = {['name'] = 'sharkhammer', 				['label'] = 'Shark',         			['weight'] = 5000,      ['type'] = 'item',      ['image'] = 'sharkhammer.png',       	['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Hammerhead Shark'},
	['sharktiger'] 			     	 = {['name'] = 'sharktiger', 				['label'] = 'Shark',          			['weight'] = 5000,      ['type'] = 'item',      ['image'] = 'sharktiger.png',       	['unique'] = true,     ['useable'] = false,     ['shouldClose'] = false,     ['combinable'] = nil,   ['description'] = 'Tigershark'},
	
	-- Gear
	['fishbait'] 			     	 = {['name'] = 'fishbait', 					['label'] = 'Fish Bait', 				['weight'] = 400, 		['type'] = 'item', 		['image'] = 'fishbait.png', 			['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Fishing bait'},
	['fishingrod'] 			 		 = {['name'] = 'fishingrod', 				['label'] = 'Fishing Rod', 				['weight'] = 750, 		['type'] = 'item', 		['image'] = 'fishingrod.png', 			['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'A fishing rod for adventures with friends!!'},	
	['anchor'] 			 	 		 = {['name'] = 'anchor', 					['label'] = 'Boat Anchor', 				['weight'] = 2500, 		['type'] = 'item', 		['image'] = 'anchor.png', 				['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Boat Anchor'},	
	['fishicebox'] 			 	 	 = {['name'] = 'fishicebox', 				['label'] = 'Fishing Ice Chest', 		['weight'] = 2500, 		['type'] = 'item', 		['image'] = 'fishicebox.png', 			['unique'] = true,     ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Ice Box to store all of your fish'},	
	
	-- Rewards
	['fishingloot'] 			 	 = {['name'] = 'fishingloot', 				['label'] = 'Metal Box', 				['weight'] = 500, 		['type'] = 'item', 		['image'] = 'fishingloot.png', 			['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Seems to be a corroded from the salt water, Should be easy to open'},	
	['fishinglootbig'] 			 	 = {['name'] = 'fishinglootbig', 			['label'] = 'Treasure Chest', 			['weight'] = 2500, 		['type'] = 'item', 		['image'] = 'fishinglootbig.png', 		['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'The lock seems to be intact, Might need a key'},	
	['fishingkey'] 			 	 	 = {['name'] = 'fishingkey', 			    ['label'] = 'Corroded Key', 			['weight'] = 100, 		['type'] = 'item', 		['image'] = 'fishingkey.png', 		    ['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'A weathered key that looks usefull'},	
	['fishtacklebox'] 			 	 = {['name'] = 'fishtacklebox', 			['label'] = 'Tackle Box', 				['weight'] = 1000, 		['type'] = 'item', 		['image'] = 'fishtacklebox.png', 		['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Seems to be left over tackle box from another fisherman'},	
	['pearlscard'] 			 	 	 = {['name'] = 'pearlscard', 				['label'] = 'Pearls Seafood', 			['weight'] = 100, 		['type'] = 'item', 		['image'] = 'pearlscard.png', 			['unique'] = false,    ['useable'] = true, 	   ['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'A special member of Pearl\'s Seafood Restaurant'},	

 ``` 

# Optional (if you are not using my **[qb-inventory](https://github.com/dojwun/qb-inventory)**)
- This code is to display **[Inventory Tooltip](https://i.imgur.com/vnpIb2b.png)** 
- inside ```qb-inventory/html/js/app.js``` look for the ```function FormatItemInfo```
```
	else if (itemData.name == "bass") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "stingray") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "flounder") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "codfish") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "mackerel") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "dolphin") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "sharkhammer") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "sharktiger") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "killerwhale") {
            $(".item-info-title").html('<p>' + itemData.label + '</p>')
            $(".item-info-description").html('<p>Species: ' + itemData.info.species + '</p>Weight: ' + itemData.info.lbs + ' lbs</p>Type: ' + itemData.info.type);
        } else if (itemData.name == "fishicebox") {
            $(".item-info-title").html('<p>' + itemData.label + ' ' + itemData.info.boxid + '</p>')
            $(".item-info-description").html('<p><strong>Box Owner: </strong><span>' + itemData.info.boxOwner + '</span></p> Ice Box to store all of your fish');
        }
```  

