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
E[🚦 Claim Workflow Orchestrator]
F[Coverage Explanation Assistant]
end

subgraph Safety Layer
C[Input Sanitation + Validation]
D[Structured Claim Data]
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

A -->|claim description| B
B -->|raw intake data| C
C -->|validated claim data| D
D -->|claim state| E

E -->|decision request| G
G -->|coverage decision| H

H -->|decision status + confidence| E

E -->|communication request| F

F -->|customer explanation| I
F -->|customer explanation| J
F -->|internal summary| K

%% styling

classDef ai fill:#ffe599,stroke:#333,stroke-width:2px
classDef orchestrator fill:#f6b26b,stroke:#333,stroke-width:4px
classDef safety fill:#d9ead3,stroke:#333,stroke-width:2px
classDef decision fill:#cfe2f3,stroke:#333,stroke-width:2px

class B,F ai
class E orchestrator
class C,D safety
class G,H decision
```
## Projects

### AI Claim Intake Assistant
Collects claim information, sanitizes inputs, and produces structured claim data.

### AI Claim Workflow Orchestrator
Routs insurance claim cases through intake, validation, decision, and communication systems.

### Coverage Explanation Assistant
Transforms structured coverage decisions into compliant customer explanations.
