# Telugu Fee Collection AI — Downloads

A local Telugu AI voice agent and dashboard for college fee collection. It reads
your student Excel sheet, calls parents in Telugu about pending fees, records
their promised payment date, and lets you export the results.

**No installation needed.** Download the single file for your operating system,
double-click it, and open the dashboard in your browser.

## 1. Download

Get the file for your computer from the **[latest release](../../releases/latest)**:

| Your computer | File |
|---|---|
| Windows | `TeluguFeeAgent-win-x64.exe` |
| macOS (Apple Silicon / M1–M4) | `TeluguFeeAgent-macos-arm64` |
| Linux | `TeluguFeeAgent-linux-x64` |

## 2. Run it

- **Windows:** double-click the `.exe`. If Windows SmartScreen warns, click
  **More info → Run anyway** (the app is safe; it is simply not code-signed).
- **macOS:** right-click the file → **Open** the first time (needed because the
  app is not signed). After that you can open it normally.
- **Linux:** in a terminal: `chmod +x TeluguFeeAgent-linux-x64 && ./TeluguFeeAgent-linux-x64`

Then open **http://localhost:3000** in your browser. To stop the app, close the
black console window (or press `Ctrl+C`).

Your data is saved in a **`data/` folder created next to the program** — back it
up by copying that folder.

## 3. Set up calling (Twilio + Sarvam)

Real phone calls need a Twilio account, a Sarvam AI key, and a public URL. Enter
these in the dashboard's **Settings** page, or create a file named **`.env`**
next to the program using **`.env.example`** in this repository as a guide.

To let Twilio reach the app for live calls, run a tunnel and paste its URL into
`WEBHOOK_BASE_URL`:

```
ngrok http 3000
```

The dashboard, Excel import/export, and in-browser voice simulator work without
any of this; only real outbound phone calls require it.

---

_Having trouble? Contact your vendor._
