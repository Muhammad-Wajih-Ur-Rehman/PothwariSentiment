# **PothwariSentiment Annotation Guidelines** 

**Version:** 1.0 **Author:** Muhammad Wajih Ur Rehman **Date:** 22 June 2026 **Project:** dataset and sentiment corpus for the Pothwari language. **Affiliation:** Independent Researcher **License:** CC BY 4.0 **Contact:** wajhirehman1@gmail.com 

## **Table Of Contents** 

**Section 1 — Project Overview** 

**Section 2 —Script, Language Variety, and Orthographic Section 3 —Sentence & Label Definitions** 

**Section 4 — Edge Cases** 

**Section 5 — Annotation Protocol** 

**Section 6 — Practice Set** 

**Section 7 — Summary Reference Card Section 8 — Technical Encoding Requirements** 

**Section 9 — Guideline Version Control and Update Protocol Section 10 — Data Backup Protocol** 

**Section 11 — Baseline Experiment Plan** 

**Section 12 — Target Journal Structure** 

## **1. Project Overview** 

## **1.1 Background** 

This document provides the official annotation guidelines for PothwariSentiment, the first publicly available sentiment analysis dataset for the Pothwari language. Pothwari (also written as Potohari, Potwari, or Pothohari) is an Indo-Aryan language spoken primarily in the Rawalpindi-Islamabad region of Punjab, Pakistan, and is classified under the Pahari-Pothwari dialect continuum. Despite being spoken by 35 to 40 million people, Pothwari has no existing labelled NLP resources in any public repository or published academic literature. This dataset addresses that gap. 

## **1.2 Purpose** 

I present the first structured written corpus of Pothwari in Nastaliq script, with sentiment annotation as the foundational NLP layer — providing the first machine-readable written resource for a language spoken by millions with zero prior digital representation. The goal of this annotation task is to assign a sentiment label to each Pothwari sentence in the dataset. Sentiment labels reflect the emotional tone expressed by the writer or speaker of the sentence. There are three possible labels: Positive, Negative, and Neutral. 

Your labels must reflect the sentiment expressed in the sentence itself — not your personal opinion about the topic being discussed, and not how the sentence makes you feel as a reader. 

Read this entire document before labelling any sentence. During annotation, if you are unsure about any sentence, return to this document before making a decision. Do not guess. 

## **1.3 Data Sources and Copyright Policy** 

All sentences in the PothwariSentiment dataset originate exclusively from one source: direct elicitation from two native speakers of Rawalpindi-region Pothwari. No social media content, no published literary works, no third-party text of any kind is included in this dataset. 

## **The Single Approved Source — Direct Contributor Elicitation** 

The dataset is constructed entirely through structured elicitation from two native Pothwari speakers: 

- The project lead, a native speaker of the Rawalpindi-region Pothwari, based in Rawalpindi 

- • One designated contributor, also a native speaker of Rawalpindi-region Pothwari, who additionally serves as the second annotator for inter-annotator agreement calculation 

Each contributor writes 1,000 original sentences in Nastaliq script following the structured prompts defined in Section 1.6. All sentences are written specifically for this dataset and have never been published elsewhere. Full copyright of contributed sentences belongs to the contributor from the moment of writing. By participating, each contributor grants irrevocable permission for their contributions to be published as part of this dataset under CC BY 4.0 license, confirmed through the written consent statement in Section 1.5. 

## **Reason of single source contribution:** 

The decision to build this dataset exclusively through native speaker elicitation rather than collecting naturally occurring text reflects a documented reality: no naturally occurring written Pothwari corpus exists in any publicly accessible digital space. Pothwari is a predominantly oral language. Where speakers write online, they use Urdu script and vocabulary rather than authentic Pothwari linguistic forms. Collecting from such sources would produce an Urdu-dominant dataset with surface-level Pothwari vocabulary, not a genuine Pothwari corpus. 

Elicitation from trained, linguistically aware native speakers, combined with the native speaker validation panel described in Section 2.5, ensures the dataset represents authentic Pothwari as spoken in the Rawalpindi and Northern Punjab region rather than an Urdu approximation. 

## **Not Approved Under Any Circumstances:** 

- Social media comments, posts, or any user-generated online content 

- Published literary works, poetry collections, or authored texts 

- Text collected through automated scraping or AI generation 

- Roman script text of any kind 

- Text produced by translation tools or language models 

## **1.4 Anonymization Policy** 

- Because all dataset sentences are written originally by two known contributors specifically for this project rather than collected from third-party sources, the anonymization burden is minimal. No sentences contain private information about external individuals by design. 

- Contributors must observe the following single rule when writing sentences: 

- **Do not include real phone numbers, CNIC numbers, precise home addresses, or any other personally identifiable information of any private individual in any submitted sentence.** If a sentence requires a name for grammatical completeness, use a generic placeholder name rather than a real person's full name. For example: "گا بندہ اے" is  احمد چن acceptable as a generic name usage. A sentence containing someone's full name, address, and phone number together is not acceptable. 

