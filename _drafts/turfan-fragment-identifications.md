---
title: "Identifying Undetermined Sanskrit Fragments from the Turfan Finds"   # working title
author: Kengo Harimoto
tags: [research, manuscripts, fragments, Turfan, Abhidharma]
description: >-
  TODO, one or two sentences: how many fragments that the catalogues list as undetermined
  could be given a text, by which means, and what kind of texts they turned out to be.
---

<!--
SKELETON. Everything inside comments is a note for writing and should be deleted before the
post moves to _posts/. Numbers are those of the findings page on 17 Nov 2026 (102 rows:
36 identified, 21 plausible, 10 editors' leads confirmed, 35 already identified elsewhere);
refresh them from research/turfan-sht before publishing.

BEFORE PUBLISHING, check:
  1. how much fragment text may be quoted, and the holding institution's rules on publication;
  2. that every identification named here is cleared for publication, with collaborators'
     consent for anything of theirs;
  3. where the post links for the full table;
  4. permission and credit lines for images.
-->

<!-- FIGURE (optional, on top as in the Nepalese scribes post): a screenshot of the findings
table, or one evidence card with the Chinese beside it. See points 1, 3 and 4 above.
![alt text]({{ '/assets/images/turfan-fragments-XXXX.png' | relative_url }})
-->

<!-- INTRODUCTION. To check: 4,712 of SHT 1–7426 is the count in IDP's online catalogue
(README of research/turfan-sht), and IDP can be stale; the counts in the last paragraph are
those of the findings page on 17 Nov. -->

So, we had this wonderful workshop in Komazawa and Sendai about Abhidharma texts in the week of 9–13 November 2026. During the workshop, our long time friend, Prof. Kazuo Kano of Komazawa University came up with an idea: what if we apply AI and other computational tools that we have now to identify unidentified Sanskrit manuscript fragments? We decided to first focus on Central Asian manuscript fragments made accessible through the International Dunhuang Programme (IDP). Kano started to work on his own to see if there are fragments of texts he was interested in. He identified a number of until then unidentified fragments. On our side, we started by basically prompting: "Will you identify the fragments that have not been identified?" in Claude Code on our work station. Claude obviously understood that it had to look for identifications in any texts, including those whose Sanskrit texts are not yet known. That meant looking into Chinese and Tibetan translations as well as Pāli texts that might have had Sanskrit equivalents. 

The following paragraph was written by Claude:

"The Sanskrit manuscripts that the German expeditions brought back from Turfan and other sites on the northern Silk Road between 1902 and 1914 are described in the catalogue *Sanskrithandschriften aus den Turfanfunden* (SHT). Its first volume appeared in 1965 and its thirteenth this year. Most of what it describes are fragments: a piece of a leaf with a few broken lines, sometimes only a few letters. The editors have given a text to a great many of them, which is remarkable considering how little there is to go on. Still, many entries carry the label 'noch nicht bestimmt', not yet determined. In the online catalogue of IDP Berlin, 4,712 of the 7,426 catalogue numbers have that label, and others are described only by genre: 'Sūtra-Fragment,' 'Abhidharma-Text.'"

Identifying a manuscript fragment was a time consuming and inefficient job. There may be several degrees of identification. From the quickest to the hardest: 1) You already know the text and once you see what's written on the manuscript, you know what it is; 2) You have a specialized knowledge of the subject matter and you know where to look at. In modern times, this was being increasingly helped by the steady increase of available e-texts. You pick up a few keywords and look for them in your collection, and find the best match; 3) You have some idea what the text is about. But however hard you try, you do not find a good Sanskrit match. You turn Tibetan, Chinese, and Pāli, guessing how the word you are looking for may turn up in the respective languages. Knowing what the fragment is about and knowing where to look in the Tibetan/Chinese/Pali corpora would have been a help, but there are chances you miss the equivalents because the translators used different words, or Chinese letters, from what you expect. 

There is an added difficulty when trying to identify such fragments as those from Central Asia. Often, those fragments are only small pieces of a folio. You do not know how much of the text is lost on the left and right of the folio. Humans would have significant difficulty when such a manuscript piece records one or two words on a line.

Things have changed. For one, Dharmamitra can search the Sanskrit, Chinese, Tibetan and Pāli corpora by meaning. So, we can now identify texts even when their Sanskrit version is not known. Secondly, AI has become so powerful that it can "read"... practically anything, including catalogues and even compare photographs if necessary. This meant that it can create a database just by reading PDF files of the catalogues.

[Mostly Claude] "This post reports what came out. Thirty-six fragments could be given a text and 21 more have a plausible one. Ten confirm a parallel that the editors had already pointed to. There were another 35 identifications we initially thought to have been new identifications but then it turned out they had been identified outside where we were looking. We keep them in the list as evidence our method independently worked."

## The fragments

