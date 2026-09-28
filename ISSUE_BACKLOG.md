# Ethereum Savings Vault Issue Backlog

This backlog is the working list of issues we plan to tackle before and during implementation. Keep it current as scope or sequence changes.

## P0 - Project Setup

### 1. Establish the project stack

Define the final frontend, contract, test, and CI stack so all later work is consistent.

Acceptance criteria:

- Stack choices are documented.
- Local development commands are defined.
- Test and lint tools are selected.

### 2. Set up repository quality scripts

Add scripts for build, test, lint, format, and any other checks we want to run locally and in CI.

Acceptance criteria:

- Scripts exist in `package.json` or the equivalent project config.
- The commands are documented.

### 3. Add CI for pull request checks

Create the first automated pipeline for validation on every pull request.

Acceptance criteria:

- CI runs tests and linting.
- Failures block merge.

## P0 - Smart Contract Foundation

### 4. Implement the savings vault contract

Create the core vault contract with deposit and withdrawal behavior.

Acceptance criteria:

- Deposits update vault state correctly.
- Withdrawals update vault state correctly.
- Reverts are used for invalid actions.

### 5. Add contract unit tests

Cover the contract with tests for the expected flows and edge cases.

Acceptance criteria:

- Happy path tests pass.
- Failure path tests pass.
- Events are tested where appropriate.

## P1 - UI Foundation

### 6. Build the vault dashboard UI

Create the main user interface for wallet state, balances, and actions.

Acceptance criteria:

- The UI shows relevant vault information clearly.
- The layout is simple and readable.

### 7. Add UI unit tests

Cover the key states and interactions in the interface.

Acceptance criteria:

- Connected and disconnected states are tested.
- Form validation is tested.
- Loading and error states are tested.

### 8. Add wallet connection flow

Connect the UI to a wallet provider so the vault can be used against a local chain or testnet.

Acceptance criteria:

- The app can detect wallet connection state.
- The user can initiate the primary vault flows.

## P1 - Integration and Merge Safety

### 9. Add integration tests for deposit and withdrawal flows

Test the full path from UI action to contract behavior.

Acceptance criteria:

- Deposit flow passes end to end.
- Withdrawal flow passes end to end.

### 10. Add branch protection and merge checks

Require passing checks before code can land.

Acceptance criteria:

- Required checks are documented.
- The workflow supports review discipline.

## P2 - Documentation and Learning

### 11. Document the architecture and learning notes

Capture the main implementation decisions and what they teach about Ethereum.

Acceptance criteria:

- Architecture is described clearly.
- Learning notes are easy to update.

### 12. Keep the reference docs in sync

Update the roadmap, backlog, and project reference with every commit that changes scope or implementation details.

Acceptance criteria:

- Planning docs are treated as living files.
- The docs remain aligned with the codebase.