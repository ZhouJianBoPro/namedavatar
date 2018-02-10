# named avatar (doing)

Avatar generated by name text based on svg

## Setup

```bash
npm install namedavatar
```

```javascript
var namedAvatar = require('namedavatar')

var img = document.querySelector('img#avatar1')

// if img.src invalid, change to data:image/svg+xml avatar uri
namedAvatar.setImg(img, 'Tom Hanks')
```

## Usage

### UMD (Requirejs)

```html
<img data-name="李连杰">
<img src="./invalid.jpg" data-name="Tom Hanks">

<script>
requirejs('namedAvatar', function(namedAvatar){
  namedAvatar.setImgs(document.querySelectorAll('img[data-name]'), 'data-name')
})
</script>
```

### Vue2

```javascript
// mian.js
import { directive } from 'namedavatar'
Vue.directive('avatar', directive);

// vue template
<img v-avatar="'Tom Hanks'" />
```

## API

### .config(Object options)

| filed    | type   | default | description      |
| -------- | ------ | ------- | ---------------- |
| nameType | string | `'firstName'` | pick from: `firstName`, `lastName`, `initials` |
| fontFamily | string | `'Verdana, Geneva, sans-serif'` | font family |
| backgroundColors | Array | Material Design colors *-500 | random background color list |
| textColor | string | `'#FFF'` | name text color |
| minFontSize | number | `8` | min font size limit |
| maxFontSize | number | `16` | max font size limit |

### .getSVG(string name, Object options)

- `name` the full name value
- `options` extended options

### .setImgs(HTMLImageElement[] imgs, string attr)

- `imgs` `<img>` list
- `attr` pick full name value from special attr, eg `'alt'`, `'data-name'`

### .setImg(HTMLImageElement[] img, string name)

- `img` `<img>` item
- `name` the full name value

## Contributing

- IE > 8 (stack `<SVG>`, `Object.assign()`)
- Continuous improvement, welcome review and suggest
