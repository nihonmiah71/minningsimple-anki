# Review Rules

There are two distinct ways you can approach your reviews:

## Review Modes

### 1. Bulk Review (Recommended)
In this mode, you do not actually perform the review directly inside Anki. Instead, you follow the [ankitolightnovel](🔗_INSERT_LINK_HERE) or the [ankitoanime](🔗_INSERT_LINK_HERE) workflow:

1. Watch, hear, and review (simultaneously) the specific chapter or episode (as part of the workflow).
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

Once you filter out the most important notes, you will notice that **two cards exist per note**:
1. **The Term Card:** Features a black background. It is designed to test the **MEANING** of the expression.
2. **The Pronunciation Card:** Features a white background. It is designed to test the **PRONUNCIATION** of the mined expression.

### Card Suspension Logic

* **Suspend the Term Card if:** 
  Meaning is not the priority. For example, you mined the expression because it has an unusual reading, contains Kanji you don't know, or you already know the meaning but want to focus entirely on how to read it. You can also suspend it if you can easily recall the meaning once you know the pronunciation.
  > **Use Case:** A very rare word with unusual Kanji that somehow captured your interest.

* **Suspend the Pronunciation Card if:** 
  The reading is obvious and you only want to focus on studying the meaning.
  > **Use Case:** A kana-only expression, or a common verb that has a lot of different meanings depending on the context.

* **Keep Both Cards if:** 
  You want to learn both the pronunciation and the term. In this case, do not suspend anything. Select all card pairs (notes) and activate the [SiblingSync Add-on](🔗_INSERT_LINK_HERE). This add-on provides a visual cue during review to show the card's status:
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
| **HintNotHidden** | Used for manual hints regarding the meaning. Appears immediately without a spoiler.<br>_Example for 額 (can mean brow/forehead [ひたい] or picture frame/amount [がく]): "NOT (picture)frame\|amount (of money) (がく)"_ | **Term Cards:** Front only. |
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

By default, these cards use the **Term Card** layout, and their Pronunciation Sibling is automatically suspended.

* **Note ID:** Derived from the `nid` of the overlaying grammar card from the grammar deck, featuring an additional suffix key identifying the grammar-sentence connection. Used for technical operations by the GrammarMiner add-on.
* **Word:** The exact regex match found by the browser add-on during the search.
* **Frequency:** Recycled to display the structural construction scraped from the overlaying grammar card, alongside a link to the original grammar card.
* **SoundFront / SoundBack:** Since these cards utilize the `miningsimple` note type, audio from the mined sentence where the grammar pattern appeared can be extracted via the [lightnoveltoanki](🔗_INSERT_LINK_HERE) workflow.
* **SentencePlain / SentenceFurigana:** Operates identically to Standard Mining Cards.
* **Other Fields:** All remaining fields are left empty by default.
