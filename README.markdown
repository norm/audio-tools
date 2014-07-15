audio-tools
===========

rip
---
Rip CDs in a paranoid, metadata-obsessed fashion.

youtube-rip
-----------

Extract the audio from YouTube videos/playlists into a `m4a` file, tagged with
the title, artist (youtube account), year/purchase date (uploaded date), album
artist ('Various Artists'), album name (either the playlist name, or
'YouTube') and thumbnail.

You'll need some command line tools and perl modules installed:

    brew install atomicparsley cpanminus ffmpeg youtube-dl
    sudo cpanm Capture::Tiny JSON Modern::Perl

Copy `youtube-rip` to your `$PATH` somewhere. Then run `youtube-rip -h` 
to find out the arguments to use. 
