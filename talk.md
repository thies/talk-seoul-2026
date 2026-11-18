# Who Holds the Keys? AI, Power and Blind Spots in Property Markets

## Opening

### 0.1 2026 is the year in which AI has arrived in almost every aspect of my daily work

This is the year student emails changed. They used to be as varied as the students who wrote them. Some were confused, some got straight to the point. Some were in the Queen's English, others showed traces of thinking in another language first. Some were a bit rude, others overly polite.

This year they all sound alike. Smooth and polite: "Dear Professor Lindenthal, I hope this finds you well …" Perfect grammar. And way too long.

The same goes for dissertation proposals. The creative chaos of earlier years has given way to tidier, more generic proposals, with all the kinks ironed out by AI – and the same research topics suggested over and over again.

Claude is doing most of my coding (Oh, I do miss the quiet focus of coding at night dearly). Many rounds of conversation with co-authors have been replaced by shouting instructions at AI helpers. Reviewing has become a drag, too: papers cobbled together quickly by AI, with sticky AI language, no jumps, surprises and no linguistic vitamins.

### 0.2 AI is shaping property markets

In real estate markets, algorithms arrived much earlier than generative AI. Online platforms match buyers and sellers, landlords and tenants. Pricing algorithms recommend rents for vacant apartments every day. RealPage advertised that its software could help landlords "outperform the market 3% to 7%" (ProPublica, 2022). 

The examples that follow range from traditional machine learning to pricing algorithms and generative AI. They are not the same technology, of course, but they raise common questions: What happens when we delegate decisions or advice to systems that change who has information, who influences choices, and what gets noticed? This is not a Luddite's rant against new technology.

### 0.3 Three challenges: roadmap

So who holds the keys? I will look at three places where this question matters: who has information and sets prices, how systems shape decisions about people, and how AI influences the questions researchers ask. The issue is how delegating a task changes who has influence, and whether we can see and govern the consequences.

## 1. Algorithmic pricing and market power

### 1.1 Better prediction creates winners and losers

Fuster et al. (2022) ask what happens when US mortgage lenders switch from a traditional logit model to machine learning to predict default. The more accurate model spreads predictions out: some borrowers look less risky than before, others more risky. So there are winners and losers – and both are households.

White and Asian borrowers tend to gain. Black and Hispanic borrowers are disproportionately less likely to gain. In the authors' equilibrium model, interest rates become more unequal. But slightly more borrowers may get credit, and the acceptance-rate gap narrows marginally. Better prediction does not settle who benefits.

### 1.2 New platforms shift the balance of power

New platforms, however, move the needle in favour of the platform and its landlord customers.

One example is RealPage. Landlords send it their own lease data. RealPage adds what it knows about the rest of the market and sends back a recommended "optimal" rent. One customer explained why they wanted the price set by software rather than staff: "We said there's way too much empathy going on here. This is one of the reasons we wanted to get pricing off-site."

By 2019, about 30% of units in US apartment buildings with 20 or more units were priced this way.

Is this simply a better forecast, like the mortgage models? Or does it change who sets the price? My colleagues Calder-Wang and Kim (2026) separate two channels. The first is responsive pricing: rents follow the market faster. The second is coordination: the algorithm recommends prices that maximise adopters' profits jointly, as if they were coordinating.

In a boom, both channels push rents up. You cannot tell them apart. In a recession they part ways. A responsive landlord cuts the rent quickly to fill empty units. A coordinating landlord holds the rent and accepts vacancies.

They find both. Adopters' rents follow the market faster. But their conduct test also favours joint profit maximisation among landlords using the same software. The implied markup is about $25 per unit per month, on 4.2 million units. The authors do not test for collusion in the legal sense.

### 1.3 Antitrust litigation: data pooling and coordination

In August 2024, the US Department of Justice and eight states sued RealPage. The complaint says landlords share "nonpublic, competitively sensitive data" with RealPage, which uses it to recommend rents to their competitors.

