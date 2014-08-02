Morpha : a morphological analyser for English
=============================================

Unpackaged original: http://www.sussex.ac.uk/Users/johnca/morph.html

A morphological analyser / lemmatiser for English based on finite-state 
techniques. Given a word form (and its part of speech if available) it 
returns the lemma and suffix. 

It covers the English productive suffixes:
* -s : plural of nouns, 3rd sing pres of verbs
* -ed : past tense
* -en : past participle
* -ing : progressive of verbs

See: doc/README for the original README

Installation
------------

To build and install the 'morpha' executable, make sure that git, 
Autoconf, Automake, and Libtool are installed on your system, and:

1. Clone this repository and reconfigure automake for the local system:
```
   $ git clone -depth 1
   $ cd morpha/
   $ sh autogen.sh
```

2. Configure, compile, and install system wide:
```
   $ ./configure
   $ make
   $ sudo make install
```

Usage
-----

An example with STDIN and STDOUT:

   $ echo "Students_NNS were_VBD writing_VBG letters_NNS" | morpha -act
   Student+s_NNS be+ed_VBD write+ing_VBG letter+s_NNS

See doc/doc.txt for the original details.
