# SCOS.java — Smart Campus Operating System

A Java-inspired, student-first campus workspace with a responsive dashboard for academics, attendance, timetable, events, notices, library and campus services.

## Visual system
- **Space Grotesk** for the interface and **JetBrains Mono** for code-inspired labels, metadata and the Java login panel.
- Dark/light themes; the selected theme is remembered in the browser.
- Responsive navigation, mobile-friendly login and accessible keyboard focus styles.
- Student-only demo entry point.

## Run locally
Open `index.html` in a browser, or run:

```bash
python -m http.server 5173
```

Visit `http://localhost:5173/`.

## Demo access
- Email: `student@scos.demo`
- Password: `demo1234`
- Access: Student workspace only

The demo uses fictional records stored in the browser. It does not require a running backend.

## Deploy to Vercel
1. Import this GitHub repository into Vercel.
2. Select **Other** as the Framework Preset and set Root Directory to `./`.
3. Leave Install Command and Build Command empty.
4. Set Output Directory to `.` if requested, then deploy.

The repository's `vercel.json` configures static hosting headers. The root `index.html` is the Vercel entry point.

## Java backend
The Spring Boot / Java 21 backend remains in `src/`. Vercel serves the static student demo and does not run Spring Boot. For live API-backed data, deploy the Java service and database separately, then connect a production frontend using an explicit API base URL and CORS configuration.
