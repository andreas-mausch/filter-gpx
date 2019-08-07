I want to know how much time I've spent in a specific area.
I use it together with PhoneTrack in my Nextcloud to track myself.

# Requirements

You need kscript installed on your machine.

# Usage

The tool takes a GPX file from PhoneTrack, you enter center coordinates and a radius
and it will tell you how much time you've spent there, grouped by day/hour/month.

```bash
./filter-gpx.kscript --center=53.1234,9.1234 --radius=100 --groupBy=DAY --verbose --hideZeros gpx.xml
```

Output will look like this:

```
2019-07-15: 05h 53m 01s (249 Points)
	Enter: 2019-07-15 11:33:51 Leave: 2019-07-15 12:44:58
	Enter: 2019-07-15 13:30:38 Leave: 2019-07-15 18:12:32
2019-07-16: 08h 24m 01s (441 Points)
	Enter: 2019-07-16 09:54:04 Leave: 2019-07-16 18:18:05
2019-07-17: 07h 55m 33s (471 Points)
	Enter: 2019-07-17 09:57:32 Leave: 2019-07-17 12:58:01
	Enter: 2019-07-17 14:27:58 Leave: 2019-07-17 19:23:02
2019-07-19: 08h 50m 57s (334 Points)
	Enter: 2019-07-19 10:04:07 Leave: 2019-07-19 12:36:30
	Enter: 2019-07-19 12:51:31 Leave: 2019-07-19 19:10:05
```

# locations.yaml

Create a file `locations.yaml` in the same directory filter-gpx is in to give your favorite locations names:

```yaml
home: 53.1234,9.1234
```

Then, you can pass `--center=home` as parameter to filter-gpx.