<!-- - Sources: SHT I–XI and BLSF I–III, read from the printed volumes (OCR).
  - How many entries, how many undetermined or labelled only by genre ("Sūtra-Fragment",
    "Abhidharma-Text").
  - What an entry gives: a few broken lines, often 50–150 legible letters.
  - SHT XII and XIII were not available here (see "Already identified"). -->

## Three ways of finding a text

### Matching against a Sanskrit e-text library

<!-- Runs of letters from the fragment searched in the library; what counts as a match
(letters matched, number of runs, recto and verso in order).
Describe the matcher as it works: the score is how many of the fragment's letters are
covered within a 3,000-letter window of a candidate text. It does not estimate line length
or judge the intervals between matches; spacing was reasoned about only in single cases
(e.g. the join 1927 + 1932). The point moved here from the introduction: a machine can align
the few surviving words of each line with a candidate and judge the match by their intervals.
Present it as what is possible, or as what was done in those cases. One example that is safe to
name, e.g. 1632 Bhadracarī vv. 2–3 or 928 Buddhacarita 11.20–29. -->

### Dharmamitra search

<!-- Semantic search over the Sanskrit, Chinese, Tibetan and Pāli corpora: what it found
that string matching did not, and where it only characterises a piece (genre, type of text)
without identifying it. -->

### Through Chinese, for texts lost in Sanskrit

<!-- The main point for this blog. The fragment is translated into Chinese by the model, the
Chinese is searched in the Taishō, and the hit is then read line by line against the fragment.
  - Why it works for Sarvāstivāda Abhidharma (Jñānaprasthāna, Prakaraṇapāda, Vibhāṣā,
    Nyāyānusāra), which survives only in Xuanzang's translations.
  - One worked example, line by line: e.g. 1732, a Vibhāṣā on shame and dread of blame
    (T 1545, 180a–c; T 1546, 136b), or 1686 (Sarvāstivāda Vinaya, T 1435, 267a).
  - What did not work: the Tibetan route. -->

## What was found

<!-- Counts, then a short table of selected pieces. Candidates that rest on our own work:

| Fragment | Catalogue | Text | Parallel |
|---|---|---|---|
| SHT VII 1632 | undetermined | Bhadracarīpraṇidhāna vv. 2–3 | T 296, 297 |
| SHT III 928 | Sūtra-Fragment | Buddhacarita 11.20–29 | D 4156 |
| SHT III 827 | Medizinisches Fragment | a Śaiva list of tīrthas | |
| SHT VII 1686 | Adhikaraṇavastu or Prātimokṣavibhaṅga (?) | Sarvāstivāda Vinaya | T 1435, 267a |
| SHT IX 2022 | undetermined | Praṇāmastava; joins 2025 f | |
| SHT VI 1433, VII 1685, IX 2028 | undetermined / Abhidharma-Text | Jñānaprasthāna, Prakaraṇapāda | T 1544, T 1542 |
| SHT VII 1732 | Abhidharma-Text | a Vibhāṣā on the Jñānaprasthāna | T 1545, 180a–c |
| Or.15009/386, /362, /105, /76 | (BLSF) | Kokanadasūtra, Poṣadhavastu, Prasādanīyasūtra, MPS 10 | |

  - Check each row against the findings page before use.
  - Joins found from the text, e.g. 2022 + 2025 f.
  - What kinds of text came out: verse (kāvya, stotra), Vinaya, Āgama sūtras, Abhidharma. -->

## Already identified

<!-- The lesson of the study: about a third of the matches (35) had been identified before.
  - Where the earlier identifications sit: the entry's own notes ("Vgl. …"), the Ergänzungen
    of later volumes, SHT XII (2017) and XIII (2026), BLSF, journal articles.
  - IDP's online labels can be stale.
  - Read the other way: the method finds what specialists found, which is a check on it.
  - False matches produced by the parsing of the printed catalogue (merged entries), and how
    they were caught. -->

## Collaboration

<!-- Subject to point 2 at the top.
  - The check of the list against SHT XII and XIII, which moved twenty pieces to "already
    identified".
  - How the exchange went: each side's results checked by the other. -->

## Limitations

<!-- - Only fragments whose text is in the library or in the Dharmamitra corpora can be found.
  - Short fragments: under about 40 letters a match is rarely decisive.
  - "Plausible" means what, exactly; which pieces stay open and why.
  - The transliterations were read from OCR of the printed volumes, not from the manuscripts;
    photographs compared only in a few cases.
  - Literature not checked (name it). -->

## What next

<!-- Optional: other collections where the same method could be tried, if you want to say so. -->

## Acknowledgements

<!-- Collaborators; the editors of SHT and BLSF; IDP Berlin / BBAW and the Staatsbibliothek for the
photographs; the Dharmamitra project. A line on how much of the text and of the work is
AI-written, as in the Nepalese scribes post. -->

## References

<!-- SHT I–XIII (VOHD X); BLSF I–III; Wille's survey in Harrison and Hartmann (eds.), From Birch
Bark to Digital Data (2014); editions used for the identified texts. -->
