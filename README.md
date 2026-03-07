# Aaron Baden

AI workflow architecture projects exploring safe AI integration into operational systems.

---

## AI Insurance Workflow Architecture

```mermaid
flowchart TD

A[Policyholder Inquiry]

subgraph AI Agents
B[AI Claim Intake Assistant]
G[Coverage Explanation Assistant]
end

subgraph Data Safety
C[Input Sanitation + Validation]
D[Structured Claim Data]
end

subgraph Decision Logic
E[Coverage Decision Engine]
F[Structured Decision Output]
end

subgraph Customer Communication
H[PHONE_SCRIPT]
I[EMAIL_RESPONSE]
J[INTERNAL_SUMMARY]
end

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
G --> I
G --> J
```

---

## Projects

### AI Claim Intake Assistant
Collects claim information, sanitizes inputs, and produces structured claim data.

### Coverage Explanation Assistant
Transforms structured coverage decisions into compliant customer explanations.
