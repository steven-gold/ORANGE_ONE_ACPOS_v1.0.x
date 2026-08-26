# AI EXECUTION ORDER

Execution sequence:

1. Read single authority master.
2. Apply `AUTHORITY_FILE_CLEANUP_REGISTRY.yaml` replacement / deprecation rules.
3. Resolve the active Page UID from `PAGE_UID_MASTER_REGISTRY.yaml`.
4. Resolve current unit identity from `ACPOS_UNIT_REGISTRY.yaml`; reject legacy units marked replaced for active rendering.
5. Validate page contract definitions and Authority Priority.
6. Load Global Shell template and page-specific layout authority.
7. If the page uses AI Conversation, load AI Core Registry → Shared AI Conversation Interface Authority → unit-specific conversation extension.
8. Build interface structure only from registered components / controls / states / visual mappings.
9. Bind backend and data contracts.
10. Implement runtime.
11. Execute QA validation and render validation.

## Stop conditions

Stop and report instead of guessing when:
- a required authority source is missing;
- a route or navigation level is unresolved;
- a legacy definition conflicts with an active replacement;
- a UI element has no Component / Control / Action / State / Permission / source trace;
- pixel-exact geometry has not been authorized;
- live API / DB / Runtime evidence is required but unavailable.

Do not create parallel specifications.
