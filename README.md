# sheets-protect
**Google Sheet Passcode Protection System** uses Google App Script and JavaScript Obfuscator Tool to protect your Google Sheet with Passcode. 

What can Google Sheets Passcode Protection System do?
- Allows you to protect your Google Sheets projects with a passcode so that you could sell your Google Sheets project.
- Prevent users from running any App Script function before getting the correct passcode from you.
- Prevent users from reselling your Google Sheets projects. 
- Make-a-copy proof, the copy will require license/passcode activation again even users make-a-copy after getting verified.



**Procedure to Implement the Google Sheet License/Passcode Protection System:**

Step 1. Open your Google Sheets Project. If you don't have one, create a new Google Sheets at sheets.new.

Step 2. Click on Tools > Script Editor in the Google Sheet.

Step 3. Open cre8tive.page.link/protect-script. The script is read-only but you can copy all the code inside and paste it (replace) at your Google Sheets Script Editor.

Step 4. The current basic level sample uses the Google Sheets ID first 6 characters as the license. For example, Google Sheet ID: 1c2g-lj2FPDAtbyacWhjiMUVFpm_uKK9qz_-j0pYRbdM, the license/passcode to unlock will be 1c2g-l.
*Google Sheet ID can be found on the URL of Google Sheet (not App Script) just between the "/d/" and "/edit" . 

Step 5. If you have JavaScript / Google App Script programming knowledge, you can change the "dis = " to any passcode/license that you wish. We recommend you not to use a fix passcode / license, instead use the Google Sheet ID and your customized standard formula as the passcode/license. If you don't have any programming knowledge, do not change any of the code!
*The reason behind some random variable like the following is use is to further increase the difficulty of others to guess the correct passcode/license from your code. You can change the variable name to anything you like:
- requestFunc() : Function that checks whether if the passcode/license is inputted previously.
- checkReq() : Function that checks  whether if the passcode/license saved in Script Properties is correct. This function is for make-a-copy proof. 
- inx : passcode/license that input by users stored in Script Properties as "iny" of the Google Sheets Projects. The program will not prompt for passcode/license if correct passcode/license is inputted and stored in "iny".
- dis : correct passcode/license string/formula.

Step 6. Replace ALL the "Your Company Name", "Link that customer able to contact you" and "Link to get the license/passcode" to your information. This will show as error message when users input the wrong passcode/license. Refer to the picture at the bottom of the page.
Example: requestFunc('Cre8tiveNow','fb.com/cre8tivenow','cre8tive.page.link/generate');

Step 7. Do not change the onOpen(e) function and onEdit(e) function. Input requestFunc('Your Company Name','Link to contact you','Link to get the Code'); to the top of all your function.
*(optional) You can include checkReq(); on top of the requestFunc();. 

Step 8. Once you save (be sure to backup a copy of all your code to a place just in case you messed up the current code). Then, copy all your code.*Once you saved, your Google Sheets projects will requires license/passcode to unlock or activate once refreshed.

Step 9. Go to https://obfuscator.io/ and paste your code to Copy & Paste JavaScript Code column. The click on Obfuscate.*Code obfuscator is to "encrypt" your code so that users will not be able to delete or remove your passcode/license function from the core function of your Google Sheets App Script project. It only make people harder to 'decrypt' your code but not impossible.

Step 10. Copy the whole output and paste it back to the Google Sheets replacing all the code. (Make sure to backup your original coding at other place or other Sheets, as the code will be replaced with obfuscated code. Else, you will have hard time changing your original code)

Step 11. Try each of the function of your Google Sheets Projects and make sure they work. Your Google Sheets Projects is now ready to sell. 
*The pop out asking for passcode will stop pop out when correct passcode is inputted and Passcode Verified pop out. If no Passcode Verified pop out shows, it maybe due to timeout. Refresh the sheet and key-in the passcode again.

**Selling your Google Sheets Project**
1. Make sure to Share your Google Sheets and change it to anyone with the link can view.

2. You can ask user/customer to make-a-copy of the Google Sheets by replacing the URL of /edit to /copy. 
Example: https://docs.google.com/spreadsheets/d/xxxx/edit change to https://docs.google.com/spreadsheets/d/xxxx/copy

3. They will get the pop-up requesting for license/passcode once they open the sheet or press on any function.
*The pop out asking for passcode will stop pop out when correct passcode is inputted and Passcode Verified pop out. If no Passcode Verified pop out shows, it maybe due to timeout. Refresh the sheet and key-in the passcode again.

**Preparing your License/Passcode Generator**
1. An easy way  is to create a new Google Sheets (sheets.new) for  code generation using formula.

2. You can use this example for your generator. Key in user's Sheet ID in column B3:B and the license/passcode will show at the passcode/license column. Copy the license/passcode to your user  to unlock/activate their Google Sheets.
*You can change the formula in the Example Code Generator Sheet to suit your passcode/license formula.
