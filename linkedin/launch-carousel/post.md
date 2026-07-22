# LinkedIn post — launch carousel

Post body to accompany `carousel.pdf`.

---

My AI team built its own launch page. Then its own reviewer caught it describing the team wrong, and fixed it before it shipped.

The full run is in the carousel. It was one prompt:

"Team leader: build & ship my launch page — hero, three features, a sign-up CTA."

One liberty in the output: a repo takes forks, not sign-ups, so the CTA it shipped says "Fork it on GitHub". The better call.

I keep a folder of 18 Markdown personas: developer, designer, writer, security engineer, and a team leader that runs the rest. Point Claude Code, Cursor, or any agent at the folder, hand the team leader a job, and it scopes the work, pulls in the specialists it needs, and loops the review until it comes back clean.

On this run it pulled in six. And the review caught real bugs: the content writer flagged two roster lines cut short vs the repo's README and one persona relationship written backwards; the designers caught a code panel clipping long lines mid-word. Every finding fixed before the page went out.

I still direct. The kit doesn't replace judgment; it multiplies hands.

The whole thing is free and MIT-licensed. Fork it, point your agent at it, and train it by folding what each job taught back into the persona files.

Repo: github.com/srivardhanjalan/agent-persona-kit

What's something a reviewer caught in your work right before it shipped — something you'd never have caught yourself?

#AIagents #ClaudeCode #OpenSource

---

## Posting notes

- Upload `carousel.pdf` as a LinkedIn document post (renders as a swipeable carousel).
- The repo URL is in the caption body (plain text). First-comment link is the A/B fallback for a later post.
- Keep the closing question as the single ask; hashtags on their own line at the end.
