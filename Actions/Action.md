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

### Add Spaces Around Dashes
This action adds spaces around the dashes and then eliminates extra spaces when necessary.
Here's how it looks when creating: ![Create an Action](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Actions/Create%20Action.JPG)

### Grammar
[Grammar](https://community.mp3tag.de/t/case-conversion/11684) is a comprehensive, collective effort among the
MP3TAG community to format, fix and standardize spellings and grammatical issues in music tags.  
- Grammar#Smart Case and Grammar Restorer #1 - Tags.mta  
- Grammar#Smart Case and Grammar Restorer #2 - Filenames.mta  
- Grammar#Smart Case and Grammar Restorer #3 - Parent Directory.mta  
- Grammar#Xtra Naming and Style Corrections.mta  
  - naming and grammatical style corrections not included in Grammartron's 3 Smart Case and Grammar Restorers.

### Remove Double Spaces
This is my first Action Creation. Use it to remove extra spaces in all tags.

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

