---
name: skill-ux-70s
description: Create and review UX designs for website pages and flows composed from shadcn/ui components. Define user journeys, page layout, component choices, visual treatment, interaction states, and responsive behavior for code implementation, Figma design, or both.
---

# Skill UX 70s

Use shadcn/ui components as building blocks for clear, accessible website experiences. Make UX decisions from the user's task and the product rules first, then choose the component whose behavior fits. Treat the component library as a flexible starting point, not a fixed visual system.

This skill delivers the UX design handoff for building a page in code, designing it in Figma, or both. Deliver a UX specification by default. Add an annotated wireframe when requested or when layout relationships are hard to convey in text. Use the destination named in the request. When none is named, write a specification that works for both. Use the appropriate implementation or Figma skill for production work in either destination.

## Workflow

1. Identify the page goal, user role, primary action, and important constraints. Resolve missing decisions using the chat guidance below.
2. Read `DESIGN.md` if it exists. Review the project's components, design tokens, and related screens to identify conventions that apply to the task.
3. Map the task into page regions and user steps. Before laying out the page, identify the relevant screen states and the next action in each. For example, an empty collection might offer **Add item**, a filtered list with no matches might offer **Clear filters**, and a recoverable load error might offer **Retry**.
4. Compose each page from the shadcn/ui components supplied by the user or documented as available in the project. If no inventory is available, use the shadcn/ui catalog and [component map](references/components.md) and mark those choices as proposed. For each region, specify its place in the layout, the components and variants it uses, their content, and the action they support. Flag any gaps in a known inventory as proposals for handoff.
5. Define the content, hierarchy, and behavior for each component: default, hover/focus, selected, disabled, loading, success, and error states where relevant.
6. Specify what happens after each action, including validation, confirmation, and cancellation.
7. Define layout changes for narrower spaces using the guidance below. Check keyboard use and assistive technology in each relevant layout.
8. Define the visual hierarchy. Name the project's tokens and their roles for surfaces, text, primary actions, focus, and feedback. Describe typography, spacing, and grouping where they guide reading or action. Where tokens are missing, propose values or treatments and mark them as proposals. Record any visual decisions that still need user input.
9. Review the result against the user's task: can they identify what to do, understand the consequence, complete the task, and recover from mistakes? When a preview is available, inspect desktop and mobile layouts, check keyboard navigation where the preview supports it, and review relevant empty and error states. Fix issues within scope and recheck the affected views.

## Design decisions in chat

- Ask the requester directly in chat when a missing answer would materially change the goal, primary flow, or a product rule. For reversible layout or visual details with a reasonable default, proceed and state the assumption in the specification.
- Use selectable options when the chat supports them. Give two or three distinct choices, put the recommended option first, label it **Recommended**, and briefly explain why it fits and what each choice changes. If selectable controls are unavailable, use short numbered choices in chat so the requester can reply with a number.
- Allow a custom answer when the requester has a preference outside the choices. Use a free-text question when only the requester can provide the value, such as approved wording or a brand color.
- Wait for the answer before finalizing the affected design decision. Continue with independent parts of the design while waiting.

## Screen states and transitions

- Confirm before creating or saving a record, applying edits to an existing record, deleting records, or performing another data-changing action that requires approval, such as publishing, archiving, or a bulk update. Place the confirmation at the point where the action would change data. Opening an edit form or typing in it is preparation for that action. For forms, validate the input before showing the `Alert Dialog`. If the user dismisses it, preserve the existing data and any relevant draft or selection. If they confirm, start the action and show the pending state and outcome. Follow explicit product rules. If it is unclear whether another action requires confirmation and the answer changes the flow, ask in chat using the guidance above.
- For each state that changes what users see or can do, specify the trigger, the shadcn/ui components and message shown, the available actions, and the resulting state. Include automatic transitions when they affect the experience, such as a loading screen resolving to content or an error.
- Design recovery for failures users can act on. For example, when saving fails, keep the form values, show a specific error near the affected form or field, and define what users see while retrying and after the retry succeeds or fails again.
- Check content that can change the layout or its meaning. For example, specify how long labels fit on narrow screens, distinguish a valid zero from missing data, and show a fallback when an image fails to load. Include the cases that affect the page's task.

### Microcopy

- Include the proposed user-facing text with the relevant state or interaction. Use specific action labels that tell users what will happen, such as **Save changes** or **Delete product**.
- For confirmation dialogs, name the action and the affected record or selection. Add consequences that help the user decide, such as who will see a publication, how many records will change, or whether deletion can be undone. Label the buttons with their outcomes. For a profile edit, use **Save profile changes?** with **Keep editing** and **Save changes**. For deletion, use **Delete this product?** with **Keep product** and **Delete product**. If saving also publishes the profile, name that effect and use **Save and publish**.
- Write messages for the actual situation. A first-time empty list can offer **Add product**. A filtered list with no matches can offer **Clear filters**. For an error, explain what happened and offer a realistic next step when available. Mention the cause only when it is known.
- Put input requirements and validation next to the relevant field. Reserve tooltips for supplementary information.
- Once the flow and actions are clear, edit the copy for familiar words, brevity, and consistent terminology. Follow the product's language and tone. Preserve facts, conditions, and uncertainty when shortening the text. For example, a failed save can show **Your changes haven't been saved** with **Try again** and a defined outcome for the retry.

