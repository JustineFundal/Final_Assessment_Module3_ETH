# Final_Assessment_Module3_ETH

This is the solidity Program that called minting and burning program, this program will show to you how to mint and how to burn the token and you will also know the total supply of the token

## Description

Our project is for MetaCrafters final assessment i make a ethereum that will mint, burn and will know the total supply of the token.

## Getting Started


### Executing program

* First search remix.etheruem.org then once you open the website find the create a new file then named it like this (name).sol then put the code then put your name on token name and to the token abbrevation. when you finish the code, Click the solidity compiler then compile your file. if you are finish compiling the code you can now press the deploy and run transactions then copy the account and use it the address of the burning,minting and balances once you finish putting the account of the address then input a value then transact first transact the minting to store the token then to burn the token just click the transact button on the burning. And if you mint 3 token then you burn 4 nothing will happen because you exceed the store value of the mint.

```
//SPDX-License-Identifier: MIT
        pragma solidity ^0.8.18;


        contract metacrafters{
                string public TokenName = "Fundsal";
                string public TokenAbbrv = "Fnds";
                uint public TotalSupply;
                       

                       mapping (address => uint) public Balances; 

                    function Minting (address Address, uint Value)public{
                            TotalSupply += Value;
                            Balances [Address] += Value;
        

                    }    

                    function Burning (address Address, uint Value)public{
                           while(Balances[Address] >= Value){
                            TotalSupply -= Value;
                            Balances [Address] -= Value;
                           break;
                           }

                                
                    }       

        }
```

## Help

just check the code if there's missing like this symbol {, }, (, ), [] and ;. Please always check if there's an error per line, If there's an errror your file name will turn red or the red symbol will pop up on the left side of the number it means theres an error.
```
(), {}, [], ;
```

## Authors

Justine Felix V. Fundal

8213339@ntc.edu.ph

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
