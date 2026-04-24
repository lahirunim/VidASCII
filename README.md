# VidASCII

VidASCII converts any video into a browser-playable ASCII animation.
No server, no dependencies, no installation — just drop a video in and open the result in your browser.

## How it works

VidASCII reads your video frame by frame using OpenCV. Each frame is converted 
to grayscale and resized to fit a character grid. Every pixel's brightness is 
then mapped to an ASCII character — dark pixels become spaces, bright pixels 
become dense characters like `#` or `@`, and everything in between fills out 
the range.

Once all frames are processed, the entire animation is saved as a single 
JavaScript file (`video_data.js`) containing every ASCII frame as a string. 
The included `viewer.html` loads that file and cycles through the frames in 
your browser at the original video's pace, creating a smooth ASCII playback 
experience entirely on the client side.

## Requirements (source)

- Python 3.x
- opencv-python (`pip install opencv-python`)

## Video guide
[Watch the tutorial](https://youtu.be/_fWkQK3yoZo)

<img width="548" height="480" alt="vlcsnap-2026-04-24-15h13m52s820" src="https://github.com/user-attachments/assets/c04bdfd7-a938-499a-8802-51a3023e6305" />


## License
MIT
