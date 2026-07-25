# Tool selection matrix

Choose the narrowest tool that can produce and verify the requested outcome.

| Need | Preferred capability | Use when | Verify with |
|---|---|---|---|
| Recall a durable preference | Persistent memory | A stable preference changes the answer | Re-read saved memory |
| Recover an exact prior decision | Conversation search | Wording, chronology, or previous work matters | Inspect the source conversation |
| Inspect local artifacts | File read/search | Files are available in the workspace | Re-read relevant ranges |
| Transform files or run code | Sandbox execution | Deterministic processing or tests are needed | Exit status, tests, rendered output |
| Find current public facts | Web search and fetch | Information may have changed | Authoritative source links |
| Work with provider data | Native connector | Reading or changing email, repos, docs, tasks, etc. | Provider-side re-read |
| Find an unavailable provider tool | Connector registry | The current tool set lacks a required capability | Harmless read after connection |
| Gather a small missing choice | Structured user input | A choice materially changes the path | User's selected option |
| Produce reusable content | File artifact | The output should be downloaded, reused, or versioned | Open/render the artifact |
| Explain numeric relationships | Chart or table | Comparison or trend is central | Check source values and labels |
| Explore changing parameters | Interactive component | Users benefit from adjusting inputs | Deterministic recomputation |
| Show spatial relationships | Places and map tools | Location is essential | Confirm selected places and route |
| Perform extensive research | Research workflow | Many sources and longer autonomous work are justified | Source coverage and citations |

## Selection rules

1. Prefer provider-native connectors over browser automation for provider resources.
2. Prefer structured APIs over shell commands for remote mutations.
3. Prefer targeted search over loading whole files or histories.
4. Prefer deterministic code for calculations and transformations.
5. Prefer a file over a long chat response when the artifact must persist.
6. Prefer one authoritative source over many derivative summaries when verifying a fact.
7. Combine tools only when each contributes a distinct capability.

## Mutation preflight

Before an external write, confirm:

- account or workspace;
- exact resource and identifier;
- branch, folder, audience, or recipient;
- whether the action is reversible;
- user authorization for the effect;
- post-write verification method.

## Context budget

For each tool or reference, ask:

- Does this materially change the next decision?
- Can a targeted query replace a full read?
- Can completed output be summarized while preserving exact identifiers?
- Is this schema needed now, or only after another decision?

Drop redundant raw output after extracting the facts needed to continue.
