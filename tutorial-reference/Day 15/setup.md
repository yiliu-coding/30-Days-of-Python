# Overview & Setup

We're going to be using Moviepy to do the following:
1. Create thumbnails from videos
2. Image Collection to Video
3. Generate a GIF animation
4. Combine Audio Samples in a Video
5. Overlay Text, Image, or Video


##### Requirements:
- Python 3.6+
- Pipenv (or another virtual environment)
- moviepy==1.0.2 (or greater)
- ffmpeg & imagemagick installed (see below)




### [FFmpeg](https://www.ffmpeg.org/download.html) ([Link](https://www.ffmpeg.org/download.html))
Moviepy and ffmpeg work well together. ffmpeg can do most/all of this on it's own but, as far as this writing, lacks Python bindings. Thus, moviepy is used!

##### macOS:

Use [homebrew](http://brew.sh)

```
brew update && brew install ffmpeg
```

#### Windows/Linux:
Use the [executable](https://www.ffmpeg.org/download.html)



### [ImageMagick](https://imagemagick.org/script/download.php) ([Link](https://imagemagick.org/script/download.php))
To add text, you must install ImageMagic.

##### macOS:

Use [homebrew](http://brew.sh)

```
brew update && brew install imagemagick
```
#### Linux:
Download [here](https://imagemagick.org/script/download.php)

#### Windows:
Use the [binary or exe](https://imagemagick.org/script/download.php#windows)


### [Moviepy](https://zulko.github.io/moviepy/) ([Link](https://zulko.github.io/moviepy/))
```
pipenv install moviepy
```
This is what we'll use for Day 15.
