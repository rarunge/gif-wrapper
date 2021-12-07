# gif-wrapper (for Mac)
A wrapper solution for converting various video formats to GitHub-supported ones (e.g. gif) to share code demos.

# Installation
Open Mac's terminal and complete the following steps.

1) Install brew (skip if you have it):
```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

2) Install "ffmpeg" (skip if you have it):
```brew install ffmpeg```

3) Link ffmpeg
```brew link ffmpeg```

# Usage Instructions
Use command+shift+5 to take video with native Apple software.
After you stop recording, the file should be saved to desktop by default (can be changed to ./input).
Drag/drop this video file into the input folder inside "gif-wrapper".

Open Mac's terminal and complete the following steps

1) Navigate to gif-wrapper folder; if it's on your desktop, the command would be:
```cd ~/Desktop/gif-wrapper```

2) Example use, after placing input files in ./input, would be:
```./script/ffmpeg-batch.sh mov gif ./input ./output '-r 30 -vf scale=720:-1'```

In the example above, the ffmpeg script converts any MP4 file in ./input to gif format. You can use different formats for either input and output. The frame rate in that example is set to 30 frames/sec; scaling 720px, while keeping the original aspect ratio. The gif you created will be saved to the ./output folder of the gif-wrapper directory.

_IMPORTANT TIP: After running the script, move ./input files to the archive folder._
_Since this works on multiple files at once, anything contained in ./input will be used/converted._
