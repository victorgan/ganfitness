# Repository Critique

## Overall Assessment

This is a well-organized, opinionated, and genuinely useful personal fitness and lifestyle guide. The writing is direct, the structure is consistent across files, and the "base program first, reasoning second" pattern is a good design choice. The content is generally evidence-informed and avoids the common pitfalls of fitness writing (vague advice, no prioritization, hype). That said, there are meaningful issues across the files — some structural, some factual, some editorial.

---

## Critique by File

### `index.md` (root)

The landing page is 12 lines linking to 8 sections. It serves its purpose as a table of contents but is extremely minimal — it provides no context about what the site is, who it's for, or how the guides relate to each other. A visitor arriving at `gan.fitness` sees a list of links with no framing. A single paragraph explaining the project's philosophy (prescriptive base programs + educational guides, personalized for a specific body type, evidence-based) would make the landing page functional instead of just navigational. The ordering of sections (lift, run, nutrition, sleep, mental, social, time, connective tissue) is reasonable but the logic behind it is unstated.

### `lift/index.md` (956 lines)

**Strengths:** The most detailed file in the repo. The base program is concrete and actionable — exercise selection, set/rep schemes, rest periods, tempo prescriptions, and progression rules are all specified. The muscle anatomy section is unusually thorough for a training document and provides genuine educational value. The "removed" annotations (e.g., "[Leg extensions as a primary quad exercise] removed") are an effective way to preempt common questions.

**Issues:**
- **Program design assumes intermediate+.** A 4-day upper/lower split with 6 training days total (4 lifting + 2 conditioning) is a significant commitment. There is no deload protocol in the base program itself — deloading is mentioned in the comprehensive guide but should be in the base program since it's a prescribed action, not optional reasoning.
- **Exercise links are fragile.** The document uses anchor links to exercises (e.g., `#barbell-back-squat`, `#standing-calf-raises`) but there's no guarantee these anchors exist or will survive edits. A single renamed heading breaks multiple cross-references. This is a maintenance risk across the entire site.
- **Volume prescription is vague in places.** The base program prescribes sets and reps but some exercises say things like "2-3 sets" without guidance on when to use 2 vs 3. For a program that says "do exactly this," ambiguity undermines the premise.
- **No warm-up protocol.** The base program specifies working sets but does not prescribe a warm-up. For heavy compound lifts (squats, bench, deadlifts), warm-up sets are not optional — they're a safety requirement.
- **Conditioning days are underdeveloped.** Conditioning A and B are described briefly compared to the lifting days. For a program that integrates running and lifting, the conditioning prescription should be more specific about how it interacts with running volume.

### `run/index.md` (391 lines)

**Strengths:** Good integration with the lifting program. The 80/20 intensity distribution is well-supported by research. The pace zone tables are concrete and useful. The injury risk section appropriately references connective tissue adaptation timelines.

**Issues:**
- **Overly personalized for general utility.** The paces are calibrated for a 1:39 half marathoner at 160 lbs. This makes the document essentially useless for anyone else without significant recalculation. If the intent is a personal reference, this is fine. If the intent is a shareable guide, the pace tables need a "calculate your zones" method, not just one person's numbers.
- **Missing periodization plan.** The document describes workout types (easy, tempo, interval, long) but doesn't prescribe a periodization structure — how these workouts are organized across weeks and months leading to a race. The lifting doc has a weekly split; the running doc has workout descriptions but no analogous weekly template in the base program.
- **Recovery compatibility section is referenced by other docs but could be more specific.** Other files (connective tissue, lift) point to `run/#recovery-compatibility`, but the actual guidance there is somewhat generic. The specific question — "I did heavy squats today, can I run tomorrow?" — deserves a concrete answer matrix.
- **No mention of environmental factors.** Heat, cold, altitude, and surface affect running performance and injury risk. For a document that covers injury risk in detail, the absence of environmental guidance is notable.

### `nutrition/index.md` (610 lines)

**Strengths:** The macro targets are specific and well-reasoned. The sample day with full macro breakdowns is immediately actionable. The meal prep section is practical. The distinction between cutting, maintaining, and bulking phases is clear.

**Issues:**
- **Hydration is underaddressed.** For someone running 40-55 miles/week and lifting 4 days/week, hydration is a significant performance and recovery factor. The document mentions water briefly but doesn't prescribe intake targets, electrolyte considerations, or guidance on how to assess hydration status.
- **Supplement section is cautious to the point of omission.** Creatine, for example, is the most well-researched sports supplement with a large evidence base for both strength and potentially connective tissue health, but it's either absent or barely mentioned. The connective tissue doc recommends gelatin + vitamin C, but the nutrition doc doesn't integrate this into the meal plan or supplement protocol.
- **Meal timing around training is vague.** For someone doing morning deep work then afternoon/evening training (per the time doc), the question of when and what to eat before/after training is important. The document mentions timing broadly but doesn't reconcile with the specific daily schedule from the time guide.
- **No guidance on eating out or travel.** The meal prep approach assumes you're always cooking at home. Most people eat out 2-4 times per week, and the document doesn't address how to maintain the nutrition framework when you can't control ingredients.
- **Food reference lists are useful but lack portion sizes.** Saying "chicken breast" is a protein source is less useful than saying "6 oz chicken breast = ~42g protein, 0g carb, 3g fat." Some entries have this; others don't.

