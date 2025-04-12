# DevToken (DVT)

DevToken es un token ERC-20 desplegado en la red Ethereum. Este proyecto fue creado como base para desarrollos futuros en la blockchain, aprendizaje de smart contracts y experimentación DeFi.

Lastimosamente la imagen no puede cargarse porque no puedo pagar la cantidad requerida para subirla, es un ejemplo de como deberia subirse la imagen pero todo el smart contract esta correctamente implementado.

---

## 🧠 Información del Token

- **Nombre:** DevToken  
- **Símbolo:** DVT  
- **Decimales:** 18  
- **Red:** SepoliaETH testnet  
- **Dirección del contrato:** [`0xde45ce5ac8c44cd431dc15ee625dc99c35c28b47`](https://etherscan.io/token/0xde45ce5ac8c44cd431dc15ee625dc99c35c28b47)

---

## 📄 Funcionalidades del Smart Contract

Este contrato incluye las siguientes funciones básicas de un token ERC-20:

- Transferencias entre direcciones
- Aprobaciones para gasto delegado
- Consulta de balances
- Total supply inicial definido

---

## 🔧 Herramientas utilizadas

- [Remix IDE](https://remix.ethereum.org/) para la escritura y despliegue
- MetaMask para firmar y publicar la transacción
- Solidity para la programación del contrato
- Ethereum Mainnet como red de despliegue

---

## 📝 Código del contrato (resumen)

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract DevToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("DevToken", "DVT") {
        _mint(msg.sender, initialSupply * 10 ** decimals());
    }
}
