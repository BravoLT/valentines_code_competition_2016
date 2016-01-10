# The 2016 Valentines Day Code Challenge - BravoLT
<img src="http://previews.123rf.com/images/sararoom/sararoom1209/sararoom120900080/15524932-illustration-of-cute-Cupid--Stock-Vector-cartoon-cupid-angel.jpg" width="200px" align="left">Cupid needs your help! He has a lot of Valentine's Day cards to deliver all over the world and the logistics are just a little too much for this little cherub. Use your genius to help this cute little baby out by giving the shortest routes to deliver all of his cards!
<br><br><br>
## Summary
You will need to write some software that takes a file and any number of city names. Your software will be called via a script `run.sh`. If preparation (compilation or other steps) are necessary, you should prepare a script `prepare.sh`. You can write the application in any language you want. The only caveats are below.

1. Any special instructions should be include in a file `INSTALL.md`. These instructions should include any special tasks or environmental concerns Santa's DevOps team needs to know about to get your application running.
1. Special instructions should be reasonable to get your application running on a Mac running Yosemite with Homebrew.
1. Your application should output as described in the *Details* section
1. Your application cannot use licensed software or any other proprietary software that is not available to other participants or to those who will be assessing your effort.

The details for accomplishing this task are below.

## Details
First place will win a Chromecast, and second place will win a Chromecast Audio. Challenge ends on Valentines Day 2016. Below are the details you will need to accomplish your task.

### Prepare Script
You will need to create a script `prepare.sh` if your application requires compiling or any other preparation. If this script is not present, we will assume that `run.sh` should complete without any intervention.

### Run Script
You will need to write a script that is responsible for running your application. This script will perform all the necessary task involved in running your application. This includes building and running (or anything else you might need to do).

```
run.sh <file> <city1> <city2> <city3> ... <cityN>
```

### Input File
The input file will have the format as shown below.

#### Format
```
<city1>,<city2>,<distance1>
<city1>,<city3>,<distance2>
...
<cityN>,<cityN+1>,<distanceN>
```

#### Example
```
valentine city,wortham,169
wortham,pumpkintown,7
pumpkintown,rusk,67
wortham,milnor,137
milnor,mongle spring,127
wortham,north greenfield,131
north greenfield,litchfield,153
wortham,carloss,170
carloss,northridge,189
wortham,clifty,60
clifty,thompson,82
pumpkintown,milnor,4
pumpkintown,north greenfield,65
```



### Output
The output of your application should be the name of each stop on your route in the order in which Cupid should visit them. Of course, Valentine City should be the first line of every file you output.

#### Format
```
valentine city
<city1>
<city2>
<city3>
...
<cityN>
```

#### Example
```
valentine city
wortham
milnor
clifty
```

You may visit any city (so long as that city is reachable from the previous one) as many times as you like. You may _not_ stay in the same city. Doing so will disqualify your results.

## Development and Testing
A couple of files are available to make development and testing easier. These files describe the set of cities, connections and distances.

1. `test1.txt`
1. `test2.txt`

## Submissions
1. Clone the repository
1. Create a branch (`git co -b <mybranch>`)
1. Push your branch
1. Create a pull request to *master*
1. Wait for the results

## Winning
In order to win the competition, your application must choose the shortest route for Santa to take in order to make all the stops specified by the input (i.e. the correct answer). The winner will be the application that gets the correct answer (accross multiple inputs) and runs with the shortest time (mean application runtime over the inputs).

## Question or Problems
If you should have questions or problems, please, email [Dustin Clifford](mailto:dustin.clifford@bravolt.com "Dustin Clifford") or [Mike Nishizawa](mailto:michael@fortitude-solutions.com "Mike Nishizawa").

Should there be questions or changes necessary to this document, there will be an updates section at the top of this document on the *master* branch.
