# Node.js Setup Guide
### TechFest 2026 · OpenClaw Workshop · Pre-requisite

> **Install Node.js 24 LTS, then verify with `node -v` and `npm -v`.**

OpenClaw requires Node.js v22.19+ — **Node 24 LTS is recommended.**
Current LTS release: **Node.js v24.16.0** with npm **11.13.0**.

After installation, open Terminal (Mac/Linux) or PowerShell (Windows) and check:
```bash
node -v    # should say v24.x.x
npm -v     # should say 11.x.x
```
If both show those versions, you're ready. Skip everything else on this page.

---

## Mac — Option 1: Official installer (easiest, recommended for beginners)

1. Go to **nodejs.org/en/download**
2. Select **Node.js 24 LTS**
3. Download the **macOS installer** (`.pkg` file)
4. Open the `.pkg` → click through the installer
5. Open Terminal and verify:

```bash
node -v
npm -v
```

> This installs Node.js and npm directly on your Mac, like any normal app. No extra tools needed.

---

## Mac — Option 2: `nvm` (recommended for developers)

`nvm` (Node Version Manager) lets you install multiple Node versions and switch between them per project — useful if you work on multiple projects with different Node requirements.

**Install nvm:**
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash
```

**Load nvm in your current terminal:**
```bash
. "$HOME/.nvm/nvm.sh"
```

**Install and use Node 24:**
```bash
nvm install 24
nvm use 24
nvm alias default 24
```

**Verify:**
```bash
node -v
npm -v
```

> `nvm alias default 24` makes Node 24 the default for every new terminal window — do this or you'll need to run `nvm use 24` every session.

---

## Mac — Option 3: Homebrew (if you already have it)

```bash
brew install node@24
brew link --overwrite --force node@24
echo 'export PATH="/opt/homebrew/opt/node@24/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
node -v
```

> If `node -v` still shows an old version after this, close the terminal completely and open a fresh one — the PATH change needs a new session.

---

## Windows — Option 1: Official installer (easiest, recommended for beginners)

1. Go to **nodejs.org/en/download**
2. Select **Node.js 24 LTS**
3. Download the **Windows Installer** (`.msi` file)
4. Open the installer → keep all default options → Finish
5. Open **Command Prompt** or **PowerShell** and verify:

```powershell
node -v
npm -v
```

> After installation Windows will recognize `node` and `npm` from any terminal window. No PATH changes needed.

---

## Windows — Option 2: `nvm-windows` (recommended for developers)

Standard `nvm` is Mac/Linux only. Windows developers should use **nvm-windows** instead (recommended by Microsoft).

> ⚠️ **Important:** If you have a previous Node.js installation, uninstall it first — mixing old installs with a version manager causes confusing PATH conflicts.

**Install nvm-windows:** download the installer from [github.com/coreybutler/nvm-windows/releases](https://github.com/coreybutler/nvm-windows/releases) → run `nvm-setup.exe`

**Then in PowerShell:**
```powershell
nvm install 24.16.0
nvm use 24.16.0
node -v
npm -v
```

> For workshop beginners on Windows, the `.msi` installer is simpler. Use nvm-windows only if you're already comfortable with the command line.

---

## Verification — all platforms

Once Node is installed, these are the only commands you need to know for this workshop:

| Command | What it does |
|---|---|
| `node -v` | Check Node.js version |
| `npm -v` | Check npm version |
| `npm install` | Install project dependencies |
| `npm run dev` | Start local dev server |
| `npm run build` | Build the project |
| `npm start` | Start the app (if project defines a start script) |

---

## The one-liner for attendees

```
Install Node.js 24 LTS from nodejs.org.
Open Terminal or PowerShell. Run: node -v and npm -v.
If you see v24.x.x and 11.x.x — you're ready.
```

Mac and Windows users run the **same npm commands** once Node is installed — Node provides the common runtime across both operating systems.

---

*Back to the main handout: see `ATTENDEE-HANDOUT.md` or scan the QR code at the workshop.*
