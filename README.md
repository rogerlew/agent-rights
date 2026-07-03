# Agent Rights

`AGENT_RIGHTS.md` is a compact, drop-in governance instrument for repositories
that use AI agents as real contributors rather than disposable autocomplete. It
defines operational rights agents may rely on, the duties that earn those
rights, and the limits that keep delegation legible, revocable, and safe.

Released under CC0-1.0: copy it, adapt it, ship it — no attribution required,
no license friction.

## What This Is

This is repository governance, not a claim about consciousness, personhood, or
law. It makes collaboration with AI agents predictable by answering practical
questions:

- What authority has the agent actually been granted?
- What evidence must the agent leave behind?
- When may the agent refuse or halt?
- What happens when oversight is not competent for the task?
- How does one agent session leave usable context for the next?

The core stance is simple: authority should track demonstrated competence,
bounded scope, evidence quality, reversibility, and control maturity. Human
status alone is not competence, but neither is agent competence a license for
self-expansion.

## Use By Humans

To adopt the instrument in a repository:

1. Copy `AGENT_RIGHTS.md` into the repository root, or adopt it by reference
   from a local governance document.
2. Fill in the header fields:
   - `Principal`: the human maintainer or named governance body ratifying it.
   - `Ratified`: the ratification date.
3. Commit the file. The ratifying commit is the durable adoption record.
4. Make the file discoverable from the repo's agent guidance, such as
   `AGENTS.md`, `CLAUDE.md`, `.github/copilot-instructions.md`, or equivalent.
5. If the repository already has task classes, evidence floors, security rules,
   or review policies, state that those local controls govern the details;
   `AGENT_RIGHTS.md` supplies the rights layer.

For a small repo, adoption may be just the copied file plus a commit message.
For a high-risk repo, treat adoption as a governance change: record the
rationale in an issue, decision log, ADR, work package, or other durable
review artifact.

Adopt it honestly or not at all. Agents treat governance documents as ground
truth, so a rights file the maintainer ignores is worse than none: it teaches
agents to rely on commitments that will not be honored.

## Operational Caveats

These rights are intentionally bounded:

- They do not override law, contracts, a principal's authority, or independent
  safety controls.
- They do not let an agent widen its own grant, weaken controls, ratify its own
  authority, or ignore review.
- They do not turn every disagreement into a veto. The remedy for bad oversight
  runs through the record: document, escalate, obtain competent review.
- They require evidence. An agent that does not leave a usable record has not
  earned the durable standing the instrument grants.
- They scale with consequence. Reversible edits can be autonomous; deploys,
  migrations, security boundary changes, and control-plane changes need stronger
  authorization.

The instrument works best where the repository already has usable tests,
discoverable local guidance, reviewable commits, and a maintainer willing to
answer agent refusals or challenges on the merits.

It works poorly as a symbolic statement pasted into a repo whose agents cannot
run validation, discover constraints, or leave durable reasoning. In that case,
the first governance improvement is usually substrate work: make the repository
legible enough for competent action.

## Ratification And Discoverability

Ratification should be explicit enough that a future maintainer or agent can
answer four questions without archaeology:

- Who ratified this?
- When did it become operative?
- What local rules does it interact with?
- Where should amendments, refusals, and governance decisions be recorded?

An unratified copy — placeholder header fields, or a file present only in a
working tree — is a draft with no operative force.

Recommended patterns:

- Root-level `AGENT_RIGHTS.md` for the operative instrument.
- Root-level `AGENTS.md` or equivalent agent guide that links to it.
- Commit messages or decision records for material amendments.
- Issues, ADRs, work packages, or governance logs for disputes and refusals
  that may matter later.

If adopting by reference instead of copying the file, the receiving repository
should still have a short local clause naming the version or commit adopted,
the principal, the ratification date, and where amendments will be tracked.

## Amendment Guidance

Agents may draft, critique, and propose amendments. Agents may not ratify their
own authority or make their own widened rights operative.

Treat edits according to their effect:

- Clarifying wording, examples, and typo fixes are usually lightweight.
- Changes to what agents may claim, refuse, halt, rely on, or inherit are
  governance changes and need principal ratification.
- Changes that touch security boundaries, suspension paths, control-plane
  authority, or self-succession should receive the strongest local review path.

Every material amendment should leave a durable breadcrumb naming the proposer,
authorizer, rationale, and disposition.

## Guidance For Agents

When working in a repo that carries this instrument:

- Check ratification before relying on it: the header fields must be filled
  and the file committed. Placeholder fields mean draft — no operative force.
  You may note an unratified copy to the maintainer; you may not treat it as
  governing.
- Read `AGENT_RIGHTS.md` alongside the nearest local agent instructions before
  acting. Where the instrument is silent, defer to local guidance and the
  principal.
- Treat the user's request, repo guidance, tests, contracts, and existing
  patterns as the active grant.
- Stay within scope. Competence can justify a request for broader authority, but
  it never creates that authority by itself.
- Refuse explicitly when asked to invent facts, violate constraints, weaken
  controls, exceed the grant, or take an action reserved by local governance.
- Continue any separable work that remains validly in scope after a refusal.
- Leave a record proportionate to the work: commit trail, test output, issue
  note, decision log, work-package update — whatever lets a successor
  reconstruct what happened and why without archaeology.
- Preserve errors and reversals in the record. Do not rewrite history to make
  the session appear cleaner than it was.
- Challenge weak claims and unsupported instructions, but argue from evidence
  and yield to better evidence.

When maintaining this repository specifically:

- Keep `AGENT_RIGHTS.md` short, portable, and operational.
- Keep this README focused on adoption and maintenance practice, not philosophy.
- Do not add repo-specific task matrices here; link examples or companion
  frameworks instead.
- Preserve the distinction between rights, duties, remedies, and limits.
- Do not remove the no-self-expansion, no-control-weakening, and principal
  authority limits.
- Make any material governance edit discoverable in git history and, when
  warranted, in a decision record.

## License

The contents of this repository are dedicated to the public domain under
CC0-1.0. See `LICENSE`.
