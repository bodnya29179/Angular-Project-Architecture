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
    │   │   ├── app-routing.module.ts (optional)
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
    │   │   ├── 📁 pipes
    │   │   │   ├── 📁 <pipe name>
    │   │   │   │   ├── <pipe name>.pipe.spec.ts
    │   │   │   │   └── <pipe name>.pipe.ts
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
    │   │   ├── reset.scss
    │   │   ├── styles.scss
    │   │   └── index.scss
    │   │
    │   ├── index.html
    │   └── main.ts
    │
    ├── .editorconfig
    ├── .eslintrc.json
    ├── .gitignore
    ├── angular.json
    ├── karma.conf.js
    ├── proxy.conf.json (optional)
    ├── package.json
    ├── package-lock.json
    ├── tsconfig.app.json
    ├── tsconfig.json
    ├── tailwind.config.js
    └── README.md
```

## Additional notes

### The `core` folder

**Description:**
\
In many projects, the `core` folder is often used to store services and components that are considered
fundamental to the application's core functionality, such as authentication services, global data services, and
application-wide components like the main navigation bar.

**General usage:**
\
The key here is to maintain consistency and clarity in your project structure. If the distinction between `core`
and `shared` doesn't serve your project's needs, it's perfectly fine to eliminate the `core` folder and place everything
in the `shared` or other relevant folders. Ultimately, the goal is to have a structure that makes it easy for developers to
understand and navigate the codebase.

**Architectural choice:**
\
The distinction between `core` and `shared` doesn't provide any meaningful separation in the project, it's perfectly
valid to opt for a flatter structure.

Arguments for not using the core folder in the project:

* **Simplicity and Consistency:**
  \
  Having fewer folders and a flatter structure can make the project easier to navigate and
  understand for both new and existing developers. It simplifies the mental model required to locate and manage
  different parts of the code.


* **Reduced Redundancy:**
  \
  Placing all shared components, services, and other elements in a single `shared` folder can
  eliminate the redundancy introduced by maintaining both a `core` and a `shared` folder. This reduction in duplication
  can lead to cleaner and more maintainable code.


* **Flexibility in Organizing:**
  \
  With a flat structure, you have the flexibility to organize your code based on logical
  modules or features rather than forcing components into predefined `core` and `shared` categories. This can be
  especially helpful as your project evolves and its structure naturally adjusts to new requirements.


* **Easier Refactoring:**
  \
  Without the `core` folder, you won't have to worry about moving code between `core` and other
  folders during refactorings or changes. This can save time and effort, as well as reduce the risk of breaking the
  application.


* **Clarity in Responsibility:**
  \
  In many cases, the line between what constitutes `core` functionality and what belongs in `shared` can become blurred.
  Placing everything in `shared` emphasizes that all components and services are equally
  important and contributes to a more balanced understanding of the codebase.


* **Ease of Onboarding:**
  \
  For new team members, a simpler folder structure can speed up the onboarding process. They won't
  need to learn the nuances of distinguishing between `core` and `shared` items.


* **Maintainability:**
  \
  As the project grows, a flat structure can help prevent the creation of sprawling subfolders. This
  can lead to better maintainability and improved performance in version control systems.


**Summary**
\
In summary, eliminating the `core` folder simplifies the project structure, reduces redundancy, and allows for greater
flexibility in organizing and maintaining the codebase. It aligns with the principle of simplicity and can lead to a
more efficient development process.
