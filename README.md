# Split

Split is a single page, centrally-divided layout for a professional online presense with a big image or video left with alongside content. It is a port of [Split](https://onepagelove.com/split) by [One Page Love](https://onepagelove.com).

This Hugo theme features an image or video visual section as well as a content section for your name, tagline, bio, and links.

![Hugo Split Theme screenshot](https://raw.githubusercontent.com/escalate/hugo-split-theme/master/images/screenshot.png)

## Installation

Inside the folder of your Hugo site run:

```bash
$ cd themes
$ git clone https://github.com/escalate/hugo-split-theme.git
```

For more information read the official [setup guide](https://gohugo.io/getting-started/quick-start/) of Hugo.

## Getting started

After installing the Split theme successfully it requires a just a few more steps to get your site finally running.

### The config file

Take a look inside the [`tests`](https://github.com/escalate/hugo-split-theme/tree/master/tests) folder of this theme. You'll find some example configurations. To use one of them, copy the `hugo.toml` in the root folder of your Hugo site. Feel free to customize this theme as you like.

### Add content

#### Homepage

Add a file named `_index.md` inside content directory to create your homepage. Use TOML configuration elements to set `title` and `tagline` of your page. Simple write your content in markdown style.

```bash
$ hugo new content/_index.md
```

```markdown
+++
title = "Jenny Jones"
tagline = "Designer. Stylist. Nomad."
+++

Donec at libero id lectus porta dapibus eu in nibh. Cras id mauris sapien. Fusce viverra [luctus urna]({{< ref "long-text.md" >}}) ac rutrum. Duis semper elit eu mi facilisis eleifend. Donec semper, [ipsum in]({{< ref "commonmark.md" >}}) malesuada congue, purus sem ullamcorper massa, sit amet lacinia nibh enim sed massa.
```

#### Additional pages

You can create additional pages as usual inside content directory.

```bash
$ hugo new content/long-text.md
```

```markdown
+++
title = "Long Text"
+++

Aenean posuere, tortor sed cursus feugiat, nunc augue blandit nunc, eu sollicitudin urna dolor sagittis lacus. Donec elit libero, sodales nec, volutpat a, suscipit non, turpis. Nullam sagittis. Suspendisse pulvinar, augue ac venenatis condimentum, sem libero volutpat nibh, nec pellentesque velit pede quis nunc.
```

### Use an image

Set `enable` to `true`. Add your image to the `static` folder and change `file` to the location of your image accordingly. By default the image position is centered, however you can specify your own by supplying `position` with a valid CSS position.

```toml
[[params.visual.image]]
  enable = true
  file = "images/background.jpg"
  position = "center center"
```

You can control displaying of the image on a per-page basis by configuring `visual.image.enable` on each respective page's FrontMatter:

```markdown
+++
visual.image.enable = false
+++

# Privacy statement
```

### Use a video

First, disable the image by setting `enable` to `false` in `[params.visual.image]`.

Second, enable the video by setting `enable` to `true` in `[params.visual.video]`.

You can either use a video that you host or one that is on YouTube.

Just like with [an image](#use-an-image) you can not display a video altogether on particular pages by setting `visual.video.enable = false` in the page's FrontMatter.

##### Use your own video

Add your video to the `static` folder and change `file` to the location of your video accordingly. Make sure you delete `youtubeId` or comment it out.

```toml
[[params.visual.image]]
  enable = false
  ...
[params.visual.video]
  enable = true
  mute = true
  file = "videos/background.mp4"
  # youtubeId = "dk9uNWPP7EA"
```

##### Use a YouTube video

Get the ID of the YouTube video and add it to `youtubeId`. Make sure you delete `file` or comment it out.

```toml
[[params.visual.image]]
  enable = false
  ...
[params.visual.video]
  enable = true
  mute = true
  # file = "videos/background.mp4"
  youtubeId = "dk9uNWPP7EA"
```

##### Add Custom CSS

Put custom css styles in static/css/style.css and enable this css in the config:

```toml
[params.custom.css]
  enable = true
```

##### Additional settings

Set `mute` to `true` if you want the video to play muted and `false` if you want the sound. The video is coded to autoplay and loop. If you want to change that the code can be found in [`layouts/partials/video.html`](https://github.com/escalate/hugo-split-theme/tree/master/layouts/partials/video.html).

### Add links

You can have up to 3 column lists in the links section. `heading` is the list heading text. For the text links `text` is the link text and `url` is the link url. Follow the same snippet structure to add more links to a list. If you only want 1 or 2 lists, just remove the link list snippet you don't want.

This is what generates one link list:

```toml
# Links List #1
[[params.links]]
  [params.links.list1]
    heading = "Connect"

    [[params.links.list1.link]]
      text = "Blog"
      url = "#"
      new_tab = true # new tab

    [[params.links.list1.link]]
      text = "Email"
      url = "#"
      new_tab = false # Default, open at same tab

    [[params.links.list1.link]]
      text = "Newsletter"
      url = "#"
```

### Add metadata

`author` and `description` metadata helps search engines with how to display your site in search results. `shareImage` and `twitterHandle` help improves how your content is displayed when your site is shared across social media sites.

```toml
[params]
  author = "Jenny Jones"
  description = "Split is a centrally-divided layout for a professional online presence with a big image or video left with alongside content."
  shareImage = "images/social.jpg"
  twitterHandle = "onepagelove"
```

### Add favicon

Replace [`static/favicon.ico`](https://github.com/escalate/hugo-split-theme/tree/master/static/favicon.ico) with your favicon. If you don't want just delete `favicon.ico` and the line below.

```toml
favicon = "favicon.ico"
```

### Add copyright

Set `copyright` with the text you want for your copyright.

```toml
copyright = "&copy;2024 Your Name"
```

### Add Google Analytics

Enable Google Analytics by adding your tracking id to `services.googleAnalytics`. Leave empty or remove if you don't want.

```toml
[services]
  [services.googleAnalytics]
    ID = "UA-XXXXXXXX-1"
```

### Nearly finished

In order to see your site in action, run Hugo's built-in local server.

```bash
$ hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.

## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](https://github.com/escalate/hugo-split-theme/issues) to let me know. Or make directly a [pull request](https://github.com/escalate/hugo-split-theme/pulls). See also the [Contributing](./CONTRIBUTING.md) notes.

## License

The original template is released under the [Creative Commons Attribution 3.0 License](https://github.com/escalate/hugo-split-theme/blob/master/LICENSE.md). Please keep the original attribution link when using for your own project. If you'd like to use the template without the attribution, you can check out the license option via the template [author's website](https://onepagelove.com/split).

To deactivate the license text after purchase, set the value of the variable `licensed` to `true`.

```toml
[params]
  licensed = true
```

## Annotations

- Original [Split](https://onepagelove.com/split) Template by [One Page Love](https://onepagelove.com)
- [Girl Image](https://unsplash.com/photos/pAs4IM6OGWI) by [Joe Gardner](https://unsplash.com/@josephgardnerphotography)
- [Clouds Over Mountain Video](http://www.wedistill.io/videos/clouds-over-the-mountain-hd-stock-video) by John Guinn
- Video integration CSS ninja skills by my bud [Manu](https://twitter.com/manuelmoreale)

Also thanks to [Steve Francia](https://github.com/spf13) for creating [Hugo](https://gohugo.io) and the awesome community around the project.
