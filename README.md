# voting-program-in-python
nominee1 = input ("Enter the name of 1st nominee:")
nominee2 = input ("Enter the name of 2nd nominee:")

# initially vote count for both must be 

nm1_votes = 0 
nm2_votes = 0
voter_id = [ 1,2,3,4,5,6,7,8,9,10 ]
no_of_voter = len(voter_id)

while True:
    if voter_id == []:  # To check when voter list is completed
       print ("voting session is over!!!")
       if nm1_votes>nm2_votes:
            percent= (nm1_votes/no_of_voter)*100   #To calculate the percent
            print (nominee1,"has won the election with",percent," % of votes ")
       break     #To get rid of infinite loop
    elif (nm2_votes>nm1_votes):
        percent = (nm2_votes/no_of_voter)*100
        print (nominee2,"has won the election with",percent," % of votes")
        break
else:
    print ("both have equal number of votes !!!! Government will declared who will rule")
    

voter = int(input("Enter your voter id:"))
if voter in voter_id:
 print ("you are a voter")
 voter_id.remove(voter)   # We Will remove so that again same voter can't vote
 print ("______")
 print ("To give vote to",nominee1,"press1")
 print ("To give vote to",nominee2,"press2")
 print ("______")

vote = int (input("Enter your precious vote:"))
if vote ==1:
    nm1_votes +=1
    print (nominee1,"Thanks you to give your important vote to them!!")
elif vote ==2:
    nm2_votes +=1
    print (nominee2,"Thanks you to give your important vote to them!!")
elif vote>2:
    print ("check your pressed key!!")
else:
    print ("you are not a voter OR you have already voted")

#End the code
