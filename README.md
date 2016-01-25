Secret Super Weapon
===================
Secret Super Weapon (SSW) is a turn-based party game built using Typescript
and Meteor. This is currently a work-in-progress.

Getting Started
---------------
* `npm install` to install dependencies. This will call TSD to (re-)install
  DefinitelyTyped definitions.
* `npm run watch` to watch and compile Typescript while running Meteor.

Other Commands
--------------
* `npm run clean` to clean up compiled Typescript files

Build Notes
------------
SSW uses `tsc` to compile Typescript into ES6 modules which are in turn compiled
into a Meteor 1.3 isomorphic app. To distinguish compiled Typescript files from
other Javascript files in the Meteor directory (like `package.js` files) for
the purposes of clean up or excluding files from source control, we append `.m`
to each Typescript module (which means Typescript files end with `.m.ts` or
`.m.tsx` and the compiled Javascript files end with `.m.js`).

This provides some boilerplate code for getting a Meteor 1.3 app with React
and Typescript working. Rather than use a Meteor Isobuild package, we use tsc
to compile Typescript into ES6 directly, and then have Meteor compile the
JS files into the actual Meteor app.
