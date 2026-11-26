# Report

One HTML page, written in the user's language, for a reader who has not seen the analysis and will decide from the page alone.

## How it reads

- **Headings are claims.** "From fifteen steps to eight, without a terminal" tells the reader the result; "Setup" tells them the topic.
- **Numbers carry the argument.** "15 steps, 4 of them in a terminal" where a draft says "setup is complicated".
- **Every weakness names its consequence**: what a user or an operator loses because of it.
- **Only confirmed claims appear as fact.** A claim the checker could not test is marked where it stands and listed again in section 11.

## Sections, in this order

1. **Head.** Target, date, commit, and the baseline's counts as a row of figures. Under it the thesis: one sentence that says where the target is strong and where the work lies.
2. **The most important.** Three to five points a reader with one minute takes away: what is strong, what is weak, what to do first.
3. **One chapter per lens.** Each opens with its verdict as the heading, then the present state, what is good, the findings as a table (severity, finding with its location, consequence, fix, effort), then its proposals. The inventory chapter comes first.
4. **What must stay.** The strengths from all lenses as one list of conditions, with their measures. Every concept and every stage is held to this list.
5. **Concepts.** Two or three ways to solve the whole, far enough apart that choosing between them is a real decision. Each with a sketch, its precedent from the outward lens, and its price in the measures of section 4. Then one recommendation, what it takes over from the others, and the risk it still carries.
6. **The recommended concept in detail**, exact enough to build from. For an interface: type sizes, spacing, radii, one meaning per colour, and the new order as one rule plus a tree of what lives where. For code: the target structure, the contracts between its parts, and the path from here to there.
7. **What comes next.** The proposals of all lenses in one table, ranked by gain against effort, with the bold bets set apart.
8. **What stays unbuilt.** The rejected ideas, each with its reason.
9. **Measure first.** The lenses' open questions as experiments with their durations: what nobody knows yet. A stage that depends on one says so.
10. **Stages.** Numbered, ordered by gain against effort, the small things with large effect first. Each stage has a name, its items, its effort, the stages it depends on, and what only the user can provide. Under the list, a note to whoever builds a stage: test each finding against the code as it is then, since the repository moves on, and hold the build to section 4.
11. **How this report was made.** The lenses, the checker and how many claims it corrected, every command that ran with its result and duration, and what was left alone under Read-only. Then **what is not verified**: every claim in the page that stands without the checker's confirmation, and why. Then the sources.

## The page

- One file that opens offline: styles and drawings inline, no requests to other hosts.
- A table of contents that stays reachable while reading, on a phone and on a desktop.
- Light and dark, following the system.
- Sketches are drawn in the page, to scale, with the real labels. An interface concept is a mockup of the actual screen. A structure concept is a diagram of the parts and what passes between them.
