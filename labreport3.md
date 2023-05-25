# **Lab Report - 3**
# **Researching Commands** 

## **Command Option 1: ```grep -c```**
The ```grep -c``` command option shows the number of lines in which a specific word appears in a file. It is used with ```-r``` to allow us to search through the files in technical. In the image below, you can see that the command prints out the name of each file that it checked and the number of lines that contain the searched word.

***Example 1:*** ```grep -c -r "world" technical```

```[cs15lsp23gv@ieng6-202]:docsearch:249$ grep -c -r "world" technical
technical/911report/chapter-1.txt:2
technical/911report/chapter-10.txt:3
technical/911report/chapter-11.txt:5
technical/911report/chapter-12.txt:44
technical/911report/chapter-13.1.txt:4
technical/911report/chapter-13.2.txt:3
technical/911report/chapter-13.3.txt:5
...
technical/plos/pmed.0020246.txt:1
technical/plos/pmed.0020247.txt:0
technical/plos/pmed.0020249.txt:0
technical/plos/pmed.0020257.txt:1
technical/plos/pmed.0020258.txt:0
technical/plos/pmed.0020268.txt:2
technical/plos/pmed.0020272.txt:0
technical/plos/pmed.0020273.txt:0
technical/plos/pmed.0020274.txt:1
technical/plos/pmed.0020275.txt:0
technical/plos/pmed.0020278.txt:0
```

In the above image, you can see that ```grep -c -r``` command goes through all th files in the directories of technical, and prints out the name of all the files along with the number of lines in which the searched string "world" appeared.

***Example 2:*** ```grep -c -r "disaster" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:250$ grep -c -r "disaster" technical
technical/911report/chapter-1.txt:0
technical/911report/chapter-10.txt:0
technical/911report/chapter-11.txt:1
technical/911report/chapter-12.txt:1
technical/911report/chapter-13.1.txt:0
technical/911report/chapter-13.2.txt:0
technical/911report/chapter-13.3.txt:0
technical/911report/chapter-13.4.txt:0
technical/911report/chapter-13.5.txt:1
technical/911report/chapter-2.txt:0
technical/911report/chapter-3.txt:1
technical/911report/chapter-5.txt:0
technical/911report/chapter-6.txt:0
technical/911report/chapter-7.txt:0
technical/911report/chapter-8.txt:0
technical/911report/chapter-9.txt:5
technical/911report/preface.txt:0
...
technical/plos/pmed.0020238.txt:0
technical/plos/pmed.0020239.txt:0
technical/plos/pmed.0020242.txt:0
technical/plos/pmed.0020246.txt:0
technical/plos/pmed.0020247.txt:0
technical/plos/pmed.0020249.txt:0
technical/plos/pmed.0020257.txt:0
technical/plos/pmed.0020258.txt:0
technical/plos/pmed.0020268.txt:0
technical/plos/pmed.0020272.txt:0
technical/plos/pmed.0020273.txt:0
technical/plos/pmed.0020274.txt:0
technical/plos/pmed.0020275.txt:0
technical/plos/pmed.0020278.txt:0
technical/plos/pmed.0020281.txt:0
```
Here, we can see that the ```grep -c -r``` command searches through all the files in technical for the string "disaster". It returns 0 for most of the files as they do not contain that string in any of the lines. But, you can see that it has returned 5 for one of the file as "disaster" must have appeared in 5 lines in that file. 

## **Command Option 2: ```grep -r```**
The ```grep -r``` command searches the directory and subdirectories for a specific string. Then, it prints out the path to the given file and the line in which the string appears.

