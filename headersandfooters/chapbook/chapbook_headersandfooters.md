# "Headers and Footers": Chapbook (v1.0.0)

## Summary

"Headers and Footers" demonstrates the use of the [`config.header` and `config.footer`](https://klembot.github.io/chapbook/guide/customization/header-and-footer.html) related configuration settings. When set within a passage, they result in the associated text being either prepended (`config.header`) or appended (`config.footer`) to it and all consecutive passages.

<div class="alertbox information"><strong>Note:</strong> As explained within the documentation, the header and footer (settings) are designed to display a <b>single</b> line of text.</div>

## Live Example

<section>
<iframe src="chapbook_headersandfooters_example.html" height=400 width=90%></iframe>


Download: <a href="chapbook_headersandfooters_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Chapbook: Headers and Footers

:: Start
config.header.center: "This is the center header!"
config.footer.center: "This is the center footer!"
--
This is content between the header and the footer.

```

Download: <a href="chapbook_headersandfooters_twee.txt" target="_blank">Twee Code</a>

