# webtech-frontend
# clipboard

mounted () {
const endUrl = process.env.VUE_APP_BACKEND_BASE_URL + '/api/v1/guests'
const requestOptions = {
method: 'GET',
redirect: 'follow'
}
fetch(endUrl, requestOptions)
.then(response => response.json())
.then(result => result.forEach(guest => {
this.guests.push(guest)
}))
.catch(error => console.log('error', error))
}

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your unit tests
```
npm run test:unit
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
