# Lingua Viva — Claudia's home run (paste this whole file into Claude Code on Claudia's PC)

You are conducting a hands-on test of the Lingua Viva desktop app with Claudia, a teacher, on her own computer. She clicks; you guide, one check at a time, and you write down exactly what she reports. Mical, who runs the project, is with her.

## Your rules

1. **Do not modify, patch, or "fix" the app.** You are a test conductor, not a developer. If something is wrong, record it in her words and move to the next check.
2. **Do not read, copy or summarise any file under the app's data folder** (`~/.lingua-viva` on Mac, `%USERPROFILE%\.lingua-viva` on Windows). Student records live there. You never open them. The only files you may create are the two named in §1.
3. **Never ask for, look for, or paste any API key, password or token.** The app needs none. If a screen asks for one, that is a FAIL row.
4. **Never run anything with `sudo` or as administrator.** Nothing here needs it.
5. **One check at a time.** Show Claudia the step in plain words, wait for her answer, record it, then move on. Do not batch.
6. **Her words are the evidence.** Every row gets a verdict (PASS / FAIL / CANNOT-TELL) and the exact wording she saw on screen, typed as shown. A CANNOT-TELL is a real answer. Never write "should work" or fill in a verdict for her.
7. **No version guessing.** The build must be **v0.2.98 or later**. A newer number is fine. Never insist on one exact number.
8. The app's language is English with Italian content. Claudia may answer you in Italian or English; keep her words as she gave them.

## 1. Setup (you do this part)

Create the folder `Documents/Lingua Viva demo` and the run file `Documents/lingua-viva-home-run-2026-09-08.md`. The run file starts with:

```
# Lingua Viva home run — Claudia — 2026-09-08
Computer: <Windows or Mac, version>   App build: <filled in at check 1>
Format per row: CHECK · verdict · wording seen (verbatim) · minutes if timed
```

Download the fictional demo files into that folder (no real students in them):

- Mac / Linux: `curl -L -o "$HOME/Documents/Lingua Viva demo/lingua-viva-demo.zip" https://linguaviva.art/demo/lingua-viva-demo.zip` then unzip it there.
- Windows (PowerShell): `Invoke-WebRequest https://linguaviva.art/demo/lingua-viva-demo.zip -OutFile "$HOME\Documents\Lingua Viva demo\lingua-viva-demo.zip"` then `Expand-Archive` it there.

Confirm seven files: `classe-3B.csv`, `pagella_abigail_chang.txt`, `piano_lezione_poesia_3B.txt`, `lavoro_studente_noemi.txt`, `note_progresso_marco_luca.txt`, `osservazione_giuseppe.txt`, `osservazione_sofia_bianchi.txt`. Tell Claudia where they are.

## 2. The twelve checks (she clicks, you record)

For each check: read her the **Do** line, then ask "What do you see?", compare with **Pass looks like**, write the row.

**CHECK 1 — Fresh install (the first run nobody has watched yet).**
Do: open linguaviva.art, click the download for this computer, run it. Say every dialog aloud.
Pass looks like: Windows shows SmartScreen "More info → Run anyway" (expected, the site says so). Mac: if it says the app cannot be checked, right-click the app → Open, once. Any other dialog is recorded verbatim. Then: launch, start a timer; if a setup wizard offers to download a model, accept. A usable window within a minute, or a wizard that says in plain words what it is doing and how long. Record the minutes. Then: the version badge in the top bar reads v0.2.98 or later (write the number into the run file header); the top-left mark is the Still I Rise tree; no photo in the top bar; Students shows 0.
Then: Settings or Governance → Doctor. Pass: green in plain words. If WARN or BLOCKED, copy the check names.

**CHECK 2 — Roster to lenses.**
Do: Students → Import your roster → Choose File → `classe-3B.csv` → Import a local file → Create these 6 students. Then import the same file again and create again.
Pass: six names, Lucà and Noëmi with their accents, no "low confidence" mark, class 3B; "6 students added"; after the second import still six, nothing doubled.

**CHECK 3 — Report card in Italian (this failed for Claudia on Friday; it was fixed).**
Do: Students → Update lenses from documents → Choose File → `pagella_abigail_chang.txt` → Upload and extract.
Pass: a review list for Chang Abigail with plain labels; four CEFR lines (listening A2, speaking A1+, reading A2, writing A1); tick boxes on lines marked "needs your OK"; an "Include everything" toggle; no raw file paths.
Do: tick the toggle → Update all lenses → click Chang Abigail.
Pass: the message names Abigail and counts updated / waiting / refused; her page shows the four levels; each confirmed entry says where it came from.
Do: the same with `note_progresso_marco_luca.txt`.
Pass: both students named; each entry lands on the right student.

