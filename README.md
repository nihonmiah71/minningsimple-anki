# Review Rules

There are two ways you can review:

## Bulk review (recommended)
You actually don't do the review on Anki, but you follow the [ankitolightnovel](🔗_INSERT_LINK_HERE) or the [ankitoanime](🔗_INSERT_LINK_HERE) workflow. You watch/hear/review the chapter/episode. You might select all the cards that are related to this chapter/episode and tag them with some kind of tag that says you have reviewed them once (for example "review1") BUT ACTUALLY DON'T bulk-grade them with some kind of add-on because you only want to put things in your Anki schedule VERY SELECTIVELY where you think long-term review is a good idea. In this case, you proceed with individual review, otherwise SUSPEND the cards (they will not be deleted, but you don't have to worry that they might appear in your reviews on Anki you want to prioritize).

## Individual review
In this review mode, you choose to do the reviewing on Anki and long-term. If you have not prepared the cards already as part of an earlier Bulk review, you either follow the [lightnoveltoanki](🔗_INSERT_LINK_HERE) or the [animetoanki](🔗_INSERT_LINK_HERE) workflow and then do the review on the prepared cards on Anki (again, you might want to filter out cards and only focus on a few ones and suspend the unnecessary ones).

---

## The rules i.e. steps for reviewing

After you have filtered out the most important notes, you have noticed that per note two cards exist. On the one hand the term card (black background), and on the other hand the pronunciation card (white background).

The term card is designed to test the MEANING of the expression, respectively the pronunciation card is designed to test the PRONUNCIATION of the expression you mined.

If you think that the meaning is not the priority of this card, but rather you mined the expression because it has an unusual reading or contains Kanjis you don't know and you want to focus on learning how to read it rather than what the expression means, or you already know the meaning but not the pronunciation, or you think you could recall the meaning easily if you see the word and know how it would be pronounced, SUSPEND the respective term card. Use case, for example: a very rare word with unusual Kanjis but that somehow captured your interest.

If you, however, have a card where the reading is obvious and you only want to focus on studying the meaning, suspend the pronunciation card just like that. Use case, for example: a kana expression, or a common verb that has a lot of different meanings depending on the context.

If you want to learn both pronunciation and term card, you don't have to suspend anything. Select all the card pairs (notes) and activate the [siblingsync](🔗_INSERT_LINK_HERE) add-on that provides an additional visual cue during the review whether the current card is a pure term card (has no pronunciation sibling, white square appears on the top right), or a pure pronunciation card (has no term sibling, black square appears on the top right).

---

## As for the reviewing itself and the pass/fail rules

If it is a pronunciation card, you have to get the exact pronunciation; it is a complete YES/NO situation where you are either right or wrong with no ambiguity.

If it is a term card, it is a bit more ambiguous. You don't want to spend too much time during the review, so you have to use a certain system: you might pass the card without actually checking the English definition overview just by feeling, but if you check the English definition overview, you have to decide whether the answer in your head is sufficient/similar enough or not. But rather than trying to think like that, think: "Is the meaning in my head COMPLETELY DIFFERENT than the meanings listed?" If yes, you fail the card; if no, you pass the card.

---

# Explanation of fields

*(In general, fields are only rendered if they are not empty and not technical fields)*

## Standard Mining Card produced with [yomitan](🔗_INSERT_LINK_HERE) and [ankiconnect](🔗_INSERT_LINK_HERE)

* **Note ID**: The purpose of this field is to uniquely identify a card during mining, so that if you mine two times the same word it will still be regarded as a unique card. For standard mining cards, it is the same as the mined sentence. It is a hidden technical field that might be used for add-on operations where the notes have to be uniquely identified, and not displayed anywhere during the review.
* **Word**: The exact expression like it has appeared in the mined sentence; that means that, for example, for verbs instead of the normalized dictionary form it will appear in the conjugated form like it has also appeared in the text. It appears both at front and back at the top regardless of card type.
* **Frequency**: For standard mining cards, this field displays how frequent the word appears. There is also a visual rule implemented: if the word belongs to the top 1000 most frequent words, the number will also appear red; if it belongs to the top 5000 most frequent words, green; top 15000, blue; top 30000, yellow; and otherwise gray (or invisible). It appears both at front and back at the top regardless of card type (however, in case the card type is term, if the frequency is over 30000 it is not visible in the front).
* **SoundFront**: It contains the audio file of the sentence like SoundBack. It is displayed at the front of the card, but only if the card is of the type term. If the card is of the type pronunciation, it does not appear, however, in the front of the card, since the sound would reveal the pronunciation it is not placed in this case.
* **SoundBack**: It contains the audio file of the sentence like SoundFront. It is displayed at the back of the card.
* **Picture**: A visual that is used to identify the source of the card and motivate the learning process. In the case of a pronunciation card, it is placed only at the back of the card. In case of the term card, a miniature version is displayed in the front as well as the usual display at the back of the card. The picture is placed in the middle of the card and also indicates that the elements below it are reference information while the elements at the same line and above are considered core information.
* **SentencePlain**: The mined sentence without furigana; the mined core expression is also displayed in bold and appears in gold during review. It appears on the front of the Pronunciation Card and the Term Card. In the term card, it also appears in the back but can be toggled with the SentenceFurigana field if clicked on.
* **Hint(Pronounciation)**: This is a field that is only used in the term card again. The user can click on it during review at the front of the card to see how the expression is pronounced. It is not used for pronunciation cards, since this is the thing that is tested in the pronunciation card. It has the same content as the field Pronunciation.
* **HintNotHidden**: This is a field that is also only used for the term card again and also only appears at the front of the card. Unlike Hint(Pronounciation), it appears immediately without a spoiler and can be seen immediately and is intended to write hints manually that give a cue or information for the meaning. For example, if the tested expression consists of Kanjis that can have different meanings like 額, which can either mean brow/forehead (ひたい) or (picture)frame|amount (of money) (がく), in this field a hint can be written like: `NOT (picture)frame|amount (of money) (がく)`.
* **Pronounciation**: Contains the reading of the expression in hiragana; it is displayed on the back of the Term Card as well as the Pronunciation Card. However, the positioning and the size differ; since it is the core element of the pronunciation card, it appears higher and in bigger font on the answer side (back of the card) than it does for the Term Card.
* **English Definiton Overview**: Contains an overview of several different English definitions that might apply for this expression. It is not the one specific definition that exactly fits the context but rather a list of all possible definitions. During the review, it is usually sufficient to have a general idea and only get one of the meanings within the list since you might also don't always want to read the sentence. It appears on the back of the Term Card as well as the Pronunciation Card. However, for the Term Card, since it is the subject that is tested, it appears in the top section above the picture element, while for the Pronunciation Card it is only secondary information and therefore placed below the picture section. Since the field might be very long, if a threshold is surpassed, it is collapsed into a details block and only unfolded if the user clicks on it again.
* **Correct English Definition**: Unlike the field English Definition Overview, it contains the one specific definition that also fits the context. By default, it is empty after the card is mined with Yomitan to Anki; it is either filled manually or with the help of an add-on as part of a workflow, for example during the "ankitolightnovel" workflow ([github link](🔗_INSERT_LINK_HERE)). It also appears where the English Definition Overview appears but is placed on top of it and in a bigger font.
* **Japanese Definition Overview**: Contains an overview of several different Japanese definitions that might apply for this expression. It is not the one specific definition that exactly fits the context but rather a list of all possible definitions. It is rather a reference than something you would actively look at. During the setup, it has also been prepared in a way so that the furigana is also displayed. It appears on the back of either card type; since it is to be seen as reference, it is placed below the picture element.
* **Correct Japanese Definition**: Unlike the field Japanese Definition Overview, it contains the one specific definition that also fits the context. By default, it is empty after the card is mined with Yomitan to Anki; it is either filled manually or with the help of an add-on as part of a workflow. It also appears where the Japanese Definition Overview appears but is placed on top of it and in a bigger font.
* **Sentence Furigana**: Copy of the Sentence Plain field but with Furigana added automatically through the [AJT addon](🔗_INSERT_LINK_HERE) which has been set up earlier. By default, it is shown at the back of the pronunciation and term card next to the picture element; it can also be toggled with the sentence plain field in case of the term card.
* **TranslationExampleSentence**: A field where later manually with the help of an add-on, for example the [google translate anki addon](🔗_INSERT_LINK_HERE), the translation of the sentences can be added in bulk. The field appears at the back of the card; it is less pronounced in the pronunciation card than in the term card. It is considered reference information and therefore, either way, below the middle line with the picture element.
* **Source**: Reference information on the back of the cards that indicates the source of the material. By default, it is left blank, but in the Yomitan settings in the "configure anki flashcards" section, the name of the source can be edited (however, every time the source changes it has to be modified again).
* **Link to Related Cards**: A field that is used in the add-on [SimpleLinker](🔗_INSERT_LINK_HERE); connections between other cards can be established through this add-on. The links are considered core information and both appear equally on pronunciation cards on the front as well as on the back (above the picture); no mobile support is provided, however.
* **Notes1**: This is also a field that does not have any automatically generated content. Unlike the hint field, it also appears in the pronunciation card (needs to be clicked on to unfold). In the pronunciation card, it appears in the front in the middle of the card, and on the back in the reference part. For the term card, in the front it appears in the footer that needs to be unfolded, and on the back in the reference part. It can be filled with additional information related to the card or substitute the hint fields for the pronunciation cards.
* **Notes2**: Analogous to Notes1.
* **NameDictionary**: Reference information where special readings for names might be displayed in the reference part of the back of a card.
* **GrammarDictionary1**: Reference information where additional grammar information might be displayed in the reference part of the back of a card (although it is obsolete since for the grammar a dedicated system is in place, however, for edge cases and very obscure grammar it might sometimes provide further hints).
* **AlternativeDictionary1**: Trivia information or special/historical information for proverbs; might be displayed in the reference part of the back of a card.
* **AlternativeDictionary2**: Trivia information or special/historical information for proverbs; might be displayed in the reference part of the back of a card.
* **SiblingSyncInfo**: A technical field the SiblingSync Addon uses to adjust and manage the pronunciation/term system.
* **Dump1 to Dump10**: Technical fields that allow to convert from previous note type to this note type, for example, without losing any information. Can also be used for technical add-ons and modifications on the cards; for example, the sibling sync add-on used the field Dump1 which was then renamed to SiblingSyncInfo and a new field with the name Dump1 was added again.

---

## Individual Grammar Card created with [(grammar web addon)](🔗_INSERT_LINK_HERE) and [(grammarminer anki addon)](🔗_INSERT_LINK_HERE) and [(grammar anki)](🔗_INSERT_LINK_HERE)

By default, the layout for the term cards are used and therefore the pronunciation sibling is automatically suspended.

* **Note ID**: For individual grammar cards, it is derived from the `nid` of the overlaying grammar card from the grammar deck (see grammar card on [grammar anki](🔗_INSERT_LINK_HERE) and individual mined grammar card on [grammar hub webaddon](🔗_INSERT_LINK_HERE)), with an additional suffix key that identifies the grammar sentence connection and is also used for technical operations during the generation of the grammar cards triggered by the grammarminer add-on.
* **Word**: The exact regex match that the web browser add-on found during the search.
* **Frequency**: Recycled and used for displaying the construction scraped from the overlaying grammar card and a link to the original grammar card.
* **SoundFront**: Since the grammar cards are also of the note type `miningsimple`, the audio of the mined sentence where the grammar pattern appeared can also be extracted as a part of the [lightnoveltoanki](🔗_INSERT_LINK_HERE) workflow.
* **SoundBack**: Analogous to SoundFront.
* **SentencePlain**: Same as standard mining.
* **SentenceFurigana**: Same as standard mining.
* **The other fields are all left empty**
