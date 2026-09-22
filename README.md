# Rafeeq Mini Labs · لابات رفيق المصغّر 

> **Advanced Agentic AI Systems Engineering**  
> A safe, auditable, and bilingual agentic operations system for delivery management.

---

##  About The Project / نبذة عن المشروع

**Rafeeq Mini** is a bilingual (Arabic/English) AI agentic operational assistant designed for a delivery company scenario. The system processes customer requests, verifies identity, retrieves context-aware policies, routes tasks to specialized agents, and executes operations safely with deterministic guardrails and required human approval for high-value actions (e.g., refunds exceeding SAR 500).

---

##  System Architecture & Agentic Flow / المخطط الهيكلي

```mermaid
flowgraph TD
    A[Bilingual Request / طلب ثنائي اللغة] --> B[Input Guard / حارس المدخلات]
    B --> C[Thin Supervisor / المنسق الخفيف]
    C --> D[OrdersAgent]
    C --> E[RefundAgent]
    E --> F[Policy + Approval / السياسة والموافقة]
    D --> G[MCP Tools + Scoped Data / أدوات وبيانات مقيدة]
    F --> G
    G --> H[Redacted Trace + Evidence / أثر منقح وأدلة]
```

---

## 🗓️ Three-Day Build Journey / مراحل البناء

| Day | Scope & Artifacts | Gate |
|---|---|---|
| **Day 1: Core & Tools** | Typed state, bounded graph, ReAct logic, safe local tools, and MCP stdio connection. | `C9_DAY1_GATE` ✅ |
| **Day 2: Memory & Orchestration** | Session memory, customer-scoped recall, active policy retrieval, specialist agents, and human approval interrupts. | `C20_DAY2_GATE` ✅ |
| **Day 3: Security & Evidence** | Threat model testing, guard repairs, bounded reflection, traces, evaluation metrics, and safe export package. | `C29_EXPORT_SAFETY_CHECK` ✅ |

---

##  Key Safety & Security Features / معايير الأمان

* **Bilingual Execution:** Native handling of Arabic and English operational prompts.
* **Deterministic Guardrails:** Input validation and prompt injection attack mitigation.
* **Human-in-the-Loop:** Automatic pause (`interrupt`) requesting human approval for refund requests $> SAR 500$.
* **Data Isolation:** Session-scoped memory and strict customer-scoped data access.
* **Auditability:** Complete JSONL traces, security scorecards, and evidence logs.

---

##  How to Run / طريقة التشغيل

1. Open the complete notebook in Google Colab: `notebooks/Rafeeq_Mini_Capstone.ipynb`.
2. Execute all cells sequentially from environment check (`C0`) to export (`C29`).
3. View generated assessment artifacts under the `reports/` directory.

---

---

*Prepared by **Areej Almutairi** for the Advanced Agentic AI Systems Engineering Program in collaboration with [SDAIA Academy](https://github.com/SDAIAAcademy).*
