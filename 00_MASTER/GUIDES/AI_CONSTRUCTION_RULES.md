# AI Construction Rules

## Execution Order

1. Read authority YAML.
2. Confirm module scope.
3. Implement only approved scope.
4. Validate before next module.

## Prohibited

- Creating duplicate authority files.
- Replacing locked definitions without approval.
- Building empty placeholders as final implementation.

## Validation

Every module requires evidence across:
- Data model
- Backend contract
- Runtime
- Frontend
- Permissions
- QA
