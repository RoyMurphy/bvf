# Bitcoin Video File

BVF is a Lossless Video Codec designed for maximum file size reduction for on-chain video streaming.

Bitcoin Video File is a highly optimized fork of the latest FFMPEG cross-platform solution to record, convert and stream audio and video. The target scripts are optimized for maximum lossless audio and video conversion to pre-process and compress all video and audio streams into the most efficient package. These use the very latest libaom, Opus, and M3U8 libraries and AV1 compression algorithms.

## How to use the BVF codec

Use the above BVF script to optimize your videos. Edit the reference and output files to your filename and desired path. Retain the final .webm file type to output the optimized BVF codecs. Either use the standalone script above and use your own FFMPEG build of choice, or download the official build which also contains the latest BVF scripts.

## Installation (Windows)

Go to Step 2 at https://phoenixnap.com/kb/ffmpeg-windows

## Installation (MacOS)

Go to Step 2 at https://phoenixnap.com/kb/ffmpeg-mac

## Installation (Linux)

See https://phoenixnap.com/kb/install-ffmpeg-ubuntu

## Resources

### FFMPEG Documentation

https://ffmpeg.org/ffmpeg.html

### FFMPEG Formats

https://ffmpeg.org/ffmpeg-formats.html

### Encode AV1

https://trac.ffmpeg.org/wiki/Encode/AV1

## How To Set Up

The BVF file should suit all kinds of videos. Both video and audio have been highly optimized out of the box. However, you might want to play around with a few fields, so there are some variables you need to know. To run the script, use either CMD prompt or Windows Powershell to begin pre-processing. See resourses above for all of the variables.

### Variables

-crf is the target frame rate. This is set to 0 for lossless compression, but takes longer to process. The range is from 0-63. A crf value of 63 will give the best final compressed file size. A crf of 23 is imperceptably lossless. The lower the value, the longer it takes to encode. Find a happy medium.

-cpu-used is the number of threads used to contiguously encode the file. Higher is quicker. Lower is higher fidelity. Values range from 0-10. Values above 8 (inclusive) require the flag -usage realtime, which speeds up encoding greatly as it's designed for live streaming/broadcasting. However, quality is greatly reduced. Please see https://trac.ffmpeg.org/wiki/Encode/AV1 for more information.

-b:a 48k is the default audio parameter defined in the BVF as it's a good quality, acceptable bitrate for most videos. Consider changing settings to 96k or 128k for higher quality sound definition. Only required for music videos with higher dynamic range. For most videos, the standard setting is perfectly acceptable to most ears.
