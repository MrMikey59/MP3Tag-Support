# MP3Tag Tags to Filename

Use the following examples in the Tag-Filename dialog to modify your music file names. The following examples use the following conventions:

    Track Number (2-4 digits), where the first 2 digits are the disc number
    Artist Name (if Various Artists Colletion)
    Song/Track Title
    All are separated by " - " (spaces & hyphen)
Like:  
`10 - Aerosmith - Ragdoll`  

**Note**: You must have values in each field to work properly!

### A Typical Song Title File name
```MP3Tag
$num(%track%,2) - %title%
```

### Include Disc Number with Track Number and Song Title
```MP3Tag
$num(%discnumber%,1)$num(%track%,2) - %title%
```

### Include the Artist for Various Artist Collections
```MP3Tag
$num(%track%,2) - %artist% - %title%
```

