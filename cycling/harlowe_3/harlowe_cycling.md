# "Cycling Choices": Harlowe (v3.0.1 or later)

<div class="alert information"><strong>Note: </strong>This example is affected by history changes in the story. Undoing or re-doing back to a passage containing this recipe has the potential to change its saved values.</div>

## Summary

"Cycling Choices" demonstrates how to create a 'cycling' effect of different choices through clicking on them.

It uses the [*(cycling-link:)*](https://twine2.neocities.org/#macro_cycling-link) macro to display a link which when selected loops though each of the elements of the *$choices* [Array](https://twine2.neocities.org/#type_array) one by one, returning to the first element once last element has been shown.

The currently displayed element's value is also stored within the *$selected* story variable.

## Live Example

<section>
<iframe src="harlowe_cycling_example.html" height=400 width=90%></iframe>


Download: <a href="harlowe_cycling_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Cycling Choices in Harlowe (v3.0.1 or later)

:: Start
{
(set: $choices to (array: "First", "Second", "Third"))
(set: $selected to $choices's 1st)

Click options to cycle: (cycling-link: bind $selected, ...$choices)
}
[[Submit|Results]]

:: Results
Selected choice: $selected
```

Download: <a href="harlowe_cycling_twee.txt" target="_blank">Twee Code</a>

## See Also

[Setting and Showing Variables](../../settingandshowing/harlowe/harlowe_settingandshowing.md), [Modularity](../../modularity/harlowe/harlowe_modularity.md)
