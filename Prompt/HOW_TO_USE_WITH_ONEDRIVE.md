# 📂 How to Use This Prompt with OneDrive

## ✅ You're All Set!

Your game prompt is now in your OneDrive folder. Here's how to use it with the game:

---

## 🔗 Step 1: Get Your OneDrive Share Link

### Option A: Share from OneDrive Web

1. Go to https://onedrive.live.com/
2. Navigate to: `EscapeTheLabGame/Prompt/`
3. Right-click `GameMasterPrompt.txt`
4. Click **"Share"**
5. Select **"Anyone with the link can view"**
6. Click **"Copy link"**

### Option B: Share from File Explorer

1. Open File Explorer
2. Navigate to this folder:
   ```
   C:\Users\wael.ibrahim\OneDrive\EscapeTheLabGame\Prompt\
   ```
3. Right-click `GameMasterPrompt.txt`
4. Click **"Share"** → **"Copy link"**

---

## 🔧 Step 2: Convert to Direct Download Link

Your sharing link will look like:
```
https://1drv.ms/t/s!ABC123xyz
```

**Convert it to direct download format:**

```
https://api.onedrive.com/v1.0/shares/u!ABC123xyz/root/content
```

**How to convert:**
1. Take your sharing code after `s!` (example: `ABC123xyz`)
2. Use this format: `https://api.onedrive.com/v1.0/shares/u![YOUR_CODE]/root/content`
3. Replace `[YOUR_CODE]` with your actual code

**Example:**

If your link is:
```
https://1drv.ms/t/s!AiB2C3D4E5F6G7H
```

Your direct link is:
```
https://api.onedrive.com/v1.0/shares/u!AiB2C3D4E5F6G7H/root/content
```

---

## ⚙️ Step 3: Configure the Game

Edit your game's `appsettings.json`:

```json
{
  "ClaudeApi": {
    "ApiKey": "YOUR_API_KEY_HERE"
  },
  "Game": {
    "TimeLimit": 600,
    "EnableStreaming": true,
    "SaveHistory": true
  },
  "Prompt": {
    "UseCloudPrompt": true,
    "CloudPromptUrl": "https://api.onedrive.com/v1.0/shares/u!YOUR_SHARE_CODE/root/content",
    "CachePrompt": true,
    "FallbackToLocal": true
  }
}
```

---

## 🎮 Step 4: Run and Test

```bash
cd C:\Users\wael.ibrahim\EscapeTheLabGame
dotnet run
```

You should see:
```
🌐 Loading game prompt from cloud...
✓ Cloud prompt loaded successfully!
```

---

## 📝 How to Update Questions

### Easy Updates!

1. **Edit this file** in any text editor:
   ```
   C:\Users\wael.ibrahim\OneDrive\EscapeTheLabGame\Prompt\GameMasterPrompt.txt
   ```

2. **Save changes** - OneDrive syncs automatically

3. **Tell players to restart** the game

4. **Everyone gets the new version!** (after OneDrive syncs)

---

## 💡 Benefits of OneDrive

✅ **Synced across devices** - Edit from anywhere
✅ **Version history** - OneDrive keeps old versions
✅ **Team sharing** - Share with colleagues easily
✅ **Automatic backup** - OneDrive protects your prompts
✅ **Offline access** - Files cache locally

---

## 🎯 Folder Structure

```
C:\Users\wael.ibrahim\OneDrive\
└── EscapeTheLabGame\
    └── Prompt\
        ├── GameMasterPrompt.txt          ← Your prompt file
        └── HOW_TO_USE_WITH_ONEDRIVE.md   ← This guide
```

---

## 🔄 Sync Status

**OneDrive Sync Indicators:**

- ✅ **Green checkmark** - File synced, ready to share
- 🔄 **Blue arrows** - Currently syncing
- ❌ **Red X** - Sync error (check OneDrive)
- ☁️ **Cloud icon** - Online-only (will download when accessed)

**Make sure file shows green checkmark before sharing!**

---

## 📊 Sharing with Your Team

### For Your Team Members:

1. **Share the OneDrive link** (converted to direct download format)
2. **They configure** their `appsettings.json` with the URL
3. **Everyone uses** the same centralized prompt
4. **You update** the file → everyone gets updates

### Example Team Setup:

**You (Organizer):**
- Keep prompt in: `C:\Users\wael.ibrahim\OneDrive\EscapeTheLabGame\Prompt\`
- Share direct link with team
- Update prompt as needed

**Team Members:**
- Get the OneDrive URL from you
- Add to their `appsettings.json`
- Game loads from your OneDrive
- Restart to get updates

---

## ❓ Troubleshooting

### "Failed to load from cloud"

**Check:**
1. Is file shared with "Anyone with link can view"?
2. Is OneDrive sync complete? (green checkmark)
3. Is URL format correct? Should start with `https://api.onedrive.com/`

### "Access Denied"

**Solution:**
1. Re-share the file
2. Make sure permission is "Anyone with link"
3. Copy new link and update config

### File not updating

**Possible causes:**
1. OneDrive not synced yet (check sync status)
2. Game using cached version (delete `Cache/cached_prompt.txt`)
3. Players haven't restarted game

**Solution:**
1. Wait for green checkmark (synced)
2. Tell players to delete cache and restart
3. Verify changes in OneDrive web

---

## 🎉 You're Ready!

Your prompt is now in OneDrive and ready to use!

**Next steps:**
1. Share the file in OneDrive
2. Get the direct download URL
3. Add to game config
4. Test with `dotnet run`

**That's it!** Update the file anytime, and everyone gets the new version! ☁️

---

## 📚 Additional Resources

- **CLOUD_SERVICES_GUIDE.md** - Detailed OneDrive instructions
- **CLOUD_PROMPT_GUIDE.md** - Complete cloud prompts guide
- **README.md** - Main game documentation

---

**Current File Location:**
```
C:\Users\wael.ibrahim\OneDrive\EscapeTheLabGame\Prompt\GameMasterPrompt.txt
```

**Enjoy your cloud-powered game!** 🎮☁️
