# Resultados de testing:

## Test 1

@ubuntu-cadhu:~$ ab -n 10000 -c 5 -C "somecookie=rawr" http://159.89.229.54/
This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 159.89.229.54 (be patient)
Completed 1000 requests
Completed 2000 requests
Completed 3000 requests
Completed 4000 requests
Completed 5000 requests
Completed 6000 requests
Completed 7000 requests
Completed 8000 requests
Completed 9000 requests
Completed 10000 requests
Finished 10000 requests


Server Software:        nginx/1.10.3
Server Hostname:        159.89.229.54
Server Port:            80

Document Path:          /
Document Length:        612 bytes

Concurrency Level:      5
Time taken for tests:   1.302 seconds
Complete requests:      10000
Failed requests:        0
Total transferred:      8540000 bytes
HTML transferred:       6120000 bytes
Requests per second:    7683.08 [#/sec] (mean)
Time per request:       0.651 [ms] (mean)
Time per request:       0.130 [ms] (mean, across all concurrent requests)
Transfer rate:          6407.57 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.1      0       1
Processing:     0    1   0.2      0       2
Waiting:        0    0   0.2      0       2
Total:          0    1   0.1      1       2
ERROR: The median and mean for the processing time are more than twice the standard
       deviation apart. These results are NOT reliable.

Percentage of the requests served within a certain time (ms)
  50%      1
  66%      1
  75%      1
  80%      1
  90%      1
  95%      1
  98%      1
  99%      1
 100%      2 (longest request)
 
 
 
## Test 2

@ubuntu-cadhu:~$ ab -kc 10 -t 30 http://159.89.229.54/
This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 159.89.229.54 (be patient)
Completed 5000 requests
Completed 10000 requests
Completed 15000 requests
Completed 20000 requests
Completed 25000 requests
Completed 30000 requests
Completed 35000 requests
Completed 40000 requests
Completed 45000 requests
Completed 50000 requests
Finished 50000 requests


Server Software:        nginx/1.10.3
Server Hostname:        159.89.229.54
Server Port:            80

Document Path:          /
Document Length:        612 bytes

Concurrency Level:      10
Time taken for tests:   3.261 seconds
Complete requests:      50000
Failed requests:        0
Keep-Alive requests:    49501
Total transferred:      42947505 bytes
HTML transferred:       30600000 bytes
Requests per second:    15331.17 [#/sec] (mean)
Time per request:       0.652 [ms] (mean)
Time per request:       0.065 [ms] (mean, across all concurrent requests)
Transfer rate:          12860.07 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.0      0       1
Processing:     0    1   5.8      0      67
Waiting:        0    1   5.8      0      67
Total:          0    1   5.8      0      68

Percentage of the requests served within a certain time (ms)
  50%      0
  66%      0
  75%      0
  80%      0
  90%      0
  95%      0
  98%      1
  99%      3
 100%     68 (longest request)
