# Overview

This project is also being used to learn how to build a CI/CD process and hopefully start using this module for the automation of processing making commits, processing pull requests, and deploying to PSGallery.

## Objectives

- Module
  - Validate a commit message meets the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) standard
  - Validate all commits since the last tag
  - Validate all commits between tags
  - Validate all commits between commits
  - Calculate semantic version based on all commits and a starting version
  - Update version file
  - Generate CHANGELOG overview of incoming commits (unreleased)
    - Format: 
      - [unreleased] - \<date: yyyy-MM-dd>
        - \<Section>
          - \<type>[optional scope]: \<description> (issue #/workitem #)
        - \<Section>
          - \<type>[optional scope]: \<description> (issue #/workitem #)
  - Generate full CHANGELOG to support CI/CD auto-generation
  - Generate Release Notes from unreleased section to support CI/CD auto-generation
  - Support Git Hooks for easy integration
    - Pre-commit
    - Pre-push
  - Support for updateable help
- CI/CD
  - Leverage Invoke-Build:
    - Build Artifact for publication
      - Build Module
      - Build Help files
      - Build Documentation
  - Support for:
    - Azure DevOps
    - Github Actions
  - Automatically generate CHANGELOG, Release Notes, new version tag and update version file
  - Create Release Artifacts ZIP files
  - Support publication to PSGallery

## References

- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- [Semantic Versioning](https://semver.org/)
- [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
- Build Process
  - [RCM folder structure](https://ramblingcookiemonster.github.io/Building-A-PowerShell-Module/)
  - [PowerShell Pipeline](https://xainey.github.io/2017/powershell-module-pipeline/)
  - [Invoke-Build youtube example](https://www.youtube.com/watch?v=PTGw4UXPPfo)
  - [another folder structure]()
- Help Documentation
  - [about file structure Sapien old](https://info.sapien.com/index.php/scripting/scripting-help/how-to-write-about-help-for-your-module)
