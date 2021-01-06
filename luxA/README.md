# Lux Arescentum

<blockquote>Once a sea of endless infinities, a desert of infinite single conclusions is all that remains.</blockquote>

## Files

LuxA follows what I hope will be a sort of standard for my small twine projects.

<table>
<tr>file<th></th><th>purpose</th></tr>
<tr><td>*.twee</td><td>Human Readable Source</td></tr>
<tr><td>*.archive.html</td><td>Twine2 Archive</td></tr>
<tr><td>*.scratch.md</td><td>Story Scratchpad</td></tr>
<tr><td>*.pal(X).png</td><td>Color Palettes</td></tr>
<tr><td>*.title(X).png</td><td>Cover Images</td></tr>
<tr><td>*.cont.X.png</td><td>Content Images</td></tr>
</table>

## Build Process

Eventually I'll script this, but for now, the following steps should be followed when making changes to the story in twee or twine.

### Twine2 changes

If content was edited in Twine2, use the following process to make a new *.twee and *.archive.html file.

1. Publish the story to luxA/luxA.html
2. Use tweego to make a new twee source
```
tweegoPath/tweego -d luxA/luxA.html > luxA/luxA.twee
```
3. Use tweego to make a new twine2 archive
```
tweegoPath/tweego -a luxA/luxA.html > luxA/luxA.archive.html
```

### Twee changes

If content was edited directly in the *.twee file, use the following process to make new *.html and *.archive.html files.

1. Use tweego to make a new published copy
```
tweegoPath/tweego luxA/luxA.twee > luxA/luxA.html
```
2. Use tweego to make a new twine2 archive
```
tweegoPath/tweego -a luxA/luxA.html > luxA/luxA.archive.html
```

## Embedding images

You can embed whatever images you would like using base64 encoding. This adds a large amount of overhead to the filesize of an image, but allows the story to be distributed as a single html file. I will describe how to do this with *.png files, but it is my understanding this can be applied to *.jpg and *.gif files as well.

1. Generate the base64 hash of your image file. This can be done using a site like [base64-image.de](https://www.base64-image.de/) or using a base64 utility in shell like so:
```
username$ base64 luxA/luxA.titleOne.png 
iVBORw0KGgoAAAANSUhEUgAAAKAAAACQCAMAAAC4a5CyAAAAAXNSR0IArs4c6QAAAAxQTFRFHh48UFBuvr7m5ub/VhjMZgAAA91JREFUeJztnOuWqyAMhbvy/g991ixbFchl7wjUesiPjgMh+QRM0EpfryVLziLfBghE7k54d0B53XyQcUD5znkswKuyAK+KByiNzCR7M5w+G7K60KgYKg2gDXAqnkhZAPpu2x6dAXkAhu60eoIxeTIfQMBRPPKAJ1pk84G0NpXA5jBT3UzA9QwzP3VPGdnO/jIggJgDFD0OphCC+gzgPrhdAAMNHvA0uJ0AXR0aUJrPvHOEgwT8eOsOaKrZQcrV7g9oWWMAz2nfbRxaIjQJQGmOacAoeWi9AphVNHOAcXD3u8UwqymmAJFGfr+oZlW9YYDtKj002/6H+qra1n8hzxigMXfZGBq43L0qs91StXVGAirxQjNWB73WGwfo23vXpADNnNIdcPcaDF8JaGegcYCxsqY6E/Alsf+ys7U4QwEC86qcWBigPRHZR8AsINiDdwf05k0yCuKAbraSSpvGcRcbYA+2aaUboHIJjQBEbI4E9ELFNUBl9oiioDQsxywAdBxMAqymWTdALbiPAARM+qU8YKNjRtsfAIRW3sMBnQcOeUA1/fx/gPXg9weMIMVzPAEwXA39OuCFMAMBxoP8ATQ9A4BqL+jBJQ1od81swNrUAiQBG1suoIwGFEXVAFRdL8DnA0aPgGlAFaaqNrpkAS7ABbgAIcAyJj4esC38HqDq+dGAJYnhcQFeBWyAWMCmuANg0W0woMF3A0DP8SDAM8VlQP3sIUBn9hxfn6CAJt8YQLvtAwGNi95zUuu6gIr9IC3FBhQVL4r6fJitYBAizeGAxBhQgHbQ8LzRgLGL0YCRiTwg8y68YwsA4I2mJcF3f8AoI4/d/BcsZ7Ta9ruJgYA7Hx4L7wjorzhGAh75Eg+GMwHlOMCj4UTAs1M8Grb5YQYfEa85wAt76bxp5ekzgMfaPoHIAhbLp3iNU1MFe4b8InDZYW1ycRYzgJpe176vA42BEIBUVg2zKXopqvuYjGUsVlaYtRSJlaX2wmF3wHbAvcaqkxAQHfZPeX1JtO1gQGyzXx5Q3QWEuDx0Jda2SYxicTXYIY5TQxbQfrvjyhzEQSJArxkJSCcGt+b99oJzlSd60N2QS9b8AUb2EkPsnzFTE27yJtacxWRhdzqagOHu3iSghcgBSrzNOw+onz0BKNurGwMBX0o3woB7ah8L2HQjBnhqlEydtqaWL8+QYaCublRw/6G4IX+/QXJTgnIXNQtwq7Nu5Cb9WgoW1eWDU/zezHC4zTUGiJd2FjAvqhG5N4vp+QmAxp3FBIGXPgNDSeQYdEU8+ugqTF6U+mCKMM6+9pNbS5YsWbJkya/KP2tCCyX6QlPnAAAAAElFTkSuQmCC
```
2. Create a new passage for your image in twine2 or in the twee code, remember this as $imgName
3. Add an image tag as below, replacing $base64 with the output of your base64 encoding
```
<img src="data:image/png;base64,$base64">
```
4. Add a note below the image tag with the original filepath/filename of the image source
```
[note]
luxA.titleOne.png
[cont]
```
5. Now whenever you want to use the image in the story you can reference it as such (this assume Chapbook story format) replacing $imgName with the passage name from step 2
```
{embed passage: '$imgName'}
```
