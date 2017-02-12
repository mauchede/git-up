# README

Fetch and rebase all locally-tracked remote branches

## Installation

Copy the script `bin/git-up` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl -sLo /usr/local/bin/git-up "https://github.com/timonier/git-up/raw/master/bin/git-up"
sudo chmod +x /usr/local/bin/git-up
```

Linux users can use the [installer](https://github.com/timonier/git-up/blob/master/bin/installer):

```sh
curl -sL "https://github.com/timonier/git-up/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the command `git-up` or `git up`:

```sh
git up
# Fetching origin
# stashing 1 changes
# master up to date
# unstashing
```

__Note__: By default, the version `0.5.12` will be used. To change the version, define the `TAG` before the command:

```sh
git-up -v
# git-up 0.5.12

TAG="..." git-up -v
# ...
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [git-up](https://github.com/aanand/git-up)
* [image "timonier/git-up"](https://hub.docker.com/r/timonier/git-up/)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
