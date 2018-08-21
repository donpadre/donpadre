---
ID: 2228
post_title: 'Astuce : Comment utiliser « Bash sur Ubuntu pour Windows » avec Cmder (ComEmu) ?!'
post_name: >
  astuce-comment-utiliser-bash-sur-ubuntu-pour-windows-avec-cmder-comemu
author: donpadre
post_date: 2016-09-25 08:00:25
layout: post
link: >
  https://www.donpadre.fr/index.php/2016/09/25/astuce-comment-utiliser-bash-sur-ubuntu-pour-windows-avec-cmder-comemu/
published: true
tags:
  - "10"
  - cmd
  - cmder
  - Développeur
  - Invité de commande
  - Linux
  - shell
  - Terminal
  - Windows
categories:
  - Application
  - Geek
  - Linux
  - Os
  - Windows
---
<p style="text-align: justify;">
  Avec la mise à jour <strong><em>Anniversary </em></strong>de Windows 10 est apparu dans sa version professionnel, <strong>"Bash sur Ubuntu pour Windows" </strong> un vrai invité de commande Linux pour Windows comme son nom l'indique. <strong>Microsoft</strong> à créer cet invité de commande en partenariat avec <strong>Canonial</strong>, l'éditeur qui se trouve derrière <em><strong>Ubuntu</strong></em>. Encore à ses balbutiements par rapport un vrai invité de commande sous <em>Linux</em> ou <em>Unix</em>, au niveau des performances d’exécution.<!--more-->
</p> [caption id="attachment_2235" align="aligncenter" width="720"]

<img class="wp-image-2235" title="Bash sur Ubuntu pour Windows" src="https://www.donpadre.fr/wp-content/uploads/2016/09/bash-windows.png" alt="bash-windows" width="720" height="302" /> Bash sur Ubuntu pour Windows[/caption] Sous *Windows* j'ai pris pour l'habitude d'utiliser **Cmder** un émulateur d'invité de commande Linux, qui contient un Bash émuler pour faire du Web développement afin d'utiliser des technologies comme ***Nodejs , **Sass, **Gulp, **Bower, ****et**** **PHP-cli***, en ligne commande. [caption id="attachment_2229" align="aligncenter" width="720"]<img class="wp-image-2229" title="Cmder avec Bash sur Ubuntu sur Windows" src="https://www.donpadre.fr/wp-content/uploads/2016/09/cmder-bash-ubuntu-for-windows-10.png" alt="cmder-bash-ubuntu-for-windows-10" width="720" height="300" /> Cmder avec Bash sur Ubuntu sur Windows[/caption] Et je me suis posé la question comment lier **Bash sur *Ubuntu* **et ***Cmder, ***en fouillant un peu sur les internet j'ai trouvé mon bonheur dans un Issues du **Github**  officiel de *Cmder.* Pour cela nous allons mettre en place une nouvelle tâche appelé  "Bash::Ubuntu" dans Cmder : 
> 1.  Ouvrir les paramètres soit en cliquant sur les 3 barres en bas a droite de la fenêtre ou en utilisant la combinaison de touche ***Win+Alt+P*,**
> 2.  Aller dans ***Startup->Tasks,***
> 3.  Cliquer sur le bouton **+** en bas à gauche afin d'ajouter une nouvelle tâche,
> 4.  **Choisir un nom pour votre tâche**,
> 5.  Dans **Task parameters ** rentrer cette ligne : 
>     *   */icon "%USERPROFILE%\AppData\Local\lxss\bash.ico"*
> 6.  Dans **Commands **: rentrer cette ligne : 
>     *   *%windir%\System32\bash.exe ~ -c zsh -cur_console:p*
> 7.  Sauvegarder votre tâche en cliquant sur **Save setting** Et voilà tout est près, vous pouvez utiliser cmder avec bash ubuntu pour windows. [caption id="attachment_2245" align="aligncenter" width="763"]

<img class="size-full wp-image-2245" src="https://www.donpadre.fr/wp-content/uploads/2016/09/cmder-settings-1.png" alt="cmder-settings" width="763" height="490" /> Paramètre de cmder[/caption] Source splash : <a href="https://ayesh.me/" target="_blank">Ayesh.me</a>