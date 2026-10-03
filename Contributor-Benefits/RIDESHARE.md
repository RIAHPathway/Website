---
document_type: contributor-benefit-framework
track: "Rideshare Ambassador"
status: "In Progress — Review and Finalization Required"
benefit_system: "RIAH Pathway"
flow_status: "draft-review"
---

# 🚗 Rideshare Ambassadors

**Status: In Progress — Review and Finalization Required**

## 💰 Tuition, Products & Pricing Resources

Contributor benefits in this documentation apply to **eligible tuition and eligible products** according to the rules for the applicable participant category.

| Pricing Resource | Purpose |
|---|---|
| 💰 [RIAH Pathway Master Pricing Data Sheet](../RIAH-Pathway-Master-Pricing-Data-Sheet.md) | Review current pathway tuition, program pricing, product pricing and other applicable pricing data. |
| 🧮 [RIAH Pathway Pricing Engine](../RIAH-Pathway-Pricing-Engine.md) | Review the pricing rules and calculation framework used to connect applicable pricing, eligibility, discounts and benefits. |

> **Pricing Calculator Development:** The interactive RIAH Pathway pricing calculator is still being developed. The intended calculator experience will allow eligible participants to apply their verified points and applicable benefit percentage to eligible tuition and product pricing so they can estimate what they may pay. Until that calculator is finalized, use the Master Pricing Data Sheet and Pricing Engine together with the applicable benefit rules in this documentation.

```mermaid
flowchart TB
    A["👤 Eligible Participant"] --> B["⭐ Earn & Verify Applicable Points"]
    B --> C["🏆 Determine Applicable Benefit Percentage"]
    C --> D{"💰 Apply Benefit To"}
    D --> E["🎓 Eligible Tuition"]
    D --> F["🛍️ Eligible Products"]
    E --> G["📊 Review Master Pricing Data Sheet"]
    F --> G
    G --> H["🧮 Apply Pricing Engine Rules"]
    H --> I["💵 Estimate Applicable Tuition & Product Cost"]
    I --> J["🚧 Interactive Pricing Calculator — In Development"]
```

## 📑 Index

I. 🚗 Category Key  
II. 🚗 End-to-End Category Flow  
III. ⚙️ Flow Metadata  
IV. 👑 General Eligibility  
V. 🧮 Benefit Formula  
VI. ⭐ Rideshare Point System  
VII. 🎪 Events, Workshops and Outreach  
VIII. 🔗 QR Codes, Referral Links and Attribution  
IX. 🏆 1%–25% Milestones  
X. 👥 Benefit Levels  
XI. 🔗 Referral and Conversion Milestones  
XII. 🛡️ Verification and Anti-Abuse  
XIII. ⏳ Status Workflow  
XIV. 📋 Participant Ledger

## I. 🚗 Category Key
| Emoji | Meaning |
|---|---|
| 🚗 | Rideshare Ambassador |
| 👑 | Approved eligibility or contribution |
| ⭐ | Approved points |
| 🏆 | Completed milestone |
| 🎓 | Tuition benefit |
| 🛍️ | Product benefit |
| 🔗 | QR, referral, routing or attribution |
| 🎪 | Event, workshop or outreach |
| 🎥 | Webinar, presentation, video or media |
| 👀 | Under review |
| 🔄 | Revision or re-verification |
| ✅ | Approved or verified |
| ❌ | Rejected or ineligible |

