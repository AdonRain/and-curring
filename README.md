#and-currying

a better way to get obj's prop without eggache(蛋疼).

##effect

if you have to do:

```
var movieName = res && res.body && res.body.data && res.body.data.movieName;
```

you can:

```
var ac = require('and-currying');
var movieName = ac(res)('body.data.movieName');
```

when a prop is  undefined, you will get:

```
{
    error: 'end at theUndefinedProp'
}
```
