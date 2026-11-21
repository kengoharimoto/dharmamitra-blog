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
post moves to _posts/. Numbers are those of the findings page on 21 Nov 2026, 13:43 (research
commit 3d581bf; 138 rows: 61 identified, 34 plausible, 8 editors' leads confirmed, 35 already
identified elsewhere; that morning 134 rows: 56, 34, 9, 35; on 17 Nov 102 rows: 36, 21, 10, 35); refresh them from research/turfan-sht
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
    (results/FOR_KANO.md: 32 Berlin rows, 21 identified and 11 plausible, and 1519, whose
    proposal changed after K. Kano's check). The British Library rows are checked against
    BLSF I–III only, some also against Chung 2008 and Wille's survey of 2014.
  - Counts by collection in the last sentence: README table at commit 3d581bf (Berlin
    42 / 26 / 6 / 33, British Library 17 / 7 / 2 / 2, St Petersburg 2 / 1 / – / –). -->

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

On the other hand, Kano's list of what volumes XII and XIII newly identify had about 100 items that our pipeline had not identified. We analyzed why and improved our methodologies. After that, we identified or proposed plausible candidates for about three dozen more items. Along the way we also took in the British Library's fragments and made a start on those in St. Petersburg. As of 21 November, our list has 138 rows: 61 identified (42 from Berlin, 17 from the British Library, 2 from St. Petersburg), 34 plausible (26, 7 and 1), 8 that confirm a lead the editors give, and 35 that were already identified.

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

"The first step was to get the readings of the fragments. While transliterations of the IDP fragments are online, on the IDP site at the British Library, that site blocks automated access; the Berlin IDP database and the Turfan site of the Berlin Academy gave only photographs and, for each fragment, a one-line identification from the online catalogue. (Both became inaccessible in mid-November, while the study was under way.) So, the study read the printed catalogue instead. We ran Chandra OCR over SHT I–XI on our workstation, and a parser cut the result into entries: catalogue number, shelfmark, script type, physical description, transliteration and notes."

"Which entries count as unidentified was decided from IDP's online catalogue. One catalogue number often covers several pieces (a, b, c and so on), and the online catalogue lists each piece separately with its own identification. We counted a catalogue number as undetermined only when all of its pieces are marked 'Noch nicht bestimmt'; a number with some pieces identified and others not was left out at first. [Upon realizing that some apparent ones were not searched, w]e added a second group: fragments that carry only a label of genre or collection, such as 'Sūtra-Fragment', 'Abhidharma-Text', 'Dhāraṇī' or 'Medizinisches Fragment', or a hedged one ('Wahrscheinlich …'). They are in effect unidentified as well. [This is an example of transmitting nuances to AI. For me, it is apparent those should have been searched in the first place.]"

"We treated the British Library's Sanskrit fragments from Central Asia in the same way. They are published in the three volumes of *The British Library Sanskrit Fragments* (BLSF), where the editors write an identification into the heading of each piece or mark it 'not yet identified'. These volumes were read with the same OCR and parsed like the SHT volumes."

"For the St. Petersburg collection we could only make a start. No catalogue of it has been published; according to a survey of 2020, 508 of its roughly 700 inventoried Sanskrit items are unidentified, and most are unpublished. We worked on what is in print. The one volume of the *St. Petersburg Sanskrit Fragments* (StPSF I) that we have edits manuscripts that are identified, but by the editors' own count 46 stories of its avadāna anthology from Merv are not. Forty-four of them could be recovered from the OCR and were searched through Chinese, Sanskrit and Pāli, and no parallel was found. Besides these, the pieces of the Berezovsky and Krotkov collections published in 2021, the Petrovsky pieces reprinted in *Pamjatniki* 3, and SI B/24,14 and SI P/16 went through the same matchers. Three of them are on our list. They are not counted in the table below."

"IDP's online catalogue marks 4,712 catalogue numbers as 'Noch nicht bestimmt'. Of these, 1,398 have numbers from 5800 on, which SHT I–XI do not describe, so they were out of our reach. That leaves 3,314 undetermined numbers in the volumes we read, and 703 more that have only a genre label: 4,017 in all. In the British Library volumes, 894 pieces are without an identification."

"Most of them could not be searched, because there is nothing to search. For 2,228 of the 4,017 SHT numbers the catalogue prints no transliteration: the entry describes a scrap of one or two centimetres and ends 'noch nicht bestimmt'. Another 106 have a transliteration in which no eight letters in a row are legible. Of the British Library pieces, 465 are too small in the same two ways."

"The parsers needed more than one round. In the first run the SHT parser missed 218 of the 4,017 numbers. For most of them the OCR had joined the heading of the entry to the end of the last line of the entry before it, usually at a page break, and the parser looked for a heading at the beginning of a line. Where a heading was lost, the text of the entry was read as part of the entry before it. We changed the parser and parsed all volumes again on 19 November. This added 279 entries, and 88 entries gave up lines that belong to the number after them. Three identifications that were already on our list turned out to rest on the next number's text and were withdrawn (SHT 963, 3238 and 3299 + 4187), and one moved from 1957 to 1958. The 139 fragments that were new or had changed were searched like the others. Twenty-five numbers are still without an entry: sixteen were transferred to another collection or merged into another number, and nine have no description of their own. A second correction on 21 November, for headings lost in SHT I and IV, changed no finding. The same check was then made for the British Library volumes, where the shelfmarks of each series should run without gaps. They did not: 206 entries were missing, because the parser expected a heading in bold and the OCR gives many without. Of the 206, 52 are unidentified pieces with enough text to search. They went through all the searches and were read; two of them could be given a text, and a third plausibly. No piece searched before changed its text."

| | SHT, undetermined | SHT, genre label only | SHT together | British Library |
|---|---|---|---|---|
| Unidentified in the volumes read | 3,314 | 703 | 4,017 | 894 |
| No transliteration printed | 2,099 | 129 | 2,228 | 93 |
| No run of eight legible letters | 92 | 14 | 106 | 372 |
| No entry (transferred, merged or not described) | 5 | 20 | 25 | – |
| **Not searched** | **2,196** | **163** | **2,359** | **465** |
| **Searched** | **1,118** | **540** | **1,658** | **429** |

"The 1,658 SHT numbers make 1,644 fragments as we searched them, since pieces that the catalogue joins count once. With the 429 British Library pieces, 2,073 fragments were searched. Not all of them were searched in every way. All went through the match against the e-text library. The 1,279 with at least 40 legible letters (1,107 from Berlin, 172 from London) also went to Dharmamitra search, and 986 fragments (859 and 127) were sent through Chinese as well. The remaining 794, with fewer than 40 letters, were tried against the e-text library only."

"After the comparison with SHT XII and XIII, described below, the same fragments were gone through again in three more ways. Each entry was cut into blocks, one side of one piece, 4,912 in all, and matched block by block, with a lower threshold and a test that the hit is not shared by many works. This run also took in 72 catalogue numbers of mixed status, with some pieces identified and others not, which the first run had left out. The Sanskrit files that are in the Dharmamitra database but were not returned by the search we queried, 1,500 of 3,274, were written out and matched directly. And the route through Chinese was built a second time without a translation model: a table of 1,080 Sanskrit stems with the renderings of the Chinese translators, by which the terms of a fragment are searched in the Taishō in the order they have in the fragment."

"Last, some fragments were not searched again but read against a text that an earlier result pointed to. Three were collated with the Pāli. The fragments that the editors compare with the Divyāvadāna were read against the Chinese and Tibetan Vinayas, since much of the Divyāvadāna is taken from the Mūlasarvāstivāda Vinaya. And when one fragment turned out to stand in the numerical section of the Sarvāstivāda Vinaya (T 1435, 346a–378c), the 44 longer passages of that section were read through for other fragments. Two pieces moved from plausible to identified in this way, and a British Library piece was found to be the list of headings that opens the Vinayamātṛkā."

"SHT XII and XIII were not available to us when the first searches ran. This matters more than it may seem: each later volume carries additions and corrections to the earlier ones, among them lists of fragments that have been identified since. K. Kano checked our list against both volumes and, on 20 November, sent a list of the 111 fragments that they newly identify, join or correct. We come back to this below."

## Methods

<!-- Six subsections since 21 Nov 2026. The first, third and fourth are the searches of the
first run; the second and fifth were added on 20–21 Nov after the comparison with SHT XII
and XIII; the sixth is the step that follows every search. They are ordered by kind (each later method follows the one it grew out of), not
by date; "The fragments" tells the order in time. -->

### Matching against a Sanskrit e-text library

<!-- Runs of letters from the fragment searched in the library; what counts as a match
(letters matched, number of runs, recto and verso in order).
Describe the matcher as it works: the score is how many of the fragment's letters are
covered within a 3,000-letter window of a candidate text. It does not estimate line length
or judge the intervals between matches; spacing was reasoned about only in single cases
(e.g. the join 1927 + 1932). The point moved here from the introduction: a machine can align
the few surviving words of each line with a candidate and judge the match by their intervals.
Present it as what is possible, or as what was done in those cases. One example that is safe to
name, e.g. 1632 Bhadracarī vv. 2–3 or 928 Buddhacarita 11.20–29.
Thresholds as they are: a hit is kept if two runs cover 26 letters or one run 30; runs
under ten letters give none. Calibration on 790 identified fragments (README, step 5): a
hit for 273 of 396 with 100 or more legible letters, 48 of 203 with 40–100, almost none
below 40. -->

### Matching by piece

<!-- Added 20–21 Nov (REVIEW Y, Z; README, step 12).
  - Why: in the first run the unit was the catalogue number, with all its pieces pooled.
    A number with one piece of one text and another of a second was treated as one text
    (1198: pieces b–c Saddharmapuṇḍarīka, piece a Madhyāntavibhāgabhāṣya, missed), and
    numbers of mixed status were not searched at all.
  - How: each entry is cut into blocks, one side of one piece each, 4,912 in all; the 72
    numbers of mixed status are included. The same matcher with lower thresholds, and a
    hit under the old thresholds is kept only when no more than two other works come near
    it and the text is Buddhist. Without that test the lower thresholds give many chance
    hits in the purāṇas and tantras.
  - What it gave: 22 per cent more hits on the identified fragments. It recovers the near
    misses 1198 a, 4221, 4246 and 412 fragm. 36. The 85 blocks on numbers with nothing
    recorded were read one by one: 1380 (Madhyamāgama 28), 1574 b (Larger Prajñāpāramitā,
    ch. 76), 1622 (maṅgala verses), 2094 (Abhidharmakośakārikā III 54–56, 61–62); plausible
    2127, 4501, 1636, 1185. Of the 40 mixed numbers read by piece, 29 only confirm pieces
    already named; new is 1252 b and c. Also 4604 + 1429 (Saṃyuktāgama 1172–1173).
  - What it does not reach: runs under ten letters (4180 fragm. 4 was found only by
    reading), and 4278, 1202 b. -->

### Dharmamitra search

<!-- Semantic search over the Sanskrit, Chinese, Tibetan and Pāli corpora: what it found
that string matching did not, and where it only characterises a piece (genre, type of text)
without identifying it.
Added 21 Nov (REVIEW X; XII_XIII_MISSES.md, cause B): 1,500 of the 3,274 Sanskrit files of
the local database were not returned by the search that was queried, among them eighteen
files of the Tridaṇḍamālā; six of the SHT XIII identifications were missed for this reason.
The files were written out and matched directly. See the note in "The fragments" on whether
and how to say this. -->

### Through Chinese, by translation

<!-- The main point for this blog: texts lost in Sanskrit. The fragment is translated into
Chinese by the model, the Chinese is searched in the Taishō, and the hit is then read line
by line against the fragment.
  - Why it works for Sarvāstivāda Abhidharma (Jñānaprasthāna, Prakaraṇapāda, Vibhāṣā,
    Nyāyānusāra), which survives only in Xuanzang's translations.
  - One worked example, line by line: e.g. 1732, a Vibhāṣā on shame and dread of blame
    (T 1545, 180a–c; T 1546, 136b), or 1686 (Sarvāstivāda Vinaya, T 1435, 267a).
  - What did not work: the Tibetan route as a search of its own. Since 21 Nov the Tibetan
    has served to confirm and to complete (REVIEW AC, AG): Or.15010/40 is confirmed by
    D 132, 280b–281b, and the Tibetan Uttaragrantha (D 7A, pa 233b–234b) has every line of
    Or.15009/468, also the three headings that T 1441 lacks. Reword accordingly.
  - Where it failed (REVIEW AA; XII_XIII_MISSES.md, cause E), which leads to the next
    subsection: where the model's wording is not the translators' (1309:
    nirodhadarśanaprahātavya rendered freely, not 見滅所斷; 1420: śivapathikā as 屍陀林, the
    Madhyamāgama has 息止道), and where the longest lines, the only ones translated, are
    not the telling ones (4442). -->

### Through Chinese, by the translators' terms

<!-- Added 20–21 Nov (REVIEW AA; README, step 10). No model is used.
  - How: a table of 1,080 Sanskrit stems with the renderings of the Chinese translators
    (Xuanzang, the older Abhidharma translations, the Āgamas, the Vinayas), e.g.
    nirodhadarśanaprahātavya → 見滅所斷 | 見滅斷 | 盡諦所斷. The stems found in a fragment, in
    the fragment's order, are its term sequence. Taishō vols 1–32 are searched for windows
    of 320 characters that have these terms, rarer terms weighing more, and the best
    windows are scored again by order. The whole run takes under two minutes.
  - Who wrote the table: REVIEW AA says "written by hand"; it was written in the study,
    by Claude. Say so if the post describes it.
  - Calibration: it places what the first route or SHT XII had placed (1309 at T 1544,
    992b18; 1854+1861; 1685; 1660). On the labelled entries whose label names a work with
    a Chinese version, the first work is right for 17 of 33 and one of the first three for
    27. So it proposes a place, and reading decides.
  - What it gave: 1946 and 1837 (Jñānaprasthāna, T 1544, 931c10–20 and 962a13–22), 4232
    (plausible), and 1439 + 1753 + 1986, one text with the Mahāvibhāṣā's tetralemmas on the
    attainments (plausible; which text is open). Not checked against SHT XII and XIII.
  - Limits: a text needs at least three terms of the table; Abhidharma formulas recur, so
    the best window is often one of several equal ones; no verse, little plain narrative. -->

### Reading against a text

<!-- Added 21 Nov. The point: the searches propose, reading decides. Every row of the list
rests on the fragment read line by line against the text; the cards of the findings page
show this reading.
  - A verdict for every candidate (REVIEW T): 787 rows in the ledger, none open. Most
    candidates are not identifications: kind only 167, known from the entry 154, stock
    phrases 153, chance 144 (state of REVIEW AB). Four of the SHT XIII identifications had
    been among the hits and were passed over because no verdict was recorded (1420, 1722,
    961, 3423 + 1749).
  - What reading can do that the searches cannot: runs under ten letters (4180 fragm. 4
    was found only by reading the paragraph); telling a text from a text that quotes it
    (1877: the series of finger-snap sūtras, of which Tridaṇḍamālā 4.2 quotes one; 1883:
    not the Akṣaṇasūtra it matched); telling a root text from its commentary (4750: a
    commentary on the Kośabhāṣya by lemma, not the Nyāyānusāra).
  - Reading by eye without a hit: the unidentified pieces of BLSF II.1 and III.1 (476
    pieces of twelve or more letters, REVIEW H) and the 85 blocks on numbers with nothing
    recorded (REVIEW Z).
  - Collation with the Pāli (REVIEW AE), the Pāli taken from the Dharmamitra database, not
    from memory: 4501 is the sūtra of the cloth similes (AN 3.99), three clauses word for
    word and in order; 1883; Or.15007/329 stays plausible.
  - Following a text for more fragments. The Divyāvadāna fragments against the Chinese
    and Tibetan Vinayas (REVIEW AD): 1519 plausibly the story of Sahasodgata as in the
    Mūlasarvāstivāda Vinayavibhaṅga (T 1442, 813c8–22), the refuge in the plural as in
    Yijing; 1663 not found. The numerical section of the Sarvāstivāda Vinaya (T 1435,
    346a–378c; REVIEW AF, AG): its 44 longer passages read and their key words looked up
    in all Berlin and British Library entries; the quarrel sūtra of 1252 stands there
    (353b2–c7), which explains a sūtra of threes among sūtras of ones; Or.15009/468, seen
    on the way, is the list of headings of the Vinayamātṛkā (T 1441, 593b29–c6), and the
    Tibetan (D 7A, pa 233b–234b) has every line. A search of the same section by terms
    gave only chance hits.
  - Photographs: compared in a few cases only (1927 + 1932; 2025 f + 2022; 1973).
  - Who reads: Claude. Say what was checked by you or by K. Kano, and what was not.
  - One example worth showing in full: 1252 or Or.15009/468. -->

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
  - Counts on 21 Nov (13:43): 138 rows, 61 identified, 34 plausible, 8 editors' leads, 35
    already identified. Three of the rows are St Petersburg pieces: SI B/24,14 (verses of
    Mahābhārata, Udyogaparvan 70, and 3.203.39 = 12.182.9, with others not in the critical
    text), SI P/16 no. 2 (a Vibhāṣā on the Jñānaprasthāna, T 1545, 921a29–b21), both
    identified, and SI P/16 no. 3 (plausibly the story of King Nanda as in the
    Kalpanāmaṇḍitikā, T 201, 272c18–273a9). By collection: Berlin 42 / 26 / 6 / 33,
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
  - Joins found from the text, e.g. 2022 + 2025 f.
  - What kinds of text came out: verse (kāvya, stotra), Vinaya, Āgama sūtras, Abhidharma. -->

## Already identified

<!-- The lesson of the study: 35 of the matches had been identified before (a third of the
102 rows of 17 Nov; of 138 now). 19 come from SHT XII and XIII (K. Kano), 15 from SHT I–XI,
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
    newly identify (111 rows). 32 rows added since are with K. Kano for the same check
    (results/FOR_KANO.md).
  - How the exchange went: each side's results checked by the other. -->

## Limitations

<!-- - Only fragments whose text is in the library or in the Dharmamitra corpora can be found.
  - Short fragments: under about 40 letters a match is rarely decisive.
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
