# Methodology

How We Analyzed Michigan Child Care Daycare Data

Since 2021, Michigan legislators have publicly quoted a number estimating that 44% of Michiganders live in a child care “desert.” In reality, that number, calculated by the Michigan League for Public Policy, misinterprets the Center for American Progress’ (CAP) definition of what is a child care desert. 

The MLPP’s desert calculation includes 5-year-olds while the CAP’s analysis includes only children under 5. Our analysis relies on CAP’s narrower age range, as well as more precise enrollment data, to find at least nine more deserts in Michigan than the MLPP originally calculated. 

In response to questions, CAP said the narrower age range is preferable because many 5-year-olds are enrolled in kindergarten or public school programs. But the MLPP; Michigan’s Early Childhood Investment Corp. a public organization that contracts with the state to help run the child care system; and the governor’s office defended their methodology. “Trusted child care advocates use the 0-5 age range to analyze various issues affecting child care in our state and the subsequent data leads to identical calls for expanded resources and support to address this critical shortage,” said Bobby Leddy, a spokesperson for the governor.

Our reporting on Michigan’s child care industry relies on data released by Michigan in response to state Freedom of Information Act requests. In March, we requested data that had been self-reported by providers who applied for two rounds of Child Care Stabilization Grants, as part of a $1.4 billion pot of federal relief funds. The data gave us two glimpses into roughly 5,900 child care providers out of a total pool of roughly 7,900 across the state.

Those providers told the state about their current enrollments, as well as about their waiting lists, staffing needs and expenses. We calculated wait lists by county and the number of providers that didn’t apply for grant monies using these figures. We also used enrollment figures to help calculate day care deserts, which previously had been calculated only using licensed capacity — or the maximum number of children that facilities can legally enroll. 

Interviews with providers indicated that enrollment numbers offered a more accurate picture of a particular county’s child care needs. This is often because facilities are short-staffed but also because many parents simply can’t afford child care. In some cases, parents said they were too anxious about COVID-19 to return their children to day care facilities, however it’s not clear if those fears are still a main driver given the availability of a vaccine for children as young as 6 months old.

To calculate deserts, we cross-referenced enrollments from the 5,900 grant recipients with the licensed capacity of the 2,000 non-applicants. In this way, we assumed an enrolled-to-capacity scenario for centers for which we had no information. 

As a result, the 20 county “deserts” we identify are a minimum estimate. If we had actual enrollment numbers for every facility in the state, it’s likely that several additional Michigan counties would qualify as deserts; Twenty-three counties are mere rounding errors away from the 3-to-1 threshold.


#  Data Files in this Repository

- "Grant Data" is a spreadsheet of largely raw data provided to us by FOIA request by the Michigan Department of Education. The file is a joined version of two files that were given in response to the request, one called "Grant Data" and "Age Details". We found the joined version was essential to doing data analysis. If you'd like the unjoined, raw versions, please email luca@muckrock.com. NB "Grant Data" does not include roughly 2,000 centers that did not apply for grants. 

- "LARA Database" is a spreadsheet of every licensed childcare facility in the state of Michigan, as of LARA's website on June 5th, 2022.

- "Final Deserts" is a spreadsheet with the essential columns for calculating Michigan county desert ratios. The values in each column originate from the above files. The columns were calculated as follows:
    - Full-Time and Part-Time Enrolled: Summing all enrolled students for each center in the grant data. This value is likely an overestimate, since we counted part-time students as equivalent to full-time students.
    - Capacity in Centers that Didn't Receive Grants: We outer joined grant-recipient centers with the LARA database to identify ~2,000 centers that didn't receive grants. This column shows the licensed capacity of those centers by county. This value is likely an overestimate, since we don't know how many of these centers are actually under-enrolled.
    - Total 'Optimistic' Childcare Enrollment: The sum of "Full-Time and Part-Time Enrolled" and "Capacity in Centers that Didn't Receive Grants"
    - ACS Population Under 5: Census demographics by county.
    - Desert Ratio: "ACS Children Under 5-Years-Old	" divided by "Total 'Optimistic' Childcare Enrollment".
