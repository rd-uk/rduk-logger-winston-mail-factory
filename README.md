# RDUK - Loggly transport factory for Winston

this module is a [Loggly transport](https://www.npmjs.com/package/winston-loggly-bulk) factory for the [Winston](https://www.npmjs.com/package/winston) implementation of [RDUK logger](https://www.npmjs.com/package/@rduk/logger)

## Installation

```sh
npm i --save --save-exact @rduk/logger @rduk/logger-winston-provider @rduk/logger-winston-mail-factory
```

## Configuration

```yaml
# config.yml (see @rduk/configuration for detail)
---
logger:
  default: winston
  providers:
    -
      name: winston
      type: '@rduk/logger-winston-provider'
      level: debug
      factories:
        mail: '@rduk/logger-winston-mail-factory'
      transports:
        mail: # options passed to factory
          ...
```

That's it!

## License and copyright

See [LICENSE](LICENSE) file