- Public figures such as politicians, sports personalities, or media figures may be named in sentences expressing opinions about their public roles without any anonymization requirement. 

- The project lead reviews all sentences for compliance with this rule during the cleaning phase before sentences enter Label Studio. Any non-compliant sentence is returned to the contributor for revision. 

## **1.5 Contributor Consent Statement** 

Before writing a single sentence for this dataset, both contributors confirm the following statement in writing via WhatsApp message to the project lead: 

_"I confirm that I am a native speaker of Pothwari as spoken in the Rawalpindi region. I agree to contribute 1,000 original sentences to the PothwariSentiment dataset. I understand that my contributions will be published publicly as part of an open academic dataset under the CC BY 4.0 license, meaning anyone can freely use, share, and build upon them with attribution to this project. My participation is entirely voluntary, and I may withdraw at any time before the dataset is published."_ 

The project lead saves a screenshot of both consent messages in the private records folder before any sentence writing begins. No sentences are used without prior confirmed consent. 

## **1.6 Label Balance Strategy** 

PothwariSentiment targets an approximately equal distribution across all three sentiment categories. The target distribution is: 

- Positive: 33% — approximately 660 sentences 

- Negative: 34% — approximately 680 sentences 

- Neutral: 33% — approximately 660 sentences 

Unlike datasets that collect naturally occurring text — where label distribution is uncontrolled — this elicited dataset allows precise balance management from day one. Each contributor follows structured prompts (Section 1.7) that specify exactly how many sentences of each sentiment type to write per session. 

**Running count tracking:** The project lead maintains a live spreadsheet that tracks sentences per category, updated after each contribution batch. This sheet is checked before each new writing session. If any category falls more than 10% below its target at any point during collection, the next session is dedicated exclusively to that category until balance is restored. 

**Contributors are explicitly told their category targets.** This transparency is methodologically sound and standard practice in elicited dataset construction. 

## **1.7 Structured Writing Prompts** 

Each contributor writes 1,000 sentences divided across five writing sessions of 200 sentences each. Sessions are separated by at least 24 hours to prevent fatigue-driven repetition and maintain linguistic naturalness across the dataset. 

## **Per session breakdown (200 sentences per session, 5 sessions):** 

- 66 POSITIVE sentences 

- 68 NEGATIVE sentences 

- 66 NEUTRAL sentences 

## **Total per contributor across all sessions:** 

- 330 POSITIVE sentences 

- 340 NEGATIVE sentences 

- 330 NEUTRAL sentences 

## **Prompts for POSITIVE sentences — write sentences that express:** 

- Happiness or joy about something that happened today or recently 

- Praise or approval of someone's work, behavior, or character 

- Love or affection toward family, friends, or home 

- Satisfaction with food, a place, a service, or an experience 

- Gratitude to God, a person, or life in general 

- Excitement about an upcoming or recent event 

- Pride in your own or someone else's achievement 

- Hope or optimism about the future 

## **Prompts for NEGATIVE sentences — write sentences that express:** 

- Complaint about a service, situation, person, or experience 

- Frustration with something that is not working or going wrong 

- Disappointment about an outcome that did not meet expectations 

- Criticism of someone's behavior, work, or decision 

- Sadness about a loss, absence, or difficult situation 

- Anger toward a person, institution, or event 

- Regret about a past decision or missed opportunity 

- Worry or fear about something uncertain or threatening 

## **Prompts for NEUTRAL sentences — write sentences that:** 

- State a fact about the weather, time, location, or daily routine 

- Describe what someone did or is doing without emotional commentary 

- Ask a plain question with no emotional loading 

- Announce something without expressing an opinion about it 

- Count, list, or enumerate something factually 

- Describe a place, object, or situation objectively 

## **Critical instruction for all sentences:** 

Every sentence must pass the authenticity test in Section 2.3 Rule 3 before submission. Do not write sentences that sound like Urdu with Pothwari words inserted. Write sentences exactly as you would say them to a family member at home. If a sentence sounds formal or Urdu-influenced when you read it back, revise it before submitting. 

## **Session management:** 

Do not write more than 200 sentences in a single day. Do not write all sentences of one category consecutively across multiple sessions — vary the categories within each session as specified. This prevents the dataset from having detectable stylistic patterns that reveal contributor fatigue or category-specific writing modes. 

## **1.7.1 AI-Assisted Elicitation Methodology:**

To ensure consistent sentiment balance across sessions and reduce cognitive load during sentence production, contributors use AI-generated English sentences as stimulus references during each writing session. This methodology is formally known as stimulus-based elicitation — a standard approach in low-resource language dataset construction where naturally occurring text is unavailable at scale.

**How it works:**

Before each writing session, the project lead generates 100 English reference sentences using a structured AI prompt. These sentences are distributed as 34 NEGATIVE, 33 POSITIVE, and 33 NEUTRAL examples covering varied everyday Pakistani topics and situations. The full AI prompt used to generate these references is archived in the /session_references/ folder of the project GitHub repository, one file per session, for complete methodological transparency.

**Critical instructions:**

