##   BASH SCRIPT - FFMpeg Automated MP4 Encoding / Folder Queuing  ##
Author - Brady Shea - bshea(at)holylinux.net

0. Prereq's

a. FFMPEG -> with x264/faad support (Static or Shared compile)
         (ubuntu - http://ubuntuforums.org/showthread.php?t=786095)
         (WARNING:
          You may be breaking law in your country enabling these features!)

b. QT-FASTSTART (May be commented out if not needed.
                 Used for streaming purposes to prep final file)

c. MPLAYER (vidinfo script only - See LICENSE)

#### Installation ####

1. Untar. "tar xvf bffmp4.tar.gz"
2. Check owner/permissions - "bffmp4" should be 0755 (as well as others)
3. Edit the 'bffmp4' script variables/sizes to what you need.
4. execute:

      ./bffmp4 &

             (or to 'detach' from session:)

      nohup ./bffmp4 &

  (nohup shouldn't necessary unless logging out.)

#### NOTES ####

Directories should be auto created on first run.

Copy (or Drag & Drop) most any video file into 'QUEUE' dir.

Completed Files will eventually appear in 'COMPLETED' dir.

Default resolutions (all sizes should be divisable by 16 if possible):

1280x720 (VBR 2-Pass hd720 for smaller file).
960x544  (CBR Encoding)
640x368  (CBR Encoding)
160x96   (CBR Encoding)
130x96   (Padded JPG capture of frame. Adjust timecode if needed)

You can monitor via log file 'encode.log' or watchprocess shell script.
Other utilities are included and should be self-explanatory by running them.

------------------------------------------------------------------------------
11AUG2011

