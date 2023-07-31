# **UCB FinTech Bootcamp Module 19 Challenge**
# *Crypto Wallets : Blockchain using Python*
## **Introduction**
### The Bootcamp Module 19 Challenge - Crypto Wallets : Blockchain using Python requires creation of a wallet to manage transactions in a blockchain-based ledger system, accessible to the user via a web interface to facilitate transaction recording and balance management: Using a Streamlit application called "Fintech Finder", the application interacts with an Ethereum blockchain network (Ganache) and allows users to hire Fintech professionals and make payments in Ether. The application allows the user to chose a FinTech professional, see their hourly rate in ETH, input the hours desired, calculates the wage rate and compare against the wallet balance; once the transaction is posted (e.g. the person hired) the blockchain ledger records the transactions in the form of a new block added to the chain.
---
## **Goals and Objectives**
### *Part I.Imports*  : The required Python modules and functions are imported, including Streamlit for the web interface, dataclasses for data structures, typing for type hints, and web3 for Ethereum blockchain interactions.
### *Part II.  Fintech Finder Candidate Information* : A dictionary (candidate_database) holds information about Fintech Finder candidates, including their names, Ethereum account addresses, ratings, and hourly rates in Ether. There is also a list of candidate names (people).
### *Part III. Streamlit Code*  : The Streamlit application interface is set up using various markdowns, headings, and text elements. The sidebar of the application is created. It displays the client's Ethereum account address and balance, which is fetched using the get_balance function from the crypto_wallet.py script.
### *Step 2, Part 1. Ether Wage Calculation* : The application calculates the total wage in Ether (wage) by multiplying the selected candidate's hourly rate with the number of hours hired (hours). It displays the calculated wage in the sidebar.
### *Step 2, Part 2. Transaction Posting* :  When the "Send Transaction" button is clicked, the application calls the send_transaction function from the crypto_wallet.py script. This function sends an Ethereum transaction to pay the hired candidate. The transaction hash is returned and displayed in the sidebar.
### Overall, this code demonstrates the basic implementation of a crypto wallet with its balance and transactions managed in a blockchain using Streamlit for user interaction.
---
## **Technologies and Tools**
### The following list includes the main technologies and tools using during the preparation and deployment of the solution:
### 1. *Python* - Programming language used to code the solution. Version 3.7.13 was used. Required libraries and frames listed in the Installation section below
### 2. *GitHub* - Reposotory for code deployment, version management and documentation of the presented solution
### 3. *Visual Studio Code* - IDE tool for coding, code testing/debugging and solution documentation. Version 1.80.2 was used
### 4. *Git Bash console* - Local console used to test the coded solution and sync wiht GitHub Version 2.40.0.windows.1 was utilized
### 5. *Slack* - Collaboration tool to communicate and brainstorm with other FinTech Bootcamp participants
### 6. *Operative System* - This solution was prepared in a PC running Windows 11 v H22
### 7. *[dataclasses](https://docs.python.org/3/library/dataclasses.html)* - The dataclasses module provides a decorator and functions for creating classes with minimal boilerplate code. It is used for creating data classes, which are classes primarily used to store data rather than providing complex behavior. No installation needed.
### 8. *[typing](https://docs.python.org/3/library/typing.html)* - The typing module provides support for type hints in Python, allowing developers to specify the types of variables, function arguments, and return values. Type hints improve code readability and can be used by type checkers and code editors to provide better hints and warnings. No additional installation needed.
---
## **Installation Guide**

### 1. [Streamlit](https://docs.streamlit.io/) : Streamlit is a Python library used for building web applications for data science and machine learning projects. It allows developers to create interactive web interfaces with minimal code, making it easy to turn data scripts into shareable web apps.
#### 1.1. Open the GitBash terminal
#### 1.2 Type the following command and press Enter:
```python 
pip install streamlit
```
### 2. [web3](https://web3py.readthedocs.io/) : Web3.py is a Python library that provides tools for interacting with Ethereum nodes through JSON-RPC. It allows you to interact with smart contracts, send transactions, and perform other blockchain-related tasks. To install, follow these instructions:
#### 2.1 Open the GitBash terminal
#### 2.2 Type this command and press Enter:
```python 
pip install web3
```
---
## **Solution Structure**

