Dashku
===

![Dashku Screenshot](https://raw.github.com/Anephenix/dashku/master/dashku-screenshot.png)

Introduction
---

Dashku is a web application for creating dashboards and widgets in HTML, CSS, and JavaScript. It is open source, and available to download from Github.


Dependencies
---

- Node.js (0.10)
- MongoDB
- Redis

Installation
---

    git clone git://github.com/jtbonhomme/dashku.git
    cd dashku
    npm install

ps: in case of error during <code>bcrypt</code> installation with npm (<code>gyp ERR! stack Error: `gyp` failed with exit code: 1</code>), simply remove <code>~/.node-gyp</code> directory

Booting the application
---

    mongod &
    redis-server &
    npm start

ps: run an local instance on port <code>3000</code>

pps: to mitigate with <code>authentication.signedIn 'caller', 'callee', and 'arguments' properties may not be accessed on strict mode functions or the arguments objects for calls to them</code> error, remove <code>'use strict';</code> directive in  <code>node_modules/socketstream/lib/request/responders/rpc/request.js</code> file. See https://github.com/Anephenix/dashku/issues/54.



Seeding the database with widget templates
---

You can seed Dashku's database with widget templates by running this command:

    npm run populateWidgetTemplates

Using Dashku to create dashboards and widgets
---

Documentation will be coming soon.

Testing
---

To run unit and functional tests:

    npm test

To run the integration tests:

    npm run cuke

License & Credits
---

&copy; 2014 Anephenix Ltd. The Nike swoosh is a registered trademark of Nike Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
