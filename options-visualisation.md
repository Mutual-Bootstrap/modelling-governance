# Option Assessment Visualisation Patterns

## Purpose

To provide a reusable set of visualisation patterns for comparing strategic options where multiple trade-offs exist and no option is universally superior.

These patterns are intended for executive decision support, architecture strategy discussions, operating model design, sourcing decisions and transformation planning.

---

## Context

Strategic decisions rarely involve choosing between a good option and a bad option.

More commonly, decision-makers are balancing competing concerns such as:

- Cost
- Risk
- Speed of delivery
- Scalability
- Organisational control
- Capability retention
- Operational resilience
- Transition complexity

Visualisation techniques help communicate these trade-offs without concealing uncertainty or oversimplifying the decision.

---

## Key Concepts

### Decision Dimensions

The criteria used to compare options.

Typical dimensions include:

- Cost
- Delivery Speed
- Operational Risk
- Scalability
- Organisational Control
- Capability Retention
- Knowledge Transfer
- Feasibility
- Transition Complexity

Dimensions should remain relatively stable regardless of the options being assessed.

---

### Trade-off Surface

A visual representation of competing forces where improving one outcome often worsens another.

Examples include:

- Lower cost versus greater risk
- Greater control versus slower delivery
- Faster implementation versus knowledge retention

Most strategic decisions are trade-off decisions rather than optimisation exercises.

---

### Comparative Visualisation

A method of comparing multiple options simultaneously using a common set of dimensions.

Good comparative visualisations:

- make trade-offs visible;
- support discussion;
- avoid suggesting false precision.

---

## Relationships

### Option → Decision Dimensions

Each option should be assessed against the same evaluation dimensions.

```text
Option
    ↓
Cost
Risk
Scalability
Control
Speed
```

Consistency of assessment is more important than precision.

---

### Dimensions → Trade-offs

Dimensions frequently conflict.

Examples:

```text
Scalability ↑
        ↓
Cost ↑
```

```text
Control ↑
        ↓
Speed ↓
```

Explicitly showing trade-offs improves decision quality.

---

### Visualisation → Decision Support

Different visualisation methods suit different audiences and purposes.

The choice of visualisation influences the nature of the subsequent discussion.

---

## Architecture Implications

### Visualisations Are Decision Tools

The objective is not visual appeal.

The objective is to accelerate understanding and improve strategic decisions.

---

### Avoid False Precision

Assigning values such as:

```text
Risk = 7.2
Scalability = 8.3
```

creates an illusion of certainty.

Executive audiences are usually better served by comparative positioning than by manufactured precision.

---

### Optimise for Discussion

The best visualisation frequently depends on the discussion that needs to occur rather than the underlying data.

If the likely debate concerns trade-offs, choose a format that exposes trade-offs.

---

### Multiple Views May Be Appropriate

No single visualisation serves every audience equally well.

An executive briefing may use one visualisation while supporting material uses another.

---

## Visualisation Patterns

### 1. Quadrant Model

Represents options against two dominant dimensions.

Common examples:

```text
Risk versus Cost
Risk versus Benefit
Control versus Delivery Speed
```

#### Advantages

- Extremely easy to interpret.
- Well understood by senior audiences.
- Highlights strategic positioning.

#### Limitations

- Only supports two dimensions.
- Can oversimplify complex decisions.

#### Best Used When

A single trade-off dominates the discussion.

---

### 1a. Bubble Chart

Extends the quadrant model by introducing additional dimensions.

Typical mapping:

```text
X-axis     = Cost
Y-axis     = Risk
Bubble Size = Scalability
Colour      = Organisational Control
```

#### Advantages

- Maintains executive readability.
- Communicates multiple dimensions simultaneously.
- Highlights relative positioning.

#### Limitations

- Requires careful explanation.
- Bubble size interpretation can vary.

#### Best Used When

Multiple dimensions matter but a simple executive view is still required.

---

### 2. Radar Chart

Plots options across a common set of dimensions.

Example dimensions:

- Cost
- Speed of Delivery
- Organisational Control
- Knowledge Retention
- Scalability
- Operational Risk

#### Advantages

- Displays multiple characteristics simultaneously.
- Makes strengths and weaknesses visible.
- Easy to generate in common reporting tools.

#### Limitations

- Interpretation varies between audiences.
- Comparative areas can be misleading.
- Some stakeholders struggle to evaluate overlapping shapes.

#### Best Used When

The audience is comfortable with analytical visualisations and many dimensions must be shown simultaneously.

---

### 3. Heatmap Assessment Matrix

Represents options as coloured ratings against evaluation dimensions.

Example:

| Dimension | Option A | Option B | Option C |
|------------|------------|------------|------------|
| Cost | Green | Amber | Red |
| Risk | Red | Amber | Green |
| Scalability | Red | Amber | Green |

#### Advantages

- Familiar to most stakeholders.
- Easy to understand.
- Supports structured discussion.

#### Limitations

- Can lead to arguments about individual ratings.
- Encourages focus on cell-level detail.
- Colour boundaries can be subjective.

#### Best Used When

Transparency and auditability are more important than narrative simplicity.

---

### 4. Comparative Scales

Represents options positioned on a series of one-dimensional scales.

Example:

```text
Low Risk  ────── Option A ─── Option B ───────── Option C ───── High Risk

Low Cost  ─────────────────── Option A ─────── Option B ────── Option C
```

#### Advantages

- Very intuitive.
- Avoids the complexity of radar charts.
- Makes trade-offs explicit.

#### Limitations

- Requires multiple scales.
- Less visually compact.

#### Best Used When

Executive audiences need clarity without reducing assessment to simplistic colour coding.

---

## Risks and Limitations

### Visual Bias

The selected visualisation may unintentionally favour one option.

Care should be taken to ensure the presentation method is not driving the decision.

---

### Reductionism

Complex organisational decisions cannot be fully represented through a small number of dimensions.

Visualisations support decision-making; they do not replace judgement.

---

### Subjective Scoring

Some methods require ratings or positions to be assigned.

These assessments should be supported by evidence wherever possible.

---

### Overconfidence

Detailed charts may imply a level of certainty that does not exist.

The presence of a visual model should not be confused with the existence of objective truth.

---

## References

### Typical Strategic Decision Dimensions

- Cost
- Speed of Delivery
- Organisational Control
- Knowledge Retention
- Scalability
- Operational Risk
- Feasibility
- Transition Complexity

### Pattern Selection Guide

| Need | Recommended Pattern |
|--------|--------|
| Quick executive comparison | Quadrant Model |
| Multi-dimensional executive discussion | Bubble Chart |
| Analytical comparison | Radar Chart |
| Governance and challenge process | Heatmap Matrix |
| Clear trade-off discussion | Comparative Scales |

### General Rule

If stakeholders are likely to debate individual scores, a Heatmap Matrix provides transparency.

If stakeholders are likely to debate overall direction, a Bubble Chart or Quadrant Model is generally more effective.
