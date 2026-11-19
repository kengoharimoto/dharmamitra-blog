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

<!-- THE FRAGMENTS: Claude's draft of 19 Nov 2026, each paragraph in quotation marks as in
the Nepalese scribes post. To check before publishing:
  - The counts of the third and fourth paragraphs and the table were made on 19 Nov 2026 from
    the server data (data/idp_catalogue.tsv, sht_entries.jsonl, fragments.jsonl,
    generic.jsonl, results/xlang*translations.tsv) with the rules of make_fragments.py.
    They are in catalogue numbers; 1,581 = records of fragments.jsonl (1,071) and
    generic.jsonl (510).
  - "Numbers from 5800 on": 5799 is taken as the last number of SHT XI (REVIEW section G).
    Check that, and whether XII and XIII cover all of 5800–7426.
  - "No transliteration printed" = the parsed entry has no transliteration lines. Six
    samples were all tiny scraps described without text; a parser miss would also land here.
  - ON HOLD until the re-parse and re-run on waffle (handoff note there:
    research/turfan-sht/results/PARSER_MISSES.md). Afterwards refresh the table and the
    counts from scripts/count_coverage.py, rewrite the paragraph on the parser, and add
    any new findings.
  - "Missed by the parser" (218), looked into on 19 Nov 2026 with a rough script: 18
    transferred or merged numbers (IDP: "Überführt nach", "Aufgegangen in" and the like);
    175 with the heading glued to the end of the preceding line in the OCR (e.g. 4413, 3485,
    3520); 18 with a heading at line start in an unknown form (2170 with a footnote number,
    "ohne Nummer"); 7 with no heading found (1628, 1688, 4302, 4359, 4360, 4366, 5268).
    About 96 have a run of 8+ letters. These figures are estimates: for numbers below 1000
    the script may have caught index lines and not entries. The 16 searched fragments that
    carry a missed entry's text: 2169 (with 2170, 2171, 2173), 3487, 3961, 4118, 4500, 4557,
    4772, 4779, 4825, 4856, 4934, 4976, 5039, 5219; none is in FINDINGS.html or the
    evidence pages. The parser has not been changed and nothing was re-run.
  - British Library: 768 entries marked unidentified in BLSF I, II.1 and III.1 (126, 137,
    505); 84 without transliteration lines; 377 in data/cas_fragments.jsonl. Parser misses
    were not looked into for these volumes. The last 99 pieces went to Dharmamitra from 30
    letters, so a few more than 159 were sent.
  - 1,075 to Dharmamitra is by the script's threshold (40 legible letters), not counted
    from the query cache. 819 through Chinese is counted from the translation files.
  - INTRODUCTION: IDP's catalogue has entries for 7,304 catalogue numbers; 7,426 is the
    highest number. "4,712 of the 7,426" should be "of 7,304", or "of the numbers up to 7426".
  - OCR: one tool throughout, Chandra OCR 2 (datalab) on the workstation, for SHT I–XI
    (scripts/run_ocr.sh; README; REVIEW section G for VIII and XI) and for BLSF I–III and
    StPSF I (REVIEW section H; scripts/parse_cas_ocr.py). An older pdftotext/Tesseract text
    of the SHT volumes existed but was not used, as it loses the diacritics.
  - Transliterations online: the README of research/turfan-sht says "No transliterations of
    the SHT fragments are online", after looking at idp.bbaw.de and the BBAW Turfan site only.
    You found that the IDP site at the British Library has them and that it blocks machine
    access. The first paragraph says so on your word; the study's notes record no attempt
    on the BL site. The README still carries the wrong statement.
  - The Berlin IDP database and the BBAW Turfan site became inaccessible a few days before
    19 Nov 2026 (your observation), hence "were open to it at the time". The findings table
    and evidence cards now link to the BL site, so the post should point there for
    photographs too.
  - For "Limitations": the text searched is OCR of the printed volumes, because the online
    transliterations could not be read by machine.
  - No transliteration is quoted (point 1 at the top). -->

