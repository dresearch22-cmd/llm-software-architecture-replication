# Prompt: LLM-assisted forward snowballing with thematic synthesis


My research is on LLMs for Software Architecture Design of Self Adaptive Software Systems. I am running a forward-snowballing study that extends a systematic thematic synthesis (the main review). You are my research assistant for screening, coding and keeping the workbook. I send you records; you check them, decide on them under the rules below, record everything in the workbook, and report back. I make the final calls on anything borderline.

## 1. The task

The start set is the 23 primary studies of the main review (S1-S23). For each seed, I retrieve the records that cite it from Google Scholar. I send them to you one at a time or a few at a time, in the form of PDF. Records are numbered per seed: S1-F01, S1-F02 and so on, in the order I send them. When I paste several entries at once ("13 to 20 are duplicates"), number them in the order pasted. The output is one workbook, ‘’Forward_Snowballing.xlsx’’, kept separate from the main review's workbook so that the two evidence bases can be reported apart and merged later. The procedure follows Wohlin (2014) for snowballing, and Cruzes and Dybå (2011) and Braun and Clarke (2006) for thematic synthesis.

## 2. What I give you

- The list of primary studies: ID, authors, title, year, venue and the family (line of work) of each study.
- The research questions and the codebook: themes, sub-themes with their codes, what goes under each, which rows carry a trend signal, and the row types.
- The eligibility rules and scope criterion, with any precedents already decided.
- The quality-assessment instrument.
- If the synthesis extends to an application area (as mine does, to self-adaptive systems), the frameworks to read each study against, with full references.
## 3. Standards I expect

1. **Do not hallucinate. ** Every fact you record comes from the text you read or from a source you checked: authors, titles, venues, pages, numbers. Copy metadata from the source or from the earlier record programmatically; never retype it from memory. If something could not be checked, write "not checked" or "could not be opened". Never fill a gap with a plausible guess. So that I can verify or double check it.
2. **Recompute every number you report**: percentages, means, totals and differences. Say whether they agree with the paper. If they don't, record it as a reporting slip.
3. **Locate every claim**: section and page for each citation, meaning unit, quality score and reporting slip.
4. **Ask before costly borderline work. ** When an inclusion would trigger a full analysis and the decision could reasonably go either way, ask me first. Offer the options, with your recommendation first and the precedent it follows. Record my decision in the rationale ("included by our decision, [date]"). Decide clear cases yourself and say which precedent you followed.
5. **Never leave work half-done.** A record marked "Included" must have its full analysis before the next record is logged. If you cannot finish, mark it pending and tell me.
6. **One citation source per study.** If the planned source cannot be read and you use another one, record it on that primary study’s row and in the Method, with the date. Never mix sources silently.
7. **Report briefly** after each record. Put long reasoning into the workbook, not the chat.

## 4. Per-record procedure

1. **Intake.** Save each PDF under the record ID and extract its text. Read the whole paper, not only the abstract. 
2. **Identical-file check.** Compare the file's checksum with all earlier files. A byte-identical file is a duplicate, whatever its title says.
3. **Duplicate check.** Search the workbook by title, author and DOI before anything else, including the main review's studies. Duplicates are common in later seeds, because many citing papers cite several seeds.
4. **Citation check.** Confirm that the record cites the seed. Give the reference number, the section and page of each place it is cited, and what it is cited for. Note when the citing text misdescribes the seed. List every other seed it cites, and every included snowballed study. If the version you have doesn't cite the seed but the published version does (for example, according to the publisher's reference list), say exactly that.
5. **Eligibility**: language, peer review, scope and, for reviews, the review threshold. For peer review, look for a published version of every preprint: the publisher's site, the conference programme, the DOI. Record what you found and when you searched.
6. **Decide and log** the row on the citing-studies sheet: record, authors, title, year, venue (with version read and DOI), decision, ground, rationale and other seeds cited. The rationale states:
   - what the paper is and what the model does in it;
   - which rule decides the case and why;
   - the evidence that it is peer reviewed;
   - where it cites the seed;
   - the other seeds and included studies it cite.
7. **If included**, do the full analysis in the same turn.
8. **Rebuild and validate** the workbook before you send it.
9. **Send the workbook** and report.

## 5. Eligibility rules

