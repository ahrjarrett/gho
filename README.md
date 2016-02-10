> sass app/assets/sass/screen.scss:app/assets/css/screen.css
(above command compiles sass)

>here ghost is setup as an npm dependency for local development with a gulp configuration to manage tasks

# get started

**make sure you have the lts version of node set up**

$ brew tap homebrew/versions
$ brew install homebrew/versions/node4-lts
$ brew unlink node
$ brew link node4-lts
- $ node -v

**insert your theme name**
- replace 'FollowClosely' with name of your theme in package.json
- replace 'FollowClosely' with name of your theme in /gulp/tasks/init.js
- replace 'FollowClosely' with name of your theme in /gulp/tasks/symlink.js

**from the new directory fire up ghost as follows**

- $ npm install
- $ gulp init
- $ gulp ghost
- navigate your browser to 127.0.0.1:2368
- access admin area by going to 127.0.0.1:2368/ghost


## notes

- init.js: this task should only be run once for every npm install & before starting our local ghost instance
- symlink.js: added as a dependency in init.js so the two run at the same time (once)
- symlink.js: symbolic link created from app directory to content/themes, so changes in this dir are reflected where ghost pulls theme data