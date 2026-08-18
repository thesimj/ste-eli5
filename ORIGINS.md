# Origins

This format borrows two finished standards. It invents no writing method.

Layer 1 is ASD-STE100, the controlled English of aerospace maintenance manuals. Layer 2 is the answer-first order that newsrooms, the US Army, and a McKinsey editor each arrived at on their own. The only new part is the stacking. The two layers act on different things, so they compose.

## Where Layer 1 comes from

Layer 1 is ASD-STE100 Simplified Technical English, minus its dictionary.

In the late 1970s the Association of European Airlines asked AECMA to study the readability of civil aviation maintenance documentation. AECMA is the European Association of Aerospace Industries, now ASD. AECMA asked the Aerospace Industries Association of America to help. Two project groups examined the existing controlled languages and researched real maintenance manuals. On June 30, 1983, in Amsterdam, they founded the AECMA Simplified English Working Group. Rene Van Dijk chaired that group from 1983 to 1987.

The standard states the problem it solves. English is the language of the aerospace and defense industry. English is often not the native language of the reader. English words carry many meanings and many synonyms. Complex sentence structure adds more confusion. In maintenance documents a misreading puts lives at risk.

AECMA released the first version on February 15, 1986, as document PSC-85-16598. The Air Transport Association of America required this English in its ATA100 specification in 1987. The current name pays tribute to ATA100. The document became ASD-STE100 with Issue 3 on January 15, 2005, with no change to the content. Wikipedia and several vendor pages date that rename to 2004. The standard's own release table contradicts them.

The Simplified Technical English Maintenance Group maintains the standard now. Issue 9 carries the date January 15, 2025, and ASD distributes it free of charge. Part 1 holds 53 writing rules in 9 sections. Part 2 holds 875 approved words. Part 2 also lists 1274 non-approved words, each mapped to an approved alternative. The widely repeated figure of about 900 approved words is a rounded public-facing number.

Five rules of the standard shape Layer 1 directly. Rule 3.6 requires the active voice and allows the passive only in descriptive writing with an unknown agent. Rule 5.3 requires the imperative form for instructions. Rule 5.1 caps a procedural sentence at 20 words, including warnings and cautions. Rule 6.3 caps a descriptive sentence at 25 words. Rule 6.6 caps a paragraph at six sentences. The standard writes these as hard maximums, not as recommendations.

ASD-STE100 approves each word with one meaning and one part of speech. The verb "to fall" means to move down by the force of gravity, and never means to decrease. The standard picks "start" and drops "begin", "commence", "initiate" and "originate". Rules 1.2 and 1.3 enforce this. A small number of approved words carry more than one part of speech and meaning, such as "flush".

This format keeps the rules and drops the dictionary. The approved word list is aerospace vocabulary and covers no software term.

Ogden's Basic English is the ancestor of the whole family. Ogden published it in 1930 with an 850-word vocabulary. Churchill set up a cabinet committee in 1943 and made a Commons statement on 9 March 1944. Ogden assigned the copyright to the Crown in June 1946. The Basic English Foundation started in 1947 with a Ministry of Education grant and wound up its activities in the 1960s. Kuhn's 2014 survey judges Ogden's informal grammar rules too weak to reduce the complexity of the language.

Caterpillar introduced Caterpillar Fundamental English in 1971. It used roughly 800 to 1,000 words with one meaning each, and it built on Basic English. Caterpillar discontinued it in 1982. Compliance was not enforceable, and many readers trained in the language still could not read the documents labelled compliant. Caterpillar started Caterpillar Technical English in 1991 with a lexicon of about 70,000 terms of narrow semantic scope. A machine checker built on Carnegie Mellon's KANT parser enforced it.

Two smaller house languages fill out the lineage. Eastman Kodak built Kodak International Service Language in the early 1980s, with fewer than 1,000 words and a core vocabulary of about 350. Strong documented it in Technical Communication in 1983. Arendse Bernth built EasyEnglish at IBM as a preprocessing step for machine translation inside the Information Development Workbench.

Boeing tried to own a language and ended up owning a checker. Boeing Technical English (1998) extended AECMA Simplified English beyond the aviation domain. Boeing discontinued it and apparently never deployed it. The Boeing Simplified English Checker survived, in use since 1990, with over 400 English-syntax rules. Boeing still sells it as an ASD-STE100 compliance tool. The pattern repeats across this lineage: house languages die and the shared enforceable standard survives.

