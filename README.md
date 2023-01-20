# Implement the code verification on the subsystem, using the RTC RAM

**project goal:**

implement the code verification on the subsystem, using the RTC RAM


1. The system admin will enter a numeric 4-to-8-digit code 

2. Will convert it to an integer and will save it into the  RTC RAM under the known address  


3. The user will enter the secret code

4. The system will get the code from the user convert it to an integer and compare it to the saved code

    • If the code is correct the blue LED will switch on

    • If the code is incorrect the buzzer will make a short beep

5. The system will count invalid code inputs
  
    • After 3 invalid tries the red LED will switch on and will prevent the user from getting more codes for 30 seconds
  
    • After 30 seconds the red LED will switch and will reset the counter
   
    • The valid code also resets the counter

6. The system will store the number of invalid code inputs in the RTC RAM


**On power off the system:**

  * This counter remains even if the user disconnects the board
 
**After 9 invalid successive tries the system will:**
       
  ◦ The red LED will switch on
       
  ◦ The system will save the current time in the RTC RAM
       
  ◦ Will prevent the user to enter the codes for 5 minutes
 
 

**On power on the system:**

  
  * The system will check the invalid tries counter
        
  * If it’s 9 or more:

    The red LED will be switched on and will be preventing the user from entering the codes and waiting until 5 minutes.
