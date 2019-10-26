# ffmpeg-static

Bash script collection to compile statically [FFmpeg](https://ffmpeg.org/) and install it using symbolic links.

Target OS is Ubuntu.

Compilation is based on [FFmpeg wiki compilation guide](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu).

FFmpeg is compiled with the following libraries :

* [libdav1d](https://code.videolan.org/videolan/dav1d)
* [libx264](https://code.videolan.org/videolan/x264)
* [libx265](https://bitbucket.org/multicoreware/x265/wiki/Home)
* [libfdk-aac](https://github.com/mstorsjo/fdk-aac)
* [libmp3lame](http://lame.sourceforge.net)
* [libopus](http://www.opus-codec.org/downloads/)
* [libvpx](https://github.com/webmproject/libvpx/)
