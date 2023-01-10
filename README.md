# aleo-worker
Our linux version of aleo worker has high performance with GPU, which can start proving easily and seamlessly with user's Aleo wallet address.

🏅  Performance:

| GPU | Result |
| :---: | :---: |
| 3090 | 4000 c/s + |
| 3080 | 3500 c/s + |
| 2080Ti | 2550 c/s + |

### How to run?
```
 nohup ./aleo-worker -g 0 -a aleoXXX >> ./worker.log 2>&1 &
 nohup ./aleo-worker -g 0,1 -a aleoXXX >> ./worker.log 2>&1 &
 nohup ./aleo-worker -g 0,1,2,3 -a aleoXXX >> ./worker.log 2>&1 &
```
-g: gpu card index, start from 0

-a: aleo wallet address

N.B. Please replace 'aleoXXX' with your aleo wallet address.

### How to check performance?
```
tail -f ./worker.log
```

it will output as following:
```
2023-01-01T15:31:22.659037Z  INFO 726242 1m: 2371.67 c/s
2023-01-01T15:32:22.696614Z  INFO 726242 1m: 2373.32 c/s
2023-01-01T15:33:22.800096Z  INFO 726242 1m: 2376.30 c/s
```
2371.67 c/s means 2371.67 commitments per second during 1 minute.

### How to check the account benefit?
```
https://www.aleo.network/leaderboard
https://www.aleo.network/leaderboard/aleoXXX
```

N.B. Please replace 'aleoXXX' with your aleo wallet address.
