# "Modularity": Chapbook (v1.0.0)

## Summary

In programming terminology, modularity refers to dividing software into different sections related to their purpose or to better organize the whole. In Chapbook, this technique can be used through the [`{embed passage:}`](https://klembot.github.io/chapbook/guide/modifiers-and-inserts/embedding-passages.html) insert to print the contents of one passage in another. Parts of a story can often be re-used in this way.

## Live Example

<section>
<iframe src="chapbook_modularity_example.html" height=400 width=90%></iframe>


Download: <a href="chapbook_modularity_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Modularity in Chapbook

:: Start
lineOne: "Give us a verse"
lineTwo: "Drop some knowledge"
--
{embed passage: "showLineOne"}
{embed passage: "showLineTwo"}

:: showLineOne
{lineOne}

:: showLineTwo
{lineTwo}
```

Download: <a href="chapbook_modularity_twee.txt" target="_blank">Twee Code</a>

