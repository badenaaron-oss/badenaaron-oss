# Aaron Baden

AI workflow architecture projects exploring safe AI integration into operational systems.

---
## AI Insurance Workflow Architecture

This architecture separates AI agents from deterministic decision logic using a sanitation and validation safety layer.

### Legend

🟨 **AI Agents** — LLM-based workflow components  
🟩 **Safety Layer** — input sanitation and structured data validation  
🟦 **Deterministic Systems** — rule-based coverage decision logic  


```mermaid
flowchart TD

A[Policyholder Inquiry]

subgraph AI Agents
B[AI Claim Intake Assistant]
C[🚦 Claim Workflow Orchestrator]
D[Coverage Explanation Assistant]
end

subgraph Safety Layer
E[Input Sanitation + Validation]
F[Structured Claim Data]
end

subgraph Deterministic Decision Layer
G[Coverage Decision Engine]
H[Structured Decision Output]
end

subgraph Customer Communication
I[PHONE_SCRIPT]
J[EMAIL_RESPONSE]
K[INTERNAL_SUMMARY]
end

A --> B
B --> E
E --> F
F --> C
C --> G
G --> H
H --> D
D --> I
D --> J
D --> K

%% styling

classDef ai fill:#ffe599,stroke:#333,stroke-width:2px
classDef safety fill:#d9ead3,stroke:#333,stroke-width:2px
classDef decision fill:#cfe2f3,stroke:#333,stroke-width:2px

class B,C,D ai
class E,F safety
class G,H decision
```
## Projects

### AI Claim Intake Assistant
Collects claim information, sanitizes inputs, and produces structured claim data.

### AI Claim Workflow Orchestrator
Routs insurance claim cases through intake, validation, decision, and communication systems.

### Coverage Explanation Assistant
Transforms structured coverage decisions into compliant customer explanations.
