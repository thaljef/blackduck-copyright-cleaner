#Black Duck Copyright Cleaner

This project is an exploration of how Machine Learning technologies could be applied to improve some of the data provided by Black Duck. Specifically, I am focussing on improving the quality of the copyright statements shown in the Notices Report produced by Black Duck. Technically, copyright statements are unstructured text, but they are fairly constrained, so this seems like an ideal application of Machine Learning.

As a starting point, I have written a small script that uses Google's Entity Analysis API. The salient parts of any copyright statement are dates (years) and the names of one or more persons or organizations. These match up pretty well with the entity types the Google API can identify.


#Input File Format

The input format is equivalent to the "Copyrights" section of the Notices file produced by Black Duck. It consists of repeated blocks of component names followed by 1 or more copyright statements. Each copyright statement is indented by 5 characters and ends in a newline character. Like this:

```
component name 1
	copyright statement 1
	copyright statement 2
	copyright statement n
component name 2
	copyright statement 1
	copyright statement 2
	copyright statement n
```
