# Python Quiz Game

## Overview

This is a Quiz Game project developed in Python, designed to test players' knowledge on various topics such as history, geography, and science. It's a beginner-friendly project, ideal for those who want to learn and practice basic programming concepts in Python.

## Features

- **User-Friendly Interface:** The game boasts a simple and intuitive interface, making it easy for players to engage.

- **Diverse Topics:** The quiz covers a range of subjects, including history, geography, science, and more.

- **Scoring System:** Players receive a score at the end of the game, encouraging multiple plays for score improvement.

- **Educational:** The project serves as a learning tool, with well-commented code that is easy to understand.

- **Customizable:** The code is open for modification, allowing users to add new questions, topics, or features.

- **Database Logging:** Correctly answered questions are logged in a file named `Quiz_game.log`, providing a record of player performance.

## How to Play

1. *Start the Game:* Run the Python script to initiate the quiz.

2. *Answer Questions:* Respond to a series of questions by choosing the correct option.

3. *View Score:* Your score is displayed at the end of the game.

4. *Database Logging:* If all questions are answered correctly, the player's performance is logged in `Quiz_game.log`.

5. *Play Again:* The game can be played multiple times for continued learning and score improvement.

## Usage

Feel free to download, use, and modify the code to suit your needs. The well-commented nature of the code makes it an excellent resource for learning and experimentation.

## Happy Coding!

Whether you're a beginner honing your Python skills or an experienced coder looking for a fun project, this Quiz Game is an enjoyable and educational choice. Have fun coding and learning!

*Note:* Ensure you have Python installed to run this project.

*Author:* Jai Prakash.R

**License:** This project is open-source and can be used and modified freely.





## Installation

Install package with pip

```bash
  pip install logging

```
    
## Deployment

To deploy this project run

