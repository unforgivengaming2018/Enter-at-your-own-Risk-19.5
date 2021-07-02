----------------------------------------------------------
DrsA19TraderMaterialTrade
----------------------------------------------------------
INDEX
	Thoughts
	XML changes
	Changelog
	Thanks & Credits
	
----------------------------------------------------------
Thoughts
----------------------------------------------------------
	
	dialogs.xml
		-contains the dialog that a Trader will have when interacting with them.
		-these are the selection menus that are either visible or invisible.
		-a statement id can contain a response_entry that calls to another statement id of the same name.
		-
	npc.xml 
		-contains the basic information outlining a trader, like name, name_key,Faction, portrait,gretting_type,stance,dialog_id.
		-if we end up creating a new Trader we would hook the trader_id # to the dialog_id for the appropriate dialog to take place.
	traders.xml 
		-contains 
			the item contents for the trader in question.
				inventory min and max
				min and max items to be swapped at reset interval
				reset interval
			the open and close times for the trader
	
	Add 
		blocks menu
			Bars
				woodBars
				woodBarsCentered
					resourceWood count="6"
				ironBars
				ironBarsCentered
					unit_iron count="100"
					unit_clay count="20"
				
			wet concrete
		
	Localization.txt
		*	replace MatName with truncated name
		**	replace Mat_Name with extended name
		***	material cost calculations ITEMa is material name in recipe, # is the amount of material in recipe for 1 output, 25/100/500/1000 is the final output to be multiplied by.
				25#ITEMa and 25#ITEMb
				100#ITEMa and 100#ITEMb
				500#ITEMa and 500#ITEMb
				1000#ITEMa and 1000#ITEMb

quest_MaterialTrader1_MatName,25 Mat_Name
quest_MaterialTrader1_MatName_subtitle,Collect 25#ITEMa and 25#ITEMb
quest_MaterialTrader1_MatName_description,Trade 25#ITEMa and 25#ITEMb for 25 Mat_Name.
quest_MaterialTrader2_MatName,100 Mat_Name
quest_MaterialTrader2_MatName_subtitle,Collect 100#ITEMa and 100#ITEMb
quest_MaterialTrader2_MatName_description,Trade 100#ITEMa and 100#ITEMb for 100 Mat_Name.
quest_MaterialTrader3_MatName,500 Mat_Name
quest_MaterialTrader3_MatName_subtitle,Collect 500#ITEMa and 500#ITEMb
quest_MaterialTrader3_MatName_description,Trade 500#ITEMa and 500#ITEMb for 500 Mat_Name.
quest_MaterialTrader4_MatName,1000 Mat_Name
quest_MaterialTrader4_MatName_subtitle,Collect 1000#ITEMa and 1000#ITEMb
quest_MaterialTrader4_MatName_description,Trade 1000#ITEMa and 1000#ITEMb for 1000 Mat_Name.




	quest.xml
		*	calculate material cost of the block/resourceForgedIron
		**	


	dialogs.xml
		*	add quest_name to relevant statement id's (either blocks or materials).
			statement id="25_blocks"
			statement id="25_materials"
			statement id="100_blocks"
			statement id="100_materials"
			statement id="500_blocks"
			statement id="500_materials"
			statement id="1000_blocks"
			statement id="1000_materials"
			


	
----------------------------------------------------------
XML changes
----------------------------------------------------------
	BLOCKS
		ADDED


		CHANGED


	BLOCKPLACEHOLDERS
		ADDED
		
		
		CHANGED


	ITEMS
		ADDED

			
		CHANGED


	ITEM_MODIFIERS
		ADDED
		
		
		CHANGED
		

	LOOT
		ADDED
			
		CHANGED			


	PROGRESSION
		ADDED
		
		
		CHANGED			

			
	RECIPES
		ADDED

			
		CHANGED
			
			
	QUESTS
		ADDED

materialTrades
	trade_blocks 100
	trade_blocks 500
	trade_blocks 1000
		flagstone
		wetconcrete
		rebar
	trade_materials 100
	trade_materials 500
	trade_materials 1000
		cobblestone
		concrete mix
		cement
		resourceForgedIron
		resourceForgedSteel


			
		CHANGED

			
	XUi
		WINDOWS

				
----------------------------------------------------------
Changelog
----------------------------------------------------------

001
	-


	
----------------------------------------------------------
Thanks & Credits
----------------------------------------------------------
	From the time I started playing 7 days to die in a17 I started to use mods to slowly adapt the game towards a style I wanted. This lept me into looking at making changes to the xml myself. 
		-Jrbarrio was the first person that got me into the xml and after that I was hooked.
		-Stallionsdens had the greatest impact on my games in regards to the mining and raincatcher as well as all the pallet and shelving becoming lootable. The mining machine became the basis of my oil and gas mod.
		-Mayic/Jayic had the single most impact in actually formulating correct xml and for giving me a home on discord. It always amazed me the wizardry that would ensue when putting a query to him that he didn't know, within hours a full investigation of the xml would have happened on his end and he would end up returning with a certain answer about the query.
		-Stasis was a tremendous wealth of knowledge when it came to xml and ideas. Discussing ideas and xml with him was always fruitful.
		-Xyth's tutorials were indespensable for my power series 1 mod and without those that mod never would have happened. Having a chance to create the upgrade path and damage amounts for his lootable steel bars mod was an honour.
	








