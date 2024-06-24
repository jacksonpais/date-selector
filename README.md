<br />
<div align="center">
  <a href="https://github.com/jacksonpais/daily-selector">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">daily-selector</h3>
</div>
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

### A simple JavaScript Datepicker

- Lightweight
- No dependencies

![daily-selector Screenshot][screenshot]

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Overview

The **daily-selector** is a lightweight and customizable date picker tool that can be easily integrated into any web application. This utility provides a user-friendly interface for selecting dates, months, and years, with a smooth and responsive design.

## Features

- **Responsive Design**: Ensures the date selector looks great on any device.
- **Month and Year Selection**: Allows users to quickly navigate between months and years.
- **Customizable UI**: Easily change the look and feel to match your application's theme.
- **No External Dependencies**: Pure HTML, CSS, and JavaScript.

## Demo

Check out the live demo [here](https://example.com).

## Installation

To integrate **daily-selector** into your project, follow these steps:

link directly to the file:

```html
    <script src="./daily-selector.js"></script>
```

## Styles

You will also need to include DailySelector CSS file.

link to the file:

```html
    <link rel="stylesheet" href="./daily-selector.css" />
```

## Usage

**daily-selector** can be bound to an input field:

```html
    <input type="text" id="birthdate" class="daily-selector" />
```

Add the JavaScript to the end of your document:

```html
    <script>
        document.addEventListener("DOMContentLoaded", (event) => {
            dailySelector.initialize({
                elementId: "birthdate",
                theme: "popup",
                displayFormat: "DD-MMM-YYYY",
                year: {
                    min: 1970,
                    max: 2024
                },
                color: {
                    primary: "purple",
                    secondary: "violet"
                }
            });
        });
    </script>
```

If you're using **jQuery** :

```javascript
    $( document ).ready(function() {
        dailySelector.initialize({
            elementId: "birthdate",
            theme: "popup",
            displayFormat: "DD-MMM-YYYY",
            year: {
                min: 1970,
                max: 2024
            },
            color: {
                primary: "purple",
                secondary: "violet"
            }
        });
    });
```
### Formatting

By default, dates are formatted and parsed using standard JavaScript Date object.

```html
  Wed Jun 05 2020 00:00:00 GMT+0530 (India Standard Time)
```

But it can be formatted with built-in options.

| Built-in Formats | Output                                      |
|------------------|---------------------------------------------|
| D                | Dates - 1, 2, 3, 4, 5,...9, 10, 11          |
| DD               | Dates - 01, 02, 03, 04, 05, ....09, 10, 11  |
| M                | Months - 1, 2, 3, 4, 5,...9, 10, 11         |
| MM               | Months - 01, 02, 03, 04, 05, ....09, 10, 11 |
| MMM              | Months - Jan, Feb, Mar.....                 |
| MMMM             | Months - January, February, March.....      |
| YY             | Years - 22, 23, 24...                         |
| YYYY             | years - 2022, 2023, 2024.....               |
| B                | Days - 1, 2, 3, 4, 5,...9, 10, 11           |
| BB               | Days - 01, 02, 03, 04, 05, ....09, 10, 11   |
| BBB              | Days - Sun, Mon, Tue.....                   |
| BBBB             | Days - Sunday, Monday, Tuesday.....         |

Allowed separators are:
```html
  - / : . , 
```