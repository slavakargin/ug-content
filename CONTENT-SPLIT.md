# UG website content split (stable vs dynamic)

This document defines the canonical home for each UG-program content block, to avoid duplication between:
- University-side site (stable pages): `ug-university-prototype` (renders `ug-content`)
- Department-side “current students hub” (dynamic pages): `ug-dept-prototype`

## Principles

1) **Canonical home is unique.** A topic has one canonical URL; the other site links to it.
2) **Catalog/requirements are never copied.** Use official catalog links via tokens:
   - {{BU_ACADEMIC_GUIDE_MATH_BA}}
   - {{BU_ACADEMIC_GUIDE_MATH_BS}}
3) **Stable = “evergreen.”** Definitions of tracks, broad descriptions, learning outcomes, teaching pathway description.
4) **Dynamic = “operational.”** Advising logistics, forms/petitions, planning sheets, deadlines, “how do I…”.
5) **Dept pages may summarize, but not duplicate.** Dept hub can give short “what to do next” guidance with a link to the stable university page for background.

## Canonical URLs (tokens)

- University UG landing: {{UNIV_UG_LANDING}}
- Dept “current students hub”: {{DEPT_CURRENT_STUDENTS_HUB}}

## Routing table

| Topic / Section | Canonical home | Where it lives (repo/path) | Other site behavior | Update cadence | Owner |
|---|---|---|---|---|---|
| UG landing / navigation | University (stable) | `ug-content` (rendered by university prototype) | Dept hub links to {{UNIV_UG_LANDING}} | rare | UG Program |
| Program overview | University (stable) | `overview/ug-program.md` | Dept hub links (no copy) | rare | UG Program |
| Learning outcomes | University (stable) | `overview/learning-outcomes.md` | Dept hub links (no copy) | rare | UG Program |
| Mathematics track description (BA/BS) | University (stable) | `tracks/pure-math.md` | Dept hub links (no copy) | rare | UG Program |
| Actuarial track description (BA/BS) | University (stable) | `tracks/actuarial.md` | Dept hub links (no copy) | rare | UG Program |
| Data Science & Statistics track description (BA/BS) | University (stable) | `tracks/data-science.md` | Dept hub links (no copy) | rare | UG Program |
| FAQ (conceptual, evergreen) | University (stable) | `policies/faq.md` | Dept hub links; may add “operational FAQ” separately | occasional | UG Program |
| Grading minimums / progression (if stable) | University (stable) | `policies/grading-minimums.md` | Dept hub links | occasional | UG Program |
| Advising: who/where/how to get advising | Dept hub (dynamic) | `ug-dept-prototype/docs/current-students/advising.md` | University site links to {{DEPT_CURRENT_STUDENTS_HUB}} | semesterly | UG Program |
| Forms & petitions (prereq, substitutions, transfer eval) | Dept hub (dynamic) | `.../current-students/forms.md` | University site links to dept hub | semesterly | UG Program |
| Degree planning logistics (how to plan, sequencing guidance) | Dept hub (dynamic) | `.../current-students/degree-planning.md` | University site links to dept hub | semesterly | UG Program |
| Sample plans / planning sheets | Dept hub (dynamic) | same as above; link out to Harpur templates {{BU_HARPUR_MAJOR_MINOR_ADVISING_TEMPLATES}} | University site links (no local copies) | annual/semesterly | UG Program + Harpur |
| Catalog degree requirements | University-external | tokens only (no content copy) | both sites link to catalog tokens | annual (check) | UG Program |
| Research opportunities (evergreen description) | University (stable) | add short block in overview or FAQ | both sites may link to dept research areas {{DEPT_WWW2_RESEARCH_AREAS}} | rare | UG Program |
| Student org links (Math Club, AWM) | University (stable) | short block (links only) | dept hub may also link (links only) | occasional | UG Program |
| Teaching pathway description | University (stable) | add short block + links | dept hub may link | rare | UG Program |
| Teaching pathway operational advice (if any) | Dept hub (dynamic) | optional future page | university links to dept hub | occasional | UG Program |

## Notes / decisions

- The dept hub should not re-host track descriptions; it should link to the stable university pages.
- “Production” university URLs are TBD; prototypes use the `prototype:` URLs in the registry for now.
- Anything that becomes “too operational” (office hours, deadlines, forms) moves to dept hub.
