# Hello!

This is @djradon's personal public wiki. Currently built using Dendron. See
https://djradon.github.io/wiki/ for more.

## Build

Latest dendron-cli is broken, so:

```shell
npm install -g @dendronhq/dendron-cli@0.122.0 
```


```shell
rm -rf .next && rm -rf docs; cd public-notes; git pull; cd ..; dendron publish export --target github --yes; git add *; git commit -m "regular update"; git push
```
