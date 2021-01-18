# 🔥 L1T Stack

Liquid, 11ty, Tailwind stack.

## 💾 Installation

1. `nvm use`
2. `npm install`
3. `npm start`
4. <http://localhost:8081>

## 🖥 Commands

### dev

1. `npm start`
2. <http://localhost:8081>

### build

Build production version of the site.

1. `npm run build`
2. output goes to `./dist`

### serve

Serve the `./dist` directory.

1. `npm run serve`
2. <http://localhost:3000>

### clean

Delete the `./dist` folder and `./src/styles/`.

1. `npm run clean`

### Notes on build process

#### Dev

1. Gulp runs PostCSS to build Tailwind to `./src/styles.css`
2. Eleventy runs and links to css at `./src/styles.css`
3. Gulp watches for changes to `.src/postcss/`
4. Eleventy watches for changes to lots of files including the output of gulp css to `.src/styles`

#### Production

1. CSS is built via PostCSS in production mode (which purges unused Tailwind classes) via Gulp
2. Then Eleventy runs in production mode
3. Gulp inlines and minifys CSS, JS, HTML from the eleventy output

## ♿️ Accessibility

- [Lighthouse](https://developers.google.com/speed/pagespeed/insights/?url=)
- [Web accessibility evaluation tool](https://wave.webaim.org/report#/)

**Note on viewport**  
To get 100% on accessibility under the Lighthouse metric you need to update the `viewport` meta tag to be:

```
<meta name="viewport" content="width=device-width, minimum-scale=1, maximum-scale=5" />
```

I've chosen not to do this as it causes the site to zoom in frequently while tapping the UI.

## 📚 References

- [eleventy](https://www.11ty.dev)
- [tailwind css](https://tailwindcss.com)
- [gulp](https://gulpjs.com)
- [liquid](https://liquidjs.com)
- [nvm](https://github.com/nvm-sh/nvm)

## 👾 Icons

Icons and hero image made using [Figma](https://www.figma.com).

[Design Document](#LINK_HERE)

## 🌎 Hosting

- CI & Hosting on [Netlify](https://www.netlify.com).
- [GoSquared](https://www.gosquared.com) analytics added as post processing step in Netlify.

## 🗺 Roadmap

- [ ] replace name in readme
- [ ] update site name in `./src/_data/site.js`
- [ ] add apple touch icon to `./src/assets`
- [ ] add favicon to `./src/assets`
- [ ] add figma doc link to readme
- [ ] deploy site
- [ ] add deploy badge to readme
- [ ] add analytics & update readme
- [ ] add url to Lighthouse in Accessibility
- [ ] add url to WAVE in Accessibility

---

If you find this project useful you can donate:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/G2G33AMQO)
