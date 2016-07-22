# NPM Scripts
Nuggets on how to use NPM Scripts as your build tool.

The Node Package Manager and the package.json file in combination makes a great option for build automation.
Using npm and package.json is simpler and has no extra dependencies such as Gulp and Grunt for example.

# Why NPM Scripts
* JavaScript all the things
* Cut down on dependencies
* Use any NPM script (Remember to --save-dev)
* Always up to date
* No need to learn extra plugins

# Create package.json
```$ npm init```

# Example
```
{
  "name": "npm-scripts-as-build-tool",
  "version": "1.0.0",
  "description": "Example package.json file",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Running test script\"",
    "start": "echo \"Running start script\"",
    "stop": "echo \"Running stop script\"",
    "restart": "echo \"Running restart script\"",

    "start:dev": "echo \"My dev script\""
  },
  "author": "Terkel Gjervig",
  "license": "MIT",
  "keywords": [
    "npm",
    "scripting"
  ]
}
```

# Invoke commands
NPM provides a couple of shorthands for invoking commands.
To list all commands in package.json run ```npm run```
```
# Start shorthand
$ npm start

# Test shorthands
$ npm test
$ npm tst
$ npm t

# Start and restart
$ npm stop
$ npm restart

# Everything else
$ npm run myscript
```
If you haven't defined ```npm restart```, NPM  will run stop and then start.


# Pre-  and Post  hooks
You can run pre and post hooks before and after a script.
A hook is just another script, prefixed with pre or post.
Hooks are just like any other scripts, and you can run them directly with npm run. The order in which you define them doesn't matter.
```
  "scripts": {
    "premyscript": "echo \"Pre script\"",
    "myscript": "echo \"Running script\"",
    "postmyscript": "echo \"Running post script\""
  },
```

# Snippets

```&&``` Chaining commands (Waits for each command to finish successfully before starting the next).
Similar to ```pre-``` or ```post-``` hooks

```|``` Piping output

```>``` Output to file

Use Parallelshell to run commands in parallel:
https://github.com/keithamus/parallelshell (Cross platform)

Break large commands into spereate files:
For example:
```
  "scripts": {
    "myscript": "bash ./deployProd.sh",
    "callscript": "npm run myscript"
  },
```

# Complex Scripts
[coming]

# NPM Config Variables
[coming]

# Version Bumping
npm version - shows current version
```
  "scripts": {
    "version:major": "npm version major",
    "version:minor": "npm version minor",
    "version:patch": "npm version patch"
  },
```

# Tools
* Nodemon
* https://github.com/Qard/onchange
* https://www.npmjs.com/package/cross-env
* https://www.npmjs.org/package/rimraf

# Links
* http://substack.net/task_automation_with_npm_run
* https://medium.com/@dabit3/introduction-to-using-npm-as-a-build-tool-b41076f488b0#.jz1v3so41
* https://css-tricks.com/why-npm-scripts/


# Help
This is a work in progress.
Got any tips? Feel free to contribute.