***Example 1:*** ```grep -r "escape" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:252$ grep -r "escape" technical
technical/911report/chapter-10.txt:                narrowly escaped direct attack. Extraordinary security precautions were put in place
technical/911report/chapter-13.4.txt:                Intelligence report, interrogation of KSM, July 12, 2003. Yousef managed to escape
technical/911report/chapter-2.txt:                felt safe in Sudan, where he had already escaped at least one assassination attempt
technical/911report/chapter-3.txt:                the FISA warrants had been misused. If that had happened, Ames might have escaped
...
technical/plos/journal.pbio.0020187.txt:        year. I term this rate of reduction of age-specific mortality risk ‘actuarial escape
technical/plos/journal.pbio.0020187.txt:        The escape velocity cusp is closer than you might guess. Since we are already so long
technical/plos/journal.pbio.0020307.txt:        discovered because most viral strains escape its neutralising properties. Lentiviruses like
technical/plos/journal.pbio.0030097.txt:        profits escape from an otherwise self-contained financial cycle to satisfy shareholders or
```
In the image above, the ```grep -r``` command searches the directories and subdirectories of technical. As a result, it prints out the names of the files and the lines in which the specified string "escape" appears. We can see that the searched string is highlighted in red in the terminal.

***Example 2:*** ```grep -r "saved" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:251$ grep -r "saved" technical
technical/911report/chapter-1.txt:    NORAD officials have maintained that they would have intercepted and shot down United 93. We are not so sure. We are sure that the nation owes a debt to the passengers of United 93. Their actions saved the lives of countless others, and may have saved either the Capitol or the White House from destruction.
technical/biomed/1471-2105-3-14.txt:          chosen in a particular bootstrap sample) are saved to a
technical/biomed/1471-213X-1-11.txt:          and saved in portable network graphic format.
technical/biomed/1471-2164-2-2.txt:          alignment was saved as a PAUP file and used to generate a
technical/biomed/1471-2164-3-23.txt:        25 ] in FASTA format and saved as plain text files. The
technical/biomed/1471-2164-3-4.txt:          cutoff) was saved along with the GI number of the query
technical/biomed/1471-2164-3-9.txt:          windows, 5; diagonals saved, 5. Multiple alignment: gap
technical/biomed/1471-2199-3-3.txt:          pellet was saved as "sup". Proteins present on the beads

...
technical/government/Gen_Account_Office/d0269g.txt:resulting in approximately $578,000 in benefits saved.
technical/government/Gen_Account_Office/d0269g.txt:for themselves in terms of dollars saved. They also can be a
technical/government/Gen_Account_Office/ffm.txt:limited. One office saved $6,600 over about 33 months. This office
technical/government/Gen_Account_Office/ffm.txt:half the amount saved for the government. GSA reported that from
technical/government/Gen_Account_Office/ffm.txt:January 1995 through September 2000, almost $823,000 was saved
technical/government/Gen_Account_Office/ffm.txt:share in the savings awards. According to Justice, it saved about
technical/government/Gen_Account_Office/og97051.txt:human lives saved or the medical costs that would be avoided 
```
In Example 2, we can see that ```grep -r``` searches technical for the string "saved". As a result, it returns the name of the file and also the lines which contain the specified string.

## **Command Option 3: ```grep -l```**
The ```grep -l``` command lists the files that are found to contain the specific String. It is used in combination with ```-r``` to allow us to search through the files in technical. The output only consists of the paths to the files that contain that String. It DOES NOT list the lines that contain the String. 

***Example 1:*** ```grep -l -r "saved" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:254$ grep -l -r "saved" technical
technical/911report/chapter-1.txt
technical/biomed/1471-2105-3-14.txt
technical/biomed/1471-213X-1-11.txt
technical/biomed/1471-2164-2-2.txt
technical/biomed/1471-2164-3-23.txt
technical/biomed/1471-2164-3-4.txt
technical/biomed/1471-2164-3-9.txt

...
technical/government/Gen_Account_Office/og97051.txt
technical/government/Gen_Account_Office/og98024.txt
technical/government/Media/Avoids_Budget_Cut.txt
technical/government/Media/families_saved.txt
technical/government/Post_Rate_Comm/Mitchell_6-17-Mit.txt
technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt
technical/plos/journal.pbio.0020224.txt
technical/plos/journal.pbio.0020347.txt
technical/plos/pmed.0020247.txt
```
In the Terminal image above, the ```grep -l -r``` command gives all the directories and subdirectories of technical for "saved". 

