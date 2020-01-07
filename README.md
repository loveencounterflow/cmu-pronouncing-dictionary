
# THE CMU PRONOUNCING DICTIONARY

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Front Matter](#front-matter)
  - [About the CMU dictionary](#about-the-cmu-dictionary)
  - [Phoneme Set](#phoneme-set)
- [cmu-pronouncing-dictionary](#cmu-pronouncing-dictionary)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Tests](#tests)
  - [Dependencies](#dependencies)
  - [Dev Dependencies](#dev-dependencies)
  - [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# Front Matter

> copied from http://www.speech.cs.cmu.edu/cgi-bin/cmudict

## About the CMU dictionary

The Carnegie Mellon University Pronouncing Dictionary is an open-source machine-readable pronunciation
dictionary for North American English that contains over 134,000 words and their pronunciations. CMUdict is
being actively maintained and expanded. We are open to suggestions, corrections and other input.

Its entries are particularly useful for speech recognition and synthesis, as it has mappings from words to
their pronunciations in the ARPAbet phoneme set, a standard for English pronunciation. The current phoneme
set contains 39 phonemes, vowels carry a lexical stress marker:

```
0    — No stress
1    — Primary stress
2    — Secondary stress
```

Bear in mind that this is a dictionary. If your word is not in it (or was misspelled) nothing will be
returned. This applies to items such as numbers. This tool will try to come up with pronunciations for words
not in the dictionary.

## Phoneme Set

The current phoneme set has 39 phonemes, not counting varia due to lexical stress. This phoneme (or more
accurately, phone) set is based on the ARPAbet symbol set developed for speech recognition uses. You can
find a description of the ARPAbet on Wikipedia, as well information on how it relates to the standard IPA
symbol set.

```
        Phoneme Example Translation
        ------- ------- -----------
        AA      odd     AA D
        AE      at      AE T
        AH      hut     HH AH T
        AO      ought   AO T
        AW      cow     K AW
        AY      hide    HH AY D
        B       be      B IY
        CH      cheese  CH IY Z
        D       dee     D IY
        DH      thee    DH IY
        EH      Ed      EH D
        ER      hurt    HH ER T
        EY      ate     EY T
        F       fee     F IY
        G       green   G R IY N
        HH      he      HH IY
        IH      it      IH T
        IY      eat     IY T
        JH      gee     JH IY
        K       key     K IY
        L       lee     L IY
        M       me      M IY
        N       knee    N IY
        NG      ping    P IH NG
        OW      oat     OW T
        OY      toy     T OY
        P       pee     P IY
        R       read    R IY D
        S       sea     S IY
        SH      she     SH IY
        T       tea     T IY
        TH      theta   TH EY T AH
        UH      hood    HH UH D
        UW      two     T UW
        V       vee     V IY
        W       we      W IY
        Y       yield   Y IY L D
        Z       zee     Z IY
        ZH      seizure S IY ZH ER
```


# cmu-pronouncing-dictionary

All the 134,000+ words in the CMU pronouncing dictionary as a simple JSON object

> The CMU Pronouncing Dictionary (also known as cmudict) is a public domain pronouncing dictionary created by Carnegie Mellon University (CMU). It defines a mapping from English words to their North American pronunciations, and is commonly used in speech processing applications

There are a handful of npm modules for working with the [CMU pronouncing dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict), but none so simple as this one. Unlike the [alternatives](https://www.npmjs.com/search?q=cmu), this module simple exports an object containing words as keys and their Arpabet transcriptions as values. Here's a sample:

```json
{
  "allergen": "AE1 L ER0 JH AH0 N",
  "allergens": "AE1 L ER0 JH AH0 N Z",
  "allergic": "AH0 L ER1 JH IH0 K",
  "allergies": "AE1 L ER0 JH IY0 Z",
  "allergist": "AE1 L ER0 JH AH0 S T",
  "allergist's": "AE1 L ER0 JH AH0 S T S",
  "allergist's(1)": "AE1 L ER0 JH AH0 S",
  "allergists": "AE1 L ER0 JH AH0 S T S",
  "allergists(1)": "AE1 L ER0 JH AH0 S",
  "allergy": "AE1 L ER0 JH IY0",
  "allers": "AO1 L ER0 Z",
  "allert": "AE1 L ER0 T",
  "allerton": "AE1 L ER0 T AH0 N",
  "alles": "EY1 L Z",
  "alleva": "AA0 L EY1 V AH0",
  "alleviate": "AH0 L IY1 V IY0 EY2 T",
  "alleviated": "AH0 L IY1 V IY0 EY2 T IH0 D",
  "alleviates": "AH0 L IY1 V IY0 EY0 T S",
  "alleviating": "AH0 L IY1 V IY0 EY2 T IH0 NG"
}
```

## Installation

Download node at [nodejs.org](http://nodejs.org) and install it, if you haven't already.

```sh
npm install cmu-pronouncing-dictionary --save
```

## Usage

```js
const words = require('cmu-pronouncing-dictionary')

words.length
// => 133779

words.phenomenon
// => 'F AH0 N AA1 M AH0 N AA2 N'
words.zygote
// => 'Z AY1 G OW0 T'
```

## Tests

```sh
npm install
npm test
```

## Dependencies

None

## Dev Dependencies

- [code](https://github.com/hapijs/code): assertion library
- [mocha](https://github.com/mochajs/mocha): simple, flexible, fun test framework
- [standard](https://github.com/feross/standard): JavaScript Standard Style

## License

ISC

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
