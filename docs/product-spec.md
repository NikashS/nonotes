# No Notes — Product Spec

## Summary

No Notes is an AI interface without chats, threads, or tasks. Users interact through one input and never need to find an old conversation. The system retrieves the right context, takes the user to the relevant place in their knowledge space, and continues the work.

Context is stored as durable artifacts—documents, decisions, visualizations, entities, and relationships—not as message history. These artifacts live on an AI-organized infinite canvas and can be retrieved semantically.

## Problem

Chat-based AI makes users remember where prior work happened. When they cannot find the right conversation, they start another one without its context. Knowledge becomes fragmented across overlapping threads, while long transcripts introduce irrelevant context.

Human thought is not neatly turn-based or task-scoped. Topics recur and connect across time, sources, and interfaces.

## Product Principles

- **One entry point:** Starting new work and continuing old work feel the same.
- **Ask, don't search:** Users request what they remember; the system finds it.
- **Solve context:** Retrieve the smallest useful set of artifacts for each request instead of loading entire histories.
- **Artifacts over transcripts:** Preserve useful outcomes, not conversation containers.
- **Navigation by intent:** Asking is the primary way to move through the canvas; panning and browsing are secondary.
- **Visual when helpful:** Explain ideas with approachable notebook-style diagrams and infographics when they improve understanding.
- **Legible memory:** Users can see what the AI knows, where it came from, and where its knowledge is incomplete.

## Core Experience

The home view is a single input over a persistent infinite canvas. It has no chat list.

For each request, the system identifies relevant entities, retrieves related artifacts, resolves ambiguity, and then answers by navigating to existing material, updating it, or creating something new.

Responses may be text, documents, diagrams, maps, or linked groups of artifacts. Related work is placed near each other. Follow-ups may modify the current artifact, add a nearby one, or shift focus to a new canvas area.

Users can return to prior work with requests such as:

- “What did we decide about onboarding?”
- “Continue the architecture diagram.”
- “How does our pricing work connect to customer research?”

The canvas remains manually explorable through pan, zoom, selection, and links, but users should not need to browse it to find something.

## Knowledge Model

Artifacts are stable, vector-searchable objects with content, provenance, revision history, relationships, permissions, and uncertainty where relevant. Common artifact types include documents, decisions, plans, visualizations, entities, source material, and unresolved questions.

Relationships such as *related to*, *depends on*, *supports*, *contradicts*, and *supersedes* guide retrieval and canvas placement. AI-inferred relationships remain distinguishable from user-confirmed ones.

The knowledge map lets users inspect major topics, relationships, sources, contradictions, and gaps. Users can correct links, merge duplicates, edit artifacts, and remove knowledge.

In the background, the system extracts artifacts from interactions, identifies new relationships, detects contradictions, and reorganizes related material. Changes remain attributable and reversible; stable spatial landmarks should be preserved.

## Multiple Entrypoints

The same knowledge is available from the main app and clients such as Slack or text. Users do not select a conversation or project first. Identity, permissions, the request, and the knowledge graph determine context.

Messaging clients return concise answers and links to relevant canvas locations. Changes made through any client update the same underlying knowledge.

## Onboarding

To address cold start, users can import selected context from sources such as ChatGPT, Claude, documents, Slack, email, or calendars. Imports are transformed into artifacts and relationships rather than reproduced as old chat lists.

Users choose the sources and scope, then review an initial knowledge map showing imported knowledge, uncertain links, and gaps.

## MVP

The MVP should prove that users can reliably continue prior work without finding an old conversation.

It includes:

- A single input with no chat or task list.
- A persistent infinite canvas with text, document, and simple diagram artifacts.
- Automatic artifact extraction and semantic retrieval.
- Basic entity and relationship linking.
- Natural-language navigation to existing canvas regions.
- Follow-ups that update or extend existing work.
- Provenance, revision history, and user correction.
- A basic knowledge map with visible gaps.
- Import from one AI conversation source and one document source.

Broad connector coverage, autonomous reorganization, advanced collaboration, and external actions are deferred.

## Success Measures

- Users retrieve and continue the intended prior work without manual search.
- Context selection is rarely corrected or rejected.
- Existing artifacts are reused instead of duplicated.
- Users reach relevant context quickly.
- Users understand why information was used and trust that the system remembers the right things.

No Notes succeeds when users stop thinking in conversations and simply ask for their work, trusting the system to recover the right context and present it in a form they can understand and continue.
