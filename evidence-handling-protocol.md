# Evidence Handling Protocol: Digital and Physical Evidence in a Copyright Complaint

**Audience:** a junior team member collecting evidence for a copyright matter.
**Purpose:** collect evidence lawfully, keep it unaltered, and record enough about it that a court can be asked to rely on it.

> Written for this fictional portfolio exercise. It is a working method, not legal advice. Before using it on a real matter, a supervising lawyer should confirm it against current law and the practice of the court concerned.

## 0. Ground rules

1. **A screenshot alone does not establish authenticity, ownership or infringement.** It shows what one screen displayed at one moment. It does not show who controls the website or account, when the content was first posted, whether the image is the claimant's file or a similar one, or who owns the copyright. Each of those needs separate proof (see section 10).
2. **Collect lawfully, or not at all.** Only look at what is publicly available or what the client lawfully holds. Do not:
   - access any account, system or area you are not authorised to access, including by guessing passwords or using someone else's login;
   - pretend to be someone else (pretexting) to obtain information;
   - make deceptive or "test" purchases using a false identity without a supervising lawyer's advice (ordinary purchases in your own name are fine);
   - scrape a website in breach of its terms;
   - record calls, follow people, or monitor anyone's private activity.
3. **Originals are never edited.** Annotations, crops and highlights go on working copies.
4. **Write it down as you go.** Every action on evidence goes in the evidence register and the custody log, at the time.
5. **Treat personal data carefully.** Collect only what is needed, restrict access, and redact before sharing.

## 1. Source and provenance

For every item, record in `templates/evidence-register.csv`:
- where it came from (URL, shop, email account, device, person);
- who obtained it, and how;
- whether it is first-hand (we captured or received it directly) or second-hand (someone forwarded it);
- for forwarded items, who the original sender was and whether we can get the original file.

Second-hand items, like a forwarded screenshot, are leads. Try to recapture the content first-hand.

## 2. URL, date and time of capture

- Record the full URL as shown in the address bar, including any query string.
- Record the date and time in **IST (UTC+05:30)** and say so, for example `2025-01-16T15:12:00+05:30`.
- Make sure the device clock is set to automatic network time before capturing.
- Keep the URL bar and system clock visible in the capture where possible.

## 3. Screenshots and full-page context

Capture in layers:
1. **Full-page capture** (browser "save as PDF" or full-page screenshot), not just the visible screen.
2. **The specific item** (for example, the banner) at the highest resolution available.
3. **The underlying file**, where publicly served: save the image file the page loads, and save the page source (HTML), which shows the file name and location.
4. **Context:** the "about" or "contact" page showing who runs the site; the account's profile page for social media.

**What a screenshot cannot show:** whether the page looked the same to other users or at other times; whether the image is the claimant's original file or a recreation; who uploaded it; how long it was live; whether the capture itself was edited. Corroborate with the steps in section 10.

## 4. Original files and metadata

- Keep original files exactly as received or created. Copy, never move.
- Metadata (for example, camera date and serial number in a photograph) is useful but **easy to alter**. Common editing software can change dates and fields, and re-saving a file changes its modification date. Treat metadata as supporting evidence, never as proof on its own.
- Record metadata observations in a separate note (see E-04 in the fictional pack) and keep the original file alongside.
- Ask for camera-original (RAW) files from the photographer where authorship is in issue.

## 5. File naming and version control

Use one pattern for every file:

```
YYYYMMDD-HHMM_<EvidenceID>_<short-description>_<type>_v<version>.<ext>
```

Example: `20250116-1512_E-08_pebblequay-home_capture_v1.pdf`

- The time is the capture time in IST.
- `v1` is always the original. Working copies get `annotated_v1`, `annotated_v2`, and so on.
- Never reuse a version number. Never overwrite.

## 6. Chronological event log

Keep a running event log (`templates/chronology-template.csv`): each event, its date, how certain the date is, who acted, and which evidence items support it. Record dates that are only asserted by the other side as allegations, not facts.

## 7. Preserving originals separately

```
matter-folder/
├── originals/   read-only; hashed; nobody edits
├── working/     copies for annotation and analysis
└── register/    evidence register, custody log, event log
```

