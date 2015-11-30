# docker-env

OS X wrapper script for `docker-machine env`, creating colored Terminal sessions for different docker machines.

## Installation

* Install the [docker-env](docker-env) script to any `bin/` directory in your `$PATH`, for example:

```
curl -sSL https://raw.githubusercontent.com/robbertkl/docker-env/master/docker-env > /usr/local/bin/docker-env
chmod +x /usr/local/bin/docker-env
```

* In order to have custom Terminal colors for your docker machines, create profiles for them in Terminal preferences. Duplicate your favorite/default profile and modify their background color. Change the profile names to their corresponding docker-machine name.

* Optionally, you can create convenient shortcut symlinks for each of your machines:

```
cd $(dirname $(which docker-env))
docker-machine ls -q | xargs -n 1 ln -s docker-env
```

## Usage

To use it, you can either call it with an argument:

```
docker-env dev
```

or, if you created the shortcut symlinks, just use the machine name:

```
dev
```

## Authors

* Robbert Klarenbeek, <robbertkl@renbeek.nl>

## License

This repo is published under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
