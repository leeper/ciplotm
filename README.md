# ciplotm
This is a fork of Nick Cox's [`ciplot` ado for Stata](https://ideas.repec.org/c/boc/bocode/s431202.html). It adds an optional `sepby` argument the controls the display behavior when using multiple variables in `varlist` combined with the `by()` option. If `sepby`, then `ciplotm` behaves the same as the original `ciplot`. If not using `sepby` (the new default), then bars for each variable are aligned (vertically or horizontally, depending on the other options).

This is athe default behavior of `ciplot` (or the optional behavior or `ciplotm` with the `, sepby` argument):

```Stata
webuse citytemp, clear
ciplot heatdd cooldd, by(region) horizontal recast(conn)
```

![ciplot](http://i.imgur.com/L55GkUk.png)

And here's the new default behavior using `ciplotm`:

```Stata
ciplotm heatdd cooldd, by(region) horizontal recast(conn)
webuse citytemp, clear
```

![ciplotm](http://i.imgur.com/r0XKbjZ.png)

See [this StackOverflow post for background context](http://stackoverflow.com/questions/30890710/align-bars-in-ciplot).
