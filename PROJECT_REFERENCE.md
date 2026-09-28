# Ethereum Savings Vault Reference

This document is the living reference for the Ethereum Savings Vault project. It is meant to stay accurate as the project evolves, and we will keep iterating on it with each commit so it always reflects the current state of the codebase.

## Planning Docs

- [Roadmap](ROADMAP.md) — the current project phases, decisions, and next milestones.
- [Issue Backlog](ISSUE_BACKLOG.md) — the work items we plan to execute and refine over time.
- This reference file stays as the top-level index for scope, standards, and the update rule.

## Purpose

Build a simple Ethereum savings vault that helps us understand the inner workings of deposits, balances, withdrawals, transactions, and smart contract behavior, while keeping the product polished and easy to reason about.

## Project Standards

- Treat the project like an enterprise app, even though the scope stays small.
- Keep the UI clean, minimal, and easy to use.
- Add unit tests for the UI and smart contract logic.
- Add integration tests for the main deposit and withdrawal flows.
- Run linting, formatting, and test checks in CI.
- Use merge checks so no change lands without passing validation.
- Keep the documentation accurate as the implementation changes.

## Product Goals

- A simple wallet-connected UI.
- A vault flow for depositing test ETH.
- A visible vault balance and user balance.
- Clear transaction states for pending, success, and failure.
- A simple explanation of what each action means so the app doubles as a learning tool.

## Technical Goals

- Smart contracts should be small, readable, and heavily tested.
- Frontend components should be testable in isolation.
- Tests should cover both happy paths and common failure cases.
- The app should be easy to run locally against a dev chain.
- The codebase should be structured so future Ethereum practice projects can reuse the same quality bar.

## Testing Plan

### Smart Contract Tests

- Deposit increases vault balance.
- Withdraw decreases vault balance.
- Unauthorized actions fail.
- Edge cases around zero amounts and insufficient balance are covered.
- Events are emitted where appropriate.

### UI Tests

- Connected wallet state renders correctly.
- Disconnected wallet state renders correctly.
- Deposit form validates input.
- Submit flow shows loading and success states.
- Errors are displayed clearly.
- Balance and status text update when state changes.

### Integration Tests

- User connects wallet and deposits test ETH.
- User withdraws from the vault.
- UI reflects contract state after transactions.
- Transaction failures are surfaced correctly.

## CI and Quality Gates

- Run tests on every pull request.
- Run lint and format checks in CI.
- Require passing checks before merge.
- Keep coverage thresholds in place as the project grows.
- Prefer small, reviewable commits.

## Working Rule

Before each commit, update this document if anything about the project scope, structure, test approach, or implementation details has changed.

## Open Questions

- Which local chain or testnet should we standardize on first?
- Which frontend stack should we use for the wallet and vault UI?
- Which contract testing framework should be the default?
- How strict should the coverage threshold be at the start?
