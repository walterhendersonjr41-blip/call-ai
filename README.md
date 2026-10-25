# Call AI

Two giant buttons: **Live talk** and **Camera**. Tap to open, tap again to close. No login. Each visitor gets 5 minutes of talk time per day (tracked in the browser).

## What it does
- **Listens** with the browser's built-in speech recognition (Chrome, Edge, Safari), hands-free: you talk, it answers out loud, then listens again.
- **Talks back** with the browser's built-in voices. It picks the most natural English voice it can find; change it in Settings (gear, top right).
- **Interrupt anytime**: start talking while it speaks and it stops to listen.
- **Live captions** of what you said and what it answered.
- **AI brain**: free by default (Pollinations, no key). Optionally paste your own xAI (Grok) or Google Gemini API key in Settings. Keys stay only in your browser.
- **Text box fallback** for browsers without voice input (for example Firefox).

## Camera / mail reader
- Tap **Camera** to open the back camera. Tap the big picture to read what it sees. Tap **Close camera** to turn it off.
- It **sorts mail first**: **REAL MAIL** (bills, government, SNAP/SSDI/Social Security, bank, medical, court, insurance, post office notices, personal), **JUNK MAIL** (ads, offers, "you may already qualify", "Current Resident", fake-official look), or **POSSIBLE SCAM** (gift-card demands, arrest threats, pretend government or bank).
- It says the one-line verdict, then asks: *"Do you want me to read it word for word, or just give you the short version?"*
  - **1** = word for word, **2** = short version. Tap the big 1 / 2 keys, say "one"/"two"/"yes"/"no", or press 1 / 2 on a keyboard. No answer in 12 seconds means the short version.
  - The short version is just the facts: who it's from, what it's about, amount due, due date, and what to do. Junk gets one sentence: nothing to do.
- After that you can ask questions about the same photo by voice ("How much do I owe?").
- Any yes/no question the AI asks uses the same pattern: **1 = yes, 2 = no**.

### How the camera reading works
- **Free (no key):** the words are read on the phone itself with Tesseract.js (open-source text reader, loaded from jsDelivr, about 15 MB the first time and then cached), and the free Pollinations AI sorts and summarizes them. This works for printed mail, labels and letters. It can't describe pictures that have no words.
- **With your own xAI or Gemini key** (Settings): the photo, shrunk to 1024 px JPEG, goes straight to that AI's vision model, so it can also describe objects, handwriting and pictures. If that fails, it falls back to the free text reader.
- If the live camera is blocked or missing, tapping the picture area opens the phone's normal photo picker instead.
- Needs HTTPS (GitHub Pages is), and works in Android Chrome and iPhone Safari.

## Files
- `index.html`: the whole app. It's static, works on GitHub Pages, and has no server and no keys in the code.

Created by Walter Henderson Jr.
