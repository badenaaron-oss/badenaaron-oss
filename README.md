# Aaron Baden

AI workflow architecture projects exploring safe AI integration into operational systems.

---

This architecture separates AI agents from deterministic decision logic using a sanitation and validation safety layer.

## AI Insurance Workflow Architecture

```mermaid
flowchart TD

A[Policyholder Inquiry]

subgraph AI Agents
B[AI Claim Intake Assistant]
G[Coverage Explanation Assistant]
end

subgraph Safety Layer
C[Input Sanitation + Validation]
D[Structured Claim Data]
end

subgraph Deterministic Decision Layer
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

%% styling

classDef ai fill:#ffe599,stroke:#333,stroke-width:2px
classDef safety fill:#d9ead3,stroke:#333,stroke-width:2px
classDef decision fill:#cfe2f3,stroke:#333,stroke-width:2px

class B,G ai
class C,D safety
class E,F decision
```
## Projects

### AI Claim Intake Assistant
Collects claim information, sanitizes inputs, and produces structured claim data.

### Coverage Explanation Assistant
Transforms structured coverage decisions into compliant customer explanations.