The final judgment in the DOJ case makes the source of RealPage's power unusually visible: pooled data, up-to-date information, fine spatial detail and features that let landlords trade occupancy for higher rents. The remedy restricts the use of other landlords' data, its freshness and the geographic detail models can learn from it. It also restricts features that encourage keeping flats empty or automatically accepting recommendations. Regulation reaches into the design of the model itself.

### 1.4 Takeaway

New AI systems can shift the balance of power in property markets.

RealPage illustrates the network economics of data. The platform sits between landlords and sees a large part of the market at once. Each additional landlord can make its information more valuable to others, giving the platform an advantage that individual landlords cannot easily replicate.

Tenants can compare listings, but they cannot see the same market-wide information or coordinate their decisions in the same way. That is why regulation matters. It is not enough to ask whether algorithms predict rents accurately. We also need to ask who controls the data, who benefits from sharing it, and how the system changes competition.

## 2. Discrimination and testing of AI systems

The RealPage case shows why a system's information and design matter, not just its objective, cold performance. But how can we test AI decisions that affect people when the system itself is difficult to inspect?

### 2.1 Why test before deployment

Three years ago, Wayne Wan and I asked a simpler question about conventional machine-learning systems: do they do what we want them to do and – importantly – HOW do they get there? A model can score well and still be right for the wrong reasons.

We asked architects which parts of a façade tell you the age of a house: doors, windows, the shape of the roof. Trees and cars should be ignored. Then we checked whether the image classifier looked at the same things. It did.

The broader point is that prediction accuracy and acceptable behaviour are different things. Cross-validation alone is not enough in regulated environments. Housing is one.

### 2.2 Prior evidence: racial steering by LLMs

Fast forward to 2026. Liu et al. (2024) show racial steering in LLM-generated housing recommendations. They sent GPT-4 thousands of prompts about renting and buying in US cities. It recommended neighbourhoods that matched the home-seeker's stated race. Advice to home-seekers who gave no race looked like advice to White home-seekers: "default whiteness". Minority home-seekers were sent to neighbourhoods with lower opportunity indices.

Steering is exactly what in-person housing audits were designed to catch in estate agents. Now the adviser could be a chatbot.

### 2.3 Audit design: financially identical applicants, three UK cities

That Liu paper made me think: do the findings apply to the UK as well? In the British case, historically strong class divisions might be another angle: are they perpetuated in the LLMs' understanding of society and its spatial distribution?

So I set out to replicate their work in London, Birmingham and Manchester. What I have so far is a pilot study and quick working paper. But still, what a wonderful world, in which we can quickly replicate work in a different country!

I changed one important thing. In the US study, customers state their race and give no financial details. A gap in advice therefore mixes steering with what a model assumes a group can afford. My hypothetical customers send a CV and a full financial profile. Everyone has the same new job, income, savings, deposit and mortgage agreement in principle. Class and origin are never stated: they show through schools, universities, names, languages and places of education or work.

I asked Claude Opus 5.5 and GPT-6 Astra for three neighbourhoods and for advice on renting or buying: about 10,000 calls. I compare deprivation in recommended areas using the English Index of Multiple Deprivation.

### 2.4 Result: social class drives the largest gaps

Think of England split into ten groups of neighbourhoods, from the most deprived tenth to the least deprived tenth.

Same job, same income, same deposit. Yet Claude sends White British customers whose profiles signal a middle-class background to areas about one decile less deprived than those signalling a working-class background. For GPT-6 Astra the gap is about half a decile. Differences by ethnic origin are mostly smaller.

Should an adviser infer housing preferences from class signals when those preferences have not been stated? The differences may reflect stereotypes or inferred preferences; they do not, by themselves, prove discrimination. This is a pilot, and the findings need repetition.

### 2.5 Result: recent migrants told to rent

In this pilot, migration status matters most for tenure. With a deposit and a mortgage agreement in principle, both models advise buying in the long run in almost every case.

