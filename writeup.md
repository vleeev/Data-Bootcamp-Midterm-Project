**NYC School Performance: What Predicts It?**

This project looks at a basic question: what kinds of things are most closely linked to how well New York City public schools perform? I focused on three results that most people care about: grades 3–8 ELA proficiency, grades 3–8 Math proficiency, and the high school graduation rate. Then I matched those results with information about each school: the size of the school, the mix of student groups, and the economic need index that the city reports. In short, the goal was to see which factors move together with better or worse outcomes.

**Data and setup**
I combined three sources. First, I pulled ELA and Math proficiency from NYC Open Data (or used a CSV copy of the same fields). Second, I used a DOE cohort file for the graduation rate. Third, I loaded the Demographic Snapshot, which includes a school’s enrollment, race/ethnicity shares, and the “economic need index,” a number between 0 and 1 that captures how many students come from low-income households or face related challenges. Everything was cleaned so each row is a school, identified by its DBN. If a field was given as a proportion (0–1), I converted it to a percent (0–100) to keep the scales consistent.

**What I looked for**
I started with basic plots and correlations to see how outcomes move with each factor. I then fit simple linear models (think: straight-line summaries) for each outcome separately. The idea wasn’t to prove cause-and-effect, but to get a clear reading on which variables line up with higher or lower performance once they are considered at the same time.

**What stood out**
The clearest pattern is the relationship between the economic need index and all three outcomes. Schools with higher economic need tend to have lower ELA and Math proficiency and lower graduation rates. This shows up in the scatterplots and in the model summaries. It’s not a surprise thateconomic stress shows up at school in lots of ways, from attendance to time for homework to access to extra help, but it’s useful to see how consistently it tracks across ELA, Math, and graduation.

The next pattern is that ELA and Math move together. The same schools that do better in ELA usually do better in Math, and the schools that struggle in one tend to struggle in the other. Math sometimes drops faster as economic need increases, but the general direction is the same. Graduation is a little steadier than the test outcomes (fewer schools at the extremes), yet it still follows the same basic relationship with economic need.

**What about school composition and size?**
Shares of racial/ethnic groups are related to outcomes in the raw data because they also line up with neighborhood and economic differences across the city. Once the model accounts for economic need, those composition effects get smaller. In other words, composition looks like a proxy for deeper, neighborhood-level conditions rather than something that independently predicts scores. Enrollment (school size) doesn’t explain much after other factors are included. In a few cases slightly larger schools do a little better, but the effect is small and inconsistent.

**How to read this**
Nothing here proves that one variable causes another. These are patterns in a single year of data, and lots of things we can’t see in a spreadsheet matter: leadership, teacher experience, specific programs, partnerships, and so on. Still, the results are useful because they point to the same conclusion from different angles: economic conditions are the strongest and most consistent correlate of school performance in this cross-section.

**Limits**
There are three main limitations to keep in mind. First, this is correlational, not causal. Second, it’s mostly a single snapshot; looking at several years would let us see whether changes at a school track with changes in outcomes. Third, some measures are proxies (for example, economic need is a summary metric), and there are likely important variables we didn’t include (program type, school selectivity, mobility, language services, etc.).

**What I would do next**
If I had more time, I’d add more years of data and re-fit the models to see if the same patterns hold; I’d also add a few neighborhood variables from the Census (income, unemployment, housing cost burden) to separate school-level and neighborhood-level effects. Finally, I’d try simple fairness checks like running the models by borough or by grade span to make sure the results don’t hinge on one subset of schools.

**Bottom line**
Across NYC schools, the factor that most closely tracks with ELA, Math, and graduation is economic need. Composition and size matter much less once that is taken into account. If the city wants to raise scores and graduation rates broadly, the data here suggest that the biggest gains will come from reducing the day-to-day pressures that come with poverty, leading more time and support for students, stronger attendance, and tutoring and enrichment where it’s needed most.