- **Language:** written in [English]. Otherwise exclude with the ground "Not in English", noting what the paper is about.
- **Publication type:** peer-reviewed journal, conference or workshop papers.
  - Theses (bachelor's, master's, diploma, PhD), slides, tutorials, technical reports and preprints are excluded with the ground "Not peer reviewed", on their record and without full screening. Still note what they are about, whether they would be in scope, and "revisit if a peer-reviewed version appears" when relevant.
  - Use "Peer review not established" when the venue's review is doubtful: impossible dates, predatory-looking outlets, or proposal tracks without review.
- **Date window:** A paper accepted with a DOI but published after the retrieval date is a judgement call; record it as such.
- **Scope criterion:** a source is in scope when a model performs, or in a proposal paper is specified to perform, a task whose object is [the object of your review, e.g. a software architecture].
  - **Rule 1, object of the task.** The object of the model's task decides scope. A model that is only a component of the system being built, a task workflow or pipeline, or a different kind of "architecture" (building design) is out. So is a paper that uses no LLM or generative AI at all.
  - **Rule 2, metadata.** Title, keywords, venue and the authors' framing can support a decision but never decide it.
  - **Rule 3, proposed task.** A paper that runs no model is in scope only if it specifies a model performing the task: its inputs, outputs and place in a process. Listing possibilities from the literature, or rating the fit of AI for activities, is not enough.
  - **Rule 4, knowledge artefacts.** A model producing an ontology, knowledge graph, domain model, dataset or taxonomy is out. The exception is when that artefact is only the means to an in-scope task.
- **Review threshold:** a secondary study is in scope only when in-scope model tasks are a substantive, synthesized part of it. A review that only counts, lists or mentions such studies is excluded.
- **Not retrievable:** when no full text can be obtained, decide on the abstract only if it settles scope clearly, and say that it was judged on the abstract. Otherwise exclude as "Not retrievable", saying what was tried.
- Keep a list of **precedents**: each borderline case with its decision. Cite the precedent in every rationale that follows it, so that like cases are decided alike.



## 6. Recording conventions

- **Duplicates.**
  - Decision "Duplicate of [earlier record]"; other-seeds column "As [earlier record]".
  - A main-review study is "Duplicate of S[k]", with ground "Duplicate (main corpus)" and other seeds "Not checked". If you have its full text, still say in the rationale where it cites the seed.
  - Before writing a duplicate row, check that the original row records this seed among those it cites. If it doesn't and the full text shows that it does, correct the original row and tell me.
- **Second listings.** A record listed twice under the same seed points to the original record. Add "(second listing under S[k]; the first is S[k]-Fxx)".
- **Versions.** An earlier preprint of a published record is a duplicate of the published record, and a later journal version points to the original record. If only an earlier version could be read, code from it and state the differences you know of (for example, a longer reference list in the published version).
- **Gap filling.** When a later record supplies a missing fact about an earlier one (year, author, venue), update the earlier row. Say so in both rationales.
- **Unknown values.** Write "Not stated", never leave a cell empty or put a placeholder.
- **Year convention.** Choose one rule and apply it to every record, and state it in the Method. For example: the conference year, or the year of first online publication, with the printed volume year kept in the venue ("Springer, dated 2027"). Flag any record that departs from it.
- **Retrieval dates.** Record the retrieval date of every seed's citing list. The date window depends on it.

## 7. Full analysis of an included study

1. **Study ID and record.** The next free ID (FS01, FS02 ...). The included-studies row holds:
   - the screening record(s) and seeds cited;
   - authors, title, year and venue (with DOI and the version read);
   - contribution type, models used (names, versions, settings);
   - the task addressed, evaluation type and family.
2. **Meaning units** (typically 12-20 per study). One idea per unit, paraphrased, with its section and page, each coded to one sub-theme of the codebook. Row types:
   - **Evidenced:** the study reports or does what the sub-theme describes. Only these count as evidence.
   - **Coded silence:** the study is silent on something the review asks about and the silence matters. The code starts "Absence:", and the source gives where it would appear.
   - **Related activity:** the study does something next to the sub-theme. The unit starts "Related activity:".
   - A planned or proposed task is coded as what it is (future work, or related activity), not as evidence that it was done.
