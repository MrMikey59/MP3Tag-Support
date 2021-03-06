# MP3Tag Actions

Some **Actions** are numbered in accordance to the tags they affect. Changing either of these number orders will result in tagging errors.

**Note** When adding new actions, restarting MP3Tag is not necessay!

#### Add Order to the Action Menu
You can make **Menu Breakouts** by catagory using the # symbol in the names.  
For example, the following file name creates a double breakout menu with **Grammatron** and the **Smart Case and Grammar Restorer** before the action is available to click:
```
Grammartron#Smart Case and Grammar Restorer #1 - Tags.mta
```
Action Menu Breakout: ![Action Menu Breakout](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Actions/Actions%20Menu%20Breakout.JPG)  

Use comments to documwent your action. Add comments in the file script using the !.
```mta
! This is my comment.
```

#### Add Keyboard Short cuts to Actions
You can use the keyboard shortcut to trigger the action group menu `Alt+A` in combination with another character from the action group name. Simply decide on the character and prefix it with &. You can then use Alt+A and the character to trigger the action group.

An example action group `&Uppercase` can be triggered by `Alt+A` plus `U`.

### Add Spaces Around Dashes
This action adds spaces around the dashes in the File Name and then eliminate extra spaces when necessary.   
Here's how it looks when creating:   
![Create an Action](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Actions/Create%20Action.JPG)

And how the code looks in the file:  
```mta
[#0]
! Add spaces around all dashes.
T=2
F=_FILENAME
1=-
2= - 
3=0|0

[#1]
! Remove extra spaces.
T=2
F=_FILENAME
1=  
2= 
3=0|0
```

### Grammar
[Grammar](https://community.mp3tag.de/t/case-conversion/11684) is a comprehensive, collective effort among the
MP3TAG community to format, fix and standardize spellings and grammatical issues in music tags.  
- Grammar#Smart Case and Grammar Restorer #1 - Tags.mta  
- Grammar#Smart Case and Grammar Restorer #2 - Filenames.mta  
- Grammar#Smart Case and Grammar Restorer #3 - Parent Directory.mta  
- Grammar#Xtra Naming and Style Corrections.mta  
  - naming and grammatical style corrections not included in Grammartron's 3 Smart Case and Grammar Restorers.

### Remove Double Spaces
This is my first Action Creation. Use it to remove extra spaces in all tags. This may need to run more than once to clear all extra spaces!

### Standard (Included in MP3Tag)
This action standardizes all tags replacing:
- %20 with space  
- Underscore with space
- and a few corrections for `DJ`, `Feat`, `MC` & `vs`.
```
Replace "_ALL": "%20" -> " "
Replace "_ALL": "_" -> " "
Replace "_ALL": "Dj" -> "DJ"
Replace "_ALL": "Feat" -> "feat" 
Replace "_ALL": "Mc" -> "MC" 
Replace "_ALL": "Vs" "vs" 
```

### Track counters
- Track Counter #1 - Track Number.mta  
  - prepend incrementing track numbers to total file number
- Track Counter #2 - Track Total.mta  
	- append total file count to track numbers
- Track Counter #3 - Both.mta  
	- increment track numbers and appending total file count
- Track Counter #4 - Vinyl (Letters).mta  
	- increment vinyl-style track numbers (A01... B01...), set DISCSUBTITLE to "Side A... Side B..."
- Track Counter #5 - Vinyl (Numbers).mta 
	- set DISCSUBTITLE to "Side 1... Side 2..."  

For Track Number Reverse Engineering, go to Actions, Select Track Update and Edit. Here's the process:  
![Track Update Script](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Actions/Track%20Number.JPG)

and the file:
```mta
[#0]
T=5
1=$num($add(%_counter%,),2)
F=TRACK
```

