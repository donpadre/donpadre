---
ID: 1453
post_title: 'FileBot, l&rsquo;outil ultime pour organiser et renommer vos médias.'
post_name: >
  filebot-loutil-ultime-pour-organiser-et-renommer-vos-medias
author: donpadre
post_date: 2015-10-25 14:39:00
layout: post
link: >
  https://www.donpadre.fr/index.php/2015/10/25/filebot-loutil-ultime-pour-organiser-et-renommer-vos-medias/
published: true
tags:
  - Application
  - Automatisation
  - Film
  - Geek
  - Manga
  - Série
categories:
  - Anime
  - Application
  - Geek
  - Linux
  - Manga
  - OSX
  - Série
  - Serveur
  - Windows
---
FileBot, l'outil ultime pour organiser et renommer vos films, émissions de télévision ou d'anime et album musique et qui peut téléchargé les sous-titres et les illustrations de vos médias.<!--more--> Voila bien deux mois que je l'utilise FileBot pour réorganiser automatiquement mes médias après mon gestionnaire de téléchargement est fini de les récupérer. 

[<img class="size-full wp-image-1480 aligncenter" src="http://www.donpadre.fr/wp-content/uploads/2015/10/filebot-renamee.png" alt="filebot-renamee" width="963" height="521" />][1] FileBot va renommer le média, le placé dans le bon dossier avec bonne orthographe et la bonne saison pour les séries et les aimes, avec le synopsis et les fan-arts. Il fera de même pour les films et les albums de vos chanteur préféré. Pour réaliser cette tâche automatique après chaque téléchargement, vous allez devoir passer par les lignes de commande dans un script console dit CLI. [pastacode lang="bash" message="Exemple de scripts bash pour filebot qui fonctionne avec rtorrent" highlight="rtorrent-postprocess" provider="manual"] 
    #!/bin/bash
    TORRENT_PATH=$1
    TORRENT_NAME=$2
    TORRENT_LABEL=$3
    
    filebot -script fn:amc --output "$HOME/Media" --log-file amc.log --action duplicate --conflict override -non-strict --def music=y artwork=y "ut_dir=$TORRENT_PATH" "ut_kind=multi" "ut_title=$TORRENT_NAME" "ut_label=$TORRENT_LABEL" & [/pastacode] [pastacode lang="bash" message="Ligne de code à ajouté dans ~/.rtorrent.rc" highlight="" provider="manual"] 

    MARKDOWN_HASH3fdeaa5322b1b85dcd4f5382081e52baMARKDOWN_HASH [/pastacode] FileBot est disponible sur l'ensemble des systèmes exploitation, disponible à cette adresse: 

<a href="http://www.filebot.net/#download" target="_blank">filebot.net</a> Pour aller plus loin avec FileBot je vous conseille de faire un tour sur leur <a href="https://www.filebot.net/forums/viewtopic.php?f=4&t=215#p5316" target="_blank">forum</a>.

 [1]: http://www.donpadre.fr/wp-content/uploads/2015/10/filebot-renamee.png