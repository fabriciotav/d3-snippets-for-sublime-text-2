D3.js snippets for Sublime Text 2
=================================

## Selections

**sel** ⇥ `d3.select('')`

**sela** ⇥ `d3.selectAll('')`

**attr** ⇥ `.attr('', )`

**translate** ⇥ `.attr('transform', 'translate(' + 0 + ',' + 0 + ')')`

**style** ⇥ `.style('fill', '#000')`

**join** ⇥

<pre><code>d3.selectAll('')
    .data()

</code></pre>

**margin** ⇥

<pre><code>var margin = { top: 10, right: 10, bottom: 10, left: 10 };
    width = 960 - margin.left - margin.right,
    height = 640 - margin.top - margin.bottom;

var svg = d3.select('body').append('svg')
    .attr('width', width + margin.left + margin.right)
    .attr('height', height + margin.top + margin.bottom)
  .append('g')
    .attr('transform', 'translate(' + margin.left + ',' + margin.top + ')');
</code></pre>

## Data

**dsv** ⇥ `var dsv = d3.dsv(';', 'text/plain');`

**csv** ⇥

<pre><code>d3.csv('/', function(d) {
  return {

  };
}, function(err, rows) {

});
</code></pre>

**json** ⇥

<pre><code>d3.json('/', function(err, data) {

});
</code></pre>

## SVG shapes

**circle** ⇥

<pre><code>.enter().append('circle')
    .attr('cx', )
    .attr('cy', )
    .attr('r', )
    .style('fill', '#000');
</code></pre>

**ellipse** ⇥

<pre><code>.enter().append('ellipse')
    .attr('cx', )
    .attr('cy', )
    .attr('rx', )
    .attr('ry', )
    .style('fill', '#000');
</code></pre>

**line** ⇥

<pre><code>.enter().append('line')
    .attr('x1', )
    .attr('y1', )
    .attr('x2', )
    .attr('y2', )
    .style('stroke', '#000');
</code></pre>

**rect** ⇥

<pre><code>.enter().append('rect')
    .attr('x', )
    .attr('y', )
    .attr('width', )
    .attr('height', )
    .attr('rx', 0)
    .attr('ry', 0)
    .style('fill', '#000');
</code></pre>

## Geography

**map** ⇥

<pre><code>var projection = d3.geo.equirectangular()
    .center([0, 0])
    .scale(0)
    .translate([width / 2, height / 2]);

var path = d3.geo.path()
    .projection(projection);
</code></pre>

## Functions

**fd** ⇥ `function(d) { return ; }`

**fdi** ⇥ `function(d, i) { return ; }`

**fn** ⇥ `function() { return ; }`

## Miscellaneous

**scale** ⇥ `d3.scale.linear().domain([]).range([]);`

**nest** ⇥

<pre><code>var nest = d3.nest()
    .key(function(d) { return d; })
    .entries([]);
</code></pre>

**locale** ⇥

<pre><code>var d3.locale.en_US = d3.locale({
  'decimal': '.',
  'thousands': ',',
  'grouping': [3],
  'currency': ['\$', ''],
  'dateTime': '%a %b %e %X %Y',
  'date': '%m/%d/%Y',
  'time': '%H:%M:%S',
  'periods': ['AM', 'PM'],
  'days': ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'],
  'shortDays': ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'],
  'months': ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
  'shortMonths': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
});
</code></pre>