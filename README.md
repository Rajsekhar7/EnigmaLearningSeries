# EnigmaLearningSeries
L1=int(1)
L2=int(1)
R1=int(1)
R2=int(1)
print("Current Status :")
print("Player 1 -",L1," ",R1)
print("Player 2 -",L2," ",R2)
while ((L1 != 0 or R1 !=0) and (L2 !=0 or R2 !=0)):
	p1= input("Enter move for Player 1 - ")
	if (p1=="A") :
		m1=input("Enter the move combination- ")
		if (m1=="L R"):
			R2=L1+R2
		elif (m1=="R L"):
			L2=R1+L2
		elif (m1=="L L"):
			L2=L2+L1
		elif (m1=="R R"):
			R2=R2+R1
		else:
			print("Invalid")
	if (p1=="S") :
		m1=input("Enter the move combination - ")
		if (m1=="L") :
			if(L1==1):
				print("Invalid")
			else :
				s1=int(input())
				s2=int(input())
				if(s1+s2==L1):
					L1=s1
					R1=s2
				else:
					print("Invalid")
		elif(m1=="R"):
			if(R1==1):
				print("Invalid")
			else :
				s1=int(input())
				s2=int(input())
				if(s1+s2==R1):
					L1=s1
					R1=s2
				else:
					print("Invalid")
	if(L2==5):
		L2=int(0)
	elif(R2==5):
		R2=int(0)
	print("Current Status :")
	print("Player 1 -",L1," ",R1)
	print("Player 2 -",L2," ",R2)
	p2= input("Enter move for Player 2 - ")
	if (p2=="A") :
		m2=input("Enter the move combination- ")
		if (m2=="L R"):
			R1=L2+R1
		elif (m2=="R L"):
			L1=R2+L1
		elif (m2=="L L"):
			L1=L2+L1
		elif (m2=="R R"):
			R1=R2+R1
		else:
			print("Invalid")
	if (p2=="S") :
		m2=input("Enter the move combination - ")
		if (m2=="L") :
			if(L2==1):
				print("Invalid")
			else :
				s3=int(input())
				s4=int(input())
				if(s3+s4==L2):
					L2=s3
					R2=s4
				else:
					print("Invalid")
		elif(m2=="R"):
			if(R2==1):
				print("Invalid")
			else :
				s3=int(input())
				s4=int(input())
				if(s3+s4==R2):
					L2=s3
					R2=s4
				else:
					print("Invalid")
	if(L2==5):
		L2=int(0)
	elif(R2==5):
		R2=int(0)
	print("Current Status :")
	print("Player 1 -",L1," ",R1)
	print("Player 2 -",L2," ",R2)
if (L1 == 0 or R1 ==0):
	print("Player 1 lost the game ! Player 2 is the winner")
elif (L2 == 0 or R2 ==0):
	print("Player 2 lost the game ! Player 1 is the winner")

