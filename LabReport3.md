# Some Command Options for 'find'
by Stephanie Frianeza

Source: ChatGPT https://chat.openai.com/chat

---
## Option 1: -name
*Description: Searches for files and directories with a specified name. 
For example, to search for files named "ch7.txt" in the current directory, you can use the command find . -name "ch7.txt".*

> Example 1:

The command
```
find -name Algarve-History.txt
```
yields
```
./travel_guides/berlitz2/Algarve-History.txt
```
**This command searches for the Algarve-History.txt file in the directory written_2 and prints out its path. It's useful for identifying the path of any file.**
> Example 2:

The command
```
find -name "chM.txt"
```
yields
```
./non-fiction/OUP/Castro/chM.txt
```
**This command searches for the chM.txt file in the directory written_2 and prints out its path. It's useful for identifying the path of any file.**

---

## Option 2: -iname
*Description: Same as -name, but case-insensitive.*

> Example 1:

The command
```
find -iname chm.txt
```
yields
```
./non-fiction/OUP/Castro/chM.txt
```
**This command finds a file (case-insensitive) within the directory and outputs its path. It's useful for identifying the path of any file without having to worry about exact spelling of the file.**
> Example 2:

The command
```
find -iname handrisrael.txt
```
yields
```
./travel_guides/berlitz1/HandRIsrael.txt
```
**This command finds a file (case-insensitive) within the directory and outputs its path. It's useful for identifying the path of any file without having to worry about exact spelling of the file.**

---
## Option 3: -name -print
*Description: Display the names of the files and directories that match the search criteria. For example, find . -name "*.txt" -print.*

> Example 1:

The command
```
find -name "ch*.txt" -print
```
yields
```
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
./non-fiction/OUP/Castro/chL.txt
./non-fiction/OUP/Castro/chM.txt
./non-fiction/OUP/Castro/chN.txt
./non-fiction/OUP/Castro/chO.txt
./non-fiction/OUP/Castro/chP.txt
./non-fiction/OUP/Castro/chQ.txt
./non-fiction/OUP/Castro/chR.txt
./non-fiction/OUP/Castro/chV.txt
./non-fiction/OUP/Castro/chW.txt
./non-fiction/OUP/Castro/chY.txt
./non-fiction/OUP/Castro/chZ.txt
./non-fiction/OUP/Fletcher/ch1.txt
./non-fiction/OUP/Fletcher/ch10.txt
./non-fiction/OUP/Fletcher/ch2.txt
./non-fiction/OUP/Fletcher/ch5.txt
./non-fiction/OUP/Fletcher/ch6.txt
./non-fiction/OUP/Fletcher/ch9.txt
./non-fiction/OUP/Kauffman/ch1.txt
./non-fiction/OUP/Kauffman/ch10.txt
./non-fiction/OUP/Kauffman/ch3.txt
./non-fiction/OUP/Kauffman/ch4.txt
./non-fiction/OUP/Kauffman/ch5.txt
./non-fiction/OUP/Kauffman/ch6.txt
./non-fiction/OUP/Kauffman/ch7.txt
./non-fiction/OUP/Kauffman/ch8.txt
./non-fiction/OUP/Kauffman/ch9.txt
./non-fiction/OUP/Rybczynski/ch1.txt
./non-fiction/OUP/Rybczynski/ch2.txt
./non-fiction/OUP/Rybczynski/ch3.txt
```
**All text files with the prefix "ch" in the directory are outputted with their paths.**
> Example 2:

The command
```
find -name "HandRHawaii.txt" -print
```
yields
```
./travel_guides/berlitz1/HandRHawaii.txt
```
**This command is useful for printing the path of any file.**

---
## Option 4: -name -ls
*Description: Display information about the files and directories in the long format, similar to the ls -l command.*

> Example 1:

