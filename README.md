I want to know how much time I've spent in a specific area.
I use it together with PhoneTrack in my Nextcloud to track myself.

The tool takes a GPX file from PhoneTrack, you enter some bounding coordinates
and it will tell you how much time you've spent there, grouped by day.

```bash
./filter-gpx.kscript --topleft=53.1234,9.1234 --bottomright=53.4321,9.4321
```

Output will look like this:

```
2019-07-15: PT5H49M17S (249 Points)
2019-07-16: PT8H21M48S (441 Points)
2019-07-17: PT7H51M32S (471 Points)
2019-07-18: PT0S (337 Points)
```
