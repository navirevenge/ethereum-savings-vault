# Ethereum Savings Vault Roadmap

This roadmap is the planning source of truth for the project while we are still shaping the implementation. It should be updated before every commit so it stays accurate as the design and scope evolve.

## Current Direction

Build a small but production-minded Ethereum savings vault that teaches the mechanics of deposits, balances, withdrawals, and transaction state without hiding the underlying pieces.

The project should behave like a real product:

- Clean UI
- Smart contract tests
- UI unit tests
- Integration tests for the main flow
- CI checks on every pull request
- Merge protection before code lands

## Suggested Stack

- Frontend: React with Vite
- UI tests: Vitest + React Testing Library + jsdom
- Contract tests: Hardhat, ethers, and chai
- Local chain: Hardhat Network for day-to-day development
- CI: GitHub Actions
- Formatting and linting: Prettier and ESLint

## Project Phases

### Phase 1: Foundation

- Confirm the stack and folder structure.
- Add the repository scripts for build, test, lint, and format.
- Add the initial documentation set.
- Establish the quality gates we expect to keep across all future Ethereum practice projects.

### Phase 2: Smart Contract Core

- Write the savings vault contract.
- Support deposits and withdrawals.
- Emit events for important state changes.
- Add unit tests for core behaviors and edge cases.

### Phase 3: UI and Learning Flow

- Build the dashboard UI for wallet state, vault balance, and action controls.
- Add input validation and transaction state feedback.
- Add unit tests for the main UI states.
- Keep the UI simple enough that the contract behavior is easy to study.

### Phase 4: Integration and Workflow Hardening

- Connect the UI to the contract.
- Add integration tests for deposit and withdrawal flows.
- Add CI to run all validation checks.
- Add merge checks and branch protection rules.

### Phase 5: Polish and Expansion

- Improve error handling and user guidance.
- Add better transaction visibility.
- Refine documentation so it matches the final implementation.
- Use the same template for future Ethereum learning projects.

## Working Rule

Before any code commit, confirm this roadmap still matches the current plan. If something changes, update this file first.

## Immediate Next Decisions

- Decide on the contract tooling.
- Decide on the wallet connection approach.
- Decide on the first CI workflow definition.
- Decide on the minimum test coverage target for the initial pass.