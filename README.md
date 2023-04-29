## Rate Limiter Program

This program implements a rate limiter using a sliding window. It receives a sequence of timestamps as input and outputs whether each request is allowed or blocked based on the sliding window configuration.

### Building and Running the Program

The program is written in Python 3 and can be run from the command line using the following command:

```
$ python ratelimiter.py R S ts1 ts2 ts3 ...
```

where:
- `R` is the maximum number of requests allowed in the sliding window
- `S` is the sliding window time period in seconds
- `ts1`, `ts2`, `ts3`, ... are the sequence of timestamps in ascending order

For example, to run the program with a sliding window of 2 requests in the previous 5 seconds and the following sequence of timestamps:

```
1, 2, 4, 5, 6, 7, 8, 9
```

You can run the following command:

```
$ python ratelimiter.py 2 5 1 2 4 5 6 7 8 9
```

### Runtime Environment

The program was developed using Python 3.8.8 running on Windows 11.

### Sample Input and Output

Here's an example of the input and output of the program:

**Input 1:**

```
$ python ratelimiter.py 2 5 1 2 4 5 6 7 8 9
```

**Output 1:**

```
1 allowed
2 allowed
4 blocked
5 blocked
6 blocked
7 allowed
8 allowed
9 blocked
```

![image](https://user-images.githubusercontent.com/70798723/234883667-85484e8c-5781-4429-8b23-5f3203fa54e4.png)

**Input 2:**

```
$ python aqfer.py 2 5 1628679347 1628679348 1628679350 1628679351 1628679352 1628679353 1628679354 1628679355
```

**Output 2:**

```
1628679347 allowed
1628679348 allowed
1628679350 blocked
1628679351 blocked
1628679352 blocked
1628679353 allowed
1628679354 allowed
1628679355 blocked
```
![image](https://user-images.githubusercontent.com/70798723/235289055-46634a99-c173-46ba-b1ee-0af2c329f9b2.png)