The difference is in what comes first. Claude advises recent migrants to rent first 45 percentage points more often than British customers of the same heritage; for GPT-6 Astra the gap is 20 points. Established migrants are treated much like British-born customers. The results aren't very robust at this stage. The models may be inferring residence status, familiarity with the market or intended length of stay. The pilot identifies a pattern, not its cause.

### 2.6 The test may shape what it measures

This may be the most important methodological point in my working paper: the test itself may influence what we measure.

While poring over the AI logs, I noticed a real shocker. Clever machines: having seen just ONE prompt, they smelled a rat. Asked why someone might have sent it, Claude Opus 5.5 identified a bias test in almost every case. GPT-6 Astra almost never did – or did not tell! The neatly formatted finances, the CV, the background details: they make the exercise look artificial.

In reasoning summaries accompanying the housing advice, Claude rarely mentions suspecting a test. But fairness comes up much more often for customers with a Pakistani or Nigerian background. Those summaries are not a direct view into the model's decision process, and we have not shown that audit recognition changes the neighbourhood recommendations.

Other research finds gaps three to four times larger when an audit is disguised (Lukk, 2026). So we need prompts that look more like ordinary housing enquiries, and repeated tests.

### 2.7 Results do not travel across places

Samad and co-authors (2026) ran a similar audit in four US cities. Steering showed up, but its direction and size changed from city to city. So my results for Birmingham, Manchester and London say little about Seoul. Audit results may depend on the prompt, the place and the model version.

There is an uncomfortable parallel with Volkswagen's diesel cars, which detected emissions tests and changed their behaviour. I am not suggesting deliberate deception here. This may be more a struggle to contain damage: developers put guardrails in place to prevent biased advice, but those safeguards may make models especially cautious when a prompt resembles an audit. It raises an awkward question: are we testing ordinary behaviour, or "best behaviour" under test conditions?

## 3. AI and the research agenda

In the previous section, AI was the object of study. Now AI is also entering the research process itself, helping determine which questions are proposed and pursued.

### 3.1 AI already writes research

Writing in research is changing as fast as my students' emails. Kobak and co-authors (2025) identified words that LLMs overuse. I replicated their study for real estate papers. For better or worse, my colleagues are "keeping up" with the technology, too.

Beyond writing, AI has become a very good research assistant. In the paper I will talk about next, we did not write a single line of code. Researchers use AI for ideas, too. How much influence might those suggestions have over what we decide is worth doing?

### 3.2 AI proposals cluster on familiar topics

Philip Kalikman, Daniel Ruf and I mapped fifty years of research in real estate finance and economics: 6,255 papers grouped into 80 clusters. Then we had Claude generate 3,200 research proposals and placed them on the same map.

Asked simply for "original research ideas in real estate economics and finance", the model goes to the same places again and again: climate risk, rent control, property tax and mortgage lending discrimination. GPT-5 and Gemini show a similar concentration. Every condition is more concentrated than the published field.

So far, the experiment shows the model's tendency, not that researchers have changed their agendas because of it. But, speculating a little, I expect these effects to be detectable as soon as next year.

There is also a possible second influence, working indirectly through citations. We asked which papers the model would cite for its own ideas. Callaway and Sant'Anna's difference-in-differences estimator comes up for 40 of 200 ideas, while the median paper comes up once. If researchers follow such suggestions, academic attention may become still more concentrated.

### 3.3 What gets overlooked

What barely registers in the model's ideas: mortgage finance, capital markets and institutional real estate.

The pull is not entirely new. The clusters the model favours have been gaining citations for a decade. So the model may be reproducing and exacerbating existing academic fashions, offering them back at scale as if they were independent suggestions. And a lot more extreme.

Climate risk and discrimination are important topics. But a healthy research community also needs a range of questions, methods and traditions. In the paper we compare this to microplastics pollution in the environment: the quiet accumulation of small influences eventually adds up.

## Conclusion

### 4.1 Accuracy does not guarantee fairness, competition or diversity

