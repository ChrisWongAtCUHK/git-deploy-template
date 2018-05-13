# git-deploy-template

> [Deploy Vue to GitHub pages-the easy way!](https://medium.com/@codetheorist/vue-up-your-github-pages-the-right-way-955486220418)

## Build Setup

``` bash
# initialize vue project
vue init webpack git-deploy-template
cd git-deploy-template

# install push-dir package
npm install --save-dev push-dir

# create the default branch for github page
git checkout -b gh-pages

#  add a key to the scripts section `deploy` with the following value
npm run build; push-dir --dir=dist --branch=gh-pages --cleanup

# open the config/index.js file and find the assetsPublicPath entry in the build section, NOT the dev section. Change the value of this to the name of you project on GitHub.
assetsPublicPath: '/git-deploy-template',

```