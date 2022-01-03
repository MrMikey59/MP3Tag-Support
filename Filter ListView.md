# MP3Tag Filter List View

Open & close the Filter using `F3`  

| Action | Filter |  
| --- | --- |  
| All files without tags | %_tag% IS "" |  
| Files with flac and ID3v2 tags | %_tag% HAS "flac id3v2" |  
| Files with mp4 extension | %_extension% IS mp4 |  
| All files with a bitrate over 180 | %_bitrate% GREATER 180 |  
| All files with embedded covers over 20 kbyte | %_cover_size% GREATER 20480 |  