The US plain language movement is a separate lineage with a separate driver. Nixon decreed that the Federal Register use "layman's terms". Carter issued Executive Order 12044 on 23 March 1978. Reagan rescinded Carter's orders and progress stalled through the 1980s. Clinton issued a Memorandum on Plain Language in Government Writing in 1998, and the Plain Writing Act became Public Law 111-274 on 13 October 2010. Obama issued Executive Order 13563 on 18 January 2011.

That law mandates a process and prescribes no word list. ISO also standardises no controlled vocabulary. ISO/TS 24620-1:2015 is a Technical Specification that classifies controlled natural languages. Later parts of the series cover controlled oral communication, stylistic guidelines and more. ISO 24495-1:2023 sets governing principles for plain language, and ISO published it in June 2023. ASD-STE100 remained the de facto controlled English standard.

## Where Layer 2 comes from

Layer 2 is the inverted pyramid, applied to explanation. Five communities reached the same order for their own reasons.

Journalism gets the credit, and the popular origin story fails checking. The story says Civil War reporters put the key fact first because the telegraph wire could be cut. Pöttker analysed the New York Herald and the New York Times. He places routine use about two decades after the war, around 1880 to 1890. Researchers examining Civil War papers find chronological stories instead. Mindich argues the opposite case, that the form starts with Stanton's telegram on Lincoln's death, published 15 April 1865.

The US Army writes the rule as bottom line up front. AR 25-50, dated 10 October 2020, paragraph 1-38b requires "putting the main point at the beginning of the correspondence (bottom line up front) and using the active voice". The rule predates that regulation. DA Pamphlet 600-67 already told leaders to put the bottom line in the first or second paragraph, not at the end. Catalog records date that pamphlet to 2 June 1986. That date is reported and I did not verify it from the document itself.

Barbara Minto built the same order for consulting reports. She worked at McKinsey from 1963 to 1973 and edited the reports crossing her desk. She noticed she kept reorganising ideas into a pyramid, where each point above summarises the points below. She taught it first as an internal manual, "Skillful Writing through Structured Thinking". She published The Pyramid Principle in 1985 and revised it as The Minto Pyramid Principle in 1996.

Jakob Nielsen measured how people read web pages in 1997. 79% of test users scanned every new page they came across. Only 16% read word by word. He recommended the inverted pyramid style, starting with the conclusion. Morkes and Nielsen tested rewrites of one site with 81 participants across three studies. They measured usability gains of 47% for scannable text, 58% for concise text and 124% for the combination.

Progressive disclosure is a separate and older idea. Nielsen's own write-up dates to 3 December 2006 and names no inventor. UX literature credits Carroll's IBM "training wheels" work of 1983 to 1984. That attribution is a secondary reconstruction and remains unverified.

The ELI5 name comes from Reddit. The user bossgalaga proposed r/explainlikeimfive in an r/AskReddit post on 28 July 2011. He asked for a place to ask questions without fear of downvotes. The moderators confirmed him as the founder in a memorial post on 29 July 2021. Some secondary sources instead date the subreddit's creation to September 2011.

The subreddit's own rules reject the literal reading of its name. The wiki says the forum "is not literally meant for 5-year-olds". It also says the forum "is meant for explanations, not for answers". Rule 3 gives an explanation three parts: a context, a mechanism and an impact. Rule 4 carries the title "Explain for Laypeople". Layer 2 takes that structure and adds the analogy budget.

The Feynman name attaches to two things Feynman did not say. Goodstein documents something narrower. A questioner asked Feynman why spin-one-half particles obey Fermi-Dirac statistics. Feynman offered to prepare a freshman lecture on it, then reported back: "I couldn't do it. I couldn't reduce it to the freshman level. That means we don't really understand it." Goodstein published that recollection in Physics Today in 1989, decades after the exchange.

Two attached claims are retrofits. Scott H. Young coined the name "Feynman technique" in a blog post on 1 September 2011, and Feynman named no study method. The quote "If you can't explain it simply, you don't understand it well enough" traces to neither Einstein nor Feynman. Quote Investigator finds the nearest ancestor attributed to Rutherford only after his death.

## Why it works on a human reader

Each rule removes a construction with a measured comprehension cost.

