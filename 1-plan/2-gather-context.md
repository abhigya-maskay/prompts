## Phase 2: Gather Context

1.  **Initial Context Seeding:** Copilot asks the user for starting points to gather context. This could be file names, class names, or keywords related to the feature.

2.  **Context Expansion & Verification:**
    *   Copilot uses the initial seeds to search the codebase for relevant files and code snippets.
    *   Copilot presents the gathered context to the user for verification.
    *   **User Checkpoint:** The user reviews the context, confirms its relevance, and suggests additions or removals. This loop continues until the user is satisfied with the context.

3.  **Document Context:**
    *   Once the context is finalized, Copilot will create a markdown file.
    *   This file will contain all the relevant code snippets, file summaries, and other contextual information.
