# Moxxi-Take-Home

Figma Design Link: https://www.figma.com/design/YzdU5ov2QfaZglfKDQAE19/Moxxi-Take-Home?node-id=0-1&t=am2aIpywRRIn4qCm-1

Live Link: https://dannioo.github.io/portfolio/Prize%20Zingo/index.html

Set-Up Instructions:
1. Ensure working internet connection
2. Download this repository
3. Open index.html in your browser

Design Write-Up
* Improvements made from the original design are based on the idea that the form should have motion and interactivity beyond the inputting of information.
* Having a button that changes on hover for example encourages the user to complete each section.
* Added a navbar to allow the user to be able to see how much of the form is left and to allow for transition between multiple steps beyond the next and previous step buttons on each section.
* Replaced static background with parallax image to encourage motion within the page.
* Text is contrasted well against the background and keyboard shortcuts work for accessibility purposes.
* I wanted to split the form into personal info, address, and contact info because I believe that is the most relevant grouping of steps in a real-world setting. First, the system should determine the user's name (common for most forms to have names at the top). Second, as this is a home-improvement sweepstakes, the system should determine the geographical location as the second step, as different locations can have different challenges and price considerations. Passing all this info into the formData object allows for the possibility for server-side processing to determine costs or other factors without passing in info that is not relevant to this step. Third, phone number and email are at the end mainly due to a psychological componenet. These two fields have the most value when it comes to user data, as most sweepstakes are ways to gather contact info for newsletters and the like, and the user is most likely to fill out this information since they've already gone through most of the form already.
* Site is fully mobile responsive, including collapsible navbar
* Incorporated light gray and green colors from original design, introduced dark gray navbar and buttons to promote color contrast
* Console logs formData at each step

Data Validation and Convenience Features
* Clicking the links in the navbar first checks if form is complete, and prevents users from resubmitting or accessing previous sections after submitting
* Next Step buttons properly verify required data in each section
* Unique fields properly invalidate incorrect information (street address requires a string of numbers followed by a space and the street name to be validated, ZIP requires exactly 5 digits, email address must follow proper name@website.com format, etc)
* Using the navbar to skip to the last section and submitting will kick the user back to previous sections and prompt them to fill out any missing information
* Completing the form will present a confirmation and prevents users from resubmitting or accessing previous sections after submitting
* I have included two commented functions in the header to handle form submission, in a real-world application, you can simply choose which method of sending the data you want and uncomment the appropriate version of the final submission function
