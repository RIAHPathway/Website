# RIAH PATHWAY PRICING ENGINE
## Final Tuition and Fees Calculator Logic and Softr Build Specification


### By Mariah Dominique Rucker


Student-facing heading:


# BUILD YOUR RIAH PATHWAY. SEE WHAT IT COSTS.


The calculator is an estimated tuition and fees calculator.


> This Markdown file preserves the complete Pricing Engine specification from the finalized chat response, including Sections 1–49, formulas, GUI logic, Softr data structure, YAML configuration, pseudocode, examples, and safeguards.




## Pricing Engine Update — Scholarships, Grants, Stipends, Contributors, and Ambassadors


### Tuition Reduction Categories


| Category | Tuition Reduction | Product Reduction |
|---|---:|---:|
| Community Contributors | Up to 25% | Up to 25% |
| Substitute Teacher Ambassadors | Up to 25% | Up to 25% |
| Rideshare and Delivery Ambassadors | Up to 25% | Up to 25% |


Each contributor or ambassador tuition-reduction dropdown contains every whole-number percentage from 1% through 25%.


Each contributor or ambassador product-reduction dropdown contains every whole-number percentage from 1% through 25%.


Contributor and ambassador tuition reductions remain subject to the existing 25% maximum stacked ordinary tuition-reduction rule. Product reductions remain separate from tuition calculations.


### Scholarships — Fixed Internal Amounts


| Scholarship | Amounts |
|---|---|
| Need-Based Scholarship | $500, $2,500, $5,000, $10,000, $15,000, $50,000 |
| Merit-Based Scholarship | $500, $2,500, $5,000, $10,000, $15,000, $50,000 |


The Scholarship interface uses a Scholarship Type dropdown and a Scholarship Amount dropdown.


### Grants — Fixed Internal Amounts


| Grant | Amounts |
|---|---|
| Need-Based Grant | $500, $2,500, $5,000, $10,000, $15,000, $50,000 |
| Merit-Based Grant | $500, $2,500, $5,000, $10,000, $15,000, $50,000 |


The Grant interface uses a Grant Type dropdown and a Grant Amount dropdown.


### Stipends — Fixed Internal Amounts


| Stipend | Amount |
|---|---:|
| Student Support Stipend Level 1 | $100 |
| Student Support Stipend Level 2 | $200 |
| Student Support Stipend Level 3 | $300 |
| Student Support Stipend Level 4 | $400 |
| Student Support Stipend Level 5 | $500 |


Stipend uses include textbooks, workbooks, graduation fees, transfer fees, educational materials, and other approved student-support expenses.


### Calculator Funding Formula


**Established Funding = Internal Scholarship + Internal Grant + Internal Stipend**


**Remaining Tuition = MAX(Tuition After Reductions − Established Funding − Estimated External Funding, $0)**


Funding does not count toward the 25% tuition-reduction maximum and cannot create negative tuition.


### Contributor and Ambassador Dropdown Logic


For Community Contributor, Substitute Teacher Ambassador, and Rideshare and Delivery Ambassador:


- Tuition Reduction: student selects 1% through 25% in 1% increments.
- Product Reduction: student selects 1% through 25% in 1% increments.
- Tuition reduction counts toward the existing 25% maximum ordinary tuition reduction.
- Product reduction is calculated separately from tuition.


### Pricing Engine Safeguards


- Need-Based Scholarship and Merit-Based Scholarship use fixed internal amounts of $500, $2,500, $5,000, $10,000, $15,000, or $50,000.
- Need-Based Grant and Merit-Based Grant use fixed internal amounts of $500, $2,500, $5,000, $10,000, $15,000, or $50,000.
- Student Support Stipend Levels 1–5 use $100, $200, $300, $400, and $500 respectively.
- Internal Scholarship, Grant, and Stipend selections are estimated funding values used within the tuition and fees calculator.
- Community Contributor, Substitute Teacher Ambassador, and Rideshare and Delivery Ambassador tuition and product reduction selectors use 1% increments from 1% through 25%.
- Existing Pricing Engine rules remain unchanged except where these additions expressly update the calculator.


## Pricing Engine Update — Education Deposit and Minor Resource Allocation


