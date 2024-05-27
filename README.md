# dita-starter

```
$ docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/test/test-topic.dita -o /src/output/test -f html5 -v
```

```
docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/test/test-map.ditamap -o /src/output/test -f html5 -v --nav-toc=full
```

```
docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/openshift-docs/openshift-enterprise.ditamap -o /src/output/rosa -f html5 -v --nav-toc=full
```


```
docker run --rm -v /workspaces/dita-starter:/src ghcr.io/dita-ot/dita-ot:4.2.3 -i /src/input/openshift-docs/openshift-enterprise-modular.ditamap -o /src/output/rosa -f html5 -v --nav-toc=full
```

```
python3 -m http.server -d output/
```

## Codeblocks

```
./dita-ot/dita-ot-4.2.3/bin/dita --version

./dita-ot/dita-ot-4.2.3/bin/dita install https://github.com/jason-fox/fox.jason.extend.css/archive/master.zip

./dita-ot/dita-ot-4.2.3/bin/dita install https://github.com/jason-fox/fox.jason.prismjs/archive/master.zip

./dita-ot/dita-ot-4.2.3/bin/dita -i input/openshift-docs/openshift-enterprise-modular.ditamap -o ./output/rosa/ -f html5 --nav-toc=full
```

```
./dita-ot/dita-ot-4.2.3/bin/dita uninstall fox.jason.prismjs

```