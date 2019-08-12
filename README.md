# islambot
An Islamic bot for Discord with support for Qu'ran, tafsir, hadith (from sunnah.com), prayer times and conversions to and from the hijri calendar.

Created by Zaify#6850. Message me if you have any suggestions or bug reports! 

Contributors: ala and Caleb

## Qu'ran 

### -quran
**-quran** allows you to quote Qu'ran verses in English, with an optional translation edition.

```
-quran <surah>:<verse(s)> [translation edition]
```

For example:

```
-quran 1:1-7 yusufali 
```
The above command would quote Surah 1, Verses 1-7 (Surah al-Fatihah) using the translation of Yusuf Ali.

#### Valid translation editions

[Click here for a list of valid editions and translations.](https://github.com/galacticwarrior9/islambot/blob/master/Translations.md)

### -aquran
**-aquran** functions in the same way as **-quran**, but quotes the verse in Arabic.

For example, to quote the first verse of the Qu'ran:
```
-aquran 1:1
```

### -morphology
**-morphology** allows you to analyse the Arabic morphology of any word in the Qur'an.

```
-morphology surah:verse:word number
```

For example:
```
-morphology 1:2:4
```
The above would analyse the morphology of the 4th word of the 2nd verse of the 1st chapter of the Qur'an. 


### -mushaf
**-mushaf** fetches the image of the page on which a verse would be on a standard *Medina Mushaf*. 

```
-mushaf <surah>:<verse>
```

For example:
```
-mushaf 1:2
```
The above would send an image of the page containing Qur'an 1:2 on a *Medina Mushaf*. 



## Tafsir (Commentaries on the Qur'an) 

### -atafsir
**-atafsir** allows you to quote from over 26 Arabic *tafaseer* (commentaries on the Qurʾān). A list of valid *tafaseer* is available [here](https://github.com/galacticwarrior9/islambot/blob/master/Tafsir.md).

```
-atafsir <surah>:<verse(s> [tafsir]
```

For example:

```
-atafsir 2:255 tabari
```

The above command would quote the tafsir of Ayatul Kursi from Tafsir al-Tabari.


### -tafsir
**-tafsir** allows you to quote the English tasfir (commentary) of verses from Tafsīr al-Jalālayn (`jalalayn`), Tafsīr Ibn Kathīr (`ibnkathir`), Tafsīr al-Tustarī (`tustari`), Rashīd al-Dīn Maybudī's Kashf al-Asrār (`kashf`), al-Qurayshi's Laṭāʾif al-Ishārāt (`qurayshi`), Tafsīr ʿAbd al-Razzāq al-Kāshānī (`kashani`) and al-Wahidi's Asbāb al-Nuzūl (`wahidi`). It works in the same manner as **-atafsir**.

```
-tafsir <surah>:<verse> <jalalayn/ibnkathir/kashf/tustari/qurayshi/kashani/wahidi>
```

For example:

```
-tafsir 1:1 ibnkathir
```
The above command would quote the tafsir of Surah al-Fatihah, verse 1 from Tafsir Ibn Kathir. 

## Hadith 

### -hadith
**-hadith** allows you to quote hadith from sunnah.com in English.

```
-hadith <hadith book name> <chapter number>:<hadith number>
```

For example, to quote the second hadith in Chapter 1 of Sahih Bukhari:
```
-hadith bukhari 1:2
```

The above would scrape the hadith from https://sunnah.com/bukhari/1/2


#### Valid hadith book names 

* bukhari = Sahih Bukhari
* muslim = Sahih Muslim
* tirmidhi = Jami` at-Tirmidhi
* abudawud = Sunan Abi Dawud
* nasai = Sunan an-Nasa'i
* ibnmajah = Sunan Ibn Majah
* malik = Muwatta Malik
* riyadussaliheen = Riyad as-Salihin
* adab = Al-Adab Al-Mufrad
* bulugh = Bulugh al-Maram
* qudsi = 40 Hadith Qudsi
* nawawi = 40 Hadith Nawawi

40 Hadith Qudsi or Nawawi are both 40 hadith long respectively, and as such do not use a chapter number.

For example:
```
-hadith qudsi 32
```

Not all hadith are indexed correctly on sunnah.com, and not all use the same numbering as in the books - so please keep this in mind.

### -ahadith
**-ahadith** is the same as -hadith, but allows you to quote hadith in Arabic. 


## Prayer (Salaah) Times

The bot can also fetch the prayer times for any location. More precise locations (e.g. addresses) will yield more precise prayer times. 

```
-prayertimes <location>
```

For example:
```
-prayertimes Los Angeles
```

..would fetch prayer times in the general area of Los Angeles. 

#### Valid method numbers

* 1 - University of Islamic Sciences, Karachi
* 2 - Islamic Society of North America (ISNA)
* 3 - Muslim World League (MWL)
* 4 - Umm al-Qura, Makkah (default)
* 5 - Egyptian General Authority of Survey
* 7 - Institute of Geophysics, University of Tehran

## Hijri Calendar

The bot can also (rather inaccurately) convert both ways between the Hijri and Gregorian calendars.

### -converttohijri
Converts a Gregorian date to its corresponding Hijri date.

```
-converttohijri DD-MM-YY 
```

For example:
```
-converttohijri 31-08-2017
```

### -convertfromhijri
Converts a Hijri date to its corresponding Gregorian date.

For example, to convert 17 Muharram 1407:
```
-convertfromhijri 17-01-1407
```

## Search

The bot can search several Islamic websites, including islamqa.org, islamqa.info and seekershub.org.

### -search
Search Islamic websites for a given query.

```
-search <search query>
```

For example:
```
-search Can Hanafis eat shrimp? 
```
