# Hardened Buildroot. Run Buildroot with SELinux in enforcing mode!

## Getting started

### Prerequisites:
  - A computer running Linux
  - Docker
  - docker-compose

## Quick setup
  - Clone this repository:
    - `git clone https://github.com/amarula/hardened-buildroot.git`
  - Build the docker container:
    - `make build` 
 - Start the docker container. The build will start automatically. IE:
   - `ENV_FILES=x86_64.json make up`
 - Images are found in `hardened-buildroot-external/output/${config_name}/images`

## Currently tested boards:
  - x86_64

## Other notes:
  - See docker/env.json.readme for env file options.
  - See `make help` for make file options.
  - `make shell` will skip building and put you into the docker shell. Navigate to `hardened-buildroot-external/output/${config_name}` to build manually.
  - Board files are found in `hardened-buildroot-external/board`
  - Config files are found in `hardened-buildroot-external/configs`
  - Buildroot patches are found in `hardened-buildroot-external/patches/builldroot`
  - After building x86_64_defconfig run `make x64-run` to start the virtual image. Note: The virbr0 must be present!
  - All defconfigs build.