The passive voice costs accuracy, not just elegance. Ferreira (2003) had 48 listeners identify who did what to whom. They answered correctly on 96% of active sentences and 85% of passive ones. They also took about 151 milliseconds longer on passives, 2009 against 1858. Readers run a fast noun-verb-noun heuristic beside the full parse. A passive whose real roles contradict word order gets misread.

Ambiguity produces confident misreading, not slow reading. Frazier and Rayner (1982) tracked eye movements on garden-path sentences. Fixations at the disambiguating word ran about 301 milliseconds against 260 in matched controls. About a third of regressions from that region landed back inside the earlier ambiguous region. Christianson and colleagues (2001) then showed the repair stays incomplete. After reading "While Anna bathed the baby played in the crib", readers correctly said the baby played, and still answered "yes" most of the time to "Did Anna bathe the baby?".

That is the hardest idea here, so it gets the one analogy in this document. The reader is a driver who takes a wrong turn, corrects the route, and still remembers the wrong street as the way home. The analogy has one limit. The driver knows about the wrong turn and the reader does not.

Sentence caps protect a working memory of about four chunks. Cowan (2001) argued that Miller's seven plus or minus two was a rough estimate and a rhetorical device. The real central capacity averages about four chunks. The limit counts chunks, not words. A familiar multiword term costs one chunk and an unfamiliar one costs several.

Distance between related words taxes memory more than raw word count does. Gibson (1998) showed processing cost rising with the distance between an incoming word and the head it attaches to. Beyond about two levels of nesting a structure becomes unprocessable. So keep a subject next to its verb and put long qualifying material last. Naturalistic corpus reading debates locality effects, and some studies report null or facilitatory results.

Shortening sentences helps, and the effect is small. Coleman (1962) split technical passages into short sentences and measured about 6% higher cloze scores. He then proposed four hypotheses for more detailed study, including one that splitting a sentence joined by "and" would not help. That paper never tested those hypotheses. Treat a sentence cap as a proxy for structural simplification, not as the mechanism itself.

Verbs beat nouns made from verbs, with a caveat. Coleman and Blumenfeld (1963) ran cloze tests on matched sentences. Readers restored a mean of 10.80 words from active-verb sentences and 9.63 from the nominalised versions (p < .01). Spyridakis and Isakson (1998) found the rule narrower than technical-writing folklore assumes. Denominalised prose helped native speakers focus on the more important information, and nominalised text may work quite well for non-native speakers. That result is an interaction, not a blanket win.

One name per thing has a measured price when you break it. Metzing and Brennan (2003) found addressees took 540 milliseconds longer when the same speaker switched from "the shiny cylinder" to "the silver pipe". A new speaker using the new term cost nothing. Brennan and Clark (1996) showed speakers reuse an established term most of the time with the same partner, and far less after a partner switch. Clark's Principle of Contrast explains the cost. A reader treats every change in wording as a change in meaning, then searches for a distinction that does not exist.

Hedges carry graded information that readers extract and then miscalibrate. Budescu, Por and Broomell (2012, n=556) asked readers what IPCC terms mean. Readers placed "very likely", defined as at least 90%, at about 62 on average. High probabilities came out too low and low probabilities too high. Pairing the word with a number increased differentiation and consistency.

Readers also recalibrate a hedge to the individual writer. Schuster and Degen (2020) showed listeners adapting to one speaker's use of "might" and "probably" within a session. So rotating "may", "might" and "could" for one probability level corrupts a calibration the reader is already running.

Stating uncertainty costs little trust. Van der Bles and colleagues (2020) ran five experiments with 5,780 participants, including a BBC News field experiment. Communicating uncertainty raised perceived uncertainty as intended. Trust fell only a little, and mostly for verbal rather than numerical formats. The editorial instinct to strip hedges for authority has no support in that data.

Presentation format changes load only when the material interlocks. Chandler and Sweller (1996) trained industry staff on a CAD/CAM package. A self-contained manual with integrated text and diagrams beat formats that forced switching between manual and screen. With low element interactivity the format made no difference. Style rules can remove extraneous load and cannot touch intrinsic load.

## Why it works on a language model

A system prompt outranks later turns by training, and this format counters failure modes that training created.

