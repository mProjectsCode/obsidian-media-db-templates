`$= '![Image|360](' + dv.current().image + ')'`

# `$= dv.current().title`

> [!INFO] Status
> `$= dv.current().watched ? 'last watched on ' + dv.current().lastWatched : 'not yet watched'`

`$= dv.current().watched ? '**Rating**: ' + dv.current().personalRating + ' out of 10' : ''`

**Genres**:
`$= dv.current().genres.length === 0 ? ' - none' : dv.list(dv.current().genres)`

```dataviewjs
let text = '';

if (!dv.current().released) {
	text += '**Not released**\n';
	if (dv.current().airedFrom) {
		text += 'The series will release on ' + dv.current().release_date + '.';
	} else {
		text += 'The series is not released yet.';
	}
	
} else if (dv.current().airing) {
	text += '**Not finished**\n';
	text += 'The series is not fully released yet.';
}

if (text) {
	dv.paragraph(text);
}
```

**Type**: `$= dv.current().type`
**Online Rating**: `$= dv.current().onlineRating`
**Episodes**: `$= dv.current().episodes`
**Duration**:  `$= dv.current().duration`
**Aired from**: `$= dv.current().airedFrom`
**Aired until**: `$= dv.current().airedTo`
**Studios**: `$= dv.current().studios.join(', ')`