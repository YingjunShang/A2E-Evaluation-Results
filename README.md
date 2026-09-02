# A²E Evaluation Results — Static Snapshot

This directory contains a standalone snapshot of the A²E evaluation UI. It reads experiment, metric, sample, and trace data from the local `data/` directory and does not connect to an A²E server or SQLite database.

Open `index.html` directly in a browser. No build command or backend process is required.

The snapshot records its source database and generation time in `data/manifest.js`. To refresh the snapshot during development, run:

```bash
npm run snapshot -- /absolute/path/to/database.db
```

The export keeps the fields displayed by the UI. Repeated LLM messages are deduplicated within each trace, and exceptionally long raw strings are truncated to keep the offline package usable.

The static snapshot intentionally excludes all CrewAI and Smolagents experiments, samples, and traces.
