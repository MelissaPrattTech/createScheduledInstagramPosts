# recof-instagram-post-scheduler 📲

A Google Apps Script that automates the creation of Instagram post content for **Real Estate Campus of Florida (RECOF)**. It randomly selects from a list of pre-written captions and media, avoids repeats, and logs the output into a Google Sheet for easy automation with Buffer, Zapier, or other scheduling tools.

---

## 📌 Features

- 🔀 Shuffles a pool of real estate-focused captions and image URLs
- 🖼️ Prevents image reuse until all have been cycled
- 🧾 Logs each post with timestamp, status, media link, and time slot (Morning / Afternoon)
- 🔗 Adds relevant hashtags and link to RECOF homepage
- ⚙️ Designed to work with external schedulers like Buffer or Zapier for auto-posting

---

## 🗂 Sheet: `IG Posts`

| Column | Purpose                                  |
|--------|------------------------------------------|
| A      | Timestamp (date the post was generated)  |
| B      | Instagram caption (text + hashtags)      |
| C      | Image URL                                |
| D      | Instagram Post ID (optional / external)  |
| E      | Status (e.g., "Ready")                   |
| F      | Auto Post flag ("Yes")                   |
| G      | Time Slot ("Morning" or "Afternoon")     |

---

## ✍️ Sample Post Output

**Caption:**
> 📘 Florida requires DBPR-approved courses — we've got you covered.  
> https://www.myrealestatecampus.com  
>  
> #realestate #floridarealestate #realestatelife #dbpr #onlinecourse #womeninrealestate ...

**Image URL:**  
> https://i.imgur.com/XQrR6Mf.png

---

## 🔁 How It Works

1. Loads a list of real estate marketing messages and image URLs.
2. Randomly pairs one message with one image.
3. Ensures no image is repeated until all have been used.
4. Adds hashtags and a link to RECOF’s homepage.
5. Logs two posts per run (morning & afternoon) into the `"IG Posts"` sheet.
6. Tracks used images using Google Script Properties.

---

## ⚙️ Setup Instructions

1. Open your Google Sheet.
2. Create a sheet named `IG Posts`.
3. Go to `Extensions > Apps Script`.
4. Paste in the `createScheduledInstagramPosts()` function (and the `shuffleArray()` helper).
5. Save and run once to test.
6. Set a time-based trigger to run the function daily.

---

## 🛠 Integration Options

You can connect the `"IG Posts"` sheet to any scheduler that supports:
- Reading Google Sheets (e.g., Zapier, Make.com)
- Scheduling Instagram media posts
- Using columns B and C for the caption and image

---

## 🌐 Branding & Hashtags

- All messages are tailored for real estate students and licensees.
- Hashtags include real estate, DBPR, study motivation, and broker licensing keywords.
- Add or edit hashtags in the script for your niche.

---

## 🔐 Privacy & Logging

- No external servers or databases are required.
- All image tracking is managed via the script’s internal `ScriptProperties`.

---

## 📄 License

MIT License – Free to use, modify, and distribute. Attribution appreciated.

---

## 🔗 Website

[https://www.myrealestatecampus.com](https://www.myrealestatecampus.com)
