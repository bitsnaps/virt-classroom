# Virtual Classroom with Vue-WebRTC

Steps to create this project:

## Project setup (vue-cli required)
```
vue create virt-classroom
cd virt-classroom
npm install vue-webrtc --save
```

## Add vue-webrtc component to your div#app in your template:
```
<vue-webrtc ref="webrtc" width="100%" roomId="sample-room"/>
```

### Add this lines to your App.vue in <script>:
```
import Vue from 'vue'
import WebRTC from 'vue-webrtc'

import * as io from 'socket.io-client'
window.io = io

Vue.use(WebRTC)
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
