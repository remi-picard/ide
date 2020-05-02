---
layout: page
title: vi
permalink: /vi/
---

## Raccourcis clavier

### Les indispensables

- `ESC` + `:q!` : quitter
- `ESC` + `:x` : quitter ET sauvegarder
- `i` : passe en mode INSERTION

### Navigation Code

- `h` : ←
- `j` : ↓
- `k` : ↑
- `l` : →

```bash
          ^
          k        Astuce :  La touche h est à gauche et déplace à gauche.
    < h       l >            La touche l est à droite et déplace à droite.
          j                  La touche j ressemble à une flèche vers le bas.
          v
```

- `^^` : DEBUT de la ligne
- `$` : FIN de la ligne
- `1G` ou `gg` : placement 1ère ligne
- `2G` : placement 2ème ligne
- `G` : placement DERNIERE ligne

### Edition

- `i` : passe en mode INSERTION
- `u` : annule

- `x` : supprimer un caractère
- `dw` : supprimer le mot
- `dd` : supprimer la ligne
- `d^^` : supprimer depuis le début de la ligne
- `d$` : supprimer jusqu'à la fin de la ligne

- `a` : avance d'un caractère et passe en mode INSERTION
- `I` : placement DEBUT de ligne et passe en mode INSERTION
- `A` : placement FIN de ligne et passe en mode INSERTION
- `O` : ajoute une ligne avant et passe en mode INSERTION
- `o` : ajoute une ligne après et passe en mode INSERTION

- `~` : minuscule
- `~~` : majuscule
- `g~~` : changement casse ligne
- `guu` : ligne en minuscule
- `gUU` : ligne en majuscule

- `yy` : copie la ligne
- `2yy` : copie 2 lignes
- `P` : colle au niveau de la ligne du dessus
- `p` : colle au niveau de la ligne du dessous

- `ESC` + `:q!` : quitter SANS sauvegarder
- `ESC` + `:x` : quitter ET sauvegarder
- `ESC` + `:e!` : retour au fichier avant modification
- `ESC` + `:2,4d` : supprime les lignes 2 à 4
- `ESC` + `:2,$d` : supprime les lignes 2 à la fin
- `ESC` + `:6,8w fileOut` : copie lignes vers fichier fileOut
- `ESC` + `:r fileIn` : lecture fileIn et insertion ligne de dessous
- `ESC` + `:set paste` : Mode copier coller
- `ESC` + `:set number` : N° de ligne
- `ESC` + `:set nonumber` : pas de N° de ligne
- `ESC` + `:set invnumber` : switch N° de ligne

## Configuration

Ajout fichier `~/.vimrc`

```bash
# Tabulation = 4 espaces
set ai ts=4 expandtab
# Abbréviation
abbr _sh #!/bin/bash
# Binding Ctrl+N = (Dés)Activation N° de ligne
nmap <C-N> :set invnumber <CR>
```

## Sources

- [Learning the Essentials of CentOS Enterprise Linux 7 Administration by Andrew Mallett](https://app.pluralsight.com/library/courses/lfcs-red-hat-7-essentials/table-of-contents)

## Annexes

Extrait du tutoriel avec la commande `vimtutor`

```txt
===============================================================================
=    W e l c o m e   t o   t h e   V I M   T u t o r    -    Version 1.5      =
===============================================================================

     Vim is a very powerful editor that has many commands, too many to
     explain in a tutor such as this.  This tutor is designed to describe
     enough of the commands that you will be able to easily use Vim as
     an all-purpose editor.

     The approximate time required to complete the tutor is 25-30 minutes,
     depending upon how much time is spent with experimentation.

     The commands in the lessons will modify the text.  Make a copy of this
     file to practise on (if you started "vimtutor" this is already a copy).

     It is important to remember that this tutor is set up to teach by
     use.  That means that you need to execute the commands to learn them
     properly.  If you only read the text, you will forget the commands!

     Now, make sure that your Shift-Lock key is NOT depressed and press
     the   j   key enough times to move the cursor so that Lesson 1.1
     completely fills the screen.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
			Lesson 1.1:  MOVING THE CURSOR


   ** To move the cursor, press the h,j,k,l keys as indicated. **
	     ^
	     k		    Hint:  The h key is at the left and moves left.
       < h	 l >		   The l key is at the right and moves right.
	     j			   The j key looks like a down arrow
	     v
  1. Move the cursor around the screen until you are comfortable.

  2. Hold down the down key (j) until it repeats.
---> Now you know how to move to the next lesson.

  3. Using the down key, move to Lesson 1.2.

Note: If you are ever unsure about something you typed, press <ESC> to place
      you in Normal mode.  Then retype the command you wanted.

Note: The cursor keys should also work.  But using hjkl you will be able to
      move around much faster, once you get used to it.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

...

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  This concludes the Vim Tutor.  It was intended to give a brief overview of
  the Vim editor, just enough to allow you to use the editor fairly easily.
  It is far from complete as Vim has many many more commands.  Read the user
  manual next: ":help user-manual".

  For further reading and studying, this book is recommended:
	Vim - Vi Improved - by Steve Oualline
	Publisher: New Riders
  The first book completely dedicated to Vim.  Especially useful for beginners.
  There are many examples and pictures.
  See http://iccf-holland.org/click5.html

  This book is older and more about Vi than Vim, but also recommended:
	Learning the Vi Editor - by Linda Lamb
	Publisher: O'Reilly & Associates Inc.
  It is a good book to get to know almost anything you want to do with Vi.
  The sixth edition also includes information on Vim.

  This tutorial was written by Michael C. Pierce and Robert K. Ware,
  Colorado School of Mines using ideas supplied by Charles Smith,
  Colorado State University.  E-mail: bware@mines.colorado.edu.

  Modified for Vim by Bram Moolenaar.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```
