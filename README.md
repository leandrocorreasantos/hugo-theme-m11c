# m11c theme

A Hugo minimalistic theme for bloggers (m10c modified)

Main features:

- Fully responsive
- Twitter Cards, Open Graph, Disqus and Google Analytics supported (see Hugo docs)
- Customizable colors
- Customizable picture and description
- Customizable menu on sidebar
- Customizable social media links on sidebar
- Optimized for performance 100/100 on Lighthouse
- All Feather and Simple Icons icons included

## Getting started

### Installation

Requirements:

- Hugo **0.158 or newer**
- [Dart Sass](https://gohugo.io/functions/css/sass/#dart-sass) on your `PATH` (required by Hugo 0.170+, where the extended edition and LibSass were removed)

Create a new Hugo site:
```bash
$ hugo new site [path]
```

Clone this repository into `themes/` directory:
```bash
$ cd [path]
$ git clone https://github.com/leandrocorreasantos/hugo-theme-m11c.git themes/hugo-theme-m11c
```

Add this line  in the `config.toml` file:
```toml
theme = "hugo-theme-m11c"
```

### Configuration

In your `config.toml` file, define the following variables in `params`:

- `author`: Name of the author
- `description`: Short description of the author
- `avatar`: Path of file containing the author avatar image
- `menu_item_separator`: Separator between each menu item. HTML allowed (default: " - ")
- `favicon`: Absolute path of your favicon.ico file (default: "/favicon.ico")

To add a menu item, add the following lines in `menu`:

```
[[menu.main]]
  identifier = "tags"
  name = "Tags"
  url = "/tags/"
```

[Read Hugo documentations](https://gohugo.io/content-management/menus/#readout) for more informations about menu

To add a social link, add the following lines in `params`:

```
[[params.social]]
  icon = "brand-github"
  name = "My Github"
  url = "https://github.com/vaga"
```

Theme colors are defined as SCSS variables at the top of `assets/css/main.scss`.
To customize them in a site without editing the theme, override the generated
rules in the site's `assets/css/_extra.scss` file (the theme imports it last).

### Icons

This theme uses two libraries for icons:

- [Feather](https://feathericons.com/) is used for application-related icons.
- [Simple Icons](https://simpleicons.org) is used for brand icons.

To differentiate brand icons from regular ones, the prefix `brand-` is added
to all icons from the Simple Icons library. (e.g., brand-github, brand-x, brand-mastodon...)

### Styling

To override styles using SCSS, add a file called `_extra.scss` to `[path]/assets/css/`.
This file is imported after all theme styles, so it can override any rule.

The theme compiles SCSS with Hugo's `css.Sass` function. Hugo 0.170 removed the
`hugo_extended` edition and LibSass, so you must install
[Dart Sass](https://gohugo.io/functions/css/sass/#dart-sass) locally and in CI.

## License

This theme is released under the [**MIT**](/LICENSE.md) License.

## Acknowledgements

- [Feather](https://feathericons.com/) - [MIT](https://github.com/feathericons/feather/blob/master/LICENSE)
- [Simple Icons](https://simpleicons.org) - [CC0 1.0](https://github.com/simple-icons/simple-icons/blob/develop/LICENSE.md)
