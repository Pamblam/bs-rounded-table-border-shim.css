# Bootstrap Rounded Table Border Shim

Putting a border-radius on a table isn't as easy as you might think.

This is because, for whatever reason, `border-collapse: collapse` breaks any `border-radius` directive.

The solution is to set `border-collapse: separate`, `border-spacing: 0`, then make sure every individual cell has a top and right border, and then only set bottom and left borders on the bottom row and left column.

These fixes work for all tables, not just Bootstrap, but I wrote the shiim specifically with Bootstrap in mind because I wanted to use Bootstrap's card component with `.d-table`, which renders it as a table.

This shim fixes Bootstrap's built-in `.table-bordered` class, and adds a new class: `.table-rounded`, which adds a border-radius to a table, with or without a border.

Check out the demo.html for examples.