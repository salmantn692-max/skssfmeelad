# നൂറിന്‍ പ്രഭ · Quiz Competition

## Setup

1. https://console.firebase.google.com ൽ ഒരു project ഉണ്ടാക്കുക.
2. Build → Firestore Database → Create database → "Start in test mode".
3. Project settings → Your apps → Web app (</>) → register ചെയ്ത് firebaseConfig കോപ്പി ചെയ്യുക.
4. index.html തുറന്ന് മുകളിലുള്ള `firebaseConfig` object-ൽ ആ values പേസ്റ്റ് ചെയ്യുക.
5. Firestore → Rules ടാബിൽ:
   ```
   rules_version = '2';
   service cloud.firestore {
     match /databases/{database}/documents {
       match /{document=**} {
         allow read, write: if true;
       }
     }
   }
   ```
6. ഈ repo GitHub-ൽ push ചെയ്ത് Settings → Pages ൽ നിന്ന് GitHub Pages enable ചെയ്യുക (Branch: main, folder: / root).
7. Admin panel password: `skssf2026` (index.html ൽ ADMIN_PASS മാറ്റാം).
