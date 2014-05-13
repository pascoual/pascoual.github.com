---
layout: post
title: Atom on Ubuntu via PPA [FR]
description: "A Hackable Text Editor for the 21st Century on Ubuntu."
modified: 2014-05-12
tags: [Atom, editor, Ubuntu, Linux]
image:
  feature: abstract-4.jpg
  credit:
  creditlink:
comments: true
share: true
---

You can find the US version of this post in [Webupd8](http://www.webupd8.org/2014/05/install-atom-text-editor-in-ubuntu-via-ppa.html), by the author of the Atom PPA for Ubuntu.

## Atom est open-source

Le 6 mai GitHub a libéré le code source d'Atom sous *[licence MIT](http://choosealicense.com/licenses/mit/)*, l'éditeur du 21ème siècle sur lequel ils travaillent depuis maintenant 6 ans Oo. Il faut avouer qu'il a un air de famille avec SublimeText, cela aura l'avantage de ne pas dérouter les migrants !

<figure>
  <img src="{{ site.url }}/images/posts/atom_screenshot.gif" alt="">
  <figcaption>L'éditeur Atom.</figcaption>
</figure>

## Atom sur votre Ubuntu 14.04LTS, 13.10 et 12.04LTS (64bit)

[Webupd8.org](http://www.webupd8.org) a créé un PPA (Personal Package Archive) pour vous éviter la compilation d'Atom sur votre distribution. Pour le moment il ne supporte que les versions 64 bits d'Ubuntu 14.04LTS, 13.10 et 12.04.

Installation :
{% highlight shell-session %}
sudo add-apt-repository ppa:webupd8team/atom
sudo apt-get update
sudo apt-get install atom
{% endhighlight %}

Sur une 13.10 le menu global d'Unity ne fontionne pas pour Atom et il vous faudra créer une entrée à la mano.

## Quelques commandes pour prendre en main cet éditeur :
1. **Ctrl-Shift-p** : c'est la commande la plus importante, elle vous ouvre la *Command Palette* qui liste toutes les commandes réalisables avec le raccourci clavier correspondant.
<img src="{{ site.url }}/images/posts/atom-cmd-shift-p.png" alt="" class="img-rounded">
2. **Ctrl-p** : permet d'ouvrir un fichier via un filtre sur son nom, quelque soit le chemin pour l'atteindre.
3. **Crtl-b** : la même chose mais uniquement concernant les fichiers déjà ouverts.
4. **Crtl-Shift-b** : vous liste les fichiers modifiés ou non suivis par rapport à votre dernier commit Git.
5. **Crtl-0** : place le focus sur l'arbroressence des fichiers. Vous pouvez bien évidemment aller cliquer dessus avec la souris mais ça fait toujours Joe le Geek de tout faire au clavier (et c'est plus rapide).
6. **Crtl-f** : si tu n'imagines pas ce que ça fait va faire un tour au [Jardiland](http://www.jardiland.com/nos-magasins) le plus proche de chez toi !
7. **Crtl-shift-f** : la même chose mais sur tous les fichiers.
8. **Crtl-r** : rechercher un symbol (une definition) dans le fichier courant, utilisant le même type de filtre que Crtl-p.
9. **Crtl-shift-r** : la même chose mais sur tous les fichiers. Attention là y'a une astuce de sioux, il faut installer *ctags* (```sudo apt-get install exuberant-ctags```), puis créer un dictionnaire (```ctags -R ./```).
10. **Crtl-k right& Crtl-k up** : split l'affichage verticalement ou horizontalement. Pour de-spliter il faut fermer tous les fichiers ouverts avec Crtl-w
11. **Crtl-w** : tu rigoles ? Je t'assure [Jardiland](http://www.jardiland.com/nos-magasins) c'est bien pour se détendre !
12. **Crtl-,** : ouvre l'éditeur de configuration d'Atom.
