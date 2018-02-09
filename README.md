# named-avatar (doing)

Avatar generated by name text based on svg

## usage

### Requirejs

```html
<img src="" data-avatar="Tom">

<script>
requirejs('namedAvatar', function(namedAvatar){
  namedAvatar(document.querySelectorAll('img[data-avatar]'))
})
</script>
```

### Vue 2.X

```javascript
import { directive } from 'named-avatar'
Vue.directive('avatar', directive);

// vue template
<img v-avatar="Tom" />
```