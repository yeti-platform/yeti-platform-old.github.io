# yeti-platform.github.io
Website / Blog

## Start local dev server with docker

```
git clone yeti-platform/yeti-platform.github.io
cd yeti-platform.github.io
docker run --rm -v $(pwd):/src  -p 1313:1313 klakegg/hugo:ext-alpine server
```
