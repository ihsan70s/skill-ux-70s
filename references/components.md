# shadcn/ui component map

Use this map to find a component family that fits the user's task. Start with the components supplied by the user or documented as available in the project. If there is no inventory, confirm candidates and their behavior in the [official component documentation](https://ui.shadcn.com/docs/components) and mark the selections as proposed. Treat an option outside a known inventory as a gap to flag in the UX specification.

## Navigation and wayfinding

| User need | Components to consider |
| --- | --- |
| Move between major areas | Navigation Menu, Menubar, Sidebar |
| Show the current location | Breadcrumb, Tabs |
| Move through a long result set | Pagination, Scroll Area |
| Open a contextual set of actions | Dropdown Menu, Context Menu |

## Forms and input

| User need | Components to consider |
| --- | --- |
| Enter short or long text | Input, Textarea, Input Group |
| Select one or more values | Native Select, Select, Combobox, Checkbox, Radio Group, Toggle Group |
| Set a yes/no preference | Switch |
| Set a numeric range | Slider |
| Enter a date | Calendar, Date Picker |
| Enter a one-time code | Input OTP |
| Group, label, and describe fields | Field, Label |
| Submit a set of related values | Form patterns documented under Forms; pair fields with Button and clear validation feedback |

## Actions and choices

| User need | Components to consider |
| --- | --- |
| Trigger a primary or secondary action | Button, Button Group |
| Toggle one option | Toggle |
| Choose from command/search results | Command |
| Confirm a consequential action | Alert Dialog |

## Information and status

| User need | Components to consider |
| --- | --- |
| Present a concise message or status | Alert, Message, Badge |
| Show a temporary confirmation or update | Toast |
| Show how far an operation has progressed | Progress |
| Show activity or preview the shape of loading content | Spinner, Skeleton |
| Explain a control on demand | Tooltip, Hover Card |
| Show a person or identity | Avatar |
| Provide an empty-state prompt | Empty |
| Display or format content | Card, Item, Typography, Separator, Aspect Ratio |
| Show a keyboard shortcut | Kbd |

## Overlays and progressive disclosure

| User need | Components to consider |
| --- | --- |
| Show a focused decision or short task | Dialog |
| Show a mobile-friendly overlay panel | Drawer, Sheet |
| Reveal supporting content near a trigger | Popover, Hover Card |
| Expand optional details in place | Accordion, Collapsible |

## Data and content

| User need | Components to consider |
| --- | --- |
| Compare structured records | Table, Data Table |
| Browse a sequence of visual items | Carousel |
| Show a chart | Chart |
| Show a media preview in a fixed shape | Aspect Ratio |
| Attach or represent files | Attachment |

## Specialized and supporting components

These components support specific product needs. Check their individual documentation before choosing them because their interaction patterns are more specialized.

| Component | UX role to assess |
| --- | --- |
| Bubble | Present a compact message or conversational item |
| Code Block | Present code that users need to inspect or copy |
| Direction | Set or communicate text and layout direction |
| Marker | Mark or call attention to a point in content |
| Message Scroller | Present a scrollable sequence of messages |
| Questionnaire | Guide a user through a question-based flow |
| Resizable | Let users adjust the space assigned to adjacent panels |
| Trace | Present a trace or structured sequence for inspection |

## Review questions

For each selected component, decide:

1. What user task does it support, and why does its interaction model fit?
2. What information or action must be visible before the user commits?
3. What are its relevant states, including disabled, pending, selected, empty, error, and success?
4. What happens on keyboard, touch, narrow screens, and assistive technology?
5. How does a user dismiss, undo, or recover from this interaction?

The official component index evolves over time. Check it before adding or removing component families from this map.
