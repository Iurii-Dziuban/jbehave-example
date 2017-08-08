# jbehave-example
Example of jbehave configuration for IDEA and maven

[![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badge/)    
[![Build Status](https://travis-ci.org/Iurii-Dziuban/jbehave-example.svg?branch=master)](https://travis-ci.org/Iurii-Dziuban/jbehave-example)
[![Coverage Status](https://coveralls.io/repos/github/Iurii-Dziuban/jbehave-example/badge.svg?branch=master)](https://coveralls.io/github/Iurii-Dziuban/jbehave-example?branch=master)
[![Dependency Status](https://www.versioneye.com/user/projects/58e33de2d6c98d0043fec7fc/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/58e33de2d6c98d0043fec7fc)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/Iurii-Dziuban/jbehave-example/issues)

## Table of contents:
 * [Static Analysis QA Checks](#checks)
 * [Project parts](#project-parts)

# Checks

Jacoco code coverage, pmd, checkstyle, enforcer, findbugs

# Project parts
Under `src/test/java` :
- Steps description is done in `ExampleSteps.java` with description annotations to each step that can be used in the `.story` files
- One story java file per one story file to be run by junit (`ExampleStory` extending `JUnitStory`). 
Steps are initialised. Mapping to story file is done by name (`ExampleStory.java` -> `example_story.story`). 
Configuration can be put into another class and reused.
- All stories file so all stories be run by junit (`AllStoriesByRegexPathTest` extending `JUnitStories`) 
Folders, paths or regex are provided to find `.story` files. 
Configuration can be put into another class and reused.
- Story file itself. `example_stories.story`
