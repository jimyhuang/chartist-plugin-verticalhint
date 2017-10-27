# Vertical Hint plugin for Chartist.js

This plugin inspired by https://github.com/tmmdata/chartist-plugin-tooltip
When mouse over the horizontal label, it will show all values of that column in the tip.

Please visit http://gionkunz.github.io/chartist-js/plugins.html for more information.

## Sample usage in Chartist.js

online demo [here](https://jimyhuang.github.io/chartist-plugin-verticalhint/index.html).

![chartist plugin verticalhint screenshot](https://jimyhuang.github.io/chartist-plugin-verticalhint/chartist-plugin-verticalhint.png)

```js
var chart = new Chartist.Line('.ct-chart', {
  labels: ['2011', '2012', '2013', '2014', '2015', '2016'],
  series: [
    // seriese 1
    [
      {meta: 'description', value: 1},
      {meta: 'description', value: 5},
      {meta: 'description', value: 3},
      {meta: 'description', value: 3},
      {meta: 'description', value: 3},
      {meta: 'description', value: 3}
    ],
    // series 2
    [
      2, 4, 2, 2, 4, 2
    ]
  ],
}, {
  plugins: [
    Chartist.plugins.verticalhint({
      valuePrefix: 'USD$',
      valueSuffix: '.00',
      customSelector: '',
      seriesLabel:[
        'Google', // series 1 label
        'Apple', // series 2 label
      ],
    })
  ]
});
```

