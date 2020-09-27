# Election Analysis

## Project Overview
The goal of this work was to audit a fictional, local congressional election. The raw data was received in a .csv file and contained the ballot ID, county, and chosen candidate.

In order to determine the election results the following objectives were required:
1. Calculate total votes.
2. Obtain a list of candidates that received votes.
3. List the counties originating the votes.
4. Total number of votes each candidate received.
5. Total number of votes from each county.
6. Percentage of votes for each candidate.
7. Determine the county with the largest turnout.
5. Determine the winner of the election based on popular vote.

## Resources
Data Source: election_results.csv
Software: Python 3.7.6, Visual Studio Code 1.49

## Results

The analysis of the data show that:
(Result numbering matches obcejtive number above)

1. There were 369,711 votes cast in the election.

2. The candidates that received votes were:
    Charles Casper Stockham
    Diana DeGette
    Raymon Anthony Doane
    
3. The counties from which these votes originated were:
    Jefferson
    Denver
    Arapahoe
  
4. The candidate results (% of vote, number of votes):
    Charles Casper Stockham: 23.0% (85,213)
    Diana DeGette: 73.8% (272,892)
    Raymon Anthony Doane: 3.1% (11,606)

5. Total votes from each county(% of total votes, number of votes from county):
    Jefferson: 10.5% (38,855)
    Denver: 82.8% (306,055)
    Arapahoe: 6.7% (24,801)
    
6. The county with the largest turnout was: 
    Denver
  
7. The winner of the election was:
    Diana DeGette with 73.8% of the vote and 272,892 votes
    
## Summary
This script can be similarly used for any election providing the raw data formatting matches. Note that this script fixes the candidate name as diplayed in the third column of the raw data file (line 49). 

`candidate_name = row[2]`

If election results are differently formatted then this line of code will have to be changed accordingly. Similarly, Line 52 pulls the county name from the second column in the raw data, changes in the raw data will need to be reflected in this line of code. 

`county_name = row[1]`

This script is designed to work with a .csv formatted input file .xls files will not result in successful running of this script. The winners in this election are determined by number of votes and percentage of vote (line 100 and line 128).

`turnout_percentage = float(turnout)/float(total_votes)*100`

`vote_percentage = float(votes) / float(total_votes) * 100`

If using a different methodology for determing winners, these lines of code need to be adjusted accordingly. 
