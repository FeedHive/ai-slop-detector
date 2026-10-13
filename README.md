# AI Slop Detector

129 patterns that make writing read like AI slop, in 9 categories. Each pattern has a short explanation, a bad example and a plain rewrite.

Give the list to your AI before it writes, or check a draft against it afterwards. To check a draft in your browser, paste it into the free [AI Slop Detector](https://www.feedhive.com/tools/ai-slop-detector).

The list doesn't try to tell whether a person or an AI wrote a text. People write these patterns too, and a model can be told to avoid them. A single pattern is normal in human writing; several in one paragraph is what makes a text read as slop.

## Use it with your AI

**Claude Code, Codex and other agents.** Give the agent this repository and ask it to install the skill:

```text
Install the AI Slop Detector skill from https://github.com/FeedHive/ai-slop-detector
```

Or install it yourself for Claude Code:

```sh
git clone https://github.com/FeedHive/ai-slop-detector.git
cp -r ai-slop-detector/skills/ai-slop-detector ~/.claude/skills/
```

**ChatGPT, Claude and other chat apps.** Paste this README into the chat and ask it to avoid every pattern in what it writes next. To check a draft, paste the README and the draft and ask for every pattern it finds, with the line it found it in.

**Your own tools.** [`patterns.json`](patterns.json) has the full list as structured data. Edit it and run `node scripts/build.mjs` to regenerate this README and the skill.

## Categories

| Category | Patterns |
|---|---|
| [Vocabulary](#vocabulary) | 21 |
| [Stock phrases](#stock-phrases) | 19 |
| [Sentence patterns](#sentence-patterns) | 24 |
| [Structure and rhythm](#structure-and-rhythm) | 12 |
| [Imagery and metaphor](#imagery-and-metaphor) | 6 |
| [Substance](#substance) | 12 |
| [Formatting and punctuation](#formatting-and-punctuation) | 10 |
| [Chatbot residue](#chatbot-residue) | 10 |
| [Social media and LinkedIn](#social-media-and-linkedin) | 15 |

<a id="vocabulary"></a>

## Vocabulary

Words that show up far more often in AI output than in human writing. One is a coincidence; three in a paragraph is a pattern.

<a id="v-01-delve-and-friends"></a>

### V-01 Delve and friends

delve, dive into, deep dive, unpack, explore (for "discuss").

Bad: "Let's delve into the data."  
Better: "Here is what the data shows."

<a id="v-02-tapestry-words"></a>

### V-02 Tapestry words

tapestry, landscape, realm, sphere, ecosystem, fabric (used abstractly).

Bad: "the ever-evolving landscape of marketing."  
Better: "marketing in 2026" or name the actual change.

<a id="v-03-testament-and-beacon"></a>

### V-03 Testament and beacon

testament to, beacon of, embodiment of, hallmark of.

Bad: "The launch is a testament to the team's dedication."  
Better: "The team shipped it in six weeks."

<a id="v-04-pivotal-and-crucial"></a>

### V-04 Pivotal and crucial

pivotal, crucial, vital, paramount, critical (as decoration).

Bad: "plays a pivotal role in growth."  
Better: "drives 40% of signups."

<a id="v-05-showcase-verbs"></a>

### V-05 Showcase verbs

showcase, highlight, underscore, emphasize, spotlight (as commentary verbs).

Bad: "The results underscore the importance of testing."  
Better: "Testing caught three bugs before launch."

<a id="v-06-foster-and-cultivate"></a>

### V-06 Foster and cultivate

foster, cultivate, nurture (applied to abstract things).

Bad: "fostering a culture of innovation."  
Better: Say what the team actually does.

<a id="v-07-leverage-and-utilize"></a>

### V-07 Leverage and utilize

leverage, utilize, harness, capitalize on.

Bad: "Leverage AI to streamline your workflow."  
Better: "Use AI to draft the weekly report."

<a id="v-08-elevate-and-enhance"></a>

### V-08 Elevate and enhance

elevate, enhance, empower, supercharge, unlock, amplify.

Bad: "Elevate your content strategy."  
Better: Name the result: "Post three times a week without writing on weekends."

<a id="v-09-seamless-and-robust"></a>

### V-09 Seamless and robust

seamless, robust, cutting-edge, state-of-the-art, best-in-class, world-class.

Bad: "a seamless, robust solution."  
Better: "it syncs in under a second and hasn't gone down this year."

<a id="v-10-intricate-and-multifaceted"></a>

### V-10 Intricate and multifaceted

intricate, multifaceted, nuanced, complex (as filler).

Bad: "the intricate interplay of factors."  
Better: Name two of the factors.

<a id="v-11-meticulous"></a>

### V-11 Meticulous

meticulous, meticulously, painstakingly, carefully crafted.

Bad: "meticulously crafted templates."  
Better: "templates tested on 200 posts."

<a id="v-12-vibrant-and-rich"></a>

### V-12 Vibrant and rich

vibrant, rich, bustling, thriving, dynamic.

Bad: "a vibrant community of creators."  
Better: "4,000 creators who post weekly."

<a id="v-13-journey-and-embark"></a>

### V-13 Journey and embark

journey, embark, navigate, voyage, path (for ordinary processes).

Bad: "embark on your SEO journey."  
Better: "start with your top ten pages."

<a id="v-14-game-changer"></a>

### V-14 Game changer

game changer, revolutionary, groundbreaking, transformative, paradigm shift.

Bad: "This feature is a game changer."  
Better: Say what changes and for whom.

<a id="v-15-transition-adverbs"></a>

### V-15 Transition adverbs

Additionally, Furthermore, Moreover, Notably, Importantly (opening sentences).

Bad: "Additionally, the tool supports exports."  
Better: "It also exports to CSV."

<a id="v-16-empty-intensifiers"></a>

### V-16 Empty intensifiers

truly, incredibly, deeply, profoundly, remarkably, fundamentally.

Bad: "a truly remarkable result."  
Better: Give the number that makes it remarkable.

<a id="v-17-quietly"></a>

### V-17 Quietly

quietly, silently, subtly (adding drama to plain events).

Bad: "Costs quietly crept up."  
Better: "Costs rose 12% in March."

<a id="v-18-align-and-resonate"></a>

### V-18 Align and resonate

align with, resonate with, speak to, in line with.

Bad: "content that resonates with your audience."  
Better: "posts your audience replies to."

<a id="v-19-key-as-an-adjective"></a>

### V-19 Key as an adjective

key insight, key takeaway, key factor, key role.

Bad: "The key takeaway is consistency."  
Better: "Post on the same days every week."

<a id="v-20-era-words"></a>

### V-20 Era words

in today's fast-paced world, in the digital age, in an era of, now more than ever.

Bad: "In today's fast-paced digital world, content is king."  
Better: Cut it and start with the point.

<a id="v-21-i-d-be-happy-to"></a>

### V-21 I'd be happy to

AI offer openers: I'd be happy to, I'd be delighted to, I'd be thrilled to.

Bad: "I'd be happy to help you with that."  
Better: "Here's what I can do."

<a id="stock-phrases"></a>

## Stock phrases

Ready-made phrases that fill space without adding meaning.

<a id="p-01-worth-noting"></a>

### P-01 Worth noting

it's worth noting, it's important to note, it should be noted.

Bad: "It's worth noting that the API is rate limited."  
Better: "The API allows 100 calls a minute."

<a id="p-02-at-its-core"></a>

### P-02 At its core

at its core, at the end of the day, when all is said and done, ultimately.

Bad: "At its core, marketing is about people."  
Better: Delete, or say something specific about people.

<a id="p-03-when-it-comes-to"></a>

### P-03 When it comes to

when it comes to, in terms of, with regard to, in the world of.

Bad: "When it comes to scheduling, timing matters."  
Better: "Posts at 9am get more reach than posts at 3pm."

<a id="p-04-let-s-dive-in"></a>

### P-04 Let's dive in

let's dive in, let's get started, buckle up, without further ado.

Bad: "Ready? Let's dive in!"  
Better: Start with the first point.

<a id="p-05-plays-a-role"></a>

### P-05 Plays a role

plays a role in, contributes to, is a factor in.

Bad: "Hashtags play a role in reach."  
Better: "Posts with 3 to 5 hashtags reached more people in our test."

<a id="p-06-stands-as"></a>

### P-06 Stands as

stands as, serves as, functions as, acts as (instead of "is").

Bad: "The dashboard serves as a central hub."  
Better: "The dashboard shows every scheduled post."

<a id="p-07-navigate-the-complexities"></a>

### P-07 Navigate the complexities

navigate the complexities of, the ins and outs of, the nuances of.

Bad: "helping you navigate the complexities of SEO."  
Better: "explains how Google picks which page to rank."

<a id="p-08-whether-you-re-x-or-y"></a>

### P-08 Whether you're X or Y

Whether you're a beginner or a pro, from startups to enterprises.

Bad: "Whether you're a solo creator or a global brand, ..."  
Better: Say who it is actually for.

<a id="p-09-look-no-further"></a>

### P-09 Look no further

look no further, you've come to the right place, this is your ultimate guide.

Bad: "Looking for a scheduler? Look no further."  
Better: "FeedHive schedules posts to 10 platforms."

<a id="p-10-unlock-the-power"></a>

### P-10 Unlock the power

unlock the power of, harness the potential of, take it to the next level.

Bad: "Unlock the full potential of your content."  
Better: Say the specific gain.

<a id="p-11-here-s-the-thing"></a>

### P-11 Here's the thing

here's the thing, here's the deal, let me be clear, I'll be honest, I'll be straight with you.

Bad: "Here's the thing: most people quit."  
Better: "Most people quit in month two."

<a id="p-12-the-truth-is"></a>

### P-12 The truth is

the truth is, the reality is, the uncomfortable truth, the hard truth.

Bad: "The hard truth is that SEO takes time."  
Better: "SEO takes about six months to show results."

<a id="p-13-sign-off-clich-s"></a>

### P-13 Sign-off clichés

I hope this helps, happy writing, feel free to reach out, let me know if you have any questions.

Bad: A post or article ending with "Hope this helps!"  
Better: End on the last useful point.

<a id="p-14-summary-openers"></a>

### P-14 Summary openers

In conclusion, In summary, To sum up, Overall, All in all.

Bad: "In conclusion, consistency is key."  
Better: End on the last concrete point; the reader was just there.

<a id="p-15-vague-future"></a>

### P-15 Vague future

the future is bright, the possibilities are endless, only time will tell, the sky's the limit.

Bad: "With AI, the possibilities are endless."  
Better: Name one thing that is now possible.

<a id="p-16-feel-free-to"></a>

### P-16 Feel free to

feel free to reach out, feel free to ask, feel free to share (as filler, not just sign-off).

Bad: "Feel free to reach out if you have any questions."  
Better: "Email me if something breaks."

<a id="p-17-keep-in-mind"></a>

### P-17 Keep in mind

keep in mind, bear in mind, it's worth remembering (hedge phrases AI overuses).

Bad: "Keep in mind that results may vary."  
Better: "Results varied by 12% in our test."

<a id="p-18-needless-to-say"></a>

### P-18 Needless to say

needless to say, it goes without saying, as you may know (filler transitions).

Bad: "Needless to say, consistency is important."  
Better: "Consistency matters."

<a id="p-19-as-a-role"></a>

### P-19 As a [role]

AI self-identification to borrow authority: As a marketing professional, As an expert in.

Bad: "As a marketing professional, I can tell you that..."  
Better: "We tested this on 40 accounts. Here's what happened."

<a id="sentence-patterns"></a>

## Sentence patterns

Constructions that AI reaches for again and again.

<a id="s-01-not-x-but-y"></a>

### S-01 Not X, but Y

"It's not X. It's Y." / "This isn't about X, it's about Y."

Bad: "It's not a tool. It's a teammate."  
Better: Say what it does: "It drafts replies for you to approve."

<a id="s-02-not-just-x-but-also-y"></a>

### S-02 Not just X, but also Y

"It's not just fast, it's also accurate."

Bad: "Not just a scheduler, but a full content engine."  
Better: List what it does.

<a id="s-03-the-question-isn-t-x"></a>

### S-03 The question isn't X

"The question isn't whether, it's when." / "The problem isn't X. The problem is Y."

Bad: "The question isn't if you should use AI. It's how."  
Better: "Here is how we use AI for first drafts."

<a id="s-04-negative-listing"></a>

### S-04 Negative listing

"Not a X. Not a Y. A Z."

Bad: "Not a plan. Not a hope. A system."  
Better: "A system: three posts a week, written on Mondays."

<a id="s-05-rhetorical-q-and-a"></a>

### S-05 Rhetorical Q and A

A question the writer immediately answers.

Bad: "Why does this matter? Because reach is everything."  
Better: "Reach decides how many people see the post."

<a id="s-06-the-obvious-question"></a>

### S-06 The obvious question

"The obvious question is...", "You might be wondering..."

Bad: "You might be wondering how this works."  
Better: Explain how it works.

<a id="s-07-colon-reveal"></a>

### S-07 Colon reveal

A short setup, a colon, then a dramatic reveal.

Bad: "The best part: it's free."  
Better: "It's free."

<a id="s-08-faux-insight"></a>

### S-08 Faux insight

"What nobody tells you", "the part most people miss", "here's what most get wrong".

Bad: "What nobody tells you about growth: distribution beats product."  
Better: "Distribution brought us more users than any feature."

<a id="s-09-this-is-where-it-gets-interesting"></a>

### S-09 This is where it gets interesting

this is where it gets interesting, this changes everything, and that's where things get wild.

Bad: "And this is where it gets interesting."  
Better: State the interesting thing.

<a id="s-10-the-useful-part-is"></a>

### S-10 The useful part is

the useful part, the part where, the best part, the exciting part, the part that stuck with me.

Bad: "The useful part is that it connects to your inbox."  
Better: "It connects to your inbox."

<a id="s-11-x-is-just-y"></a>

### S-11 X is just Y

Calling something "just" a vivid unrelated thing to make a point.

Bad: "Posting without a plan is just gambling with your time."  
Better: "Without a plan you post less and repeat topics."

<a id="s-12-trailing-ing-analysis"></a>

### S-12 Trailing -ing analysis

A sentence ends with an -ing clause that tells you what it means.

Bad: "Sales rose 20%, highlighting the strength of the brand."  
Better: "Sales rose 20%."

<a id="s-13-rule-of-three"></a>

### S-13 Rule of three

Lists of exactly three adjectives or phrases, by reflex.

Bad: "fast, simple, and powerful."  
Better: Keep the one that is true and provable.

<a id="s-14-synonym-cycling"></a>

### S-14 Synonym cycling

Rotating names for the same thing to avoid repetition.

Bad: "The agent drafts. The assistant reviews. The tool publishes."  
Better: "The agent drafts, reviews and publishes."

<a id="s-15-arbitrary-one"></a>

### S-15 Arbitrary "one"

Putting "one" before a noun to sound focused when the number means nothing.

Bad: "Start with one workflow."  
Better: "Start with your weekly newsletter."

<a id="s-16-fake-strong-verbs"></a>

### S-16 Fake-strong verbs

boasts, features, offers, maintains (instead of "has").

Bad: "The app boasts an intuitive interface."  
Better: "The app has a drag-and-drop calendar."

<a id="s-17-imagine-a-world"></a>

### S-17 Imagine a world

imagine a world where, picture this, what if I told you.

Bad: "Imagine a world where your posts write themselves."  
Better: Describe what the product does today.

<a id="s-18-hedge-stacking"></a>

### S-18 Hedge stacking

may potentially, could possibly, might help to, can sometimes.

Bad: "This may potentially help improve results."  
Better: "This improved reply rate by 8% in our test." Or cut it.

<a id="s-19-both-sides-filler"></a>

### S-19 Both-sides filler

"While X has benefits, it also has drawbacks."

Bad: "While automation saves time, it's important to stay authentic."  
Better: Take a position and support it.

<a id="s-20-from-x-to-y-range"></a>

### S-20 From X to Y range

"From startups to enterprises", "from strategy to execution".

Bad: "From ideation to publication, we've got you covered."  
Better: Name the two steps you actually handle.

<a id="s-21-interpretive-asides"></a>

### S-21 Interpretive asides

Telling the reader how to read the text.

Bad: "That last point matters more than it sounds."  
Better: Show why it matters, or delete the aside.

<a id="s-22-rhetorical-self-correction"></a>

### S-22 Rhetorical self-correction

"Actually, let me rephrase that", "Or rather..."

Bad: "It's fast. Or rather, it's instant."  
Better: "It's instant."

<a id="s-23-if-you-ve-ever"></a>

### S-23 If you've ever...

False familiarity setup: If you've ever wondered, If you've ever struggled with.

Bad: "If you've ever struggled with writer's block, this is for you."  
Better: "This helps when you can't think of what to post."

<a id="s-24-sound-familiar"></a>

### S-24 Sound familiar?

Rhetorical resonance device: Sound familiar?, Ring a bell?, You know the feeling?

Bad: "Deadlines, pressure, no time to think. Sound familiar?"  
Better: "Most teams don't have time to write posts."

<a id="structure-and-rhythm"></a>

## Structure and rhythm

Slop is often in the shape of the text, not the words.

<a id="r-01-one-line-paragraph-stacks"></a>

### R-01 One-line paragraph stacks

Many short lines in a row, each a slogan.

Bad: "I quit my job. / I built a product. / Nobody came. / Then I learned this."  
Better: Write it as one paragraph.

<a id="r-02-fragment-drumbeat"></a>

### R-02 Fragment drumbeat

Strings of fragments for rhythm.

Bad: "Code. Content. Customers. Every day."  
Better: One full sentence that says what you do every day.

<a id="r-03-repeated-starters"></a>

### R-03 Repeated starters

Several lines that start with the same word or phrase.

Bad: "It saves time. It saves money. It saves your sanity."  
Better: "It saves about four hours a week."

<a id="r-04-identical-sentence-shapes"></a>

### R-04 Identical sentence shapes

Every sentence the same length and structure.

Bad: A paragraph of 12-word sentences, each "Subject verb object, comma, clause."  
Better: Vary length when it helps the point.

<a id="r-05-list-dumps"></a>

### R-05 List dumps

Long inventories of nouns in one breath.

Bad: "sales, marketing, support, ops, finance, hiring, legal and product."  
Better: Pick the two that matter here.

<a id="r-06-bullets-for-everything"></a>

### R-06 Bullets for everything

Bullet points where two sentences of prose would read better.

Bad: Three bullets of four words each.  
Better: One sentence.

<a id="r-07-headings-on-tiny-sections"></a>

### R-07 Headings on tiny sections

Headers over one or two sentences.

Bad: "## Why it matters" followed by one line.  
Better: Fold it into the paragraph above.

<a id="r-08-recap-ending"></a>

### R-08 Recap ending

A final paragraph that repeats the whole piece.

Bad: "To recap, we covered A, B and C."  
Better: End on the last point or the next action.

<a id="r-09-mic-drop-ending"></a>

### R-09 Mic-drop ending

A final "deep" one-liner.

Bad: "The future isn't coming. It's already here."  
Better: End on the clearest concrete sentence.

<a id="r-10-challenges-and-future-outlook"></a>

### R-10 Challenges and future outlook

A formulaic "Despite challenges, the future looks promising" closer.

Bad: "Despite these challenges, the outlook remains positive."  
Better: Name the challenge and what is being done.

<a id="r-11-fake-unscripted-scaffolding"></a>

### R-11 Fake-unscripted scaffolding

"And honestly...", "And look...", "So yeah..." used as filler.

Bad: "And honestly? That's when it clicked."  
Better: Say what clicked.

<a id="r-12-over-structured-short-answers"></a>

### R-12 Over-structured short answers

A short reply split into sections with headers and bold labels.

Bad: A three-sentence answer with "Overview", "Key Points" and "Conclusion".  
Better: Three sentences.

<a id="imagery-and-metaphor"></a>

## Imagery and metaphor

AI likes making things vivid when they should be clear.

<a id="m-01-cute-metaphors"></a>

### M-01 Cute metaphors

Abstract things doing human or physical actions.

Bad: "Your data is whispering insights."  
Better: "Your data shows Tuesday posts get more replies."

<a id="m-02-things-that-live-or-sit"></a>

### M-02 Things that "live" or "sit"

Data, products or agents that live or sit somewhere.

Bad: "where your customer data lives."  
Better: "where your customer data is stored."

<a id="m-03-honest-dashboards"></a>

### M-03 Honest dashboards

Systems that "get honest", "tell the truth", "hide" or "reveal".

Bad: "Analytics finally get honest."  
Better: "Analytics now count only real views."

<a id="m-04-mixed-and-stacked-metaphors"></a>

### M-04 Mixed and stacked metaphors

Two or three images in one sentence.

Bad: "a north star that fuels the engine of growth."  
Better: Drop both images and say what drives growth.

<a id="m-05-fuel-and-engine"></a>

### M-05 Fuel and engine

fuel, engine, rocket, catalyst, springboard, flywheel (as decoration).

Bad: "content that fuels your growth engine."  
Better: "posts that bring in signups."

<a id="m-06-secret-sauce"></a>

### M-06 Secret sauce

secret sauce, magic, silver bullet, holy grail.

Bad: "Consistency is the secret sauce."  
Better: "Accounts that posted weekly grew twice as fast."

<a id="substance"></a>

## Substance

The deepest kind of slop: text that sounds informative and says nothing.

<a id="c-01-importance-puffery"></a>

### C-01 Importance puffery

Inflating significance: "marks a pivotal moment", "a significant shift".

Bad: "This marks a pivotal moment for the industry."  
Better: State the fact and let the reader judge.

<a id="c-02-vague-attribution"></a>

### C-02 Vague attribution

experts agree, studies show, many believe, it is widely regarded.

Bad: "Studies show posting daily works."  
Better: Name the study, or cut the claim.

<a id="c-03-generic-claims-without-receipts"></a>

### C-03 Generic claims without receipts

Claims any company could make.

Bad: "AI can transform your business."  
Better: "Our AI drafts a week of posts from a 3-line brief."

<a id="c-04-the-portability-test"></a>

### C-04 The portability test

A sentence that could move unchanged to another company or topic.

Bad: "We're committed to delivering value to our customers."  
Better: A sentence only you could write.

<a id="c-05-fake-profound-wisdom"></a>

### C-05 Fake-profound wisdom

Lines that sound deep and mean nothing concrete.

Bad: "Growth is a mindset, not a metric."  
Better: Say what you measure and why.

<a id="c-06-smoothing-the-specific"></a>

### C-06 Smoothing the specific

Replacing a sharp fact with a generic description.

Bad: "a leading expert in the field."  
Better: "who wrote the Kubernetes scheduler."

<a id="c-07-made-up-specifics"></a>

### C-07 Made-up specifics

Invented numbers, names or examples presented as real.

Bad: "Sarah, a marketing manager, saved 10 hours a week." (no Sarah exists)  
Better: A real example, or none.

<a id="c-08-telling-instead-of-showing"></a>

### C-08 Telling instead of showing

Labeling something surprising, important or interesting.

Bad: "Surprisingly, the simple version won."  
Better: "The simple version got twice the clicks."

<a id="c-09-canned-notability"></a>

### C-09 Canned notability

"featured in top outlets", "widely recognized", "has an active social media presence".

Bad: "She has been featured in numerous leading publications."  
Better: Name one, with a link.

<a id="c-10-superficial-balance"></a>

### C-10 Superficial balance

Every point gets a "however" so the text never commits.

Bad: "AI is powerful. However, it has limitations."  
Better: Say which limitation matters for this reader.

<a id="c-11-advice-with-no-steps"></a>

### C-11 Advice with no steps

Telling the reader to "optimize", "be strategic" or "stay consistent" without saying how.

Bad: "Optimize your posting schedule."  
Better: "Post Tuesday to Thursday between 8 and 10am."

<a id="c-12-hollow-promises"></a>

### C-12 Hollow promises

"Everything you need to know", "the ultimate guide", "master X in minutes".

Bad: "The ultimate guide to LinkedIn."  
Better: "How to write a LinkedIn post that gets replies."

<a id="formatting-and-punctuation"></a>

## Formatting and punctuation



<a id="f-01-em-dash-habit"></a>

### F-01 Em dash habit

Em dashes used everywhere for rhythm.

Bad: "It's fast — really fast — and free."  
Better: "It's fast and free." Use commas, periods or parentheses.

<a id="f-02-bold-sprinkled-mid-sentence"></a>

### F-02 Bold sprinkled mid-sentence

Random words in bold for emphasis.

Bad: "This is **really important** for **growth**."  
Better: No bold; let the sentence carry it.

<a id="f-03-emoji-as-bullets"></a>

### F-03 Emoji as bullets

✅ 🚀 💡 👉 used as list markers or decoration.

Bad: "✅ Faster ✅ Cheaper ✅ Better"  
Better: A plain sentence.

<a id="f-04-title-case-headings"></a>

### F-04 Title Case Headings

Every Word Capitalized In Headings.

Bad: "How To Grow Your Audience On LinkedIn"  
Better: "How to grow your audience on LinkedIn"

<a id="f-05-colon-label-lines"></a>

### F-05 Colon-label lines

Every line starts with a bold label and a colon.

Bad: "**Speed:** fast. **Price:** low. **Support:** great."  
Better: A sentence about the one that matters.

<a id="f-06-markdown-in-the-wrong-place"></a>

### F-06 Markdown in the wrong place

Asterisks, hashtags or headers pasted into emails, posts or forms.

Bad: "**Subject:** ..." inside a LinkedIn post.  
Better: Plain text.

<a id="f-07-curly-quote-and-character-mix"></a>

### F-07 Curly-quote and character mix

Curly quotes, special dashes and non-breaking spaces mixed with plain text.

Bad: “quotes” next to "quotes" in one paragraph.  
Better: Pick one style.

<a id="f-08-exclamation-inflation"></a>

### F-08 Exclamation inflation

Exclamation marks on ordinary sentences.

Bad: "We updated the settings page!"  
Better: "We updated the settings page."

<a id="f-09-unicode-bold-and-fancy-fonts-in-long-posts"></a>

### F-09 Unicode bold and fancy fonts in long posts

𝗕𝗼𝗹𝗱 or 𝓈𝒸𝓇𝒾𝓅𝓉 letters across whole lines.

Bad: An entire LinkedIn post in Unicode bold.  
Better: Plain text, one bold phrase at most (screen readers can't read these).

<a id="f-10-tables-for-two-facts"></a>

### F-10 Tables for two facts

A table where a sentence would do.

Bad: A 2x2 table comparing price and speed.  
Better: "A is cheaper; B is faster."

<a id="chatbot-residue"></a>

## Chatbot residue

Text that was clearly copied out of a chat window.

<a id="b-01-assistant-openers"></a>

### B-01 Assistant openers

Certainly!, Absolutely!, Great question!, Of course!

Bad: "Certainly! Here's a LinkedIn post about..."  
Better: Delete it.

<a id="b-02-sycophancy"></a>

### B-02 Sycophancy

You're absolutely right, what a great idea, I love this.

Bad: An email reply starting "Great point, you're absolutely right!"  
Better: Answer the point.

<a id="b-03-offer-to-do-more"></a>

### B-03 Offer to do more

Would you like me to..., Let me know if you'd like a shorter version.

Bad: A published post ending "Would you like me to adjust the tone?"  
Better: Delete it.

<a id="b-04-here-is-a"></a>

### B-04 Here is a...

Lead-ins like "Here is a polished version of your post:" left in the final text.

Better: Delete the line.

<a id="b-05-placeholder-text"></a>

### B-05 Placeholder text

[Your Name], [Company], [insert statistic], XX%.

Better: Fill it in or cut the sentence.

<a id="b-06-ai-disclaimers"></a>

### B-06 AI disclaimers

As an AI, I don't have personal opinions; my knowledge is limited to...

Better: Delete it.

<a id="b-07-source-hedging"></a>

### B-07 Source hedging

"Based on available information", "specific details are limited".

Bad: "While specific figures are not widely available, ..."  
Better: Find the figure or don't mention it.

<a id="b-08-citation-debris"></a>

### B-08 Citation debris

Leftover markers like [1], contentReference, oaicite, turn0search0.

Better: Remove them, and check the claim they were attached to.

<a id="b-09-happy-to-help"></a>

### B-09 Happy to help!

Standalone AI closer: Happy to help!, Glad I could help!, Happy to assist!

Bad: "Let me know if you need anything else. Happy to help!"  
Better: "Let me know if you need anything else."

<a id="b-10-i-m-here-to-help"></a>

### B-10 I'm here to help

AI availability assertion: I'm here to help, I'm here to assist, Don't hesitate to ask.

Bad: "I'm here to help if you need anything."  
Better: Delete it. The work speaks for itself.

<a id="social-media-and-linkedin"></a>

## Social media and LinkedIn

Patterns that turn a post into "LinkedIn slop".

<a id="l-01-broetry"></a>

### L-01 Broetry

One sentence per line, top to bottom.

Bad: A 20-line post where every line is a new sentence.  
Better: Short paragraphs.

<a id="l-02-hook-formulas"></a>

### L-02 Hook formulas

"I was fired. Best thing that ever happened.", "Unpopular opinion:", "Stop doing X."

Better: Open with the specific thing that happened or the specific claim.

<a id="l-03-thrilled-to-announce"></a>

### L-03 Thrilled to announce

I'm thrilled/excited/humbled to announce, I'm proud to share.

Bad: "I'm thrilled to announce I've joined Acme!"  
Better: "I joined Acme to lead the growth team."

<a id="l-04-read-that-again"></a>

### L-04 Read that again

Read that again., Let that sink in., I'll say it louder.

Better: Delete it. If the line needs a second read, rewrite it.

<a id="l-05-agree-thoughts"></a>

### L-05 Agree? / Thoughts?

Engagement-bait closers.

Bad: "Agree? 👇"  
Better: Ask a real question, or don't.

<a id="l-06-the-lesson-list"></a>

### L-06 The lesson list

"Here are 7 lessons I learned from..." with generic lessons.

Better: One lesson with the story behind it.

<a id="l-07-humblebrag-setup"></a>

### L-07 Humblebrag setup

"I don't usually post this, but...", "This might be controversial, but..."

Better: Post it without the preamble.

<a id="l-08-thread-markers"></a>

### L-08 Thread markers

🧵, 1/, "A thread" on content that isn't a thread.

Better: Write the post.

<a id="l-09-hashtag-walls"></a>

### L-09 Hashtag walls

Ten or more hashtags at the end.

Better: Three relevant ones, or none.

<a id="l-10-that-s-it-that-s-the-post"></a>

### L-10 That's it. That's the post

Self-aware closers that announce the ending.

Bad: "That's it. That's the tweet."  
Better: Just stop.

<a id="l-11-p-s-engagement"></a>

### L-11 P.S. engagement

"P.S. Repost ♻️ if this helped." on every post.

Better: Drop it, or use it rarely.

<a id="l-12-no-fluff-just-value"></a>

### L-12 No fluff, just value

Announcing quality instead of delivering it: no fluff, just value; straight to the point; real talk.

Better: Delete the announcement.

<a id="l-13-comment-slop"></a>

### L-13 Comment slop

Generic replies: "Great insights!", "So true!", "Thanks for sharing, this is gold."

Better: Reply to something specific in the post, or don't reply.

<a id="l-14-fake-vulnerability-arc"></a>

### L-14 Fake vulnerability arc

"I failed. I was broke. Then I discovered X." built to sell.

Better: Tell what happened, with dates and numbers.

<a id="l-15-contrarian-template"></a>

### L-15 Contrarian template

"Everyone says X. They're wrong."

Better: Make your claim and back it up; skip the strawman.

## License

MIT. Use it, change it and ship it in your own tools.
