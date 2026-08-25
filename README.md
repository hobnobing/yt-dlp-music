# yt-dlp-music

Simple [yt-dlp](https://github.com/yt-dlp/yt-dlp) bash script that formats all audio to FLAC and automatically adds song metadata, including cover art. For GUI frontend see [yt-dlp-music-gui](https://github.com/romululz/yt-dlp-music-gui).


<img width="800" height="542" alt="ezgif-36f1ab6b1e465c15" src="https://github.com/user-attachments/assets/49be6afb-39f9-436d-b520-229df0c4144b" />


### Dependencies

Arch
```
sudo pacman -S --needed yt-dlp ffmpeg python-mutagen git wget imagemagick flac nodejs
```

### Cookies shenanigans

You need to export your YouTube cookies to use as authentification.
Use the "Get cookies.txt LOCALLY" extension. 
Go to ```https://www.youtube.com``` click the extension, "Export As", save as cookies.txt.

Then make this new directory and move cookies.txt to it.
```
mkdir -p ~/.config/yt-dlp
mv ~/Downloads/cookies.txt ~/.config/yt-dlp/cookies.txt
```

### Installation

```
mkdir -p ~/.local/bin
git clone https://github.com/hobnobing/yt-dlp-music.git
mv ~/yt-dlp-music/yt-dlp-music ~/.local/bin/
rm -rf ~/yt-dlp-music
chmod +x ~/.local/bin/yt-dlp-music
```



The script uses ```yt-dlp``` to download the audio as FLAC along with its thumbnail. It then uses ```magick``` to crop the thumbnail from a 16:9 rectangle to a 1:1 square. Finally ```mutagen``` is used to embed the cropped image as album art into the FLAC file.

All music is downloaded to ~/Music/ to change this edit

```
~/.local/bin/yt-dlp-music
```

and change --output to your liking.




