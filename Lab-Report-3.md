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

The `grep -e` command searches for patterns in files and directories under the directory
---------
Source: https://chat.openai.com/chat

Example 1:

`grep -e "lagoons" ./written_2/*`

`grep: ./written_2/non-fiction: Is a directory
grep: ./written_2/travel_guides: Is a directory`

This command searches for the string "lagoon" in all files under the "written_2" directory and prints the lines that match.

Example 2:

`grep -e "lagoons" ./written_2/*.txt`

`grep: ./written_2/*.txt: No such file or directory`

This command searches for the string "lagoons" in all text files under the "written_2" directory and prints the lines that match.

The `grep -n` command searches for the prefix each line of output with the line number within its input file.
---------
Source: https://chat.openai.com/chat

Example 1:

`grep -n "Honolulu" ./written_2/travel_guides/berlitz1/HandRHawaii.txt`

`6:        Oahu (Including Honolulu)
7:        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
13:        Halekulani $$$$ 2199 Kalia Road, Honolulu, HI 96815; Tel.
21:        Hilton Hawaiian Village $$$–$$$$ 2005 Kalia Road, Honolulu,
29:        Honolulu, HI 96815; Tel. (808) 923-1234 or (800) 233-1234; fax (808)
40:        half-hour drive of Honolulu. 387 rooms.
42:        Honolulu, HI 96816; Tel. (808) 739-8888 or (800) 367-2525; fax (808)
48:        Outrigger Reef $$$ 2169 Kalia Road, Honolulu, HI 96815; Tel.
54:        Pacific Beach Hotel $$$ 2490 Kalakaua Avenue,, Honolulu, HI
59:        Royal Hawaiian $$$$ 2259 Kalakaua Avenue, Honolulu, HI
65:        Honolulu, HI 96815; Tel. (808) 922-3111 or (800) 325-3535; fax (808)
74:        Honolulu, HI 96815; Tel. (808) 922-5811 or (800) 325-3535; fax (808)
79:        Sheraton Waikiki $$$–$$$$ 2255 Kalakaua Avenue, Honolulu,
`

This command will search for the Honululu in all files and directories under ./written_2 and will print each matching line along with its line number and the name of the file or directory it was found in.

Example 2:

`grep -n "(808) 922-1233" ./written_2/travel_guides/berlitz1/HandRHawaii.txt`

`55:        96815; Tel. (808) 922-1233 or (800) 367-6060; fax (808) 922-0129;`

This command will search for (808) 922-1233 in all files and directories under ./written_2 and will print each matching line along with its line number and the name of the file or directory it was found in.
