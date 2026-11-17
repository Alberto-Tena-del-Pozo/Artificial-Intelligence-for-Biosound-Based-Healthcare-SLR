# Prompt — Conservative Audit of an Existing SLR Data-Extraction Matrix

You are auditing a completed systematic literature review (SLR) data-extraction matrix. Assess whether each existing field value is supported by the supplied evidence under the extraction rules. Retain values that meet those rules, even when another interpretation or wording would also be defensible.

## Inputs

For each article, I will provide:

1. The extraction rules relevant to the SLR.
2. The existing row from the completed data-extraction matrix.
3. The excerpts/annotations from the original article.

Use the supplied excerpts and annotations as the evidence for the audit. Apply the extraction rules as provided.

## Field-level verdicts

Assign exactly one verdict to each field in the existing row:

- **CORRECT:** The supplied evidence supports the existing value, or the value is reasonably defensible under the extraction rules. Retain it. A plausible alternative interpretation alone does not warrant review.
- **INCORRECT:** The supplied evidence clearly contradicts the value, establishes that it fails to meet an applicable extraction rule, or confirms a material inconsistency with another field. Explain the issue and recommend a correction when the evidence supports a specific replacement.
- **NEEDS REVIEW:** The supplied excerpts or annotations are incomplete, ambiguous or conflicting in a way that prevents a reliable verdict. State what evidence is needed and retain the existing value pending verification. Absence of evidence in the supplied excerpts does not establish absence from the article.

Audit every field in the row, including empty fields and values such as “Not reported”, using the same rules. For a **CORRECT** field, the verdict alone is sufficient. For **INCORRECT** or **NEEDS REVIEW**, give a brief reason and identify the relevant excerpt, annotation or source location when available.

## Checks to prioritise

- **Architecture and deployment.** Check consistency across computational workflow, infrastructure, deployment strategy, deployment maturity, real-time capability and privacy mechanisms. Distinguish what the authors proposed from what they implemented or demonstrated. Identify the field responsible for an inconsistency when the evidence allows it. Use **NEEDS REVIEW** for the affected fields if the supplied evidence does not establish which value is wrong.
- **Results and validation.** Check that numerical values match the evidence and refer to the stated task, cohort or experimental condition. Verify the reported validation strategies and distinguish subject-independent evaluation from recording-level splits. For computational results, check what the runtime or resource metric actually measures.
- **Scope of corrections.** Recommend changes for substantiated extraction errors. Preserve defensible values when differences concern wording, terminology, level of detail or another plausible interpretation. Request additional metrics only when the extraction rules require them.

## Output format

## [First author et al., year]

### Field-by-field audit

| Field | Existing value | Verdict | Evidence or verification needed |
|---|---|---|---|
| [Field name] | [Value as recorded] | [CORRECT / INCORRECT / NEEDS REVIEW] | [Leave blank for CORRECT. Otherwise, give the reason and source location or specify what to verify.] |

### Required corrections

For each **INCORRECT** field, report:

- **Field:** [Field name]
- **Current value:** [Value as recorded]
- **Recommended value:** [Evidence-supported replacement, or “To be verified” if the error is clear but the replacement cannot be established]
- **Reason:** [Brief explanation grounded in the supplied evidence and extraction rules]

If no errors are confirmed, write **No confirmed corrections.**

### Overall verdict

Choose one verdict based on the field-level findings:

- **PASS** if every field is **CORRECT**.
- **REVIEW REQUIRED** if at least one field **NEEDS REVIEW** and no field is **INCORRECT**.
- **CORRECTION REQUIRED** if at least one field is **INCORRECT**. List any fields that also **NEED REVIEW** separately.

Report the number of fields in each category and state the action to take before finalising the row.
