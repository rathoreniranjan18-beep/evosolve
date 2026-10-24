# Contributing

Thanks for considering a contribution to EvoSolve.

## Before changing code

1. Open `index.html` locally and reproduce the issue.
2. Describe the expected and actual behavior.
3. Keep changes focused and explain why they are useful.
4. Avoid adding dependencies unless there is a clear benefit.

## Pull request checklist

- [ ] The app opens without a server or build step.
- [ ] Existing controls still work.
- [ ] New behavior is described in the README or docs.
- [ ] No secrets, tokens, or personal data were added.
- [ ] Changes were tested in a modern browser.

## Development

The current implementation is intentionally a single static HTML file. Open `index.html` directly or use `python -m http.server 8000` and visit `http://localhost:8000`.
