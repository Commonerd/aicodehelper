


# AI Code Helper

This extension utilizes GPT artificial intelligence to add comments to code, perform code reviews, and even refactor and generate code.  

<img src="https://blog.kakaocdn.net/dn/050HO/btr2OStdFHu/dqokZRPisKgwkqReTjmjdk/img.gif" width="100%" />

## Requirements

To use this extension, you will need an API key for the GPT API provided by OpenAI.  
Please note that this extension operates based on OpenAI's GPT API, which means that every time you use the extension's features, a request will be made to the GPT API. Therefore, please be aware that there may be charges incurred depending on your usage.  
You can obtain an API key from here: https://platform.openai.com/account/api-keys  

## Powered by

This extension is powered by Chat Completion(model: gpt-3.5-turbo) API of OpenAI.

## Extension Settings

This extension contributes the following settings:
* `aicodehelper.gptkey`: API Key of OpenAI
* `aicodehelper.language`: What language would you like AI to use? (ex: english, korean, chinese)
* `aicodehelper.codereviewprompt`: Prompt template to request a code review from OpenAI
* `aicodehelper.refactoringprompt`: Prompt template to request a refactoring from OpenAI
* `aicodehelper.commmentingprompt`: Prompt template to request adding comments from OpenAI
* `aicodehelper.generatingprompt`: Prompt template to request generating code from OpenAI

## Known Issues

The results obtained from GPT artificial intelligence while using this extension may contain errors or incorrect information. So, be sure to keep this in mind and use it. Users of this extension are solely responsible for its use.

## How to use

AI Code Helper is a tool that automatically performs tasks such as adding comments, refactoring, code review, and general requests while writing code.

### Preparation

