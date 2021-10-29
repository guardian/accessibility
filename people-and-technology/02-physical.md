# Physical

In the UK around [7 million people have a physical impairment][impairment-types] that limits their
movement. A further 3.5 million people have a disability that impacts their
dexterity. Examples of conditions that limit movement include Cerebral Palsy,
Parkinson's and Repetitive Strain Injury.

[impairment-types]: https://www.gov.uk/government/statistics/family-resources-survey-financial-year-2019-to-2020/family-resources-survey-financial-year-2019-to-2020#impairment-types-reported-by-disabled-people-2017-to-2018-2018-to-2019-and-2019-to-2020-united-kingdom

## Keyboard

Many people find it easier to navigate websites using the keyboard rather than
the mouse.

Commonly used controls include:

- arrow keys to scroll, or change the selected value of a radio button group
- `Tab` to move from one focussable item to the next
- `Enter` to activate a link or button
- `Space` to select or deselect a checkbox
- `Esc` to cancel a prompt

_Note:_ if you are using Firefox on Mac you need to make some changes to [make tab behaviour work as expected](https://stackoverflow.com/questions/11704828/how-to-allow-keyboard-focus-of-links-in-firefox.).

### General guidance

- Ensure interactive controls are focussable using the `Tab` key.
- Keep the tab order logical. Ensure focus doesn't skip unpredictably around the
  page while tapping the `Tab` key.
- It should be immediately obvious which element is currently in focus. Ensure
  the focus state of each interactive element is clear.
- If there are a lot of navigation controls at the top of the page, provide a
  [skip link][skip-link] that takes the user to the main content.

[skip-link]: https://design-system.service.gov.uk/components/skip-link/

### Links, forms and buttons

- All links, form fields and buttons should be accessible using the `Tab` key
- Buttons should be activated using both the `Enter` and `Space` keys
- Links should be activated using the `Enter` key
- Consider a default action for pressing the `Enter` key while a form field is in focus

### Dropdown menus

- Dropdown menus should be expanded using the `Enter` key
- When a dropdown menu is expanded, links within the menu should be accessible using the `Tab` key
- When a dropdown menu is collapsed, links within the menu should not be accessible using the `Tab` key
- Dropdown menus should be collapsed using the `Esc` key

### Modal dialogs

- Modal dialogs should be closed using the `Esc` key
- When a modal dialog is open, the focus should be trapped (i.e. pressing the Tab key should never move focus outside of the dialog) until the dialog is closed

### Tab lists

- Tabs (i.e. elements with `role=tab`) should be accessible using the `Tab` key
- Tabs should be activated using the `Enter` key
- When a tab panel becomes active, focus should be moved into that tab panel
- Focusable elements in the active tab panel should be accessible using the `Tab` key
- Focusable elements in hidden tab panels should not be accessible using the `Tab` key

### Carousels

- Consider implementing intuitive shortcuts, such as using the `Left` and `Right` cursor keys to move backwards and forwards through the carousel

### Further resources

- [How to implement websites that are ready for keyboard only usage](https://www.accessibility-developer-guide.com/knowledge/keyboard-only/how-to-implement/)

## Switch controls

People with limited or no upper body movement may use switch controls, as well
as people with cognitive and learning difficulties.

There are several types of switches that accommodate different needs:

- Sip-and-puff switches are "clicked" by sipping and puffing into a straw
- Button switches can be activated using the hand, foot or head.
- Camera switches can be activated when tilting the head into a camera
- Eye tracking controls can measure where a user is looking, or track the motion
  of an eye relative to the head.

_Note: It is possible to turn your keyboard into a button switch by [adjusting
your computer's accessibility settings](https://support.apple.com/en-gb/guide/accessibility-mac/mh43182/mac)._

### Guidance

Much of the guidance that is true for keyboard controls is also true for switch
controls. There are also some unique considerations for switch users:

- Typing using switches is much slower than using a keyboard, with users
  typically entering between 1 and 2 words per minute. Consider implementing
  features that reduce the need for typing, such as autocompletion or word
  prediction.
- Avoid imposing time limits on form completion or confirmation controls.
- Scrolling can be slow as operating systems tend to bury the scroll controls.
  Product developers should try to make important navigation and information
  appear above the fold, to reduce the impact of scroll fatigue.
- Switch users may spend a long time completing text fields on forms. If a
  browser crashes, or the user accidentally closes a tab or hits the Back
  button, it can be very frustrating to lose all that typing. A feature that
  automatically saves work in progress can save a lot of time.
- People are likely to make typos when using switches. Make it easy for users
  to go back and correct mistakes on forms.

### Further resources

- [I used a switch control for a day](https://www.24a11y.com/2018/i-used-a-switch-control-for-a-day/)
- [Single switch usability](https://www.youtube.com/watch?v=UKVgfiIqZUM&t=63s)

## Speech input

Speech recognition software enables spoken language to be translated into text
and commands.

### Guidance

Again, much of the guidance that is true for keyboard controls is also true for
speech input. There are also some more nuanced design decisions to consider:

- Ensure shortcut keys can be disabled or customised. If a speech input user
  attempts to dictate some text into a field for instance, they might
  inadvertently activate several shortcut keys.
- Speech input users activate links by reading the link text. Try to ensure
  link text is unique, rather than a series of _Read more_ links.