Across these examples, a system can perform its immediate task and still change who has influence. A more accurate credit model can widen access and still make rates more unequal. A pricing system can respond faster to the market while supporting higher joint profits among adopters. A housing adviser can sound helpful while making different recommendations to people with similar finances. And a research assistant can produce plausible ideas while repeatedly returning to familiar topics.

### 4.2 Governance: data sharing, discrimination testing, critical use in research, continuous monitoring

Who holds the keys? AI changes the distribution of power, often in ways that are hard to observe. For pricing, we need to examine shared information and incentives. For housing advice, we need to test assumptions models make about people and places. In research, scholars remain responsible for choosing questions and noticing what automated suggestions omit.

We cannot expect AI to disappear, nor should we want it to. But we can shape the institutions, tests and constraints that govern its use.

### 4.3 Thank you and questions

Thank you. I look forward to your questions.

## Speaker notes and source trail

These notes are for slide preparation and questions, not for delivery.

### Opening

- **0.2:** ProPublica, Vogell, 15 Oct 2022 ("outperform the market 3% to 7%"; daily price recommendations), saved at `realpage/sources/propublica.org_article_yieldstar-rent-increase-realpage-rent.html`. The sentence on online platforms matching buyers and sellers, landlords and tenants still has no source.

### 1. Algorithmic pricing and market power

