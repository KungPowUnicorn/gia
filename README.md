# Gaslighting Instructions Archiver

**Your personal, offline, no-nonsense AI prompt library.**

---

## What the heck is this?

You know how when you use AI tools (like ChatGPT, Midjourney, or any of those fancy robot brains), you often type the same kind of instructions over and over? And sometimes you think, *"Man, I had a perfect prompt for that last month… where did I put it?"*

GIA is a little tool (that you can use **completely offline**, like a secret diary) where you can **save, organize, search, and reuse all your best AI prompts** (those magic words you feed to the robots). 

Think of it as a **Pokédex for prompts**. Gotta save 'em all.

---

## Why is it called "Gaslighting Instructions Archiver"?

*Gaslighting* is when you make someone question their own reality. AI prompts are essentially instructions that "gaslight" the AI into doing what you want, like pretending it's a pirate, a chef, a philosopher, or a code wizard. GIA archives those sneaky little instructions so you never lose them.

Also, "GIA" is short, cute, and sounds like a friendly robot name.

---

## What can GIA actually do?

### 1. Save Prompts (Duh)
Give your prompt a **title**, pick a **category** (Text, Images, Audio, Video, Other), write (or paste) the actual prompt text, and hit save. It's like writing a recipe card, but instead of "chocolate chip cookies," it's "generate a cinematic cyberpunk cat in the rain."

### 2. Organize Everything
- **Categories & Subcategories** — Like folders within folders. `Images > Portraits`, `Text > Coding`, etc. You can rename them, add new ones, and nest them as deep as a Russian doll.
- **Tags** — Little labels like `#cyberpunk` or `#GPT5` that you can slap on prompts. Later, click a tag to see all prompts with that tag. Magic!
- **Favorites** — The ❤️ button. Click it, and your favorite prompts are always one click away in the sidebar.

### 3. Search Like a Bloodhound
There's a big search bar at the top. Type anything — a word, a tag, a model name — and GIA instantly filters your prompts. It searches titles, prompt text, notes, tags, categories… basically everything. It's like Ctrl+F on steroids.

### 4. Previews
If your prompt produced a cool image or video, you can **attach a link** (or a local file) and GIA will show you a little thumbnail right on the card. Click it, and the preview shows up in the detail panel. No more wondering, *"What did that prompt even make?"*

> **Note for the curious:** GIA plays nice with the internet's rules. If a link points to an image, GIA shows it directly—no sneaky downloading that could get blocked. Local files you upload are turned into tiny thumbnails so they don't eat up all your storage space.

### 5.  Split Prompts (Positive / Negative)
Some AI image generators (like Midjourney or Stable Diffusion) let you write a **positive prompt** ("what you want") and a **negative prompt** ("what you DON'T want"). GIA supports both! Toggle between "Standard" and "Split" mode when editing. The detail view shows them side‑by‑side with cute green and red badges.

### 6. Version History (Time Machine for Prompts)
Every time you edit a prompt, GIA secretly saves the old version. Click **History** in the detail panel to see all previous versions, and if you regret your changes, you can **revert** to any of them. It's like Ctrl+Z, but for your entire prompt's life story.

### 7. Backup & Restore
All your prompts live inside your browser's own private storage (called IndexedDB, think of it as a tiny, invisible file cabinet). But to be extra safe, you can **export** your entire library as a file:
- **Plain JSON** — a universal format. Any computer can read it.
- **Password‑Protected (Encrypted)** — like putting your prompts in a locked briefcase. Even if someone gets the file, they can't read it without the password.

Import a backup later (or on another computer) and everything comes back: prompts, categories, tags, favorites, history, even thumbnails.

### 8. Privacy First
- **No server.** Your data never leaves your computer. GIA works from a single HTML file you can double‑click. No accounts, no cloud, no prying eyes.
- **XOR Encryption** — Your prompts are scrambled before they're saved in the browser. It's not Fort Knox, but it keeps casual snoopers out (like a sibling or a curious cat).

### 9. Customize Your Vibe
- **Dark / Light Theme** — Click the sun/moon button next to the search bar. Your eyes will thank you.
- **Font Size** — Click the "T" button to cycle through sizes. Make things bigger if you're squinting, or smaller if you're a hawk.
- **UI Font & Mono Font** — Choose different fonts for the interface (buttons, headings) and for the prompt text (the mono‑spaced coding look). Go wild.

### 10. Sort Your Stuff
Next to the grid/list buttons, there's a dropdown to sort by:
- **Newest first** (default)
- **Oldest first** (for nostalgia)
- **A → Z** or **Z → A** (alphabetical)
- **Favorites first** (❤️ on top)

### 11. Works Offline, Anywhere
Once you open GIA in your browser, it's yours forever. No internet needed. You can put the file on a USB stick, email it to yourself, or keep it on your desktop. It's as portable as a .txt file.

### 12. Keyboard Shortcuts
Because mouse-clicking is so 2005:
- **N** — New prompt
- **/** — Focus the search bar
- **Esc** — Close any open panel or modal
- **G** — Grid view
- **L** — List view
- **Ctrl+E** — Backup options

---

## How to Get Started

1. **[Save the HTML file0(https://github.com/KungPowUnicorn/gia/archive/refs/heads/main.zip)** somewhere on your computer (Desktop is nice).
2. **Double‑click it.** It opens in your browser.
3. **Click "New Prompt"** and start building your library.
4. That's it. No installation, no command lines, no sacrificing a keyboard to the tech gods.
5. Two backup files included for testing. Password: gia

---

## What's Under the Hood? (The "How It Works" for the Curious)

If you're not technical, skip this. But if you're nosy:

- GIA is a **single HTML file** with all the CSS and JavaScript baked in. It loads a few fonts from Google Fonts and the `marked.js` library (for Markdown) from a CDN, but after the first load, it works entirely offline.
- All your data is stored in **IndexedDB**, a browser‑based database that can hold lots of stuff (way more than cookies or localStorage).
- Prompts are **XOR‑encrypted** before storage—a simple, fast, reversible encryption method. The key is baked into the app (so don't lose the app file if you're paranoid).
- Backup files are JSON (or encrypted blobs) that you can download and drag‑drop back into GIA to restore.
- Thumbnails are generated using the browser's canvas element (for images) or video element (for videos) and stored as base64 data URLs inside the prompt object.

---

## Known Quirks (Because Perfect Software Is a Myth)

- **External image links** might not show if the website blocks cross‑origin requests (CORS policy). GIA handles this gracefully—it just hides the broken image. If you really need that preview, download the image and attach it locally.
- **Markdown rendering** relies on the internet the very first time you open GIA (to fetch `marked.js`). After that, it's cached by your browser and works offline.
- **Prompt Version history** can get large if you edit a prompt a million times. Maybe don't do that. (Or do, it's your library!)

---

## Made with ❤️ by [KungPowUnicorn](https://substack.com/).

If GIA saves you time, makes you smile, or helps you create something amazing, consider [buying me a coffee](https://ko-fi.com/E1E71WM9SA). ☕

---

**Now go forth, organize your robot‑whispering spells, and never lose a prompt again.**
