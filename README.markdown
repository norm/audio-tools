audio-tools
===========

rip
---
Rip CDs in a paranoid, metadata-obsessed fashion.

youtube-rip
-----------
Extract the audio from YouTube videos/playlists.

You'll need some command line tools and perl modules installed:

    brew install atomicparsley cpanminus ffmpeg youtube-dl
    sudo cpanm Capture::Tiny JSON Modern::Perl

Copy `youtube-rip` to your `$PATH` somewhere. Then run it. It will
automatically tag the output files with metadata. In particular, the title,
artist (youtube account), year/purchase date (uploaded date), album artist
('Various Artists'), album name (either the playlist name,  or 'YouTube')and
thumbnail.

    # rip the audio from one youtube video
    youtube-rip 'https://www.youtube.com/watch?v=HU2ftCitvyQ'

    # rip an entire playlist
    youtube-rip 'https://www.youtube.com/playlist?list=PL4zR2yLTCZ8dkQat9b7BQCOqpqYVRmePl'

    # different album name
    youtube-rip -a 'Weird Stuff Norm is Obsessed With' 'https://www.youtube.com/playlist?list=PL4zR2yLTCZ8dkQat9b7BQCOqpqYVRmePl'

    # other options
    youtube-rip -v ...      # verbose output
    youtube-rip -r ...      # re-rip already ripped videos
    youtube-rip -f ...      # don't clean up intermediate files