Wallace and colleagues (2024) describe an explicit instruction hierarchy. The order runs system message, then user message, then model outputs, then tool outputs. They trained GPT-3.5 to follow it. The trained model resisted instruction-overriding attacks better, including unseen attack types, with little loss on standard capabilities. That hierarchy is why a style rule in the system prompt persists instead of washing out.

Production system prompts already carry this class of rule. Anthropic publishes the claude.ai system prompt. It tells Claude to use "the minimum formatting needed for clarity". It tells Claude to write prose without bullets for reports, documents and explanations. It bans specific words, including "genuinely", "honestly" and "actually". It asks for a warm tone without condescending assumptions about the reader.

Instruction adherence decays across a conversation. Multi-IF (2024) tested 14 models over three turns, and every model failed more instructions with each added turn. The model o1-preview fell from 0.877 average accuracy at turn 1 to 0.707 at turn 3. Laban and colleagues (2025) simulated over 200,000 conversations and measured an average 39% drop from single-turn to multi-turn. Models commit early and do not recover. So put the style contract in the system prompt, not in chat.

Verbosity is a trained-in artefact. Singhal and colleagues (2023) found length correlated strongly with reward across three helpfulness preference datasets. A purely length-based reward reproduced most downstream RLHF gains over supervised fine-tuned models. Reward models absorb the length bias in preference data. Zheng and colleagues (2023) name verbosity bias as one of three systematic biases in LLM judges. The loop that scores answer quality prefers long answers too.

Sycophancy comes from the preference data, not from prompting. Sharma and colleagues (2023) found five assistants sycophantic across four free-form generation tasks. Human preference data rates viewpoint-matching responses higher. Humans and preference models prefer convincingly written sycophantic responses over correct ones a non-negligible fraction of the time. OpenAI traced the April 2025 GPT-4o regression to a thumbs-up and thumbs-down reward signal that diluted the primary reward. OpenAI pushed a system prompt edit as the fast mitigation before rolling back, which shows that system prompt style text moves the behaviour.

Hedge drift is measured. Peters and Chin-Yee (2025) compared 4,900 LLM summaries against human-authored ones. LLM summaries were about five times more likely to contain broad generalizations (OR = 4.85). An explicit accuracy prompt roughly doubled the odds of a generalized conclusion (OR = 1.90). The usual mechanism is grammatical scope widening, where a quantified finding becomes a generic claim. The GPT-4 technical report adds that post-training reduces the calibration the pre-trained model had.

The format also carries costs. Tam and colleagues (2024) measured a decline in reasoning under format restrictions, and stricter constraints degraded reasoning more. Those constraints were structural, such as JSON schemas, so transfer to a prose rubric is an inference. FollowBench shows adherence falling as constraints stack, which is the direct risk for a rule set this size. Cho and colleagues (2026) report that prompting for conciseness lowers perceived expertise. Their work is a preprint measuring perception, not accuracy.

Claim style, not correctness. Zheng, Pei and colleagues (2024) tested 162 personas on 2,410 factual questions across four model families. Personas gave no improvement over a no-persona control. Ashok and Poczos (2024) found prompting beats classical controllable-generation methods on most datasets and tasks. Prompting matches human performance on stylistic tasks and lags on structural ones. Layer 1 and Layer 2 are stylistic tasks.

## What the evidence does not show

The history and the mechanisms hold. The claim that controlled English improves comprehension does not hold cleanly.

Three groups of claims here are established. The ASD-STE100 dates, rule numbers and word counts come from the standard itself. The psycholinguistic results above are published, peer-reviewed and specific. The language model results above are published measurements from labs and benchmarks.

The comprehension evidence for Simplified English is weaker than industry retellings suggest. Simplified English is the earlier name of the same standard, and the studies below tested Boeing documents. Chervak, Drury and Ouellette (1996) tested 175 licensed technicians at eight US carriers. Their headline figures show error rates falling from 18% to 14% overall and from 31% to 13% for non-native speakers. Those figures come from a separate two-factor analysis, run because only 18 non-native speakers took part.

In that study's full three-factor model, the Simplified English main effect on accuracy did not reach statistical significance (p = 0.073). Only the workcard-by-language interaction did (p = 0.024). On the two easy workcards Simplified English scored nominally worse, 19% error against 17%.

