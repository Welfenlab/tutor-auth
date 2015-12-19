# @tutor/auth

Authentification module for tutor.

## Installation

Via npm (at least version 2 for user packages):

```
npm install --save @tutor/auth
```

## Usage

The package exports a function that creates the necessary express api calls

```js
var authentification = function(name, pw) {
	// you should use a better authentification
	console.error('dummy authentification!')
	return name == pw
};
require('@tutor/auth')(connection, RethinkdbDriver, authentification)
```

You must explicitly pass the connection and the driver. This package uses [`express-session-rethinkdb`](https://github.com/Welfenlab/express-session-rethinkdb)
under the hood and that currently only works if the correct driver is passed through.