Contributors use AI reference sentences as emotional and topical stimuli only. The process is:
Step 1 — Read the English reference sentence and understand its emotion and topic
Step 2 — Look away from the reference sentence completely before writing
Step 3 — Ask yourself: how would I express this feeling or situation in natural Pothwari as I would speak it at home?
Step 4 — Write that Pothwari sentence without looking at the English again
Step 5 — Apply the authenticity test from Section 2.3 Rule 3 before finalising
The English sentence and the resulting Pothwari sentence will share a sentiment category and general topic. They will not share vocabulary, sentence structure, or grammatical form. A Pothwari sentence that follows the syntactic structure of its English reference is not acceptable and must be rewritten from scratch.

**Puropse:**

Guaranteed sentiment balance across every session without manual counting during writing
Topic diversity enforced by the reference prompt structure
Edge case coverage: The AI prompt is designed to include sarcasm, rhetorical questions, blessings, and factual-sad sentences matching every edge case in Section 4
Reduced cognitive burden on contributors: Topic generation is handled by the reference, allowing contributors to focus entirely on authentic Pothwari language production

## **2. Script, Language Variety, and Orthographic Standards** 

## **2.1 Script Decision** 

All sentences in the PothwariSentiment dataset are written exclusively in Nastaliq script using the Perso-Arabic writing system standard in Pakistan. This decision reflects the historically established written tradition of Pothwari, which — where written forms exist — has always used the Shahmukhi/Nastaliq script as documented in classical works including those of Mian Muhammad Bakhsh (1830–1907). 

No Roman transliteration is accepted in this dataset under any circumstances. This restriction exists for two reasons. First, no standardized Roman orthography exists for Pothwari — informal online romanization varies entirely by individual preference and cannot be enforced consistently across contributors. Second, the purpose of this dataset is to establish the first structured written corpus of Pothwari in its authentic script. Accepting Roman text would undermine this foundational contribution. 

## **2.2 Language Variety** 

This dataset specifically represents the Rawalpindi-region variety of Pothwari as spoken in Rawalpindi district and the Islamabad Capital Territory. This variety is linguistically distinct from: 

- Pahari as spoken in Azad Jammu and Kashmir (covered by Gardazi et al., 2026) 

- • Mirpuri Pothwari as spoken in Mirpur district 

- Pahari as spoken in the Murree-Galyat area 

Contributors must be native speakers of the Rawalpindi-region variety specifically. Sentences reflecting other regional varieties should be flagged for review rather than labelled or included directly. 

## **2.3 Orthographic Standards — Critical** 

This section is the most important technical instruction in the entire document. Read it carefully before writing a single sentence. 

Pothwari has no formally published orthographic standard. This dataset is the first attempt to write Pothwari systematically and consistently in Nastaliq at scale. Every sentence contributed to this dataset is therefore an orthographic decision — a small act of establishing how this language looks in written form. 

Contributors must follow these orthographic rules without exception: 

## **Rule 1 — Use Pothwari grammatical markers, not Urdu equivalents** 

Pothwari and Urdu share the same script but have different grammatical markers. Always use the Pothwari form: 

|**Function**|**Pothwari (Use This)**|**Urdu (Do Not Use)**|
|---|---|---|
|Masculine possessive|نا|کا|
|Feminine possessive|نی|کی|
|Plural possessive|نے|کے|
|First person singular present|آں|ہوں|
|Second/third person plural present|و ےپ|ہیں|
|Past tense marker|سا|تھا / تھی / تھے|
|Negation|نئیں|نہیں|
|This/that|ایہہ / اوہ|یہ / وہ|
|Come/go (present)|اشنا / گشنا|آتا / جاتا|



## **Rule 2 — Use Pothwari vocabulary where it differs from Urdu** 

When a Pothwari word exists that differs from its Urdu equivalent, use the Pothwari word. Do not substitute Urdu vocabulary because it is easier to type or more familiar in written form. 

## Common examples: 

|**Meaning**|**Pothwari (Use This)**|**Urdu (Do Not**<br>**Use)**|
|---|---|---|
|Good / Fine|چنگا|اچھا|
|Very|وں ب / بڑا|بہت|
|To say / speak|آکھنا|کہنا|
|To do|کرنا (shared)|کرنا|
|House|کآر|گھر|
|Water|پانی (shared)|پانی|
|To eat|کھانا (shared)|کھانا|
|Now|ہن|اب|
|Why|کیاں|کیوں|
|What|کےہ|کیا|



Note: Many words are shared between Pothwari and Urdu. Shared vocabulary is acceptable. The rule applies specifically where a distinct Pothwari form exists — in those cases the Pothwari form must be used. 

## **Rule 3 — The authenticity test** 

Before submitting any sentence, apply this test: would you say this sentence exactly this way to a family member at home in Pothwari? If the sentence sounds like formal Urdu with one or two Pothwari words, revise it. If it sounds like natural spoken Pothwari written down, submit it. 

