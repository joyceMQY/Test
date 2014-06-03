CS6300 Summer 14 Assignment 2

Important: Please make sure that there is no blank in your path.

To use the script testCalculator.sh, please perform the following steps:
  1. Open the terminal and cd into your working directory.
  2. Put testCalculator.sh and 6300Sum14Assignment2-grading project in your working directory.
  3. Check the package names (both under src and test) of the student's solution. If the names are gatech.cs6300.assignment2 then use 2 as the third argument; else if the names are gatech.cs6300.assignment1 then use 1 as the third argument; else the package name is incorrect.
  4. Do not modify MANIFEST.MF under META-INF folder in 6300Sum14Assignment2-grading unless the Main-Class and Class-Path info should be changed.
  5. Run testCalculator.sh using command "./testCalculator.sh \<gt_userid\> \<path_of_student_repo\> \<number_1_or_2\>". The first argument is the student's gt userid, the second one is the path of the student's repo after you pull it from GitHub, and the third argument is the number of assignment used in the package name(ie., gatech.cs6300.assignment2 is 2). 
  6. An example command is "<b>./testCalculator.sh ao44 E:/CS6300Sum14ao44 2</b>"
  7. Result will be shown on the terminal: "true" means tests passed, otherwise the failure info appears.
