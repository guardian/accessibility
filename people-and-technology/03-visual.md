# Visual

In the UK around [2 million people live with sight loss][sight-loss]. There are 350,000 people on the registers of blind and partially sighted people in the UK.

[sight-loss]: https://www.rnib.org.uk/professionals/knowledge-and-research-hub/key-information-and-statistics

## Screen reader

Screen readers provide an audio representation of a website. They enable people with a vision impairment to navigate and perceive the meaningful content of the website.

Screen reader software reads out everything on screen including text, headings, lists, buttons, text alternatives for images, and form inputs.

When web content is coded correctly a screen reader announces the name, role and state of an element. For example, if navigating a form it can read "Select Terms and Conditions, checkbox, not checked". This breaks down as follows:

- **Name** is "Select Terms and Conditions"
- **Role** is "checkbox"
- **State** is "not checked"

### Guidance

Although we don't maintain a list of screen readers we support, the best screen readers to test with are:

- On MacOS, VoiceOver + Safari
- On Windows, NVDA + Firefox

### Further resources

WebAIM provides a useful guide to [testing accessibility with VoiceOver](https://webaim.org/articles/voiceover/).

## Keyboard

Screen reader users rely fully on the keyboard to navigate. Many of the challenges they experience are the same as a sighted keyboard users we explore in the [Keyboard section on physical disability](./02-physical.md#Keyboard).

## Colour

The legibility of text content is affected by the contrast between the text and the background.

Colour contrast has the greatest impact on legibility for people with moderately low vision or colour deficiencies, such as colour blindness.

### Guidance

#### Contrast

We aim to meet the [WCAG 2.1 AA standard for colour contrast](https://www.w3.org/TR/WCAG21/#contrast-minimum).

The standard requires a contrast ratio of at least 4.5:1 for normal text and 3:1 for large text. Large text is consider 24px or larger (18.5px or larger for bold text).

#### Use of colour

Avoid using colour only to indicate a change in state. This pattern excludes users who are unable to distinguish certain colours, such as colourblind users or users operating devices in direct sunlight.

For example, if a field is in an error state, it is not enough to change the colour of the label to red. It is necessary to make at least one non-colour change such as increasing the font weight of the label or adding an error icon.

### Further resources

[Who Can Use](https://whocanuse.com/) is a tool that can test a combination of background and foreground colours. It gives an indication of the people who may be excluded from reading your content, based on the vision type they have.
