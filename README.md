# OLÁ SOU O (LUIZ DEV👋)
 



# título:
   "ESTOU EM MEU PROCESSO DE ESTUDO HTML,CSS,FRONT-END".



https://github.com/CodigoMaquina/code.git
git ## Usage

Import `@testing-library/jest-dom` once (for instance in your [tests setup
file][]) and you're good to go:

[tests setup file]:
  https://jestjs.io/docs/en<div align="center">
<h1>jest-dom</h1>

<a href="https://www.emojione.com/emoji/1f989">
  <img
    height="80"
    width="80"
    alt="owl"
    src="https://raw.githubusercontent.com/testing-library/jest-dom/main/other/owl.png"
  />
</a>

- [Installation](#installation)
- [Usage](#usage)
  - [With `@jest/globals`](#with-jestglobals)
  - [With Vitest](#with-vitest)
  - [With TypeScript](#with-typescript)
  - [With another Jest-compatible `expect`](#with-another-jest-compatible-expect)
- [Custom matchers](#custom-matchers)
  - [`toBeDisabled`](#tobedisabled)
  - [`toBeEnabled`](#tobeenabled)
  - [`toBeEmptyDOMElement`](#tobeemptydomelement)
  - [`toBeInTheDocument`](#tobeinthedocument)
  - [`toBeInvalid`](#tobeinvalid)
  - [`toBeRequired`](#toberequired)
  - [`toBeValid`](#tobevalid)
  - [`toBeVisible`](#tobevisible)
  - [`toContainElement`](#tocontainelement)
  - [`toContainHTML`](#tocontainhtml)
  - [`toHaveAccessibleDescription`](#tohaveaccessibledescription)
  - [`toHaveAccessibleErrorMessage`](#tohaveaccessibleerrormessage)
  - [`toHaveAccessibleName`](#tohaveaccessiblename)
  - [`toHaveAttribute`](#tohaveattribute)
  - [`toHaveClass`](#tohaveclass)
  - [`toHaveFocus`](#tohavefocus)
  - [`toHaveFormValues`](#tohaveformvalues)
  - [`toHaveStyle`](#tohavestyle)
  - [`toHaveTextContent`](#tohavetextcontent)
  - [`toHaveValue`](#tohavevalue)
  - [`toHaveDisplayValue`](#tohavedisplayvalue)
  - [`toBeChecked`](#tobechecked)
  - [`toBePartiallyChecked`](#tobepartiallychecked)
  - [`toHaveRole`](#tohaverole)
  - [`toHaveErrorMessage`](#tohaveerrormessage)
- [Deprecated matchers](#deprecated-matchers)
  - [`toBeEmpty`](#tobeempty)
  - [`toBeInTheDOM`](#tobeinthedom)
  - [`toHaveDescription`](#tohavedescription)
- [Inspiration](#inspiration)
- [Other Solutions](#other-solutions)
- [Guiding Principles](#guiding-principles)
- [Contributors](#contributors)
- [LICENSE](#license)
<p>Custom jest matchers to test the state of the DOM</p>

</div>

---

<!-- prettier-ignore-start -->
[![Build Status][build-badge]][build]
[![Code Coverage][coverage-badge]][coverage]
[![version][version-badge]][package] [![downloads][downloads-badge]][npmtrends]
[![MIT License][license-badge]][license]

[![All Contributors](https://img.shields.io/badge/all_contributors-28-orange.svg?style=flat-square)](#contributors-)
[![PRs Welcome][prs-badge]][prs] [![Code of Conduct][coc-badge]][coc]
[![Discord][discord-badge]][discord]

[![Watch on GitHub][github-watch-badge]][github-watch]
[![Star on GitHub][github-star-badge]][github-star]
[![Tweet][twitter-badge]][twitter]
<!-- prettier-ignore-end -->

## The problem

You want to use [jest][] to write tests that assert various things about the
state of a DOM. As part of that goal, you want to avoid all the repetitive
patterns that arise in doing so. Checking for an element's attributes, its text
content, its css classes, you name it.

## This solution

The `@testing-library/jest-dom` library provides a set of custom jest matchers
that you can use to extend jest. These will make your tests more declarative,
clear to read and to maintain.

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Installation](#in
- [Usage](#usage)
  - [With `@jest/globals`](#with-jestglobals)
  - [With Vitest](#with-vitest)
  - [With TypeScript](#with-typescript)
  - [With another Jest-compatible `expect`](#with-another-jest-compatible-expect)
- [Custom matchers](#custom-matchers)
  - [`toBeDisabled`](#tobedisabled)
  - [`toBeEnabled`](#tobeenabled)
  - [`toBeEmptyDOMElement`](#tobeemptydomelement)
  - [`toBeInTheDocument`](#tobeinthedocument)
  - [`toBeInvalid`](#tobeinvalid)
  - [`toBeRequired`](#toberequired)
  - [`toBeValid`](#tobevalid)
  - [`toBeVisible`](#tobevisible)
  - [`toContainElement`](#tocontainelement)
  - [`toContainHTML`](#tocontainhtml)
  - [`toHaveAccessibleDescription`](#tohaveaccessibledescription)
  - [`toHaveAccessibleErrorMessage`](#tohaveaccessibleerrormessage)
  - [`toHaveAccessibleName`](#tohaveaccessiblename)
  - [`toHaveAttribute`](#tohaveattribute)
  - [`toHaveClass`](#tohaveclass)
  - [`toHaveFocus`](#tohavefocus)
  - [`toHaveFormValues`](#tohaveformvalues)
  - [`toHaveStyle`](#tohavestyle)
  - [`toHaveTextContent`](#tohavetextcontent)
  - [`toHaveValue`](#tohavevalue)
  - [`toHaveDisplayValue`](#tohavedisplayvalue)
  - [`toBeChecked`](#tobechecked)
  - [`toBePartiallyChecked`](#tobepartiallychecked)
  - [`toHaveRole`](#tohaverole)


<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Installation

This module is distributed via [npm][npm] which is bundled with [node][node] and
should be installed as one of your project's `devDependencies`:

```
npm install --save-dev @testing-library/jest-dom
```

or

for installation with [yarn](https://yarnpkg.com/) package manager.

```
yarn add --dev @testing-library/jest-dom
```

> Note: We also recommend installing the jest-dom eslint plugin which provides
> auto-fixable lint rules that prevent false positive tests and improve test
> readability by ensuring you are using the right matchers in your tests. More
> details can be found at
> [eslint-plugin-jest-dom](https://github.com/testing-library/eslint-plugin-jest-dom).

## Usage

Import `@testing-library/jest-dom` once (for instance in your [tests setup
file][]) and you're good to go:

[tests setup file]:
  https://jestjs.io/docs/en/configuration.html#setupfilesafterenv-array

```javascript
// In your own jest-setup.js (or any other name)
import '@testing-library/jest-dom'

// In jest.config.js add (if you haven't already)
setupFilesAfterEnv: ['<rootDir>/jest-setup.js']/configuration.html#setupfilesafterenv-array

```javascript
// In your own jest-setup.js (or any other name)
import '@testing-library/jest-dom'

// In jest.config.js add (if you haven't already)
setupFilesAfterEnv: ['<rootDir>/jest-setup.js']
```

### With `@jest/globals`

If you are using [`@jest/globals`][jest-globals announcement] with
[`injectGlobals: false`][inject-globals docs], you will need to use a different
import in your tests setup file:

```javascript
// In your own jest-setup.js (or any other name)
import '@testing-library/jest-dom/jest-globals'
`
