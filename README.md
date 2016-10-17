# online-quiz-system
An online quiz system built on PHP, JS and HTML. It has inbuilt Timer support along with Admin Panel

This project is a great improvement of 'Online-Exam-System-' created by Sunny Prakash Tiwari (https://github.com/sunnygkp10). Since it was licensed under MIT so I think I have rights to improve and re-distribute it. I have again licensed it under MIT. You are free to modify and re-distribute

#Added features: 

1. Added Timer support.
2. Added control to "Enable" and "Disable" the quiz on the Admin panel
3. Added control to navigate among all the questions of quiz (during the quiz) and finish the quiz whenever the user wants.
4. Added control so that user can start the quiz at any time and continue the quiz even if some error or session timeout occurs.
5. Added control to store the answers to question and show a detailed analysis of the quiz results.
6. Improved GUI of the quiz panel.

#Setup:

1. Create a new database in MySQL.
2. Run the SQL query in "quizzer.sql".
3. Open the file "dbConnection.php" and change the Server name, Username, Password and Database name.
3. Visit the home page in browser. Use the "Admin Login" link to login to Admin Panel. Default user - 'sonudoo' pass - '1234567890'

#How to Use

1. Use the Admin Panel to set up quiz. Quiz won't be enabled unless you click the "Enable" button. Click on the same to enable an added quiz.
2. Scores are updated realtime on the server, however the leaderboard will be updated only when the user finishes the quiz, or there is a time out or the admin ends the quiz by clicking on "Disable" button.
3. Once the admin clicks on the disable button, the quiz ends for all the users taking that quiz, irrespective of their active or inactive state (whether logged in or left the quiz in the middle only). The leaderboard will be updated either when a user "Finishes" his /her quiz and when the admin "disables" the quiz. 
4. Once the quiz is disabled, the quiz becomes inaccessible. If the quiz is enabled again later, only those user who have not already taken the quiz can take the quiz.
5. It is recommended that you Enable the quiz when all the users are ready and disable the quiz when all the users have completed the quiz or time limit of taking the quiz has exceeded.

#Bugs:

1. Too many SQL queries, needs optimization. Yet not suitable for more than 200 simultaneous user.
2. Security issues, need to sanitize the URL queries.