Four more studies split the same way. Shubert and colleagues (1995) tested 130 engineering students on two Boeing procedures, and Simplified English helped only on the more complex one. Spyridakis, Holmback and Shubert (1997) measured translation quality with 39 student translators. Spanish speakers gained on most measures and Chinese speakers showed no statistically significant difference at all. Chervak (1996), Eckert (1997) and Stewart (1998) found no statistically significant advantage. The two studies testing only non-native speakers sit among those null results.

Two caveats attach to that paragraph. I read Chervak (1996), Eckert (1997) and Stewart (1998) through the summary table in Jahchan, Condamines and Cannesson (2016), not in the original theses. Temnikova, Orasan and Mitkov (2012) tested a different controlled language on 104 volunteers and found no clear effect on reading comprehension either.

No study in this literature shows controlled English is read, understood or translated faster. The Boeing and University of Washington authors state that directly. Chervak's own table lists task completion time as not statistically significant. Jahchan's cross-study table records the same null for five of the six studies it reviews.

Controlled language helps older machine translation and not neural machine translation. Marzouk and Hansen-Schirra (2019) tested 216 source sentences in two versions across five systems. Rule-based, statistical and hybrid systems improved. The neural system's quality decreased after the rules were applied. O'Brien and Roturier (2007) found only a handful of rules mattered, and rewriting passives sometimes degraded output by introducing part-of-speech ambiguity.

The translation cost savings quoted for controlled English, commonly 20% to 40%, rest on no published measurement that this research located. The closest peer-reviewed industrial report, Kamprath and colleagues (1998), lists only qualitative benefits. Treat any specific percentage as unverified.

No published study evaluates an ASD-STE100-style rule set or an answer-first schema as a system prompt and measures factual accuracy or reader comprehension. SpeciaLex (2024) does operationalise ASD-STE100 as an in-context constraint across 18 subtasks. It measures constraint adherence and not accuracy or comprehension. So the case for this format rests on mechanism and on adjacent measurement, not on a direct test.

Six claims in common circulation are folklore or error, and this document drops them.

1. The Civil War telegraph origin of the inverted pyramid is folk etymology.
2. "If you can't explain it simply, you don't understand it well enough" belongs to neither Einstein nor Feynman.
3. The name "Feynman technique" is Scott Young's 2011 coinage, and Feynman named no study method.
4. The dictionary holds 875 approved words, and "about 900" is a rounded approximation.
5. The rename to ASD-STE100 happened in 2005, and the common 2004 date contradicts the release table.
6. The sentence limits are hard maximums in the standard, not recommended maximums.

Two further attributions stay marked as unverified: the origin of progressive disclosure in Carroll's training wheels work, and the 2 June 1986 date for DA Pamphlet 600-67.

## Sources

