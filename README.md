<div align="center">
<img src="https://github.com/JosefinaAureaAmaro/00_Python_Beginner/blob/master/images/github_repo_header_img.PNG">
</div>
<h2> Repository Details </h2>
<div>
  <p><b>Data Source Format:</b> Excel CSV</p>
  
  
  <p>The <b>objectives</b> of this repository was to practice beginner techniques of python by iterating through CSV data to return results that meet conditions, sumate the values per categorical data & structure the final result into a legible format for reporting.</p>
  <p> Also, demonstrated was a technique called List Comprehension, which was efficent short hand that still displayed readable logic to the developer.</p>
  <p> Lastly, the result of these excerises were to print the results in the console & to export the result into .txt file format.</p>
</div>

<h2> Code Samples 📓</h2>
<p><b> Sample from:</b> Python_For_and_While_Loops</p>

```python
    # Objectives: 
    # 1. To loop thorough the candidate column and the list of candidates to calculate total votes per Candidate
    # 2. Calculate the % of votes per candidate


    while i < len(list_candidates):

        # (Boolean) total votes per candidate =  count the number of times the candidate name appears in the column by adding 1 for each True conditon
        total_votes_per_candidate = sum( 1 for x in candidates if x == list_candidates[i]) 
        percent_votes_per_candidate = round((total_votes_per_candidate / tot_votes) * 100,2)
        #print list of candidates, percentofvotespercan & totalvotespercan
        results_output = (f"{list_candidates[i]}:{percent_votes_per_candidate}% ({total_votes_per_candidate})")

        # to create a list of total votes per candidates produced
        ## the total votes per candidate come out with the same index value as the ordered list of candidates
        candidate_vote_tally.append(total_votes_per_candidate)
        tally_results.append(results_output)
        
        i += 1
 ```
<div align="center">
<a href="https://github.com/JosefinaAureaAmaro/00_Python_Beginner/blob/master/Python_For_and_While_Loops/election_analysis.py">
<img src="https://github.com/JosefinaAureaAmaro/00_Python_Beginner/blob/master/images/code_click_img.PNG"></a>
</div>

<p><b> Sample from:</b> Python_For_Loop_List_Comprehension</p>

```python 
 #----------------- Budget Analysis Examples--------------------------------------
 
    # Reformat Data: convert profit value strings to intergers
    profit_values = [int(x) for x in profit]
    
    # to calculate avg variance in profit&loss month over month
    profit_variance = [profit_values[i+1] - profit_values[i] for i in range((tot_months -1))]
    
    ## Analysis Results
        budget_analysis_results = (f"""Financial Analysis\n
                    --------------------------\n
                    Total Months: {tot_months}\n
                    Total: ${tot_prof}\n
                    Average Profit Value: ${average_profit}\n
                    Average Profit Variance: $ {average_profit_variance}\n
                    Largest Increase in Profitability: {month_of_max_profit_variance} (${max_profit_variance})\n
                    Largest Descrease in Profitability: {month_of_min_profit_variance} (${min_profit_variance})""")

    
        print(budget_analysis_results)
    
    
 
    #-------------to print budget analysis to a .txt file-------

        import sys

        budget_data_path = os.path.join('.','budget_analysis_results.txt')
        with open(budget_data_path,'w') as budget_analysis_file:
            sys.stdout = budget_analysis_file

            print(budget_analysis_results)
```
<div align="center">
<a href="https://github.com/JosefinaAureaAmaro/00_Python_Beginner/blob/master/Python_For_and_While_Loops/election_analysis.py">
<img src="https://github.com/JosefinaAureaAmaro/00_Python_Beginner/blob/master/images/code_click_img.PNG"></a>
</div>
