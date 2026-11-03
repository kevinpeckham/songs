# Songs

Songs by Kevin Peckham, as Barmark chord charts. **The songs are ©
Kevin Peckham, all rights reserved** (see [COPYRIGHT.md](COPYRIGHT.md)):
this repository is public so the charts can be read and checked, not
reused.

Each chart is a `.chart.md` file in [`songs/`](songs), written in
[Barmark](https://barmark.dev), a plain-text notation for chord charts.

## Checks

On every push and pull request, [`check.yml`](.github/workflows/check.yml)
runs the [`barmark` command](https://www.npmjs.com/package/@barmark/cli)
over `songs/`:

- `barmark check --strict` reads every chart and fails on any error or
  warning, with each problem marked on its line;
- `barmark format --check` fails if a chart isn't in Barmark's standard
  form. `barmark format --write songs` puts it there.

To run them locally (Node 20.6 or later):

```sh
npx -y @barmark/cli@0.1.2 check --strict songs
npx -y @barmark/cli@0.1.2 format --check songs
```
