Electricity Bill Management System
This project is a simple Electricity Bill Management System built using Python and SQLite.
It calculates electricity charges based on units consumed and applies fines based on delayed payment days.
The generated bill details are stored in a SQLite database (EBILL.db).

📂 Project Structure
├── file1.py        # Main program: takes input, calculates bill, stores & displays records
└── calc.py         # Contains tariff calculation and fine computation functions


🔧 Features


Accepts consumer details (ID, Name, Units, Delayed Days)


Calculates electricity bill based on slab rates


Adds fine based on no. of delayed days


Stores all records in a SQLite database


Prevents duplicate Consumer IDs


Displays all stored bill entries after completion



⚡ Tariff Calculation (calc_amount)
Units RangeRate (₹/unit)0 – 2003.00201 – 4004.50401 – 8006.50Above 8008.00

💸 Fine Calculation (fine)
Delay (Days)Fine Applied0No fine1 – 102% of bill amount11 – 205% of bill amount21 – 3010% of bill amountAbove 3015% of bill amount

🗄️ Database Structure (EBILL1 Table)
Column NameTypeDescriptioncon_idINTEGER (PK)Consumer ID (unique)nameVARCHAR(100)Consumer NameunitsINTEGERUnits ConsumeddaysINTEGERDelay in paymentamountFLOATFinal Bill Amount

▶️ How to Run


Ensure Python 3 is installed.


Run the main program:


python file1.py



Enter consumer details when prompted.


Continue adding entries or exit using the menu option.


After exiting, all stored records will be displayed.



📘 Example Workflow
Enter Consumer ID: 1234
Enter Consumer Name: Rahul
Enter Consumed units: 350
Enter the no. of days delayed: 5

Enter option 1.Add consumer 2.exit: 2

~~~~~~~~~~~~~~~~~~~~~~~
Consumer ID  : 1234
Consumer Name: Rahul
Units        : 350
Days delayed : 5
Amount       : 1214.0
~~~~~~~~~~~~~~~~~~~~~~~


📑 Notes


The database is automatically created if not present.


The script drops and recreates the table on every execution.


Duplicate Consumer IDs are not allowed during the session.