## II. 🚗 End-to-End Category Flow
```mermaid
flowchart TB
A["🚗 Rideshare Ambassador"] --> B["👑 Eligibility, Orientation & Marketing Training"]
B --> C["🚘 Approved Vehicle Branding"]
C --> D["🪑 Seat Covers + 📱 Back-Seat Display + 🔗 QR Code"]
D --> E["📄 Brochures, Flyers, Business / Information Cards"]
E --> F["👤 Passenger Chooses to Engage"]
F --> G["🔗 Website, Webinar, Program, Application or Product Destination"]
G --> H{"🎯 Verified Outcome?"}
H --> I["🔗 Qualified Referral +10"]
H --> J["🎥 Webinar Attendance +15"]
H --> K["📝 Application +25"]
H --> L["🎓+ Enrollment +100"]
H --> M["🛒 Product Purchase +25"]
I --> N["📋 Verification & Activity Ledger"]
J --> N
K --> N
L --> N
M --> N
N --> O["⭐ Approved Points"]
O --> P{"🏆 Complete 100-Point Milestone?"}
P -- No --> Q["⭐ Carry Points Forward"]
P -- Yes --> R["🎓 +1% Tuition & 🛍️ +1% Products"]
R --> S{"👑 2,500 Points?"}
S -- No --> C
S -- Yes --> T["👑🏆 25% Tuition + 25% Products Maximum"]
```

## III. ⚙️ Flow Metadata
```yaml
track: "Rideshare Ambassador"
profile_category: "Rideshare Ambassador"
status: "in-progress"
verification_required: true
points_require_approval: true
benefit_record_required: true
review_state:
  - pending
  - under-review
  - revision-if-required
  - approved
  - credited
```

Eligible Rideshare contributions may include approved RIAH vehicle vinyl, vehicle branding, branded seat covers, back-seat tablets or digital displays presenting approved RIAH content and the RIAH Pathway website, passenger-accessible QR codes, brochures, flyers, business or information cards, Education Pathway information, Experiential information, certification information, product information, webinar information, unique referral links, community events, booths, approved campaigns, qualified referrals, student conversions and product conversions.

## IV. 👑 General Eligibility
Participants must maintain an identifiable profile; use assigned participant, Ambassador, referral or contributor identifiers when required; follow program instructions; use approved RIAH Pathway branding and current marketing materials; accurately represent programs, products, services and pathways; never make unauthorized promises regarding admission, accreditation, authorization, financial aid, employment, certification, licensure or educational outcomes; follow applicable school, employer, venue, platform and property requirements; obtain required permissions; submit evidence for point-bearing activity; use assigned QR codes and referral links where required; protect student, prospect, customer, employee and organizational information; never fabricate activity or conversions; complete required training; follow applicable RIAH policies; and receive verification before points become permanent.

Materials must be used appropriately, comply with applicable platform and vehicle requirements, not interfere with passenger safety, and not create unwanted pressure on passengers.

## V. 🧮 Benefit Formula
**100 approved points = 1% eligible tuition + 1% eligible products.** Maximum: **2,500 points = 25% tuition + 25% products**.

## VI. ⭐ Rideshare Point System
| Activity | Points |
|---|---:|
| Complete Ambassador orientation | 25 |
| Complete marketing training | 25 |
| Install approved vehicle vinyl | 50 |
| Install approved branded seat-cover package | 25 |
| Install approved back-seat digital display | 25 |
| Maintain approved vehicle marketing kit | 15 |
| Display active assigned QR code | 10 |
| Maintain assigned referral link | 10 |
| Attend approved community event | 25 |
| Staff approved booth | 50 |
| Complete approved outreach campaign | 25 |
| Qualified referral | 10 |
| Referral attends educational webinar | 15 |
| Referral completes application | 25 |
| Verified referral becomes enrolled student | 100 |
| Verified referred product purchase | 25 |
| Coordinate approved community event | 75 |
| Host approved information session | 50 |
| Major approved Ambassador campaign | 100–200 |

Installation points are normally awarded once for the approved installation.

## VII. 🎪 Events, Workshops and Outreach
Eligible activities may include college fairs, career fairs, community festivals, education fairs, school district events, parent information events, workforce events, career-development workshops, college-readiness events, professional-development events, community-center events, library events, approved school events, virtual information sessions, educational webinars, certification workshops, career workshops and Experiential pathway sessions.

| Event Contribution | Points |
|---|---:|
| Attend and support | 25 |
| Staff booth or table | 50 |
| Present approved session | 50 |
| Coordinate event participation | 75 |
| Organize approved RIAH workshop | 75 |
| Lead major approved event | 100 |
| Coordinate major multi-partner event | 150–200 |

