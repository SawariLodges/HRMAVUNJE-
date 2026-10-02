# Sawari HR Hub (Mavunje)

Employee files, leave, sick leave, salary advances and notices for Sawari Lodges (Namibian Labour Act 11 of 2007).

- Website: GitHub Pages from `main` (root). `index.html` is the whole app.
- Logins and data: Firebase project **SawariLodges** (Authentication: Email/Password, Firestore).
- Works offline: records are kept on each device and sync when the connection is back; `sw.js` keeps the app itself available offline. The first sign-in on a device needs internet.

## Firebase setup (one time)
1. Authentication → Sign-in method → enable **Email/Password**.
2. Authentication → Settings → Authorized domains → add `sawarilodges.github.io`.
3. Firestore Database → Create database (production mode).
4. Firestore Database → Rules → paste `firestore.rules` → Publish.
5. Paste the web app `firebaseConfig` into `index.html` (`FIREBASE_CONFIG`).
6. Open the site: the first person becomes the administrator and adds everyone else on the Users page.

## Roles
- Administrator: everything, plus manages users
- HR: all employee files, leave, sick leave, advances, notices and settings
- Staff: apply for leave and read notices only
