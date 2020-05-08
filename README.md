# 🌍 Bulwark FM Site

Easily generate a static site for your podcast feed, powered by the feed generated by [bulwarkfm/glue](https://github.com/bulwarkfm/glue).

[![Build site CI](https://github.com/bulwarkfm/site/workflows/Build%20site/badge.svg)](https://github.com/bulwarkfm/site/actions)

[**View example site →**](https://bulwarkfm.github.io/site/)

## 💡 Getting started

1. Set up a repository [using this template](https://github.com/bulwarkfm/site/generate) or fork this repository
2. Clone the repository locally and run the command `npm run setup`
3. To generate your static site, run the command `npm run build`

### Initial setup

![Screen recording of npm run setup](https://user-images.githubusercontent.com/2841780/81385438-f9957200-9130-11ea-9d47-b50aff95119d.gif)

After running `npm run build`, you can manually edit the keys in `package.json` to change the podcast description, theme colors, and sections. For more customization like adding custom sections, see the [Staart Site documentation](https://staart.js.org/site).

### Building site

To build the site, run `npm run build` and serve from the `public` folder. Run `npm run serve` to start a local development server with hot reloading.

We recommend using GitHub Actions to automatically generate and deploy your site to GitHub Pages. You can use the workflow in this repository to get started quickly.

### Example configuration

```json
{
  "@staart/site": {
    "title": "Couples Therapy with Candice and Casey",
    "baseUrl": "https://bulwarkfm.github.io/site",
    "listSubpages": true,
    "ignoreHomeSubpages": true,
    "theme": {
      "headerBackgroundColor": "#7ed6df",
      "headerTextColor": "#000000",
      "textColor": "#002024",
      "linkColor": "#000000",
      "buttonBackgroundColor": "#f9ca24",
      "buttonBackgroundColorLight": "#f6e58d",
      "buttonTextColor": "#000000",
      "doodleFillColor": "#f9ca24"
    },
    "navbar": [
      "<a href='https://bulwarkfm.github.io/site/episodes'>Episodes</a>",
      "<a href='https://bulwarkfm.github.io/site/listen'>How to Listen</a>"
    ],
    "preFooter": [
      {
        "type": "message",
        "style": {
          "background-color": "var(--headerBackgroundColor)",
          "color": "var(--headerTextColor)",
          "padding": "5vh 0 10vh 0"
        },
        "illustration": "dancing",
        "title": "Couples Therapy with Candice and Casey is available wherever you listen to podcasts.",
        "ctaText": "Listen now →",
        "ctaLink": "https://bulwarkfm.github.io/site/listen"
      }
    ],
    "footer": {
      "text": "Hosted by Casey Neistat and Candice Pool",
      "links": [
        "<a href='https://bulwarkfm.github.io/glue/feed.xml'>RSS</a>",
        "<a href='https://bulwarkfm.github.io/glue/meta.xml'>API</a>"
      ]
    }
  },
  "bulwark": {
    "apiUrl": "https://bulwarkfm.github.io/glue"
  }
}
```

## 📄 License

[MIT](./LICENSE) © Bulwark FM