***Example 2:*** ```grep -l -r "fire" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:255$ grep -l -r "fire" technical
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
...
technical/plos/journal.pbio.0020047.txt
technical/plos/journal.pbio.0020054.txt
technical/plos/journal.pbio.0020105.txt
technical/plos/journal.pbio.0020146.txt
technical/plos/journal.pbio.0020267.txt
technical/plos/journal.pbio.0020302.txt
technical/plos/journal.pbio.0020346.txt
technical/plos/journal.pbio.0020400.txt
technical/plos/pmed.0020208.txt
technical/plos/pmed.0020209.txt
```
Here we can see that the ```grep -l -r``` command gives all the directories and subdirectories as it did previously. All the files that contain the string "fire" are printed.

## **Command Option 4: ```grep -n```**
The ```grep -n``` command prefixes each line of output with the corresponding line number in that file. We use it in combination with ```r``` which will allow us to access all the files in technical.

***Example 1:*** ```grep -n -r "hero" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:256$ grep -n -r "hero" technical
technical/911report/chapter-13.4.txt:2294:                after the September 11 attacks as "more than heroes." FBI letterhead
technical/911report/chapter-13.5.txt:2899:                against drug warehouses and heroin laboratories." United States Institute of Peace
technical/911report/chapter-3.txt:2972:                Ahmed Shah Massoud. Reflective and charismatic, he had been one of the true heroes
technical/911report/chapter-3.txt:2975:                through trade in heroin. Nor had Massoud shown much aptitude for governing except as
technical/911report/preface.txt:92:                heroism and bravery. We have examined the staggering impact of the events of 9/11 on
...
technical/plos/pmed.0020160.txt:33:        well understood. The inflammatory response therefore not only indicates atherosclerotic
technical/plos/pmed.0020160.txt:34:        potential, but may accelerate atherosclerosis.
technical/plos/pmed.0020160.txt:82:          defined as prevalent atherosclerotic cardiovascular disease (ASCVD). Prevalent
technical/plos/pmed.0020160.txt:187:        atherosclerotic cardiovascular disease.
technical/plos/pmed.0020160.txt:276:        decline in former smokers simply indicates a prevalent underlying burden of atherosclerotic
```
In the Terminal screenshot above, we can see that the command goes through all the files in the directories and subdirectories of technical for the String "hero". As a result, it prints the paths, names, lines, and line number in the file in which the String "hero" is present.

***Example 2:***: ```grep -n -r "high" technical```
```
[cs15lsp23gv@ieng6-202]:docsearch:257$ grep -n -r "high" technical
technical/911report/chapter-1.txt:140:    At 9:32, controllers at the Dulles Terminal Radar Approach Control "observed a primary radar target tracking eastbound at a high rate of speed." This was later determined to have been Flight 77.
technical/911report/chapter-1.txt:230:    The threat of Soviet bombers diminished significantly as the Cold War ended, and the number of NORAD alert sites was reduced from its Cold War high of 26. Some within the Pentagon argued in the 1990s that the alert sites should be eliminated entirely. In an effort to preserve their mission, members of the air defense community advocated the importance of air sovereignty against emerging "asymmetric threats" to the United States: drug smuggling, "non-state and state-sponsored terrorists," and the proliferation of weapons of mass destruction and ballistic missile technology.
technical/911report/chapter-1.txt:242:Interagency Collaboration. The FAA and NORAD had developed protocols for working together in the event of a hijacking. As they existed on 9/11, the protocols for the FAA to obtain military assistance from NORAD required multiple levels of notification and approval at the highest levels of government.
...
technical/plos/pmed.0020274.txt:31:        HCoV-NL63-positive patients with high HCoV-NL63 load and absence of co-infection had croup,
technical/plos/pmed.0020274.txt:32:        compared with 6% in the HCoV-NL63-negative group. Indeed, a significantly higher fraction
technical/plos/pmed.0020274.txt:39:        However, the authors warned that the high percentage of HCoV-NL63-positive samples could
technical/plos/pmed.0020275.txt:22:        high proportion of dementia patients are thought to have a vascular component to their
technical/plos/pmed.0020278.txt:23:        injection drug users in Thailand [3] and a multinational trial of over 5,000 high-risk
technical/plos/pmed.0020278.txt:28:        imperatives dictate that no animal model, even higher primates, gives information
```
In the image above, we can see that the ```grep -n -r``` command prints the paths and names of all the files that contain the specified string. It also prints the lines and the line numbers where the String "high" is present.

