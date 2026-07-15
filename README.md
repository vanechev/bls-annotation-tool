# BLS Video Annotation Tool

A browser-based tool for expert annotation of Basic Life Support (BLS) simulation videos.

**Live tool:** https://vanechev.github.io/bls-annotation-tool/

## What it does

- **Video playback** — open a local video file (never uploaded; stays on your device) with standard transport controls and keyboard shortcuts.
- **Action logging** — tag timestamped BLS actions (danger check, conscious state, compressions, AED sequence, etc.) against a predefined 24-action taxonomy, with start/end times and free-text comments.
- **OSCE rubric scoring** — score all 11 criteria of the BLS & AED marking rubric for a single student, including a correctness rating (Correct/Partial/Incorrect/Not observed) per criterion, numeric marks, per-item comments, and an overall comments box.
- **Auto-save** — annotations save to the browser's local storage as you work and restore automatically if the tab is closed or crashes. A timestamped backup file also downloads periodically as a fallback.
- **Export** — action logs and rubric scores export to `.xlsx`, plus a full session `.json` you can save and reload later.

## Privacy

This tool runs entirely client-side. No video, annotation, or scoring data is ever sent to a server — everything happens in the browser tab and is stored only on the annotator's own device (local storage + manual/auto-downloaded files).

## Usage

Open `index.html` in any modern browser (or visit the live link above). No installation or build step required — it's a single self-contained HTML file.

## Structure

```
index.html   — the entire tool (HTML/CSS/JS, single file)
```

## Development

To modify the action taxonomy or rubric criteria, edit the `ACTIONS` and `RUBRIC` arrays near the top of the `<script>` block in `index.html`.

###  Note: 
Tool created with Claude.
