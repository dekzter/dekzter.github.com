---
layout: posts
category: Projects
preview: For my senior design project at NC State University, my team was to make an automated ID3 metadata extractor for MP3 files as well as a digital music jukebox that would ultimately be placed in social areas (such as coffee shops) around college campuses.
title: Crumbs Music Media
---

<img src="/images/crumbs.png" alt="crums jukebox pic" width="550px" />

For my senior design project at NC State University, my team was to make an automated ID3 metadata extractor for MP3 files as well as a digital music jukebox that would ultimately be placed in social areas (such as coffee shops) around college campuses.

Essentially, the project was split into the two sub-projects: the metadata extractor and the digital jukebox. My portion of the project was dealing with the jukebox. The page itself was coded in PHP with jQuery and AJAX powering the dynamic search (so the page doesn't require a reload to populate the search, thus stopping the song from playing).

For the actual audio player, we used the open-source [jPlayer](http://www.jplayer.org/) which uses HTML5 with a Flash fallback, which is quite nice since not only would you have to worry about mobile browsers such as Safari on the iPhone, but also Firefox does not natively support MP3 playback in HTML5.

The database we used was MySQL, which was populated with the metadata information from the backend extractor portion of the project. Essentially, a preset directory is checked about once every 5 minutes for any contents. If there are any files present, it goes through each file to process. If the file is not an MP3, it is discarded. The metadata is extracted through third-party open-source applications (currently [eyeD3](http://eyed3.nicfit.net/), [mp3info](http://www.ibiblio.org/mp3info/), and [id3v2](http://www.id3.org/)) in addition to soundstretch to determine the song's BPM. A MySQL query is then constructed with that information and inserted into the database while the MP3 file is moved to a processed directory and its name is changed to that of its songID in the database.

Overall, the project was very enjoyable. It was an opportunity to bring my 2 favorite things together: music and programming. I'm quite pleased with the outcome, and if you'd like to check it out, head on over to [the jukebox](http://crumbs.codersmanifesto.com/).