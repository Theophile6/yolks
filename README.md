# Yolks

A curated collection of core images that can be used with Pterodactyl's Egg system. Each image is rebuilt
periodically to ensure dependencies are always up-to-date.

Images are hosted on `ghcr.io` and exist under the `games`, `installers`, and `yolks` spaces. The following logic
is used when determining which space an image will live under:

* `games` — anything within the `games` folder in the repository. These are images built for running a specific game
or type of game.
* `installers` — anything living within the `installers` directory. These images are used by install scripts for different
Eggs within Pterodactyl, not for actually running a game server. These images are only designed to reduce installation time
and network usage by pre-installing common installation dependencies such as `curl` and `wget`.
* `yolks` — these are more generic images that allow different types of games or scripts to run. They're generally just
a specific version of software and allow different Eggs within Pterodactyl to switch out the underlying implementation. An
example of this would be something like Java or Python which are used for running bots, Minecraft servers, etc.

All of these images are available for `linux/amd64` and `linux/arm64` versions, unless otherwise specified, to use
these images on an arm system, no modification to them or the tag is needed, they should just work.

### Contributing

When adding a new version to an existing image, such as `java v42`, you'd add it within a child folder of `java`, so
`java/42/Dockerfile` for example. Please also update the correct `.github/workflows` file to ensure that this new version
is tagged correctly.

## Available Images

* [`alpine`](/oses/alpine)
  * `ghcr.io/pterodactyl/yolks:alpine`
* [`arma3`](/games/arma3)
  * `ghcr.io/pterodactyl/games:arma3`
* [`debian`](/oses/debian)
  * `ghcr.io/pterodactyl/yolks:debian`
* [`fivem`](/games/fivem)
  * `ghcr.io/pterodactyl/games:fivem`
* [`golang`](/go)
  * [`go1.14`](/go/1.14)
    * `ghcr.io/pterodactyl/yolks:go_1.14`
  * [`go1.15`](/go/1.15)
    * `ghcr.io/pterodactyl/yolks:go_1.15`
  * [`go1.16`](/go/1.16)
    * `ghcr.io/pterodactyl/yolks:go_1.16`
* [`java`](/java)
  * [`java7`](/java/7)
    * `ghcr.io/pterodactyl/yolks:java_7`
  * [`java8`](/java/8)
    * `ghcr.io/pterodactyl/yolks:java_8`
  * [`java9`](/java/9)
    * `ghcr.io/pterodactyl/yolks:java_9`
  * [`java11`](/java/11)
    * `ghcr.io/pterodactyl/yolks:java_11`
  * [`java14`](/java/14)
    * `ghcr.io/pterodactyl/yolks:java_14`
  * [`java16`](/java/16)
    * `ghcr.io/pterodactyl/yolks:java_16`
* [`nodejs`](/nodejs)
  * [`node12`](/nodejs/12)
    * `ghcr.io/pterodactyl/yolks:nodejs_12`
  * [`node14`](/nodejs/14)
    * `ghcr.io/pterodactyl/yolks:nodejs_14`
  * [`node15`](/nodejs/15)
    * `ghcr.io/pterodactyl/yolks:nodejs_15`
  * [`node16`](/nodejs/16)
    * `ghcr.io/pterodactyl/yolks:nodejs_16`
* [`python`](/python)
  * [`python3.7`](/python/3.7)
    * `ghcr.io/pterodactyl/yolks:python_3.7`
  * [`python3.8`](/python/3.8)
    * `ghcr.io/pterodactyl/yolks:python_3.8`
  * [`python3.9`](/python/3.9)
    * `ghcr.io/pterodactyl/yolks:python_3.9`

### Installation Images

* [`alpine-install`](/installers/alpine)
  * `ghcr.io/pterodactyl/installers:alpine`

* [`source-install`](/installers/source)
  * `ghcr.io/pterodactyl/installers:source`
