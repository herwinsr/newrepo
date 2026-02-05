 partner-onboarding@R002.3.0.0.42 dev
> cross-env NODE_ENV=development nodemon src/index.js

[nodemon] 3.1.11
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,cjs,json
[nodemon] starting `node src/index.js index.js`
node:internal/modules/cjs/loader:1146
  throw err;
  ^

Error: Cannot find module 'puppeteer'
Require stack:
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\controllers\legal_team\legalTeam_api\convertHtmlCodeToPdf_DNU.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\controllers\legal_team\legalTeam_api\index.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\controllers\legal_team\index.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\controllers\index.js       
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\routes\configuration\country\countryRoutes.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\routes\configuration\index.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\routes\index.js
- C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\index.js
    at Module._resolveFilename (node:internal/modules/cjs/loader:1143:15)
    at Module._load (node:internal/modules/cjs/loader:984:27)
    at Module.require (node:internal/modules/cjs/loader:1231:19)
    at require (node:internal/modules/helpers:179:18)
    at Object.<anonymous> (C:\Users\herwinsel.v\Tops\TOPS onboarding\topspartneronboarding\modules\Partner-Onboarding\src\controllers\legal_team\legalTeam_api\convertHtmlCodeToPdf_DNU.js:11:19)
    at Module._compile (node:internal/modules/cjs/loader:1369:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1427:10)
    at Module.load (node:internal/modules/cjs/loader:1206:32)
    at Module._load (node:internal/modules/cjs/loader:1022:12)
    at Module.require (node:internal/modules/cjs/loader:1231:19) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\controllers\\legal_team\\legalTeam_api\\convertHtmlCodeToPdf_DNU.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\controllers\\legal_team\\legalTeam_api\\index.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\controllers\\legal_team\\index.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\controllers\\index.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\routes\\configuration\\country\\countryRoutes.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\routes\\configuration\\index.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\modules\\Partner-Onboarding\\src\\routes\\index.js',
    'C:\\Users\\herwinsel.v\\Tops\\TOPS onboarding\\topspartneronboarding\\index.js'
  ]
}

Node.js v20.12.2
[nodemon] app crashed - waiting for file changes before starting...
