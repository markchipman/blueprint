@# Control groups

A `.pt-control-group` renders several distinct controls as one unit, squaring the borders between
them. It supports any number of `.pt-button`, `.pt-input`, `.pt-input-group`, and `.pt-select`
elements as direct children.

Note that `.pt-control-group` does not cascade any modifiers to its children. For example, each
child must be marked individually as `.pt-large` for uniform large appearance.

<div class="pt-callout pt-intent-success pt-icon-comparison">
    <h4 class="pt-callout-title">Control group vs. input group</h4>
    <p>Both components group multiple elements into a single unit, but their usage patterns are
    different.</p>
    <p>Think of `.pt-control-group` as a parent with multiple children, each of them a
    "control."</p>
    <p>Conversely, a `.pt-input-group` is a single control, and should function like so. A
    button inside of an input group should only affect that input; if its reach is further, then it
    should be promoted to live in a control group.</p>
</div>

@css pt-control-group

@## Responsive control groups

Add the class `pt-fill` to a control group to make all elements expand equally to fill the
available space. Then add the class `pt-fixed` to individual elements to revert them to their
original default sizes.

Alternatively, add the class `pt-fill` to an individual element (instead of to the container)
to expand it to fill the available space while other elements retain their original sizes.

You can adjust the specific size of an element with the `flex-basis` CSS property.

@css pt-control-group.pt-fill

@## Vertical control groups

Add the class `pt-vertical` to create a vertical control group. Controls in a vertical group
will all have the same width as the widest control.

@css pt-control-group.pt-vertical

@## JavaScript API

The `ControlGroup` component is available in the **@blueprintjs/core** package. Make sure to review [getting started docs for installation info](#blueprint/getting-started).

This component is a simple wrapper around the corresponding CSS API. It supports the full range of HTML props.

```tsx
<ControlGroup fill={true} vertical={false}>
    <Button icon="filter">Filter</Button>
    <InputGroup placeholder="Find filters..." />
</ControlGroup>
```

@reactExample ControlGroupExample

@interface IControlGroupProps
