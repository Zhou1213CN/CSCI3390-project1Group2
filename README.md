*HW Group 2 Zehua Zhang, Zheng Zhou*

*CSCI3390-Project1*

## Question 1

#### a. k = 2 :

xS = 1098872048this_is_a_bitcoin_block_of_66118645_and_25117738

number of trials = 300

Hash value = 002c2284b1b0807a299864473e9b637711fe1384e84b3356a98baf6f7aab4776)

Time elapsed = 9s

#### b. k=3 

xS = 2039064391this_is_a_bitcoin_block_of_66118645_and_25117738

number of trials = 1000

Hash value = 000be26daeb62dd0834b80b0a17303597a41891a0f32fef0019ef177f3053bc5)

Time elapsed = 9s

#### c. k = 4 

xS = 715024134this_is_a_bitcoin_block_of_66118645_and_25117738

number of trials = 70000

Hash value = 0000298cb454a28c175e196b8ac313d73ddcb8270f8165f0d804e009bcf6b6c5

Time elapsed = 10s

#### d. k = 5

xS = 1618493004this_is_a_bitcoin_block_of_66118645_and_25117738

number of trials = 1000000

Hash value = 000007da5bf379d338f7ca5fd4476fde8ecb5582f00c8e6e5b13ad71a6a62b72

Time elapsed = 15s

#### e. k = 6

xS = 1495472627this_is_a_bitcoin_block_of_66118645_and_25117738

number of trials = 5000000

Hash value = 0000005d02352f4927c59d090272e8cfccbdf989d4c378c3acaa7b1642a20a98

Time elapsed = 31s



## Question 2

k = 7

xS = 1749757147this_is_a_bitcoin_block_of_66118645_and_25117738

Hash value = 0000000e401e631dabe5b5e7131350ffa44f7a9a786c73f0203d4cf83a2965ec

number of trials = 200,000,000

Time elapsed = 790s

Machine type： n1-standard-4

A easy way to estimate the number of trials to have 7 leading zeroes in a SHA256 ouput would be::

1.If we are getting 0000000fffffffffffffffffffffffffffffffffffffffffffffffffffffffff,
we could get it divided by ffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff, the maximum value of a 256-bit number. 

2.So if we are going to hit the 256 bit number with one trial, the probability that we are getting 7 zeroes in a row will be $\frac{1}{16^{7}}$ We can then get the trials number that are required by $16^{7}$, which is 268,435,477 which is approximately 2 and a half billion times of trial. 



## Question 3

```scala
//Original Line
iter.map(x => rand.nextInt(Int.MaxValue - 1) + 1)

//Revised Line
iter.map(x => rand.nextInt(trials) + 1)

```

