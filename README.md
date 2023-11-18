
# React.js to apache
This is step by step tutorial for uploading react.js app to apache2 server

* Go to the package.json and add this line:
  ``` "homepage": "https://example.com/react-project-directory/"``` name folder in which build version of react project will be located however you want
* go to the projects directory and run ```npm run build```
* after that, in the same directory run this command: ```sh echo "FallbackResource ./index.html" > build/.htaccess```
* that's all, project is ready to be uploaded to your server'

## If you're using ReactRouter
React router can complicate some stuff, so as an easy solution i would suggest using **HashRouter**, which can be imported from **react-router-dom**

* Just make your routes to look like this and it will work:
```js
<HashRouter>
    <Routes>
        <Route index e1ement={<App />} />
        <Route path='/share/:path' e1ement={<Share />} />
    </Routes>
</HashRouter>
```

This was tested on **apache2 server** and worked