The command
```
find -name "ch*.txt" -ls 
```
yields
```
204832549   52 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    46915 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch1.txt
204832550   44 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    39905 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch14.txt
204832551   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    43918 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch15.txt
204832552   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    44782 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch2.txt
204832553   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    35141 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch3.txt
204832554   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    42225 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch6.txt
204832555   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    42444 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch7.txt
204832556   56 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    52468 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch8.txt
204832557   36 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    31283 Feb  6 13:14 ./non-fiction/OUP/Abernathy/ch9.txt
204832560   96 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    92355 Feb  6 13:14 ./non-fiction/OUP/Berk/ch1.txt
204832561  108 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23   102942 Feb  6 13:14 ./non-fiction/OUP/Berk/ch2.txt
204832562   72 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    66887 Feb  6 13:14 ./non-fiction/OUP/Berk/ch7.txt
204832564   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    35675 Feb  6 13:14 ./non-fiction/OUP/Castro/chA.txt
204832565   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    32819 Feb  6 13:14 ./non-fiction/OUP/Castro/chB.txt
204832566   28 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    23635 Feb  6 13:14 ./non-fiction/OUP/Castro/chC.txt
204832567   28 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    24476 Feb  6 13:14 ./non-fiction/OUP/Castro/chL.txt
204832568   60 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    55410 Feb  6 13:14 ./non-fiction/OUP/Castro/chM.txt
204832569   12 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     9182 Feb  6 13:14 ./non-fiction/OUP/Castro/chN.txt
204832570   12 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     8349 Feb  6 13:14 ./non-fiction/OUP/Castro/chO.txt
204832571   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    41470 Feb  6 13:14 ./non-fiction/OUP/Castro/chP.txt
204832572   12 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     8274 Feb  6 13:14 ./non-fiction/OUP/Castro/chQ.txt
204832573   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    33420 Feb  6 13:14 ./non-fiction/OUP/Castro/chR.txt
204832574   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    19909 Feb  6 13:14 ./non-fiction/OUP/Castro/chV.txt
204832575    8 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     6724 Feb  6 13:14 ./non-fiction/OUP/Castro/chW.txt
204832576    8 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     5424 Feb  6 13:14 ./non-fiction/OUP/Castro/chY.txt
204832577    8 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23     5431 Feb  6 13:14 ./non-fiction/OUP/Castro/chZ.txt
204832579   52 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    46376 Feb  6 13:14 ./non-fiction/OUP/Fletcher/ch1.txt
b  6 13:14 ./non-fiction/OUP/Kauffman/ch4.txt
204832945   32 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    27196 Feb  6 13:14 ./non-fiction/OUP/Kauffman/ch5.txt
204832946   68 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    61513 Feb  6 13:14 ./non-fiction/OUP/Kauffman/ch6.txt
204832947   56 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    50095 Feb  6 13:14 ./non-fiction/OUP/Kauffman/ch7.txt
204832948  104 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    99145 Feb  6 13:14 ./non-fiction/OUP/Kauffman/ch8.txt
204832949   92 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    86220 Feb  6 13:14 ./non-fiction/OUP/Kauffman/ch9.txt
204832951   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    34412 Feb  6 13:14 ./non-fiction/OUP/Rybczynski/ch1.txt
204832952   44 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    38052 Feb  6 13:14 ./non-fiction/OUP/Rybczynski/ch2.txt
204832953   56 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    52179 Feb  6 13:14 ./non-fiction/OUP/Rybczynski/ch3.txt
```
**This command printed out information in the long format for all .txt files with the prefix "ch" inside the directory.**
> Example 2:

The command
```
find -name "History*.txt" -ls 
```
yields
```
204832970   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    15962 Feb  6 13:14 ./travel_guides/berlitz1/HistoryDublin.txt
204832971   28 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    21027 Feb  6 13:14 ./travel_guides/berlitz1/HistoryEdinburgh.txt
204832972   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    18298 Feb  6 13:14 ./travel_guides/berlitz1/HistoryEgypt.txt
204832973   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    15011 Feb  6 13:14 ./travel_guides/berlitz1/HistoryFWI.txt
204832974   44 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    38509 Feb  6 13:14 ./travel_guides/berlitz1/HistoryFrance.txt
204832975   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    18666 Feb  6 13:14 ./travel_guides/berlitz1/HistoryGreek.txt
204832976   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    16522 Feb  6 13:14 ./travel_guides/berlitz1/HistoryHawaii.txt
204832977   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    14614 Feb  6 13:14 ./travel_guides/berlitz1/HistoryHongKong.txt
204832978   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    12703 Feb  6 13:14 ./travel_guides/berlitz1/HistoryIbiza.txt
204832979   60 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    54898 Feb  6 13:14 ./travel_guides/berlitz1/HistoryIndia.txt
204832980   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    16573 Feb  6 13:14 ./travel_guides/berlitz1/HistoryIsrael.txt
204832981   32 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    27099 Feb  6 13:14 ./travel_guides/berlitz1/HistoryIstanbul.txt
204832982   52 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    48191 Feb  6 13:14 ./travel_guides/berlitz1/HistoryItaly.txt
204832983   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    17168 Feb  6 13:14 ./travel_guides/berlitz1/HistoryJamaica.txt
204832984   48 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    41789 Feb  6 13:14 ./travel_guides/berlitz1/HistoryJapan.txt
204832985   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    18491 Feb  6 13:14 ./travel_guides/berlitz1/HistoryJerusalem.txt
204832986   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    13596 Feb  6 13:14 ./travel_guides/berlitz1/HistoryLakeDistrict.txt
204832987   20 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    18968 Feb  6 13:14 ./travel_guides/berlitz1/HistoryLasVegas.txt
204832988   12 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    11857 Feb  6 13:14 ./travel_guides/berlitz1/HistoryMadeira.txt
204832989   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    12519 Feb  6 13:14 ./travel_guides/berlitz1/HistoryMadrid.txt
204832990   40 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    35725 Feb  6 13:14 ./travel_guides/berlitz1/HistoryMalaysia.txt
204832991   16 -rwxr-x---   1 cs15lwi23agp ieng6_cs15lwi23    13730 Feb  6 13:14 ./travel_guides/berlitz1/HistoryMallorca.txt
```
**This command printed out information in the long format of all .txt files in the directory starting with the word "History".**