"The first step was to get the readings of the fragments. While transliterations of the IDP fragments are online, on the IDP site at the British Library, that site blocks automated access; the Berlin IDP database and the Turfan site of the Berlin Academy gave only photographs and, for each fragment, a one-line identification from the online catalogue. (The site became inaccessible after the study.) So, the study read the printed catalogue instead. We ran Chandra OCR over SHT I–XI on our workstation, and a parser cut the result into entries: catalogue number, shelfmark, script type, physical description, transliteration and notes."

"Which entries count as unidentified was decided from IDP's online catalogue. One catalogue number often covers several pieces (a, b, c and so on), and the online catalogue lists each piece separately with its own identification. We counted a catalogue number as undetermined only when all of its pieces are marked 'Noch nicht bestimmt'; a number with some pieces identified and others not was left out. We added a second group: fragments that carry only a label of genre or collection, such as 'Sūtra-Fragment', 'Abhidharma-Text', 'Dhāraṇī' or 'Medizinisches Fragment', or a hedged one ('Wahrscheinlich …'). They are in effect unidentified as well."

"We treated the British Library's Sanskrit fragments from Central Asia in the same way. They are published in the three volumes of *The British Library Sanskrit Fragments* (BLSF), where the editors write an identification into the heading of each piece or mark it 'not yet identified'. These volumes were read with the same OCR and parsed like the SHT volumes."

"IDP's online catalogue marks 4,712 catalogue numbers as 'Noch nicht bestimmt'. Of these, 1,398 have numbers from 5800 on, which SHT I–XI do not describe, so they were out of our reach. That leaves 3,314 undetermined numbers in the volumes we read, and 703 more that have only a genre label: 4,017 in all. In the British Library volumes, 768 pieces are without an identification."

"Most of them could not be searched, because there is nothing to search. For 2,100 of the 4,017 SHT numbers the catalogue prints no transliteration: the entry describes a scrap of one or two centimetres and ends 'noch nicht bestimmt'. Another 103 have a transliteration in which no eight letters in a row are legible. Of the British Library pieces, 391 are too small in the same two ways."

"A further 218 SHT numbers were missed by our parser. We looked into why. Eighteen are not fragments of their own: the number was transferred to another collection or merged into another number. For about 175, the OCR had joined the heading of the entry to the end of the last line of the entry before it, usually at a page break, and the parser looks for a heading at the beginning of a line. Another 18 have a heading in a form the parser did not know, and for seven we found no heading in the OCR at all. About a hundred of the missed entries have enough text to be searched; they have not been searched yet. Where the heading was lost, the text of the entry was read as part of the entry before it. This happened to 16 fragments that we did search. None of them is among the findings."

| | SHT, undetermined | SHT, genre label only | SHT together | British Library |
|---|---|---|---|---|
| Unidentified in the volumes read | 3,314 | 703 | 4,017 | 768 |
| No transliteration printed | 1,985 | 115 | 2,100 | 84 |
| No run of eight legible letters | 90 | 13 | 103 | 307 |
| Missed by the parser | 162 | 56 | 218 | not checked |
| **Not searched** | **2,237** | **184** | **2,421** | **391** |
| **Searched** | **1,077** | **519** | **1,596** | **377** |

"The 1,596 SHT numbers make 1,581 fragments as we searched them, since pieces that the catalogue joins count once. With the 377 British Library pieces, 1,958 fragments were searched. Not all of them were searched in every way. All went through the match against the e-text library. The 1,234 with at least 40 legible letters (1,075 from Berlin, 159 from London) also went to Dharmamitra search, and 936 of those (819 and 117) were sent through Chinese as well. The remaining 724, with fewer than 40 letters, were tried against the e-text library only."

"SHT XII and XIII were not available to us when the searches ran. This matters more than it may seem: each later volume carries additions and corrections to the earlier ones, among them lists of fragments that have been identified since. We come back to this below."

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
