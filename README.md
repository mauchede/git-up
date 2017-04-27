# README

Fetch and rebase all locally-tracked remote branches

## Installation

Copy `bin/git-up` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/git-up "https://github.com/timonier/git-up/raw/master/bin/git-up"
sudo chmod +x /usr/local/bin/git-up
```

Linux users can use the [installer](https://github.com/timonier/git-up/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/git-up/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the command `git-up` or `git up`:

```sh
# See all git-up options

git-up --help

# Run git-up

git-up
# Fetching origin
# develop                                        up to date
# master                                         up to date
# release/1.1.0                                  up to date
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [image "timonier/git-up"](https://hub.docker.com/r/timonier/git-up/)
* [msiemens/PyGitUp](https://github.com/msiemens/PyGitUp)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