### `sleep/index.md` (501 lines)

**Strengths:** The base program is concrete — 10 PM bedtime, 6 AM wake, 90-minute wind-down protocol. The sleep disruptors section is comprehensive and evidence-based. The connection between sleep and training recovery is well-articulated.

**Issues:**
- **The 10 PM - 6 AM schedule conflicts with the time doc.** The time doc says "9:30 PM in bed" and "6:00 AM wake." The sleep doc says "10 PM bedtime." These should be reconciled. A 30-minute discrepancy undermines the "do exactly this" framing.
- **No guidance for shift workers or non-standard schedules.** The document acknowledges that the schedule can be shifted but doesn't provide guidance for people with irregular hours, which is a significant population.
- **Napping guidance is absent or minimal.** For an athlete training twice daily (or lifting + running), strategic napping is a legitimate recovery tool. The document should address whether, when, and how long to nap.
- **Sleep tracking recommendations could be more specific.** The doc mentions tracking but doesn't recommend specific approaches or warn about the anxiety that sleep tracking can create (orthosomnia).

### `mental/index.md` (596 lines)

**Strengths:** The daily maintenance routine (morning journal, evening check-in) is concrete and low-friction. The cognitive distortions section is genuinely educational and correctly describes each pattern. The professional help criteria are clear and appropriately serious. The crisis resources section is essential.

**Issues:**
- **The document conflates mental health maintenance with mental health treatment.** The base program is a maintenance routine for someone who is basically well. The comprehensive guide includes cognitive distortions and emotional regulation techniques that border on therapeutic interventions. There should be a clearer line between "daily hygiene" and "if you're struggling, here's what helps" — and stronger caveats that the latter is not a substitute for professional support.
- **Meditation guidance is generic.** "Sit quietly and focus on your breath" is the entirety of many meditation instructions. The doc could benefit from specifying a method (e.g., body scan, noting, open awareness) or recommending a guided resource for someone starting from zero.
- **No mention of screen time / digital mental health.** Given that the time doc and sleep doc both address screen management, the mental health doc should address the relationship between social media, news consumption, and mental health — it's one of the strongest modifiable risk factors.
- **Exercise as mental health intervention is underemphasized.** The doc cross-references the lifting program but doesn't highlight the strong evidence for exercise as a first-line intervention for mild-to-moderate depression and anxiety. This is arguably the single most important cross-reference in the entire site.

### `social/index.md` (466 lines)

**Strengths:** The relationship tier system is clear and realistic. The "what counts / what doesn't count" distinction for maintenance is sharp and useful. The initiation section acknowledges the structural difficulty of adult friendship with unusual honesty. The vulnerability graduation framework (Levels 1-4) is well-designed.

**Issues:**
- **The document assumes a specific personality type.** The entire framing is for someone who is willing but neglectful — someone who would maintain friendships if only they had a system. For someone with social anxiety, avoidant attachment, or neurodivergent social processing, the prescriptions ("text 2 friends per week") may feel overwhelming rather than minimal. The Individual History section at the end addresses this but should be referenced much earlier.
- **No guidance on romantic relationships.** The document mentions "partner" in several places but doesn't address the unique maintenance and repair dynamics of romantic partnerships. This is a notable gap given that partner relationship quality is the single strongest predictor of life satisfaction in most research.
- **The "pruning" section could cause harm without more nuance.** Deciding to end friendships based on a checklist is risky. The criteria ("costs more energy than it provides") could justify dropping someone going through a difficult period. More nuance about distinguishing temporary difficulty from fundamental incompatibility would help.
- **Digital community is not addressed.** Online communities, gaming friends, and virtual social groups are real social connections for many people. The document's implicit hierarchy (in-person > everything else) is defensible but should be stated and defended rather than assumed.

### `time/index.md` (500 lines)

**Strengths:** The base program is the most immediately actionable of all the guides. The weekly planning ritual is specific down to the minute allocation per step. The sample week integrates lifting, running, work, social, and sleep into a single view — this is the document that ties the whole system together. The "saying no" section is excellent.

