# Snyk submodule problem

Running Maven from the top level doesn't trigger a problem report:

```
$ pwd
~/snyk-problem
$ mvn install
.... build ok
$ ( cd api && mvn install )
.... build fails due to snyk check
```

Note that the first `mvn install` must be executed so parent is
available in the local repository so sub-module can be built individually.

