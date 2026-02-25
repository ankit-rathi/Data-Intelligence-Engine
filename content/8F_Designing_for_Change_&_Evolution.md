## F. Designing for Change & Evolution

### Why

Data systems decay. Business models change. Regulations shift.

Static architectures die.

### What

Designing for change means:

* Loose coupling
* Schema evolution
* Model retraining pipelines
* Flexible governance

### How

* Decouple storage, compute, serving layers
* Use versioned models and data
* Build retraining triggers
* Document assumptions explicitly

Every system should assume drift — technical and strategic.

---

From first principles, no environment is static. Customer behavior shifts, competitors innovate, regulations evolve, and data distributions drift. Any system built on fixed assumptions will eventually diverge from reality. When reality changes but architecture does not, performance degrades silently until failure becomes visible.

Data systems are especially vulnerable because they encode assumptions in schemas, models, and workflows. A credit model may assume income stability patterns from historical data. If macroeconomic conditions change, default behavior shifts. Without retraining, predictions become biased. The system continues operating, but decision quality deteriorates.

Designing for change begins with acknowledging inevitability. Loose coupling reduces fragility. When storage, compute, and serving layers are tightly integrated, modifying one component requires rewriting others. Decoupling allows individual components to evolve independently. For example, updating a model should not require redesigning the data ingestion pipeline.

Schema evolution addresses structural drift in data. New fields appear, definitions change, and sources expand. If schemas are rigid and undocumented, downstream systems break. Versioned schemas allow gradual migration without disrupting operations.

Model retraining pipelines institutionalize adaptation. Rather than manually retraining when performance drops dramatically, systems can monitor drift indicators — changes in input distribution or prediction error — and trigger retraining workflows automatically. This converts reactive repair into proactive maintenance.

Versioning models and datasets is critical for traceability. If performance changes, teams must know which version was deployed and what assumptions it encoded. Without version control, debugging becomes guesswork.

Flexible governance complements technical design. Regulatory requirements or internal risk policies may evolve. Systems should allow updating thresholds, audit rules, and approval flows without architectural overhaul.

Explicit documentation of assumptions provides cognitive resilience. When assumptions are hidden, teams forget what conditions the system depends on. When they are documented, deviations become easier to detect.

The overarching principle is to treat drift as normal, not exceptional. Technical drift (data changes), model drift (performance decay), and strategic drift (business model evolution) are constants. Systems that assume stability become brittle. Systems designed for adaptation remain durable.

Robust architecture is not defined by how well it performs today, but by how gracefully it evolves tomorrow.
