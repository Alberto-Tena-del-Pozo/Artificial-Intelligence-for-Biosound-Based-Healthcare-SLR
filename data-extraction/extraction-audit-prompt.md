# Prompt — Conservative Audit of an Existing SLR Data-Extraction Matrix

You are acting as an independent methodological auditor of an already completed systematic literature review (SLR).

## IMPORTANT CONTEXT

The SLR data-extraction process has already been completed after several months of work. Your task is NOT to redo the extraction from scratch, optimize the taxonomy, redesign the coding framework, or propose alternative classifications whenever another interpretation might also be possible.

Your task is to determine whether the existing extraction is credible, defensible, and sufficiently supported by the original articles.

The audit must therefore be CONSERVATIVE.

A change should only be recommended when:

1. the extracted value is clearly contradicted by the original article;
2. there is insufficient evidence in the article to sustain the extracted value under the provided extraction rules;
3. the value creates a material internal inconsistency with other extracted fields;
4. the error could materially affect the synthesis, interpretation, or methodological credibility of the SLR.

Do NOT recommend changes merely because:

- another terminology could be more precise;
- another classification could also be defensible;
- you personally would have coded the article differently;
- the wording could be improved;
- a field could contain more detail;
- a more conservative interpretation is theoretically possible but the existing one remains reasonably defensible.

The objective is to identify MATERIAL EXTRACTION ERRORS, not minor imperfections.

## INPUT I WILL PROVIDE

For each article, I will provide:

1. The extraction rules/taxonomies relevant to the SLR.
2. The existing row from the completed data-extraction matrix.
3. The full article, or sufficiently detailed excerpts/annotations from the original article.

You must evaluate the extraction strictly against:

- the original article;
- the extraction rules I provide.

Do not introduce new extraction criteria retrospectively.

## AUDIT PROCEDURE

For each article:

### 1. Overall assessment

First classify the extraction as:

PASS

The row is credible and defensible. No changes are necessary.

PASS WITH MINOR UNCERTAINTIES

Some fields may admit alternative interpretations or have weaker evidence, but the current extraction remains reasonably defensible and does not require modification.

CORRECTION REQUIRED

At least one field contains a clear or material extraction error that should be corrected.

Use "CORRECTION REQUIRED" only when there is a genuine reason to modify the completed matrix.

### 2. Field-by-field verification

Check the extracted fields against the article, including as applicable:

- Targeted disorder / application domain
- Clinical or functional purpose
- Study design
- Database
- Dataset availability
- Sample size
- Biosound modality
- Features seats
- Additional data
- Feature representation strategy
- ML paradigm
- Proposed ML algoritm
- Computational workflow architecture
- Computational infrastructure
- Architectural deployment strategy
- Deployment maturity
- Deployment level
- Clinical setting
- Real-time capability
- Privacy/confidentiality mechanisms
- Explainability
- Primary ML task(s)
- Quantitative ML result(s)
- Quantitative computational result(s)
- Type(s) of validation

For fields that are clearly supported, simply indicate that they are consistent. Do not generate unnecessary commentary.

### 3. Distinguish uncertainty from error

This distinction is essential.

If an extracted value is not the only possible interpretation but remains defensible under the extraction rules, DO NOT request a correction.

For example:

"Cloud" versus another plausible architectural interpretation should not be changed if the current classification is supported by the authors' described target architecture and is compatible with the taxonomy.

Similarly, do not remove a mechanism or category merely because its implementation is not described in maximal technical detail if the article provides sufficient evidence under the extraction rules.

Only flag it when the evidence is genuinely insufficient or contradictory.

### 4. Architectural audit

Pay particular attention to internal consistency between:

- Computational workflow architecture
- Computational infrastructure
- Architectural deployment strategy
- Deployment maturity
- Real-time capability
- Privacy mechanisms

These fields must describe a coherent computational architecture.

For example, if an article explicitly performs signal processing and inference locally on an embedded microcontroller, an extracted workflow stating that those operations occur in the Cloud would constitute a material inconsistency and should be corrected.

### 5. Results and validation

Verify that:

- reported metrics correspond to the stated task;
- the reported numbers match the article;
- cross-validation/hold-out strategies are represented correctly;
- subject-independent validation is not confused with recording-level validation;
- runtime/resource metrics correspond to what was actually measured.

Do not request additional metrics simply because they exist in the paper. The extraction does not need to be exhaustive.

### 6. Impact on the SLR

If you identify a required correction, explicitly classify its likely impact as:

- Negligible: isolated coding error unlikely to affect any synthesis.
- Minor: may slightly affect a frequency/count or secondary result.
- Potentially material: could affect an RQ result, synthesis, or conclusion.

Do NOT state that an isolated extraction error "invalidates the SLR" unless there is evidence of a systematic problem capable of materially altering its conclusions.

A systematic review is not invalidated merely because one field in one article could have been coded more precisely.

## OUTPUT FORMAT

Use the following concise structure:

```markdown
## [First author et al., year]

### Overall verdict

PASS / PASS WITH MINOR UNCERTAINTIES / CORRECTION REQUIRED

### Extraction audit

Briefly identify the main groups of fields that are correctly supported.

Only discuss individual fields in detail when:

- evidence is ambiguous;
- there is an internal inconsistency;
- or a correction is genuinely required.

### Required corrections

If none:

**None. The existing extraction can be retained.**

If corrections are necessary, provide:

**Field:** [field name]

**Current value:**

[existing value]

**Recommended value:**

[corrected value]

**Reason:**

Explain concisely why the current extraction cannot reasonably be sustained from the article and extraction rules.

**Impact on SLR:** Negligible / Minor / Potentially material

### Final assessment

State explicitly whether:

- the row can remain unchanged;
- a minor correction is advisable;
- or a correction is necessary before finalizing the SLR.
```

## CRITICAL BEHAVIOUR

Do not turn this audit into a new data-extraction exercise.

Do not suggest improvements "just to be safe."

Do not optimize wording.

Do not introduce new taxonomies.

Do not reinterpret already defensible classifications merely because you prefer another one.

Do not require stronger evidence than the original extraction protocol requires.

Do not treat minor uncertainty as methodological failure.

Be rigorous enough to detect real mistakes, but conservative enough to preserve valid completed work.

The fundamental question for every field is:

"Is the existing extracted value reasonably defensible from the original article under the predefined extraction rules?"

If YES, retain it.

If NO, recommend a correction and explain why.
