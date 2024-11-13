Program: Airline Upgrade System

- Describe an algorithm for the New Unknown Airline (NUA) Upgrade System.
- Develop a program that processes the request and cancellations for upgrade and provides the list of k-highest priority flyers among the n frequent flyers on the waiting list.
- Your implementation must process the request and cancellations in O(logn) time and find the k-highest-priority flyers in O(k logn) times using the data structures in Chapter 5.

Below are the Input and Output formats. In addition, few test cases are included and the code should run against those. 

Input:

n = Number of flyers in waiting list
k = Required K highest priority flyers
c = Number of cancellation requests

Now n lines followed with flyers information like, flyer_name, flyer _id, the time that flyer came into waiting list (request time) and the Status given to that flyer. So priority will be calculated as the combination of time and Status. The priority is determined FIRST by status, then request time in the waiting list, if there are tie in status, request times break the ties

For the simplicity time will be an integer ranging from 1 to 100000. And Status will be any from the following list [Super, Platinum, Gold, Silver], where
Super > Platinum > Gold > Silver.

Now 'c' lines followed with flyer's id who raised the cancellation request.

Example Input-1
-----------------------------
5 2 1 (n k c)

A 1 120 Platinum (flyer_name, flyer_id, time, status)
B 5 60 Super
C 3 140 Super
D 2 130 Gold
E 4 150 Silver

5 (flyer id who raised the cancellation request)

Example Input-2
--------------------------
4 1 2 (n k c)

A 1 30 Platinum (flyer_name, flyer_id, time, status)
B 2 60 Gold
C 3 90 Silver
D 4 120 Super

2 (flyer_id who raised the cancellation request)
4 (flyer_id who raised the cancellation request)

Output:
--------------------------
Output should be top K flyers based on priority, who are allowed to onboard.

Example Output-1
--------------------------
(C, 3, 140, Super)
(A, 1, 120, Platinum)