### The **[18.DeFi](https://github.com/LUTOV001/18.DeFi)** repository in GitHub contains the solution components. The repository consists of the following folders and contents as described below:
 
###   *1. Results :* Contains the screenshot files showing the results of running the Streamlit application as well as the transactions as recorded in the Ganache application
###   *2. gitignore :* Instructions for which files/file types to exclude from the sync process between GitHub and the local environment.
###   *3. README.md :* The present file containing this outline of the challenge and its components and results.
###   *4. fintech_finder.py:* This is the Python program with the code for the challenge solution.
---
## **User Instructions**
### 1. Launch the GitBash terminal and navigate to the folder containing the repository. Once there, execute the program using the following command line:
```python 
streamlit run fintech_finder.py
```
### 2. In the launched streamlit web page, in the sidebar on the left, verify that the **ETH balance** reflects your account/wallet balance in Ganache (e.g. the opening wallet balance) 
### 3. Review the list of FinTech professionals and their rates (wage) on center of the page.
### 4. In the drop down menu on the left, select the FinTech professional you want to hire and the input number of hours you want to hire them for. Press *Enter*
### 5. Verify the calculation of the cost to hire them (e.g. wage rate times the hours desired) to verify your wallet balance has enough ETH to cover the cost.
### 6. Press the **Send Transaction** button to have the application validate the data and post the transaction in the blockchain (See the balloons!!). Observe the **ETH Balance"** getting updated (e.g. reduced) by the cost of the transaction. Navigate to Ganache to see the details of the posted transaction in the blockchain and the details of the block created into the chain.
####
---
## **Results**
#### Below are the screen shots showing the application and results from executing the steps described above:  
### ***1. Initial Wallet Balance in Ganache***
#### Shows the initial wallet balance in Ganache. There were 100 ETH balance on each address.
##### ![Ganache_Initial_Bal.jpg](https://github.com/LUTOV001/19.CryptoPay/blob/main/Results/Ganache_Initial_Bal.jpg)
#####
### ***2. FinTech Finder Transaction Posted***
#### Shows the results of the selection of the FinTech professional hiring, including the the hash of the block created and the ***Total Wage in Ether*** of 0.061 ETH to be deducted from the initial wallet balance.
##### ![Transaction_hash.jpg](https://github.com/LUTOV001/19.CryptoPay/blob/main/Results/Transaction_hash.jpg)
#####
### ***3. Ganache End Balance***
#### Shows the final wallet balance of 99.98 ETH in Ganache after the ***Total Wage in Ether*** of 0.016 ETH (rounded to 0.02 ETH) has been deducted from the original 100 ETH balance
##### ![Ganache_End_Balance.jpg](https://github.com/LUTOV001/19.CryptoPay/blob/main/Results/Ganache_End_Balance.jpg)
####
### ***5. Transaction Count***
#### Shows the ***Transaction Count*** of 1 in the crated block in Ganache (Block 6)
#### ![transaction_count.jpg](https://github.com/LUTOV001/19.CryptoPay/blob/main/Results/transaction_count.jpg)
####
### ***5. Block in Ganache ***
#### Shows the details of the block created in Ganache (Block 6). Note that the ***To Address*** corresponds to the address of the selected FinTech professional(Kendall), also shown on screenshot 2 above.
#### ![block.jpg](https://github.com/LUTOV001/19.CryptoPay/blob/main/Results/block.jpg)
---
### **Credits**
#### Prepared by Luis Torres 
#### [LUTOV001](https://github.com/LUTOV001)
#### July 2023