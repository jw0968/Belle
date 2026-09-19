# Zelle (Chase) send-money clone

Single-file, dependency-free recreation of the Chase app's *Send money with Zelle®* flow:
Zelle® hub → Select Recipient (or Add Recipient) → Enter Amount → Confirmation → back to the hub (Pay again + Money sent activity).

- **Run locally:** open `index.html`, or use the VS Code launch config (`Run and Debug → Preview Zelle clone`),
  which serves the folder on `http://localhost:5173` and opens Chrome at phone size.
- **Add to your iPhone home screen** from Safari to hide the browser chrome (the page pads for the notch and home indicator itself).
- **Demo settings** (recipient nickname, registered name, phone/email handle, amount, balance, profile photo) live behind the
  gear icon (top-right of the Zelle hub) and the "Zelle® settings" row. Everything is stored in `localStorage`.
- Sends are recorded to "Money sent activity" on the hub (newest first, three most recent) and the recipient appears under "Pay again"; tapping a Pay-again contact starts a new send to them.
- Random incidental details: the checking account's last four digits and the initials on the filler contacts are randomised
  once and persisted; "Re-roll" in settings regenerates them.

No network calls are made and nothing is looked up online: Zelle has no public profile pages, so the recipient is
entirely driven by the settings page.
