<details>
<summary>original text before ai rewrite</summary>

```text
Review Rules

There are two ways you can review

Bulk review (recommended)

You actualy dont do the review on anki but you follow the ankitolightnovel or the ankitoanime workflow. You watch/hear/review the chapter/episode. You might selectt all the cards that are related to this chapter/episode and tag them with some kind of tag that says you have reviewed them once (for example "review1") BUT ACTUALLY DONT bulkgrade them with some kind of addon because you only want to put things in your anki shedule VERY SELECTIVELY where you think longterm review is a good idea, in this case you proceed with indivisual review otherwise SUSPEND the cards (they will not be deleted but you dont have to worry that they might appear in your reviews on anki you want to prioritize)

Individual review

In this review mode you chose to do the reviewing on anki and longterm. If you have not prepared the cards already as part of an earlier Bulk review, you either follow the lightnoveltoanki or the animetoanki workflow and then do the review on the prepared cards on anki (again you might want to filter out cards and only focus on a few ones and suspend the unnecessary ones)

The rules i.e. steps for reviewing

After you have filtered out the most important notes (initial filtering) you have noticed that per note two cards exist. On the one hand the term card (black background), and on the other hand the pronounciation card (white background). I recommend to decide whether you want to have the word you mined as a pure term card, a pure pronounciation card or a hybrid card, to review the card after your initial filtering once individualy and then suspend the pronounciation i.e. term part as needed **(second filtering)**.

The term card is designed to test the MEANING of the expression, respectively the pronounciation card is designed to test the PRONOUNCIATION of the expression you mined.

If you think think that the meaning is not the priority of this card but rather you mined the expression because it has an unusual reading or contains kanjis you dont know and you want to focus on learning how to read it rather than what the expression means, or you already know the meaning but not the pronounciation, or you think you could recall the meaning easily if you see the word and know how it would be pronounced, SUSPEND the respecitve term card. Usecase for example: a very rare word with unusual kanjis but that somehow captured your interest

If you however have a card where the reading is obvious and you only want to focus on studying the meaning suspend the pronounciation card just like that. Usecase for example: a kana expression, or a common verb that has a lot of different meanings depending on the context

If you want to learn both pronounciation and term card you dont have to suspend anything. Select all the card pairs (notes) and activate the siblingsync addon that provides an additional visual cue during the review whether the current card is a pure term card (has no pronounciation sibling, white square appears on the top right), a pure pronounciation card (has no term sibling, black square appears on the top right)


As for the reviewing itself and the pass/fail rules

If it is a pronounciation card, you have to get the exact pronounciation, it is a complete YES/NO situation where you are either right or wrong with no ambiguity.
If it is a term card it is a bit more ambigious. You dont want to spend too much time during the review so you have to use a certain system: you might pass the card without actually checking the english definition overview just by feeling, but if you check the english definition overview you have to decided whether the answer in your head is sufficient/similar enough or not, but rather than trying to think like that think "Is the meaning in my head COMPLETELY DIFFERENT than the meanings listed?" if yes, you fail the card, if no you pass the card.

Explanation of fields

(In generl fields are only rendered if they are not empty and not technical fields)


Standard Mining Card produced with yomitan and ankiconnect

Note ID

The purpose of this field is to uniquely identify a card during mining, so that if you mine two times the same word it will still be regarded as a unique card. For standard mining cards it is the same as the mined sentence. It is a hidden technical field, that might be used for addon operations where the notes have to be uniquely identified ,and not displayed anywhere during the review

Word

The exact expression like it has appeared in the mined sentece, that means that for example for verbs instead of the normalized dictionary form it will appear in the conjugated form like it has also appeared in the text. It appears both at front and back at the top regardless of cardtype.

Frequency

For standard mining cards this field displays how frequent the word appears, there is also a visual rule implemented, if the word belongs to the top 1000 most frequent words the number will also appear red, if it belongs to the top 5000 most frequent words green, top 15000 blue, top 30000 yellow and otherwise gray (or invisible). It appears both at front and back at the top regardless of cardtype.(however in case the card type is term if the frequency is over 30000 it is not visible in the front)

SoundFront

It contains the Audio File of the sentence like SoundBack, it is displayed at the front of the card, but only if the card is of the type term. If the card is of the type pronounciation it does not appear however in the front of the card, since the sound would reveal the pronounciation it is not placed in this case.

SoundBack

It contains the Audio FIle of the sentence like SoundFront, it is displayed at the back of the card.

Picture

A visual that is used to identify the source of the card and motivate the learning process. In the case of pronouncation card it is placed only at the back of the card. In case of the term card a miniature version is displayed in the front as well as the usual display at the back of the card. The picture is placed in the middle of the card and also indicated that the elements below of it are reference information while the elements at the same line and above are considered core informations.

SentencePlain

The mined sentence without furigana, the mined core expression is also displayed in bold and appears in gold during review. It appears on the front of the Pronounciation Card and the Term Card. In the term card it also appears in the back but can be toggled with the SentenceFurigana field if clicked on.  

Hint(Pronounciation)

This is a field that is only used in the term card again. The user can click on it during review at the front of the card to see how the expression is pronounced. It is not used for pronounciation cards, since this is the thing that is tested in the pronounciation card. It has the same content as the field Pronounciation.

HintNotHidden

This is a field that is also only used for the term card again and also only appears at the front of the card unlike Hint(Pronounciation) it appears immediatley without a spoiler and can be seen immediatley and is inteded to write hints manualy that gives a cue or information for the meaning. For example if it the tested expression consists of kanjis that can have different meanings like 額 which can either mean brow/forehead (ひたい) or (picture)frame|amount (of money) (がく), in this field a hint can be written like NOT (picture)frame|amount (of money) (がく)

Pronounciation

Contains the reading of the expression in hiragana, it is displayed on the back of the Term Card as well as the Pronounciation Card. However the positioning and the size differs, since it is the core element of the pronounciation card it appears higher and in bigger font on the answer side (back of the card) than it does for the Term Card.

English Definiton Overview

Contains an overview of several different english definitions that might apply for this expression. It is not the one specific definition that exactly fits the context but rather a list of all possible definitions. During the review it is usually sufficient to have a general idea and only get one of the meanings within the list since you might also dont always want to read the sentence. It appears on the back of the Term Card as well as the Pronounciation Card. However for the Term Card since it is the subject that is tested it appears in the top section above the picture element, while for the Pronounciation Card it is only secondary information and therfore placed below the Picture section. Since the field might be very long if a treshhold is surpassed it is collapsed into a details block and only unfolded if the user clicks on it again.

Correct English Definition

Unlinke the field English Definition Overview it contains the one specific definition that also fits the context, by default it empty after the card is mined with yomitan to anki, it is either filled manualy or with the help of an addon as part of a workflow for example during the "ankitolightnovel" workflow (github link). It also appears where the English Definition Overview appears but is placed on top of it and in a bigger font.

Japanese Definition Overview

Contains an overview of several different japanese definitions that might apply for this expression. It is not the one specific definition that exactly fits the context but rather a list of all possible definitions. It is rather a reference than something you would actively look at. During the setup it has also been prepared in a way so that the furigana is also displayed. It appears on the back of either card type, since it to be seen as reference it is placed below the picture element.

Correct Japanese Definition 

Unlinke the field Japanese Definition Overview it contains the one specific definition that also fits the context, by default it empty after the card is mined with yomitan to anki, it is either filled manualy or with the help of an addon as part of a workflow. It also appears where the Japanese Definition Overview appears but is placed on top of it and in a bigger font.

Sentence Furigana

Copy of the Sentence Plain field but with Furigana added automatically through the AJT addon which has been set up earlier. By default it shown at the back of the pronounciation and term card next to the picture element, it can also be toggled with the sentence plain field in case of the term card.

TranslationExampleSentence

A field where later manualy with the help of an addon for example the google translate anki addon the translation of the sentences can be added in bulk. The field appears at the back of the card, it is less pronounced in the pronounciation card than in the term card. It is considerered reference information and therefore eitherway below the middle line with the picture element

Source

Reference information on the back of the cards that indicate the source of the material, by default it is left blank but in the yomitan settings in the "configure anki flashcards" section the name of the source can be edited (however everytime the source changes it has to be modified again)

Link to Related Cards

A field that is used in the addon SimpleLinker, connections between other cards can be established through this addon. The links are considered core information and both appear equaly on pronounciation cards on the fron as well as on the back(above the picture), no mobile support is provided however, 

Notes1

This is also a field that does not have any automaticaly generated content. Unlike the hint field it also appears in the pronounciation card (needs to be clicked on to unfold). In the pronounciation card it appears in the front in the middle of the card, and on the back in the reference part. For the term card in the front it appears in the footer that needs to be unfolded, and on the back in the reference part. It can be filled with additional information related to the card or substitute the hint fields for the pronounciation cards.

Notes2

Analogous to Notes1

NameDictionary

Reference Information where special readings for names might be displayed in the reference part of the back of a card

GrammarDictionary1

Reference Information where additional grammar information might be displayed in the reference part of the back of a card (although it is obsolete since for the grammar a dedicated system is in place however for edge cases and very obscure grammar it might sometimes provide further hints)

AlternativeDictionary1

Trivia Information or Special/Historical Information for proverbs, might be displayed in the reference part of the back of a card

AlternativeDictionary2

Trivia Information or Special/Historical Information for proverbs, might be displayed in the reference part of the back of a card

SiblingSyncInfo

A technical field the SiblingSync Addon uses to adjust and manage the pronounciation/term system.

Dump1 to Dump10

Technical fields that allows to convert from previous notetype to this notetype for example without losing any information, can also be used for technical addons and modifications on the cards, for example the sibling sync addon used the field Dump1 which was then renamed to SiblingSynInfo and a new field with the name Dump1 was added again.

Individual Grammar Card created with (grammar web addon) and (grammarminer anki addon) and (grammar anki)

By default the layout for the term cards are used and therefore the pronounciation sibling is automaticaly suspended.


Note ID

For individual grammar cards it is derived from the nid of the overlaying grammar card from the grammar deck (see grammar card on grammar anki and individual mined grammar card on grammar hub webaddon), with an additionaly suffix key that identifies the grammar sentence connection and also used for technical operations during the generation fo the grammar cards triggered by the grammarminer addon.

Word

The exact regax match that the webbrowser addon found during the search

Frequency

Recycled and used for displaying the construction scrapped from the overlaying grammar card and a link to the original grammar card.

SoundFront

Since the grammar cards are also of the note type miningsimple the audio of the mined sentence where the grammar pattern appeared can also be extracted as a part of the lightnoveltoanki workflow

SoundBack

Analogous to SoundFront

SentencePlain

Same as standard mining

SentenceFurigana


Same as standard mining

The other fields are all left empty

```
</details>


