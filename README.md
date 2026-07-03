SCENARIO 1 IN BDD FORMAT 

Verify the functionality of the compose button
 Given :- The compose button is visible.
 When :- The user wants to send a mail 
 And :- User clicks on the button 
 Then :- User enters the mail id , the subject , the body , attach file 
 And :- Send the mail , shows a progress that the mail is sent 

 Scenario 2 
 Verify the app does not crash or freeze 
  Given :- The compose button is there 
  When :- User clicks on the button multiple times 
  Then :- The mail should not get stopped or crashed 
  And :- Should show the email box efficiently 

  Scenario 3 
  Verify the mail is not getting sent without entering the mail id 
   Given :- A field with placeholder 'To'
   When :- Users do not provide email id 
   And :- Users try to send the mail 
   Then :- The mail is not sent 
   And :- Should show a message that mail id is required 

   Scenario 4 
   Verify the functionality when user sends a mail without subject 
    Given :- The subject field whcich is efficiently used by the users 
    When :- User keeps the subject field empty 
    Then :- Should show a message that field is necessary ( Depends upon business requirements)
    And :- User provides the subject and clicks on send 
    Then :- The mail gets send 

    Scenario 5 
   Verify the functionality when the text in the body is too long 
    Given :- Users are given a mail body
    When :- Users enters long words in the mail body 
    And :- Try to send the mail 
    Then:- Should show a validation message that the word limit has exceeded ( Depends upon business requirements)
    And :- User provides the words in the mail body without exceeding the limit and as a result the ui looks formatted in all devices and browsers 

    Scenario 6 
    Verify the network support upon trying to send a mail containing long texts 
     Given :- There is long text in the mail body 
     When :- User has only mobile network 
     And :- Try to send the mail over mobile network 
     Then - Should show a message mail not send , try switching over a different network lor wifi . 


     Scenario 2 
     Rejects the long texts which depends upon business requirements 
      Given :- A long text is there and user enters it in the mail body 
      When :- There is a word limit (Depends upon business requirements )
      And :- Check the response body , the payload, the postman console and then the response as well 
      Then :- Record all this and log the bug 
      And :- Assign it to the developer mentioning under which conditions the error arises 

      Verifying the response based on data limit and validation 
      Given :- User enters the long text , keeps the subject empty 
      When:- User check the response (Should show 400 , it shows when the data mismatches or empty data is there 
      Then :- User validates the response 
      And :- If wrong , checks the payload, the console and records the response 
      Then :- Logs the bug and informs the developer 
