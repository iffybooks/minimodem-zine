<img title="" src="images/ade32cf7d73fefcf9bb6089d50b370b8b91eeabd.png" alt="Minimodem_Zine_Cover.png" data-align="center" width="474">

<div style="page-break-after: always;"></div>

# Turning Data into Sound and Back with Minimodem

At 100 baud, 17 KB of data is equivalent to roughly half an hour (one side of a 60-minute cassette tape).

For this workshop we'll only be working with plaintext data.

## Make a text file

❏ Open Sublime Text or a similar plaintext editor. Write a few lines of text, or paste in some text from the web.

❏ Save your file to the desktop with a name like `text_file.txt`.

## Open a terminal window and cd to the Desktop

❏ Open a new terminal window. In Ubuntu you can press `ctrl + alt + t`.

❏ Enter the following command to change your working diretory to the desktop:

```
cd ~/Desktop
```

<div style="page-break-after: always;"></div>

## Convert text to sound at 100 baud

❏ Run the following command, substituting the name of your text file if it's different. The "|" character is called a pipe; you can find it above the backslash on your keyboard.

```
cat text_file.txt | minimodem --write 100 -f modem_audio.wav
```

In the file explorer, find the WAV file you just created. To play it back, right-click the file and open it with VLC.

## Text to sound at 5 baud

❏ Run the following command to convert your file to audio at 5 baud. That's slow! Make sure your input file is small, or this will create a huge audio file.

```
cat input_file.txt | minimodem --write 5 -f modem_audio.wav
```

In the file explorer, find the WAV file you just created. To play it back, right-click the file and open it with VLC.

<div style="page-break-after: always;"></div>

## More minimodem options

Run the following command to see a list of options for minimodem:

```
minimodem --help
```

## Sound to tape

❏ Plug an audio cable into your computer's headphone output and connect the other side to the "line in" port on your tape recorder.

❏ Make sure your tape recorder is set to "tape" mode. Insert a tape and rewind to the beginning.

❏ Press record on your tape recorder.

❏ In the file explorer, find the audio file you want to record. To play it, right-click the file and open it with VLC.

## Tape to screen

❏ Plug an audio cable into your tape player's headphone output and connect the other side to the microphone input on your computer.

❏ In a terminal window, run the following command to receive data at 100 baud. The `-q` option means "quiet," which tells minimodem not to output unncessary text.

```
minimodem --rx 100 -q
```

❏ Press play on your tape player. After a few seconds you should see text start appearing in the terminal window. 

If you don't see anything onscreen or the output is jumbled, try adjusting the tape player's volume up and down until it looks right.

## Quit Minimodem

❏ To stop displaying text onscreen, press `ctrl + c`. 

❏ To clear the terminal window, run the `clear` command.

```
clear
```

<div style="page-break-after: always;"></div>

## Modem audio file to text file

If you want to convert an audio file containing modem audio directly to a text file, you can use a command like the one below. The file `modem_audio.wav` is a WAV audio file containing text data encoded at 100 baud. This command will write the text to a new file called `output_file.txt`.

```
minimodem --rx 100 -q --file modem_audio.wav > output_file.txt
```

## Convert an image file to base64 text

❏ To store an image on a cassette tape, you may want to convert it to the text-based base64 format beforehand. You'll want to use a small image file, and store the data several times in case it gets corrupted. 

```
base64 photo.jpg > photo_base64.txt
```

<div style="page-break-after: always;"></div>

## Check the size of a file

❏ You can use the `du` command to check how much disk space is being used by a file.

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

```
ascii-image-converter -d 80,50 -C photo.jpg > photo.txt
```

<div style="page-break-after: always;"></div>

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

<img src="images/1297802d662a37d2e50f8226a98a834411a74a06.png" title="" alt="Ditto_pin_v3.png" width="116">

**Anti-copyright 2023**

<br />
<br />

### Iffy Books&nbsp;

**319 N. 11th St. #2I, PHL**

**iffybooks.net**

<br />

**Many thanks to our supporters!**<br />
**https://iffybooks.net/donate**
