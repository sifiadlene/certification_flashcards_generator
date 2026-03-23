# Certification Practice Website

This app provides browser-based practice for the certification decks stored in the repository root.

## Commands

```bash
npm install
npm run dev
npm run build
```

## How It Works

- [scripts/buildFlashcardData.mjs](scripts/buildFlashcardData.mjs) reads the CSV decks from [../flashcards](../flashcards)
- the script selects the latest file for each exam and writes normalized JSON into [public/data](public/data)
- the React app loads that manifest and renders exam selection, practice mode, timed quizzes, and missed-question review

## Notes

- progress is stored in browser `localStorage`
- the app is built for static hosting
- GitHub Pages deployment is configured in the repository root workflow
