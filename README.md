# MafiaHelp
Help pls , if players >= 13 my code input to much Peace roles. idk what i can do fro this dont happend , u are have ideas?

import random
from random import randint
import time


players = int(input("Введите кол-во игроков : "))
mafia = int(input("Введите кол-во мафии : "))
roles = []
roles.append("Doctor")
roles.append("Sheriff")
if players >= 12 :
    roles.append("Putana")
if players >=13 :
	for i in range(1):
		roles.append("Friend "  + str(random.randint(2,2)))
	for i in range(1):
		roles.append("Friend "  + str(random.randint(1,1)))
if players >=13 :
	for i in range(players-5-mafia):
		roles.append("Peace")
if players == 12:
	for i in range(players-2-mafia):
		roles.append("Peace")
if players < 12:
	for i in range(players - 3 - mafia):
		roles.append("Peace")
	
if mafia >= 3 :
	mafia = mafia - 1
	for i in range(1):
		roles.append("Don")
for i in range(mafia):
	roles.append("mafia")
random.shuffle(roles)
for i in range(len(roles)):
	print("Player " + str(i+1) + " - ", roles[i] )
