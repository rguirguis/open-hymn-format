# Open Hymn Format

Open file format for hymn lyrics.

## Scope

This is initial draft of the format to share hymn lyrics in standard way.   
Tools to export the format to "_.odp_" files will enable users to generate presentation right from the "_.ohf_" format.

[.lrc](https://en.wikipedia.org/wiki/LRC_(file_format)) format has similar goal, but it enforce timing and should always be associated with the audio file to work properly. _Open Hymn Format_ goal is provide a standalone format to display hymn lyrics along with hymn meta information like writer and composer without the audio files.  
_Open Hymn Format_ is ideal for digital lyrics distribution. The ultimate goal is to provide mobile apps means to search and display hymns offline to allow group of people to sing along.

## Format Features

* **Verse Index**  
  For quick search without external indexing.
* **Verse/Chorus selection**  
  Select which verse to display, handy for large hymns.
* **Verse/Chorus repetition**  
  Select which verse and chorus repetition.
* **Unicode Support**  
  Support Unicode songs for non-Latin languages
* **Attribution**  
  Author and Composer attribution, with support to other meta information like year of release.
* **License**  
  Support for [Creative Commons license](https://creativecommons.org/choose/).

## Roadmap

* Support time signature
* Timing auto-play
* Export tools:
  * Open Document Presentation Format `.odp`
  * LRC Format `.lrc` template

