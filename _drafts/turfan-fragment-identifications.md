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
post moves to _posts/. Numbers are those of the findings page on 21 Nov 2026, 18:22 (research
commit 3777ce5; 140 rows: 63 identified, 34 plausible, 8 editors' leads confirmed, 35 already
identified elsewhere; at 13:43 138 rows: 61, 34, 8, 35; that morning 134 rows: 56, 34, 9, 35; on 17 Nov 102 rows: 36, 21, 10, 35); refresh them from research/turfan-sht
(GitHub: kengoharimoto/etexts-research) before publishing.

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

<!-- INTRODUCTION. To check:
  - 4,712 of 7,304 is the count in IDP's online catalogue (scripts/count_coverage.py: IDP
    has entries for 7,304 catalogue numbers, the highest is 7426), and IDP can be stale.
  - Last two paragraphs, adjusted on 21 Nov 2026 from the README and
    results/XII_XIII_MISSES.md. "About 100 matches" = the 102 rows of 17 Nov, the 35
    already identified among them. Of the 35 now (README as rewritten on 21 Nov, commit
    5e53618): 19 from K. Kano's check of SHT XII and XIII and his list of 20 Nov, 15 found
    in SHT I–XI, BLSF and the literature, one against its printed entry (1746). The split
    by collection in the last sentence is the README's table. Kano's list of 20 Nov has
    111 rows: 11 already marked as known here, 60 never searched, 4 with only the Chinese
    side identified, 36 searched and missed. The text does not make this split (your word,
    21 Nov): the 60 should have been looked at in the first place, so all count as
    missed. "About three dozen" is yours; the rows added
    on 20–21 Nov cover about 35 catalogue numbers, joined pieces counted singly. The last
    sentence gives the findings page of 21 Nov.
  - The new rows of 20–21 Nov are not yet checked against SHT XII and XIII
    (results/FOR_KANO.md: 34 Berlin rows, 23 identified and 11 plausible, and 1519, whose
    proposal changed after K. Kano's check). The British Library rows are checked against
    BLSF I–III only, some also against Chung 2008 and Wille's survey of 2014.
  - Counts by collection in the last sentence: README table at commit 3777ce5 (Berlin
    44 / 26 / 6 / 33, British Library 17 / 7 / 2 / 2, St Petersburg 2 / 1 / – / –). -->

So, we had this wonderful workshop in Komazawa and Sendai about Abhidharma texts in the week of 9–13 November 2026. During the workshop, our long time friend, Prof. Kazuo Kano of Komazawa University came up with an idea: what if we apply AI and other computational tools that we have today to identify unidentified Sanskrit manuscript fragments? We decided to first focus on Central Asian manuscript fragments made accessible through the long standing German publications of Central Asian Sanskrit manuscript collection and now the International Dunhuang Programme (IDP). 

Kano started to work on his own to see if there are fragments of texts he was interested in. He identified a number of until then unidentified fragments. On our side, we started by basically prompting: "Will you identify the fragments that have not been identified?" in Claude Code on our work station. Claude obviously understood that it had to look for identifications in any texts, including those whose Sanskrit texts are not yet known. That meant looking into Chinese and Tibetan translations as well as Pāli texts that might have had Sanskrit equivalents.

This post is about the project that initially took a night. And here is the results. This may be updated from time to time. We will try to make the source—tables and scripts, etc.—available via GitHub. The whole web pages do not require anything else. So, one might just download the html files and consult the table locally.

https://claude.ai/artifact/APfbfj2ydCB1wb6QnfqSo9

The following paragraph was written by Claude:

"The Sanskrit manuscripts that the German expeditions brought back from Turfan and other sites on the northern Silk Road between 1902 and 1914 are described in the catalogue *Sanskrithandschriften aus den Turfanfunden* (SHT). Its first volume appeared in 1965 and its thirteenth this year. Most of what it describes are fragments: a piece of a leaf with a few broken lines, sometimes only a few letters. The editors have given a text to a great many of them, which is remarkable considering how little there is to go on. Still, many entries carry the label 'noch nicht bestimmt', not yet determined. In the online catalogue of IDP Berlin, 4,712 of the 7,304 catalogue numbers have that label, and others are described only by genre: 'Sūtra-Fragment,' 'Abhidharma-Text.'"

Identifying a manuscript fragment was a time consuming and inefficient job. There may be several degrees of identification. From the quickest to the hardest: 1) You already know the text and once you see what's written on the manuscript, you know what it is; 2) You have a specialized knowledge of the subject matter and you know where to look at. In modern times, this was being increasingly helped by the steady increase of available e-texts. You pick up a few keywords and look for them in your collection, and find the best match; 3) You have some idea what the text is about. But however hard you try, you do not find a good Sanskrit match. You turn to Tibetan, Chinese, and Pāli, guessing how the word you are looking for may turn up in the respective languages. Knowing what the fragment is about and knowing where to look in the Tibetan/Chinese/Pali corpora would have been a help, but there are chances you miss the equivalents because the translators used different words, or Chinese letters, from what you expect. 

There is an added difficulty when trying to identify such fragments as those from Central Asia. Often, those fragments are only small pieces of a folio. You do not know how much of the text is lost on the left and right of the folio. Humans would have significant difficulty when such a manuscript piece records one or two words on a line.

Things have changed. For one, Dharmamitra can search the Sanskrit, Chinese, Tibetan and Pāli corpora by meaning. So, we can now identify texts even when their Sanskrit version is not known. Secondly, AI has become so powerful that it can "read" ... practically anything, including catalogues and even compare photographs if necessary. This meant that it can create a database just by reading PDF files of the catalogues.

