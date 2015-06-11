## opam-release

Simplify the release of opam packages

### Install

```
opam pin add opam-release https://github.com/samoht/opam-release.git
```

### Use

0. Host your package on GitHub and tag your release with the raw version
   number (ie. **not** prefixed by `v`)

1. Have a git remote called `upstream` poiting at the origin project on
   GitHub (not your fork). This will be used to tag the new version when
   you create the release.

2. Install [opam-publish](https://github.com/OCamlPro/opam-publish) in a
   switch called `publish`:

    ```
opam switch publish -A system
opam install opam-publish
     ```

     This will be used to publish the new release to
     [opam-repository](https://github.com/ocaml/opam-repository)

Once this is done, go to the root of your project and to tag and publish a new
release, simply use:

```
$ opam release
```
