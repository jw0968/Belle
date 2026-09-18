# Zelle (Chase) send-money clone

Single-file, dependency-free recreation of the Chase app's *Send money with Zelle®* flow:
Select Recipient → Enter Amount → Confirmation → Activity.

- **Run locally:** open `index.html`, or use the VS Code launch config (`Run and Debug → Preview Zelle clone`),
  which serves the folder on `http://localhost:5173` and opens Chrome at phone size.
- **Add to your iPhone home screen** from Safari to hide the browser chrome (the page pads for the notch and home indicator itself).
- **Demo settings** (recipient nickname, registered name, phone/email handle, amount, balance, profile photo) live behind the
  person icon at the top-left of the home screen. Everything is stored in `localStorage`.
- Sends are recorded to the Activity list on the home screen (newest first, relative timestamps, "Send again").
- Random incidental details: the checking account's last four digits and the initials on the filler contacts are randomised
  once and persisted; "Re-roll" in settings regenerates them.

No network calls are made and nothing is looked up online: Zelle has no public profile pages, so the recipient is
entirely driven by the settings page.
