# "Cycling Choices": Chapbook (v1.0.0)

## Summary

"Cycling Choices" demonstrates how to create a 'cycling' effect of different choices through clicking on them. 

The [{cycling link}](https://klembot.github.io/chapbook/guide/player-input/dropdown-menus-cycling-links.html#cycling-links) insert generates a link that allows the cycling though the array of values you provide as the insert's `choices:` argument. Whichever array value that is currently displayed will be assigned to the variable indicated in the optional `for:` argument.

## Live Example

<section>
<iframe src="chapbook_cycling_example.html" height=400 width=90%></iframe>


Download: <a href="chapbook_cycling_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Cycling Choices in Chapbook

:: Start
Click options to cycle: {cycling link for: 'cyclingResult', choices: ["First", "Second", "Third"]}

[[Submit|Results]]

:: Results
{cyclingResult}

```

Download: <a href="chapbook_cycling_twee.txt" target="_blank">Twee Code</a>

## See Also

[Setting and Showing Variables](../../settingandshowing/chapbook/chapbook_settingandshowing.md)
