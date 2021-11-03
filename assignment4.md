# Analysis of Sen. Blumenthal's (D-CT) Campaign Donations from 2021-2022

### A link to the dataset: [Campaign donations to Sen. Richard Blumenthal (D-CT), 2021-2022](https://www.fec.gov/data/receipts/?data_type=efiling&committee_id=C00492991)

* What percentage of Sen. Richard Blumenthal’s (D-Conn.) campaign donations comes from PACs, ORGs, etc.?

    * INDs = 47%
    * PACs = 34%
    * COMS = 15%
    * ORGs = 4%

* Are there any connections that stands out between his donors and the pieces of legislation he either sponsors or c-sponsors?

  * I did not notice any obvious connections between his donors and the pieces of legislation he supports. Although I did think it was interesting that only 4% of Sen. Blumenthal’s campaign donations come from organizations, most of those organizations represent different tribes. There are no pieces of legislation sponsored by Blumenthal directly related to supporting Native Americans in 2020 or 2021. This information led me to my next question.

* Who are his top donors and what are their backgrounds?

  * Most of his individual donors are identified as attorneys or working for investment companies. After researching some of the legislation that Blumenthal sponsored/co-sponsored in 2020 and 2021, he has largely supported legislation having to do with public health or gun control. It seems that Blumenthal is not highly influenced by his individual donors or organizations. PACs do not disclose the sources of their funding, and the companies who donated do not seem to be related to public health or gun control either. However, some of the largest companies within Blumenthal’s state are hospital/medical related. It is possible that medical companies are donating to Blumenthal through PACs, but according to Open Secrets, pharmaceutical companies, physicians and health professionals typically donate directly to individual candidates. After analyzing the data, there does not seem to be any money donated to Blumenthal that may influence his work.
  
### Steps Used to Analyze and Clean Data 

* First, I cleaned the load_timestamp column displaying hashtags by highlighting the whole column and selecting the dropdown menu. There I pressed short date to show actual dates.

* Second, I cleaned the contribution_receipt_amount column by highlighting the whole column and selecting the dropdown menu. There I pressed currency to display dollar amounts.
 
* Third, I deleted columns with information that was not very useful. I kept:

  * entity_type (PAC, IND, COM, ORG) 
  
  * load_timestamp 
  
  * contributor_first_name
  
  * contributor_middle_name 
  
  * contributor_last_name
  
  * contributor_city
  
  * contributor_state
  
  * contributor_zip
  
  * contributor_employer
  
  * contributor_occupation
  
  * contributor_aggregate_ytd
  
  * contribution_receipt_amount
  
  * contribution_receipt_date
  
  * memo_text

* Fourth, I alphabetized the contributor_last_name column to better organize those that donated as indidivuals and donations made by PACs.

* Fifth, I put filters on the entity_type column and the contribution_receipt_amount column to help answer my questions listed above. 

* Lastly, I used the =sum() function to add up donation amounts from different donors and I used the "/" to divide by totals to calculate percentages.

### Sample Headline and Story

#### As Far as We Know, Blumenthal’s Finances Leave Senator’s Integrity Intact

Sen. Richard Blumenthal, D-CT, is known for being an avid supporter of public health legislation. His individual donors don’t seem to be influencing his behavior, but that doesn’t guarantee that the wealthiest donors aren’t still pulling the strings behind the curtain.

It’s often said that money talks, and when it comes to politicians, many have been accused of being “puppets” to wealthy donors. There are laws in place to limit and prevent wealthy donors from pushing their agenda, but PACs have still made it possible for big money to continue getting ideal politicians ahead. In Blumenthal's case, PACS are the second largest group of donors listed in his campaign finances.
