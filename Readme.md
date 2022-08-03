# H1 Methodology

How We Analyzed Michigan Child Care Daycare Data

Our reporting relies on data released by the State of Michigan in response to a Freedom of Information Request (FOIA). In March, MuckRock requested data self-reported by providers who applied for two rounds of Child Care Stabilization Grants. The data gave us two glimpses into roughly 5,900 child care providers out of a total pool of roughly 7,900.

Those providers told the state about their current enrollments, as well as about their waiting lists, staffing needs, and expenses. MuckRock used those enrollments to help calculate daycare deserts, which previously had only been calculated with licensed capacity – or the maximum number of children that facilities can legally enroll. Interviews with providers indicated that enrollment numbers offered a more accurate picture of a county’s needs. This is often because facilities are short-staffed, but also because parents can’t afford the service. To calculate deserts, MuckRock stitched enrollments from the 5,900 grant recipients with the licensed capacity of the 2,000 non-applicants. In this way, we assumed an enrolled-to-capacity scenario for centers for which we had no information. As a result, the 18 deserts we identify are a minimum estimate. If we had actual enrollment numbers for every facility in the state, it’s likely we’d see a handful more counties qualify as deserts – already, more than 24 are extremely close to the 3:1 threshold.

# H1 A Note On Previous Desert Estimates

Michigan legislators have publicly quoted a number popularized in 2021, which states that 44% of Michiganders live in a child care desert. That number, calculated by the Michigan League for Public Policy in 2021, actually uses a different definition than the Center for American Progress’s (CAP) definition of a child care desert. MLPP’s deserts include children age 5, while CAP’s (and MuckRock’s) only includes children under 5. The reason for this is because many 5-year-olds spend some, or all, of their year in kindergarten programs. Because MLPP included more children in their analysis, their 2021 report overestimates Michigan child care deserts. Despite that, MuckRock’s analysis uses CAP’s narrower age range, as well as more precise enrollment data, to find at least 7 more deserts than MLPP calculated.

#H1 Data Files in this Repository

"Grant Data" is a spreadsheet of largely raw data provided to us by FOIA request by the Michigan Department of Education. The file is a joined version of two files that were given in response to the request, one called "Grant Data" and "Age Details". We found the joined version was essential to doing data analysis. If you'd like the unjoined, raw versions, please email luca@muckrock.com. NB "Grant Data" does not include roughly 2,000 centers that did not apply for grants. 

"LARA Database" is a spreadsheet of every licensed childcare facility in the state of Michigan, as of LARA's website on June 5th, 2022.

"Final Deserts" is a spreadsheet with the essential columns for calculating Michigan county desert ratios. The values in each column originate from the above files. The columns were calculated as follows:
    - Full-Time and Part-Time Enrolled: Summing all enrolled students for each center in the grant data. This value is likely an overestimate, since we counted part-time students as equivalent to full-time students.
    - Capacity in Centers that Didn't Receive Grants: We outer joined grant-recipient centers with the LARA database to identify ~2,000 centers that didn't receive grants. This column shows the licensed capacity of those centers by county. This value is likely an overestimate, since we don't know how many of these centers are actually under-enrolled.
    - Total 'Optimistic' Childcare Enrollment: The sum of "Full-Time and Part-Time Enrolled" and "Capacity in Centers that Didn't Receive Grants"
    - ACS Population Under 5: Census demographics by county.
    - Desert Ratio: "ACS Children Under 5-Years-Old	" divided by "Total 'Optimistic' Childcare Enrollment".
