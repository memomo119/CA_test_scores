#### README

## Problem Statement

This project examines the performance of California high school students on college entrance exams to identify specific schools that could benefit from additional resources. Moreover, this project identifies a few trends that may be generalizable to other states and/or schools not surveyed.

## Data Dictionary

Some of the terms in the NCES dataset are also defined in their [data glossary](https://nces.ed.gov/ccd/commonfiles/glossary.asp). 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|avg_math_score|int|SAT Natl 2019|the mean average score of all test-takers in the state on the math section of the SAT|
|avg_reading_writing_score|int|SAT Natl 2019|the mean average score of all test-takers in the state on the evidence-based reading and writing section of the SAT|
|avg_total_score|int|SAT Natl 2019|the mean average score of all test-takers in the state when both subscores on the two sections of the SAT are combined|
|charter|object|NCES|Per NCES: A school providing free public elementary and/or secondary education to eligible students under a specific charter granted by the state legislature or other appropriate authority, and designated by such authority to be a charter school. See the [NCES glossary](https://nces.ed.gov/ccd/commonfiles/glossary.asp)|
|county|object|NCES, SAT-CA|the county where the school is located|
|district|object|NCES, SAT-CA|the school district the school is part of|
|free_reduced_lunch|float|NCES|percent of all students at the school who meet the income-based federal eligibility criteria to receive low-cost or no-cost meals through the National School Lunch program|
|locale|object|NCES|Per NCES: An indication of school's location relative to a populous area. The locales assigned to school districts are based on the locale code of their schools, weighted by the size of the schools' membership. The urban-centric locale assignment system has been used starting in 2006-07. For more detailed definitions, please see the [NCES glossary](https://nces.ed.gov/ccd/commonfiles/glossary.asp).|
|magnet|object|NCES|Per NCES: A special school or program designed to attract students of different racial/ethnic backgrounds for the purpose of reducing, preventing, or eliminating racial isolation (50 percent or more minority enrollment); and/or to provide an academic or social focus on a particular theme (e.g., science/math, performing arts, gifted/talented, or foreign language). See the [NCES glossary](https://nces.ed.gov/ccd/commonfiles/glossary.asp)|
|num_students|int|NCES|the total enrollment for the school in the 2019-20 school year|
|participation_rate|float|SAT Natl 2019|percent of eligible students in the state who took the SAT exam during that school year|
|participation_rate|float|SAT-CA|percent of all students enrolled in the school who took the SAT exam as an 11th or 12th grader during that school year|
|pct_erw_benchmark_met_12|float|SAT-CA|percentage of 12th grade students meeting the SAT benchmark score in evidence-based reading and writing (ERW)|
|pct_math_benchmark_met_12|float|SAT-CA|percentage of 12th grade students meeting the SAT benchmark score in math|
|pct_math_benchmark_met_11|float|SAT-CA|percentage of 11th grade students meeting the SAT benchmark score in math|
|pct_both_benchmarks_met_12|float|SAT-CA|percentage of 12th grade students meeting both SAT benchmark scores in evidence-based reading and writing and math|
|pct_both_benchmarks_11|float|SAT-CA|percentage of 11th grade students meeting both SAT benchmark scores in evidence-based reading and writing and math|
|school_name|object|NCES, SAT-CA|the official name of the school|
|state|object|all|state, territory, or federally recognized region of the United States|
|state_scid|float|NCES, SAT-CA|a unique identifier for each school in the data set| |title_1|object|NCES|Yes/No value indicating if this school receives federal funding under Title I to support core academic programming at low-income schools|

## Analysis

Overall, California students are doing okay on the SAT. The state has a slightly below-average total average score, but somewhat higher participation. Higher participation generally depresses scores, so we should not be concerned about California on the whole. 

However, when we add in measurements of socioeconomic level, namely student eligibility for free and reduced lunch and school Title I status, we can see that lower incomes are strongly correlated with lower test scores and lower test participation rates.

## Conclusions

Based on my exploration of the data, I have a few recommendations for education policy-makers and non-profit organizations that operate out of public schools.

- Given that a college degree is a proven mechanism for increasing lifetime earnings, it should be a priority to ensure that low-income students graduate ready for college.
- Low-income California students are not as well-prepared for important college entrance exams like the SAT as their higher-income peers. We need to allocate additional resources to help more low-income students succeed on these tests.
- This project focuses on the state of California, but the conclusions are informed by national-level data. The relationship between free and reduced lunch eligibility and test scores is clear, strong, and alarming. Policy-makers in other jurisdictions should consider conducting similar examinations in their own region.
- The two federal programs considered here -- National School Lunch and Title I -- are not sufficient to erase achievement disparities based on socioeconomic factors. We need to invest in our students if we want to see them go to college and break out of cyclical poverty.

## External Sources

* [National Center for Education Statistics (NCES)](https://nces.ed.gov/ccd/schoolsearch/) School Search

* [Social Security Administration](https://www.ssa.gov/policy/docs/research-summaries/education-earnings.html) research summary on education and lifetime earnings. 

* [National School Lunch program](https://www.fns.usda.gov/nslp/nslp-fact-sheet), one of the federal programs operating in schools to address low-income students' food insecurity needs. 

* [Title I](https://www2.ed.gov/programs/titleiparta/index.html), another federal funding program for low-income K-12 schools. 
