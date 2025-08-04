# Description
<!--- Describe your changes in detail -->

# Requirements
<!--- This sections defines on a high level what the reviewer might need to test/conduct a review. This can include other PRs, toolchains, softwares, files etc. -->
<!--- For example, Requirements can be a specific branch of another repository that is a dependency. -->
<!--- Another example can be downloading tools like VS or anaconda -->
- PR #(Link PR)


# Issues Referenced
<!-- If Any -->
- Fixes # (issue)

# Documentation update
Link to a change in documentation (if any)

# Notes for Reviewer
- Add detailed notes explaining code changes, algorithms or any other information that can help the reviewer understand the PR better.


<!--- The following section is relevant only for PRs in ofxEmotiBit repository. delete the section if creating a PR for ay other repo. -->
# List of new distributable files (For software PR only)
- Name all new files added with this PR that need to be distributed with the release package. This includes files like `.json`, `.xml` settings files etc.

# Testing
<!--- The testing results should be added to the main PR behind this bug-fix/ feature-add -->
<!--- If another **linked PR** is the main PR for this bug-fix/ feature-add, you may then remove this testing section and add a link to the main PR here with the explicit statement "testing results added to PR(link)". -->

## Feature Tests (Integration tests)
<!--- For each test case, create a feature test in the `EmotiBit Feature Test Protocol` document. -->
<!--- The corresponding results are recorded in the `EmotiBit Feature Testing Results` sheet. -->
<!--- Update the table below with the test results -->
|Feature Test | Result|
|--------------|-------|
|Feature test 1| ✔️ or ✖️|

## Unit Tests
<!--- Unit tests should be checked into the Repository under the testing/test folder  -->

|Unit Test | Result|
|--------------|-------|
|Feature test 1| ✔️ or ✖️|

# Shared files
- Firmware binary: [Link to firmware binary]
- Other files.

# Checklist to allow merge
- [ ] All dependent repositories used were on branch `master`
- Software
  - [ ] Get approval from the reviewer
  - [ ] Passed testing on Windows
  - [ ] Passed testing on macOS *(for major changes/GUI changes/ PRs adding files distributed with the EmotiBit software)*
  - [ ] Passed testing on linux (ubuntu) *(for major changes/GUI changes/ PRs adding files distributed with the EmotiBit software)*
  - [ ] Update software bundle version in `ofxEmotiBitVersion.h`
- Firmware
  - [ ] Set testingMode to TestingMode::NONE
  - [ ] Set [const bool `DIGITAL_WRITE_DEBUG`](https://github.com/EmotiBit/EmotiBit_FeatherWing/blob/e2ed2dcb70c57c33f70e3a131f82c16627b519df/EmotiBit.h#L58) = false (if set true while testing)
  - [ ] Update version in EmotiBit.h
  - [ ] Update library.properties to the correct version (should match EmotiBit.h)
- [ ] doxygen style comments included for new code snippets
- [ ] Required documentation updated


## Screenshots:
