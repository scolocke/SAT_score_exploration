Problem Statement: We believe that the current usage of standardized tests, such as the SAT, has inherent bias based on demographics, and we examine the extent of this possible bias.

Looking into demographics, specifically based on race, to see if there are any major biases that could be found in how the SAT judges performance. 

### My Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|categories|object|SAT|Different demographic categories,broken into ethnicity and gender for a given state and year| 
|test_takers|float|SAT|Number of test takers for the for the specific category|
|total_mean|float|SAT|Average combined score for math and evidence based reading and writing (max score 1600, min score 400)|
|erw_mean|float|SAT|Average score on the evidence based reading and writing section (200-800)|
|math_mean|float|SAT|Average score on the math section (200-800)|
|met_both|float|SAT|Proportion of students that meet both benchmarks for math and evidence based reading and writing. Benchmark corresponds to score assigned to likely achieve a score of 75% or greater in the corresponding freshman courses|
|met_neither|float|SAT|Proportion of students that did not meet either benchmarks for math and evidence based reading and writing. Benchmark corresponds to score assigned to likely achieve a score of 75% or greater in the corresponding freshman courses|
|erw_met|float|SAT|Proportion of students that meet benchmark for evidence based reading and writing. Benchmark corresponds to score assigned to likely achieve a score of 75% or greater in the corresponding freshman courses|
|math_met|float|SAT|Proportion of students that meet benchmark for math. Benchmark corresponds to score assigned to likely achieve a score of 75% or greater in the corresponding freshman courses|
|year|int|SAT|Year that the test results were recorded.|
|state|object|SAT|State for which the data set corresponds. "all" refers to the data corresponding to all of the US|
|participation|float|SAT|Proportion of the student popualtion for the given state that partook in the SAT|
|diff_to_ave|float|SAT|Difference between category and total for the correspoding state and year.|

#Brief Analysis
See that white and Asian groups perform well compared to average, while the rest perform poorly to average.

States with higher participation rates tend to have lower average scores than those states with lower participation rates. This is likely a difference in accessability of the tests in different states, allowing people to take it if on the fence, as opposed to those who are sure they are college bound opting in, and more likely better prepared. Motivates wanting to take references to state mean. 

Mapping to difference from average, greatly reduces varaince, but there is still a lot there compared to splitting on gender which resembles a more natural statistical fluctuation. Shows that not all of the correlation is fixed with this method. 

All categories, have fairly wide spread, which is reduced when corrected by state. The state correction greatly reduces uncertainty, and a larger gap between ethnicities can be seen. The raw mean total tracks with meeting both benchmarks as expected, but one misleading thing most people would probably overlook is what the scale translates to for a score and whether or not they meet benchmarks. Comparing latinos to whites, a little more than a 100 point difference in the average total score (with a max score of 1600) translates to ~30% to the group median meeting both benchmarks, nearly doubling the overall value. These are standardized tests and fall on a bell curve, so a >100 point increase is nearing a standard devation difference for the actual population. 

These two are the two categories with closest negative and positive average difference to the total mean respectivley, and the problem would only become even more exagerated going to other demographics on the negative end. 

#Conclusion
Results from the SAT show a strong correlation between ethnicity and SAT performance, and therefore at some level there is a fundamental bias. However, correlation does not prove causation

Although the bias is clear, more studies would need to be performed to better understand the cause of these differences.

 - Potential causes could stem from socioeconomic factors, cultural importance on scholastic performance and test preparation, and difference in public school quality based on location.
  - Difference in SAT scores may not be indicative of an actual difference in intelligence

Recommend placing less emphasis on SAT results for college admission until more research can be done on the cause of discrepancies

Outside data sets from:
 - 2017 ([*source*](https://research.collegeboard.org/programs/sat/data/2017-sat-suite-annual-report))
 - 2018 ([*source*](https://research.collegeboard.org/programs/sat/data/2018-sat-suite-annual-report))
 - 2019 ([*source*](https://research.collegeboard.org/programs/sat/data/2019-sat-suite-annual-report))