# DEMO (ACTIVATE THE SOUND 🔊)

https://github.com/user-attachments/assets/c42f565e-16dd-431d-9bf4-429a3aa229f1


# Review Rules

There are two distinct ways you can approach your reviews:

## Review Modes

### 1. Bulk Review (Recommended)
In this mode, you do not actually perform the review directly inside Anki. Instead, you follow the [ankitolightnovel](🔗_INSERT_LINK_HERE) or the [ankitoanime](🔗_INSERT_LINK_HERE) workflow:

1. Watch, hear, or review the specific chapter or episode.
2. Select all cards related to this chapter/episode.
3. Tag them with a tracking tag (for example, `"review1"`) to indicate they have been reviewed once.
4. **Do not** bulk-grade them using an add-on. You want to add cards to your Anki schedule **very selectively**—only where you think long-term review is beneficial.
5. If a card is worth long-term retention, proceed with an **Individual Review**. Otherwise, **SUSPEND** the cards. Suspended cards will not be deleted, but they won't clutter your active Anki review queue, allowing you to prioritize effectively.

### 2. Individual Review
In this mode, you choose to handle the reviewing process long-term within Anki. 

* If you have not prepared the cards during an earlier Bulk Review, follow either the [lightnoveltoanki](🔗_INSERT_LINK_HERE) or the [animetoanki](🔗_INSERT_LINK_HERE) workflow.
* Perform the reviews on the prepared cards inside Anki. 
* *Tip:* You may still want to filter out cards, focusing only on a select few and suspending the unnecessary ones.

