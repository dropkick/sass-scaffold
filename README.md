# Sass Scaffold

A scaffold or boilerplate Based on [sass-boilerplate](https://github.com/KittyGiraudel/sass-boilerplate/tree/master) by Kitty Giraudel

Each folder of this project has its own `README.md` file to explain the purpose and add extra information.

## Using the indented syntax

### Sass conversion

This boilerplate does not provide a `.sass` version as it would be painful to maintain both versions without an appropriate build process. However, it is very easy to convert this boilerplate to Sass indented syntax.

Clone it, head into the project and then run:

```bash
sass-convert -F scss -T sass -i -R ./  && find . -iname “*.scss” -exec bash -c 'mv "$0" “${0%\.scss}.sass"' {} \;
```

### Use with Sass

When using `sass` - in order to build that boilerplate, one needs to:

- install `sass` if not yet installed:

```bash
npm install -g sass
```

- run build command from command line:

```bash
sass stylesheets/main.scss dist/main.css
```

## Main file

The main file (usually labelled `main.scss`) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@import` and comments.

Reference: [Sass Guidelines](https://sass-guidelin.es/) > [Architecture](https://sass-guidelin.es/#architecture) > [Main file](https://sass-guidelin.es/#main-file)
