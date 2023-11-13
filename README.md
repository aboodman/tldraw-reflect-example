# tldraw-reflect-example

This repository shows how you might use [tldraw](https://github.com/tldraw/tldraw) together with the [reflect](https://reflect.net/) library.

## Develop

```
npm run dev
npx reflect dev // in separate terminal
```

## Publish

```
npx reflect publish // modify .env VITE_REFLECT_SERVER
```

## TODO

- Right now this demo has a non-optimal "double-update": tldraw tells Reflect about a change it has _already made_, then Reflect turns around and tells tldraw to make the change again. The perf impact small and there's no correctness issue, but it's inelegant. It would be nice to see if there's an easy "controlled" interface that could be submitted to tldraw to fix this.
- This demo generates its own patch on each mutator, but tldraw already has this info internally. Can we get it? Or submit a PR to get it?
- Demonstrate support for custom shapes + migration via Reflect mutators and roomStart event handler.