**Issues:**
- **The sample week is extremely full.** Every hour from 6 AM to 9:30 PM is accounted for. There is almost no unstructured time. The document itself warns against over-scheduling but then presents a schedule with no slack. For someone who already feels overwhelmed, this could be counterproductive.
- **The schedule assumes remote work.** The commute note is a parenthetical rather than an alternative schedule. For someone with a 45-60 minute commute, the entire daily structure breaks down and the document doesn't provide a rebuilt version.
- **Saturday stacking of Lower B + Conditioning B is aggressive.** The document proposes doing both sessions on Saturday morning starting at 6:30. Depending on the intensity of Lower B, this could be 90+ minutes of continuous training. The lifting doc should be cross-referenced for whether this is advisable from a recovery standpoint.
- **The protection rules conflict slightly with other docs.** "No email before 8:30 AM" is a protection rule here, but someone following the schedule is in a deep work block from 6:30-8:30 anyway, making the rule redundant. The 9:30 PM bedtime vs 10 PM in the sleep doc is another discrepancy noted above.

### `connective-tissue/index.md` (341 lines)

**Strengths:** This is the most technically rigorous document in the repo. The adaptation timeline table is the single most valuable reference in the entire site. The mismatch problem section explains the root cause of most overuse injuries more clearly than most textbooks. The integration with both the lifting and running programs is thorough. The gelatin + vitamin C protocol is correctly cited.

**Issues:**
- **No base program.** Every other guide has a "do exactly this" base program. This guide has "Recommended Practices" which is structured more like a reference than a prescription. A base program should specify: what exercises, how many sets/reps, how often, and when in the week to do them relative to lifting and running. As written, someone would need to synthesize the information themselves, which contradicts the site's design philosophy.
- **Recommended practices are not integrated into the weekly schedule.** The time doc's sample week doesn't show when eccentric heel drops, Spanish squats, or mobility work happen. These are described as "non-negotiable maintenance" but have no place in the schedule. They need to be added to the sample week or the lifting base program.
- **The document is dense.** At 341 lines, it's the shortest guide but the most information-dense. The physiology sections (tendon structure, bone remodeling, mechanotransduction) are excellent educational content but may overwhelm someone looking for "what do I do." Consider restructuring so the recommended practices section is more prominent and self-contained.
- **Some force calculations are presented without sources.** "6-8x body weight through the Achilles tendon during push-off" and "every stride generates approximately 2.5x body weight" are specific claims that should be cited or at least noted as approximations. The precision implies certainty that the underlying research doesn't fully support (these values vary significantly with speed, surface, and footwear).

### `CNAME`, `.gitattributes`, `robots.txt`

- `robots.txt` disallows all crawlers (`Disallow: /`), and each page also has `<meta name="robots" content="noindex, nofollow">`. This is belt-and-suspenders, which is fine, but it means the site is intentionally invisible to search engines. If this is a personal reference, that makes sense. If you ever want it discoverable, both need to change.
- `CNAME` correctly points to `gan.fitness`.
- `.gitattributes` handles line endings. No issues.

---

## Cross-Cutting Issues

1. **Cross-reference fragility.** The site relies heavily on internal links (between files and within files). These are all manual Markdown links to anchors. A renamed heading in any file silently breaks links in other files. There's no automated link checking. This is the single biggest maintenance risk.

2. **Inconsistent sleep/wake times.** The sleep doc says 10 PM bedtime; the time doc says 9:30 PM. These are both in base programs that say "do exactly this." One of them is wrong.

3. **Connective tissue work is nowhere in the schedule.** The connective tissue doc prescribes daily eccentric heel drops, Spanish squats, mobility work — probably 20-30 minutes per day. The sample week in the time doc has no slot for this. Either the connective tissue work needs to be folded into lifting sessions (as warm-up or accessory work) or the schedule needs updating.

4. **The site is hyper-personalized but occasionally speaks generically.** Most sections are written for a 5'8", 160 lb runner-lifter with a long torso and large calves. But some sections (social, mental, time) speak in general terms to "you." This creates a tonal inconsistency — is this a personal reference manual or a guide for others? Committing to one framing would improve coherence.

5. **No change log discipline.** Several files have change logs with only one or two entries, all from the same date (2026-02-08). This is a good practice to start but needs to be maintained as the documents evolve.

6. **No warm-up or cool-down protocols anywhere.** The lifting doc doesn't prescribe warm-ups. The running doc doesn't prescribe warm-ups or cool-downs. The connective tissue doc's mobility work would be a natural warm-up/cool-down, but this connection is never made explicit.

7. **Nutrition-training timing gap.** The nutrition doc prescribes meal timing. The time doc prescribes a daily schedule. The lifting doc prescribes training times. But nowhere is the question "what do I eat at what time on a training day vs. a rest day" answered in a single, integrated view. A worked example ("Tuesday: Lower A day — here's the full schedule including meals") would fill this gap.
