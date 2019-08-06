I want to know how much time I've spent in a specific area.
I use it together with PhoneTrack in my Nextcloud to track myself.

The tool takes a GPX file from PhoneTrack, you enter center coordinates and a radius
and it will tell you how much time you've spent there, grouped by day/hour/month.

```bash
./filter-gpx.kscript --center=53.1234,9.1234 --radius=100 --groupBy=DAY --verbose --hideZeros gpx.xml
```

Output will look like this:

```
2019-07-15: PT5H53M1S (249 Points)
	Enter: 2019-07-15T09:33:51Z Leave: 2019-07-15T10:44:58Z
	Enter: 2019-07-15T11:30:38Z Leave: 2019-07-15T16:12:32Z
2019-07-16: PT8H24M1S (441 Points)
	Enter: 2019-07-16T07:54:04Z Leave: 2019-07-16T16:18:05Z
2019-07-17: PT7H55M33S (471 Points)
	Enter: 2019-07-17T07:57:32Z Leave: 2019-07-17T10:58:01Z
	Enter: 2019-07-17T12:27:58Z Leave: 2019-07-17T17:23:02Z
2019-07-19: PT8H50M57S (334 Points)
	Enter: 2019-07-19T08:04:07Z Leave: 2019-07-19T10:36:30Z
	Enter: 2019-07-19T10:51:31Z Leave: 2019-07-19T17:10:05Z
```
