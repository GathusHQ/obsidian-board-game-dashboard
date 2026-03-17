## 📘 **Obsidian Board Game Dashboard — Installation & Setup Guide**

This starter kit gives you a clean, interactive way to track your board game collection inside Obsidian. It includes:

- **Board Game Dashboard** — browse, filter, search, and rate your games
- **Add New Game** — a form that creates new game notes automatically
- **Board Games/** — the folder where all game notes will be stored

Everything runs on **DataviewJS** and core Obsidian features. No external scripts, no QuickAdd, no configuration steps.

---

## 📁 Folder Contents

When you unzip the download, you’ll see:

```
Board Games/   ← Folder where your game notes will live
		Botany.md   ← example game
	Board Game - Add New Game.md
	Board Game - Dashboard.md
	Readme.md
```

---

## 🎨 Theme and Appearance Settings to Match the Screenshots

These settings are optional, but they will make your vault look like the screenshots shown in this guide. They don’t affect functionality—only appearance and layout.

### **Theme**

The screenshots use the **Fancy A Story** theme with these style presets:

- **Board Game Dashboard:** _Art Deco — Light Silver_
- **Movie Dashboard:** _Art Deco — Dark Chocolate_

The dashboards work with any theme; these are just the ones used in the screenshots.

### **Appearance Settings**

These settings affect layout, spacing, and how clean the pages look:

- Appearance → Inline title → **Off**
- Editor → Readable line length → **Off**
- Editor → Properties in document → **Hidden**
- Core plugins → Page preview → **Off**

### **Editor Behavior**

These settings ensure the dashboard and forms open in the correct mode:

- Editor → Default view for new tabs → **Reading view**
- Editor → Default editing mode → **Source mode**

These match the environment used to create the screenshots and help the dashboards display cleanly and consistently.

---

## 🚀 Installation (2 minutes)

Follow these steps:

1. **Unzip the download.**
2. **Copy all three items into the root of your Obsidian vault** (the top level).
	You can skip copying the Readme.md if you’ve already read it or don’t need it in your vault.

```
    Board Games/
		    Botany.md   ← example game
	    Board Game - Add New Game.md
	    Board Game - Dashboard.md
```

3. Open Obsidian and make sure the plugin **Dataview** is installed and enabled.
    - Settings → Community Plugins → Browse → search “Dataview”
    - Enable **Dataview**
    - Settings → Dataview → **Enable JavaScript Queries** (required for the dashboard and form)
4. Open **Board Game Dashboard** or **Board Game – Add New Game** and start using the system.

That’s it. No configuration, no renaming, no plugin setup beyond Dataview.

---

## 📝 How to Add a New Game

1. Open **Board Game – Add New Game.md**
2. Fill out the form fields
3. Click **Create Board Game**
4. A new note will appear inside the `Board Games/` folder

Each note includes:

- YAML metadata
- Cover image
- Description
- Pros & Cons
- Purchase link

The dashboard reads all of this automatically.

---

## 📊 Using the Dashboard

Open **Board Game Dashboard.md** to:

- Browse your collection
- Filter by category
- Search by title
- Page through large collections
- Toggle “Show All” mode
- Click **🎲 Surprise Me!** to open a random game
- Adjust ratings with a slider (saved instantly to the note)

The dashboard updates itself every time you add or edit a game.

---

## 🗂️ Customizing the System (Keep It Simple)

This kit is designed to be easy to use right away — and easy to tweak if you want.

**The safest & most common change: Rename the games folder**  
If you’d rather call it “My Games”, “Collection”, “Boardgames”, or anything else:

1. Open **Board Game - Add New Game.md**  
   Find this line near the top:  
   const BOARD_GAME_FOLDER = "Board Games";  
   Change "Board Games" to your preferred name (keep the quotes).

2. Open **Board Game Dashboard.md**  
   Find this line:  
   const allGames = dv.pages('"Board Games"')  
   Change "Board Games" to match exactly what you picked above.

3. (If you already added games) Rename or move the “Board Games” folder in your vault to the new name.

That’s all it takes — the form will save to the new location, and the dashboard will read from it.

**Want to do more?**  
You can safely edit labels, add/remove tags/categories in the notes themselves, or experiment with the form/dashboard code. Everything is plain text — if something breaks, just replace the file from your backup. For bigger changes (like adding new fields to track), search online for “Obsidian Dataview frontmatter” or “DataviewJS tutorial” — there are tons of friendly guides.

Have fun with your board game collection! 🎲

---

## 🧩 Troubleshooting

**Dashboard is empty**

- Make sure your game notes are inside the `Board Games/` folder
- Make sure Dataview is enabled
- Make sure DataviewJS is enabled

**Images not showing**

- Check that your Cover Image URL is valid
- Try using a direct image link (ending in .jpg or .png)

**Rating slider doesn’t update**

The most common cause is that the game note was edited in a way that removed the information block at the top of the file. Each game page needs that block so the dashboard knows where to save your rating.

To fix it:

- Open the game note
    
- Make sure the top of the file still contains the information section created by the Add Game form
    
- If it’s missing, recreate the game using the form

---

## 🎉 Enjoy Your Board Game Tracker

This system is designed to be simple, clean, and easy to extend. You can customize it as much or as little as you want.
