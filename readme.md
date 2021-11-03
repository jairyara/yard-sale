#Yard Sale

E-commerce for yard sale in your neighborhood.

## Resources

- Desktop design. Click in [guidelines](https://www.figma.com/proto/bcEVujIzJj5PNIWwF9pP2w/Platzi_YardSale?node-id=3%3A2112&amp%3Bscaling=scale-down&amp%3Bpage-id=0%3A998&amp%3Bstarting-point-node-id=5%3A2808).
- Mobile design. Click in [guidelines](https://www.figma.com/proto/bcEVujIzJj5PNIWwF9pP2w/Platzi_YardSale?node-id=0%3A684&amp%3Bscaling=scale-down&amp%3Bpage-id=0%3A1&amp%3Bstarting-point-node-id=0%3A719).
- Scene guidelines. Click in [zeplin](https://scene.zeplin.io/project/60afeeed20af1378ed046538)

## Installation

For this project I use HTML, Postcss, git.

##### Install postcss

```bash
npm install --save-dev postcss-cli postcss
```

Install in dev dependencies, isn't necessary production compile

For use nesting is necessary install nesting plugin

```bash
npm install --save-dev postcss-nesting
```

Create a file .postcssrc (JSON file) with this configuration

```bash
{
  "plugins": {
    "postcss-nesting": true,
    "autoprefixer": true
  }
}
```

In postcss.config.js (JS) 

```bash
module.exports = {
  plugins: {
    "postcss-nesting": true,       /* Nesting CSS */
    "autoprefixer": true           /* CSS Vendor prefixes */
  }
}
```

I use browserslist for major support in this project. For install

```bash
npm install --save-dev browserslist
```

In package.json set next information

```bash
{
  ...
  "browserslist": [ "last 1 versions" ]
}
```

For installation autoprefixer

```bash
npm install --save-dev postcss-cli autoprefixer
```

Activate plugin for use autoprefixer

## Compile postcss

For compilation code traditional mode

- Option 1 - Compile 1 time

```bash
npx postcss index.pcss -u postcss-nesting --no-map -o index.css
```

- Option 2 - Compile watching changes

```bash
npx postcss --watch src/css/style.pcss -o public/css/style.css
```

- Option 3 - Compile using npm

Compiling option 1 using npm

```bash
npm run css
```

Compiling option 2 using npm

```bash
npm run css-watch
```