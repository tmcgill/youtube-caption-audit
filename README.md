# YouTube Caption Audit
This application checks all public videos in a given YouTube channel and reports back which videos do not have human-created closed captions. All required code is contained in a single file for ease of sharing and distribution. Run this in whatever environment(s) permitted by your API key.
## Usage
Enter your API key and YouTube channel ID and click 'Check videos'.
### Presets
You can optionally define API key and Channel ID presets in an sidecar file named config.json located in the same directory as index.html
```JSON
{
	"apiKey": "[your API key]",
	"filtering": "off" || "on",
	"channels": [
		{
			"name": "[your chosen preset name]",
			"id": "[channel ID for this preset]"
		},
		{
			"name": "[your chosen preset name]",
			"id": "[channel ID for this preset]"
		}
	]
}
```
There is no limit to the number of channel presets you can define, but they will all use the same API key. If "filtering" is included in config.json and its value is set to "off", all videos for a selected channel will be included in the results table (not just the uncaptioned ones). This may be useful for debugging or deomonstration, but "filtering" should be omitted or set to "on" for normal usage.
## Copyright and License
Developed by UCI Strategic Communications & Public Affairs

Copyright 2018 UC Regents

Licensed under MIT (https://opensource.org/licenses/MIT)
