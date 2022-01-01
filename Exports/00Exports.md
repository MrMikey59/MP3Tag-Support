# MP3Tag Exports

### Basic List for Artists by Album and Track List
```mte
$filename(%artist%.txt,utf-8)%artist%
List created %_datetime%
 
Albums
======
$loop(%album%,1) %_counter% - %album%  -  %year%  -  %genre%
$loopend()
 
Album Track Lists
=============
$loop(%album%)%album%  -  %year%  -  %genre%
------------------------------------------
$loop(%_path%) %track%  -  %title% ($replace(%_codec%,MPEG 1 Layer III,MP3) @ %_bitrate% %_vbr%)
$loopend()
$loopend()
```