Multiple event awards require genuinely separate responsibilities.
## VIII. 🔗 QR Codes, Referral Links and Attribution
Each applicable Ambassador uses an individually attributable QR code and referral link. Approved destinations may include the RIAH Pathway website, program pages, educational webinars, application pages, event registration, product pages, information-request forms and approved landing pages.

**Ambassador → QR or Link → Engagement → Lead → Webinar → Application → Enrollment or Purchase**

Conversions must be traceable to the assigned identifier or otherwise verified. Self-referrals do not qualify. Duplicate referrals do not create duplicate conversion awards.
## IX. 🏆 1%–25% Milestones
| Points | Tuition | Products |
|---:|---:|---:|
| 100 | 1% | 1% |
| 200 | 2% | 2% |
| 300 | 3% | 3% |
| 400 | 4% | 4% |
| 500 | 5% | 5% |
| 600 | 6% | 6% |
| 700 | 7% | 7% |
| 800 | 8% | 8% |
| 900 | 9% | 9% |
| 1000 | 10% | 10% |
| 1100 | 11% | 11% |
| 1200 | 12% | 12% |
| 1300 | 13% | 13% |
| 1400 | 14% | 14% |
| 1500 | 15% | 15% |
| 1600 | 16% | 16% |
| 1700 | 17% | 17% |
| 1800 | 18% | 18% |
| 1900 | 19% | 19% |
| 2000 | 20% | 20% |
| 2100 | 21% | 21% |
| 2200 | 22% | 22% |
| 2300 | 23% | 23% |
| 2400 | 24% | 24% |
| 2500 | 25% MAX | 25% MAX |

Only complete 100-point thresholds increase the benefit. Remaining points carry forward. Participation may continue after 2,500 points, but these benefits remain capped at 25%.

## X. 👥 Benefit Levels
| Level | Points | Benefit |
|---|---:|---:|
| 🟢 Level I | 100–400 | 1%–4% |
| 🔵 Level II | 500–900 | 5%–9% |
| 🟣 Level III | 1,000–1,400 | 10%–14% |
| 🔴 Level IV | 1,500–1,900 | 15%–19% |
| 👑 Level V | 2,000–2,400 | 20%–24% |
| 👑🏆 Maximum | 2,500+ | 25% |

## XI. 🔗 Referral and Conversion Milestones
| Stage | Points |
|---|---:|
| Qualified Referral | 10 |
| Webinar or Information Session Attendance | +15 |
| Completed Application | +25 |
| Verified Enrollment | +100 |
| Verified Product Purchase | +25 |

A verified student completing the referral journey through enrollment may generate 150 points: 10 + 15 + 25 + 100.

## XII. 🛡️ Verification and Anti-Abuse
Verification may include activity records, event registration or check-in, appropriate event evidence, QR analytics, referral analytics, webinar registration, application attribution, enrollment attribution, product-order attribution, approved campaign records, GitHub records where applicable, and coordinator or maintainer approval.

No points are awarded for fake, duplicate or self-referrals; fake purchases; fraudulent transactions; fabricated events or attendance; QR manipulation; automated fake traffic; spam; plagiarism; duplicate submissions; unauthorized copyrighted material; fabricated testing or research; unauthorized school, vehicle or brand marketing; misleading program claims; pressure-based marketing; abandoned or rejected work; or restricted/confidential information.

One underlying activity normally receives one primary award unless separate point-bearing milestones or deliverables are independently verified.

## XIII. ⏳ Status Workflow
**⏳ Pending → 👀 Under Review → 🔄 Revision if Required → ✅ Approved → 👑 Credited**

Pending work receives no permanent points. Rejected work receives zero points.

## XIV. 📋 Participant Ledger
Record Participant, Participant ID, Track, Activity or Contribution ID, Activity, Attribution, Submission Date, Verification Source, Points, Approved By, Previous Total, Added Points, New Total, Milestone, Tuition Benefit, Product Benefit, Next Milestone, Points Remaining and Status.
