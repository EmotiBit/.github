# Description
<!--- Describe your changes in detail -->

# Requirements
- PR #(Link PR)


# Issues Referenced
<!-- If Any -->
- Fixes # (issue)

# Documentation update
Link to a change in documentation (if any)

# Notes for Reviewer
- Add detailed notes explaining code changes, algorithms or any other information that can help the reviewer understand the PR better.

# Testing
<!--- The testing results should be added to the main PR behind this bug-fix/ feature-add -->
If another **linked PR** is the main PR for this bug-fix/ feature-add, you may then remove this testing section and add a link to the main PR here with the explicit statement "testing results added to PR(link)". 

## Results
- Synopsis of results, details if required.
- The main results should be recorded in the appropriate testing results sheet.

## Unit Tests
For each test case, create a unit test in the `EmotiBit Feature Test Protocol` document. 
- For firmware, the corresponding results recorded in the `EmotiBit Feature Testing Results` sheet.
- For software, the corresponding results are recorded in the `EmotiBit Software Testing Records` sheet. 

## Steps to test
Import the steps from the `EmotiBit Feature Test Protocol` for quick access for the reviewer

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
  - [ ] Set const bool `DIGITAL_WRITE_DEBUG` = false (if set true while testing)
  - [ ] Update version in EmotiBit.h
  - [ ] Update library.properties to the correct version (should match EmotiBit.h)
- [ ] doxygen style comments included for new code snippets
- [ ] Required documentation updated

## Unit test
Specify the name of unit tests created/added with this feature add/bug fix. Add this new test into the `EmotiBit Feature Test Protocol` document.
 

## Screenshots:
