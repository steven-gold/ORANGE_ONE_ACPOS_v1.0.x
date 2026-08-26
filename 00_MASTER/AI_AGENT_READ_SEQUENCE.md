# AI Agent Read Sequence

1. Read `00_MASTER/AUTHORITY/SOURCE_AUTHORITY.md`.
2. Read `00_MASTER/ACPOS_AI_SEQUENCED_SINGLE_AUTHORITY_CONSTRUCTION_PACKAGE/ACPOS_SINGLE_AUTHORITY_CONSTRUCTION_MASTER_AI_SEQUENCED_FINAL.yaml`.
3. Read `00_MASTER/AUTHORITY_FILE_CLEANUP_REGISTRY.yaml` before consuming any legacy registry or historical construction record.
4. Read `00_MASTER/PAGE_UID_MASTER_REGISTRY.yaml` and resolve active Page UID / replacement mapping.
5. Read `00_MASTER/ACPOS_UNIT_REGISTRY.yaml` and reject legacy units marked REPLACED for active rendering.
6. Read current UI / Navigation / AI Core authorities required by the assigned page.
7. Validate the page contract and all source-trace dependencies.
8. Read page-specific Authority files in declared priority order.
9. Execute assigned scope only after conflict and replacement validation passes.

## Mandatory precedence rules

- `AUTHORITY_FILE_CLEANUP_REGISTRY.yaml` must be applied before `00_MASTER/REGISTRY/ACPOS_REGISTRY_RESTRUCTURED_COMPLETE.csv` or any other historical registry row is used.
- A legacy ID marked `REPLACED`, `REPLACED_AS_SEPARATE_PAGE`, or `active_render: false` must not create an active page.
- `GLOBAL-SHELL-001` is a template, not a Page UID and not a route.
- `L1-01 Dashboard` is the only ACPOS home page.
- For CORE, current active page authority is `ACPOS_AUTHORITY/CORE/CORE_PAGE_REGISTRY.yaml` and current Page UID is `CORE-01`.
- CORE-02 through CORE-06 historical definitions may be used only for audit/migration trace, not active UI construction.
- AI Conversation pages must read `AI_CORE_AUTHORITY_REGISTRY.yaml` and `AI_CONVERSATION_INTERFACE_AUTHORITY.yaml` before a unit-specific conversation extension.

No parallel conflicting authority is allowed. When conflict remains unresolved, stop construction and report the conflict instead of guessing.
