## Reproduce the issue

```sh
pnpm install
pnpm deploy --filter package-a ./package-a-deployed
# folder "package-a-deployed" contains lodash@4.17.21 in node_modules/.pnpm, although it is not in the dependency graph (lodash is only used by package-b and package-b is not in use by package-a)
```
