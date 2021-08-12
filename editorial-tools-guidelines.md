# Editorial Tools Accessibility Guidelines

## Why do we need specific guidelines for Editorial Tools?
Our Editorial Tools have markedly different UI requirements than our reader-facing website and app.

In order to provide maximum utility to our journalists, Tools must fit a lot of functionality into a small amount of screen space – a UI challenge shared with traditional desktop applications.

Our Source components, which aim to provide great accessibility by default, have been designed with reader-facing applications in mind – and the Editorial Tools will aim to use them as a baseline, while modifying styles to fit into a smaller amount of screen space.

This is a working document, and one which we expect to change over time.

## Goal 

The goal of these guidelines is to support the development of tools which are usable by a broad range of users with differing needs, and to make it simple for developers to identify what they should do in order to make accessible tool interfaces.

## Top-level guidelines
1. **Start with source components.** Where possible, we should try to use existing Source components, because they have already been designed with accessibility in mind. 
However, a user interface for an Editorial Tool requires different solutions to our core news website - specifically; space is at a premium because we need to fit a lot of functionality into a small area, in the same way that a desktop application would. 
Therefore, we should modify existing components<sup>[1](#appendix-modifying-source-components)</sup> to work in our context (i.e. less padding, smaller more concise interfaces), while meeting our own subset of accessibility guidelines<sup>[2](#our-accessibility-checklist).
2. If creating a custom component or modifying a Source component - **it must meet our minimum accessibility requirements** - an abridged checklist of the most relevant Web Content Accessibility Guidelines (WCAG).

## Minimum accessibility requirements
We have chosen not to simply ask developers to follow WCAG – the guidelines are long, quite abstract, and not all relevant to the domain of Editorial Tools. Additionally, asking developers to know them in full creates a time burden that decreases the chance of compliance. Instead we ask for Editorial Tools developers to follow a managed subset of WCAG guidelines, which will be included as a checklist in PR templates.

This subset is based on the WCAG guidelines most relevant to Editorial Tools user interfaces, but has been slightly reworded to make their application a bit clearer.

### Our accessibility checklist:

- Ensure the component is fully functional via keyboard input. [[WCAG Success Criteria (SC) 2.1.1](https://www.w3.org/WAI/WCAG21/Understanding/keyboard.html), 2.1.2].
- Ensure the component is fully functional via screen reader - especially by making sure non-text content has a text equivalent. [[WCAG SC 1.1.1](https://www.w3.org/WAI/WCAG21/Understanding/non-text-content.html)]
- Don’t use colour as the only visual means of conveying information [[WCAG SC 1.4.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-without-color.html)]
- Ensure text and icons in active components have a contrast ratio of at least 4.5:1 compared to their background ([check here](https://webaim.org/resources/contrastchecker/)). [[WCAG SC 1.4.3](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html)]
- Ensure the focus ring remains functional (with browser default styling), or is replaced with [the Source focus halo](https://theguardian.design/2a1e5182b/p/300696-). [[WCAG SC 1.4.13](https://www.w3.org/WAI/WCAG21/Understanding/content-on-hover-or-focus.html)]
- Ensure that no content flashes more than three times in any one second period in order to reduce the risk of inducing a seizure. [[WCAG SC 2.3.1](https://www.w3.org/WAI/WCAG21/Understanding/three-flashes-or-below-threshold.html)]
- Use relevant semantic HTML elements where possible rather than exclusively, for example, generic `div` and `span` elements. [[WCAG 1.3.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html)]

### Appendix: Modifying Source components:

There are a number of ways to [override styles](https://github.com/guardian/source/blob/main/docs/07-overriding-styles.md) from Source. A good option is to use the cssOverrides prop which is available on every component. Create a wrapper around the component that you want to customise, and use the wrapper to apply the styles. If you keep the API of the wrapper the same as the Source component, you can spread all the props.