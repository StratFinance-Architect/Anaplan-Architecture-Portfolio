# IFRS 18 Implementation Project 


Numbered List 
<img width="799" height="521" alt="image" src="https://github.com/user-attachments/assets/21f02eb3-5e79-41a4-a1f3-89c4f1439948" />
I used a Numbered List so I can handle thousands of accounts without worrying about duplicate names crashing the model. The 'Display Name' you see is actually pulling live from my SYS01 mapping module. It keeps the technical IDs (like GL007) hidden and the UI clean for the finance team.

Module: CALC03 Disaggregation Engine
<img width="925" height="370" alt="image" src="https://github.com/user-attachments/assets/64a52daa-f190-4f87-9657-488dcd899efa" />
I built the CALC03 Disaggregation Engine to handle IFRS 18 requirements where G/L accounts like Interest must be split across Operating, Investing, and Financing categories.

Instead of hardcoding values, I used percentage-based drivers to ensure the logic remains scalable regardless of the transaction volume or timescale in the source data. To prevent manual entry errors, I embedded an automated Integrity Check that uses a dimensional override to verify that total allocations for each account equal exactly 100%. 

