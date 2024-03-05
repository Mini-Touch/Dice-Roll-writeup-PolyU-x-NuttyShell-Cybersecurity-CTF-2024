## Challenge Name: Dice Roll 擲骰仔
Category: Blockchain
Points: 453
Solves: 17

Challenge Description: 
I bet you can't guess it.

我賭你估唔到。

http://chal.polyuctf.com:11337/

Flag format 格式: PUCTF24{xxx}

Author 作者: Sunny

### Approach

1. Open [Remix - Ethereum IDE](https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.24+commit.e11b9ed9.js)--> open a new .sol file --> copy the code from [Dice Roll](http://chal.polyuctf.com:11337/level/0x0A14079e1215a4758Aa0215B50581A225930f721)

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/copy.png" border="0">

3. Setup the attack Code
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/add_attack.png?raw=true" border="0">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/add_attack.png?raw=true" border="0">

5. Compile --> change environment --> deploy --> attact
   
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/environment.png" border="0">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/deploy.png" border="0">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/attack.png" border="0">

7. Flag
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/check.png" border="0">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/enter_10times.png" border="0">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/flag.png" border="0">

### Flag
Flag: PUCTF24{n0_r3n4omn3ss_1n_bl0ckch41n_vuLptYG7wexbBQ8ZvtYhGU2MdW4uT7po}

### Reference
https://ctf-wiki.org/blockchain/ethereum/attacks/randomness/
https://www.youtube.com/watch?v=YGIDhidOwFM
https://ethernaut.openzeppelin.com/
---
[Back to home](<link>)
