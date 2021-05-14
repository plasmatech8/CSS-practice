# Bootstrap 5 tutorial - crash course for beginners in 1.5H (stable release May 2021)

https://www.youtube.com/watch?v=rQryOSyfXmI

https://github.com/mdbootstrap/knowledge-base/tree/main/x-in-one-video/Bootstrap5

See also:
* [How I stopped using Bootstrap's layout thanks to CSS Grid](https://blog.theodo.com/2018/03/stop-using-bootstrap-layout-thanks-to-css-grid/)

## Contents

- [Bootstrap 5 tutorial - crash course for beginners in 1.5H (stable release May 2021)](#bootstrap-5-tutorial---crash-course-for-beginners-in-15h-stable-release-may-2021)
  - [Contents](#contents)
  - [01. Introduction](#01-introduction)
    - [What is Bootstrap?](#what-is-bootstrap)
    - [Why use Bootstrap](#why-use-bootstrap)
    - [Some important components & helpers](#some-important-components--helpers)
    - [Whats new in Bootstrap 5](#whats-new-in-bootstrap-5)
    - [Installation](#installation)
  - [02. Bootstrap Grid](#02-bootstrap-grid)
    - [Container](#container)
    - [Row](#row)
    - [Column](#column)
    - [Note](#note)
  - [03. Buttons](#03-buttons)
  - [04. Cards and Panels](#04-cards-and-panels)
  - [05. Typography](#05-typography)
  - [06. Responsive images](#06-responsive-images)
  - [07. Utilities/spacing](#07-utilitiesspacing)
  - [08. Tables](#08-tables)
  - [09. Alerts and Toasts](#09-alerts-and-toasts)
  - [10. Carosel](#10-carosel)
  - [11. Scrollspy](#11-scrollspy)
  - [12. Navbars, Navs, Tabs](#12-navbars-navs-tabs)
  - [13. Offcanvas](#13-offcanvas)
  - [14. Icons](#14-icons)
  - [15. Forms](#15-forms)
  - [16. Other cools stuff](#16-other-cools-stuff)
  - [Personal notes](#personal-notes)

## 01. Introduction

### What is Bootstrap?

* 72% of CSS framework market
* Mobile first

### Why use Bootstrap

* Development speed
* Consistency
* Community
* Browser compatability

### Some important components & helpers

* Alerts, Badges, Breadcrumbs, Buttons, Cards, Carousel, Collapse, Dropdowns
* List group, Model, Navbars, Panels, Paginations, Popovers, Progress bars, Scrollspy
* Spinners Toasts, Tooltips, Clearfix, Icons, Tables, Gutters

### Whats new in Bootstrap 5

* No JQuery
* Dropped IE support
* RTL support (right to left)
* Less JS in favour of CSS (CSS custom properties)
* ALmost every option available as data attribute (without need for JS)
* Enhanced grid system
* New components
* Enhanced icons

### Installation

Install through either CDN or download and reference.

## 02. Bootstrap Grid

![](img/2021-05-14-14-41-36.png)

The grid works using a 12 point system.

Gutters
* Use `.g*` (instead of `.gutter` now)

### Container

* `.container` block element that has left and right padding
* `.container-fluid` will have 0 padding left and right
* `.container-md` fluid up to medium width

### Row

* `.row`
* Usually we try to ensure that columns in a row sum up to 12.

### Column

* If we use `.col`, it will autocalculate the size

Specify the size of a column in breakpoints using class:
* `.col-xxl-1`
* `.col-sm-12`
* etc...

* `col-md` means that the grid will only activate at or above md, and below md will be full-width

### Note

Use `my-4` for y margin.

## 03. Buttons

Create a button using `.btn` and add extra attributes such as primary/secondary, size, styles, etc.

`btn btn-primary btn-sm`


## 04. Cards and Panels

Cards
* `card`
* `card-body`
* `card-img-top`
* `card-title`
* `card-text` can have multiple
* `card-header`
* `card-footer`
* `card-group` for grouped cards


## 05. Typography

Headings styles can be applied to non-h* elements if desired.

We can use normal html elements and the styles will be automatically applied. e.g.
* `h1`
* `mark` (highlight)
* `del` or `s` (strikethrough)
* `ins` or `u` (underline)
* `strong` or `b` (bold)
* `em` (italicised)
* Lists

Class Components:
* `backquote`
* `backquote-footer` (i.e. - Some famous dude)
* `list-inline`
* `list-inline-item`

The `display-*` class appears to change the font to a larger kind of heading.

## 06. Responsive images

You are going to want to use `.img-fluid` on your image tags because:
* The container will not resize to the same width as the image
* The image itself will not resize to the desired `width: X%`

Use:
* `rounded` to round edges
* `float-end` to align right
* `d-block` and `mx-auto` to display as block (for flex) and align center

We need to use a div with `.clearfix` after each floating element because otherwise, elements
like typeography will flow alongside the floating element. The clearfix can either be the
container or a seperate empty preceding element.

clearfix = clear floated content

## 07. Utilities/spacing

https://getbootstrap.com/docs/5.0/utilities/spacing/

Padding:
* `ps-5` padding start
* `pe-5` padding end
* `pt-5` padding top
* `pb-5` padding bottom
* `py-5` padding Y
* `px-5` padding X

Width:
* `w-25`, `w-50`, `w-75`, `w-100` set width

Other:
* `mx-auto` center an element in the x
* `text-center` center text

Visibility:
* `visible`
* `invisible`

## 08. Tables

Table:
* `table`
* `table-responsive-md`

Styling:
* `table-dark`
* `table-striped`
* `table-bordered`
* `table-hover`
* `table-primary` color on rows
* `table-active` on rows

## 09. Alerts and Toasts

Just simple message boxes.

Alerts:
* `alert`

Styling:
* `alert-primary`, etc...

Dismissing:
* `alert-dismissible` finds a `btn-close` element and brings it to the top-right.
* `fade` allows it to have a fade effect
* `show` an alert with fade is invisible by default

Toasts:
* https://getbootstrap.com/docs/5.0/components/toasts/
* Popup boxes like modals in the corner of your screen.
* `toast`
* `toast-header`
* `toast-body`
* `toast-container` for stacking
*  Does not appear to come with 'dismiss' functionality

## 10. Carosel

Carousel:
* https://getbootstrap.com/docs/5.0/components/carousel/
* Need to add an ID to the carousel and reference the ID as targets.
* `.carousel`
* `.courousel-indicators`
* `.carousel-inner`
* `.carousel-item .active`
* `.carousel-control-prev`
* `.carousel-control-prev-icon`

## 11. Scrollspy

Highlights the item the nav by knowing which heading we are currently located/scrolled to
on the page. e.g.
```html
<div id="list-example" class="list-group">
  <a class="list-group-item list-group-item-action" href="#list-item-1">Item 1</a>
  <a class="list-group-item list-group-item-action" href="#list-item-2">Item 2</a>
  <a class="list-group-item list-group-item-action" href="#list-item-3">Item 3</a>
  <a class="list-group-item list-group-item-action" href="#list-item-4">Item 4</a>
</div>
<div data-bs-spy="scroll" data-bs-target="#list-example" data-bs-offset="0" class="scrollspy-example" tabindex="0">
  <h4 id="list-item-1">Item 1</h4>
  <p>...</p>
  <h4 id="list-item-2">Item 2</h4>
  <p>...</p>
  <h4 id="list-item-3">Item 3</h4>
  <p>...</p>
  <h4 id="list-item-4">Item 4</h4>
  <p>...</p>
</div>
```

## 12. Navbars, Navs, Tabs

Navbars are really good.

Navbar
* Navbar is a container used to hold stuff
* https://getbootstrap.com/docs/5.0/components/navbar/#supported-content

Nav
* Nav is just a set of links used in a navbar
* https://getbootstrap.com/docs/5.0/components/navs-tabs/
* Variants
  * Use `.nav-tabs` or `.nav-pills` to change the styling
* Can use `.dropdown-toggle` in a nav item

## 13. Offcanvas

Used for togglable side-menus.
* https://getbootstrap.com/docs/5.0/components/offcanvas/
* Backdrop = darken the page
* Scrollable = allow scrolling while open

## 14. Icons

Icons
* https://icons.getbootstrap.com/
* `npm i bootstrap-icons`

## 15. Forms

* Form elements are styled by default.
* Forms work well with the bootstrap grid and cards

Validation:
* Classes to add/remove via JS
  * `.is-valid`
  * `.is-invalid`
  * `.was-validated`
* Properties which are partly handled by default via vanilla
  * `required` causes submit to stop if the field is empty or does not match the input type (email/number/etc)
  * The box will glow red (but does not add validation markers) if input is required and does not match the input type
* Use `.form-check` to automatically show/update validation markers based on content
* Use `.invalid-feedback` or `.invalid-tooltip` to show feedback.

## 16. Other cools stuff

* Pagination
* Tooltips
* Popovers
* Modals
* Badges
* List Groups

## Personal notes

* I think vanilla CSS grid is slightly better, but bootstrap grid is definitely convenient for a lot of cases.
* Use bootstrap for its components such as:
  * container
  * buttons
  * cards
  * (typography)
* Use bootstrap for its utilities such as:
  * Margin mx-5, mx-auto
  * Padding px-5
  * Pointer events pe-none
  * User select user-select-none


