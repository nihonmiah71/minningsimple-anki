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

After you have filtered out the most important notes you have noticed that per note two cards exist. On the one hand the term card (black background), and on the other hand the pronounciation card (white background).

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
