# SCOS Interactive Student Demo

A polished, Java-inspired Smart Campus OS student experience. The standalone demo is static HTML, CSS and JavaScript; sample records are stored in the browser with `localStorage`. It does not require a running Spring Boot backend.

## Run locally

Open `index.html` in a modern browser, or serve the project root:

```bash
python -m http.server 5173
```

Then visit `http://localhost:5173/`. The same experience is available at `prototype/index.html`.

## Student demo sign-in

- Email: `student@scos.demo` (any valid email address is accepted)
- Password: `demo1234`
- Access: Student workspace only

The session is stored in the current browser tab. Demo data changes are saved in that browser's local storage. Open **Settings** to reset the sample dataset.

## Deploy to Vercel

1. Push this repository to GitHub and import it in Vercel.
2. Select **Other** as the Framework Preset and keep the Root Directory as `./`.
3. Leave Install Command and Build Command empty. Use `.` as the Output Directory if Vercel asks for one.
4. Deploy. `vercel.json` provides clean URLs and baseline browser security headers; `index.html` serves the student demo at the domain root.

You can also deploy from the project directory with the Vercel CLI:

```bash
npm install --global vercel
vercel
vercel --prod
```

## Java backend note

The Spring Boot / Java 21 backend in `src/` is retained in this repository, but Vercel hosts this front-end demo as a static site. The prototype uses local browser data and does not call the Java API. For live API-backed data, deploy the Spring Boot service and database separately, then connect a production frontend to that API with an explicit API base URL and CORS configuration.

All sample names, events and records are fictional. Intelligence panels are transparent rule-based demonstrations, not machine-learning predictions. Attendance thresholds: below 75% HIGH; 75% to below 90% MEDIUM; 90%+ LOW.
