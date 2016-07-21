# NPM Scripts
Nuggets on how to use NPM Scripts as your build tool. You don't need Grunt or Gulp anymore.

# Why NPM Scripts
* Cut down on dependencies
* Always up to date
* No need to learn extra plugins

# Invoke commands
NPM provides a couple of shorthands for invoking commands.
```
# Start shorthand
$ npm start
$ npm run
$ npm run start

# Test shorthands
$ npm run test
$ npm test
$ npm tst
$ npm t

# Other shorthands
$ npm stop
$ npm restart

# Custom
$ npm run myscript
```

# Post and Pre hooks
[coming]

# Snippets
Sequential/Combining Tasks: && (Waits for each command to finish successfully before starting the next)
You can either use the ```pre-``` or ```post-``` hooks

Parallel: &

Piping: |

Anding:

Or:

Output to file: >

https://github.com/keithamus/parallelshell (Cross platform)

# Complex Scripts

# NPM Config Variables

# Multiplatform

# Version Bumping

# Tools
https://github.com/Qard/onchange

https://www.npmjs.com/package/cross-env

https://www.npmjs.org/package/rimraf

# Links
* http://substack.net/task_automation_with_npm_run
* https://medium.com/@dabit3/introduction-to-using-npm-as-a-build-tool-b41076f488b0#.jz1v3so41
* https://css-tricks.com/why-npm-scripts/