**Application to AI-referenced sentences:**
When using an English reference sentence as a stimulus, the authenticity test becomes even more important. After writing your Pothwari sentence, compare it against the English reference. If your Pothwari sentence follows the same word order as English, uses direct translations of English phrases, or sounds like it was constructed from English rather than spoken naturally, discard it and write again without looking at the reference at all. The English reference should have influenced only your choice of topic and emotional territory, nothing else.

## **Rule 4 — Diacritics (Zabar, Zer, Pesh)** 

Add diacritics where they are necessary to distinguish meaning or ensure correct pronunciation. Do not add diacritics to every word — that is unnecessary and inconsistent with how Nastaliq is normally written. Add them only where their absence would cause genuine ambiguity. 

## **Rule 5 — Typing method** 

Contributors who find Nastaliq typing difficult are encouraged to use the voice-to-text function on their smartphone's Urdu keyboard. Speak the sentence in Pothwari naturally. The phone will produce approximate Nastaliq output in Urdu. The contributor then corrects the grammatical markers and vocabulary to their authentic Pothwari equivalents using Rules 1 and 2 above. This correction step typically involves 2-4 word changes per sentence and takes under 30 seconds. 

## **2.4 Quality Control for Authenticity** 

The project lead reviews every contributed sentence specifically for linguistic authenticity before it enters the dataset. Any sentence that: 

- Uses Urdu grammatical markers where Pothwari markers exist 

- Uses exclusively formal Urdu vocabulary with no Pothwari features 

- Appears to be an Urdu sentence with superficial Pothwari substitutions 

will be returned to the contributor for revision with specific feedback on which words or markers need changing. Sentences that cannot be revised into authentic Pothwari will be discarded. 

This quality control step is not a criticism of contributors — it is the mechanism that ensures this dataset represents genuine Pothwari rather than Urdu in a Pothwari register. The linguistic integrity of the entire corpus depends on this distinction being maintained consistently. 

## **2.5 Native Speaker Validation Panel** 

To establish the linguistic legitimacy of the corpus and confirm that the Nastaliq Pothwari sentences represent authentic Rawalpindi-region Pothwari rather than Urdu in a Pothwari register, a Native Speaker Validation Panel is convened after sentence collection is complete and before annotation begins. 

**Panel composition:** A minimum of five native speakers of Rawalpindi-region Pothwari who are not contributors to the dataset. Panel members are recruited from the project lead's community network. They are not required to have academic or linguistic credentials — their qualification is native fluency in the Rawalpindi variety specifically. 

## **Process:** 

Each panel member independently reviews a randomly selected sample of 100 sentences from the cleaned dataset. For each sentence, they answer one question only: "Does this sentence sound like natural Pothwari as spoken in Rawalpindi, or does it sound like Urdu?" Response options are: Natural Pothwari / Sounds like Urdu / Uncertain. 

A sentence is flagged for revision if more than two panel members independently mark it as "Sounds like Urdu." Flagged sentences are returned to the contributing annotator for revision. If a sentence cannot be revised into natural Pothwari, it is discarded. 

**Documentation:** Each panel member's full name, approximate age, and neighborhood within Rawalpindi or Islamabad is recorded with their written consent via WhatsApp. This documentation is included in the dataset's published metadata as evidence of community validation. Panel members do not label sentiment; they assess linguistic authenticity only. 

**Purpose:** This step directly addresses the challenge of building a written corpus for an oral language. The two contributors are linguistically aware native speakers who produce high-quality Pothwari sentences. The validation panel confirms that this quality extends to broader community recognition. Together, they establish that the dataset represents the language as a community rather than two individuals' idiolects. 

## **3. Label & Sentence Definitions** 

## **3.1 Definition of a Valid Sentence** 

For this dataset, a valid sentence is defined as follows: 

**Length:** Between 5 and 50 words. Anything shorter than 5 words lacks sufficient context for reliable sentiment judgment. Anything longer than 50 words likely contains multiple sentiments and should be split or discarded. 

**Unity:** One sentence expresses one coherent thought or emotion. If a statement contains two clearly separate ideas — even joined by "اور" or "پر" — it must be split into two separate meaningful sentences before submission. Each part must independently meet the 5-word minimum. 

**Completion:** A sentence must be grammatically complete and independently understandable without additional context. Incomplete thoughts, sentence fragments, or statements that only make sense when read alongside another sentence are not valid. 

**Script:** Written entirely in Nastaliq script. No Roman characters, no English words, no numerals unless the numeral is integral to the meaning and cannot be written otherwise. 

## **Examples of valid sentences:** 

- A complete opinion about food, a person, an event, or a situation 

- A complete factual statement about something observable 

- A complete question with a clear emotional tone or no emotional tone 

- A complete blessing, prayer, or expression of feeling 

## **Examples of invalid sentences — discard these:** 

- Sentences under 5 words, even if emotionally clear 

- Sentences over 50 words — split them first, then evaluate each part 

- Sentences mixing Roman and Nastaliq script 

- Sentences that are clearly incomplete thoughts 

- Sentences requiring the previous sentence for context 