- Minor Student Resource Allocation: **$500 per selected Minor**.
- The Minor allocation supports the actual textbooks for the three major courses, applicable software, and the Minor Applied Learning and Capstone Collection, including applicable software associated with that collection.
- Associate's Student Resource Allocation: **$500 each**.
- Bachelor's Student Resource Allocation: **$1,000 each**.
- Master's Student Resource Allocation: **$1,000 each**.
- MBA Student Resource Allocation: **$1,000 each**.
- Education Deposit RIAH Fee: **$500 once**.


**MINOR_RESOURCE = minor_count × $500**


**TOTAL_STUDENT_RESOURCE_ALLOCATION = MINOR_RESOURCE + ASSOCIATE_RESOURCE + BACHELOR_RESOURCE + MASTER_RESOURCE + MBA_RESOURCE**


**EDUCATION_DEPOSIT = $500 + TOTAL_STUDENT_RESOURCE_ALLOCATION**


## Pricing Engine Update — Title IV and Non-Title-IV Payment Logic


### Title IV — Fixed Semester Payment


When **Title IV = Yes**:


- Automatically select **Semester** as the payment structure.
- Hide or disable Upfront, Monthly, and Per Course as accelerated payment paths while Title IV funding is being used.
- Use the pathway's typical duration and fixed six-month semesters.
- Assign the fixed courses established for each semester.
- The student completes the fixed courses for the current semester before progressing to the next semester.


**TITLE_IV_SEMESTER_TUITION = APPLICABLE_PROGRAM_TUITION ÷ TYPICAL_SEMESTER_COUNT**


JD example:


**Typical JD Duration = 4 Years**


**Typical JD Semesters = 8**


**$40,000 ÷ 8 = $5,000 Per Semester**


**$5,000 × 2 = $10,000 Per Year**


**$10,000 × 4 = $40,000 Total Tuition**


### Non-Title IV — Available Payment Structures


When **Title IV = No**, display:


- Upfront
- Monthly
- Per Course


Non-Title-IV students may accelerate. Acceleration changes completion timing and does not independently reduce total-program tuition.


### Upfront


The existing **15% Upfront Payment Reduction** remains subject to the existing 25% ordinary tuition-reduction maximum.


JD example, assuming only the 15% Upfront Payment Reduction:


**$40,000 × 15% = $6,000 Reduction**


**$40,000 − $6,000 = $34,000 Upfront Tuition**


Courses remain sequential. After the current course is completed, the next course unlocks without an additional tuition payment because the applicable tuition has already been paid upfront.


### Monthly


Monthly payment operates at the individual-course level.


Using the **$40,000 JD**:


**JD_COURSE_COST = $40,000 ÷ CONFIGURED_JD_COURSE_COUNT**


The JD course count is not currently configured. The calculator must not invent a JD per-course or monthly dollar amount.


For a course costing **$X**:


**MAXIMUM_MONTHLY_COURSE_PERIOD = 6 months**


**MONTHLY_COURSE_PAYMENT = $X ÷ 6**


**CURRENT_COURSE_COMPLETED = TRUE AND CURRENT_COURSE_PAID_IN_FULL = TRUE → NEXT_COURSE_UNLOCKED**


If either condition is false, the next course remains locked.


If the student does not complete the current course within the applicable enrollment period, the student may return to the same course, satisfy applicable remaining payment or re-enrollment requirements, complete it, and then proceed. An unpaid or incomplete course cannot be skipped.


### Per Course


Using the **$40,000 JD**:


**JD_PER_COURSE_TUITION = $40,000 ÷ CONFIGURED_JD_COURSE_COUNT**


Do not display an exact JD per-course amount until the JD course count is configured.


**Pay Course 1 → Course 1 Unlocks → Complete Course 1 → Pay Course 2 → Course 2 Unlocks → Repeat**


### Payment Safeguards


- Title IV uses the fixed Semester payment structure.
- Title IV students progress through fixed six-month semesters and fixed semester course sets.
- Non-Title-IV students may use Upfront, Monthly, or Per Course.
- Upfront courses unlock sequentially after completion without a new course payment.
- Monthly requires the current course to be both completed and paid in full before the next course unlocks.
- Per Course requires payment for the next course before that course unlocks.
- Monthly students may take up to six months to complete the currently enrolled course.
- Acceleration changes timing, not established total-program tuition.
- The calculator must not invent a JD course count or JD per-course amount until configured.