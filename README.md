# Microteia — releases

Distribution artifacts for the Microteia platform. **No source lives here**: what travels is compiled.

- `kernel/index.json` — the catalog the Microteia Console reads. It lists every published version with
  its size and sha256, and the absolute URLs of the files that carry it.
- Each version is a release tagged `kernel-<version>`, carrying the package and its manifest.

Nobody downloads from here by hand:

    npm i -g @microteia/console
    microteia unpack --version latest

The Console reads the catalog, verifies what it downloads against the sha256 above, and only then puts
it in place.
