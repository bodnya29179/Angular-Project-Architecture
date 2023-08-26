# Angular Project Architecture

## Small & Middle Architecture

```bash
.
└── 📁 project
    ├── 📁 scripts
    │   ├── <file name>.js
    │   └── ...
    │
    ├── 📁 src
    │   ├── 📁 app
    │   │   ├── 📁 pages
    │   │   │   ├── 📁 <page name>
    │   │   │   │   ├── 📁 components
    │   │   │   │   │   ├── ...
    │   │   │   │   │   └── index.ts
    │   │   │   │   │
    │   │   │   │   ├── 📁 services
    │   │   │   │   │   ├── ...
    │   │   │   │   │   └── index.ts
    │   │   │   │   │
    │   │   │   │   ├── 📁 interfaces
    │   │   │   │   │   ├── ...
    │   │   │   │   │   └── index.ts
    │   │   │   │   │
    │   │   │   │   ├── 📁 store
    │   │   │   │   │   ├── 📁 actions
    │   │   │   │   │   │   ├── <actions group name>.actions.ts
    │   │   │   │   │   │   ├── ...
    │   │   │   │   │   │   └── index.ts
    │   │   │   │   │   │
    │   │   │   │   │   ├── 📁 effects
    │   │   │   │   │   │   ├── <effects group name>.effects.ts
    │   │   │   │   │   │   ├── ...
    │   │   │   │   │   │   └── index.ts
    │   │   │   │   │   │
    │   │   │   │   │   ├── 📁 reducers
    │   │   │   │   │   │   ├── <reducer name>.reducer.ts
    │   │   │   │   │   │   ├── ...
    │   │   │   │   │   │   └── index.ts
    │   │   │   │   │   │
    │   │   │   │   │   ├── 📁 selectors
    │   │   │   │   │   │   ├── <selectors group name>.selectors.ts
    │   │   │   │   │   │   ├── ...
    │   │   │   │   │   │   └── index.ts
    │   │   │   │   │   │
    │   │   │   │   │   └── index.ts
    │   │   │   │   │   └── state.ts
    │   │   │   │   │
    │   │   │   │   └── <page name>.module.ts
    │   │   │   │
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── app.component.html
    │   │   ├── app.component.spec.ts
    │   │   ├── app.component.ts
    │   │   └── app.module.ts
    │   │
    │   ├── 📁 shared
    │   │   ├── 📁 components
    │   │   │   ├── 📁 <component name>
    │   │   │   │   ├── <component name>.component.html
    │   │   │   │   ├── <component name>.component.scss
    │   │   │   │   ├── <component name>.component.spec
    │   │   │   │   └── <component name>.component.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 directives
    │   │   │   ├── 📁 <directive name>
    │   │   │   │   ├── <directive name>.directive.spec.ts
    │   │   │   │   └── <directive name>.directive.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 services
    │   │   │   ├── 📁 <service name>
    │   │   │   │   ├── <service name>.service.spec.ts
    │   │   │   │   └── <service name>.service.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 guards
    │   │   │   ├── 📁 <guard name>
    │   │   │   │   ├── <guard name>.guard.spec.ts
    │   │   │   │   └── <guard name>.guard.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 interceptors
    │   │   │   ├── 📁 <interceptor name>
    │   │   │   │   ├── <interceptor name>.interceptor.spec.ts
    │   │   │   │   └── <interceptor name>.interceptor.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 utils
    │   │   │   ├── 📁 <util name>
    │   │   │   │   ├── <util name>.util.spec.ts
    │   │   │   │   └── <util name>.util.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 interfaces
    │   │   │   ├── <interface name>.interface.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 types
    │   │   │   ├── <type name>.type.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 enums
    │   │   │   ├── <enum name>.enum.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 constants
    │   │   │   ├── <constant name>.const.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── 📁 store
    │   │   │   ├── 📁 actions
    │   │   │   │   ├── <actions group name>.actions.ts
    │   │   │   │   ├── ...
    │   │   │   │   └── index.ts
    │   │   │   │
    │   │   │   ├── 📁 effects
    │   │   │   │   ├── <effects group name>.effects.ts
    │   │   │   │   ├── ...
    │   │   │   │   └── index.ts
    │   │   │   │
    │   │   │   ├── 📁 reducers
    │   │   │   │   ├── <reducer name>.reducer.ts
    │   │   │   │   ├── ...
    │   │   │   │   └── index.ts
    │   │   │   │
    │   │   │   ├── 📁 selectors
    │   │   │   │   ├── <selectors group name>.selectors.ts
    │   │   │   │   ├── ...
    │   │   │   │   └── index.ts
    │   │   │   │
    │   │   │   └── index.ts
    │   │   │   └── state.ts
    │   │   │
    │   │   ├── shared.module.ts
    │   │   └── public-api.ts
    │   │
    │   ├── 📁 assets
    │   │   ├── 📁 animations
    │   │   │   ├── <file name>.json
    │   │   │   └── ...
    │   │   │
    │   │   ├── 📁 fonts
    │   │   │   └── 📁 <font name>
    │   │   │       ├── <font name>-Regular.ttf
    │   │   │       ├── <font name>-Bold.ttf
    │   │   │       ├── <font name>-Light.ttf
    │   │   │       ├── <font name>-Italic.ttf
    │   │   │       └── ...
    │   │   │
    │   │   ├── 📁 i18n
    │   │   │   ├── <language code>.json
    │   │   │   └── ...
    │   │   │
    │   │   ├── 📁 icons
    │   │   │   └── <file name>.svg
    │   │   │   └── ...
    │   │   │
    │   │   ├── 📁 images
    │   │   │   ├── <file name>.png
    │   │   │   ├── <file name>.jpg
    │   │   │   ├── <file name>.jpeg
    │   │   │   └── ...
    │   │   │
    │   │   ├── 📁 sprite
    │   │   │   └── svg-sprite.svg
    │   │   │
    │   │   └── favicon.ico
    │   │
    │   ├── 📁 environments
    │   │   ├── 📁 endpoints
    │   │   │   ├── <api name>-endpoints.ts
    │   │   │   ├── ...
    │   │   │   └── index.ts
    │   │   │
    │   │   ├── environment.ts
    │   │   └── environment.prod.ts
    │   │
    │   ├── 📁 styles
    │   │   ├── 📁 mixins
    │   │   │   ├── <file name>.scss
    │   │   │   ├── ...
    │   │   │   └── index.scss
    │   │   │
    │   │   ├── 📁 variables
    │   │   │   ├── <file name>.scss
    │   │   │   ├── ...
    │   │   │   └── index.scss
    │   │   │
    │   │   ├── 📁 buttons
    │   │   │   ├── <file name>.scss
    │   │   │   ├── ...
    │   │   │   └── index.scss
    │   │   │
    │   │   ├── 📁 inputs
    │   │   │   ├── <file name>.scss
    │   │   │   ├── ...
    │   │   │   └── index.scss
    │   │   │
    │   │   ├── 📁 placeholders
    │   │   │   ├── <file name>.scss
    │   │   │   ├── ...
    │   │   │   └── index.scss
    │   │   │
    │   │   └── index.scss
    │   │
    │   ├── index.html
    │   ├── main.ts
    │   └── style.scss
    │
    ├── .editorconfig
    ├── .eslintrc.json
    ├── .gitignore
    ├── angular.json
    ├── karma.conf.js
    ├── package.json
    ├── package-lock.json
    ├── tsconfig.app.json
    ├── tsconfig.json
    ├── tailwind.config.js
    └── README.md
```
