# sentiment-sort

Design an efficient program that picks the first N among a sorted array of numbers representing customer ratings from -5 to 5 based on sentiment . Positive or Negative Sentiments are ranked higher than median/unbiased ones. eg: -4 should be sorted higher than 3; 2 sorted higher than -1; 5 is sorted higher than 4, and -5 is sorted higher than -4, etc. The array may be of any size < 100, will be un-sorted, and you need to pick only N. You can use any language you like.

### Clojure

```
% lein run -h

-n,   --number N : Take n from sorted array
-a,   --array xs : Array of numbers to sort
-csv, --csv PATH : Sentiment sort a csv file. Treat each line as n,xs pair.
				   Outputs results to out.csv file
```

Examples:

1.

	$ java -jar target/sentiment-sort-0.1.0-standalone.jar --csv-in ../input.csv
	$ cat out.csv

2.

	$ java -jar target/sentiment-sort-0.1.0-standalone.jar -n 5 -a "1 2 3 4 5"

### Go

```
% go-sentiment -h
Usage of go-sentiment:
  -a value
		comma seperated ints to sort
  -csv-in FILE
		Sorts each line of FILE.
  -n N
		Take N after sorting. (default 10)
```

Examples:

1.

	$ go-sentiment -csv-in ../input.csv
	$ cat out.csv

2.

	$ go-sentiment -n 2 -a 1,2,3,4,5
