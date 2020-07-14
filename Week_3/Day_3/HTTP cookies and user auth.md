# HTTP Cookies & user Authentication


resiter form in express example.
```
// this will display the register form to the user.
app.get('/register', (req, res) => {
  res.render('registerejs')
})
```

in the form on the ejs template, take note of the action and set the action POST. 
IF we want to catch that POST request, we need to catch the submit to our 

```
app.post('/register, (req, res) => {
  // extract the user info from the form (see below)
  // check if the user already exists in the users db
  // add the user in the users db
      --> generate ID
      --> create new user obj => value assiociated with the id
      --> add new user obj to the users db
      --> return user ID
  // set the user id in the cookie 
  // redirect to another page ( GET  /quote example).
});
```

## Extract from URL, use:
`req.params`

<br>

### extract from the form
the `name` attribute in the HTML form/input, is `catchable` on server side in `req.body`!
example:
```
const name = req.body.name
const email = req.body.email
const password = req.body.password
```
or (ES6 syntax):
```
const {name, email, password} = req.body
```