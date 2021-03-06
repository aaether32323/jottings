# Jottings

> A featherweight (4kb gzipped) theme for pandoc's html output

[Demo page.](https://a-vrma.github.io/jottings/)

## Usage

Put `jottings.html` in your pandoc template directory and `jottings.css` wherever you like.
Change `{{jottings}}` in `jottings.html` to the path of `jottings.css`. Here is a somewhat
automated way to do that:

```sh
pan_data="$HOME/.local/share/pandoc/templates"
mkdir -p "$pan_data"
curl -fL "https://github.com/a-vrma/jottings/raw/master/test/jottings.css" -o "${pan_data}/jottings.css
curl -fL "https://github.com/a-vrma/jottings/raw/master/jottings.html" |
  sed "s|{{jottings}}|${pan_data}/jottings.css|" >"${pan_data}/jottings.html"
```

You can also copy the content of `jottings.css` to `jottings.html` inside a `style` element
if you want fully standalone files.

## Features

- System font stack.
- Styling for every feature of pandoc's markdown.
- Styles table of contents if used with `--toc`.

## Todo

- View end of table of contents.

## License

MIT/Expat. Includes [normalize.css](https://github.com/necolas/normalize.css)
which is under the same license. See LICENSE file for details.
