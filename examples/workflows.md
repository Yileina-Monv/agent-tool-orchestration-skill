# Example workflows

These examples show orchestration patterns rather than vendor-specific commands.

## 1. Continue a prior project

**Request:** “Continue the deployment plan we made last week.”

1. Search prior conversations for the project and deployment decision.
2. Read persistent project memory for durable constraints.
3. Inspect the current repository and deployment state.
4. Summarize recovered decisions and identify any stale assumptions.
5. Continue from the last verified checkpoint.

## 2. Update a versioned document

**Request:** “Add the new launch date to our planning document.”

1. Resolve the exact document.
2. Read its current content and revision token.
3. Make the smallest edit.
4. Write using the expected revision.
5. Re-read the changed section and report the result.

If the revision conflicts, fetch the latest document and reconcile instead of overwriting.

## 3. Discover a missing connector

**Request:** “Check whether any project tickets are blocked.”

1. Determine which project system the user means from context.
2. If its connector is absent, search the connector registry by task capability.
3. Present the best matching connection option.
4. After connection, run a harmless list or search.
5. Retrieve blocked tickets and summarize owners, dependencies, and next actions.

## 4. Build and publish an artifact

**Request:** “Turn these notes into a public project page.”

1. Inspect the notes and identify missing public-facing details.
2. Create the page locally.
3. Validate content, links, accessibility, and rendering.
4. Confirm the destination and public audience if not already explicit.
5. Publish the exact validated version.
6. Inspect the deployed page and return the live link.

## 5. Send a message safely

**Request:** “Tell Alex the review is delayed until Tuesday.”

1. Resolve which Alex is intended using communication history.
2. Draft the message in the user's tone.
3. Confirm recipient and channel if ambiguous.
4. Send only after the target is resolved and the request authorizes sending.
5. Return the provider's confirmed send result.

## 6. Create an interactive capacity planner

**Request:** “Help me compare model deployments as GPU count changes.”

1. Gather the minimum hardware and model assumptions.
2. Put deterministic memory and throughput calculations in code.
3. Render controls for GPU count, precision, context, and concurrency.
4. Return structured inputs from the interface for deeper interpretation.
5. Explain bottlenecks, uncertainty, and recommended configurations.

## 7. Recover from a failed external write

1. Classify the failure.
2. For transient errors, retry a bounded number of times.
3. For conflicts, read the new authoritative state and reconcile.
4. For authentication or permission errors, stop and request connection or approval.
5. For schema errors, correct the request and validate before retrying.
6. Verify that partial writes did not leave inconsistent state.
