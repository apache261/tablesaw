# Tablesaw

A set of plugins for responsive tables.

## Table Modes

### Stack

The Stack Table stacks the table headers to a two column layout with headers on the left when the viewport width is less than `40em` (`640px`).

    <table data-mode="stack">

* [Stack Table Demo](http://filamentgroup.github.io/tablesaw/demo/stack.html)

### Toggle

The Column Toggle Table allows the user to select which columns they want to be visible.

    <table data-mode="columntoggle">

Table headers must have a `data-priority` attribute to be eligible to toggle. `data-priority` is a numeric value from 1 to 6, which determine default breakpoints at which a column will show. As of first release, the defaults are:

    <th data-priority="persist"><!-- Not eligible for toggle, always shows --></th>
    <th data-priority="1"><!-- Shows at (min-width: 20em) (320px) --></th>
    <th data-priority="2"><!-- Shows at (min-width: 30em) (480px) --></th>
    <th data-priority="3"><!-- Shows at (min-width: 40em) (640px) --></th>
    <th data-priority="4"><!-- Shows at (min-width: 50em) (800px) --></th>
    <th data-priority="5"><!-- Shows at (min-width: 60em) (960px) --></th>
    <th data-priority="6"><!-- Shows at (min-width: 70em) (1120px) --></th>

* [Column Toggle Demo](http://filamentgroup.github.io/tablesaw/demo/toggle.html)

### Swipe

Allows the user to use the swipe gesture (or use the left and right buttons) to navigate the columns.

    <table data-mode="swipe">

Columns also respect the `data-priority="persist"` attribute.

    <th data-priority="persist"><!-- Always shows --></th>

* [Swipe Demo](http://filamentgroup.github.io/tablesaw/demo/swipe.html)

## Mode Switcher

* [Mode Switcher Demo](http://filamentgroup.github.io/tablesaw/demo/modeswitch.html)

    <table data-mode-switch>

    <!-- With a different default mode -->
    <table data-mode="swipe" data-mode-switch>

    <!-- Exclude a mode from the switcher -->
    <table data-mode-switch data-mode-exclude="columntoggle">

## Sortable

Allows sorting on columns.

    <table data-sortable>
        <thead>
            <tr>
                <!-- Default column -->
                <th data-sortable-col data-sortable-default-col>Rank</th>
                <th data-sortable-col>Movie Title</th>
                <th data-sortable-col>Year</th>
                <th data-sortable-col><abbr title="Rotten Tomato Rating">Rating</abbr></th>
                <!-- Unsortable column -->
                <th>Reviews</th>
            </tr>
        </thead>
        ...

Use `data-sortable-switch` to add a form element to choose the sort order.

    <table data-sortable data-sortable-switch>

* [Sortable Demo](http://filamentgroup.github.io/tablesaw/demo/sort.html)

## Kitchen ~~Table~~ Sink

All of the above options combined into a single table.

* [Kitchen Sink Demo](http://filamentgroup.github.io/tablesaw/demo/kitchensink.html)

## Getting Started

```html
<link rel="stylesheet" href="tablesaw.css"></script>
<script src="jquery.js"></script>
<script src="tablesaw.js"></script>
```

## Release History
_(Nothing yet)_

## TODO

* Generate a zip file that can be downloaded (includes minified/full sources, icons)
* Tests
* Add to bower
* Add VanillaJS/non-jQuery version