# jsonnet-lib-test

## Install from another `jsonnet` project using `jb`

```bash
jb install https://github.com/botflux/jsonnet-lib-test@main
```

Create a project using jb

```bash
jb init
```

Create a `main.jsonnet`:

```jsonnet
local helper = import 'github.com/botflux/jsonnet-lib-test/main.libsonnet';

{
  "square_of_4": helper.square(4)
}
```

Generate the final json:

```bash
jsonnet -J vendor main.jsonnet
```