- Set `originals/` to read-only after each addition.
- Keep a second copy of `originals/` on separate storage.
- Never put real evidence in a public repository. The `.gitignore` in this project excludes `originals/`, `working/` and similar folders for that reason.

## 8. Access restrictions and personal data

- Limit access to the matter team.
- Mark each item in the register: personal data present (Yes/No) and what kind.
- Redact phone numbers, bank details and names of uninvolved people in working copies shared outside the team. Keep the unredacted original in `originals/`.
- The Digital Personal Data Protection Act, 2023 contains an exemption for processing necessary to enforce a legal right or claim (s. 17(1)(a)). Secondary sources report that this section and most operative provisions commence on 13 May 2027. Minimise and protect personal data regardless.

## 9. Chain of custody

For each item, the custody log records every handover: date and time (IST), from whom, to whom, purpose, and the hash value checked at handover. Physical items (such as a purchased product) go in a sealed, labelled bag with the purchase bill; record who opened the bag and why, each time.

## 10. Integrity verification with SHA-256

**What a hash is, in plain English.** A hash function reads every byte of a file and produces a short fixed-length "fingerprint". SHA-256 produces 64 hexadecimal characters. If even one byte of the file changes, the fingerprint changes completely. If you hash the file today and again in a year and get the same value, the file has not changed in between. A hash does not show who made the file or whether its contents are true; it shows only that the file is the same file.

**One example command (Linux or macOS terminal):**

```
sha256sum .gitignore
```

On Windows PowerShell the equivalent is `Get-FileHash .gitignore -Algorithm SHA256`.

**Worked example from this repository.** Running the command above on this repository's `.gitignore` file, as delivered on 30 October 2026, printed:

```
51fb76d03caafa1e9aff72a3d3aff66ae0cbbe5c85a8c53350b0facc71842395  .gitignore
```

This value was actually computed from the file. If you edit `.gitignore`, the value will change, which is exactly what a hash is meant to show.

**Practice:**
- Hash each original at capture or receipt; record the value in the register (`sha256_hash`) with `hash_status` = `COMPUTED`.
- Re-hash at each handover and before filing; record a match or mismatch.
- Any value that was not computed from a real file must be marked as a placeholder, as in the EXAMPLE rows of `evidence-register.csv`.
- Under s. 63(4) of the Bharatiya Sakshya Adhiniyam, 2023, a certificate in the form of the Schedule must accompany an electronic record each time it is submitted for admission. Commentary and the Supreme Court's order in *Pune Bar Association v. Union of India* (2026) describe the Schedule as requiring the hash value, with a part for the party and a part for an expert. Hashing at capture makes that certificate possible later.

## 11. Limits of screenshots, web archives and third-party tools

| Tool | Useful for | Limits |
|---|---|---|
| Screenshot / full-page capture | What a page displayed at a moment | Easily edited; one viewer's view; no proof of who controls the page or since when |
| Public web archives | Showing a page existed on an earlier date, from a third party | Not every page or date is archived; images may not be captured; the archive's own reliability may need proof |
| Third-party capture services | Independent, timestamped capture | Depends on the provider's process and records; may need a witness or certificate from the provider; check terms of use |
| Page source (HTML) and served file | Shows the actual file name and location | Pages change; content delivery networks may serve different files to different users |
| Metadata | Supporting dates and devices | Editable; changed by re-saving; camera clocks may be wrong |

## 12. Corroboration needed for each proposition

| Proposition | A screenshot shows | Corroboration needed |
|---|---|---|
| The content was really on the site | One display at one time | Independent or archived capture; page source; the other side's admission |
| The site or account is the respondent's | A name or logo | Domain or account ownership records; the respondent's own pages linking to it; admission |
| The date of use | The capture date only | Archives; platform post dates; the respondent's records |
| The image is the claimant's work | Visual resemblance | The served file compared with the original; expert comparison; the respondent's source files |
| The claimant owns the copyright | Nothing | Contracts, assignments, the author's testimony, original files |
| The use was unlicensed | Nothing | Licence documents and their construction |

## 13. Before you finish each collection session

- [ ] Every new file is in `originals/`, hashed, and in the register.
- [ ] Custody log updated.
- [ ] Event log updated.
- [ ] Personal data flagged.
- [ ] Nothing collected by any method listed under ground rule 2.
