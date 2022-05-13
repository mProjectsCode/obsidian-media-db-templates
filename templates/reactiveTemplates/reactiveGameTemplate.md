`$= '![Image|360](' + dv.current().image + ')'`

# `$= dv.current().title`

> [!INFO] Status
> `$= dv.current().played ? 'played' : 'not yet played'`

`$= dv.current().played ? '**Rating**: ' + dv.current().personalRating + ' out of 10' : ''`

**Genres**:
`$= dv.current().genres.length === 0 ? ' - none' : dv.list(dv.current().genres)`

`$= !dv.current().released ? '**Not released** The game is not yet released.' : ''`
**Type**: `$= dv.current().type`
**Online Rating**: `$= dv.current().onlineRating`
**Release Date**: `$= dv.current().releaseDate`