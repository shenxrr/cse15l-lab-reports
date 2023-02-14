Lab Report 3 - Command lind options for grep
=========

The `grep -r` command reads all files under each directory, recursively. 
---------

Source: https://en.wikibooks.org/wiki/Grep

Example 1:

`grep -r "Waikiki" ./written_2`

`./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        Waikiki, that organized tourism took hold. Steamships of the Matson
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        military base, was ruled by martial law. The Waikiki hotels housed
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        Canada, and Australia from Waikiki, millions fell under the spell of a
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        right on Waikiki Beach; Sheraton and other hotel chains followed. Among
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:        Oahu: Waikiki Beach is the tourist center of the islands,
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:        Waikiki (see page 28).
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        kitchens. Lanais afford views of the Diamond Head end of Waikiki Beach.
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.hawaiianvillage.hilton.com>. Waikiki’s larg­est resort
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Hyatt Regency Waikiki $$$–$$$$ 2424 Kalakaua Avenue,
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Head end of Waikiki’s shopping avenue (across the street from the
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        best stretches of Waikiki oceanfront, is more deluxe than most
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        the Diamond Head end of Waikiki, are a block from Kuhio Beach. Rooms
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.royal-hawaiian.com>. Waikiki’s “Pink Palace,” built by the
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        sets the tone for Waikiki’s most charming historic hotel, which opened
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Waikiki Beach, but a few steps from the heart of the Waikiki shopping
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Sheraton Waikiki $$$–$$$$ 2255 Kalakaua Avenue, Honolulu,
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        largest of Sheraton’s four Waikiki beachfront hotels, with the most`

This command searches for the string "Waikiki" in all files and directories under ./written_2.

Example 2:

`grep -r "Waikiki" --include "*.txt" ./written_2`

`./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        Waikiki, that organized tourism took hold. Steamships of the Matson
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        military base, was ruled by martial law. The Waikiki hotels housed
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        Canada, and Australia from Waikiki, millions fell under the spell of a
./written_2/travel_guides/berlitz1/HistoryHawaii.txt:        right on Waikiki Beach; Sheraton and other hotel chains followed. Among
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:        Oahu: Waikiki Beach is the tourist center of the islands,
./written_2/travel_guides/berlitz1/WhereToHawaii.txt:        Waikiki (see page 28).
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        kitchens. Lanais afford views of the Diamond Head end of Waikiki Beach.
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.hawaiianvillage.hilton.com>. Waikiki’s larg­est resort
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Hyatt Regency Waikiki $$$–$$$$ 2424 Kalakaua Avenue,
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Head end of Waikiki’s shopping avenue (across the street from the
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        best stretches of Waikiki oceanfront, is more deluxe than most
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        the Diamond Head end of Waikiki, are a block from Kuhio Beach. Rooms
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.royal-hawaiian.com>. Waikiki’s “Pink Palace,” built by the
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        sets the tone for Waikiki’s most charming historic hotel, which opened
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Waikiki Beach, but a few steps from the heart of the Waikiki shopping
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        Sheraton Waikiki $$$–$$$$ 2255 Kalakaua Avenue, Honolulu,
./written_2/travel_guides/berlitz1/HandRHawaii.txt:        largest of Sheraton’s four Waikiki beachfront hotels, with the most`

This command searches for the string "Waikiki" only in files with the .txt extension under ./written_2.

The `grep - w` command searches for the files that exactly match this word.
---------

Source: https://linuxcommand.org/lc3_man_pages/grep1.html

Example 1:

`grep -w "Honululu"  ./written_2.`

`grep: ./written_2.: No such file or directory`

It searches for the exact word 'Honululu' in all files under the ./written_2. There is no such file because I spelt the word wrong.

Example 2:

`grep -w "Honolulu" ./written_2/*`

`grep: ./written_2/non-fiction: Is a directory
grep: ./written_2/travel_guides: Is a directory`

This searches for the word "Honolulu" in all files under the ./written_2 directory. 