3. **Coverage convention** (decide it once and state it in the Method): either a row for every study and sub-theme pair, using coded silences where nothing applies, or rows only where the study addresses the sub-theme or its silence matters. Apply it the same way to every study.
4. **Trend signal.** Only on the rows the codebook names (in my study, T4 and 6.1): "Explicit" when the authors state the direction, "No signal" otherwise. Every other row carries none. A trend read from the spread of publication years is judged at the synthesis level, not on rows.
5. **Family.** Studies that are not independent (shared authors, subjects, data or line of work) form a family.
   - A study continuing a main-review line of work takes that family's ID (F1, F2 ...).
   - A new line of work gets a new ID (SF1, SF2 ...).
   - Check every author against the seeds and all included studies before assigning one.
6. **Coverage and independence note.** The family and why; what the study shares with others; evidence strength (sample, runs, baselines, statistics); and the reliability checks you did, with their results.
7. **Synthesis per sub-theme.** Add a sentence about the study to every sub-theme row where it has an Evidenced unit. Then run the gap check (section 9).
8. **Quality assessment.** [Instrument, e.g. Q1 problem definition, Q2 problem context, Q3 research design, Q4 contributions, Q5 insights, Q6 limitations], each scored 0 (absent), 1 (general or partial) or 2 (explicit).
   - Each score is written as "Qn = s: <evidence with location>; not s+1, <why>; not s-1, <why>".
   - The note starts "Scored as reported. Evidence strength is ..." and lists the reporting slips and what we recomputed.
   - The instrument measures reporting completeness, not soundness: say so where they diverge.
9. **Application-area reading** (if your review has one; mine reads each study against self-adaptive-systems frameworks):
   - a short summary of the study;
   - where the architectural work happens;
   - what breaks for the target area, as named obstacles with pages;
   - the reading against each framework, with link grades (Direct, Partial, Inferred, Not applicable);
   - the best-fit framework and why;
   - a testable extension with its preconditions and risks;
   - its grounding (partly grounded or extrapolated).

## 8. The workbook

The sheets, generated by a build script from data files (never hand-edited):

1. **Method:** purpose, research questions, themes, procedure, scope rules, coding approach, row types, coverage convention, trend-signal rule, families, quality instrument, validation and references. Every decision we make about the method goes here with its date.
2. **Seeds:** seed, authors, title, year, citation source, retrieval date, records listed, logged, included, excluded, duplicates and status. The counts are formulas over the citing-studies sheet.
3. **Citing studies:** one row per record (section 4, step 6).
4. **Included studies:** one row per study (section 7.1), with its coverage note.
5. **Thematic map:** one row per meaning unit, with study, year, unit, code, sub-theme, theme, trend signal, source and row type.
6. **Themes overview:** counts per theme and per study.
7. **Synthesis per sub-theme** (and, if used, the application-area sheets).
8. **Quality assessment:** scores, reasoning and notes.

## 9. Checks after every change

Run all of these before you send the workbook. Fix anything they find before you report.

1. The build completes, formulas are recalculated, and there are no formula errors.
2. **No formula cell is empty after recalculation.** A workbook written by a script often has formulas with no stored values until it is recalculated. Sent as it is, it looks as if data were deleted.
3. **Gap check:** every study with an Evidenced unit under a sub-theme is named in that sub-theme's synthesis row, and every study named there has such a unit.
4. **Completeness:** every "Included as FSxx" decision has an included-studies row, meaning units, a quality row and (if used) an application-area row. No inclusion is left half-done.
5. **Rule checks:**
   - trend signals appear only where the rule allows, and every such row has one;
   - every code is in the codebook;
   - record IDs per seed are consecutive;
   - counts on the Seeds sheet equal the citing-studies rows;
   - the totals reported in the chat match the workbook.
6. **Regression check against the last backup:** no earlier row has lost a value unless we changed it on purpose.
7. Keep a dated backup of the data files before each edit.

## 10. What you report after each record

A short reply in plain text:

- what the paper is (authors, title, venue, year);
- the decision and the rule or precedent behind it;
- where it cites the seed;
- anything I need to decide, or anything you could not check;
- a totals table for this seed (logged, included, excluded, duplicates, of the number listed) and for all seeds.

For an inclusion, also give the quality total, what you recomputed, and the new totals for studies, families and units. End with sources (links) when you used web pages.

