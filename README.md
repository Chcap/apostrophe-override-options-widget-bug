# Bug with apostrophe-override-options

To reproduce the bug:

1. Install the project by running `npm install`
2. Add user by running `node app.js apostrophe-users:add admin admin`
3. Launch the application with `node app`
4. Goto http://localhost:3000/login and login with `admin/admin`
5. On the home page, add the widget "My Example" and click "Save My Example"
6. You should see "My example option: []"
7. Reload the page: "My example option: [\"foo\"]"

Here is the bug: the option is not visible after widget insert/update, but it is on page loading
