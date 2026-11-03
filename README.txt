# ProManage — Firebase Realtime Demo

## Deploy
1. Extract this ZIP.
2. Open the `ProManage` folder.
3. In Netlify, open your existing site → Deploys.
4. Drag the **ProManage folder** into the deploy area to update the existing site.
5. Open the same Netlify link on your laptop and phones. Internet is required.

## Firebase Rules — TEMPORARY DEMO ONLY
This simple version uses no login service for cloud access. To allow it to sync, Firebase Console → Realtime Database → Rules must be set to:

{
  "rules": {
    ".read": true,
    ".write": true
  }
}

Click Publish. WARNING: anyone who discovers the database URL can read, change or delete the demo data. Use only fake test names/passwords and non-confidential files. Do not use these rules for a real/public production system. A real deployment needs Firebase Authentication and role-based rules.

## Demo logins
Admin: `Praga` / `Praga2713`
Users: `USR001` / `Alex123`, `USR002` / `Maya123`, `USR003` / `Ravi123`

## Notes
- Updates to tasks, members and statuses sync to devices using the same deployed website.
- Uploaded files are stored as Base64 in the database; keep them small (the UI limit is 1.5 MB).
- The Firebase web config is visible in browser code by design; database rules must protect data.
