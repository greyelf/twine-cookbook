# "Arrays": Harlowe (v3.0.1 or later)

## Summary

[Arrays](https://twine2.neocities.org/#type_array) are a collection of values. Each entry in an array is assigned an *index*, which is a number that corresponds to its position in the array. In Harlowe, and unlike in JavaScript, arrays are *one-based*, meaning the first element in the array is given the index `1`. Arrays can be created using the `(a:)` or `(array:)` macro and assigning a variable to it: `(set: $myArray to (a:))`.

Specific elements in an array can be accessed by following its variable name with a possessive `'s` and an ordinal number referencing the index to check, (`$myArray's 2nd`); the final entry, `$myArray's last`, points to the final element. Its contents can be tested using the `contains` operator (e.g. `(if: $myArray contains 'something')[...]`), add new items using the `+` operator (e.g. `(set: $myArray to + (a: 'something'))`), and remove items using the `-` operator. All elements in an array can be passed to macros as separate arguments with the spread operator (`...`). 

## Live Example

<section>
<iframe src="harlowe_arrays_example.html" height=400 width=90%></iframe>


Download: <a href="harlowe_arrays_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Arrays in Harlowe


:: init [startup]
<!-- it is always a good idea to initialize your variables, but with arrays it is particularly important -->
(set: $inventory to (a:))
(set: $chest to (a: 'a shield', 'a suit of armor'))
(set: $chestOpen to false)


:: inventory [header]
You are currently carrying:
{
	<!-- if the inventory contains nothing, show "nothing" -->
	(if: $inventory's length is 0)[
		nothing.
	](else:)[
		<!-- we iterate over the array and print each item -->
		(for: each _item, ...$inventory)[
			_item (unless: $inventory's last is _item)[, ]
		].
	]
}
<hr>


:: Start
<!-- we use the + operator and wrap the target elements in an (a:) macro to add to the array -->\
You find yourself inside a small room. In the corner, you see a sword, and decide to pick it up.

(set: $inventory to it + (a: 'a sword'))\
[[Continue|hallway]]


:: hallway
You see a chest here in the hallway.  \
(unless: $chestOpen)[\
    Do you want to open it?

    {
		(link-reveal-goto: 'Open the chest.', 'chest')[
			<!-- adding to arrays together can also be done with the + operator -->
			(set: $inventory to it + $chest)
			(set: $chestOpen to true)
		]
    }
](else:)[\
    It's open, and there's nothing inside.
]\

[[Move on.|dart trap]]


:: chest
You open the chest and find (for: each _item, ...$chest)[\
    _item (unless: $chest's last is _item)[ and ]\
].

(link-goto: 'Okay', (history:)'s last)


:: dart trap
Several darts shoot out of a wall at you!
<!-- we can check to see if the player has a given item with the contains operator -->
(if: $inventory contains 'a shield')[\
    Luckily, your shield will protect you.
](else:)[\
    With no way to defend yourself, you die.
]


:: UserStylesheet [stylesheet]
/* Hide empty lines created by startup tagged special passage. */
tw-include[type="startup"] {
	display: none;
}

/* Fix displaying of block based elements issue. */
hr {
	display: inline-block;
	width: 100%;
}
```

Download: <a href="harlowe_arrays_twee.txt" target="_blank">Twee Code</a>