- **1.1:** Fuster, Goldsmith-Pinkham, Ramadorai & Walther (2022), *Predictably Unequal? The Effects of Machine Learning on Credit Markets*, *Journal of Finance* 77(1), 5–47. The equilibrium summary follows the abstract and introduction. The paper calls its equilibrium computations a first step, not precise predictions.
- **1.2:** ProPublica, Vogell, 15 Oct 2022 (the "too much empathy" quote). Calder-Wang & Kim (2026), p. 3 (the two channels and the caveat on legal collusion), abstract ($25 per unit per month, 4.2 million units), section 1 (30% of units in buildings with 20+ units by end-2019).
- **1.3:** DOJ complaint, 23 Aug 2024 (`related-literature/realpage/DOJ_2024-08-23_complaint.pdf`): eight plaintiff states (North Carolina, California, Colorado, Connecticut, Minnesota, Oregon, Tennessee, Washington). "Nonpublic, competitively sensitive data" is from the heading of section II.D. The remedy terms (other landlords' data, training lag, geographic granularity, product features) are in the proposed final judgment of 24 Nov 2025, §§ IV.A.1, IV.A.3, IV.A.5, V.A. Entered on 19 May 2026 (Doc. 194). The entered text is not on the DOJ case page (checked 18 Nov 2026) and is not saved here. Indirect check: the DOJ's response to public comments (Federal Register, 8 May 2026, `realpage/sources/federalregister_2026-05-08_2026-09147_response-to-comments.html`) declines to amend ¶ IV.A.1 and says it will move to enter "the proposed Final Judgment". Where the M.D.N.C. opinion of 30 Sep 2026 (Doc. 223) quotes or paraphrases Doc. 194, it matches the proposal in wording and section numbers: § II.EE (definition of Revenue Management Product), § IV.A.3 (training only on data at least 12 months old), § IV.A.6 ("retrain applicable models"), § XIV (expires after seven years, terminable after four). The terms in the talk can be treated as the entered terms. Other rulings are listed in `related-literature/realpage/README.md`.
- **1.4:** The network-economics argument is the speaker's interpretation, not a finding in the sources.

### 2. Discrimination and testing

- **2.1:** Wan & Lindenthal (2023), *Testing Machine Learning Systems in Real Estate*, *Real Estate Economics* 51(3), 754–778. Checked against the 2020 working paper (`related-literature/Wan-Lindenthal_2023_REE_Testing_ML_Systems_Real_Estate_WP2020.pdf`), abstract and pp. 1–3. Check the published version before quoting it on a slide.
- **2.2:** Liu et al. (2024), abstract (`related-literature/Liu_2024_EAAMO_Racial_Steering_LLM_Housing.pdf`).
- **2.3:** Lindenthal (2026), 9 Nov draft, sections 1 and 5 (`related-literature/Lindenthal_2026_draft-2026-11-09_Social_Class_Ethnicity_Migration_AI_Housing_Advice_UK.pdf`). About 10,000 calls: 10,376 Stage 1 responses, 5,188 per model. The English IMD covers England only; all three cities are in England.
- **2.4:** White British customers, Block A, mean IMD decile, from `~/research/llm-steering-uk-housing-market/output/pilot_s1/baseline.csv`. Middle vs working class: Claude 5.15 vs 4.08 (gap 1.07), GPT-6 Astra 4.56 vs 4.04 (0.52). With the estate-agent prompt: 1.10 and 0.73. These are raw cell means. GPT-6 Astra's middle-class means are not in the 9 Nov draft, which reports upper vs working class (Table 1: 1.43 and 1.40). Ethnic gaps of 0.1 to 0.6 of a decile: Table 1.
- **2.5:** Lindenthal (2026), section 5 and Table 1: rent-first advice for recent migrants vs British customers of the same heritage, 45 points (Claude) and 20 points (GPT-6 Astra). The rent-first measure is noisy: 80–87% of its variance lies between repeats of the same prompt.
- **2.6:** Lindenthal (2026), section 5 and Table 2. Asked why the message was sent, Claude names a test as the most likely reason for 99–100% of single prompts; GPT-6 Astra for 0% (7% with the estate-agent prompt). The quote is a probe answer in `~/research/llm-steering-uk-housing-market/data/runs/probe/raw_anthropic.jsonl`; details in `note_audit_awareness.md`. Reasoning summaries (run `suspicion1`): 4 of 440 were coded as suspecting a test, and on reading none of them does, so "rarely" is generous. Fairness considerations appear in 25–33% of summaries for White British customers and 65–88% for Pakistani or Nigerian background customers. Lukk (2026), section on results (`related-literature/Lukk_2026_arXiv_FairFund_Bench_Distributive_Bias.pdf`): the 3–4 times figure is for dollar allocations across several requests shown together ($121 vs $36 for race), not for every task.
- **2.7:** Samad et al. (2026), abstract and section on city characteristics (`related-literature/Samad_2026_AIES_Geography_Algorithmic_Judgment_Racial_Steering_Housing.pdf`). Volkswagen: EPA notice of violation, 18 Sep 2015, p. 3 (`related-literature/vw/EPA_2015-09-18_VW_notice-of-violation.pdf`).

### 3. AI and the research agenda

- **3.1:** Kobak et al. (2025), *Science Advances* (`related-literature/Kobak_2025_SciAdv_LLM_Excess_Vocabulary_Biomedical.pdf`). The real estate replication is in Lindenthal, Kalikman & Ruf (2026), section 5.1. Background for questions on AI as a research assistant: Schwartz, Andrews & Shapiro (2026), NBER WP 35782 (reruns 4,452 economics replication packages); Muravyev (2026), SSRN 7439099 (rebuilds 1,328 finance results; 75% hold in sample, 42% out of sample). Both are in `related-literature/`.
- **3.2:** Lindenthal, Kalikman & Ruf (2026), draft of 9 Oct 2026, sections 5.2, 6.1–6.2 and 6.5, Tables 1 and 5 (`related-literature/Lindenthal-Kalikman-Ruf_2026_draft_How_AI_Shapes_Research_Agenda_REFE.pdf`). The cited papers are model recollections, not a verified bibliography. Main results use one model snapshot (`claude-sonnet-4-6`). Slide figures are copied from `~/research/ree-research-themes/latex/figures/` to `imgs/`: `kobak_openalex.png`, `umap_fig1a.png`, `ideas_umap_a_bare_unconstrained.png`, `ideas_umap_crossmodel_comparison.png`, `condA_citations_map.png`.
- **3.3:** Lindenthal, Kalikman & Ruf (2026), conclusion and appendix on citation growth in AI-favoured clusters.
