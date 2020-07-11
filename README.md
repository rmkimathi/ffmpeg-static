# ffmpeg-static

Bash script collection to compile statically [FFmpeg](http://ffmpeg.org/releases/?C=M;O=D) and install it using symbolic links.

Target OS is Ubuntu.

Compilation is based on [FFmpeg wiki compilation guide](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu).

nasm version ≥ 2.14  
yasm version ≥ 1.2.0  
meson version ≥ 0.47

FFmpeg is compiled with the following libraries :

* [nasm](https://www.nasm.us/pub/nasm/releasebuilds/?C=M;O=D)
* [libdav1d](https://code.videolan.org/videolan/dav1d/-/releases)
* [libx264](https://code.videolan.org/videolan/x264)
* [libx265](https://bitbucket.org/multicoreware/x265/downloads/)
* [libfdk-aac](https://github.com/mstorsjo/fdk-aac/releases)
* [libmp3lame](http://lame.sourceforge.net)
* [libopus](http://www.opus-codec.org/downloads/)
* [libvpx](https://github.com/webmproject/libvpx/releases)

## Installation

```

===== Symbolic links folder =====
mkdir -p ~/bin

===== nvenc =====
git -C nv-codec-headers pull 2> /dev/null || git clone https://git.videolan.org/git/ffmpeg/nv-codec-headers.git
cd nv-codec-headers
make
sudo make install

===== Documentation =====
echo "MANPATH_MAP $HOME/bin $HOME/ffmpeg-static/build/current/share/man" >> ~/.manpath

===== Script =====
export FFBUILD_VERSION=4.3.1 #ffmpeg version (optional maintain version build folder. /etc/environment)
git clone https://github.com/rmkimathi/ffmpeg-static.git
cd ~/ffmpeg-static
./build.sh -h
./build.sh all

```
