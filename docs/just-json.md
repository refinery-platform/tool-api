Just trying to get some examples of the data shapes we'll need.
Goal is to clarify the requirements for each example, then rename the properties for consistency,
and then articulate a schema + other checks that do what we need.

I'm a little bit wary of trying to find the fully general solution now... 
Risk of expending effort on features that we end up not really needing.

For the sake of focus, just doing the inputs here.

## IGV

```json
{
  "tracks": [
    {
      "uuid": "12345-67890 and we'll check the file type before launch?",
      "title": "can be specified manually?"
    },
    {
      "url": "http://example.com/check-extension-and-make-sure-that-this-supports-cors-unless-server-caches?"
    }
  ],
  "optional_columns_to_display": [
    "server checks that",
    "these names correspond",
    "to metadata fields?"
  ],
  "required_genome": "hg19, unless it can be determined from data? Hard to capture in declarative syntax"
}
```

## Heatmap-Scatterplot

```json
{
  "files": [
    "uuid",
    "and/or url?"
  ]
}
```