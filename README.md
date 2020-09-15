---
title: SpeakBook Index Page
description: This is a project to build a toolchain for multi-lingual PDF's. Initial document is SpeakBook; a low-tech communication chart and book.
---
<img src="https://i.imgur.com/FyH8YF2.png" :src="$withBase('/assets/logo.png')" alt="SpeakBook" style="width:100%">

This is a repository to hold the working versions of [Patrick Joyce's SpeakBook project](https://web.archive.org/web/20170325172200/http://www.speakbook.org/). We aim to provide a platform for crowd-sourced version control of future PDF's here. More info (*and the current final releases*) can be found at the Ace Centre's project page [here](http://acecentre.org.uk/project/speakbook/).

The current *in-progress* versions (Note: will only look as intended in Chrome. We recommend looking at the PDF builds):

## Complete Translatons

- 🇬🇧[English SpeakBook](/speakbook/), [Printing Instructions](/speakbook/printing-instructions.html) (and [PDF](/speakbook/index.pdf), [PDF - Printing Instructions](/speakbook/printing-instructions.pdf))
- 🇹🇷[Turkish Speakbook](/tr/speakbook/), [Printing Instructions](/tr/speakbook/printing-instructions.html) (and [PDF](/tr/speakbook/index.pdf), [PDF - Printing Instructions](/tr/speakbook/printing-instructions.pdf))
- 🇿🇦[Afrikaans SpeakBook](/af/speakbook/), [Printing Instructions](/af/speakbook/printing-instructions.html) (and [PDF](/af/speakbook/index.pdf), [PDF - Printing Instructions](/af/speakbook/printing-instructions.pdf))

## Needing "Printing Instructions" (but complete otherwise)

- 🇸🇪[Swedish SpeakBook](/sv/speakbook/) (and [PDF](/sv/speakbook/index.pdf))
- 🇵🇹[Portuguese SpeakBook](/po/speakbook/) (and [PDF](/po/speakbook/index.pdf))
- 🇪🇸[Spanish SpeakBook](/es/speakbook/) (and [PDF](/es/speakbook/index.pdf))
- 🇩🇪[German SpeakBook](/de/speakbook/) (and [PDF](/de/speakbook/index.pdf))
- 🇫🇷[French SpeakBook](/fr/speakbook/) (and [PDF](/fr/speakbook/index.pdf))
- 🇿🇦[Zulu SpeakBook](/zu/speakbook/) (and [PDF](/zu/speakbook/index.pdf))
- 🇲🇹[Maltese SpeakBook](/mt/speakbook/) (and [PDF](/mt/speakbook/index.pdf))


To help out with translation into new languages join the [POEditor project here](https://poeditor.com/join/project/wKsMtKRLIj)

[Issues here](https://github.com/acecentre/SpeakBook/issues).  

## How do I create a new version for my language - or improve a language translation

Firstly - *Great!* Here are the steps: 

1. Go to <https://poeditor.com/join/project/wKsMtKRLIj> and join up. Pick a current language to help edit - or create a new one. 
2. What happens is you end up with a table. In one column is English snippets of text. And in the other you write that languages translation. Have a look at the [English](https://speakbook.netlify.app/speakbook/index.pdf) version where the strings are from. It should make sense what things mean.  There are some strange bits - some bits later on have html embedded in them. Don’t worry - just do what you can. You can’t break anything! 
3.  Once you have done what you can - send [me an email](mailto:wwade@acecentre.org.uk) and I’ll run a little script that converts it. It really takes me no more than about 10 minutes to do. Once done you can see the changes on our [development page](http://speakbook.netlify.app) 
4.  There’s usually tweaks to be made around how we do the e-Tran frame and finger spelling page. At that stage we just have a email chat about the best way forward. Some languages don’t bother to use all their letters - or we ignore the numbers. Lots of things we can do. And feel free to change things like the static words like “I feel hot” to something more regional. 
5.  *Lastly** - we translate the printing instructions page. That’s just a text or word file you can [send me](mailto:wwade@acecentre.org.uk).  Example [here](https://speakbook.netlify.app/speakbook/printing-instructions.pdf) 


**Urgent needs**
- Need translations for a [printed instructions sheet ](https://acecentre.org.uk/wp-content/uploads/2018/11/Printing-Instructions1.pdf)
- More serious coding issues see the queue [ here](https://github.com/acecentre/SpeakBook/issues). 

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/) [![OpenAAC](https://img.shields.io/badge/OpenAAC-💬-red?style=plastic&logoWidth=40&link=https://www.openaac.org)](https://img.shields.io/badge/OpenAAC-💬-red?style=plastic&logoWidth=40&link=https://www.openaac.org) [![Netlify Status](https://api.netlify.com/api/v1/badges/e7e4b2ad-fd21-4239-8141-ea608482fea7/deploy-status)](https://app.netlify.com/sites/speakbook/deploys)

## Technical Background

This is simply a Vue.js themed template with some scripts to generate a PDF of the html document that is created. Its designed for chrome as chrome does the PDF generation.  We use [PO language strings](https://www.gnu.org/software/gettext/manual/html_node/PO-Files.html) in this project. On each markdown file we have a ``text:`` field where there is a list of strings available to the page. This means you can separate the design logic from the language information. We have some scripts to aid this process. A Markdown->PO script to create a PO file from a file - and then a PO->Markdown script that applies new language strings to a markdown file.  

### Layout

    .vuepress/
        build-pdf-plugin.js    <-  The pdf build plugin. 
        config.js
        dist/                  <- Where the final build is outputted
        public/                <- Static assets like images sit here and in SpeakBook/
        theme/  
            layouts/
                SpeakBook.vue  <- The main logic for SpeakBook
            styles/
            util/
            fonts/
            components/         

    .scripts/
        common.js
        apply-po-to-md.js     <- Apply a PO Language file to Markdown file. 
        getPOfiles.js         <- NOT WORKING - Grab files from POEditor
        po-from-md.js         <- Make a master PO file from a markdown file.        

    speakbook/
        README.md             <- The English version of SpeakBook

    lang/speakbook/
        README.md             <- Other language versions

### Package scripts

```
# run a local server for development
$ yarn dev
# build it in static html format
$ yarn build
# build pdf format for all pages
$ yarn buildpdf
```

There is also a way we can use Google translate to start a new language. This is useful to get you going in the right direction.. 

setup:
```npm install parse5-serializer-stream, parse5, @vitalets/google-translate-api  ```
and then run:
```node .scripts/po-google-translate.js res/lang/master.po res/lang/SpeakBook_Armenian.po English Armenian'```

e.g. For English to Armenian

```node .scripts/po-google-translate.js res/lang/master.po res/lang/SpeakBook_Armenian.po en hy```


### Script to update all files from POEditor

```
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Arabic.po ar/speakbook/README.md > ar/speakbook/README2.md && mv ar/speakbook/README2.md ar/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Spanish.po es/speakbook/README.md > es/speakbook/README2.md && mv es/speakbook/README2.md es/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_French.po fr/speakbook/README.md > fr/speakbook/README2.md && mv fr/speakbook/README2.md fr/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Portuguese.po po/speakbook/README.md > po/speakbook/README2.md && mv po/speakbook/README2.md po/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Swedish.po sv/speakbook/README.md > sv/speakbook/README2.md && mv sv/speakbook/README2.md sv/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_German.po de/speakbook/README.md > de/speakbook/README2.md && mv de/speakbook/README2.md de/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Afrikaans.po af/speakbook/README.md > af/speakbook/README2.md && mv af/speakbook/README2.md af/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Zulu.po zu/speakbook/README.md > zu/speakbook/README2.md && mv zu/speakbook/README2.md zu/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Turkish.po tr/speakbook/README.md > tr/speakbook/README2.md && mv tr/speakbook/README2.md tr/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Maltese.po mt/speakbook/README.md > mt/speakbook/README2.md && mv mt/speakbook/README2.md mt/speakbook/README.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Armenian.po hu/speakbook/README.md > hu/speakbook/README2.md && mv hu/speakbook/README2.md hu/speakbook/README.md 
```
and likewise for Classic (colour version):

```
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Arabic.po ar/speakbook/classic.md > ar/speakbook/classic2.md && mv ar/speakbook/classic2.md ar/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Spanish.po es/speakbook/classic.md > es/speakbook/classic2.md && mv es/speakbook/classic2.md es/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_French.po fr/speakbook/classic.md > fr/speakbook/classic2.md && mv fr/speakbook/classic2.md fr/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Portuguese.po po/speakbook/classic.md > po/speakbook/classic2.md && mv po/speakbook/classic2.md po/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Swedish.po sv/speakbook/classic.md > sv/speakbook/classic2.md && mv sv/speakbook/classic2.md sv/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_German.po de/speakbook/classic.md > de/speakbook/classic2.md && mv de/speakbook/classic2.md de/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Afrikaans.po af/speakbook/classic.md > af/speakbook/classic2.md && mv af/speakbook/classic2.md af/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Zulu.po zu/speakbook/classic.md > zu/speakbook/classic2.md && mv zu/speakbook/classic2.md zu/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Turkish.po tr/speakbook/classic.md > tr/speakbook/classic2.md && mv tr/speakbook/classic2.md tr/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Maltese.po mt/speakbook/classic.md > mt/speakbook/classic2.md && mv mt/speakbook/classic2.md mt/speakbook/classic.md 
node .scripts/apply-po-to-md.js res/lang/SpeakBook_Armenian.po hu/speakbook/classic.md > hu/speakbook/classic2.md && mv hu/speakbook/classic2.md hu/speakbook/classic.md 
```