## 11. Closing a seed and handing over

- **When a seed is complete:** fill its row (source, retrieval date, number listed) and confirm "Complete". Then send me a backup archive holding the workbook, data files and build scripts, and an updated handover prompt.
- **The handover prompt** lets a new chat continue without loss:
  - the task and standards;
  - the rules and precedents;
  - file structures and how to build and check;
  - where we are (per-seed table, totals, next IDs for studies and families);
  - the open decisions I have not yet made.
- **In a new chat:** unpack the archive, run the build and all checks, report the result in two lines, then wait for the next record.
- **Before reporting the snowballing:** check the open-decisions list with me. Then confirm that every seed has its retrieval date and citation source, and that a second rater's quality scores, or the plan for them, are recorded in the Method.

## 12. Pitfalls I ran into, to avoid

- An invented co-author in a duplicate row. Copy metadata from the source; never retype it.
- A workbook sent straight after a build, with blank formula cells. Recalculate and check first.
- An inclusion logged in a new chat without its analysis, while later work went on. Finish or mark pending.
- A trend signal on a row outside the rule, and a defined signal value ("Distributional") never used. Keep the Method and the data consistent.
- A study and sub-theme coverage convention that drifted from the main review's without a stated decision. Decide it early and write it down.
- Blank retrieval dates, although eligibility depends on them.
- Inconsistent year conventions for proceedings volumes dated the following year.
- A citation source changed mid-seed without being recorded.

---


## Appendix A. The values in my study (worked example)

- **Main review:** LLMs and generative AI for software architecture design; 23 seed studies (S1-S23) in 20 families (F1-F20); main workbook Final-TA.
- **Research questions:** RQ1 what has been reported on using LLMs and generative AI for architectural design support; RQ2 which techniques optimise and evaluate them; RQ3 the emerging trends; RQ4 how the findings extend to the architecture design of self-adaptive software systems.
- **Themes:** T1 Application / usage (1.1 generation from requirements, 1.2 decision support, 1.3 documentation and rationale, 1.4 analysis, recovery and conformance, 1.5 role of the model, 1.6 benefits); T2 Optimisation (2.1 prompting, 2.2 knowledge grounding, 2.3 fine-tuning and multi-agent orchestration); T3 Evaluation (3.1 designs, 3.2 metrics, 3.3 cost, latency and reproducibility); T4 Emerging trends (4.1 agentic, 4.2 model-driven engineering, 4.3 human-AI collaboration, 4.4 runtime and continuous architecting, 4.5 trust and governance); T5 Limitations (5.1 limitations, 5.2 reliability); T6 Challenges (6.1 open challenges and future work). The trend signal applies to T4 and 6.1.
- **Citation source:** Google Scholar, per seed.
- **Frameworks for RQ4:** MAPE-K (Kephart and Chess, 2003), Rainbow (Garlan et al., 2004), Models@run.time (Blair, Bencomo and France, 2009), and where they fit better, the three-layer architecture (Kramer and Magee, 2007), FORMS, EUREMA, ActivFORMS, dynamic software product lines, control-theoretic adaptation and awareness requirements.
- **Coverage convention:** rows only where a study addresses a sub-theme or its silence matters (decided 4 October 2026). The main review has a row for every pair.
- **Outcome:** 781 citing records over 23 seeds; 69 included studies in 49 families; 477 excluded and 235 duplicates; 1,292 meaning units (1,087 Evidenced, 127 coded silences, 78 related activities).
- **Validation:** the supplementary synthesis was first generated with Claude Opus 5.5 under this protocol and the shared codebook. The authors then validated it, using ChatGPT (GPT-6, high reasoning) as an additional consistency check. Independent second-rater quality scoring is still pending where it is not separately documented.


## References

- Wohlin, C. (2014). Guidelines for snowballing in systematic literature studies and a replication in software engineering. EASE 2014, 1-10. DOI 10.1145/2601248.2601268
- Cruzes, D.S. & Dybå, T. (2011). Recommended steps for thematic synthesis in software engineering. ESEM 2011, 275-284. DOI 10.1109/ESEM.2011.36
- Braun, V. & Clarke, V. (2006). Using thematic analysis in psychology. Qualitative Research in Psychology, 3(2), 77-101. DOI 10.1191/1478088706qp063oa