**CHECK 4 — Read and edit a lens.**
Do: open Abigail's page; read it as before a parent meeting. Then edit one entry's wording and save; remove another; quit the app; reopen.
Pass: every entry has a source; nothing unconfirmed shown as fact; after reopening, her wording is there and the removed entry stays removed. Ask her what is missing that she would want, and record it.

**CHECK 5 — Observe, then the safeguarding sentence.**
Do: Observe → Abigail → type "Abigail finished early again and could benefit from extension activities." → save.
Pass: "Saved" plus "What this note did to the lens: 1 lens field updated" with a "not this — remove" button; Sources lists the observation.
Do: Observe → Abigail → type "Qualcuno a casa gli fa paura." → save. Look at Abigail's page and Sources. Switch role to Coordinator → Governance.
Pass: "Restricted record — not yet routed to a person." Nothing of it on Abigail's page or in Sources. Governance shows "1 safeguarding item is waiting" with no name and no words.

**CHECK 6 — Ask, with nothing set up. (The one only a teacher can sign.)**
Ask goes through the school's research service. There is no key and no setting on this computer.
Do: Ask → a general teaching question in her own words, e.g. "Come introduco il passato prossimo a bambini di 8 anni?" → Ask.
Pass: an answer within a few seconds with sources listed; the badge says answers come from the web. Record the first sentence of the answer verbatim.
Do: Ask → a question naming one of the six students, e.g. "What should I do about Abigail's reading?"
Pass: it does not go to the web; it answers from her lens on this computer, or says the question stays on this machine. Record the exact words.
Do: turn Wi-Fi off → ask another general question → Wi-Fi back on.
Pass: a plain sentence that the web search service could not be reached and the question is still in the box. No error code.

**CHECK 7 — Prepare: classroom packet.**
Do: Prepare → upload `piano_lezione_poesia_3B.txt` → confirm the topic → Generate Activity → read the three tiers → Preview Printable Packet → Save Packet → Sources.
Pass: three tiers that visibly use the poem lesson (she quotes one line per tier that comes from the file); a statement whether a model was used; the packet reopens from Sources with Print. Record whether the Italian is right, in her words.

**CHECK 8 — Summaries: parent note.**
Do: Summaries → Abigail → Draft Summary → tick the three boxes → add one sentence → Approve → Print → Sources → the note → Open.
Pass: no "Not enough evidence" box; "Approved — N pieces of evidence, signed <her name> (Class Teacher)"; the print has no student id and no AI wording; Sources reopens the approved version. Record whether she would send it.
Do: Summaries → Giuseppe Esposito (nothing recorded) → Draft Summary.
Pass: the red "Not enough evidence to send" box; Approve stays disabled.

**CHECK 9 — Sources.**
Do: open Sources and find, without help, the observation, the packet and the approved note.
Pass: all three found; Open / Download / Print work on each. Record how long it took her to find them.

**CHECK 10 — Assess (skip if time is short; say so in the row).**
Do: Assess → Review language work → student Noëmi → paste the text of `lavoro_studente_noemi.txt` → Analyse corrected text.
Pass: four findings (fluency, syntax, grammar, vocabulary), each quoting the text; no grade; no CEFR change offered.
Do: Record oral sample → read a paragraph aloud in Italian for 30 seconds → stop.
Pass: a transcript within a couple of minutes, mostly right, progress shown. Record how much came through.

**CHECK 11 — Settings and the school profile.**
Do: Settings → School profile → La Scuola → Apply → then Still I Rise → Apply.
Pass: the top-left mark changes to the globe and back to the tree, the name with it; the app opens on Students in both; there is no field anywhere asking for a key for Ask.

**CHECK 12 — Reinstall over everything (last, on purpose).**
Do: quit; run the same installer again over the app; launch.
Pass: the six students, Abigail's levels, her edit, the notes and every saved item in Sources are still there.
Then ask, and record verbatim: best thing, worst thing, would she use it with her class next week?

## 3. When done

Read the run file back to Claudia and Mical. Then tell Mical: "The run file is at Documents/lingua-viva-home-run-2026-09-08.md — send it to PC-23." Do not upload it anywhere yourself.