```bash
import time
import logging

logging.basicConfig(filename = "Quiz_game.log", level = logging.DEBUG, format = ("%(asctime)s %(levelname)s %(message)s"))

 
def sleep_time():
    print("Loading your Question Paper", end="")
    a = 0
    while a<100:
        print(".", end="")
        time.sleep(0.05)
        a+=1
    return " "
try:
    ok = 0
    ng = 0
    wrong = []

    ans = input("Are you ready to play Quiz Game? ").lower()

    if ans != "yes":
        print("Thank You")
        logging.info("user aren't ready to play Quiz Game")
        pass
    else:
        logging.info("user ready to play")
        name_list = []
        name = input("Please Give Your Name: ")
        logging.info("user name is: %s", name)
        name_list.append(name)
        mobile = input("Please Give Your Mobile Number: ")
        logging.info("user mobile number is: %s", mobile)
        name_list.append(mobile)
        age = input("please Give Your Date of Birth: like dd/mm/yy ")
        logging.info("user birth day date is: %s", age)
        name_list.append(age)

        print("\n" + "="*57 + " Thank You " + "="*57)

        print(f"""
    Your Name is:          {name_list[0]}
    Your Mobile Number is: {name_list[1]}
    Your Date of Birth is: {name_list[2]}     
        """) 
        ask = input("is everything correct? ")

        if ask != "yes":
            print("please try again")
        else:
            print("Creating your Gaming ID ", end="")
            a = 0
            while a<102:
                print(".", end="")
                time.sleep(0.05)
                a+=1
            print ("\n\n" + f"Your Quiz Gaming ID is: {name_list[0][0] + name_list[1][1::2] + name_list[2][-4::1]}")
            
            user_id =  name_list[0][0] + name_list[1][1::2] + name_list[2][-4::1]
            
            logging.info("User Quiz Gaming ID is: %s", user_id)

            time.sleep(2)
            print("\n" + "="*53 + " Let's start the Game " + "="*52)

            print("""

    Please Select the Subject 🙂

    1. Science
    2. Robotics
    3. Movies and TV Shows
    4. Computer
    5. General Knowledge
                """)
            sub = input("please choose one: ").lower()
            
            logging.info("user choosed %s no subject", sub)

            if sub == "1" or sub == "science":
                    print("\n"+"="*47 + " Thank you for selected Science " + "="*47)
                    sleep_time()

    #Q1 for Science
                    q1 = input("""1. Which of the following is used in pencils?
    a) Graphite
    b) Silicon
    c) Charcoal
    d) Phosphorous
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "a" or q1 == "graphite":
                        ok += 1
                    else:
                        ng +=1
                        wrong.append(f"""1. Which of the following is used in pencils?
    a) Graphite
    b) Silicon
    c) Charcoal
    d) Phosphorous

    Correct ans is:- a)Graphite
    you gave: {q1}
    """)

    # Q2 for Science
                    q2 = input("""2. Chemical formula for water is
    a) NaAlO2
    b) H2O
    c) Al2O3
    d) CaSiO3
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "b" or q2 == "h20":
                        ok += 1
                    else:
                        ng += 1
                        wrong.append(f"""2. Chemical formula for water is
    a) NaAlO2
    b) H2O
    c) Al2O3
    d) CaSiO3

    Correct ans is:- b)H2O
    you gave: {q2}
    """)

    # Q3 for Science
                    q3 = input("""3. The gas usually filled in the electric bulb is
    a) Nitrogen
    b) Hydrogen
    c) Carbon Dioxide
    d) Oxygen
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "a" or q3 == "nitrogen":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. The gas usually filled in the electric bulb is
    a) Nitrogen
    b) Hydrogen
    c) Carbon Dioxide
    d) Oxygen

    Correct ans is:- a)Nitrogen
    you gave: {q3}
    """)

    # Q4 for Science
                    q4 = input("""4. Which of the gas is not known as green house gas?
    a) Methane
    b) Nitrous oxide
    c) Carbon dioxide
    d) Hydrogen         
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "d" or q4 == "hydrogen":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. Which of the gas is not known as green house gas?
    a) Methane
    b) Nitrous oxide
    c) Carbon dioxide
    d) Hydrogen         

    Correct ans is:- d)Hydrogen
    you gave: {q4}
    """)

    # Q5 for Science
                    q5 = input("""5. Which of the following is used as a lubricant?
    a) Graphite
    b) Silica
    c) Iron Oxide
    d) Diamond           
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "a" or q5 == "graphite":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. Which of the following is used as a lubricant?
    a) Graphite
    b) Silica
    c) Iron Oxide
    d) Diamond           

    Correct ans is:- a)Graphite
    you gave: {q5}
    """)
            elif sub == "2" or sub == "robotics":
                    print("\n" + "="*47 + " Thank you for selected Robotics " + "="*47)
                    sleep_time()

    #Q1 for robotics
                    q1 = input("""1. What is the full meaning of IR sensor?
    a) infrared
    b) infrared light
    c) international radio
    d) internet refollow
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "a" or q1 == "infrared":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. What is the full meaning of IR sensor?
    a) infrared
    b) infrared light
    c) international radio
    d) internet refollow

    Correct ans is:- a)infrared
    you gave: {q1}
    """)

    #Q2 for robotics
                    q2 = input("""2. What is the full meaning of PIR sensor?
    a) positive infrared
    b) point of infrared
    c) Passive infrared
    d) plus infrared 
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "passive infrared":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. What is the full meaning of PIR sensor?
    a) positive infrared
    b) point of infrared
    c) Passive infrared
    d) plus infrared 

    Correct ans is:- c)Passive infrared
    you gave: {q2}
    """)

    # Q3 for robotics
                    q3 = input("""3. What is the full meaning of RF?
    a) Radio frequency
    b) Radio free
    c) Radio fall
    d) Radio following
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "a" or q3 == "radio frequency":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. What is the full meaning of RF?
    a) Radio frequency
    b) Radio free
    c) Radio fall
    d) Radio following

    Correct ans is:- a)Radio frequency
    you gave: {q3}
    """)
    # Q4 for robotics
                    q4 = input("""4. What is the full meaning of AI?
    a) Artificial internet
    b) Artificial information
    c) Artificial interface
    d) Artificial intelligence
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "d" or q4 == "artificial intelligence":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. What is the full meaning of AI?
    a) Artificial internet
    b) Artificial information
    c) Artificial interface
    d) Artificial intelligence

    Correct ans is:- d)Artificial intelligence
    you gave: {q4}
    """)

    # Q5 for robotics
                    q5 = input("""5. what is the name of world best robot?
    a) Reco            
    b) Sophia
    c) Roba
    d) Seba
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "b" or q5 == "sophia":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. what is the name of world best robot?
    a) Reco            
    b) Sophia
    c) Roba
    d) Seba

    Correct ans is:- b)Sophia
    you gave: {q5}
    """)
            elif sub == "3" or sub == "Movies and TV shows":
                    print("\n" + "="*47 + " Thank you for selected Movies and TV shows " + "="*47)
                    sleep_time()

    #Q1 for Movies and TV shows
                    q1 = input("""1. Who played the lead role in the movie "The Shawshank Redemption"?
    a) Tom Hanks
    b) Morgan Freeman
    c) Tim Robbins
    d) Brad Pitt
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "c" or q1 == "Tim Robbins":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""Who played the lead role in the movie "The Shawshank Redemption"?
    a) Tom Hanks
    b) Morgan Freeman
    c) Tim Robbins
    d) Brad Pitt

    Correct ans is:- c) Tim Robbins
    you gave: {q1}
    """)

    #Q2 for Movies and TV shows
                    q2 = input("""2. In the TV series "Stranger Things," what is the name of the parallel dimension?
    a) The Underworld
    b) The Netherworld
    c) The Upside Down
    d) The Other Side
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "The Upside Down":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. In the TV series "Stranger Things," what is the name of the parallel dimension?
    a) The Underworld
    b) The Netherworld
    c) The Upside Down
    d) The Other Side

    Correct ans is:- c)The Upside Down
    you gave: {q2}
    """)

    #Q3 for Movies and TV shows
                    q3 = input("""33. Which film won the Academy Award for Best Picture in 2020?
    a) Joker
    b) Parasite
    c) 1917
    d) La La Land
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "b" or q3 == "Parasite":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. Which film won the Academy Award for Best Picture in 2020?
    a) Joker
    b) Parasite
    c) 1917
    d) La La Land

    Correct ans is:- b)Parasite
    you gave: {q3}
    """)

    #Q4 for Movies and TV shows
                    q4 = input("""4.  What is the iconic catchphrase of Arnold Schwarzenegger's character in the movie "The Terminator"?
    a) I'll be back
    b) Say hello to my little friend
    c) Hasta la vista, baby
    d) May the Force be with you
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "a" or q4 == "I'll be back":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4.  What is the iconic catchphrase of Arnold Schwarzenegger's character in the movie "The Terminator"?
    a) I'll be back
    b) Say hello to my little friend
    c) Hasta la vista, baby
    d) May the Force be with you

    Correct ans is:- a) I'll be back
    you gave: {q4}
    """)

    #Q5 for Movies and TV shows
                    q5 = input("""5. Which TV series features characters known as Walter White and Jesse Pinkman?
    a) Breaking Bad
    b) The Sopranos
    c) Game of Thrones
    d) The Wire
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "a" or q5 == "Breaking Bad":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. Which TV series features characters known as Walter White and Jesse Pinkman?
    a) Breaking Bad
    b) The Sopranos
    c) Game of Thrones
    d) The Wire

    Correct ans is:- a)Breaking Bad
    you gave: {q5}
    """)
            elif sub == "4" or sub == "computer":
                    print("\n" + "="*47 + " Thank you for selected Computer " + "="*47)
                    sleep_time()

    #Q1 for computer
                    q1 = input("""1. When was the first computer invented?
    a) 1945
    b) 1943
    c) 1918
    d) 1937
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "b" or q1 == "1943":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. When was the first computer invented?
    a) 1945
    b) 1943
    c) 1918
    d) 1937

    Correct ans is:- b)1943
    you gave: {q1}
    """)


    #Q2 for computer
                    q2 = input("""2. What was the name of the first computer invented?
    a) ENIAC
    b) ENI
    c) ENCIA
    d) ENICA
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "a" or q2 == "eniac":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. What was the name of the first computer invented?
    a) ENIAC
    b) ENI
    c) ENCIA
    d) ENICA

    Correct ans is:- a)ENIAC
    you gave: {q2}
    """)

    #Q3 for computer
                    q3 = input("""3. Who is known as the father of computers?
    a) Pascal
    b) Hollerith
    c) Newman
    d) Charles Babbage
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "d" or q3 == "charles babbage":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. Who is known as the father of computers?
    a) Pascal
    b) Hollerith
    c) Newman
    d) Charles Babbage

    Correct ans is:- d)Charles Babbage
    you gave: {q3}
    """)

    #Q4 for computer
                    q4 = input("""4. When was the first 1 GB disk drive released in the world?
    a) 1980
    b) 1970
    c) 1981
    d) 1971
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "a" or q4 == "1980":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. When was the first 1 GB disk drive released in the world?
    a) 1980
    b) 1970
    c) 1981
    d) 1971

    Correct ans is:- a)1980
    you gave: {q4}
    """)

    #Q5 for computer
                    q5 = input("""5. What was the name of the first computer programmer?
    a) Alan Turing
    b) Ada Lovelace
    c) Tim Berners - Lee
    d) Steve Wozniak
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "b" or q5 == "ada lovelace":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. What was the name of the first computer programmer?
    a) Alan Turing
    b) Ada Lovelace
    c) Tim Berners - Lee
    d) Steve Wozniak

    Correct ans is:- b)Ada Lovelace
    you gave: {q5}
    """)
            elif sub == "5" or sub == "General Knowledge":
                    print("\n" + "="*47 + " Thank you for selected General Knowledge " + "="*47)
                    sleep_time()

    #Q1 for GK
                    q1 = input("""1. What is the capital city of Australia?
    a) Sydney
    b) Melbourne
    c) Canberra
    d) Brisbane
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "c" or q1 == "Canberra":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. What is the capital city of Australia?
    a) Sydney
    b) Melbourne
    c) Canberra
    d) Brisbane

    Correct ans is:- c)Canberra
    you gave: {q1}
    """)

    #Q2 for GK
                    q2 = input("""2. When was the first World Cup?
    a) 1926
    b) 1928
    c) 1930
    d) 1932
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "1930":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. When was the first World Cup?
    a) 1926
    b) 1928
    c) 1930
    d) 1932

    Correct ans is:- c)1930
    you gave: {q2}
    """)

    #Q3 for GK
                    q3 = input("""3.  What is the largest planet in our solar system?
    a) Venus
    b) Jupiter
    c) Saturn
    d) Mars
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "b" or q3 == "Jupiter":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3.  What is the largest planet in our solar system?
    a) Venus
    b) Jupiter
    c) Saturn
    d) Mars


    Correct ans is:- b)Jupiter
    you gave: {q3}
    """)

    #Q4 for GK
                    q4 = input("""4.  Who wrote the play "Romeo and Juliet"?
    a) Charles Dickens
    b) William Shakespeare
    c) Jane Austen
    d) Mark Twain
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "b" or q4 == "William Shakespeare":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4.  Who wrote the play "Romeo and Juliet"?
    a) Charles Dickens
    b) William Shakespeare
    c) Jane Austen
    d) Mark Twain

    Correct ans is:- b)William Shakespeare
    you gave: {q4}
    """)

    #Q5 for GK
                    q5 = input("""5. What is the currency of Japan?**
    a) Won
    b) Yuan
    c) Yen
    d) Ringgit
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "c" or q5 == "Yen":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. What is the currency of Japan?**
    a) Won
    b) Yuan
    c) Yen
    d) Ringgit

    Correct ans is:- c) Yen
    you gave: {q5}
    """)
            else:
                    print("you are selected the wrong subject, please try again")
                    logging.info("user are selected wrong subject")

            if sub == "1" or sub == "2" or sub == "3" or sub == "4" or sub == "5":
                result_ok = int((ok/5)*100)
                result_ng = int((ng/5)*100)
                if result_ok == 100:
                    print ("\nCongratulations 😍")
                    print(f"you gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                elif result_ok > 50 and result_ok <100:
                    print ("\nCongratulations 🙂")
                    print(f"you gave {result_ok} % correct answers & {result_ng} % wrong answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ng} % wrong answers")
                else:
                    print("\n 😟😟😟")
                    print(f"you gave {result_ok} % correct answers & {result_ng} % wrong answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ng} % wrong answers")

                if len(wrong) != 0:

                    ask1 = input("are you want to see which question you gave the wrong answer to? ")
                    if ask1 != "yes":
                        logging.info("user aren't want to see worng answers")
                        pass
                    else:
                        logging.info("user want to see wrong answers")
                        for i in wrong:
                            print(i)
                            logging.info("%s",i)
                else:
                    print("🙂🙂🙂")

                    
except Exception as e:
    print(e)
    logging.error("Error is happend")
    logging.exception("error is %s",e)          
```


## You can ask me any questions about this project contact me at:

mail-id:- jaiprakash292033@gmail.com

Linkedin:- https://www.linkedin.com/in/jai-prakash-ramesh/

instagram:- https://www.instagram.com/jaiprakash._.official/

If you have any confusion, please feel free to contact me. Thank you.

