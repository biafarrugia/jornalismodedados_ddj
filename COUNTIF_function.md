Go to https://data.europa.eu/
<p> Download the dataset “Consolidated list of persons, groups and entities subject to EU financial sanctions” - version 1.1 Full
<p> Import the dataset into Excel. </p>
<p> Objective: find out which programme has the most number of people, groups and entities subject to EU financial sanctions.
Angle story: ranking 
<p> <b> Computational thinking </p> </b>
<p><i> Decomposition: </i>  The dataset has dozens of columns and rows, but we need just to focus on the main information. 
<p><i> Abstraction: </i> Considering the objective of this story, the most important column is “O” (Entity_Regulation_Programme).
<p><i> Pattern recognition: </i> We are working with strings (not numbers). The first step is to check if there is any blank row - and correct/delete them.
Then, we need to find functions and algorithms to deal with text/strings.
<b> <i> <p> Functions and Algorithms: </b> </i>
<p> Using the function Filtering, we can realise that there are more than 30 programmes in the list. 
<p> Now we have to calculate which programme appears more in the EU financial sanctions list.
<p> I choose the algorithm COUNT.IF to check it. Example: =CONT.SE(A1:A13549;"TAQA")
<p> Then, I organised the data by Z-A classification and, finally, I use the SUM to calculate the total of occurrences and its percentage. 

<b> Data Story: </b>
The terrorist group Al Qaeda is the target of 4,237 operative financial sanctions today in the EU, according to an official database published on Data Europe website. 
Al Qaeda is mentioned in the report as “TAQA programme” and detains 36% of all financial sanctions occurrences against persons, groups and entities applied by the EU and UN.

After Al Qaeda, Syria and Ukraine are on the top of the list with 2,208 and 1,013 occurrences, respectively, followed by Iran (944) and Iraq (761).
</html>

Acronyms and Programs List: https://webgate.ec.europa.eu/fsd/fsf/public/files/pdfFullSanctionsList/content?token=dG9rZW4tMjAxNw
