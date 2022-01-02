# MP3Tag Actions

Some **Actions** are numbered in accordance to the tags they affect. Changing either of these number orders will result in tagging errors.

**Note** When adding new actions, restarting MP3Tag is not necessay!

### Grammartron
[Grammartron](https://community.mp3tag.de/t/case-conversion/11684) is a comprehensive, collective effort among the
MP3TAG community to format, fix and standardize spellings and grammatical issues in music tags.  
- 01 Grammartron - Smart Case and Grammar Restorer #1 - Tags.mta  
- 01 Grammartron - Smart Case and Grammar Restorer #2 - Filenames.mta  
- 01 Grammartron - Smart Case and Grammar Restorer #3 - Parent Directory.mta  

You can make **Menu Breakouts** by catagory using the # symbol in the names.  
For example, the following file name creates a double breakout menu with **Grammatron** and the **Smart Case and Grammar Restorer** before the action is available to click:
```
Grammartron#Smart Case and Grammar Restorer #1 - Tags.mta
```
Action Menu Breakout: ![Action Menu Breakout](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Actions/Actions%20Menu%20Breakout.JPG)

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

