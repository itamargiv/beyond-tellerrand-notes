# More to give than just the `<div>`
Semantics and how to get them right 

> By: [Hidde de Vries](https://beyondtellerrand.com/events/dusseldorf-2021/speakers/hidde-de-vries)
>
> **Video:** https://www.youtube.com/watch?v=YG9WQUfH7ZU
>
> [Slides](https://talks.hiddedevries.nl/Ahs3lw/more-to-give-than-just-the-div-semantics-and-how-to-get-them-right#sSk4Nh5)

## A bit about semantics

- Semantics come up almost in every project as a problem point, when auditing
  websites.
- Semantics are theories of meaning, and we have been philosophizing about them
  for a few millennia already.
- Correspondence theories of meaning: A phrase's meaning is determined by it's
  correspondence to an object in the world
- Wittgenstein in "Philosophical investigations" directly links meaning to it's
  usage in the language. The meaning only starts to exist when the language is
  used. A glass a of water only acquires it's meaning by a community of people
  using the same words do describe it.
- That is, a meaning can only exist if it's shared. 

## Semantics in Web development

- In terms of web development, you can think of design system as a shared
  language between different roles within an organization.
- An API and component library are also a shared language between various code
  bases.
- Classification depends on place and culture and thus it is hard. That's why AI
  is not really good at it.
- On the web you have various types of semantics. XML for example is system to
  generate your own semantics and schema.
- However, for accessibility, semantics have to be shared on a global level.
  That is everyone needs to use the same semantics, which is what HTML 5 is.

## What is HTML?

- HTML is not a way to declare what stuff looks like on a page, it's for stuff
  stuff **is** on a pge.
- HTML semantics are not about behaviour either. 
- HTML enables a cross platform multi device web.
- Default stylesheets are also enables by html's structure.
- Browse by heading is supported by semantic HTML.
- Default form behaviour is included in the box with simple HTML.
- "Reader Mode" also works based on the structural semantics provided by HTML.
- Our responsibility as developers is to point assistive technologies to the
  correct content by applying proper structure

## HTML Semantics in practice

- Semantics in html is in the elements, the attributes and also in attribute
  values.
- WAI-ARIA defines semantics beyond what HTML can afford. For instance, tab
  layouts.
- There are a lot of instances where ARIA is redundant, since HTML is a living
  standard.
- Thus ARIA is like a polyfill that adds semantics to HTML until HTML standards
  catch up.
- Since HTML provides a much more robust support than specifying everything by
  WAI-ARIA, always prefer the correct HTML element over a div with WAI-ARIA
  attributes.
- There are places where this can become confusing, such as the difference
  between a link and a button. However, what we really care about semantics is
  just having the right element in the DOM, regardless of it's appearance.

## Roles

- Semantic HTML element are parsed by assistive technologies into a certain role
  in the page.
- In Design Systems, we should really see if our design choices encourage the
  correct roles being used

Some examples:

- Using the correct heading elements means your document can be properly parsed
  by reader mode and get the correct emphasis with screen readers. When you
  write a heading, consider how it would show up in 
- Buttons can perform actions on a page, even without JS (like sending forms),
  you can press it with just keyboard
- Lists make it clear to screen readers and reader mode that the content being
  parsed is a list with X amount of elements
- autocomplete attributes on inputs allows users to tell their browser to fill
  inputs for them. In addition screen readers can announce the purpose of the
  input.
- Tables and captions allows screen readers to navigate tables with correct
  semantics.

## Learn More

https://developers.whatwg.org - A great manual for developers on HTML and accessibility

https://HTMHell.dev - collects examples of what **not** to do with your html

## Caveats

- Some css attributes can really harm semantics. Especially the `display`
  attribute on tables and lists.
- List can lose their semantics if using the `list-style-type: none` in Safari -
  which is done on purpose, since they decided developers are using too many
  unstyled lists.
- The `summary` element obliterates the semantics of it's child elements. This
  might have to do with a bugs in the HTML specs, since summary elements are
  regarded as buttons, but are also noted to be able to allow child element
  roles.
- A screen reader bug causes `text-transform: uppercase` to be read as an
  abbreviation: letter by letter.
- `::before` and `::after` are actually included in the content of the page.
  USing emojis in this content might cause the emoji to be read out.

## The Future

- Open UI: Hopes to change the stylability issues that causes DS Engineers and
  Designers reinvent the wheel on some html element, like selects. As well as
  add missing elements like tabs, carousels, an popovers.
- Could AI apply semantics in the future? Perhaps with bigger datasets, but even
  then the classification problem exists.

## Summary

- Semantics only works when it is shared
- Semantic HTML has many benefits
- Beware of how CSS affects semantics on the page.
