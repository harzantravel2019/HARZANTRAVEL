# HARZAN TRAVEL Accounting System

A static web-based travel-agency accounting system built for **HARZAN TRAVEL**.

## Included Pages

- `Dashboard` for totals, recent activity, and balance overview
- `Clients` for adding, editing, and deleting client records
- `Debts & Payments` for posting ledger entries
- `Debt & Payment History` for reviewing transaction history by client
- `Login` for email/password access and Google sign-in

## Web Deployment

- The project is fully static HTML, CSS, and JavaScript
- It is designed for **GitHub Pages** hosting
- Accounting data and authentication are handled by **Supabase**
- No Node server or desktop app version is used anymore

## Publish On GitHub Pages

1. Push this project to a GitHub repository
2. Keep the default branch as `main` or `master`
3. Open `Settings > Pages` in GitHub
4. Set the source to `GitHub Actions`
5. Push changes and let [.github/workflows/pages.yml](D:/AI/.github/workflows/pages.yml) deploy the site
6. Your live URLs will be similar to:
   - `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`
   - `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/login.html`

## Supabase Setup

1. Open your Supabase project for `HARZAN TRAVEL`
2. Go to `SQL Editor`
3. Run [supabase/schema.sql](D:/AI/supabase/schema.sql)
4. Go to `Authentication > Providers`
5. Enable `Email`
6. Enable `Google` if you want Google sign-in
7. Go to `Authentication > URL Configuration`
8. Add your allowed redirect URLs, including:
   - `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/login.html`
9. The app uses:
   - Project ref: `zubzqddtxdbzmhacrqqh`
   - URL: `https://zubzqddtxdbzmhacrqqh.supabase.co`
   - Publishable key from [supabase-config.js](D:/AI/assets/js/supabase-config.js)

## Notes

- Accounting data is loaded from Supabase
- The app requires Supabase authentication before any accounting page loads
- Closing the browser tab logs the user out automatically
- Re-run [supabase/schema.sql](D:/AI/supabase/schema.sql) if you previously used the older open-anon policy version
- Statements are exported through the browser print dialog using **Save as PDF**
- Deleting a client also deletes that client's ledger records
- [404.html](D:/AI/404.html) is included for cleaner GitHub Pages behavior
