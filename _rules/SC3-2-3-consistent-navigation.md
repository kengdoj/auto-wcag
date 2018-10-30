---
name: Consistent navigation
description: |
  Each navigational mechanism that is repeated on multiple pages is in the [same relative order](https://www.w3.org/TR/WCAG20/#samerelorderdef) on each page

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

The rule applies to any [navigational mechanism](auto-wcag/pages/glossary/navigational-mechanism.md) that is [visible on the page](auto-wcag/pages/glossary/visible-on-the-page.md) and repeated on two or more [web pages](https://www.w3.org/TR/WCAG20/#webpagedef) within a [set of Web pages](https://www.w3.org/TR/WCAG20/#set-of-web-pagesdef).

### Expectation

Each target element occurs in the same relative order each time it is repeated on a page.

## Accessibility Support

There are no major accessibility support issues known for this rule.

## Background
- [G61: Presenting repeated components in the same relative order each time they appear](https://www.w3.org/TR/WCAG20-TECHS/G61.html)
- [F66: Failure of Success Criterion 3.2.3 due to presenting navigation links in a different relative order on different pages](https://www.w3.org/TR/WCAG20-TECHS/F66.html)

## Test cases
Thank you, Alistair.

### Passed

#### Passed example 1

Navigational mechanisms (Search form and navigation links) repeated on two pages in same relative order.

Page A:
```html
<input type="text" aria-label="search">
<a href="link1.html">Page 1</a>
<a href="link2.html">Page 2</a>
<a href="link3.html">Page 3</a>
```

Page B:
```html
<input type="text" aria-label="search">
<a href="link1.html">Page 1</a>
<a href="link2.html">Page 2</a>
<a href="link3.html">Page 3</a>
```

#### Passed example 2

Top level navigation links with expanded menu in same relative order.

Page A:
```html
<ul>
  <li><a href="link1.html">Page 1</a></li>
    <ul>
      <li><a href="link1a.html">Page 1a</a></li>
      <li><a href="link1b.html">Page 1b</a></li>
    </ul>
  <li><a href="link2.html">Page 2</a></li>
  <li><a href="link3.html">Page 3</a></li>
</ul>
```

Page B:
```html
<ul>
  <li><a href="link1.html">Page 1</a></li>    
  <li><a href="link2.html">Page 2</a></li>
    <ul>
      <li><a href="link2a.html">Page 2a</a></li>
      <li><a href="link2b.html">Page 2b</a></li>
    </ul>
  <li><a href="link3.html">Page 3</a></li>
</ul>
```


### Failed

#### Failed example 1

Navigational mechanisms (Search and navigation links) on two pages not in same relative order.

Page A:
```html
<input type="text" aria-label="search">
<a href="link1.html">Page 1</a>
<a href="link2.html">Page 2</a>
<a href="link3.html">Page 3</a>
```

Page B:
```html
<a href="link1.html">Page 1</a>
<a href="link2.html">Page 2</a>
<a href="link3.html">Page 3</a>
<input type="text" aria-label="search">
```

#### Failed example 2
Links within a repeated navigation mechanism not in same relative order.

Page A:
```html
<a href="link1.html">Page 1</a>
<a href="link3.html">Page 3</a>
<a href="link2.html">Page 2</a>
```

Page B:
```html
<a href="link1.html">Page 1</a>
<a href="link2.html">Page 2</a>
<a href="link3.html">Page 3</a> 
```

#### Failed example 3
Search field is in different locations on the page.

Page A:
```html
<!--footer-->
<input type="text" aria-label="search">
```

Page B:
```html
<!--top of page-->
<input type="text" aria-label="search">
```

### Inapplicable

#### Inapplicable example 1

Pages have no repeated components

Page A:
```html
<!--footer-->
<input type="text" aria-label="search">
```

Page B:
```html
<!--footer-->
<!--no search form-->
```

#### Inapplicable example 2


#### Inapplicable example 3


#### Inapplicable example 4









