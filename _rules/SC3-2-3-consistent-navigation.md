---
name: Consistent navigation
description: |
  Each image that is not marked as decorative, has an accessible name

success_criterion:
- 3.2.3 # Consistent navigation

test_aspects:
- DOM tree
- CSS styling

authors:
- Kathy Eng

---

## Test procedure

### Applicability

The rule applies to any navigational mechanism (to be defined) that is [visible on the page](#visible-on-the-page.html) and repeated on two or more web pages (add web page def link)within a set of Web pages (add link).

### Expectation

Each target element occurs is in the same relative order each time they are repeated.

## Accessibility Support

(add from another rule that has no acc support - see page title)

## Background
- [G61](https://www.w3.org/TR/WCAG20-TECHS/G61.html)
- [F66]

## Test cases
Thank you, Alistair.

### Passed

#### Passed example 1

Image has accessible name

```html
something.html
<img alt="W3C logo" />
```

### Failed

#### Failed example 1

No accessible name

```html
<img />
```

#### Failed example 2

Non-image element with image role but no accessible name.
```html
<div role="img"></div>
```

#### Failed example 3

Image element inside a div positioned off screen with no accessible name.
```html
<div style="margin-left:-9999px;"><img /></div>
```

### Inapplicable

#### Inapplicable example 1

decorative image.

```html
<img alt="" />
```

#### Inapplicable example 2

decorative image.

```html
<img role="presentation" />
```

#### Inapplicable example 3

`img` element with no role.

```html
<img role="none" />
```

#### Inapplicable example 4

Non-image element.

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
</svg>
```
To do:
Test Cases 
Failure1: block of nav, then heading. page2: heading, then nav
Pass1: block of nav then heading on both pages

definition navigational mechanisms: repeated unit of content

- footers
- breadcrumb
- skip to nav link
- search
- logos
From [G61](https://www.w3.org/TR/WCAG20-TECHS/G61.html):
- A Web site has a logo, a title, a search form and a navigation bar at the top of each page; these appear in the same relative order on each page where they are repeated. On one page the search form is missing but the other items are still in the same order.
- A Web site has a left-hand navigation menu with links to the major sections of the site. When the user follows a link to another section of the site, the links to the major sections appear in the same relative order in the next page. Sometime links are dropped and other links are added, but the other links always stay in the same relative order. For example, on a Web site of a company that sells products and offers training, when a user moves from the section on products to the section on training, the links to individual products are removed from the navigation list, while links to training offerings are added.








