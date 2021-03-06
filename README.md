# Edge Hugo Theme

Edge is a Hugo theme for personal cycling websites. Originally built for my own site at https://cycling.paluchowski.com. For the time being it's very underdeveloped, because the blog that runs it has very litle content. With time, as the blog grows so will this theme, with more features. 

## Installation

Clone the repository to your `/themes` directory, ie.

```shell
$ cd /your/hugo/site
$ git clone https://github.com/mpaluchowski/hugo-edge themes/edge
```

Build the [SASS](http://sass-lang.com/) files in `/assets/css`:

```shell
$ cd themes/edge
$ sass --no-source-map --style=compressed --update assets:assets
```

Then tell Hugo to render your site with the theme:

```shell
$ hugo --theme=edge
```

## Customization

The theme is built primarily for my own use, so while it does offer some configuration and customization options, it will often impose a certain structure on you.

## Shortcodes

### `strava-activity`

Renders a single [Strava](https://www.strava.com) activity:

```go
{{< strava-activity id="840057488" hash="6a93a704064cb3cf22b266a1698cf9870fd1765a" >}}
```

Where `id` and `hash` are values you'll get when you open an activity, open the "Embed on Blog" dialog, which'll offer you an `IFRAME` code, with the values baked into the URL:

```html
<iframe height='405' width='590' frameborder='0' allowtransparency='true' scrolling='no' src='https://www.strava.com/activities/<id>/embed/<hash>'></iframe>
```
