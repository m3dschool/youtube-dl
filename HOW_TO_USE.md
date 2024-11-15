CLI

SINGLE DOWNLOAD
yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 https://youtu.be/NdEYFcO9SIE


MULTIPLE DOWNLOAD
yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 --batch-file DOWNLOAD_LIST.txt


### Basic Commands

#### 1. **Download a Playlist**
```powershell
yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 <playlist_url>
```

#### 2. **Download an Entire Channel**
```powershell
yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 <channel_url>
```

### Recommended Options for Better Experience
You can add the following options to customize the download further:

- **`-o "%(title)s.%(ext)s"`**: Sets the output filename as the video title.
- **`--yes-playlist`**: Ensures it downloads the entire playlist, not just a single video.
- **`--merge-output-format mp4`**: Merges audio and video into an MP4 file.
- **`--continue`**: Resumes partially downloaded files.
- **`--no-overwrites`**: Prevents overwriting existing files.
- **`--download-archive archive.txt`**: Keeps track of downloaded videos to avoid re-downloading.

### Full Command Example
```powershell
yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 --yes-playlist --merge-output-format mp4 --continue --no-overwrites --download-archive archive.txt -o "%(title)s.%(ext)s" <playlist_or_channel_url>
```

### Explanation:
- `-f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4`: Downloads the best MP4 format available.
- `--yes-playlist`: Downloads all videos in the playlist/channel.
- `--merge-output-format mp4`: Ensures the output is in MP4 format.
- `--continue`: Resumes downloads if they were interrupted.
- `--no-overwrites`: Avoids overwriting existing files.
- `--download-archive archive.txt`: Tracks downloaded videos in `archive.txt` to prevent duplicates.
- `-o "%(title)s.%(ext)s"`: Saves files with the video title.

Let me know if you have any specific preferences or need additional options!