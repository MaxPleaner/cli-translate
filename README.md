# cli-translate

This is a script for getting quick translation and pronounciation.

To install:

- copy the translate_to file into /usr/local/sbin or somewhere on the path
- mark it as executable

To use:

```sh
$ translate_to <lang code> <phrase or phrases>
```

What this does:

- speaks the result
- prints a full translation
- prints a brief translation (at the bottom, for quickly reading)
- unless the "to" language in English, reverse looks it up (into english) and prints that.

Example:

**whole phrases** - _does a single lookup to Google translate. The whole phrase is between quotes._

```sh
max@max ~> translate_to zh "chinese is known for being difficult to translate back and forth between english"
chinese is known for being difficult to translate back and forth between english

中国人很难在英语之间来回翻译
(Zhōngguó rén hěn nán zài yīngyǔ zhī jiān láihuí fānyì)

Translations of chinese is known for being difficult to translate back and forth between english
[ English -> 简体中文 ]

chinese is known for being difficult to translate back and forth between english
    中国人很难在英语之间来回翻译, 中国被称为是很难翻译来回英语之间
中国人很难在英语之间来回翻译

reverse translation: 
It is difficult for Chinese people to translate back and forth between English
```

**segmented phrase** - _no quotes surround the phrase, so each word triggers a new lookup_

```sh
max@max ~> translate_to de this is an apple
this
/T͟His/

Dies

Definitions of this
[ English -> Deutsch ]

pronoun
    dieses
        this
    dieser
        this
    diese
        this, these
    dies
        this
    das
        that, this, it, who
is

Ist

Translations of is
[ English -> Deutsch ]

is
    Ist
an
/an/

ein

Definitions of an
[ English -> Deutsch ]

article
    eine
        a, an
    ein
        a, an
apple
/ˈapəl/

Apfel

Definitions of apple
[ English -> Deutsch ]

noun
    (der) Apfel
        apple
Dies
Ist
ein
Apfel

reverse translation: 
This Is An Apple
```


