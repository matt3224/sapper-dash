# Repro

To see the issue, clone this repo and run `npm i` then `npm run dev`

If i include a script tag for dash in `src/template.html` things work as expected, however importing it as a module within a route or component (see `src/routes/index.svelte`) gives the following error:

```Module specifier, 'stream' does not start with "/", "./", or "../".```

with the dev command flagging these items also:

```bash
'stream' is imported by node_modules/sax/lib/sax.js, but could not be resolved – treating it as an external dependency
'string_decoder' is imported by node_modules/sax/lib/sax.js, but could not be resolved – treating it as an external dependency
'stream' is imported by stream?commonjs-external, but could not be resolved – treating it as an external dependency
'string_decoder' is imported by string_decoder?commonjs-external, but could not be resolved – treating it as an external dependency
```

Thanks!
