# "Google Fonts": Chapbook (v1.0.0)

## Summary

"Google Fonts" uses a [Google Font](https://fonts.google.com/) loaded via Chapbook's ```config.style.googleFont``` [External Web Fonts](https://klembot.github.io/chapbook/guide/customization/external-web-fonts.html) configuration setting. A class style rule ("message") is then created using the imported font-family and applied to a ```<div>``` element within a single passage. 

Other Google Fonts could be imported and applied using the same method, creating new class or ID style rules to be applied for and across different HTML elements in the same way.

## Live Example

<section>
<iframe src="chapbook_googlefonts_example.html" height=400 width=90%></iframe>


Download: <a href="chapbook_googlefonts_example.html" target="_blank">Live Example</a>
</section>

## Twee Code

```
:: StoryTitle
Chapbook: Google Fonts

:: StoryStylesheet [stylesheet]
.message {
	font-family: 'Roboto', sans-serif; 
}

:: Start
config.style.googleFont: '<link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">'
--
<div class="message">This text is styled using a Google Font</div>

```

Download: <a href="chapbook_googlefonts_twee.txt" target="_blank">Twee Code</a>
