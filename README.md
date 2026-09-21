# JsonTags_To_DOM

Zero-dependency declarative **JsonTags_To_DOM compiler and specification
renderer**.

This project transforms a serializable JSON specification into live
native DOM elements in the browser.

## Overview

The project uses JSON to describe an HTML structure.

Each JSON object can define:

-   `tagName` -- HTML tag to create
-   `attributes` -- HTML attributes and Bootstrap classes
-   `children` -- nested DOM elements
-   `textContent` -- text inside an element

The JSON specification is converted into real HTML DOM elements at
runtime.

## Running the Project

Start a static server from the project directory:

``` bash
npx serve
```

Open the URL shown in the terminal.

The browser renders the JSON specification as native DOM elements.

## Project Structure

``` text
JsonTags_To_DOM/
│
├── samples/
│   └── v1/
│       ├── index.html
│       └── spec.json
│
├── src/
│   └── ...
│
├── .gitignore
├── LICENSE
└── README.md
```

## JSON to DOM

The main concept of the project is:

``` text
JSON
 ↓
DOM Specification
 ↓
Native HTML Elements
 ↓
Browser Rendering
```

For example:

``` json
{
  "tagName": "a",
  "attributes": {
    "href": "#",
    "class": "icon-link"
  },
  "textContent": "Call to action"
}
```

is converted into a native anchor element.

## Purpose

The project provides a declarative way to describe UI structures using
JSON instead of writing the complete HTML structure manually.

It can be used for:

-   JSON-based UI definitions
-   DOM generation
-   Reusable UI specifications
-   Specification validation
-   Bootstrap-based UI generation
-   Testing JSON-to-DOM conversion

## Key Idea

> **JsonTags_To_DOM converts a serializable JSON specification into live
> native DOM elements through a declarative JSON-based structure.**