# Code!

Yes, here is some code:

```js
// Authentication endpoints.
app.get('/login',
  passport.authenticate('auth0', { connection: nconf.get('AUTH0_CONNECTION') }),
  function(req, res) { });
app.get('/login/callback',
  passport.authenticate('auth0'),
  function(req, res) { res.redirect('/'); });
app.get('/logout',
  function(req, res) {
    req.session.destroy();
    req.logout();
    res.redirect('/');
  });
```
