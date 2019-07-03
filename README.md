# producerpy
Python scripts for automating tedious music production tasks.


## Audio + Image(s) = Video
Useful for Instagram content, eliminates the need to open any video editing software.  Visual component can be a single image, or several images displayed gif style.
```
python audio_plus_image_to_video.py <audio fp> <image(s) fp>
```

## Stem Killer (delete silent files)
Deletes any audio files that are completely silent.  Often times when you export your tracks to stems to:
- mix in a different DAW
- share with a friend your project will contain stems
```
python delete_silent_files.py <top_dir_of_stems>
```

you will find stems that contain no audio content.  These take up significant diskspace, and clutter your work environment/DAW.  This script only deletes files that are truly silent, files with very quiet sounds (reverb, noise, etc) will not be deleted.

## Giffer
Nothing new here, just a script to generate audio-less gif's given the top folder filepath.
```
python giffer.py <image_dir> <fps>
```


## To run:
Install Python via anaconda using the instructions [here](https://www.anaconda.com/distribution/).

You will also need a few open source CLI tools:
```
brew install ffmpeg libav
```
```
pip install ffmpeg opencv-python moviepy librosa soundfile
```