---

## Step-by-Step Review Rules

Once you filter out the most important notes **(initial filtering)**, you will notice that **two cards exist per note**:
1. **The Term Card:** Features a black background. It is designed to test the **MEANING** of the expression.
2. **The Pronunciation Card:** Features a white background. It is designed to test the **PRONUNCIATION** of the mined expression.

I recommend to decide whether you want to have the word you mined as a pure term card, a pure pronounciation card or a hybrid card, to review the cards after your initial filtering once individualy and then suspend the pronounciation i.e. term part as needed (second filtering).

### Card Suspension Logic

* **Suspend the Term Card if:** 
  Meaning is not the priority. For example, you mined the expression because it has an unusual reading, contains Kanji you don't know, or you already know the meaning but want to focus entirely on how to read it. You can also suspend it if you can easily recall the meaning once you know the pronunciation.
  > **Use Case:** A very rare word with unusual Kanji that somehow captured your interest.

* **Suspend the Pronunciation Card if:** 
  The reading is obvious and you only want to focus on studying the meaning.
  > **Use Case:** A kana-only expression, or a common verb that has a lot of different meanings depending on the context.

* **Keep Both Cards if:** 
  You want to learn both the pronunciation and the term. In this case, do not suspend anything.
  
* **After suspending (second filtering):** 
  Select all card pairs (notes) and activate the [SiblingSync Add-on](🔗_INSERT_LINK_HERE). This add-on provides a visual cue during review to show the card's status:
  * **Pure Term Card** (no pronunciation sibling): A **white square** appears on the top right.
  * **Pure Pronunciation Card** (no term sibling): A **black square** appears on the top right.

