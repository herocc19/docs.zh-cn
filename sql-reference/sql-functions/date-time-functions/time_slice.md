# time_slice

## 功能

根据指定的时间粒度周期，将给定的时间转化为其所在的时间粒度周期的起始时刻。

## 语法

```Plain Text
DATETIME time_slice(DATETIME dt, INTERVAL N type)
```

## 参数说明

- `dt`：需要转化的时间。支持的数据类型为 DATETIME。

- `INTERVAL N type`：`N`是INT类型的时间周期；`type`值可以是：YEAR，MONTH，DAY，HOUR，MINUTE，SECOND，WEEK，QUARTER。

## 返回值说明

返回值的数据类型为 DATETIME。

## 注意事项

时间粒度周期从公元`0001-01-01 00:00:00`算起。

## 示例

示例一：将给定时间转化到以5秒为时间粒度周期的起始时刻。

```Plain Text
select time_slice('2022-04-26 19:01:07', interval 5 second);
+------------------------------------------------------+
| time_slice('2022-04-26 19:01:07', INTERVAL 5 SECOND) |
+------------------------------------------------------+
| 2022-04-26 19:01:05                                  |
+------------------------------------------------------+
```

示例二：将给定时间转化到以5天为时间粒度周期的起始时刻。

```Plain Text
select time_slice('0001-01-07 19:01:07', interval 5 day);
+---------------------------------------------------+
| time_slice('0001-01-07 19:01:07', INTERVAL 5 DAY) |
+---------------------------------------------------+
| 0001-01-06 00:00:00                               |
+---------------------------------------------------+
```
