# Type error with `fallthroughAttributes`

## Install dependencies

```bash
pnpm i
```

## Type check

```
pnpm type-check
```

Should return something like

```
src/App.vue(6,50): error TS2353: Object literal may only specify known properties, and 'status' does not exist in type 'Partial<{}> & Omit<{} & VNodeProps & AllowedComponentProps & ComponentCustomProps, never>'.
src/App.vue(17,18): error TS2353: Object literal may only specify known properties, and 'status' does not exist in type 'Partial<{}> & Omit<{} & VNodeProps & AllowedComponentProps & ComponentCustomProps, never>'.
```
