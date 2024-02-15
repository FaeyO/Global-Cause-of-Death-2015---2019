# Global Cause of Death : 2015 - 2019

### Dashboard Link : https://public.tableau.com/views/Globalcausesofdeath2015-2019/GlobalcauseofdeathDS?:language=en-US&publish=yes&:sid=&:display_count=n&:origin=viz_share_link

## Problem Statement

Within the dynamic realm of public health, data serves as an illuminating guide. Deep diving into an extensive dataset spanning from 2015 to 2019, I unravel the intricate tapestry of global causes of death.

By meticulously analyzing a myriad of causes, ranging from communicable diseases to non-communicable conditions, profound insights emerge, shedding light on the multifaceted challenges that impact global health.
Over the course of five years, I meticulously decipher temporal nuances in causes of death. This exploration uncovers emerging trends on a global scale, offering valuable insights that shape our understanding of public health priorities.

Each region narrates a unique story. Through a meticulous dissection of causes of death across countries and continents, utilizing tools like Pareto's chart, I unravel the complex interplay of significant few causing major mortality.
Are there new patterns on the horizon? Uncovering emerging trends becomes pivotal for anticipating health challenges and proactively designing effective interventions.

### Steps followed 

- Step 1 : Write SQL query to get data needed for analysis from the database.
- Step 2 : Data Cleaning and validation was carried to ensure data quality and intergrity is kept.
- Step 3 :  Save the cleaned and filtered data to a csv file.
- Step 4 :  Load the dataset into Tableau for visualizations..
- Step 5 : Create a calculated field called 'disease' by cleaning the 'diseases' column
- Step 6 : Each graph was used as a filter for easy visualization and interaction. 
- Step 7 : Various  Visual like Paretto's chart, line charts, bar charts ,and pie chart was used to show the various insights below;

  (a) Occurence of death in countries over the years.

  (b) The significant cause of death driving 80% of death in a country.
  
  (c) Contry and their total mortality value.
  
  (d) Percentage of fatalities due to illness.

  (e) Death toll of a country
  

- Step 9 : In the report view, three text boxes were added to the canvas, to show the Number of Entity in the dataset, the number of disease suffered in a country, and the death toll of a country.

- Step 10 : In the dashboard view, under the object tab, using using image option elements were added to the report design area. 

- Step 11 : A Paretto chart was created to visualize the significant cause driving 80% of death in a country.
        
- Step 12 : New measure was created to 

i. clean the various names of the disease.
    

Following Tableau expression was written for the same,
        
        Replace(REPLACE([Pivot Field Names],'Deaths - ',''),'-  Sex: Both - Age: All Ages (Number)','')

ii. calculate the 20% of disease causing 80% of death 

Follwing Tableau expression was written for the same ,

        RUNNING_SUM(SUM([number of death])) / TOTAL(SUM([number of death]))


 - step 13:        
A card visual was used to represent the number of Entity

![entity_page-0001](https://github.com/FaeyO/Global-Cause-of-Death-2015---2019/assets/118575325/b0d7211a-69c0-4656-a3b8-e896d130e1a4)

 - Step 14 : The report was uploaded to the Tableau public server.
 
# Insights

A single page report was created on Tabeau, and the following inferences can be drawn from the dashboard;

### [1] The number of disease suffered in country Nigeria was 33 unique disease condition across the year 2015 - 2019

### [2] The death toll was about 7 million plus.

### [3] There was a slight reduction in the occurence of fatalities over the years.

### [4] Majority of death were caused by :
 - Neonatal disorders
 - Diarrheal
 - Malaria
 - Lower respiratory infections
 - Cardiovascular diseases

### Use the filter button to see information on other contries.


### Dashboard view

![Global cause of death DS](https://github.com/FaeyO/Global-Cause-of-Death-2015---2019/assets/118575325/463b1910-737d-46f3-ad5e-0fa07f4b16ed)
