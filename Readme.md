# This is my MP3Tag Support Project

#### Find the Data
| Contents | Folder |   
| --- | --- |  
| Installed Program | `C:\Program Files (x86)\Mp3tag` <BR> `%mp3tag%` [Portable install] |  
| Error Log | `%appdata%\Mp3tag\` <BR> `%mp3tag%` [Portable install] |  
| mta (MP3Tag Action files) | `%appdata%\Mp3tag\export` <BR> `%mp3tag%\export\` [Portable install] |  
| mte (Export Files) | `%appdata%\mp3tag\data\sources` <BR> `%mp3tag%\Data\Sources` [Portable install] |  
| src (Source Files) <br> inc (Include Files) | `%appdata%\mp3tag\data\actions` <BR> `%mp3tag%\Data\Actions`  [Portable install] |  

**Note**: %appdata% = “C:\Users\ %username% \AppData\Roaming\”

**Note 2**: Installtion also creates these folder wih included Actions, Exports & Sources that can include your shared files:
- `C:\Program Files (x86)\Mp3tag\data\actions`
- `C:\Program Files (x86)\Mp3tag\export`
- `C:\Program Files (x86)\Mp3tag\data\sources`

#### Resources:  
-	To find more web [sources scripts](https://community.mp3tag.de/c/development/web-sources-scripts/12) for Mp3tag.  
-	To learn more about how to [use web sources scripts](https://github.com/jonaaa20/itunes-web-sources) in Mp3tag.   
-	To learn more about the [syntax of these web sources scripts](https://help.mp3tag.de/main_online.html) for Mp3tag.  
-	To learn more about the [tag fields in Mp3tag](https://help.mp3tag.de/main_tags.html).  
-	To learn more about the [XID tag field](https://community.mp3tag.de/t/support-for-itunesalbumadvisory-field/51715/10).  

#### Inspirations
- https://github.com/rarestMeow/mp3tag_actions 
- https://github.com/seanap/Audible.com-Search-by-Album
- https://github.com/vibe-x/mp3tag 
- https://github.com/jerelhenderson/mp3tag_actions 
- https://github.com/tknr/mp3tag_data_sources
- https://github.com/Mp3tag/Tidier-Audio-Tag-Naming-Convention/blob/master/Releases/TAT%20Naming%20Convention%201.0.mta

## MTA: MP3Tag Action File

## MTE: MP3Tag Export File

## SRC: MP3Tag Source File

## Tags
| MP3Tag Element|Description |  
| --- | --- |  
| %_directory%|Directory |  
| %_file_create_datetime_raw%| |  
| %_parent_directory%|Parent Directory  |  
| %albumartist%|Album Artist |  
| %comment%|Comment |  
| %date%|Date |  
| %discnumber%|Disc Number  |  
| %dummy%| |  
| %label%|Producer Label |  
| %subtitle%| |  
| %title%|Title |  
| %track%|Track Number |  
| %year%|Year (Release) |  