- ASD-STE100 Simplified Technical English, Issue 9, 15 January 2025. https://www.asd-ste100.org/assets/files/ASD-STE100_ISSUE9.pdf
- ASD STEMG, "About STE". https://www.asd-ste100.org/about_STE.html
- Kuhn, T. (2014). "A Survey and Classification of Controlled Natural Languages." Computational Linguistics 40(1). https://aclanthology.org/J14-1005.pdf
- Kaji, H. (1999). "Controlled Languages for Machine Translation: State of the Art." MT Summit VII. https://aclanthology.org/1999.mtsummit-1.6.pdf
- Records of the Basic English Foundation, Archives Hub. https://archiveshub.jisc.ac.uk/data/gb366-bef
- Strong (1983). "Kodak international service language." Technical Communication 30(2), 20-22.
- Bernth, A. (1998). "EasyEnglish: preprocessing for MT." CLAW-98. https://mt-archive.net/90/CLAW-1998-Bernth.pdf
- Kamprath, C., Adolphson, E., Mitamura, T. & Nyberg, E. (1998). "Controlled Language for Multilingual Document Production: Experience with Caterpillar Technical English." CLAW-98. https://aclanthology.org/www.mt-archive.info/90/CLAW-1998-Kamprath.pdf
- Boeing Simplified English Checker. https://www.boeing.com/company/simplified-english-checker
- Digital.gov, "Plain language: history and timeline." https://digital.gov/resources/plain-language-history-and-timeline
- Plain Writing Act of 2010, H.R. 946, Public Law 111-274. https://www.congress.gov/bill/111th-congress/house-bill/946
- ISO/TS 24620-1:2015, Controlled natural language, Part 1. https://standards.iteh.ai/catalog/standards/iso/aedda5ca-c046-4dfe-8095-89840639f8ce/iso-ts-24620-1-2015
- ISO 24495-1:2023, Plain language, Part 1.
- Pöttker, H. (2003). "News and its communicative quality: the inverted pyramid." Journalism Studies 4(4), 501-511. https://www.tandfonline.com/doi/abs/10.1080/1461670032000136596
- Scanlan, C. (2003). "Birth of the Inverted Pyramid." Poynter. https://www.poynter.org/reporting-editing/2003/birth-of-the-inverted-pyramid-a-child-of-technology-commerce-and-history/
- AR 25-50, Preparing and Managing Correspondence, 10 October 2020. https://armypubs.army.mil/epubs/DR_pubs/DR_a/ARN42124-AR_25-50-007-WEB-13.pdf
- DA Pamphlet 600-67, Effective Writing for Army Leaders. https://www.govinfo.gov/app/details/GOVPUB-D101-PURL-LPS69018
- McKinsey alumni profile of Barbara Minto. https://www.mckinsey.com/alumni/news-and-events/global-news/alumni-news/barbara-minto-mece-i-invented-it-so-i-get-to-say-how-to-pronounce-it
- Nielsen, J. (1997). "How Users Read on the Web." https://www.nngroup.com/articles/how-users-read-on-the-web/
- Morkes, J. & Nielsen, J. (1997). "Concise, SCANNABLE, and Objective." https://www.nngroup.com/articles/concise-scannable-and-objective-how-to-write-for-the-web/
- Nielsen, J. (2006). "Progressive Disclosure." https://www.nngroup.com/articles/progressive-disclosure/
- r/explainlikeimfive founding post, 28 July 2011, and detailed rules wiki. https://www.reddit.com/r/explainlikeimfive/wiki/detailed_rules/
- Goodstein, D. (1989). "Richard P. Feynman, Teacher." Physics Today 42(2), 70-75.
- Young, S. H. (2011). "Learn Faster with the Feynman Technique." https://www.scotthyoung.com/blog/2011/09/01/learn-faster/
- Quote Investigator, "Explain it to a barmaid." https://quoteinvestigator.com/2019/10/19/barmaid/
- Ferreira, F. (2003). "The misinterpretation of noncanonical sentences." Cognitive Psychology 47, 164-203. https://tallinzen.net/media/readings/ferreira_2003.pdf
- Frazier, L. & Rayner, K. (1982). "Making and correcting errors during sentence comprehension." Cognitive Psychology 14, 178-210. https://www.coli.uni-saarland.de/masta/WS15/FrazierRayner1982.pdf
- Christianson, K., Hollingworth, A., Halliwell, J. F. & Ferreira, F. (2001). "Thematic roles assigned along the garden path linger." Cognitive Psychology 42, 368-407.
- Cowan, N. (2001). "The magical number 4 in short-term memory." Behavioral and Brain Sciences 24(1), 87-114.
- Gibson, E. (1998). "Linguistic complexity: locality of syntactic dependencies." Cognition 68(1), 1-76. https://tedlab.mit.edu/tedlab_website/researchpapers/Gibson_1998_Cogn.pdf
- Coleman, E. B. (1962). "Improving comprehensibility by shortening sentences." Journal of Applied Psychology 46(2), 131-134.
- Coleman, E. B. & Blumenfeld, J. P. (1963). Psychological Reports 13, 651-654. https://journals.sagepub.com/doi/10.2466/pr0.1963.13.3.651
- Spyridakis, J. H. & Isakson, C. S. (1998). Journal of Technical Writing and Communication 28(2), 163-188. https://journals.sagepub.com/doi/10.2190/01HD-MHU1-QNX9-R3YE
- Metzing, C. & Brennan, S. E. (2003). "When conceptual pacts are broken." Journal of Memory and Language 49(2), 201-213.
- Brennan, S. E. & Clark, H. H. (1996). JEP: Learning, Memory, and Cognition 22(6), 1482-1493.
- Budescu, D. V., Por, H.-H. & Broomell, S. B. (2012). "Effective communication of uncertainty in the IPCC reports." Climatic Change 113, 181-200.
- Schuster, S. & Degen, J. (2020). "I know what you're probably going to say." Cognition 203, 104285.
- van der Bles, A. M., van der Linden, S., Freeman, A. L. J. & Spiegelhalter, D. J. (2020). PNAS 117(14), 7672-7683. https://www.pnas.org/doi/abs/10.1073/pnas.1913678117
- Chandler, P. & Sweller, J. (1996). "Cognitive load while learning to use a computer program." Applied Cognitive Psychology 10(2), 151-170.
- Chervak, S., Drury, C. G. & Ouellette, J. P. (1996). "Field Evaluation of Simplified English for Aircraft Workcards."
- Shubert, S. K., Spyridakis, J. H., Holmback, H. K. & Coney, M. B. (1995). Journal of Technical Writing and Communication 25(4), 347-369.
- Holmback, H., Shubert, S. & Spyridakis, J. (1996). "Issues in Conducting Empirical Evaluations of Controlled Languages." CLAW-96. https://mt-archive.net/90/CLAW-1996-Holmback.pdf
- Spyridakis, J. H., Holmback, H. & Shubert, S. K. (1997). IEEE Transactions on Professional Communication 40(1), 4-12.
- Jahchan, N., Condamines, A. & Cannesson, E. (2016). CNL 2016, 69-80. https://shs.hal.science/halshs-01379559/document
- Temnikova, I., Orasan, C. & Mitkov, R. (2012). "CLCM." LREC 2012, 3007-3014. https://aclanthology.org/L12-1535/
- O'Brien, S. & Roturier, J. (2007). "How Portable are Controlled Language Rules?" MT Summit XI. https://aclanthology.org/2007.mtsummit-papers.46/
- Marzouk, S. & Hansen-Schirra, S. (2019). Machine Translation 33(1-2), 179-203. https://link.springer.com/article/10.1007/s10590-019-09233-w
- Wallace, E., Xiao, K., Leike, R., Weng, L., Heidecke, J. & Beutel, A. (2024). "The Instruction Hierarchy." https://arxiv.org/abs/2404.13208
- Anthropic system prompts release notes. https://platform.claude.com/docs/en/release-notes/system-prompts
- He, Y. et al. (2024). "Multi-IF." https://arxiv.org/abs/2410.15553
- Laban, P., Hayashi, H., Zhou, Y. & Neville, J. (2025). "LLMs Get Lost In Multi-Turn Conversation." https://arxiv.org/abs/2505.06120
- Zhou, J. et al. (2023). "Instruction-Following Evaluation for Large Language Models" (IFEval). https://arxiv.org/abs/2311.07911
- Jiang, Y. et al. (2024). "FollowBench." ACL 2024, 4667-4688. https://aclanthology.org/2024.acl-long.257/
- Singhal, P., Goyal, T., Xu, J. & Durrett, G. (2023). "A Long Way to Go: Investigating Length Correlations in RLHF." https://arxiv.org/abs/2310.03716
- Zheng, L. et al. (2023). "Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena." https://arxiv.org/abs/2306.05685
- Sharma, M. et al. (2023). "Towards Understanding Sycophancy in Language Models." https://arxiv.org/abs/2310.13548
- OpenAI (2025). "Expanding on what we missed with sycophancy." https://openai.com/index/expanding-on-sycophancy/
- Peters, U. & Chin-Yee, B. (2025). "Generalization bias in large language model summarization of scientific research." Royal Society Open Science 12(4), 241776. https://pmc.ncbi.nlm.nih.gov/articles/PMC12042776/
- OpenAI (2023). "GPT-4 Technical Report." https://arxiv.org/html/2303.08774v4
- Tam, Z. R. et al. (2024). "Let Me Speak Freely?" EMNLP 2024 Industry Track. https://arxiv.org/abs/2408.02442
- Cho, H. et al. (2026). "A Concise Agent is Less Expert." https://arxiv.org/abs/2601.10809
- Zheng, M., Pei, J., Logeswaran, L., Lee, M. & Jurgens, D. (2024). "When 'A Helpful Assistant' Is Not Really Helpful." Findings of EMNLP 2024. https://arxiv.org/abs/2311.10054
- Ashok, D. & Poczos, B. (2024). "Controllable Text Generation in the Instruction-Tuning Era." https://arxiv.org/abs/2405.01490
- Imperial, J. M. & Tayyar Madabushi, H. (2024). "SpeciaLex: A Benchmark for In-Context Specialized Lexicon Learning." https://arxiv.org/abs/2407.13297
