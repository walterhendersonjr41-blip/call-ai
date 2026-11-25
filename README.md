# Call AI

Two giant buttons: **Live talk** and **Camera**. Everything else, like the history guide, works by just asking. Tap to open, tap again to close. No login. Each visitor gets 5 minutes of talk time per day (tracked in the browser).

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

## History around me (just ask, no button)
- Say or type things like *"What's the history around me?"*, *"Where am I?"*, *"Tell me about this place"*, *"Any history near me?"* or *"What's the history of Chattanooga?"*. There's no extra button. It works by asking.
- It asks the phone for your **location** (you'll see the normal "Allow location" prompt), finds the town with **OpenStreetMap Nominatim** (free, no key, at most 1 lookup a second), then pulls real nearby places within about 6 miles (10 km) from **Wikipedia** with short summaries.
- The AI tells it like a friendly local tour guide: a few short sentences, one surprising fact, then it offers more or something nearby. You can follow up ("tell me more about the battle") and it sticks to the same facts.
- It only uses the Wikipedia facts it found and **never makes up history**. If it doesn't have something, it says so.
- If location is blocked or off, it asks you to say where you are ("I'm at Rock City") and looks that place up on Wikipedia instead. If a name could mean more than one place, it says which one it picked so you can correct it.
- Questions like "history of the Super Bowl" that aren't about a place get a normal answer.


## Dad page (one button)

A simpler page for an older parent: [call-ai/dad](https://walterhendersonjr41-blip.github.io/call-ai/dad/). The whole screen is one button.

- **Tap once** to talk. It listens, answers out loud, then listens again. Tap once more to stop.
- **Tap twice** (two quick taps) to read a letter or paper. The back camera opens, it says "Hold it still," then "Reading now," and takes the picture by itself. No extra button to snap. It speaks a short summary right away: who it is from, what it is about, any amount due, the due date, and what to do. It will say if it looks like junk or a possible scam.
- After the summary, tap once to ask a follow-up question by voice, or tap twice to read something else.
- If the live camera cannot start, it will ask you to tap once to take or choose a photo instead.
- No login. Free (same Pollinations AI and Tesseract word reader). Talk time on this page is 60 minutes a day. Reading mail still works after that.
- Works in Android Chrome and iPhone Safari, on HTTPS. The first time, the phone will ask to allow the microphone and camera.
- The original two-button app at the main address is unchanged.

## Files
- `index.html`: the original two-button app. It's static, works on GitHub Pages, and has no server and no keys in the code.
- `dad/index.html`: the one-button page described above, at `/dad/`.

Created by Walter Henderson Jr.
