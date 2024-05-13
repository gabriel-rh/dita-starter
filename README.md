# dita-starter

```
$ docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/test/test-topic.dita -o /src/output/test -f html5 -v
```

```
docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/test/test-map.ditamap -o /src/output/test -f html5 -v --nav-toc=full
```