[![Go Reference](https://pkg.go.dev/badge/github.com/sitnikovv/jodaTime.svg)](https://pkg.go.dev/github.com/sitnikovv/jodaTime)
[![Build Status](https://travis-ci.org/sitnikovv/jodaTime.svg)](https://travis-ci.org/sitnikovv/jodaTime)
[![Coverage Status](https://coveralls.io/repos/github/sitnikovv/jodaTime/badge.svg?branch=master)](https://coveralls.io/github/sitnikovv/jodaTime?branch=master)
[![Go Report Card](http://goreportcard.com/badge/sitnikovv/jodaTime)](http:/goreportcard.com/report/sitnikovv/jodaTime)

# JodaTime
forked from https://github.com/vjeantet/jodaTime
* Format golang date time.Time with joda layout
* Parse time with joda layout


reference : [http://joda-time.sourceforge.net/apidocs/org/joda/time/format/DateTimeFormat.html](http://joda-time.sourceforge.net/apidocs/org/joda/time/format/DateTimeFormat.html)

# Usage
```go
package main

import (
	"fmt"
	"time"

	"github.com/sitnikovv/jodaTime"
)

func main() {
	date := jodaTime.Format("YYYY.MM.dd", time.Now())
	fmt.Println(date)

	dateTime, _ := jodaTime.Parse("dd/MMMM/yyyy:HH:mm:ss", "30/August/2015:21:44:25")
	fmt.Println(dateTime.String())
}

```

# Format
```
 Symbol  Meaning                      Presentation  Examples
 ------  -------                      ------------  -------
 G       era                          text          AD
 C       century of era (>=0)         number        20
 Y       year of era (>=0)            year          1996

 x       weekyear                     year          1996
 w       week of weekyear             number        27
 e       day of week                  number        2
 E       day of week                  text          Tuesday; Tue

 y       year                         year          1996
 D       day of year                  number        189
 M       month of year                month         July; Jul; 07
 d       day of month                 number        10

 a       halfday of day               text          PM
 K       hour of halfday (0~11)       number        0
 h       clockhour of halfday (1~12)  number        12

 H       hour of day (0~23)           number        0
 k       clockhour of day (1~24)      number        24
 m       minute of hour               number        30
 s       second of minute             number        55
 S       fraction of second           number        987654321

 z       time zone                    text          Pacific Standard Time; PST
 Z       time zone offset/id          zone          -0800; -08:00; America/Los_Angeles

 '       escape for text              delimiter
 ''      single quote                 literal       '
```
