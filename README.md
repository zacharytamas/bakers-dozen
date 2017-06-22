# bakers-dozen

A Baker's Dozen Solitaire game.

This is a semester project for the Software Engineering course at Kennesaw State University.

## Contributors:

- [Zachary Jones](https://github.com/zacharytamas)
- [Stanley Gilstrap](https://github.com/Stangil)
- [Dewong Lucas Jr](https://github.com/Dewonglucas11)
- [Matthew Hull](https://github.com/mattdhull94)
- [Anthony Lee](https://github.com/anthonylee83)

## Developing

To develop on this project you'll need:

- Git. You probably already have this if you've made it this far.
- Node.js with `npm`. How to install this will vary by your platform.
- Bower. Newly deprecated but this is where Google publishes Polymer's code for now. We're moving to NPM eventually. Install with `npm install -g bower`
- Polymer CLI. This is a handy tool for developing Polymer. It includes a linter, bundler, static server, etc. Install with `npm install -g polymer-cli`

### Typical lifecycle

When developing you can start the built-in Polymer server with:

    polymer serve

It'll start a local web server you can open in your web browser. It's usually something like [http://127.0.0.1:8081](http://127.0.0.1:8081) but the port number might be different depending on what else you have running on your machine.

*TODO(zachary)* Need to finish documenting the other parts of the lifecycle such as `polymer build`. This isn't really needed until we are cutting production builds of the app.
