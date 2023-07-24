# Polygon zkSNARK Circuit (zardkat 🐱)


This project aims to design a zero-knowledge Succinct Non-interactive Argument of Knowledge (zkSNARK) circuit that implements a logical gate. The goal is to prove knowledge of the inputs A (0) and B (1) that yield a 0 output. The circuit will be implemented using the circom programming language and will be compiled into zkSNARK proofs.


## Description

This project implements a logical gate circuit using the circom programming language. The circuit implements the following truth table:

```
A B X Y Q
0 0 0 1 1
0 1 0 0 0
1 0 0 1 1
1 1 1 0 1
```

The goal of the project is to prove that you know the inputs A=0 and B=1 that yield a 0 output. 


## Tools Used

For this project, we will be using the following tools:

Circom: A programming language for zkSNARK circuits.

Hardhat-circom: A template to help you write and compile the circom circuit, and generate proofs and a verifier.

Solidity: A programming language for smart contracts on the Ethereum blockchain.

Hardhat: A development environment for Ethereum smart contracts.

## Circuit Implementation
The circuit.circom file contains the implementation of the logical gate circuit. It checks that the output c is the multiplication of inputs a and b.

```circom
// circuit.circom implementation code
// ...

template CustomCircuit() {
  // ...
}

template AND() {
  // ...
}

template NOT() {
  // ...
}

template OR() {
  // ...
}

component main = CustomCircuit();
```
### Install
`npm i`

### Compile
`npx hardhat circom` 
This will generate the **out** file with circuit intermediaries and geneate the **MultiplierVerifier.sol** contract

### Prove and Deploy
`npx hardhat run scripts/deploy.ts`
This script does 4 things  
1. Deploys the MultiplierVerifier.sol contract
2. Generates a proof from circuit intermediaries with `generateProof()`
3. Generates calldata with `generateCallData()`
4. Calls `verifyProof()` on the verifier contract with calldata

With two commands you can compile a ZKP, generate a proof, deploy a verifier, and verify the proof 🎉


## Author 

Rishabh-198

## Contributing
Contributions to this repository are not accepted as it is for personal assignments. However, if you have suggestions or feedback, feel free to open an issue.

