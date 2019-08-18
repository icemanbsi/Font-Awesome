This library contains a dart package useful to develop web-applications
using `fontawesome` icons

# The iconic font and CSS framework

Font Awesome is a full suite of 675 pictographic icons for easy scalable
vector graphics on websites, created and maintained by \[Dave
Gandy\](<https://twitter.com/davegandy>). Stay up to date with the
latest release and announcements on Twitter:
\[@fontawesome\](<http://twitter.com/fontawesome>).

Get started at \<<https://fontawesome.com/>!>

# Usage in Web and CSS

1 - Create a new project with next structure:

    [project_root]
      ├─ analisys_options.yaml
      ├─ pubspec.yaml
      ├─ web
      │  ├─ index.html
      │  ├─ style.css
      │  └─ ... other files and folders ...

2 - In the `pubspec.yaml` file add the `font_awesome` dependency as
below:

```yaml
name: web_css_sample
description: An absolute bare-bones web app.

environment:
  sdk: '>=2.4.0 <3.0.0'

dependencies:
#  font_awesome: any # uncomment and change for latest version

dev_dependencies:
  build_runner: ^1.5.0
  build_web_compilers: ^2.1.0
  pedantic: ^1.7.0
```

3 - In `styles.css` file import the css file from `font_awesome`
library:

```css
@import url(https://fonts.googleapis.com/css?family=Roboto);

@import url(/packages/font_awesome/css/all.css); /* font_awesome css file is imported here */

html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

#output {
  padding: 20px;
  text-align: center;
}
```

4 - In `index.html` add the needed component and classes:

```html
<!DOCTYPE html>

<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="scaffolded-by" content="https://github.com/google/stagehand">
    <title>web_css_sample</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="favicon.ico">
    <script defer src="main.dart.js"></script>
</head>

<body>

  <div id="output"></div>

<!--  Next code will show an icon star from font_awesome library-->
  <p>
      Star Icon: <i class="fa fa-star"></i>
  </p>
</body>
</html>
```

5 - Run next command to start development server:

```sh
webdev serve --auto refresh
```

6 - Once you are ready to build and deploy your project run next
command:

```sh
webdev build
```

# Usage in Web and Sass

1 - Create a new project with next structure:

    [project_root]
      ├─ analisys_options.yaml
      ├─ pubspec.yaml
      ├─ web
      │  ├─ index.html
      │  ├─ style.scss
      │  └─ ... other files and folders ...

2 - In the `pubspec.yaml` file add the `font_awesome` and `sass_builder`
dependencies as below:

```yaml
name: web_sass_sample
description: An absolute bare-bones web app.
# version: 1.0.0
#homepage: https://www.example.com
#author: luis <luisvargastijerino@gmail.com>

environment:
  sdk: '>=2.4.0 <3.0.0'

dependencies:
#  font_awesome: any # uncomment and change for latest version

dev_dependencies:
  build_runner: ^1.5.0
  build_web_compilers: ^2.1.0
  pedantic: ^1.7.0
  sass_builder: ^2.1.2
```

> **Note**
> 
> During development `sass_builder` compiles the `scss` files whenever
> they change and generates a bundled `css` file that only exist in
> memory. During final build it generates a `css` file in the `build`
> folder.

3 - In `styles.css` file import the css file from `font_awesome`
library:

```css
@import url(https://fonts.googleapis.com/css?family=Roboto);

// If fonts are in different location change the path with next line:
// $fa-font-path:         "/<path to your>/font_awesome/webfonts" !default;

// We import font_awesome sass files here
@import "package:font_awesome/scss/fontawesome";
@import "package:font_awesome/scss/solid";

html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

#output {
  padding: 20px;
  text-align: center;
}
```

4 - In `index.html` add the needed component and classes:

```html
<!DOCTYPE html>

<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="scaffolded-by" content="https://github.com/google/stagehand">
    <title>web_sass_sample</title>
    <link rel="stylesheet" href="styles.css"> <!-- We import the `styles.css` file instead `styles.scss` -->
    <link rel="icon" href="favicon.ico">
    <script defer src="main.dart.js"></script>
</head>

<body>

  <div id="output"></div>

  <!--  Next code will show an icon star from font_awesome library-->
  <p>
      Star Icon: <i class="fa fa-star"></i>
  </p>
</body>
</html>
```

5 - Run next command to start development server:

```sh
webdev serve --auto refresh
```

6 - Once you are ready to build and deploy your project run next
command:

```sh
webdev build
```

# License

  - The Font Awesome font is licensed under the SIL OFL 1.1:

  - <http://scripts.sil.org/OFL>

  - Font Awesome CSS, LESS, and Sass files are licensed under the MIT
    License:

  - <https://opensource.org/licenses/mit-license.html>

  - The Font Awesome documentation is licensed under the CC BY 3.0
    License:

  - <http://creativecommons.org/licenses/by/3.0/>

  - Attribution is no longer required as of Font Awesome 3.0, but much
    appreciated:

  - `Font Awesome by Dave Gandy - http://fontawesome.io`

  - Full details: <http://fontawesome.io/license/>

# Contributing

Please read through our [contributing
guidelines](https://github.com/FortAwesome/Font-Awesome/blob/master/CONTRIBUTING.md).
Included are directions for opening issues, coding standards, and notes
on development.

# Author

  - Email: <dave@fontawesome.io>

  - Twitter: <http://twitter.com/davegandy>

  - GitHub: <https://github.com/davegandy>

## Dart Package Maintainer

  - Luis vargas: <luisvt@github.com>
