# godui UI profile

Companion to the [adoption entry](UNNDEV-UI-STANDARDS.md) and [shared core](UNNDEV-UI-STANDARDS-CORE.md).

## Applicable surfaces

WEB + TOUCH for reusable components, documentation and Storybook; EDITOR only where a consuming surface requires it.

## Local authority and preservation

- [Agent rules](../AGENTS.md) and [contribution guidance](../CONTRIBUTING.md) preserve the component workflow and required skills.
- [Component source](../packages/components/src/), [theme](../packages/components/theme/) and [registry](../registry.json) remain the local owners. Keep Tailwind utilities static and use named semantic tokens and the existing z-index scale.
- Preserve the no-new-component-CSS rule, per-component animation registration, hand-maintained registry entries and the local OKLCH / gamut handling rules. The shared standard does not replace those requirements.
- Component changes still require source, type exports, registry entry, Storybook coverage, tests and categorized docs. Do not add a second component implementation merely to demonstrate a shared rule.
- Verify accessible names, interaction and state in actual component examples; a registry build or successful render alone is not an accessibility audit.

## Verification

Before committing, the existing rules require pnpm check and pnpm test. Registry/component changes additionally require pnpm build:registry. This documentation adoption changes neither component code nor the registry.

For each future implementation, record the affected states and input methods, relevant core rule IDs, focused checks and manual evidence. Documentation installation alone establishes neither runtime compliance nor completion of the existing release gates.

## Exceptions

No new exception is granted by this profile. Keep named existing local exceptions with their governing source. Any new exception must identify the rule ID, bounded surface, reason, owner, compensating behavior, verification and review date. Escalate unresolved conflicts before implementation.