## **Handling Pothwari Couplets (Sher):** 

A sher consists of two lines (مصرع). Each line is treated as a separate sentence and evaluated independently. Do not submit or label a full couplet as one unit. Split it into its two individual lines first, verify each line meets the 5-word minimum, then submit them as two separate entries. The separate entities must be meaningful on their own. 

## **Label Definitions and Examples** 

## **3.2 POSITIVE** 

A sentence is labelled POSITIVE when it expresses any of the following: happiness, joy, praise, satisfaction, love, gratitude, excitement, pride, approval, hope, or any other favorable emotion or opinion toward a person, object, event, or situation. 

## **Example sentences labelled POSITIVE:** 

1. [Pothwari sentence expressing happiness about the day] — _Reason: expresses joy_ 

2. [Pothwari sentence praising someone's work] — _Reason: expresses approval and praise_ 

3. [Pothwari sentence expressing love for family] — _Reason: expresses affection_ 

4. [Pothwari sentence saying food is delicious] — _Reason: expresses satisfaction_ 

5. [Pothwari sentence expressing gratitude to God] — _Reason: expresses gratitude_ 

6. [Pothwari sentence expressing excitement about an event] — _Reason: expresses excitement_ 

7. [Pothwari sentence congratulating someone] — _Reason: expresses approval and warmth_ 

8. [Pothwari sentence expressing pride in a child's achievement] — _Reason: expresses pride_ 

## **3.3 NEGATIVE** 

A sentence is labelled NEGATIVE when it expresses any of the following: sadness, anger, frustration, disappointment, criticism, complaint, hatred, jealousy, regret, fear, or any other unfavorable emotion or opinion toward a person, object, event, or situation. 

## **Example sentences labelled NEGATIVE:** 

1. [Pothwari sentence complaining about bad work] — _Reason: expresses criticism_ 

2. [Pothwari sentence expressing sadness] — _Reason: expresses sadness_ 

3. [Pothwari sentence expressing anger at someone] — _Reason: expresses anger_ 

4. [Pothwari sentence expressing disappointment about an outcome] — _Reason: expresses disappointment_ 

5. [Pothwari sentence saying a place is terrible] — _Reason: expresses disapproval_ 

6. [Pothwari sentence expressing frustration] — _Reason: expresses frustration_ 

7. [Pothwari sentence expressing regret about a decision] — _Reason: expresses regret_ 

8. [Pothwari sentence expressing worry or fear] — _Reason: expresses fear_ 

## **3.4 NEUTRAL** 

A sentence is labelled NEUTRAL when it conveys factual information, states an observation, asks a plain question, or makes a statement with no emotional leaning in either direction. The sentence neither praises nor criticizes. It simply states something. 

## **Example sentences labelled NEUTRAL:** 

1. [Pothwari sentence stating a meeting will happen tomorrow] — _Reason: factual statement, no emotion_ 

2. [Pothwari sentence saying someone went to the market] — _Reason: factual observation_ 

3. [Pothwari sentence asking what time school starts] — _Reason: plain question, no emotion_ 

4. [Pothwari sentence saying it rained yesterday] — _Reason: factual weather observation_ 

5. [Pothwari sentence stating how many people are present] — _Reason: factual count_ 

6. [Pothwari sentence describing a road being constructed] — _Reason: factual description_ 

7. [Pothwari sentence asking where someone is going] — _Reason: plain question_ 

8. [Pothwari sentence stating the name of a place] — _Reason: factual information only_ 

## **4. Edge Cases** 

This section covers every difficult or ambiguous situation you may encounter. Read all of it carefully. 

## **4.1 Sarcasm** 

If a sentence uses positive words but the clear intention is mockery, criticism, or the opposite of what the words literally say, label it NEGATIVE. 

If you are not certain whether a sentence is sarcastic, label based on the literal words only. Do not assume sarcasm without clear evidence in the sentence itself. 

## **Example:** 

- [Pothwari sentence meaning "Oh, wonderful, you've broken it again" said mockingly] → NEGATIVE 

- [Pothwari sentence meaning "Great job" said sincerely as a compliment] → POSITIVE 

## **4.2 Mixed Sentiment** 

If a sentence contains both positive and negative feelings, choose the label that represents the stronger or dominant emotion overall. 

If the positive and negative elements are genuinely equal and you cannot determine which is stronger, label NEUTRAL. 

## **Example:** 

- [Pothwari sentence meaning "The food was good but the service was very bad"] → NEGATIVE, because the complaint about service is the dominant feeling being expressed 

- [Pothwari sentence meaning "It was an okay experience, some things were fine and some were not"] → NEUTRAL, because neither side dominates 

## **4.3 Code-Switched Sentences** 

It is natural for Pothwari speakers to mix Urdu or Punjabi words into their speech. This does not affect your labelling — assess the overall emotional tone of the sentence regardless of which language the individual words come from. 

However, if a sentence is more than 60% Urdu words and contains barely any Pothwari vocabulary or grammar, do not label it. Select EXCLUDE instead, and it will be removed from the dataset. 

## **4.4 Questions** 

A plain question with no emotional tone is NEUTRAL. 

A question that clearly expresses an emotion — frustration, excitement, sadness, disbelief — should be labelled according to that emotion. 

## **Examples:** 

- [Pothwari sentence meaning "What time is it?"] → NEUTRAL 

- [Pothwari sentence meaning "How many times do I have to explain this to you?!" expressing clear frustration] → NEGATIVE 

- [Pothwari sentence meaning "Did you really get full marks?!" expressing excitement and pride] → POSITIVE 

## **4.5 Prayers, Blessings, and Curses** 

These are very common in Pothwari speech and must be handled consistently. 

- Prayers for someone's health, wellbeing, success, or long life → POSITIVE 

- Expressions of gratitude to God → POSITIVE 

- Curses, ill-wishes, or prayers for harm toward someone → NEGATIVE 

## **Examples:** 

- [Pothwari blessing meaning "May God keep you safe and healthy"] → POSITIVE 

- • [Pothwari curse meaning "May God ruin your house"] → NEGATIVE 

## **4.6 Proverbs and Idioms** 

Label by the sentiment the speaker clearly intends, not by the literal meaning of the individual words. 

If the intended meaning is unclear from the sentence alone and no context is available, label NEUTRAL. 

## **4.7 Very Short Sentences** 

Sentences of fewer than 5 words that cannot be clearly understood without additional context should be labelled NEUTRAL unless the sentiment is completely obvious from the words alone. 

## **Examples:** 

- [Pothwari word or phrase meaning "Excellent!"] → POSITIVE, obvious from the word itself 

- [Pothwari phrase meaning "He went"] → NEUTRAL, no emotion determinable 

## **4.8 Factual Statements About Emotional Topics** 

A sentence can describe a sad, happy, or difficult event without the writer expressing any personal emotion. Label based on the emotional tone of the sentence, not the topic it describes. 

## **Examples:** 

- [Pothwari sentence meaning "My grandfather passed away last year" stated as a plain fact] → NEUTRAL, no emotional expression 

- [Pothwari sentence meaning "I am devastated since my grandfather passed away"] → NEGATIVE, clear emotional expression of grief 

- [Pothwari sentence meaning "There was an accident on the road today" stated as news] → NEUTRAL, factual report 

## **4.9 Religious and Political Statements** 

Label based on emotional tone only, not on your personal agreement or disagreement with the content. Your personal beliefs must not influence your label. If a religious or political sentence is stated as a neutral fact, label it NEUTRAL. If it expresses clear positive or negative emotion, label accordingly. 

## **4.10 What to Flag for Exclusion** 

Do not assign a Positive, Negative, or Neutral label to the following. Select EXCLUDE instead: 

- Sentences shorter than 5 words where the sentiment is not immediately obvious 

- • Sentences that are predominantly Urdu with minimal Pothwari content (more than 60% Urdu) 

- Sentences with no clear or interpretable meaning 

- Exact duplicate sentences 

- Spam, gibberish, random characters, or broken text 

- Sentences in a language other than Pothwari or mixed Pothwari-Urdu 

## **5. Annotation Protocols** 

## **5.1 Inter-Annotator Agreement Protocol** 

Inter-annotator agreement is measured using Cohen's Kappa, calculated between two designated overlap annotators: the project lead and one designated second annotator. 

**Overlap set:** 400 sentences selected randomly from the full cleaned dataset before annotation begins. These 400 sentences are assigned to both the project lead and the designated second annotator. All remaining sentences are assigned to single annotators only. 

**Independence requirement:** The two overlap annotators must complete their labels entirely independently. No discussion, no comparison, no sharing of labels until both have fully completed the overlap set. 

**Calculation:** Cohen's Kappa is calculated using sklearn.metrics.cohen_kappa_score in Python after both annotators complete the overlap set. 

**Target:** Kappa of 0.80 or above. If Kappa falls below 0.75, annotation guidelines are reviewed, problematic categories identified, guidelines updated, and the overlap set re-annotated from scratch. 

## **Interpretation scale used in this project:** 

|**Kappa Value**|**Interpretation**|
|---|---|
|Below 0.60|Poor — guidelines require major revision|
|0.60 – 0.74|Moderate — guidelines require clarification|
|0.75 – 0.84|Good — acceptable for publication|
|0.85 – 1.00|Excellent — strong methodological validity|



## **Annotator Timestamp Verification** 

Label Studio automatically records a timestamp for each annotation. The project lead reviews these timestamps after each session. Any session where 50 or more annotations were completed in under 20 minutes is flagged for quality review, as this pace is insufficient for genuine 30second-per-sentence consideration 

## **5.2 Annotation Rules and Process** 

Follow these rules strictly throughout every annotation session: 

1. Read the full sentence completely before deciding on a label 

2. Do not spend more than 30 seconds on any single sentence 

3. If you are still unsure after 30 seconds, label it NEUTRAL and move on 

4. Do not discuss your labels with other annotators during an active session 

5. Do not look at what other annotators have labelled before completing your own labels 

6. Complete a maximum of 50 sentences per sitting 

7. Take a minimum 10-minute break after every 50 sentences — consistency drops significantly without breaks 

8. Do not go back and change previous labels unless you discover you fundamentally misunderstood a guideline, in which case, inform the project lead before making any changes 

9. If you notice a sentence that seems offensive, harmful, or deeply inappropriate, flag it for the project lead rather than labelling or excluding it yourself 

## **6. Practice Set** 

Before beginning real annotation, complete the following 20 sentences independently. Write your answers on paper or a separate document without consulting anyone. After completing all 20, compare your answers with the answer key provided by the project lead. If you disagree with more than 4 answers, re-read the guidelines and repeat the practice set. 

Do not proceed to real annotation until you have passed the practice set. 

## **# Sentence Your Label** 

- 1 [Pothwari sentence] 

- 2 [Pothwari sentence] 

- 3 [Pothwari sentence] 

- 4 [Pothwari sentence] 

- 5 [Pothwari sentence] 

- 6 [Pothwari sentence] 

- 7 [Pothwari sentence] 

- 8 [Pothwari sentence] 

- 9 [Pothwari sentence] 

- 10 [Pothwari sentence] 

- 11 [Pothwari sentence] 

- 12 [Pothwari sentence] 

- 13 [Pothwari sentence] 

- 14 [Pothwari sentence] 

- 15 [Pothwari sentence] 

- 16 [Pothwari sentence] 

- 17 [Pothwari sentence] 

- 18 [Pothwari sentence] 

- 19 [Pothwari sentence] 20 [Pothwari sentence] 

**Answer Key** (provided separately by project lead after annotator completes the practice set) 

## **7. Summary Reference Card** 

Print this and keep it visible during annotation sessions. 

**Label Use when the sentence expresses...** POSITIVE Happiness, praise, love, gratitude, satisfaction, excitement, approval 

NEGATIVE Sadness, anger, frustration, disappointment, criticism, complaint, fear, regret 

NEUTRAL Facts, plain questions, observations with no emotional tone 

EXCLUDE Too short, predominantly Urdu, meaningless, duplicate, gibberish 

**Golden rule: Label the emotion in the sentence, not your reaction to the topic.** 

## **8. Technical Encoding Requirements** 

All files in the PothwariSentiment project containing Pothwari text must be saved in UTF-8 encoding. This applies to every CSV file, every text file, and every document containing Nastaliq script. 

## **For annotators submitting contributed sentences:** 

Type your sentences in any Urdu keyboard app on your phone and send them to the project lead via WhatsApp. Do not attempt to type and format your own CSV files. The project lead handles all file formatting. 

## **For the project lead when handling files:** 

In Microsoft Excel: Never open a CSV file by double-clicking it. Always open Excel first, go to Data → From Text/CSV → select your file → in the import wizard, select UTF-8 encoding explicitly before finishing import. 

In Notepad or any text editor: When saving any file containing Pothwari text, go to File → Save As → change encoding dropdown from ANSI to UTF-8. 

In Python: Always use this exact syntax when reading or writing any file: 

Python: 

_# Reading a file_ 

_with open('dataset.csv', 'r', encoding='utf-8') as f:_ 

_data = f.read()_ 

_# Writing a file_ 

_with open('dataset.csv', 'w', encoding='utf-8', newline='') as f:_ 

_writer = csv.writer(f)_ 

Never omit encoding='utf-8' when working with Pothwari text in Python under any circumstances. 

## **Verification check:** 

After saving any CSV file, reopen it and confirm the Nastaliq characters display correctly. If you see question marks, boxes, or random symbols instead of Nastaliq text, the encoding is wrong and must be fixed before the file is used. 

## **9. Guideline Version Control & Update Protocol** 

## **9.1 Version Numbering** 

Every update to this document produces a new version number recorded at the top of the document. Minor clarifications that do not change any label definition increment the decimal — v1.0 becomes v1.1. Any change that redefines a label, adds a new edge case rule, or removes an existing rule increments the whole number — v1.0 becomes v2.0. 

## **9.2 Freeze Point** 

These guidelines are considered frozen after the annotator training session. From that point forward, label definitions cannot change. Only clarifications of existing definitions are permitted, and only as minor decimal increments. 

The freeze date is recorded here once the training session is completed: **[DATE TO BE FILLED AFTER TRAINING SESSION]** 

## **9.3 If a Minor Clarification Is Needed After Freeze** 

A minor clarification means adding an example or explaining an existing rule more clearly without changing what the rule actually says. 

Process: 

- Project lead updates document to next decimal version 

- All annotators are notified via WhatsApp with the specific change highlighted 

- Annotators confirm receipt in writing 

- No re-labelling required 

- Change is documented in the version log below 

## **9.4 If a Major Change Is Required After Freeze** 

A major change means any alteration to what a label actually means or covers. 

Process: 

- Stop all annotation immediately 

- Project lead reviews all previously labelled sentences in the affected category 

- Affected sentences are re-labelled from scratch under the new definition 

- Version number increments to the next whole number 

- All annotators are retrained on the specific change before resuming 

- The reason for the change and the number of sentences re-labelled is recorded in the version log 

## **9.5 Version Log** 

|**Version**|**Date**|**Type**|**What Changed**|**Sentences**<br>**Affected**|
|---|---|---|---|---|
|1.0|22 June 2026|Initial|Document created|N/A|
|1.1|24 June 2026|Minor|Added Section 1.7.1 describing AI-assisted elicitation methodology and added authenticity guidance for AI-referenced sentences to Section 2.3 Rule 3|N/A Pre-collection update|




Every future update adds one row to this table. This log is included as an appendix in the final published paper. 

## **Collection Period Documentation** 

All sentences were collected between [START DATE] and [END DATE]. This collection period is documented to allow future researchers to contextualize any topical or temporal bias in the data. 

## **10. Data Backup Protocol** 

## **10.1 Label Studio Export Schedule** 

At the end of every annotation session without exception, the project lead exports the current state of all annotations from Label Studio as a CSV file and commits it to the private backup branch of the GitHub repository. 

This takes less than two minutes and is non-negotiable. No session ends without a backup being committed. 

Export procedure: 

- Open Label Studio project 

- Click Export 

- Select CSV format 

- Save file as: annotations_backup_[DATE].csv using today's date in YYYYMMDD format 

- Example: annotations_backup_20260621.csv 

- Commit this file to GitHub immediately 

## **10.2 Backup Folder Structure on GitHub** 

The GitHub repository maintains a dedicated folder called /backups/ containing every annotation export. Old backup files are never deleted — they accumulate as a timestamped history of the entire annotation process. 

Your repository structure should look like this: 

PothwariSentiment/ 

- ├ README.md 

├ annotation_guidelines.md 

- ├  .editorconfig 

- ├  .gitignore 

- ├ backups/ 

- │   ├ annotations_backup_YYYYMMDD.csv 

- │   ├ annotations_backup_YYYYMMDD.csv 

- │   └  ... 

- ├ raw_collected_data/ ← gitignored, never uploaded 

- └ scripts/ 

## **10.3 Secondary Backup** 

In addition to GitHub, the project lead maintains one additional backup of the most recent annotation export on Google Drive or any cloud storage service. This secondary backup protects against the unlikely scenario of both local machine failure and GitHub access loss simultaneously. 

## **10.4 Contributor Sentence Backups** 

All sentences received from contributors via WhatsApp are saved in a dedicated WhatsApp chat and additionally copied into a Google Doc immediately upon receipt. Never rely on WhatsApp alone as a storage system — messages can be lost if a phone is changed or an account is deleted. 

## **11. Baseline Experiment Plan** 

Upon completion of the annotated dataset, a baseline machine learning experiment will be conducted to demonstrate the dataset's utility for the sentiment classification task. 

## **Experimental Setup:** 

## **Dataset split:** 

- Training set: 80% of the final dataset (approximately 1,600 sentences) 

- Test set: 20% of the final dataset (approximately 400 sentences) 

- Split is stratified — meaning each split contains approximately equal proportions of Positive, Negative, and Neutral labels 

**Model:** Logistic Regression classifier using TF-IDF (Term Frequency-Inverse Document Frequency) character n-gram features. Character n-grams are used rather than word n-grams because Pothwari morphology is complex, and character-level features capture subword patterns more effectively for low-resource languages. 

Library: scikit-learn (Python) 

## **Evaluation Metrics Reported:** 

- Accuracy (overall) 

- Precision per class 

- Recall per class 

- F1 score per class 

- Macro-averaged F1 score 

## **Purpose of Baseline:** 

This experiment does not claim state-of-the-art performance. Its sole purpose is to demonstrate that the dataset contains a learnable sentiment signal and is suitable for training machine learning classifiers. Results establish a benchmark for future researchers to improve upon. 

## **Reporting:** 

Results are reported in a confusion matrix and a classification report table in the paper. All code used for the baseline experiment is published in the project GitHub repository under an MIT license for full reproducibility. 

## **12. Target Journal: Data in Brief (Elsevier)** 

Manuscript must follow the Data in Brief article structure exactly: 

1. Specifications Table — mandatory structured table covering subject area, data type, data collection method, data source location, data accessibility, and related research article 

2. Value of the Data — minimum 4 bullet points explaining why this data is useful, who benefits, and how it builds on existing work 

3. Data Description — what the dataset contains, its structure, and statistics 

4. Experimental Design, Materials and Methods — how it was collected, annotated, and validated 

5. Dataset Access — Hugging Face link, Zenodo DOI, GitHub link 

Paper length target: 4-6 pages excluding references. Data in Brief papers are deliberately short. 

Submission checklist before sending: 

- Dataset live on Hugging Face 

- DOI obtained from Zenodo 

- Cohen's Kappa score calculated and confirmed above 0.75 

- Baseline experiment complete (Section 11) 

- All author information and ORCID included 



*End of document*
