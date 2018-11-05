# Payroll Entry interface with MAS90 (C++)


### Background
- For some odd reason the company's the payroll module of the enterprise accounting software was set up to process payroll every two when historically the company processes payroll on the 15th and end of month. The parent company had about 40 restaurant locations which were treated as seperate companies in the accounting software.
- A seperate program had already been developed that was supposed to accept hours for each employee, save internally, calculate regular and overtime hours for importing into MAS90 process payroll. The main program was that this program that was cobbled to together in Microsoft Access hard to use and also imported bad data into MAS90 which, of course, takes awhile to correct. 
- The enterprise accounting software (MAS90) ran on the local network.

### Solution
- The application I wrote was far more intitive and always passed good payroll data into MAS90. 
- It worked so well, I was asked interface with their Aloha POS system that already collected hours when employees clocked in. Aloha also ran on a local server at the home office. 


#### Initial screen 

Below is the screen the end user sees when entering payroll. The end user is first prompts with the most likely payroll ending date which is calculate based on the current date. The spinner control allows the user to selected a different end date. Once the user tabs out the date field, the ending date is locked in for the session. 

Next the end user selects the company which is a specific restaurant location. When the company (location) is selected, my application retrieves all the valid employes in MAS90 and also retreives previously entered hours which are applicable. Then end users is prompted to enter hours for the current period.

Note: All screens have live data so indentifying information is pixilated.

![pte_0515-select-company-pix-border](https://user-images.githubusercontent.com/23184069/47984957-d9997400-e09d-11e8-9f6a-aae8a7aa6b34.jpg "Initial Screen")




![pte_0930-time-entry-screen_pix_border](https://user-images.githubusercontent.com/23184069/47985268-ba4f1680-e09e-11e8-8b79-1b23795b9a1e.jpg)

![pte_0615_aloha_inactive_pix_border](https://user-images.githubusercontent.com/23184069/47985208-8d026880-e09e-11e8-8818-7c33ea608b3c.jpg)

![pte_0515-timeentryscreen_pix_border](https://user-images.githubusercontent.com/23184069/47985144-5c223380-e09e-11e8-8c4a-3ad4b2368d74.jpg)

![pte_1215-managers time entry form0002-border](https://user-images.githubusercontent.com/23184069/47985311-d81c7b80-e09e-11e8-8ef6-d4ad93efe285.jpg "Time Sheet")


