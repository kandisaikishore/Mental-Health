# Development, Safety, and Privacy Guide

This is a mental-wellbeing application project. Confirm current features and integrations from source before describing them as implemented. The app should offer supportive information, not present itself as a diagnostic or emergency service unless an appropriately reviewed capability exists.

## Setup

```bash
git clone https://github.com/kandisaikishore/Mental-Health.git
cd Mental-Health
```

Use the runtime and scripts defined by the project manifests. Configure credentials locally and never commit real user records, API keys, or private conversations.

## Functional QA

For implemented workflows, test:
- Empty and malformed inputs
- Save, edit, and clear behavior for personal entries
- Loading, empty, success, and recoverable error states
- Keyboard navigation, accessible labels, and mobile layout
- Provider timeout and malformed responses if external services are integrated
- Session expiry and access control if accounts are supported

## Privacy expectations

Collect only the information needed for the feature. Document where entries are stored, how long they remain, and what clearing/deleting them removes. Do not log sensitive wellbeing text by default. If account support exists, test that one user cannot retrieve another user's records.

## Safety expectations

- Use clear, supportive, non-stigmatizing language.
- Do not claim to diagnose, treat, or replace professional care.
- Do not invent clinical citations or emergency contact information.
- If crisis-resource guidance is present, verify it for the intended region and keep it easy to find.
- Make limitations clear and do not promise a human response unless one is actually provided.

## Pull-request checklist

- [ ] Add tests for normal, invalid, and safety-relevant inputs.
- [ ] Run the project's declared test/build commands.
- [ ] State which external integrations were mocked.
- [ ] Review logs and errors for sensitive content.
- [ ] Document data retention/deletion behavior from actual implementation.
