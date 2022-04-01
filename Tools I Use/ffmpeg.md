cli tool to do **video manipulation**, recording, and more

installed with **brew**


# Command Line Parameters
-s resolution
-r frame rate
-f has to be avfoundation on mac
-i "text" text has to be in the name of the webcam, case sensitive
-b:v video bandwidth
-c:v video codec

# Example commands
**want to record webcam at highest quality**
```
ffmpeg -s 1280x720 -r 30 -f avfoundation -i "FaceTime" -b:v 80000k -c:v libx264  out.mp4
```
  - Built in FaceTime camera only supports 1280x720

**get list of inputs available**
```
ffmpeg -f avfoundation -list_devices true -i ""
```

**capture the atem mini pro**
```
ffmpeg -s 1920x1080 -r 25 -f avfoundation -i "Blackmagic" -b:v 8000k -c:v libx264  out.mp4
```