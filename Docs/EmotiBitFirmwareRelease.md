# Description
Follow the steps below to create releasea release for EmotiBit firmware.

## Creating a PR
- ToDo: Add link to rules for creating a PR.

## Testing
- Each new feature or bug fix should have a unit test in the `EmotiBit_FeatherWing/testing/` folder.

## Release Process
- [ ] After the PR has been reviewed and tested, merge it into master.
- [ ] Verify the library version has been bumped accordingly. See [semver](https://semver.org/) for more information on version bumps. The library version is specified in the `library.properties` file.
- [ ] Verify that the FW version in `EmotiBit.h` matches the version in `library.properties`.
- [ ] Tag the latest commit on the master(after merging the PR). The tag name is the same as the library version, prefixed by `v`.
  - For example, if the release is 2.0.0, the tag will be `v2.0.0`.
  - See [git tag documentation](https://git-scm.com/book/en/v2/Git-Basics-Tagging) for help with creating tags.

### Template draft release
```
# Changelog
- Briefly list of changes added to the library

## Dependency update
- highlight any libraries that have been updated as a part of this firmware update.

# PRs referenced 
- name1 - #number1
- name2 - #number2

# Compatibility
- A complete list of dependencies and corresponding versions. (see helper scripts below to get list of library versions)
```

## Creating distributable binary
- Run the [checkout-and-pull-master.sh](https://github.com/EmotiBit/Helper-Scripts/tree/main/checkout-and-pull-master) script to make sure all dependency libraries are on master
- Run the [get-libdeps-version.sh](https://github.com/EmotiBit/Helper-Scripts/tree/main/get-libdeps-version) to get the library versions.
  - Use this list to populate the Release notes
- Create the required binaries
  - A binary is created for every variant+board.
    - For example:
    - There are 2 binaries for the stock firmware (Feather M0 and ESP32)
    - There are 2 binaries for 100Hz PPG (Feather M0 and ESP32)
  - Binary naming
    - `EmotiBit_stock_firmware_<firmware_variant>.<feather_variant>.bin`
    - Examples:
      - `EmotiBit_stock_firmware.feather_esp32.bin`
      - `EmotiBit_stock_firmware.feather_m0.bin`
      - `EmotiBit_stock_firmware_PPG_100Hz.feather_esp32.bin`
      - `EmotiBit_stock_firmware_PPG_100Hz.feather_m0.bin`
- Add the binaries to the draft release
  - Add the created binaries to the draft release
- Create releases for any dependency
  - If any EmotiBit controlled library needs a release, release that library. Check out the [FW dependencies release](./FirmwareDependencyRelease.md) for more details.
- Publish the release.