### Pass/Fail Criteria

* **Pronunciation Cards:** You must get the exact pronunciation right. This is a strict **YES/NO** situation with no ambiguity.
* **Term Cards:** Criteria here are more flexible. To keep reviews fast and efficient, use the following system:
  * You may pass a card without checking the English definition overview if your intuition feels correct.
  * If you do check the English definition, ask yourself: *"Is the meaning in my head completely different from the meanings listed?"* 
    * If **yes** $\rightarrow$ **Fail** the card.
    * If **no** $\rightarrow$ **Pass** the card.

---

## Explanation of Fields

> **General Note:** Fields are only rendered during review if they contain content and are not technical/hidden fields.

### Standard Mining Cards
*Produced using [Yomitan](🔗_INSERT_LINK_HERE) and [AnkiConnect](🔗_INSERT_LINK_HERE).*

| Field Name | Description | Placement & Visibility |
| :--- | :--- | :--- |
| **Note ID** | Uniquely identifies a card during mining so duplicate words remain unique. For standard cards, it matches the mined sentence. | Hidden technical field. Used for add-on operations; never displayed during reviews. |
| **Word** | The exact expression as it appeared in the mined sentence (e.g., verbs will appear in their conjugated form rather than the dictionary form). | Appears at the top of both the Front and Back, regardless of card type. |
| **Frequency** | Displays how frequently the word appears. Colors represent frequency tiers:<br>• **Top 1,000:** Red<br>• **Top 5,000:** Green<br>• **Top 15,000:** Blue<br>• **Top 30,000:** Yellow<br>• **Other:** Gray / Invisible | Appears on both Front and Back. *Exception:* On Term Cards, frequencies over 30,000 are hidden on the Front. |
| **SoundFront** | Contains the audio file of the sentence. | **Term Cards:** Displayed on the Front.<br>**Pronunciation Cards:** Hidden on the Front to avoid revealing the answer. |
| **SoundBack** | Contains the audio file of the sentence. | Displayed on the Back of all cards. |
| **Picture** | A visual asset used to identify the source and motivate learning. Serves as a divider: elements below it are reference info; elements on or above it are core info. | **Term Cards:** Miniature version on the Front; full version in the middle of the Back.<br>**Pronunciation Cards:** Displayed only in the middle of the Back. |
| **SentencePlain** | The mined sentence without furigana. The core expression is highlighted in **bold gold**. | Appears on the Front of both card types. On Term Cards, it also appears on the Back and can be toggled with `SentenceFurigana` when clicked. |
| **Hint (Pronunciation)** | Displays the reading of the expression (same content as the `Pronunciation` field) via a clickable spoiler. | **Term Cards:** Front only.<br>**Pronunciation Cards:** Not used. |
| **HintNotHidden** | Used for manual hints regarding the meaning. Appears immediately without a spoiler.<br>_Example for 額 (can mean brow/forehead [ひたい] or picture frame/amount [がく]), type in the field as hint: "NOT (picture)frame\|amount (of money) (がく)"_ | **Term Cards:** Front only. |
| **Pronunciation** | Contains the reading of the expression in hiragana. | Displayed on the Back of both card types. On Pronunciation Cards, it is positioned higher and uses a larger font. |
| **English Definition Overview** | A list of all possible English definitions for the expression rather than one context-specific definition. Automatically collapses into a clickable dropdown if it exceeds a length threshold. | **Term Cards:** Top section (above the picture).<br>**Pronunciation Cards:** Bottom section (below the picture as secondary info). |
| **Correct English Definition** | The single, specific definition that fits the exact context. Left blank by default after mining; filled manually or via an add-on during workflows like [ankitolightnovel](🔗_INSERT_LINK_HERE). | Placed directly on top of the `English Definition Overview` in a larger font. |
| **Japanese Definition Overview** | A list of possible Japanese definitions for reference, configured to display furigana. | Displayed below the picture element on the Back of both card types. |
| **Correct Japanese Definition** | The single, specific Japanese definition fitting the context. Left blank by default; populated manually or via an add-on. | Placed directly on top of the `Japanese Definition Overview` in a larger font. |
| **Sentence Furigana** | A copy of `SentencePlain` with furigana added automatically via the [AJT Add-on](🔗_INSERT_LINK_HERE). | Displayed on the Back next to the picture. On Term Cards, it can be toggled with `SentencePlain`. |
| **TranslationExampleSentence** | Contains bulk-generated sentence translations added via tools like the [Google Translate Anki Add-on](🔗_INSERT_LINK_HERE). | Reference information located below the picture line on the Back. Less pronounced on Pronunciation Cards. |
| **Source** | Indicates the source material. Edited via Yomitan's "Configure Anki Flashcards" section. | Reference information on the Back; left blank by default. |
| **Link to Related Cards** | Establishes connections between cards using the [SimpleLinker Add-on](🔗_INSERT_LINK_HERE). *Note: No mobile support available.* | Core information. Appears equally on the Front and Back (above the picture) of Pronunciation Cards. |
| **Notes1** | A manual field for custom information or pronunciation hints. | **Pronunciation Cards:** Click to unfold on the Front (middle) and Back (reference section).<br>**Term Cards:** Unfolds in the Front footer and appears on the Back (reference section). |
| **Notes2** | Identical functionality to `Notes1`. | Reference section on the Back. |
| **NameDictionary** | Reference info displaying special readings for names. | Reference section on the Back. |
| **GrammarDictionary1** | Reference info for supplementary grammar data (mostly obsolete due to a dedicated grammar system, but kept for edge cases). | Reference section on the Back. |
| **AlternativeDictionary1** | Trivia, special, or historical information for proverbs. | Reference section on the Back. |
| **AlternativeDictionary2** | Trivia, special, or historical information for proverbs. | Reference section on the Back. |
| **SiblingSyncInfo** | A technical field used by the [SiblingSync Add-on](🔗_INSERT_LINK_HERE) to manage the pronunciation/term card system. | Hidden technical field. |
| **Dump1 to Dump10** | Technical fields allowing layout conversions from older note types without data loss. | Hidden technical fields. (e.g., `Dump1` was repurposed for `SiblingSyncInfo` and a new `Dump1` was recreated). |

---

### Individual Grammar Cards
*Created using a grammar web add-on, the [GrammarMiner Anki Add-on](🔗_INSERT_LINK_HERE), and [Grammar Anki](🔗_INSERT_LINK_HERE).*

#### Preview and Connection to Base Grammar Notes

https://github.com/user-attachments/assets/0e4ca214-63b5-4fa3-8457-0beb05aa9284

#### Field Recycling
By default, these cards use the **Term Card** layout, and their Pronunciation Sibling is automatically suspended.

* **Note ID:** Derived from the `nid` of the overlaying grammar card from the grammar deck, featuring an additional suffix key identifying the grammar-sentence connection. Used for technical operations by the GrammarMiner add-on.
* **Word:** The exact regex match found by the browser add-on during the search.
* **Frequency:** Recycled to display the structural construction scraped from the overlaying grammar card, alongside a link to the original grammar card.
* **SoundFront / SoundBack:** Since these cards utilize the `miningsimple` note type, audio from the mined sentence where the grammar pattern appeared can be extracted via the [lightnoveltoanki](🔗_INSERT_LINK_HERE) workflow.
* **SentencePlain / SentenceFurigana:** Operates identically to Standard Mining Cards.
* **Other Fields:** All remaining fields are left empty by default.
