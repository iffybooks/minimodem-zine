# Turning Data into Sound and Back

text only for this guide

## Make a text file

## Text to sound at 100 baud

```
cat input_file.txt | minimodem --write 100 -f modem_audio.wav
```

Find the WAV file you just created in the file explorer. To play it back, right-click the file and open it with VLC.

## Text to sound at 5 baud

```
cat input_file.txt | minimodem --write 5 -f modem_audio.wav
```

Find the WAV file you just created in the file explorer. To play it back, right-click the file and open it with VLC.

## More minimodem options

Run the following command to see a list of options for minimodem:

```
minimodem --help
```

## Sound to tape

Plug an audio cable into your computer's headphone output and connect the other side to the "line in" port on your tape recorder.

Make sure your tape recorder is set to "tape" mode. Insert a tape and rewind to the beginning.

Press record on your tape recorder.

In the file explorer, find the audio file you want to record. To play it, right-click the file and open it with VLC.

## Tape to screen

## Audio file to data

## Convert an image file to base64 text

```
base64 photo.jpg > photo_base64.txt
```

## Check the size of a file

```
du -h photo_base64.txt 
```

## Image file to ASCII art (b&w)

Convert an image to ASCII art from the command line:

```
ascii-image-converter -d 80,50 photo.jpg > photo.txt
```

Use an alternate color setting:

```
ascii-image-converter -d 80,50 -c photo.jpg > photo.txt
```

## Image file to ASCII art (color)

<div style="page-break-after: always;"></div>

```
ascii-image-converter -d 80,50 -C photo.jpg > photo.txt
```

Alternate color setting:

```
ascii-image-converter -d 80,50 -c -C photo.jpg > photo.txt
```

## Movie to frames with ffmpeg

Download video:

```
yt-dlp "http://video_url.com/1339482883"
```

Extract 1 frame per second to jpeg files:

```
ffmpeg -i "video_file.webm" -vf fps=1/1 img%03d.jpg
```

<div style="page-break-after: always;"></div>

<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />

<img src="images/453eacede0b6ddf49a2ebc7bb7bad9b852f26d35.png" title="" alt="Ditto_pin_v3.png" width="95">

**Anti-copyright 2023**

**iffybooks.net**

<br />
<br />

**Iffy Books**&nbsp;

**319 N. 11th St. #2I, PHL**
