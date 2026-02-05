npm install puppeteer --legacy-peer-deps
npm ERR! code 1
npm ERR! path C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\node_modules\puppeteer
npm ERR! command failed
npm ERR! command C:\Windows\system32\cmd.exe /d /s /c node install.mjs
npm ERR! **INFO** Skipping Firefox download as instructed.
npm ERR! Error: ERROR: Failed to set up chrome v145.0.7632.26! Set "PUPPETEER_SKIP_DOWNLOAD" env variable to skip download.
npm ERR!     at downloadBrowser (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/puppeteer/lib/esm/puppeteer/node/install.js:26:15)
npm ERR!     at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
npm ERR!     at async Promise.all (index 0)
npm ERR!     at async downloadBrowsers (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/puppeteer/lib/esm/puppeteer/node/install.js:84:9) {
npm ERR!   [cause]: Error: All providers failed for chrome 145.0.7632.26:
npm ERR!     - DefaultProvider: Download failed: server returned code 403. URL: https://storage.googleapis.com/chrome-for-testing-public/145.0.7632.26/win64/chrome-win64.zip
npm ERR!       at installWithProviders (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/@puppeteer/browsers/lib/esm/install.js:108:11)
npm ERR!       at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
npm ERR!       at async install (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/@puppeteer/browsers/lib/esm/install.js:118:12)
npm ERR!       at async downloadBrowser (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/puppeteer/lib/esm/puppeteer/node/install.js:14:24)
npm ERR!       at async Promise.all (index 0)
npm ERR!       at async downloadBrowsers (file:///C:/Users/herwinsel.v/Tops/TOPS%20onboarding/topspartneronboarding/node_modules/puppeteer/lib/esm/puppeteer/node/install.js:84:9)
npm ERR! }

npm ERR! A complete log of this run can be found in: C:\Users\herwinsel.v\AppData\Local\npm-cache\_logs\2026-02-05T11_21_34_268Z-debug-0.log
PS C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding> 
