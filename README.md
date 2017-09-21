# code-your-own-quiz
# IPND Stage 2 Final Project


#questions.
easy_question = '''The name of the first day of the week is Sunday.
The name of the second day of the week is Monday.
The seventh day of the week is Saturday.
Finally, the sixth day of the week is Friday.'''

medium_question = '''The first month of the year is January.
The seventh month of the year is July.Fall starts in this month September.,
This month has the spring equinox March.'''

hard_question = '''There are 52 weeks in a year.
The answer to the universe and everything is 42.,
The legal voting age is 18. , There are 366 days in a leap year.'''

easy_answers = ("Sunday", "Monday", "Saturday", "Friday")
medium_answers = ("January", "July", "September", "March")
hard_answers = ("52", "42", "18", "366")


questions = [easy_question, medium_question, hard_question]
answers = [easy_answers, medium_answers, hard_answers]

#define difficulty level easy medium hard or error
def level_of_diff():
    print "Welcome to the game!"
    diff_level = raw_input("Would you like an easy, medium or hard level?")
    if diff_level == "easy":
        print "\nYou chose easy. You have 3 chances to answer correctly."
        return quiz_start(easy_question, easy_answers)
    elif diff_level == "medium":
        print "\nYou chose medium. You have 3 chances to answer correctly."
        return quiz_start(medium_question, medium_answers)
    elif diff_level == "hard":
        print "\nYou chose hard. You have 3 chances to answer correctly."
        return quiz_start(hard_question, hard_answers)
    else:
        print "\nTry again."
        return level_of_diff()
    
def answer_blank(word, answers):
        if blank in word:
            return blank
        return None
#quiz begins here
#def quiz_start(level_of_diff,answers):
#    replaced = []
 #   count = 0
#    attempt = 1
#    last_attempt = 3
 #   """while user_input != answers:
  #          print "Incorrect"
 #           if last_attempt == 3:
 #           print "you are out of chances."""
       
def play_game(diff_level, blank):    
    replaced = []
    diff_level = diff_level.split()
    for word in diff_level:
        replacement = answer(word, answers)
        if replacement != None:
            user_input = raw_input("What is yor answer?: " + replacement + " ")
            word = word.replace(replacement, user_input)
            replaced.append(word)
        else:
            replaced.append(word)
    replaced = " ".join(replaced)
    return replaced
 



#print play_game()

   
if __name__ == "__play_game__":
	play_game()

