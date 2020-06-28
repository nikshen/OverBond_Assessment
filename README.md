# SDE Online Assessment
Submitted by: Nikhil Shenoy
Date of Submission: 06/28/2020

** OBJECTIVE **

Objective of the assessment was to capture inputs from a input file named 'sample_input.json', determine 
1. Closest Government bond benchmark
2. Spread between the corporate bond and govt bond benchmark 

** INSTRUCTIONS **
Please place this python executable in the same directory as the the 'sample_input.json' file. 
The code, reads only files named as 'sample_input.json'. 

** LOGIC **
**Step1**: The attached code first captures the file stored in the same location as that of python executable 
**Step2**: Once captured into a dictionary of key value pairs, we first pick the first corprorate bond (identified by a 'c' prefix to 'id' key) and capture the value stored                  against the 'tenor' key of the bond record. 
           **Note**: we have an additional check here to ensure the 'yield' key does not have a 'Null' or 'None' value. 
**Step3**: We screen through all records to find government bonds (identified by a prefix of 'g' in the 'id' key) and determine the tenor difference i.e. absolute value of                    differnece in corporate tenor and govt tenor key value and find the minimum difference. For cases where the difference is same, we compare the 'outstanding_amount' 
          **Note**:
            **Assumptions**
              1. The government bond will NOT have a Null or None! value in its yeild key 
              2. If the differnece  or deviation is same and the outstanding amount is also same, the logic will pick the first occuring id 
**Step4**: Once the id is determined, we compute the base points using the logic provided 
**Step5**: The results are appended to a dictionary
**Step6**: The final result is written and dumped into a file named 'sample_output.json



** TESTING **
The code was tested varying the inputs in the 'sample_input.json' file to test the boundary and regular conditions 
1.Returning multiple corproate bond results
2.Testing with same outstanding amount when difference or diviation was same 

** ASSUMPTIONS **
1.The government bond will NOT have a Null or None! value in its yeild key 
2. If the differnece  or deviation is same and the outstanding amount is also same, the logic will pick the first occuring id
3. The code does not handle formating issues, i.e. $ instead of %  or blank spaces instead of NULL etc. 

PL Used: Python
Environment: Jupyter notebook

              

