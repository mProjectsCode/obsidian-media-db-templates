`$= '![Image|360](' + dv.current().image + ')'`

# `$= dv.current().title`

> [!INFO] Status
> `$= dv.current().watched ? 'last watched on ' + dv.current().lastWatched : 'not yet watched'`

`$= dv.current().watched ? '**Rating**: ' + dv.current().personalRating + ' out of 10' : ''`

**Genres**:
`$= dv.current().genres.length === 0 ? ' - none' : dv.list(dv.current().genres)`

`$= !dv.current().released ? '**Not released** The movie is not yet released.' : ''`
**Type**: `$= dv.current().type`
**Online Rating**: `$= dv.current().onlineRating`
**Duration**:  `$= dv.current().duration`
**Premiered**: `$= dv.current().premiere`
**Producer**: `$= dv.current().producer`