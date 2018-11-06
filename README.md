# Payroll Entry interface with MAS90 (C++)


### Background
- For some reason the payroll module of the enterprise accounting software for a company was set up to process payroll every two when historically the company processes payroll on the 15th and end of month. The parent company had about 40 restaurant locations which were treated as seperate companies in the accounting software.
- A seperate program had already been developed that was supposed to accept hours for each employee, save internally, calculate regular and overtime hours for importing into MAS90 process payroll. The main problem was that this program that was cobbled to together in Microsoft Access hard to use and also imported bad data into MAS90 which, of course, takes awhile to correct. 
- The enterprise accounting software (MAS90) ran on the local network.

### Solution
- The application I wrote was far more intitive and always passed good payroll data into MAS90. 
- It worked so well, I was asked interface with their Aloha POS system that already collected hours when employees clocked in. Aloha also ran on a local server at the home office. 


#### Initial screen 

Below is the screen the end user sees when getting ready to enter payroll. The end user is first prompts with the most likely payroll ending date which is calculate based on the current date. In the previous program this had to me selected everytime. The spinner control allows the user to select a different end date. Once the user tabs out the date field, the ending date is locked in for the session. 

Next the end user selects the company which is a specific restaurant location. When the company (location) is selected, my application retrieves all the valid employes in MAS90 and also retreives previously entered hours which are applicable. Then end users is prompted to enter hours for the current period.

Note: All screens have live data so indentifying information is pixilated.

![pte_0515-select-company-pix-border](https://user-images.githubusercontent.com/23184069/47984957-d9997400-e09d-11e8-9f6a-aae8a7aa6b34.jpg "Initial Screen")

Once a company (restaurant location) is selected, hours for each employee are entered. Time sheets were faxed to the home office at that time. Note the "Status:" edit box which gives the user details on what is happening in the background including any descrepencies. In this case, company 613 was selected, 42 employees were (probabbly some were no longer active but data is there), 30 employees were active in MAS90. Company 613 had employee hours collected in the POS system (Aloha) and automatically uploaded. In this case, the hours for each employee are automatically populated on the screen for review. When Aloha is available, the end user can just export for upload and the location (company) is done in less than a minute.

![pte_0930-time-entry-screen_pix_border](https://user-images.githubusercontent.com/23184069/47985268-ba4f1680-e09e-11e8-8b79-1b23795b9a1e.jpg "Screen for coding hours")

In the case below my application indicates a descrepency that needs attention. Aloha reports hours for two employees that aren't active in MAS 90 for some reason. This will need to be corrected, obviously.     

![pte_0615_aloha_inactive_pix_border](https://user-images.githubusercontent.com/23184069/47985208-8d026880-e09e-11e8-8818-7c33ea608b3c.jpg "Coding more hours")

The Status box below shows routine processing. The application was opened and ending date selected. Location 622 was selected and processed, then location 628. Once my application was tweaked I was told that entering payroll for processing took just 10 minutes. 

![pte_0515-timeentryscreen_pix_border](https://user-images.githubusercontent.com/23184069/47985144-5c223380-e09e-11e8-8c4a-3ad4b2368d74.jpg)

Time sheets then need to be printed out to send to each restaurant. My program produced produced time sheets for each employee formated on a calender for the upcoming pay period. Note: this company's work week is Mon-Sun, as opposed to Sun-Sat.

![pte_1215-managers time entry form0002-border](https://user-images.githubusercontent.com/23184069/47985311-d81c7b80-e09e-11e8-8ef6-d4ad93efe285.jpg "Time Sheet")

The application also produced some reports like to tracking overtime which was important. 