Initially, we tried to identify fragments in SHT I–XI that were not yet identified or for which only the genre was mentioned. We came up with about 100 matches. Then volumes XII and XIII became available to Kazuo Kano and he compared our identifications with them. Thirty-five of our matches had already been identified: 19 in volumes XII and XIII, and 16 in the volumes we had read ourselves (SHT I–XI and BLSF) or elsewhere in the literature, for instance in the additions and corrections that each volume carries to the earlier ones. It was a good thing. For one, we got confirmations that our identifications were correct.

On the other hand, Kano's list of what volumes XII and XIII newly identify had about 100 items that our pipeline had not identified. We analyzed why and improved our methodologies. After that, we identified or proposed plausible candidates for about three dozen more items. Along the way we also took in the British Library's fragments and made a start on those in St. Petersburg. As of 21 November, our list has 140 rows: 63 identified (44 from Berlin, 17 from the British Library, 2 from St. Petersburg), 34 plausible (26, 7 and 1), 8 that confirm a lead the editors give, and 35 that were already identified.

What follows is how it was done in some details, mostly written by Claude. One may read "Claude" when the following says "the study." The text in brackets are added by me.

## The fragments

<!-- THE FRAGMENTS: Claude's draft of 19 Nov 2026, revised on 21 Nov 2026 after the re-parse
and the work of 19–21 Nov (research/turfan-sht on GitHub, etexts-research, commit 9f4b7d1;
README, results/REVIEW.md sections Q–AB, results/XII_XIII_MISSES.md). Each paragraph in
quotation marks as in the Nepalese scribes post. To check before publishing:
  - The counts and the table are the output of scripts/count_coverage.py, run on waffle on
    21 Nov 2026 at commit 3d581bf (again after the British Library re-parse; the SHT
    figures are as at 9f4b7d1). They are in catalogue numbers; 1,644 = records of
    fragments.jsonl (1,112) and generic.jsonl (532). Run it again if the data change.
  - "Through Chinese" (986 = 477 + 382 + 127) also counts results/reparse_xlang_translations.tsv,
    which count_coverage.py does not read yet (its own figure is 943). Five of the 986 have
    fewer than 40 letters. This is the first route, with the translation model.
  - 1,107 + 172 to Dharmamitra is by the script's threshold (40 legible letters), not counted
    from the query cache.
  - "Numbers from 5800 on": 5799 is taken as the last number of SHT XI (REVIEW section G).
    Check that, and whether XII and XIII cover all of 5800–7426.
  - "No transliteration printed" = the parsed entry has no transliteration lines. Six
    samples were all tiny scraps described without text; a parser miss on the lines would
    also land here. The figure rose from 2,100 to 2,228 with the re-parse: most of the
    entries the parser had missed print no text.
  - The parser paragraph follows REVIEW section Q. The re-parse was done by a subagent; six
    cases of its report were checked again, the rest was not (Q says so). The 25 numbers
    without an entry: "16 transferred, 9 without a description of their own" is Q's wording;
    results/parser_missed.tsv lists them. README, Open points, still lists as to do "review
    the hits of the 139 new or changed records"; the paragraph therefore says only that
    they were searched.
  - British Library, after the heading check of 21 Nov (REVIEW AC): 894 entries marked
    unidentified in BLSF I, II.1 and III.1 (127, 150, 617); 93 without transliteration
    lines; 429 in data/cas_fragments.jsonl; 372 = the rest. Before: 768, 84, 377. 2,755
    entries (2,549); 206 recovered, of which 116 unidentified with printed text, 52 with
    a run of eight letters. The Dharmamitra search of the 52 was run from 30 letters
    (17 pieces), the count above is by the 40-letter threshold. Their verdicts are in
    REVIEW AC, not in the ledger. Gaps that remain in the shelfmark series (14) are joins
    named under another shelfmark or pieces not printed; hence "–" in the table.
  - The eighth paragraph (reading against a text) follows REVIEW AD–AG. 1519's plural
    refuge agrees with Yijing's Chinese; the Tibetan and the Divyāvadāna have one man.
  - The Dharmamitra index gap (1,500 of 3,274 Sanskrit files of the local database not
    returned by the search; REVIEW section X) is stated in the seventh paragraph. Decide
    whether the blog should say this, and in which words; it concerns the local stack on
    the workstation as queried on 20–21 Nov.
  - OCR: one tool throughout, Chandra OCR 2 (datalab) on the workstation, for SHT I–XI
    (scripts/run_ocr.sh; README; REVIEW section G for VIII and XI) and for BLSF I–III and
    StPSF I (REVIEW section H; scripts/parse_cas_ocr.py).
  - Transliterations online: the README of research/turfan-sht still says "No transliterations
    of the SHT fragments are online". You found that the IDP site at the British Library has
    them and that it blocks machine access. The first paragraph says so on your word.
  - idp.bbaw.de answered again on 22 Nov 2026 (REVIEW AI; item pages by pressmark); the
    first paragraph says so. You wanted to say that the Berlin site is deprecated. A web check on 22 Nov found no
    statement of that: the BBAW page on IDP Berlin (turfan.bbaw.de/idp-berlin-en.html)
    speaks of idp.bbaw.de in the present tense; Wikipedia (International Dunhuang
    Programme) says London maintains the IDP database and the main English-language
    website, that the other centres "previously maintained local-language versions" and
    that "efforts are ongoing to unify the IDP's digital platforms", and lists Berlin among
    the centres with active websites. idp.bl.uk/about could not be read (403). So the
    sentence says only that the BL site is the main one. Ask IDP or the Turfanforschung if
    you want to say more. Whether the Academy's Turfan site is back is not in the notes.
  - The Berlin IDP database and the BBAW Turfan site became inaccessible a few days before
    19 Nov 2026 (your observation). Check whether they are back before publishing. The
    findings table and evidence cards link to the BL site, so the post should point there
    for photographs too.
  - St Petersburg: the fourth paragraph, added on 21 Nov at your word, from the README
    (section "St Petersburg"), REVIEW O and P and data/stpetersburg_online_survey.md.
    "508 of roughly 700" is Mesheznikov & Shomakhmadov 2020, p. 27, as quoted in the
    survey ("the overwhelming majority of the Buddhist Sanskrit texts (508 items) have not
    been identified"); "most unpublished" rests on Mesheznikov & Klementeva 2026, p. 93
    ("only about 100 items" in circulation). Neither article was read for this post. The
    2021 pieces are Lundysheva, Maue and Wille, WMO 7/1–2 (data/stp_fragments.jsonl, 35
    records; stp_pam3.jsonl, 17).
    The St Petersburg pieces are not in the table or in the counts of fragments searched.
    The title and the description still say Turfan; SI P/16 is from Kucha, the anthology
    from Merv.
  - No transliteration is quoted (point 1 at the top). The README now records your word of
    18 Nov that quoting SHT transliterations is fine and that the BBAW's rules concern the
    photographs. -->

"The first step was to get the readings of the fragments. While transliterations of the IDP fragments are online, on the IDP site at the British Library, that site blocks automated access; the Berlin IDP database and the Turfan site of the Berlin Academy gave only photographs and, for each fragment, a one-line identification from the online catalogue. (Both became inaccessible in mid-November, while the study was under way. The Berlin IDP database was online again on 22 November. Our list still links to the British Library's site, which is the main site of IDP.) So, the study read the printed catalogue instead. We ran Chandra OCR over SHT I–XI on our workstation, and a parser cut the result into entries: catalogue number, shelfmark, script type, physical description, transliteration and notes."

"Which entries count as unidentified was decided from IDP's online catalogue. One catalogue number often covers several pieces (a, b, c and so on), and the online catalogue lists each piece separately with its own identification. We counted a catalogue number as undetermined only when all of its pieces are marked 'Noch nicht bestimmt'; a number with some pieces identified and others not was left out at first. [Upon realizing that some apparent ones were not searched, w]e added a second group: fragments that carry only a label of genre or collection, such as 'Sūtra-Fragment', 'Abhidharma-Text', 'Dhāraṇī' or 'Medizinisches Fragment', or a hedged one ('Wahrscheinlich …'). They are in effect unidentified as well. [This is an example of transmitting nuances to AI. For me, it is apparent those should have been searched in the first place.]"

"We treated the British Library's Sanskrit fragments from Central Asia in the same way. They are published in the three volumes of *The British Library Sanskrit Fragments* (BLSF), where the editors write an identification into the heading of each piece or mark it 'not yet identified'. These volumes were read with the same OCR and parsed like the SHT volumes."

"For the St. Petersburg collection we could only make a start. No catalogue of it has been published; according to a survey of 2020, 508 of its roughly 700 inventoried Sanskrit items are unidentified, and most are unpublished. We worked on what is in print. The one volume of the *St. Petersburg Sanskrit Fragments* (StPSF I) that we have edits manuscripts that are identified, but by the editors' own count 46 stories of its avadāna anthology from Merv are not. Forty-four of them could be recovered from the OCR and were searched through Chinese, Sanskrit and Pāli, and no parallel was found. Besides these, the pieces of the Berezovsky and Krotkov collections published in 2021, the Petrovsky pieces reprinted in *Pamjatniki* 3, and SI B/24,14 and SI P/16 went through the same matchers. Three of them are on our list. They are not counted in the table below."

"IDP's online catalogue marks 4,712 catalogue numbers as 'Noch nicht bestimmt'. Of these, 1,398 have numbers from 5800 on, which SHT I–XI do not describe, so they were out of our reach. That leaves 3,314 undetermined numbers in the volumes we read, and 703 more that have only a genre label: 4,017 in all. In the British Library volumes, 894 pieces are without an identification."

"Most of them could not be searched, because there is nothing to search. For 2,228 of the 4,017 SHT numbers the catalogue prints no transliteration: the entry describes a scrap of one or two centimetres and ends 'noch nicht bestimmt'. Another 106 have a transliteration in which no eight letters in a row are legible. Of the British Library pieces, 465 are too small in the same two ways."

"The parsers needed more than one round. In the first run the SHT parser missed 218 of the 4,017 numbers. For most of them the OCR had joined the heading of the entry to the end of the last line of the entry before it, usually at a page break, and the parser looked for a heading at the beginning of a line. Where a heading was lost, the text of the entry was read as part of the entry before it. We changed the parser and parsed all volumes again on 19 November. This added 279 entries, and 88 entries gave up lines that belong to the number after them. 

Three identifications that were already on our list turned out to rest on the next number's text and were withdrawn (SHT 963, 3238 and 3299 + 4187), and one moved from 1957 to 1958. The 139 fragments that were new or had changed were searched like the others. Twenty-five numbers are still without an entry: sixteen were transferred to another collection or merged into another number, and nine have no description of their own. A second correction on 21 November, for headings lost in SHT I and IV, changed no finding. The same check was then made for the British Library volumes, where the shelfmarks of each series should run without gaps. They did not: 206 entries were missing, because the parser expected a heading in bold and the OCR gives many without. Of the 206, 52 are unidentified pieces with enough text to search. They went through all the searches and were read; two of them could be given a text, and a third plausibly. No piece searched before changed its text."

| | SHT, undetermined | SHT, genre label only | SHT together | British Library |
|---|---|---|---|---|
| Unidentified in the volumes read | 3,314 | 703 | 4,017 | 894 |
| No transliteration printed | 2,099 | 129 | 2,228 | 93 |
| No run of eight legible letters | 92 | 14 | 106 | 372 |
| No entry (transferred, merged or not described) | 5 | 20 | 25 | – |
| **Not searched** | **2,196** | **163** | **2,359** | **465** |
| **Searched** | **1,118** | **540** | **1,658** | **429** |

"The 1,658 SHT numbers make 1,644 fragments as we searched them, since pieces that the catalogue joins count once. With the 429 British Library pieces, 2,073 fragments were searched. Not all of them were searched in every way. All went through the match against the e-text library. The 1,279 with at least 40 legible letters (1,107 from Berlin, 172 from London) also went to Dharmamitra search, and 986 fragments (859 and 127) were sent through Chinese as well. The remaining 794, with fewer than 40 letters, were tried against the e-text library only."

"After the comparison with SHT XII and XIII, described below, the same fragments were gone through again in three more ways. Each entry was cut into blocks, one side of one piece, 4,912 in all, and matched block by block, with a lower threshold and a test that the hit is not shared by many works. At first a short hit was kept only when it was in a Buddhist text; the hits dropped for that reason were read afterwards. This run also took in 72 catalogue numbers of mixed status, with some pieces identified and others not, which the first run had left out. The Sanskrit files that are in the Dharmamitra database but were not returned by the search we queried, 1,500 of 3,274, were written out and matched directly. And the route through Chinese was built a second time without a translation model: a table of 1,080 Sanskrit stems with the renderings of the Chinese translators, by which the terms of a fragment are searched in the Taishō in the order they have in the fragment."

"Last, some fragments were not searched again but read against a text that an earlier result pointed to. Three were collated with the Pāli. The fragments that the editors compare with the Divyāvadāna were read against the Chinese and Tibetan Vinayas, since much of the Divyāvadāna is taken from the Mūlasarvāstivāda Vinaya. And when one fragment turned out to stand in the numerical section of the Sarvāstivāda Vinaya (T 1435, 346a–378c), the 44 longer passages of that section were read through for other fragments. Two pieces moved from plausible to identified in this way, and a British Library piece was found to be the list of headings that opens the Vinayamātṛkā."

"SHT XII and XIII were not available to us when the first searches ran. This matters more than it may seem: each later volume carries additions and corrections to the earlier ones, among them lists of fragments that have been identified since. K. Kano checked our list against both volumes and, on 20 November, sent a list of the 111 fragments that they newly identify, join or correct. We come back to this below."

## Methods

<!-- METHODS: Claude's prose of 21 Nov 2026, each paragraph in quotation marks, written from
the README (Method, steps 5–13) and results/REVIEW.md of research/turfan-sht at commit
3d581bf; "Matching by piece" revised at commit 3777ce5 (REVIEW AH). Six subsections, ordered by kind (each later method follows the one it grew out
of), not by date; "The fragments" tells the order in time. To check, for all of them:
  - Short pieces of transliteration are quoted (1632, 1686, 1309, 1420, 1946, 4501,
    Or.15009/468), on your word of 18 Nov that quoting SHT transliterations is fine; point 1
    at the top still stands for the British Library piece.
  - Fragments named as examples must be cleared (point 2 at the top). Of those named as
    new, only 1632, 1686, 1433, 1685 and 2028 were on the page at K. Kano's check of
    13 Nov; 23, 1630, 1946, 1837, 1380, 1574, 1622, 2094, 1252, 4501, 1883, 1519 are not checked
    against SHT XII and XIII.
  - Figures are those of the notes; none was recounted for this section. -->

### Matching against a Sanskrit e-text library

<!-- README step 5; XII_XIII_MISSES.md for the thresholds. 1632: REVIEW A (88 of 104
letters, 3 runs). "About a minute" is on 100 cores of the workstation. The last paragraph
keeps the point that the matcher does not judge intervals; 1927 + 1932 are K. Kano's
subject (Kano 2027), named here only as the case where spacing was reasoned about: check
with him or take the sentence out. -->

"The first search is a plain one: does the wording of the fragment stand in a Sanskrit text that we have as a file? The library is a collection of 6,503 Sanskrit e-texts. A fragment is not a continuous text, so each transliterated line is cut at its lacunae into runs, stretches of letters with no gap. The editors' brackets are dropped and the letters kept. Runs and library are then folded in the same loose way, so that differences of spelling do not count: no diacritics, *b* and *v* alike, double consonants single, the nasals alike."

"Each run is broken into overlapping pieces of ten letters, and the pieces are looked up in the library. Pieces that occur in more than forty files are thrown out as stock. For every fragment and every file, the score is the number of the fragment's letters that are covered within the best stretch of 3,000 letters of that file. A hit is kept when two runs together cover 26 letters, or one run 30. All fragments against all files take about a minute."

"We tried the matcher first on 790 fragments that the catalogue does identify. It found a text for 273 of the 396 with a hundred legible letters or more, for 48 of the 203 with forty to a hundred, and for almost none below forty. When sixty letters or more were covered, the text was nearly always the right one or a parallel version of it. What it missed were mostly texts that survive only in Chinese, Tibetan or Pāli. A clear case among the undetermined fragments is SHT VII 1632: 88 of its 104 letters, in three runs, stand in verses 2 and 3 of the Bhadracarī (*kṣetrarajopamakāyapramāṇaiḥ sarvajināna karomi praṇāmam*)."

"The matcher counts letters. It does not estimate how long a line of the leaf was, and it does not judge whether the distances between the matched words fit the lost text between them. That was reasoned about only in single cases, such as the question whether SHT 1927 and 1932 are two pieces of one leaf."

### Matching by piece

<!-- REVIEW Y, Z; README step 12; XII_XIII_MISSES.md, cause C and the 60 never searched.
The block count is 4,912 after the parser fix of 21 Nov (4,963 before); "22 per cent" is
144 added to 647 on the identified fragments, 26 per cent is 170 (REVIEW Y). The third and
fourth paragraphs follow REVIEW AH (21 Nov, commit 3777ce5), written after your objection
to the Buddhist-only rule; the paragraph does not name you, add a bracket if you wish. The
figure given here before, 247 of 372 short hits outside Buddhist texts, was wrong (the
count tested the file name without its path); the right figures are 115 outside and 365
in Buddhist files. The rule is still in the script as a filter for the main list; what it
drops now goes to results/block_candidates_other.tsv and is read. The 115 by place:
śāstra 38, Śaiva and Vaiṣṇava texts 25, Dharmamitra files outside the index 16, kāvya,
drama, poetics and anthologies 13, purāṇas 11, Mahābhārata 8, Veda 3, an inscription 1.
SHT 23: the hit was 29 letters in one run, in the Rājanighaṇṭu; the leaf is in Gupta
script, the nighaṇṭu is much later, so "found in" and not "from". "Another scribe" is
the editors' observation ("von einem anderen Schreiber geschrieben"). 1630: Subhāṣitāvalī
3320 is marked sārāśītyām there. Neither is checked against SHT XII and XIII (SHT XIII
has 23 c as Tridaṇḍamālā 3.3.11). -->

"In the first run the unit was the catalogue number, with all its pieces pooled. The comparison with SHT XII and XIII showed what this costs. SHT V 1198 has the Saddharmapuṇḍarīka on two of its pieces and, as SHT XIII now says, the Madhyāntavibhāgabhāṣya on a third; the number was taken as one text and the third piece was not looked at again. And a number with some pieces identified and others not was in neither of our sets."

"So each entry was cut into blocks, one side of one piece each: 4,912 blocks, those of 72 numbers of mixed status among them. The same matcher was run with lower thresholds. Lower thresholds alone bring in chance, since a short phrase may stand in many texts. A short hit is therefore kept only when no more than two other works come near it."

"At first there was a second condition: the text had to be a Buddhist one. The reason was that most short hits in purāṇas, tantras and kāvya are chance. On the identified fragments the rule adds 22 per cent to the hits with this condition and 26 per cent without it. [I objected to this restriction upon reading about it in this blog draft. I expressed my concern to Claude on the workstation. Then...] But the condition shut out the literature that only this search can reach. The routes through Chinese and Tibetan lead to Buddhist texts by their nature; a medical text, a grammar or a poem can be found only in the library. The test was also a blunt one. It went by the place of a file in the library, so the Buddhacarita passed it, and the Saundarananda, which is filed under kāvya, did not. Longer hits were never under the condition, and two pieces of the Yogaśataka, a medical text, had been found by them."

"So the 115 short hits that the condition had dropped were read as well. Most are indeed chance: single words shared with a kāvya, or stock phrases of Buddhist verse and of spells that the purāṇas and tantras have too. Two are real. On leaf b of SHT I 23 another scribe wrote three verses in praise of buttermilk after the verses on a caitya, and these verses are found in the medical glossaries (Rājanighaṇṭu 15.56–57, one of them also in the Bhāvaprakāśa). Verse 12 of SHT VII 1630, a verse text on rebirth and impermanence, is no. 3320 of Vallabhadeva's Subhāṣitāvalī (*narakanilayāt pretāvāsaṃ* …); the work to which the fragment belongs is still unidentified. For three more fragments we could name only the type of text, not the text itself: SHT VII 1665 is a grammatical commentary on the suffixes of descent, and 1620 and 1641 are two manuscripts of verses on a preparation against old age. The hits outside Buddhist texts are now written to a list of their own on every run, and that list is read."

"Among the Buddhist texts, the matching by piece recovered pieces that SHT XIII has and that we had missed by a few letters, among them 1198 a. Some of the blocks with a hit belong to catalogue numbers for which we had recorded nothing so far, neither an identification nor a verdict on an earlier hit. These blocks were read one by one. Four could be given a text: SHT VI 1380 (Madhyamāgama 28), 1574 piece b (the Larger Prajñāpāramitā, chapter 76), VII 1622 (a set of maṅgala verses) and IX 2094 (verses of the Abhidharmakośa without the Bhāṣya). Of the forty mixed numbers that had hits, 29 only confirmed the pieces already named; one gave something new, pieces b and c of SHT VI 1252. What this search still does not reach are pieces of a line with fewer than ten letters."

### Dharmamitra search

<!-- README step 7; REVIEW E, X; XII_XIII_MISSES.md, cause B. The second paragraph is a
judgement of mine from the notes: no row of the page rests on the Dharmamitra search of
the Sanskrit alone, as far as the notes show (not checked row by row). You may see it
differently; this is the Dharmamitra blog. The third paragraph states the index gap;
decide whether and how to say it (note in "The fragments"). The paragraph on 4217 follows REVIEW AI (22 Nov, research commit 147f4d0), written after your two points (the Nayacakra may report a rival school, so read the context; the ink of 4217 is faded); it does not name you. The Nayacakra is Mallavādin's, with Siṃhasūri's commentary (Jambūvijaya's edition); 38,392 segments read from the local database; the two passages are segments 10955 and 5585. The other neighbour was Durveka. The Sängim manuscript: SHT VII 1747, VIII 1903, 1904, 1906, 1907, 1908, X 3278; it names a kośāntarakārikāvṛtti and treats Kośa V 7–8. Measured on the photographs: lines 1.14 cm apart in 1907, 1.2 in 1908 and 4217; a letter about 0.65 cm wide in 1907, 0.6 in 4217. The find-place of 4217 is not known. Claude's reading of the subject (the life faculty and the attainments without mind, Kośa II 41–45) is uncertain and is not in the paragraph. 4217 stays "type of text only" on the page. The composite photograph is not published (point 4 at the top). "Ascribed to Aśvaghoṣa" is from the database's file names (SA_T10_Aśvaghoṣa_Tridaṇḍamālā); check how you want the work described. Cause B of XII_XIII_MISSES.md has six rows, seven with 646. The search used was the local
stack on the workstation. -->

"Dharmamitra searches the Sanskrit, Chinese, Tibetan and Pāli corpora, by wording and by meaning. Fragments with at least forty legible letters were sent to it: one search by wording for each run of fifteen letters or more, up to six runs, and one search by meaning for the fragment as a whole, with its runs joined. A work counts as a candidate when two of these searches have it among their first five results."

"For Sanskrit texts the search mostly confirmed what the library match had found; for SHT 1632 it named the Gaṇḍavyūha and the Bhadracarī as well. Where no text could be found it often still told us what type of text a fragment is."

"[A first draft of this part by Claude said something completely different. The follow-up research and new findings on it were literally prompted by my query.] How far such a neighbour can be trusted shows in SHT X 4217. The fragment has inferences that give a reason with a similar and a dissimilar example (*… vāyuvat, vaidharmyeṇa* …). The search by meaning put two passages of the Nayacakra next to it, a Jaina work that reviews the doctrines of other schools, so it might have been reporting the argument of the fragment. We read the whole Nayacakra, taken from the Dharmamitra database, and it is not. The two passages are inferences of the same build on other matters, and the terms of the fragment do not come together anywhere in the work. The search had matched the form of the argument. A better lead is in the catalogue itself. The entries of 4217 and of SHT VIII 1907 refer to each other for the phrase *vaidharmyeṇa śaśaviṣāṇam*, 'by unlikeness: a hare's horn'. According to the editors, 1907 belongs to a manuscript from Sängim of an unknown commentary on an Abhidharma text, of which seven numbers are known. On the photographs the two agree in the format of the leaf, the distance between the lines and the size of the letters. Whether 4217 is a piece of that commentary, or of that manuscript, is open; the letter forms need the eye of a palaeographer."

"The larger part of Dharmamitra in this study was another one. The Chinese, Tibetan and Pāli that the next subsections use were searched and read in Dharmamitra: the Chinese for the route by translation, the Pāli for the collations, the Tibetan for the two pieces it confirmed."

"One limit came to light through SHT XIII. Many of its identifications rest on the *Tridaṇḍamālā*, an anthology ascribed to Aśvaghoṣa. Eighteen files of that work are in the Dharmamitra database, but the search we queried did not return them, not even for their own sentences. A test of the whole Sanskrit collection showed the same for 1,500 of 3,274 files. We wrote these files out and ran them through the library matcher. With the *Tridaṇḍamālā* files, several of the SHT XIII identifications came out, and so did two fragments that are not among them, SHT VIII 1877 and 1883. The other files confirmed one more and brought nothing new."

### Through Chinese, by translation

<!-- REVIEW I, AA; XII_XIII_MISSES.md, cause E. The example is 1686, not 1732 as the old
note proposed: 1732 was among the hits of this route that were not kept, and was
identified later by reading (REVIEW L). 976/986 fragments went this way (see "The
fragments"). The model is the local mitra-chat-qwen (Ollama); name it if you wish. 1433 at
T 1543, 800b; 1685 at T 1542, 743b; 2028 at T 1542, 705c–706b. 1389 and 1854+1861 are in
SHT XII (J. Chung). -->

"Much of what the Turfan fragments contain is lost in Sanskrit. The canonical Abhidharma of the Sarvāstivādins, the Jñānaprasthāna, the Prakaraṇapāda, the Vibhāṣā, survives in the Chinese of Xuanzang and his predecessors, and so do the Āgamas and the Sarvāstivāda Vinaya. No match against Sanskrit files can find such a fragment. For fragments of forty letters or more without a confirmed Sanskrit text, the four longest lines were therefore translated into classical Chinese by a language model, and each translation was searched in the Chinese canon. A work counts when two lines have it among their first five results. Every hit that was kept was then read against the Taishō, line by line."

"SHT VII 1686 shows how it works. The online catalogue has it as 'Adhikaraṇavastu oder Prātimokṣavibhaṅga (?)'. Its lines speak of a suspended monk, one who sides with him, and one who sides with that one: *utkṣiptaka*, *anuvartaka*, and *anuvartaka* again. The search led to the Sarvāstivāda Vinaya, where Upāli asks who is able to split the community (T 1435, 267a), and the Chinese has the same three in the same order: 擯比丘、隨順擯比丘、助隨順擯比丘. In this way SHT VI 1433 was placed in the Jñānaprasthāna and VII 1685 and IX 2028 in the Prakaraṇapāda. Two more fragments that the route gave to the Jñānaprasthāna, 1389 and 1854 + 1861, turned out to be identified in SHT XII already, at the same passages."

"The route fails in two ways. The model translates the sense, and the search needs the translators' words. In SHT VI 1309 it rendered *nirodhadarśanaprahātavya*, 'to be abandoned by seeing cessation', as a free sentence where Xuanzang writes 見滅所斷, and the Jñānaprasthāna did not come up; SHT XII has the fragment at T 1544, 992b–c. In SHT VI 1420 it took *śivapathikā* for a charnel ground, 屍陀林, where the Madhyamāgama has 息止道. And the four longest lines of a fragment are not always the ones that decide: in SHT XI 4442 they are connecting phrases. The same step into Tibetan gave nothing that survived reading. The model repeated stock phrases, or wrote the Sanskrit in Tibetan letters."

### Through Chinese, by the translators' terms

<!-- REVIEW AA, AC; README step 10. "Written in the course of the study" = by Claude, from
its knowledge of the translations, not from a dictionary; REVIEW AA says "written by
hand". Calibration figures are those of the second run (1,080 stems): 17 and 27 of 33.
1946 at T 1544, 931c10–20; 1837 at T 1544, 962a13–22; 1439 + 1753 + 1986, cf. T 1545,
852c–856b. The false candidate for Or.15010/40 (-gāmī read as anāgāmin) is an example of
the folding's cost, if one is wanted. -->

"The second route through Chinese uses no model. It rests on a table of 1,080 Sanskrit stems with the words that the Chinese translators use for them: Xuanzang, the older translators of the Abhidharma, those of the Āgamas and the Vinayas. For *nirodhadarśanaprahātavya* the table has 見滅所斷, 見滅斷 and 盡諦所斷. The table was written in the course of the study, not taken from a dictionary, and it can be extended."

"The stems that occur in a fragment, in the order they have there, are its sequence of terms. A stem cut off by a lacuna counts when more than half of it stands at the edge of a run. All renderings are located in volumes 1 to 32 of the Taishō, some 41 million characters. Every stretch of 320 characters is scored by the terms of the fragment that it contains, a rare term weighing more than a common one, and the best stretches are scored again by order: only terms that follow each other in the Chinese as they do in the fragment count. All fragments, block by block, take under two minutes."

"The route places the fragments that the first route or SHT XII had placed, SHT 1309 among them, at the passage SHT XII gives. Tried on entries whose label names a work that exists in Chinese, it has the right work first in about half of the cases and among the first three in about four of five. So it proposes a place, and reading decides. Read against the Chinese, its candidates gave SHT VIII 1946 and 1837, both Jñānaprasthāna. In 1946 the count of the latent defilements ends with *(ārūpya)pratisaṃyuktā ekatriṃśa(t)*, thirty-one that belong to the formless realm, 三十一無色界繫 in the Chinese. SHT VI 1439, VII 1753 and VIII 1986 came out as pieces of one text, which has the Mahāvibhāṣā's sets of four alternatives on the attainments but is not Xuanzang's text word for word."

"Its limits are plain. A fragment needs at least three terms of the table. The formulas of the Abhidharma recur, so the best place is often one of several equal ones, in the root text and in its commentaries. The table has no verse and little plain narrative, and a sūtra with no doctrinal terms, no stock phrases and no names stays out of reach."

### Reading against a text

<!-- REVIEW T (ledger; the figures 167 / 154 / 153 / 144 are of REVIEW AB and the count on
waffle), H, Z, AD–AG. The reading was done by Claude; your introduction says so for "the
study". The last paragraph should say what you or K. Kano checked; I have written only
what the notes record (Kano's check of 13 Nov, the 34 rows not checked). 4501: AN 3.99 as
numbered on SuttaCentral (PTS 3.97–98). Or.15009/468: T 1441, 593b29–c6; D 7A, pa
233b–234b. 1883: T 1435, 356a13–b19. 1252: T 1435, 353b2–c7. -->

"None of these searches identifies anything. Each one proposes a text, and the proposal is then read: the lines of the fragment, in their order, against the lines of the text. The cards of our list show this reading. Most proposals do not survive it. The record of verdicts has 787 candidates, and for most of them the verdict is not an identification: the hit tells only the type of text (167), the text is already named in the printed entry (154), the shared wording is a stock phrase (153), or the hit is chance (144)."

"That record did not exist at first, and this cost us. Four of the identifications of SHT XIII had been among our hits and were passed over, because no verdict had been written down for them. Since 20 November every candidate has one."

"Reading also does what the searches cannot. It can tell a text from another that quotes it: SHT VIII 1877 matched a chapter of the *Tridaṇḍamālā*, but it repeats the chapter's formula with other objects, so it is the series of sūtras from which the anthology quotes one. It can tell a root text from a commentary: SHT XI 4750 follows a passage of the Nyāyānusāra and is, by its lemmas, a commentary on the Kośabhāṣya. And it works where a line has kept too few letters for any search. The unidentified pieces of two British Library volumes, 476 of them, were simply read, and so were the blocks that the matching by piece had left without a record."

"Three fragments were collated with the Pāli, taken from the Dharmamitra database. In SHT XI 4501 three clauses of the sūtra of the cloth similes (AN 3.99) stand nearly word for word and in order; *ya etaṃ sevante bhajante pa(ryupāsate)* answers to *ye kho panassa sevanti bhajanti payirupāsanti*."

"A text once found can be followed for more. SHT VIII 1883, the bad monk as a great robber, turned out to stand in the numerical section of the Sarvāstivāda Vinaya (T 1435, 346a–378c), a stretch of short sūtra-like pieces between lists of Vinaya terms. Its 44 longer passages were read and their key words looked up in all Berlin and British Library entries. One sūtra of SHT VI 1252, on monks who quarrel, is there, under the ones, which explains why the fragment has a sūtra of threes among sūtras of ones. On the way a British Library piece, Or.15009/468, proved to be the list of headings that opens the Vinayamātṛkā; the Chinese (T 1441) has most of its lines, and the Tibetan has every one. The fragments that the editors compare with the Divyāvadāna were read against the Vinayas in the same manner: SHT VI 1519 is plausibly the story of Sahasodgata as the Mūlasarvāstivāda Vinayavibhaṅga tells it (T 1442, 813c)."

"The reading has limits of its own. It was done on the printed transliterations; photographs were compared in a few cases only. And it does not replace a check of the literature: K. Kano checked the list as it stood on 13 November against SHT XII and XIII, and the rows added since are not yet checked."

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

  - Check each row against the findings page before use. Changed since this table was
    written: 2022 with its join to 2025 f is Melzer's (SHT XIII; now "already identified"),
    so that row goes; 1176 and 1958 are plausible (Jñānaprasthāna).
  - Candidates from 20–21 Nov, none yet checked against SHT XII and XIII (FOR_KANO.md):
    950 Gaṇḍavyūha, Nidānaparivarta vv. 13–26; 1327 Madhyamāgama 172; 1380 Madhyamāgama 28;
    1855 Madhyamāgama 177; 2094 Abhidharmakośakārikā III 54–56, 61–62; 1622 maṅgala verses;
    1837, 1946, 3421 (+ 3921, 3961), 3633 Jñānaprasthāna; 3030, 3316 Prakaraṇapāda;
    4243 Saṅgītiparyāya; 4604 + 1429 Saṃyuktāgama 1172–1173; 2369 Skandila's
    Abhidharmāvatāra (18 Nov; not in SHT XII and XIII according to K. Kano).
  - Counts on 21 Nov (18:22): 140 rows, 63 identified, 34 plausible, 8 editors' leads, 35
    already identified; fourteen more fragments are listed by type of text only. Three of the rows are St Petersburg pieces: SI B/24,14 (verses of
    Mahābhārata, Udyogaparvan 70, and 3.203.39 = 12.182.9, with others not in the critical
    text), SI P/16 no. 2 (a Vibhāṣā on the Jñānaprasthāna, T 1545, 921a29–b21), both
    identified, and SI P/16 no. 3 (plausibly the story of King Nanda as in the
    Kalpanāmaṇḍitikā, T 201, 272c18–273a9). By collection: Berlin 44 / 26 / 6 / 33,
    British Library 17 / 7 / 2 / 2, St Petersburg 2 / 1 / – / –.
  - New on 21 Nov after the morning (REVIEW AC–AG): Or.15010/40 Śūraṃgamasamādhisūtra
    (T 642, 636a27–b28; folio 36; BLSF II.1 prints it without a title); Or.15007/537
    Saṃyuktāgama 263 (T 99, 67a25–b5); Or.15009/468 the list of headings of the
    Sarvāstivāda Vinayamātṛkā (T 1441, 593b29–c6; D 7A, pa 233b–234b; which school's
    Mātṛkā is open); Or.15007/329 plausibly a sūtra on what is foremost with the prince
    Cunda (cf. AN 5.32). Now identified, before plausible: 4501 the sūtra of the cloth
    similes (AN 3.99) and 1883 the great robber and the bad monk in triads (T 1435,
    356a13–b19). 1519, before an editors' lead, is plausibly the story of Sahasodgata as
    in the Mūlasarvāstivāda Vinayavibhaṅga, pāyantika 31 (T 1442, 813c8–22). 1663 was not
    found in the Chinese or Tibetan Vinayas. Or.15003/5 stays a lead, not on the page.
  - New on 21 Nov, evening (REVIEW AH), from texts outside Buddhist literature: SHT 23,
    leaf b, the buttermilk verses (Rājanighaṇṭu 15.56–57; Bhāvaprakāśa, takravarga 7);
    1630, verse 12 = Subhāṣitāvalī 3320, the work itself open. By type of text only: 1665 a
    grammatical commentary on the patronymic suffixes (not the Kāśikā); 1620 and 1641
    ślokas on a preparation against old age.
  - Joins found from the text, e.g. 2022 + 2025 f.
  - What kinds of text came out: verse (kāvya, stotra), Vinaya, Āgama sūtras, Abhidharma;
    outside Buddhist literature medicine (Yogaśataka, the buttermilk verses), an anthology
    verse, the Mahābhārata (SI B/24,14), a Śaiva list of tīrthas (827), grammar by type of text only. -->

## Already identified

<!-- The lesson of the study: 35 of the matches had been identified before (a third of the
102 rows of 17 Nov; of 140 now). 19 come from SHT XII and XIII (K. Kano), 15 from SHT I–XI,
BLSF and the literature, one from its printed entry (1746). 33 are Berlin rows, 2 British
Library.
  - The other direction (results/XII_XIII_MISSES.md): of the 111 rows of Kano's list of
    20 Nov, 11 were known here. The rest are all misses of ours; do not present the 60 below
    as out of scope, they should have been looked at in the first place (your word, 21 Nov).
    60 were not in the sets searched (31 in numbers IDP labels as a whole,
    19 in numbers of mixed status, 5 SHT XII numbers, 3 without a parsed entry, 2 without
    printed text); 4 identify only a Chinese side; 36 were searched and missed: 16 in no
    source searched (ten of them parts of the Tridaṇḍamālā not held), 6 in the Dharmamitra
    database but not returned by its search, 4 under the matcher's thresholds, 4 among the
    hits and passed over in the review, 3 failed on the Chinese route, 3 with too little
    text. What was done about each: every candidate now has a recorded verdict (787 rows,
    none open); matching by piece; the files outside the index matched directly; the
    Chinese route by terms; the addenda of SHT VII–XI parsed (2,105 records for 736
    numbers), which settled eighteen candidates as already identified.
  - Withdrawn after the re-parse: 963, 3238, 3299 + 4187 (they rested on the next number's
    text); earlier, for the same reason, 1999, 2012, 4313, 5799, 1938.
  - Where the earlier identifications sit: the entry's own notes ("Vgl. …"), the Ergänzungen
    of later volumes, SHT XII (2017) and XIII (2026), BLSF, journal articles.
  - IDP's online labels can be stale.
  - Read the other way: the method finds what specialists found, which is a check on it.
  - False matches produced by the parsing of the printed catalogue (merged entries), and how
    they were caught. -->

## Collaboration

<!-- Subject to point 2 at the top.
  - The check of the list against SHT XII and XIII, which moved twenty pieces to "already
    identified" (19 now, by the README of 21 Nov), and the list of 20 Nov 2026 of what the two volumes
    newly identify (111 rows). 34 rows added since are with K. Kano for the same check
    (results/FOR_KANO.md).
  - How the exchange went: each side's results checked by the other. -->

## Limitations

<!-- - Only fragments whose text is in the library or in the Dharmamitra corpora can be found.
  - Short fragments: under about 40 letters a match is rarely decisive.
  - Short hits were at first kept only in Buddhist texts; the 115 dropped were read on
    21 Nov (two real). The library is the only route to texts outside Buddhist literature.
  - 2,334 of the 4,017 SHT numbers have no searchable text in the print at all.
  - The unit was the catalogue number: single pieces of numbers that IDP labels as a whole
    were not searched (31 rows of Kano's list are of this kind).
  - The rows added on 20–21 Nov are not checked against SHT XII and XIII.
  - The British Library rows are checked against BLSF I–III only (some also against
    Chung 2008 and Wille's survey of 2014); the St Petersburg rows against the editions.
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
