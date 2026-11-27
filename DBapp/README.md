# DB Navigator Next-Gen — Baden-Württemberg Interactive Prototype

An interactive web & mobile UI prototype reimagining **Deutsche Bahn's DB Navigator** across **all of Baden-Württemberg** (*bwtarif* + DB Regio + 22 Regional Transit Associations), built around suggested-plus-editable multi-leg route planning, **Deutschlandticket** filtering, **interactive transit cartography**, **geospatial bus city-center bearings**, and operational **News & Alerts**.

## Live Website Deployment (GitHub Pages)

This project is a **100% static client-side web application** (HTML5 + CSS3 + bundled JS with live HTTPS CORS calls to `v6.db.transport.rest` and built-in offline simulation). No backend server or API keys are required.

### Option A: Upload via GitHub Web Interface (No Git CLI Required)
1. Sign in to [github.com](https://github.com) and click **New repository** (e.g., `db-navigator-bw-prototype`, set to **Public**).
2. Click **uploading an existing file** on the empty repository screen.
3. Select **all files and folders** inside this `projectDB` folder (`index.html`, `css/`, `js/`, `.nojekyll`, `README.md`, `build_bundle.py`) and drag them into the upload box, then click **Commit changes**.
4. Open **Settings → Pages** in your GitHub repository.
5. Under **Build and deployment → Source**, select **Deploy from a branch**, choose **`main`** and **`/ (root)`**, and click **Save**.
6. Within ~60 seconds, your live website will be published at:
   `https://<your-github-username>.github.io/<repository-name>/`

*(Desktop visitors see the interactive presentation companion panel + smartphone frame; mobile visitors on iPhone/Android automatically get a full-screen native-style web app!)*

### Option B: Run Locally
* **Direct File Open:** Double-click `index.html` in File Explorer (`js/bundle.js` runs without a server).
* **Local Web Server:** Double-click `start_prototype.bat` or run `python -m http.server 8765` and visit `http://localhost:8765`.
* **Rebuilding after JS edits:** If you modify modular source files inside `js/`, run `python build_bundle.py` to update `js/bundle.js`.

---

## Core Features

1. **Suggested + Modular Route Builder (`Build Route` tab)**
   * Pick **From**, **To**, and optional **Via** stops across 55 Baden-Württemberg stations, start from **Best Suggested / Fastest / Alt Corridor** presets, and customize any leg (`⇄ Swap Ride`, `⊕ Add Stop / Detour`, transfer buffer chips, `+ Add Another Leg`).
2. **Interactive Baden-Württemberg Transit Map**
   * Displays state borders, *Schwarzwald* & *Schwäbische Alb*, rivers (*Rhein, Neckar, Donau*), *Bodensee*, color-coded multi-leg route polylines, pan/zoom, and tap-any-station routing.
3. **Deutschlandticket Statewide Filter**
   * Excludes paid `ICE`/`IC` Fernverkehr in one tap while keeping `RE`, `IRE`, `MEX`, `S-Bahn`, `U-Bahn`, and all 22 BW Verbund bus networks.
4. **Bus Schedules & City-Center Bearing Radar (`Buses` tab)**
   * Tags local buses across 9 BW cities (*Stuttgart, Heidelberg, Mannheim, Karlsruhe, Freiburg, Ulm, Tübingen, Konstanz, Heilbronn*) as **→ Toward City Center (*Stadteinwärts*)**, **← Away from Center (*Stadtauswärts*)**, or **↻ Cross-Town (*Querverbindung*)** with a live bearing radar map.
5. **BW Rail & Mobility News (`News` tab)**
   * Covers *bwtarif & Deutschlandticket*, *Stuttgart 21* hub transfer advisories, *Rheintal / Schwarzwald* connections, and live API remarks.
