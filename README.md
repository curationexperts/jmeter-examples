# jmeter-examples

The `Search Result Pagination` test will determine the total number of search result pages
for all search results in a repoistory and then loop through each search result page the
specifified number of times.

You can launch the test and capture repeated results from the command line using a
command something like this
```
USERS=1; LOOPS=1; jmeter -n -t Search\ Result\ Pagination\ Test.jmx  -l "./results/results-${USERS}x${LOOPS}.log" -j "./results/logfile-${USERS}x${LOOPS}.log" -e -o "./results/summary-${USERS}x${LOOPS}"  -Jloops_per_user=$LOOPS -Jusers=USERS`
```

Results will be saved to the `./results/` subdirectory which is git-ingored, so be sure to copy results
if you want to keep them permanently.