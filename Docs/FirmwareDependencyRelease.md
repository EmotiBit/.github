# Description
Follow the steps below to create releases for libraries EmotiBit Firmware is using as dependency.

## Creating a PR
- ToDo: Add link to rules for creating a PR.

## Testing
- Each new feature or bug fix should have a unit test in the `library/testing/` folder.

## Release Process
- [ ] After the PR has been reviewed and tested, merge it into master.
- [ ] Verify the library version has been bumped accordingly. See [semver](https://semver.org/) for more information on version bumps. The library version is specified in the `library.properties` file.
- [ ] Tag the latest commit on the master. The tag name is the same as the library version, prefixed by `v`.
  - For example, if the release is 2.0.0, the tag will be `v2.0.0`.
- [ ] Create a release.
  - The release name should match the tag name.
  - Add the following template to the release body and upate it accordingly. 
```
# Changelog
- Briefly list of changes added to the library

# PRs referenced
- name - #number
- name - #number

# Compatibility
- Highlight if this version is incompatible with an earlier version of emotibit firmware.
```

