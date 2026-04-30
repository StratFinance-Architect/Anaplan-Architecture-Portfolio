# IFRS 18 Implementation Project 


Numbered List 
<img width="799" height="521" alt="image" src="https://github.com/user-attachments/assets/21f02eb3-5e79-41a4-a1f3-89c4f1439948" />
I used a Numbered List so I can handle thousands of accounts without worrying about duplicate names crashing the model. The 'Display Name' you see is actually pulling live from my SYS01 mapping module. It keeps the technical IDs (like GL007) hidden and the UI clean for the finance team.

Module: CALC03 Disaggregation Engine
<img width="925" height="370" alt="image" src="https://github.com/user-attachments/assets/64a52daa-f190-4f87-9657-488dcd899efa" />
I built the CALC03 Disaggregation Engine to handle IFRS 18 requirements where G/L accounts like Interest must be split across Operating, Investing, and Financing categories.

Instead of hardcoding values, I used percentage-based drivers to ensure the logic remains scalable regardless of the transaction volume or timescale in the source data. To prevent manual entry errors, I embedded an automated Integrity Check that uses a dimensional override to verify that total allocations for each account equal exactly 100%. 


<img width="1022" height="526" alt="image" src="https://github.com/user-attachments/assets/0efe9b50-6022-435b-9066-e18255084837" />
Automated IFRS 18 restatement engine in Anaplan that "walks" Trial Balance into the new mandatory structure of Operating, Investing, and Financing categories. 

Instead of simple remapping, I engineered a disaggregation logic (CALC03) that uses percentage-based drivers to split individual G/L accounts, ensuring core costs are separated from financing elements like lease interest. 


<img width="896" height="585" alt="image" src="https://github.com/user-attachments/assets/2ac234f8-3c02-4151-9bd9-501a9c455af3" />



To guarantee data integrity, I implemented a zero-leakage audit module (AUD01) that reconciles the restated totals back to the source data, proving that while the "Operating Profit" has been divided, the total bottom line remains identical. The final output is a specialized reporting layer (REP01) that powers an executive waterfall chart, providing a clear, audit-ready visual of how the P&L shifts from the old standard to the new IFRS 18 definition.
