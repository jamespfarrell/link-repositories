``` 
git clone git@github.com:org/sub-repo.git

npm i

npm link
```

copy the resulting path after the '->'

for example - /home/user/.nvm/versions/node/v11.14.0/lib/node_modules/sub-repo -> ***/home/james/code/org/sub-repo***

Navigate to the root folder of the parent project and run:

Past the path copied above here
``` 
npm link /home/james/code/org/sub-repo

npm install --save /home/james/code/org/sub-repo
```

In package.json under dependencies you should see something like:

```
"sub-repo": "file:../sub-repo",
```
