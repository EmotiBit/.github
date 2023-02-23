# Description
<!--- Describe your changes in detail -->

# Requirements
- PR #(Link PR)


# Issues Referenced
<!-- If Any -->
- Fixes # (issue)

# Documentation update
Link to a change in documentation (if any)

# Testing

**Test Configuration**:
* Firmware version:
* Hardware:
* EmotiBit software version

|Test | Result | Link |
|-----|--------|------|

# Checklist to allow merge
- [ ] All dependent repositories used were on branch `master`
- Software
  - [ ] Passed testing on Windows
  - [ ] Passed testing on macOS
  - [ ] Passed testing on linux (ubuntu)
- Firmware
  - [ ] Set testingMode to TestingMode::NONE
  - [ ] Set const bool `DIGITAL_WRITE_DEBUG` = false (if set true while testing)
  - [ ] Update version in EmotiBit.h
  - [ ] Update library.properties to the correct version (should match EmotiBit.h)
- [ ] Installers (for windows) and project file (for macOS) are updated with any new file to be added with the distributables.
- [ ] Update software bundle version in `ofxEmotiBitVersion.h`
- [ ] doxygen style comments included for new code snippets
- [ ] Required documentation udpated

## Screenshots:
