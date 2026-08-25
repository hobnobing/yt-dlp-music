# yt-dlp-music

Simple [yt-dlp](https://github.com/yt-dlp/yt-dlp) bash script that downloads in m4a and automatically adds song metadata, including cover art.


<img width="600" height="400" alt="ezgif-36f1ab6b1e465c15" src="https://github.com/user-attachments/assets/49be6afb-39f9-436d-b520-229df0c4144b" />


### Dependencies

Arch
```
sudo pacman -S --needed yt-dlp ffmpeg python-mutagen git wget imagemagick flac nodejs
```

### Cookies shenanigans

You need to export your YouTube cookies to use as authentication.
Use the "Get cookies.txt LOCALLY" extension. 
Go to ```https://www.youtube.com``` sign in, click the extension, "Export As", save as cookies.txt.

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

All music is downloaded to ~/Music/ to change this edit

```
~/.local/bin/yt-dlp-music
```

and change --output to your liking.