1. Open VS Code and go to Settings by pressing `Cmd+,`.
2. Search for `aicodehelper` and check the settings values.
3. Set the API key for OpenAI, which can be obtained from [OpenAI](https://platform.openai.com/account/api-keys), to `gptkey`.
4. Set the language you want to use for GPT in `language`.
5. You can optionally modify the `prompt template`.

### Usage
1. **Adding Comments**
   This feature uses artificial intelligence to analyze code and provide explanations for the code.
   <img src="https://blog.kakaocdn.net/dn/bNM7Lr/btr2TC3VdgJ/3WlDMegYVucPwOANBQVRtk/img.gif" width="100%" />
   Select the code you want to add a comment to in the code editor and press `Ctrl+Shift+Alt+Z`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located  
   *Select the code that looks like the one shown below and press the shortcut.*

       for(let i=0;i<10;i++) {  
          code();  
          main();  
       }  
  
   *This will be converted like*

       // Using a for loop to iterate from 0 to 9.
       for(let i=0;i<10;i++) {
    
          // Calling the function "code".
          code();
    
          // Calling the function "main".
          main();
       
       }  // End of the for loop.

2. **Refactoring**
   This feature uses artificial intelligence to refactor code
   <img src="https://blog.kakaocdn.net/dn/bNM7Lr/btr2TC3VdgJ/3WlDMegYVucPwOANBQVRtk/img.gif" width="100%" />
   Select the code you want to refactor in the code editor and press `Ctrl+Shift+Alt+R`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located  
   *Select the code that looks like the one shown below and press the shortcut.*

       let a = 20;
       if(a==30){
          console.log('d is 300')
       }
       if(a==10){
          console.log('d is 100')
       }
       if(a==20){
          console.log('d is 200')
       }
   
   *This will be converted like*


       const a = 20;
 
       const conditions = {
          30: 'd is 300',
          10: 'd is 100',
          20: 'd is 200'
       };
 
       if (conditions[a]) {
          console.log(conditions[a]);
       }


3. **Code Review**
   This feature uses artificial intelligence to identify the strengths and weaknesses of the code and provide code reviews.
   <img src="https://blog.kakaocdn.net/dn/bNM7Lr/btr2TC3VdgJ/3WlDMegYVucPwOANBQVRtk/img.gif" width="100%" />
   Select the code you want to review in the code editor and press `Ctrl+Shift+Alt+C`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located  
   *Select the code that looks like the one shown below and press the shortcut.*

         let a = 20;
         if(a==30){
            console.log('d is 300')
         }
         if(a==10){
            console.log('d is 100')
         }
         if(a==20){
            console.log('d is 200')
         }

   *This will be converted like*

		// Good part: 
		The code correctly checks the value of variable "a" against different conditions and prints the corresponding message when the condition is true. 

		// Bad part: 
		The code uses multiple if statements instead of else if or switch statement, which can result in unnecessary checks and slower performance. Additionally, there is no default or catch-all condition for when "a" does not match any of the given conditions, so the code will not output anything in that case.

		let a = 20;
		if(a==30){
		   console.log('d is 300')
		}
		if(a==10){
		   console.log('d is 100')
		}
		if(a==20){
		   console.log('d is 200')
		}


4. **General Requests**
   This feature uses artificial intelligence to handle requests for various queries beyond programming code
   <img src="https://blog.kakaocdn.net/dn/bNM7Lr/btr2TC3VdgJ/3WlDMegYVucPwOANBQVRtk/img.gif" width="100%" />
   Select the code you want to request in the code editor and press `Ctrl+Shift+Alt+M`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located  
   *Select the code that looks like the one shown below and press the shortcut.*

       Write a lyrics praise javascript in a style of a song "Ain't no mountain high enough".
   *This will be converted like*

		(Verse 1)
		There ain't no code too complex
		No function too hard to execute
		With JavaScript by my side
		I can conquer any coding plight

		(Chorus)
		Ain't no problem too big
		Ain't no bug too tough
		With JavaScript on my side
		I can make anything work

		(Verse 2)
		From web pages to apps
		From front-end to back-end
		JavaScript is the glue that holds it all
		Together, seamless and smooth
		...   
5. **Code Generating**
   This feature uses artificial intelligence to generate code based on the description of the desired functionality provided in the explanation
   <img src="https://blog.kakaocdn.net/dn/bNM7Lr/btr2TC3VdgJ/3WlDMegYVucPwOANBQVRtk/img.gif" width="100%" />
   Select the code you want to request in the code editor and press `Ctrl+Shift+Alt+G`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located  
   *Select the code that looks like the one shown below and press the shortcut.*

       Make a function that take two arguments and plus them and return.
   *This will be converted like*
   
		# Define a function that takes two arguments
		def add_two_numbers(num1, num2):
		    
		    # Add the two numbers
		    result = num1 + num2
		    
		    # Return the result
		    return result
6. **General Requests with Inputbox**
   This feature is useful when you want to request additional processing for something that has already been created.  
   <img src="https://blog.kakaocdn.net/dn/TEKHP/btr3dDug45L/HaOxtv8CXeQBYHa8sBnQy0/img.gif" width="100%" />
   Select the code you want to request in the code editor and press `Ctrl+Shift+Alt+,(comma)`.  
   If you press the shortcut key without making a selection, it automatically selects the line where the cursor is located.  
   The entered prompts can be reused with `Ctrl+Shift+Alt+.(full stop)` function.  
   *Select the code that looks like the one shown below and press the shortcut.*

       Write a lyrics praise javascript in a style of a song "Ain't no mountain high enough".
   *This will be converted like*

		(Verse 1)
		There ain't no code too complex
		No function too hard to execute
		With JavaScript by my side
		I can conquer any coding plight

		(Chorus)
		Ain't no problem too big
		Ain't no bug too tough
		With JavaScript on my side
		I can make anything work

		(Verse 2)
		From web pages to apps
		From front-end to back-end
		JavaScript is the glue that holds it all
		Together, seamless and smooth
		...   

## Release Notes

### 1.0.34

Initial release of this extention

---