## Layout and responsive behavior

- Group components by user task. Keep related controls close together and use larger gaps between groups, following the project's spacing scale where available. Use a divider when spacing alone leaves the boundary unclear.
- Align headings, controls, and content to shared edges. Put the most important information and actions where users can find them quickly. Keep the visual order, reading order, and keyboard focus sequence coherent across layouts.
- Describe what wraps, moves behind a visible control, or stays visible as available space narrows. Base the change on when content and controls stop fitting comfortably, including with longer labels. Keep the primary action reachable. For example, keep search visible and move secondary filters into a Sheet opened by a labeled **Filter** button when the toolbar gets crowded.

## Component decisions

- Prefer the simplest component pattern that supports the real task. Do not add controls or decoration without a user need.
- Use one clear primary action per decision area. Keep destructive actions visually distinct and confirm them when the consequence is meaningful or hard to reverse.
- Choose inputs according to the value and selection behavior: free text, one option, multiple options, date/time, numeric range, or a binary setting.
- Keep labels visible and specific. Use helper text for requirements or examples, and place validation feedback next to the field that needs attention.
- Preserve entered values after recoverable errors. Explain what needs to change and how to fix it.
- Use dialogs for focused, short decisions that need attention. Use a side panel or drawer when users need context or a larger task. Avoid nesting overlays.
- Use tables when users need to compare or scan records across consistent fields. Provide a mobile-appropriate presentation when the table cannot be read comfortably at small widths.
- Use status, progress, and feedback components to explain system state. Do not rely on color alone.
- Use disclosure components when secondary information can remain hidden without blocking the task. Make the collapsed state understandable.
- Keep navigation and page structure predictable. Use breadcrumbs, tabs, pagination, or a sidebar only when they help users understand location or move between related areas.

## Interaction and accessibility

- Make all actions operable by keyboard and show a visible focus state.
- Give every input a programmatic label; associate hints and errors with the relevant field.
- Use semantic headings and landmarks, and keep the reading and focus order aligned with the visual order.
- Ensure controls have clear accessible names, including icon-only buttons.
- For overlays, move focus into the active surface, keep keyboard focus contained while it is open, and return focus to the invoking control when it closes.
- Do not communicate status or validation by color alone. Pair visual signals with text or an accessible announcement.
- Respect reduced-motion preferences and avoid motion that delays or blocks task completion.
- Make targets easy to activate, especially on touch screens, and avoid relying on hover to reveal essential actions.

## Design review

- Match the review to the stage. In a specification or wireframe, check the primary flow, page structure, and whether users can find the main action. In a detailed design, also check visual consistency, microcopy, accessibility, and relevant states such as a failed save or cancelled deletion.
- Write each finding as **Observation → Impact → Suggested fix**. Point to the screen, component, or state, then explain how it affects the user's task. For example, a delete confirmation uses **Yes** as its action label. Users must recall what **Yes** does. Change the label to **Delete product**.
- Prioritize issues that block the task, obscure the consequence of an action, or prevent recovery. Fix findings within the design scope and recheck the affected flow. When a fix depends on a product decision, ask in chat using the options and recommendation format above.

## Output expectations

When designing or reviewing a page, provide:

- A short page and user-task summary.
- The page layout in reading order, with the shadcn/ui components, variants, and content used in each region.
- Visual decisions for color, typography, spacing, and hierarchy, with the relevant design tokens where available.
- Key interactions and relevant screen and component states, with triggers, proposed user-facing copy, next actions, and transitions for states that affect the user's task.
- Responsive layout rules, including what changes as space narrows, how primary actions remain reachable, and any accessibility considerations.
- Open questions or assumptions that affect product behavior.

Tailor the handoff to the destination. For code, specify the page regions, shadcn/ui component variants, and the triggers and outcomes that the implementation should reproduce. For Figma, identify the frames and state variants to draw, the library components and tokens to reuse when available, and the interactions to show in a prototype when relevant. When both are requested, use the same state names, copy, and design decisions across both handoffs.

### Figma workflow

- When the user shares an existing Figma design as input, inspect the relevant frames, component instances, properties, and variants through the available Figma integration. Identify which states and transitions are already represented and specify the missing ones that affect the user's task. If only a screenshot or description is available, state the assumptions that affect the design.
- Map the planned states to named frames or component variants and specify the prototype interactions needed to demonstrate important flows. For example, show how a delete action opens confirmation, returns to the list on cancellation, or proceeds to a pending state and its outcome on confirmation.
- When the user asks to build or update a page, screen, dialog, or other composed view directly in Figma, load `figma:figma-generate-design` alongside `figma:figma-use` and use the UX specification as the design brief. Reuse the target file's library components, variants, and tokens where available. Follow `figma:figma-use` before every `use_figma` call, including programmatic inspection, and `figma:figma-create-new-file` if a new file is requested. When the request is for a Figma-ready plan, deliver the specification.

## Reference

Use [references/components.md](references/components.md) as a component discovery map. For component behavior and variants, consult the official [shadcn/ui components documentation](https://ui.shadcn.com/docs/components) and the relevant component page.
