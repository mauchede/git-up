### Installation

Copy the script `bin/git-up` into your executable folder (like `/usr/local/bin` or `$HOME/bin`).

```bash
sudo curl -sLo /usr/local/bin/git-up https://github.com/timonier/git-up/raw/master/bin/git-up
sudo chmod +x /usr/local/bin/git-up
```

### Usage

Run the command `git-up` or `git up`:

```bash
git up
# Fetching origin
# stashing 1 changes
# master up to date
# unstashing
```

__Note__: By default, the version `0.5.12` will be used. To change the version, define the `TAG` before the command:

```bash
TAG="latest" git up -v
```

### Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

### Links

* [git-up](https://github.com/aanand/git-up)
* [image "timonier/git-up"](https://hub.docker.com/r/timonier/git-up/)
