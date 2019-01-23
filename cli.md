# bash-utils
Personal list of bash utilities and commands for my frontend development

## require_resolve {lib}

> What's the file path that {lib} will resolves to?

```bash
require_resolve() {
  echo "console.log(require.resolve('$1'))" | node
}
```

Usage: `require_resolve react`

## jira XXXX-1234

Quick shortcut to open jira ticket with the number

```bash
jira() {
  open "https://jira.path.com/browse/$1" -a Google\ Chrome
}
```

## gs

Switch git branch faster, see [gs](https://github.com/tanhauhau/gs).

## yx

Run npm commands faster, see [yx](https://github.com/tanhauhau/yx).

## latest_version {lib}
> What is the latest version published of this library?

```bash
latest_version() {
  yarn info $1 --json | jq '.data.versions[-1]'
}
```

Usage: `latest_version react`

See: https://stedolan.github.io/jq/ to install `jq` before use
