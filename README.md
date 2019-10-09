## PALI dictionary (correction tool)

**The biggest Pali dictionary project**

Proposal for the building of the tool for:

- collection of all existing Pali language dictionaries
- rating and correction of the translation by Pali schollars or monastics
- producing various dictionaries files as output

## NEED HELP:

```diff
! Somebody who is willing to help with data cleaning (scripting experts, regex experts, database experst)
! Somebody with skills to build serious database and build web UI in top of it
! Any additional ideas or new Pali dictionaries datasets
```

## DONE:

- [x] Building the database structure (only MS Access solution)
- [x] Building of standard tables (partly done)
- [x] Collection of all Pali dictionaries  (partly done)

## TODO:

- [ ] Standardizing of the data
- [ ] Buidling the UI
- [ ] Correction and rating of the translation by mainly by Pali schollars or monastics
- [ ] Building the functionaliy to output the data
- [ ] Conversion of data to various formats (Stardic, Kindle, CSV, Apple dictionary….)

## 1. Building the database structure: 

Here is my proposal of the database structure. I started project as simple MS Access database, with queries executing VB scripts (mainly when transcribing the words to different language). But soon I have realized that the project is too big to be build in MS Acesss. As I don't have any experiences building the databases in other way, the regarding the database stops here. This is the database structure from MS Access:

![db](/Users/dxcore35/Documents/Projects/Big Pali dictionary/db.jpg)

## 2. Building of standard tables 2

![db](/Users/dxcore35/Documents/Projects/Big Pali dictionary/standardtables.jpg)

**Tables for diacritic transcription**

- - [x] Pali diacritic <> Slovak / Czech diacritic
- - [ ] Pali diacritic <> Burmese diacritic: Incomplete
- - [ ] Pali diacritic <> Thai diacritic:  Incomplete
- - [ ] Pali diacritic <> Devanagari diacritic: Incomplete

**Tables for cleaning / standardising of the text**

- - [x] Pali diacritic <> old ASIC Pali diacritic
- - [x] Pali diacritic <> Pali without special characters

**Tables for phonetic transcription**

- - [x] Pali diacritic <> [International Phonetic Alphabet](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet)

**Tables for grammar information**

- - [ ] Indeclinable table: Incomplete
- - [ ] Part of speach: Incomplete

**Tables for additional research and experiments**

- - [ ] Frequency of all Pali words from all Tipitaka: to be checked

## 3. Collection of all Pali dictionaries

Till now I have collected dictionaries listed below. Most of them are not  standardized: 

**Czech / Slovak**

- Buddhist Dictionary	(Buddhist Dictionary by NYANATILOKA MAHATHERA)

**English**

- Pali > English Buddhist Dictionary	(Buddhist Dictionary by NYANATILOKA MAHATHERA)
- Pali <> English Concise Dictionary	(Concise Pali-English Dictionary by A.P. Buddhadatta Mahathera)
- English <> Pali Concise Dictionary	(Concise Pali-English Dictionary by A.P. Buddhadatta Mahathera)
- Pali > English PTS Dictionary	(PTS Pali-English dictionary The Pali Text Society's Pali-English dictionary)
- Pali > English Proper Names Dictionary	(Buddhist Dictionary of Pali Proper Names by G P Malalasekera)
- Pali > English Dictonary from VRI	(Pali-Dictionary Vipassana Research Institute)
- Pali > English GPBD_Glossary of Pali and Buddhist terms (unknown source, probably [accesstoinsight.org](http://accesstoinsight.org))
- Pali > English MettaNet-Lanka Dictionary (MettaNet-Lanka Dictionary)
- Pali > English Buddhist Dictionary (Manual of Buddhist Terms and Doctrines)

Special:

- Pali > English Buddhas India map (Details about the place with location and picture)
- Pali > Tibetian, Sanskrit, English (PDOB_The Princeton dictionary of Buddhism)
- Sanskrit > Pali, Tibetian, English  (Buddhist Hybrid Sanskrit Dictionary)

**Myanmar**

- Pali Roots Dictionary	(Pali Roots Dictionary ဓါတ္အဘိဓာန္)
- Tipiṭaka Pāḷi-Myanmar Dictionary	(Tipiṭaka Pāḷi-Myanmar Dictionary တိပိဋက-ပါဠိျမန္မာ အဘိဓာန္)
- Pali Myanmar Dictionary	(Pali Word Grammar from Pali Myanmar Dictionary)
- U Hau Sein’s Pāḷi-Myanmar Dictionary	(U Hau Sein’s Pāḷi-Myanmar Dictionary ပါဠိျမန္မာ အဘိဓာန္(ဦးဟုတ္စိန္)

**Chinese**

- パーリ语辞典	(パーリ语辞典 增补改订 日本水野弘元)
- パーリ语辞典	(パーリ语辞典 日本水野弘元)
- パーリ语辞典-勘误表	(水野弘元-巴利语辞典-勘误表 Bhikkhu Santagavesaka 覓寂尊者)
- 巴利语入门	(巴利语入门释性恩(Dhammajīvī))
- 巴利语字汇	(四念住课程开示集要巴利语字汇（葛印卡)
- 巴利语汇解	(巴利语汇解&巴利新音译 玛欣德尊者)
- 巴汉佛学辞汇	(巴利文-汉文佛学名相辞汇 翻译：张文明)
- 巴汉词典	(巴汉词典Mahāñāṇo Bhikkhu编著)
- 巴汉词典	(巴汉词典明法尊者增订)
- 巴英术语汇编	(巴英术语汇编 法的医疗附 温宗堃)
- 汉译パーリ语辞典	(汉译パーリ语辞典 黃秉榮譯)
- 汉译パーリ语辞典	(汉译パーリ语辞典 李瑩譯)
- Chinese > English (unknown probably extract from CKJ Buddhism Dictionary)

**Vietnam**

- Pali Viet Abhi- Terms	(Pali Viet Abhidhamma Terms )
- Pali Viet Dictionary	(Pali Viet Dictionary  Bản dịch của ngài Bửu Chơn.)
- Pali Viet Vinaya Terms	(Pali Viet Vinaya Terms  Từ điển các thuật ngữ về luật do tỳ khưu Giác Nguyên sưu tầm.)

## 4. Standardizing of the data

Almost all of the datasets are just translation in JSON, CSV and some in HTML format. Almost all of the data needs to be standardized and cleaned

For example this is description for word **abbhantara** from one of the dictionary:

| Word       | Translation                     |
| ---------- | ------------------------------- |
| abbhantara | [nt.] ; . (adj.), ; internal."" |

But this should be normalized into 4 columns and 2 rows

| Word       | Translation | Gender | Type      |
| ---------- | ----------- | ------ | --------- |
| abbhantara | the inside  | neuter | subject   |
| abbhantara | interior    | neuter | subject   |
| abbhantara | inner       |        | adjective |
| abbhantara | internal    |        | adjective |

In this regard there is a lot of work to do. But my assumption is that sombody familiar with scripting, regular expressions and JSON can do it quite quickly.

# FAR FUTURE

- Buidling the UI
- Correction and rating of the translation by mainly by Pali schollars or monastics
- Building the functionaliy to output the data
- Conversion of data to various formats (Stardic, Kindle, CSV, Apple dictionary….)
