
# very simple time format module


### function time_format(time, options);

#### 参数

* time         {Date}   日期对象，可选
* options      {Object} 选项，可选<br>
  options.date {Bool}   是否包含日期，默认值为 true<br>
  options.time {Bool}   是否包含时间，默认值为 true<br>
  options.zone {Bool}   是否包含时区，默认值为 false<br>


#### 返回值 
 {String} 格式如 '2015-11-13 21:45:48 +0800'


### Usage:
```
var time_format = requrie('time_format');

time_format();                              // => '2015-10-01 10:05:05'
time_format({ time: false });               // => '2015-10-01'
time_format({ date: false });               // => '10:05:05'
time_format({ zone: true  });               // => '2015-10-01 10:05:05 +08:00'
time_format({ time: false, zone: true  });  // => '2015-10-01 +08:00'

var d = new Date();
time_format(d);                                // => '2015-10-01 10:05:05'
time_format(d, { time: false });               // => '2015-10-01'
time_format(d, { date: false });               // => '10:05:05'
time_format(d, { zone: true  });               // => '2015-10-01 10:05:05 +08:00'
time_format(d, { time: false, zone: true  });  // => '2015-10-01 +08:00'

```
