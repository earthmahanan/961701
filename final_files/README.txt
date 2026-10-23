Ping River Health Network: synthetic data for the 961701 final exam
All records are fabricated; no real patients.

patients.csv    9,400 registered patients (9,000 type 2, 250 type 1, 150 gestational), snapshot 15 Oct 2026
reviews.csv     37,000+ annual review visits, 2020-2025 (includes 40 duplicate entries and the 2024 pilot arms)
admissions.csv  hospital admissions 2020 - Sep 2026; source = network or claims
                (claims arrive up to 90 days late, so recent claims are missing)

Outcome codes (serious complication admission): icd10_main E11.0, E11.1 (hyperglycaemic crisis),
E11.5 (foot ulcer/infection; icd10_other Z89.4 = amputation), E11.6 + E16.0 (severe hypoglycaemia).
About 6% of diabetic-foot admissions are coded L03.1 or L97 without a diabetes code.
Test period check: type 2 index visits Jan-Jun 2025 = 4,809; 12-month complication rate = 16.0%.
Regenerate: python gen_data.py --out <folder>   (seed 961701, b0 -2.84)
