![megaeth_soft]

> [!WARNING]  
> This is my first software using web3.py. I am not an experienced web3 developer. If you find a shitty code, a bug, or a way to make something better - open a pull request.

# MegaETH
A simple software for swapping, staking, minting on MegaETH testnet.

## Installation

1. Clone the repository:
   
```sh
git clone https://github.com/TestnetMaster29/MegaETH-auto.git
```

```sh
cd MegaETH-auto
```


2. Install dependencies:
```sh
pip install -r requirements.txt
```

4. Create a virtual environment:
 
- **on Linux/Mac**
    ```sh
    python3 -m venv venv
    ```

- **on Windows**
    ```sh
    python -m venv venv
    ```

**Activate the virtual environment:**

- **on Linux/Mac**
    ```sh
    source venv/bin/activate
    ```
    
- **on Windows**
     ```sh
     venv\Scripts\activate
     ```

4. Install the required packages:

- **on Linux/Mac**
    
    ```sh
    pip3 install -r requirements.txt
    ```
    
- **on Windows**
     ```sh
     pip install -r requirements.txt
     ```

5. **RENAME** ```env``` **FILE TO** ```.env```


6. Add your wallet address and private key in ```.env``` file.


7. Configure the software by adding/removing action, or leave the default configuration



8. Start the ```main.py``` file


   
```sh
python main.py
```


## Configuration
### Modes
This software has three modes.

1 - Will execute **user-defined actions** in order(from actions.py) **once**. 

2 - Will **infinitely** execute **random** actions. 

3 - Will **infinitely** execute **user-defined actions in order** (from actions.py).

### actions.py Configuration

In actions.py file you have array called ```ACTIONS```. Customization of user actions for the first and third modes is performed by changing this array. For example:


```
ACTIONS = [
    ("Mint cUSD", mint_cusd, False),
    ("Send GM", send_gm, True),
    ("Random Swap", swap_tokens, True),
    ("tkUSDC staking", stake_tkusdc, True),
    ("Swap all to ETH", swap_all_tokens_to_eth, True),
]
```

This config will execute actions: Mint cUSD, Send GM, Random Swap, tkUSDC staking and Swap all to ETH once in the first and infinitely in second mode.

To make custom action chains you need to change the ```ACTIONS``` array by adding or removing lines. All lines are available here, or at the bottom of the actions.py file starting from line 27 for Russian and from line 57 for English languages.

**All actions:** 
```
(“tkUSDC staking”, stake_tkusdc, True),
(“tkUSDC unstaking”, unstake_tkusdc, True),
(“Mint cUSD”, mint_cusd, False),
(“Random Swap”, swap_tokens, True),
(“Swap all to ETH”, swap_all_tokens_to_eth, True),
(“Send GM”, send_gm, True),
```
```tkUSDC staking``` = *Staking via Teko*

```tkUSDC unstaking``` = *Unstaking via Teko*

```Mint cUSD``` = *Mint cUSD*

```Random Swap``` = *Random Swaps via gte*

```Swap all to ETH``` = *Swap all tokens to ETH*

```Send GM``` = *Send gm via onchaingm (once every 24 hours)*

Last updated: Mon Apr 14 13:36:41 UTC 2025
