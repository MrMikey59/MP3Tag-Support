# This is my MP3Tag Support Project

An action is the feature of Mp3Tag allows to edit tags in automatic (pre-programmed) way.  

Mp3tag is a powerful and yet easy-to-use tool to edit ID3-tags and OGG Comments of MP3- and Ogg Vorbis files. It can rename files based on the tag information, replace characters or words from tags and filenames, import/export tag information, create playlists and more. The program supports online freedb database lookups for selected files, allowing you to automatically gather proper tag information. 

**Note**: The *.mta, *.mte & *.src files are plain text files with a certain syntax, just like other programming formats.

### Media File Tags (File Extensions) Supported:
- ID3v1 (MP3)
- ID3v2 (MP3)
- APEv1 (APE)
- APEv2 (APE )
- Ogg Vorbis Comments (OGG, FLAC)
- iTunes Metadata (MP4, M4A, M4B)
- WMA (WMA)

### Find the Data
| Contents | Folder |   
| --- | --- |  
| Installed Program | `C:\Program Files (x86)\Mp3tag` <BR> `%mp3tag%` [Portable install] |  
| Error Log | `%appdata%\Mp3tag\` <BR> `%mp3tag%` [Portable install] |  
| mta (MP3Tag Action files) | `%appdata%\Mp3tag\data\actions` <BR> `%mp3tag%\actions\` [Portable install] |  
| mte (Export Files) | `%appdata%\mp3tag\exports` <BR> `%mp3tag%\Data\exports` [Portable install] |  
| src (Source Files) <br> inc (Include Files) | `%appdata%\mp3tag\data\sources` <BR> `%mp3tag%\data\sources`  [Portable install] |  

**Note**: %appdata% = “C:\Users\ %username% \AppData\Roaming\”

**Note 2**: Installtion also creates these folder wih included Actions, Exports & Sources that can include your shared files (**Warning: These could go away on the next update!**):
- `C:\Program Files (x86)\Mp3tag\data\actions`
- `C:\Program Files (x86)\Mp3tag\export`
- `C:\Program Files (x86)\Mp3tag\data\sources`

### Resources:  
- [MP3Tag Source](http://www.mp3tag.de/en/), it's support [Community](https://community.mp3tag.de/) and [Change Log](https://www.mp3tag.de/en/changelog.html). And when all else fails get [support](mailto:support@mp3tag.de) by email!
    - [Actions](https://help.mp3tag.de/options_format.html)
    - [Export Variables](http://help.mp3tag.de/options_export.html)  
    - [Scripting Language](http://help.mp3tag.de/main_scripting.html)  
-	To find more web [sources scripts](https://community.mp3tag.de/c/development/web-sources-scripts/12) for Mp3tag.  
-	To learn more about how to [use web sources scripts](https://github.com/jonaaa20/itunes-web-sources) in Mp3tag.   
-	To learn more about the [syntax of these web sources scripts](https://help.mp3tag.de/main_online.html) for Mp3tag.  
-	To learn more about the [tag fields in Mp3tag](https://help.mp3tag.de/main_tags.html).  
-	To learn more about the [XID tag field](https://community.mp3tag.de/t/support-for-itunesalbumadvisory-field/51715/10).  

### Inspirations
- https://github.com/rarestMeow/mp3tag_actions 
- https://github.com/seanap/Audible.com-Search-by-Album
- https://github.com/vibe-x/mp3tag 
- https://github.com/jerelhenderson/mp3tag_actions 
- https://github.com/tknr/mp3tag_data_sources
- https://github.com/Mp3tag/Tidier-Audio-Tag-Naming-Convention/blob/master/Releases/TAT%20Naming%20Convention%201.0.mta
- https://github.com/jonaaa20/itunes-web-sources

### Other Links:  
- [MusicBee](https://getmusicbee.com/)
- [MusicBrainz Style Guidelines](https://musicbrainz.org/doc/Style)
- RegEx: Regular Expressions  
  - [RegEx on Wikipedia](https://en.wikipedia.org/wiki/Regular_expression) 
  - [RegExOne](https://regexone.com/) 

## Filter Your View List
You can filter your view within the list using a filter.  Filters use the same functions and expressions used in all scripting within MP3Tag. 

#### Filter for Files with no Cover
```filter
%cover% = ""
```

#### Filter for no Album Artist
```filter
%albumartist% = ""
```

## MTA: MP3Tag Action File
Mp3tag provides a variety of actions, which can be applied to filenames and tags. The actions are grouped together into named sets (action groups), which can be applied independently via Actions `Alt+6`. If you do not want to create a reusable action group for applying one single action, the `Actions (Quick)` toolbar button or keyboard shortcut `Shift+Alt+6` can be used.  
You can create, edit, duplicate, and delete action groups using the buttons on the right or the context menu. The button Utils allows for saving the current selection state to a file using the `Save selection...` menu item. These are then listed in the menu and can be later restored by clicking on the configuration name. The Save menu item saves the current selection state directly (this is only necessary if you choose to not exit the dialog via the OK button).    
The Action Menu ![Action Menu](https://github.com/MrMikey59/MP3Tag-Support/blob/master/Action%20Menu.JPG)
#### Adding New Actions
1.	Download or Create a Action File
2.	Copy the .mta file to the Actions Folder
## MTE: MP3Tag Export File

#### Adding New Exports
1.	Download or Create an Export File
2.	Copy the .mte file to the Export Folder

#### Some Simple Example Exports

To use these, copy text into an empty test file and rename to an `<ExportFileName>.mte` file when saved. Now just move it to the Export folder.

###### List All Albums
```mte
$filename(ListAlbums.txt)
$loop(%artist%-%album%,1)%artist%-%album%
$loopend()
```

###### List All FLAC Albums
```mte
$filename(mp3.txt)$loop(%artist%-%album%,1)$if($eql($strstr(%_extension%,flac),0),,
%artist%-%album%
)$loopend()
```

###### List All M4A (MP4) Albums
```mte
$filename(mp3.txt)$loop(%artist%-%album%,1)$if($eql($strstr(%_extension%,m4a),0),,
%artist%-%album%
)$loopend()
```

###### List All MP3 Albums
```mte
$filename(mp3.txt)$loop(%artist%-%album%,1)$if($eql($strstr(%_extension%,mp3),0),,
%artist%-%album%
)$loopend()
```

###### List All WMA Albums
```mte
$filename(mp3.txt)$loop(%artist%-%album%,1)$if($eql($strstr(%_extension%,wma),0),,
%artist%-%album%
)$loopend()
```

## SRC: MP3Tag Source File

#### Adding New Sources
1.	Download or Create a Source File
2.	Copy the .src file to the Sources Folder

#### Use a Tag/Cover Source
1. Click on `Tag Sources`
2. Move you mouse to the selected `Source`
3. When prompted, add the `Artist name` and the `Album name` for search
4. On the Search Results, choose one on the search results.
5. The tag information will be pulled into a new dialog box with the new data on the left side and your current datat on the right side. 
6. Move the files to link with correct line, then click OK to update your files. 

## Tags
| MP3Tag Element|Description |  
| --- | --- |  
| %_directory%| Directory |  
| %_extension% | File Extension |
| %_file_create_datetime_raw%|  |  
| %_filename% | Filename without the extension |  
| %_parent_directory%| Parent Directory  |  
| %_total% | Number of tracks from xx/xx track-number field  |  
| %album%| Album Title |  
| %albumartist%| Album Artist |  
| %artist% | Track Artist |  
| %comment%| Comment |  
| %date%| Date |  
| %discnumber%| Disc Number  |  
| %dummy%| Ignore Information |  
| %genre%  | Genre  |  
| %label%| Producer Label |  
| %subtitle%| |  
| %title%| Track Title |  
| %track%| Track Number |  
| %year%| Year (Release) |  

